---
layout: home
---

<div class="alert alert-info hidden-print" role="alert"><span class="glyphicon glyphicon-info-sign"></span> Due to the ongoing COVID-19 situation, Microservices 2020 will take place as a virtual meeting. All the information regarding the conference (scheduling, platform, etc.) will be published on this website as soon as possible. </div>

<ul class="nav nav-tabs nav-justified">
  <li role="presentation" class="active"><a href="#about">About</a></li>
  <li role="presentation" id="cfp_tab"><a href="#call-for-papers">Call for Papers</a></li>
  <li role="presentation" id="submission_tab"><a href="#submission">Submission</a></li>
</ul>

<div class="tab-content">
<div role="tabpanel" class="tab-pane active" id="about">
  {% include_relative include_md.html file="subpages/about.md" %}
</div>

<div role="tabpanel" class="tab-pane" id="call-for-papers">
  {% include_relative include_md.html file="subpages/call_for_papers.md" %}
</div>

<div role="tabpanel" class="tab-pane" id="submission">
{% include_relative include_md.html file="subpages/submission.md" %}
</div>
</div>

<script>
$(function(){
  
  let url = location.href.replace(/\/$/, "");
 
  if (location.hash) {
    const hash = url.split('#');
    $('.nav-tabs li a[href="#'+hash[1]+'"]').tab('show');
    //url = location.href.replace(/\/#/, '#');
    url += '/';
    history.replaceState(null, null, url);
    setTimeout(() => {
      var t = $(document.getElementById(hash[1]));
      if (t.length > 0){
        $(window).scrollTop(t.first().offset().top);
      } else {
        $(window).scrollTop(0);
      }
    }, 400);
  } 
   
  $('.nav-tabs li a').on('click', function(e) {
    e.preventDefault();
    $(this).tab('show');
    let newUrl;
    const hash = $(this).attr('href');
    newUrl = url.split('#')[0];
    if(hash != '#about') {
      newUrl +=  '/' + hash + '/';
    }
    history.replaceState(null, null, newUrl);
  });

  $('a.link-to-tab').on('click', function() {
    let hash = $(this).attr('href');
    newUrl = url.split('#')[0];
    if(hash != '#about') {
      newUrl += '/' + hash + '/';
    }
    history.replaceState(null, null, newUrl);
    hash = hash.split('#');
    $('.nav-tabs li a[href="#'+hash[1]+'"]').tab('show');
    setTimeout(() => {
      var t = $(document.getElementById(hash[1]));
      if (t.length > 0){
        $(window).scrollTop(t.first().offset().top);
      } else {
        $(window).scrollTop(0);
      }
    }, 400);
    return false;
  });
});
</script>
