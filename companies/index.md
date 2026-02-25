---
layout: default
title: Companies - Ruby Singapore
description: Companies in Singapore using Ruby and supporting the RubySG community.
---
{% include site_header.html %}

<main>
  <section class="section">
    <div class="wrap">
      <div class="page-header-row">
        <h2 class="heading-center">Our Community Supporters! Thank you! &#10084;</h2>
        <a class="back-link" href="/">&larr; Back home</a>
      </div>
      <p class="center section-intro">These companies have recently sponsored RubySG meetups and/or provided speakers</p>
      <div class="company-grid">
        {% for company in site.data.companies.supporters %}
          {% include company_card.html company=company %}
        {% endfor %}
      </div>
    </div>
  </section>

  <section class="section">
    <div class="wrap">
      <h2 class="heading-center">More Companies Using Ruby</h2>
      <div class="company-grid">
        {% for company in site.data.companies.more_companies %}
          {% include company_card.html company=company %}
        {% endfor %}
      </div>
    </div>
  </section>

  <section class="section">
    <div class="wrap">
      <p class="center note">
        More Ruby jobs in Singapore
        <a href="{{ site.data.companies.more_jobs_url }}" target="_blank" rel="noopener noreferrer">here</a>!
      </p>
    </div>
  </section>
</main>

{% include site_footer.html %}
