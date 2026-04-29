---
layout: page
permalink: /fieldwork/
title: fieldwork
description: 
nav: true
nav_order: 7
---

<style>
  .fieldwork-page {
    color: var(--global-text-color);
  }

  .fieldwork-page .section-title,
  .fieldwork-page .section-subtitle,
  .fieldwork-page .quote,
  .fieldwork-page .quote-author,
  .fieldwork-page p,
  .fieldwork-page li,
  .fieldwork-page .bold {
    color: inherit;
  }

  .fieldwork-page a {
    color: var(--global-theme-color);
  }

  .fieldwork-page .quote {
    font-style: italic;
    font-size: 1.1em;
    border-left: 4px solid var(--global-divider-color);
    padding-left: 20px;
    margin: 20px 0;
  }

  .fieldwork-page .quote-author {
    font-style: normal;
    display: block;
    margin-top: 10px;
  }

  .fieldwork-page .highlight {
    background-color: var(--global-code-bg-color);
    padding: 2px 4px;
  }

  .fieldwork-page .section {
    margin-top: 40px;
  }

  .fieldwork-page .section-header {
    text-align: center;
    margin-bottom: 30px;
  }

  .fieldwork-page .section-title {
    font-size: 1.5em;
    font-weight: bold;
    margin: 0;
  }

  .fieldwork-page .section-subtitle {
    font-size: 1.2em;
    margin: 5px 0 0;
  }

  .fieldwork-page .bold {
    font-weight: bold;
  }

  .fieldwork-page .image-gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: 20px;
    margin-bottom: 20px;
  }

  .fieldwork-page .image-gallery img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }

  @media (max-width: 768px) {
    .fieldwork-page .section-title {
      font-size: 1.3em;
    }
    .fieldwork-page .section-subtitle {
      font-size: 1.1em;
    }
    .fieldwork-page .image-gallery {
      grid-template-columns: 1fr;
    }
  }

  .fieldwork-page .logo-row {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: nowrap;
    margin: 20px 0;
  }

  .fieldwork-page .logo-row img {
    max-width: 22%;
    height: auto;
    object-fit: contain;
    background-color: #fff;
    padding: 5px;
    border-radius: 5px;
  }

  @media (max-width: 768px) {
    .fieldwork-page .logo-row {
      flex-wrap: wrap;
    }
    .fieldwork-page .logo-row img {
      max-width: 45%;
      margin-bottom: 10px;
    }
  }

  .fieldwork-page .acknowledgment {
    margin-top: 50px;
    padding: 20px;
    background-color: var(--global-card-bg-color);
    border-top: 1px solid var(--global-divider-color);
    font-size: 0.9em;
  }

  .fieldwork-page .appreciation {
    margin-top: 50px;
    padding-top: 20px;
    border-top: 1px solid var(--global-divider-color);
    font-size: 0.9em;
    line-height: 1.6;
  }

  .fieldwork-page .appreciation a {
    text-decoration: none;
  }

  .fieldwork-page .appreciation a:hover {
    text-decoration: underline;
  }
</style>

<div class="fieldwork-page">

<div class="quote">
  "Introducing innovation and reform is not easy, because change inevitably confronts established sets of ideas, practices, relationships, and results… We have learned that <span class="bold">locally-led</span> development is more likely to be sustained when it alters incentives and institutions."
  <span class="quote-author">— United States Agency for International Development (USAID)</span>
</div>

<div class="section">
  <div class="section-header">
    <h2 class="section-title">Deploying Machine Learning for Medicine Allocation in Sierra Leone</h2>
    <p class="section-subtitle">-- Improving Access to Maternal &amp; Child Health Products</p>
  </div>
  
  <p>In collaboration with National Medical Supplies Agency (NMSA) and Ministry of Health and Sanitation (MoHS) in Sierra Leone, we've developed and deployed a machine learning framework to enhance the efficient allocation of essential medicines for women and children under five. Check <a href="https://analytics.wharton.upenn.edu/news/research-spotlight-angel-chung/?fbclid=IwAR3iEks2-Xu9e03F8BeeZw2NRHL3oUYOjHJ0QgvPmvVCk-7iuM65VDqpEss_aem_AVVmrYAwtwUrDmd0pjIE75g59MS9TR_eI51F8SolsVR1zjt0v6LpkrY3Z3w3z4G7rTXoIWw3BiO_aes-egehzpZh">Analytics at Wharton's Research Spotlight</a> on this work.</p>
  
  <div class="image-gallery">
    <img src="/assets/img/SLTruck.png" alt="Sierra Leone Fieldwork 2">
    <img src="/assets/img/SLWarehouse.png" alt="Sierra Leone Fieldwork 3">
    <img src="/assets/img/SLMalaria.png" alt="Sierra Leone Fieldwork 4">
    <img src="/assets/img/SLMeeting.jpg" alt="Sierra Leone Fieldwork 5">
  </div>
</div>

<div class="section">
  <div class="section-header">
    <h2 class="section-title">Generative AI for Public Health in Somaliland</h2>
  </div>
  
  <p>In collaboration with the Ministry of Health and Development (MoHD) in Somaliland and Taiwan International Cooperation Development Fund (ICDF), we are developing effective and safe AI methodologies to improve healthcare accessibility, quality, and efficiency in this resource-constrained environment.</p>
  
  <div class="image-gallery">
    <img src="/assets/img/SomalilandHGH.jpg" alt="Somaliland Fieldwork 1">
    <img src="/assets/img/SomalilandMoHMeeting.jpg" alt="Somaliland Fieldwork 2">
    <img src="/assets/img/SomalilandMoHS.jpg" alt="Somaliland Fieldwork 3">
    <img src="/assets/img/SomalilandNCD.jpg" alt="Somaliland Fieldwork 4">
  </div>
</div>

<div class="section">
  <div class="section-header">
    <h2 class="section-title">Generative AI for Education in Indonesia & Taiwan</h2>
  </div>
  
  <p>In collaboration with schools and governments, we are developing GenAI-driven adaptive learning systems to improve educational outcomes.</p>
  
  <div class="logo-row">
    <img src="/assets/img/NTU.png" alt="NTU Logo">
    <img src="/assets/img/BINUS.jpeg" alt="BINUS Logo">
    <img src="/assets/img/DoE.png" alt="DoE Logo">
    <img src="/assets/img/AIC.png" alt="AIC Logo">
  </div>
</div>

<div class="appreciation">
  <p>We sincerely appreciate the support from the following organizations to enable transformative impact of research in real-world practice: 
  <a href="https://global.upenn.edu/grants/">Penn Global</a>, 
  <a href="https://ai-analytics.wharton.upenn.edu/wharton-healthcare-analytics-lab/">Wharton Healthcare Analytics Lab</a>, 
  <a href="https://ai-analytics.wharton.upenn.edu">Wharton AI & Analytics Initiative</a>, 
  <a href="https://global.wharton.upenn.edu">Wharton Global Initiatives</a>, 
  <a href="https://mackinstitute.wharton.upenn.edu">Mack Institute for Innovation Management</a>, 
  <a href="https://www.tanotofoundation.org/en/">Tanoto ASEAN Initiative</a>.</p>
</div>

</div>
