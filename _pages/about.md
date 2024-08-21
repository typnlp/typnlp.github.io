---
layout: about
title: Home
permalink: /
subtitle:

profile:
  align: left
  image: typnlp.png
  image_circular: true # crops the image to make it circular

news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: true # includes social icons at the bottom of the page

groups: [staff, support]
staff:
  title: Research Staff
  people:
    - name: Johannes Bjerva
      description: Associate Professor <br> Head of TypNLP
      website: https://bjerva.github.io/
      picture: people/Johannes.jpg
    - name: Heather Lent
      description: Postdoc (2022–)
      website: https://vbn.aau.dk/da/persons/154463/
      picture: people/Heather.jpg
    - name: Mike Zhang
      description: Postdoc (2024–)
      website: https://jjzha.github.io/
      picture: people/Mike.jpg
    - name: Russa Biswas
      description: Postdoc (2024–)
      website: https://vbn.aau.dk/da/persons/rubi
      picture: people/Russa.png
    - name: Yiyi Chen
      description: PhD Fellow (2022–)
      website: https://siebeniris.github.io/
      picture: people/Yiyi.jpg
    - name: Marcell Fekete
      description: PhD Fellow (2022–)
      website: https://vrmer.github.io/
      picture: people/Marcell.jpg
    - name: Esther Ploeger
      description: PhD Fellow (2022–)
      website: https://vbn.aau.dk/en/persons/155453/
      picture: people/Esther.jpg
    - name: Ernests Lavrinovićs
      description: PhD Fellow (2024–)
      website: https://ernlavr.github.io/
      picture: people/Ernests.jpg
    - name: Rasmus Jensen
      description: Industrial PhD Fellow (2024–)
      website: https://vbn.aau.dk/da/persons/rtaj
      picture: typnlp-5.png

---

  <h1><b>TypNLP</b> Research Lab</h1>

  Welcome to the TypNLP research lab at the Data, Knowledge, and Web Engineering group 
  at Aalborg University led by <a href="https://bjerva.github.io/">Associate Professor Johannes Bjerva</a>. 
  The lab engages in research in Natural Language Processing (NLP), with interdisciplinary overlap in Education 
  and Cybersecurity. Our scope revolves around leveraging linguistic synergies between languages to develop robust 
  NLP models and building NLP applications that aid multiple domains outside of NLP.

  <div class="projects">
    <h2 class="category">News</h2>
      {% include news.liquid %}

  {%- for group in page.groups -%}
  <h2 class="category">{{page.[group].title}}</h2>
    <div class="grid">
      {%- for person in page.[group].people -%}
          <article class="grid-item card">
            {% if person.picture -%}
              <img class="avatar" src="/assets/img/{{person.picture}}" alt="Portrait ({{person.name}})" width="auto" height="auto">
            {%- else -%}
              <img class="avatar" src="/assets/img/typnlp.png" alt="Portrait ({{person.name}})" width="auto" height="auto">
            {%- endif -%}
          <div class="card-body">
            <!-- <h2 class="card-title">{{person.name}}</h2> -->
            <h2 class="card-title">
              {% if person.website -%}
                <a href="{{person.website}}">{{person.name}}</a>
              {%- else -%}
                {{person.name}}
              {%- endif -%}
            </h2>
            <div class="card-text">
              {{person.description}}
              </div>
            </div>
          </article>
      {%- endfor -%}
    </div>
  {%- endfor -%}

 <h2 class="category">Alumni</h2>
  <ul>
    <li>Hans Heje (Research Assistant, 2023–2024)</li>
  </ul>

  <h2 class="category">Job Openings</h2>
  Join us! <a href="/jobs">→Open positions</a>