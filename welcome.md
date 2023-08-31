---
layout: default
---

<script>
  window.onload = function() {
    var username = localStorage.getItem('username');
    if (username) {
      var userElement = document.getElementById('user-name');
      if (userElement) {
        userElement.textContent = username;
      }
    }
  };
</script>

Welcome, <span id="user-name"></span>!