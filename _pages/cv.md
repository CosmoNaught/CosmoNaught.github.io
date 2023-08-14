---
layout: archive
title: "Bio"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

## Professional Experience
------
### Technical Analyst – Machine Learning & Complex Systems
*Imperial College London, U.K. (2023 – Ongoing)*
- Championed evidence-based advocacy, influencing global policies on malaria prevention strategies.
- Engineered machine learning algorithms, focusing on Gaussian Processes and Neural Network emulators, to study malaria dynamics in Africa.
- Led research projects emphasizing statistical evaluations of bed net strategies for malaria control, revealing potential improvements via data-driven approaches.
  
### Research Scientist – Machine Learning & Applied Mathematics
*German Centre for Artificial Intelligence (DFKI), DE (2022 – 2023)*
- Spearheaded research using Deep Neural Networks for complex system modelling, including predictive tumour growth tools using Deep Neural Universal Differential Equations.
- Extended machine learning tools to model criminal behaviour and gun violence dispersion.
- Advocated and practiced AI ethics and safety in all research dimensions.
- Enhanced modelling techniques using open-source frameworks like SciML and TuringLang.

### Research Assistant – COVID-19 Real Time Modelling
*Imperial College London, U.K. (2021 – 2023)*
- Awarded the “SPI-M-O Award for Modelling and Data Support” presented by the UK Government’s Chief Scientific and Medical Officers.
- Produced comprehensive weekly reports for SPI-M-O & SAGE during the COVID-19 pandemic.
- Developed models for infectious disease transmission.
- Supervised open-source package developments, ensuring rigorous statistical consistency.

### MRC GIDA Internal Seminar Series Co-Organiser
*Imperial College London, U.K. (2023 – Ongoing)*
- Orchestrated weekly seminar events, promoting intellectual discussions among department members.
  
Education
======
### MSc Epidemiology 
*Imperial College London, U.K. (2020 – 2021)*
  * Notable Modules; Advanced Regression, Bayesian Modelling for Spatial and Spatio-temporal Data, Research Methods, Introduction to Statistical Thinking and Data Analysis, Further Methods in Infectious Disease Modelling, Outbreaks
  * Dissertation Project; “Investigating co-existence dynamics of plankton biotic resistance on Batrachochytrium dendrobatidis as a food-web based ecological management strategy for mountainous aquatic ecosystems.”
  
### BSc Mathematics with Economics
*Aston University, U.K. (2015 – 2019)*
  * Notable Modules; Statistical Machine Learning, Partial Differential Equations, Numerical Methods (I & II), Mathematical Algorithms
  * Dissertation Project; "From Concept to Simulation: Designing and Conducting CFD Analysis on Auger Reactors through Granular and Volumetric Approaches"

Technical Skills & Languages
======
* Programming: R, Python, Julia, C#/C++, SQL, Matlab, SAS, Latex
* Research Software: PyTorch, TensorFlow, Keras, RStan, Julia SciML, TuringLang
* Software Management: Git Version Control, Bash Shell Scripting (Linux/Unix)
* Languages: Fluent in English & Spanish, Working proficiency in German & French

Publications & References
======
* Publications:
  * Imai, N., Rawson, T., et. al., [Quantifying the impact of delaying the second COVID-19 vaccine dose in England](https://doi.org/10.1016/S2468-2667(22)00337-1).
  * Perez-Guzman, P. N., Knock, E., et. al., [Epidemiological drivers of transmissibility and severity of SARS-CoV-2 in England](https://doi.org/10.1038/s41467-023-39661-5).

* Manuscripts in Preparation:
  * "Applying Neural Network Emulation to Assess the Impact of Pyrethroid-Pyrrole Bed Nets on Malaria in Africa."
  * "Applying Deep Neural Universal Differential Equations: A Novel Approach for Tumour Volume Growth in Complex Mathematical Systems."
  * "Investigating Parameterisation and Inference Trade-Offs in Stochastic and Deterministic Models."

* Software & Tools:
  * [siremu](https://github.com/epiyasin/siremu); A (WIP) Python Package for Epidemic Simulation and Emulation utilising advanced Neural Network architectures.
  * [sircovid](https://mrc-ide.github.io/sircovid/); Tools to perform Bayesian analysis of complex stochastic models using adaptive Metropolis-Hastings and particle MCMC.
  * [spimalot](https://mrc-ide.github.io/spimalot/); The models in this package can be used to estimate key epidemic parameters and predict the course of the epidemic under different intervention scenarios.
  * [MCState](https://mrc-ide.github.io/MCstate/); Allows users to infer parameters for stochastic, compartmental models from data, using Monte Carlo methods.

Conferences & Presentations
======
* **Upcoming Conferences**:
  * 9th International Conference on Infectious Disease Dynamics, Bologna, Italy, November 2023
    * "Evaluating improved malaria control by switching to pyrethroid-pyrrole insecticide treated nets in Africa"
    * "Investigating Parameterisation and Inference Trade-Offs in Stochastic and Deterministic Epidemic Models"

* **Past Presentations**:
  * MRC GIDA Seminars, London, U.K., December 2022
    * Topic: Parameterisation and Inference in Epidemic Models

Teaching
======
{% assign teaching_posts_grouped_by_venue = site.teaching | group_by: "venue" %}

<ul>

{% assign imperial_posts = site.teaching | where: 'venue', "Imperial College London, Department of Infectious Disease Epidemiology" %}
{% if imperial_posts.size > 0 %}
  <li><strong>Imperial College London, Department of Infectious Disease Epidemiology</strong>
    <ul>
      {% for post in imperial_posts %}
        <li>{% include archive-single-cv.html %}</li>
      {% endfor %}
    </ul>
  </li>
{% endif %}

{% for venue_group in teaching_posts_grouped_by_venue %}
  {% unless venue_group.name == "Imperial College London, Department of Infectious Disease Epidemiology" %}
    <li><strong>{{ venue_group.name }}</strong>
      <ul>
        {% assign posts_sorted_by_date = venue_group.items | sort: 'date' | reverse %}
        {% for post in posts_sorted_by_date %}
          <li>{% include archive-single-cv.html %}</li>
        {% endfor %}
      </ul>
    </li>
  {% endunless %}
{% endfor %}

</ul>

Voluntary & Leadership
======
* Authored '30 Machine Learning Algorithms in 30 Days', an interactive educational series, 2023 – Ongoing
* MSc. Epidemiology Graduate Teaching Assistant, Imperial College London, U.K., 2021 – 2022
* NHS COVID-19 Clinical Vaccinator, NHS England, U.K., 2021
* Lay Grant Reviewer, Parkinson’s UK, U.K., 2019 – Ongoing
* BSc. Mathematics Undergraduate Teaching Assistant, Aston University, U.K., 2017 – 2019
* Engineering and Applied Sciences Research Assistant (Year in Industry), Aston University, U.K., 2017 – 2018

