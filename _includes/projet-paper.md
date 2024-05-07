<h2 id="publications" style="margin: 2px 0px -15px;">Projects&papers</h2>

<div class="publications">
<ol class="bibliography">

{% for item in site.data.project-paper.main %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ item.image }}" class="teaser img-fluid z-depth-1" style="width:200px;height:auto;">
    {% if item.conference_short %} 
    <abbr class="badge">{{ item.conference_short }}</abbr>
    {% endif %}
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 15px;">
      <div class="title"><a href="{{ item.pdf | default: item.page | default: item.code }}">{{ item.title }}</a></div>
      <div class="author">{{ item.authors }}</div>
      <div class="periodical"><em>{{ item.conference }}</em></div>
      <div class="comment">{{ item.comment }}</div>
    <div class="links">
      {% if item.pdf %} 
      <a href="{{ item.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if item.code %} 
      <a href="{{ item.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if item.page %} 
      <a href="{{ item.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if item.github %} 
      <a href="{{ item.github }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Github</a>
      {% endif %}
      {% if item.bibtex %} 
      <a href="{{ item.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if item.notes %} 
      <strong> <i style="color:#e74d3c">{{ item.notes }}</i></strong>
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>
