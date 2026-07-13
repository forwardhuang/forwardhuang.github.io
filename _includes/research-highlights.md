<br>
<h2 id="research-highlights" class="section-title">Research Highlights</h2>

<div class="publications publication-highlights research-highlights">
  <ol class="bibliography highlight-list">
    {% for highlight in site.data['research-highlights'].items %}
    <li>
      <article class="highlight-card">
        <div class="highlight-visual">
          {% if highlight.image != "" %}
          <img src="{{ highlight.image }}" alt="{{ highlight.image_alt }}" loading="lazy" decoding="async">
          {% else %}
          <div class="highlight-image-placeholder" aria-hidden="true"></div>
          {% endif %}
        </div>
        <div class="highlight-content">
          <h3 class="highlight-title">{{ highlight.title }}</h3>
          <p class="highlight-summary">{{ highlight.summary }}</p>
          <div class="highlight-actions">
            {% if highlight.slides != "" %}<a href="{{ highlight.slides }}" target="_blank" rel="noopener">Slides</a>{% else %}<span aria-disabled="true">Slides</span>{% endif %}
            {% if highlight.video != "" %}<a href="{{ highlight.video }}" target="_blank" rel="noopener">Video</a>{% else %}<span aria-disabled="true">Video</span>{% endif %}
          </div>
        </div>
      </article>
    </li>
    {% endfor %}
  </ol>
</div>
