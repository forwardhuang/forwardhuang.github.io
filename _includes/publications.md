<br>
<h2 id="publications" class="section-title">Publications</h2>

<p class="publication-note">
  A complete and automatically updated publication record is available on
  <a href="https://scholar.google.com/citations?user=8Q6n2YoAAAAJ&hl=en" target="_blank" rel="noopener">Google Scholar</a>.
</p>

<h3 class="subsection-title">Highlighted Publications</h3>

<div class="publications publication-highlights">
  <ol class="bibliography highlight-list">
    {% for link in site.data.publications.main %}
    {% if link.image %}
    <li>
      <div class="pub-row highlight-card">
        <div class="col-sm-3 abbr pub-media">
          <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" alt="Publication teaser">
          {% if link.conference_short %}
          <abbr class="badge">{{ link.conference_short }}</abbr>
          {% endif %}
        </div>
        <div class="col-sm-9 pub-content">
          <div class="title"><a href="{% if link.code %}{{ link.code }}{% elsif link.pdf %}{{ link.pdf }}{% else %}#{% endif %}">{{ link.title }}</a></div>
          <div class="author">{{ link.authors }}</div>
          <div class="periodical"><em>{{ link.conference }}</em></div>
          <div class="links">
            {% if link.pdf %}
            <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">DOI / Link</a>
            {% endif %}
            {% if link.code %}
            <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">PDF</a>
            {% endif %}
            {% if link.page %}
            <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Project Page</a>
            {% endif %}
            {% if link.bibtex %}
            <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">BibTeX</a>
            {% endif %}
            {% if link.notes %}
            <strong><i>{{ link.notes }}</i></strong>
            {% endif %}
            {% if link.others %}
            {{ link.others }}
            {% endif %}
          </div>
        </div>
      </div>
    </li>
    {% endif %}
    {% endfor %}
  </ol>
</div>

<h3 class="subsection-title">Publication List</h3>

<div class="publication-list-panel">
  <ol class="publication-list citation-list">
    {% for link in site.data.publications.main %}
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
  </ol>
</div>
