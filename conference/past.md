---
layout: default
title: "Past Music Encoding Conferences"
---

# Past Music Encoding Conferences

{% assign c = site.conferences | where:"role","about" | sort: "date" | reverse %}

<div class="columns">
  {% for conference in c %}

    <div class="column col-4 col-sm-12 col-lg-6 conferences">
      <div class="card project">
        <div class="card-image">
          {% if conference.image %}
            <img class="mei-project-image img-fit-cover" src="{{ site.baseurl }}/images/{{ conference.image }}"/>
          {% else %}
            <div class="hero hero-sm bg-primary text-light">
              <div class="hero-body">
                <h1>{{ conference.tag }}</h1>
              </div>
            </div>
          {% endif %}
        </div>
        <div class="card-header">
            <div class="card-title h5">
                {{ conference.title }}
            </div>
            <div class="card-subtitle text-gray">
              {% if conference.subtitle !="" %}
                {{ conference.subtitle }}
                <br/>
              {% endif %}
              {{ conference.venue }}
            </div>
        </div>
        <div class="card-footer">
            <a class="btn float-right btn-sm" href="{{conference.permalink}}">More…</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>
