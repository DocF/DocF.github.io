<h2 id="publications">Publications</h2>

<div class="publications">
<ol class="bibliography publication-list">

{% for link in site.data.publications.main %}

<li class="publication-item">
  <div class="publication-meta">
    {% if link.year %}
    <span class="publication-year">{{ link.year }}</span>
    {% endif %}
    {% if link.cas_zone %}
    <span class="cas-zone">{{ link.cas_zone }}</span>
    {% endif %}
  </div>
  <div class="publication-body">
    <div class="title">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" target="_blank" rel="noopener">{{ link.title }}</a>
      {% else %}
      {{ link.title }}
      {% endif %}
    </div>
    <div class="author">{{ link.authors }}</div>
    <div class="periodical"><em>{{ link.conference }}</em></div>
    <div class="links">
      {% if link.pdf %}
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Paper</a>
      {% endif %}
      {% if link.code %}
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Code</a>
      {% endif %}
      {% if link.page %}
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">Project Page</a>
      {% endif %}
      {% if link.bibtex %}
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener">BibTeX</a>
      {% endif %}
      {% if link.notes %}
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %}
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</li>

{% endfor %}

</ol>
</div>
