---
title: Ruby Singapore
---
{% include site_header.html %}

<main>
  <section class="section">
    <div class="wrap-narrow">
      <h2 class="heading-with-line">Every 1st Wednesday of the Month</h2>
      <p>We hold meetups with speakers giving talks about Ruby and share 5 random Ruby tips. Building &amp; shipping is how we roll. It&apos;s a great way to meet Ruby enthusiasts!</p>
      <div class="actions">
        {% for button in site.data.home.meetup_buttons %}
          <a class="{{ button.class_name }}" href="{{ button.url }}" target="_blank" rel="noopener noreferrer">{{ button.label }}</a>
        {% endfor %}
      </div>
    </div>
  </section>

  <section class="section section-blue">
    <div class="wrap-narrow">
      <h2 class="heading-center">Chat with us on Telegram</h2>
      <div class="qr-block">
        <img src="/assets/images/telegram-qr.png" alt="RubySG Telegram QR code" width="220" height="220" />
      </div>
      <p class="center"><a class="btn" href="{{ site.data.home.telegram_url }}" target="_blank" rel="noopener noreferrer">Join Telegram</a></p>
    </div>
  </section>

  <section class="section">
    <div class="wrap-narrow">
      <h3 class="heading-with-line">Looking for Ruby jobs?</h3>
      <p>These Singapore companies use Ruby and they may be hiring.</p>
      <div class="logo-grid">
        {% for company in site.data.companies.supporters limit: 8 %}
          <a class="logo-tile" href="{{ company.url }}" target="_blank" rel="noopener noreferrer">
            {% if company.logo_url %}
              <img src="{{ company.logo_url }}" alt="{{ company.logo_alt }}" loading="lazy" />
            {% else %}
              <span>{{ company.logo_fallback }}</span>
            {% endif %}
          </a>
        {% endfor %}
      </div>
      <p class="center"><a class="btn" href="/companies/">See more</a></p>
    </div>
  </section>

  <section class="section section-gray">
    <div class="wrap-narrow center">
      <h3 class="heading-center heading-with-line">Visiting Singapore?</h3>
      <img class="hero-image" src="/assets/images/skyline.png" alt="Singapore skyline illustration" />
      <p>We have prepared a guide for visiting Rubyists. Check out <a href="{{ site.data.home.visit_guide_url }}" target="_blank" rel="noopener noreferrer">the guide on GitHub</a> and feel free to reach out to us!</p>
    </div>
  </section>
</main>

{% include site_footer.html %}
