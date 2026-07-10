<br>
<h2 id="publications" class="section-title">Selected Papers</h2>

{% assign publication_categories = "AI for Power Electronics|Wireless Power Transfer|Other Power Electronics|Wave Energy Converters" | split: "|" %}

<div class="publication-groups">
  {% for category in publication_categories %}
  {% assign category_publications = site.data.publications.main | where: "category", category %}
  {% if category_publications.size > 0 %}
  <section class="publication-category">
    <h3 class="publication-category-title">{{ category }}</h3>
    <ul class="publication-list citation-list">
      {% for link in category_publications %}
      <li>
        <span class="citation-text">
          {% if link.citation %}
          {{ link.citation }}
          {% else %}
          {{ link.authors }}, "{{ link.title }}," <em>{{ link.conference }}</em>.
          {% endif %}
        </span>
        <span class="citation-links">
          {% if link.pdf %}<a class="citation-icon doi-icon" href="{{ link.pdf }}" target="_blank" rel="noopener" aria-label="DOI link">DOI</a>{% endif %}
          {% if link.code %}<a class="citation-icon pdf-icon" href="{{ link.code }}" target="_blank" rel="noopener" aria-label="PDF">PDF</a>{% endif %}
          {% if link.page %}<a class="citation-icon page-icon" href="{{ link.page }}" target="_blank" rel="noopener" aria-label="Project page">PAGE</a>{% endif %}
          {% if link.bibtex %}<a class="citation-icon bib-icon" href="{{ link.bibtex }}" target="_blank" rel="noopener" aria-label="BibTeX">BIB</a>{% endif %}
        </span>
      </li>
      {% endfor %}
    </ul>
  </section>
  {% endif %}
  {% endfor %}
</div>
