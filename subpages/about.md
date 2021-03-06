The **International Conference on Microservices** is a forum for the discussion of all aspects of microservices: their design, programming, and operations. The 2020 edition of the conference (Microservices 2020) will take place in Bologna, Italy. Dates and venue will be announced shortly.


The conference's overarching aim is to bring together industry and academia, to foster discussion on practice and research of microservices. 

Microservices 2020 is part of a conference series started with [Microservices 2017](https://www.conf-micro.services/2017/index.html) which successfully brought together many international practitioners and researches interested in the software paradigm of microservices. During Microservices 2017 the [Microservices Community](https://microservices.community) was founded with the aims of sharing of knowledge, fostering of collaborations, and organising events around microservices.
Like Microservices 2019, this edition will be co-located and intertwined with the first international edition of the **Meeting on Microservices** (the [first national edition](http://www.italianasoftware.com/mom2016_eng.html) took place in Bologna, Italy), an event specifically oriented towards companies where invited speakers from industry report success stories, best practices, current challenges, and attendees participate to discussion panels on the adoption and evolution of microservices in production.

### Keynote Speakers

{% if site.data.keynotes %}
{% for keynote in site.data.keynotes %}
  <div class="panel panel-primary" style="display:inline-block; padding:10px; margin:10px; width: 30%">
    {% if keynote.picture %}
    <div class="row text-center">
    <img class="card-img" style="max-height:120px;max-width:120px;" src="{{ 'assets/images/speakers/' | append: keynote.picture | relative_url }}">
    </div>
    {% endif %}
    <div class="card-body">    
      {%- if keynote.title -%}
      {%- assign anchor = keynote.title | slugify -%}
      <h4 class="card-title"><a href="{{ 'keynotes/#' | append: anchor  | relative_url }}">{{keynote.title}}</a></h4>
      {%- endif -%}
      <p class="card-text">
      {%- if keynote.website -%}
        <a href="{{ keynote.website }}"> {{keynote.speaker}} </a>
      {%- else -%}
        {{keynote.speaker}}
      {%- endif -%}<br>
      {{keynote.affiliation}} </p>
      {% comment %}<a class="card-link" href="{{ 'keynotes/#' | append: anchor  | relative_url }}">Details</a>{% endcomment %}
    </div>
  </div>
{% endfor %}
{% else %}
TBA
{% endif %}

<div markdown="1">
### Microservices & Cyber Security

The general theme of Microservices 2020 is the interplay between microservices and cyber security.

On one hand, the adoption of microservices is fostering the adoption of new architectural styles and software construction paradigms; understanding the security properties (or the emerging vulnerabilities) of the resulting constructs calls for the development of a fresh mindset in analysts and testers alike.
In addition, the additional middleware layers often proposed for the management of microservice-based architectures could expand the attack surface of the systems.
On the other hand, the same frameworks could instead prove valuable allies to collect security-relevant information and to coordinate defenses.

These considerations are about the intrinsic interplay between the fields of microservices and security. However, it should be noted that the context is peculiarly sensitive to them. Microservices are adopted as an accelerator of Digital Transformation, as the successful past edition of the conference  proved, and security issues should be a primary concern, possibly taking the chance to integrate security-by-design into the microservice-led revolution in software development.

Microservices welcomes both theoretical and experimental submissions on topics ranging from formal frameworks to industrial experience reports and demonstrations. Presentations will be selected based on abstract submissions of maximum two pages. See the <a class="link-to-tab" href="#call-for-papers">call for papers</a> for details.
</div>