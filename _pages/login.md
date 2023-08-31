---
layout: none
title: Login
permalink: /login/
description: 
nav: false
nav_order: 7
horizontal: false
---

<style>
  body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }
  
  .centered-div {
    background-color: lightgray;
    padding: 20px;
  }
</style>

<script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.min.js"></script>


<script>
function test_pwd(pwd){
    var cor_hash = "ea6e060c7ef219fa26bedd023b843610";
    var hash = CryptoJS.MD5(pwd).toString();
    if (hash ==  cor_hash){
        return true;
    }else{
        return false;
    }
}

function testCookieValue(cookieName, expectedValue) {
  var cookies = document.cookie.split(';');
  for (var i = 0; i < cookies.length; i++) {
    var cookie = cookies[i].trim();
    if (cookie.indexOf(cookieName + '=') === 0) {
      var cookieValue = cookie.substring(cookieName.length + 1);
      if (cookieValue === expectedValue) {
        return true;
      }
    }
  }
  return false;
}

function setCookie(cookieName, cookieValue, expirationDays, domain) {
  var date = new Date();
  date.setTime(date.getTime() + (expirationDays * 24 * 60 * 60 * 1000));
  var expires = "expires=" + date.toUTCString();
  var cookieString = cookieName + "=" + cookieValue + ";" + expires + ";path=/";

  if (domain) {
    cookieString += ";domain=" + domain;
  }

  document.cookie = cookieString;
}

function on_click_unlock(ctrl_id, alert_id){
    var url = "{{ '/' | relative_url }}";
    var p_pwd = document.getElementById(ctrl_id);
    var p_alt = document.getElementById(alert_id);
    if (test_pwd(p_pwd.value)){
        setCookie('Unlock_SOIREE', 'True', 3);
        window.location.href = url;
    }else{
        p_alt.style.display = "block";
        p_alt.value = 'Password is incorrect! Please try again!';
        return false;
    }
}

function deleteCookie(cookieName) {
  document.cookie = cookieName + "=; expires=Thu, 01 Jan 1970 00:00:00 UTC; path=/;";
}

function on_click_lock(ctrl_id, alert_id){
    var p_pwd = document.getElementById(ctrl_id);
    var p_alt = document.getElementById(alert_id);
    deleteCookie('Unlock_SOIREE');
    p_alt.style.display = "none";
    p_alt.value = '';
    return True;
}
</script>

<!-- body for login page -->

<div id="centered-div">
<div>
<h2>Welcome to Laviebay</h2>
<img src="../assets/img/bagua_gorden_blue.jpg" style="width: 400px; height: 400px;" />
</div>

<div id="login_div">
    <label for="pwd">Please input password to access to Laviebay</label><br>
    <input id="pwd" type="password" style="width: 200px;"><br>
    <input id="alert" type="text" readonly style="width: 600px; display:none; color: red; border: none;"><br>
    <input type="button" value="Unlock" onclick='return on_click_unlock("pwd", "alert");'><br>
    <!-- <input type="button" value="Lock" onclick='return on_click_lock("pwd", "alert");'> -->
</div>

</div>