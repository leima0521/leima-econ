<h3 id="publications" style="margin: 2px 0px -15px;">Work In Progress</h3>

<div class="publications">
<ol class="bibliography">

{% for link in site.data.publications.main %}

<li>
<div class="pub-row">
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 0px;">
      <div class="title"><a>{{ link.title }}</a></div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.authors or link.abstract %}
        <div class="author">
        {% if link.authors %} 
          {{ link.authors }}
        {% endif %}
        {% if link.abstract %} 
          <button id="{{ link.id }}" onClick="reply_click()" class="accordion"> Abstract </button>
        {% endif %}
        </div>
      {% endif %}
      {% if link.others %} 
        {{ link.others }}
      {% endif %}
      <div id="{{ link.id }}" class="panel" style="background-color: #F1F1F1; color: #666; padding: 10px;">
    {{ link.abstract }}
  </div>
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>

