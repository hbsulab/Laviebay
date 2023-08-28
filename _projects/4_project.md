---
layout: page
title: Drug Design
description: Explore Potential Inhibitors for Proteins
img: assets/img/drug_design_project/CADD.jpg
importance: 3
category: work
giscus_comments: true
---

<h4 style="text-align: left;"><strong>Molecular Docking</strong></h4>
<hr>

<div class="row">
    <div class="col-lg-7">
        Molecular docking is a computer technique that simulates the interaction process between small molecule drugs and biological macromolecules (such as proteins). This process mainly considers the shape and charge matching of the binding pocket between the drug molecule and the target protein, and predicts the optimal position and posture of the drug molecule in the binding pocket by optimizing the energy score function.  <br>
    </div>
    <div class="col-lg-5 mt-3 mt-md-0">
        {% include figure.html path="assets/img/drug_design_project/docking.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<br>


<h4 style="text-align: left;"><strong>Free Energy Calculation</strong></h4>
<hr>

<div class="row">
    <div class="col-lg-7 mt-3 mt-md-0">
        {% include figure.html path="assets/img/drug_design_project/FEP.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-lg-5">
        In protein-ligand systems, alchemical methods are often used to model the progression of ligands from the dissociated state to the bound state. In this case, the alchemical method uses <strong> Lagrange multipliers (λ) </strong> to adjust the potential energy function of the ligand, thus simulating a "smooth" transition between the dissociated and bound states of the ligand. Different λ values correspond to different ligand states, ranging from complete dissociation (λ=0) to complete binding (λ=1).
    </div>
</div>
<br>

The Binding Free Energy can be calculated using <strong> Thermodynamic Integration (TI) </strong> or <strong> Free Energy Perturbation (FEP) </strong>. Both methods are based on the principles of thermodynamics, but differ in practice. In thermodynamic integration, the derivative of the mean potential energy of the system at each λ value is integrated to calculate the binding free energy. The advantage of this method is that the results are accurate, but it is computationally expensive because all lambda values need to be integrated. The FEP is calculated by comparing the energies of the system at adjacent λ values. The FEP method generally requires fewer sampling times than the TI method, but may be more sensitive to the choice of λ values.<br>

Overall, enhanced sampling (alchemical method), TI, and FEP are powerful tools for computational chemistry that can be used to predict the free energy of protein-ligand binding, thereby helping to understand the nature of molecular interactions and design new drug molecules.<br>

$$
\Delta{G_{b}^o} = -\Delta{G_{elec+vdW+restr}^{prot}} + \Delta{G_{elec+vdW}^{solv}} + \Delta{G_{restr}^{solv}}
$$

{% include figure.html path="assets/img/drug_design_project/FEP_result.jpg" title="example image" class="img-fluid rounded z-depth-1" %}


<br>