---
title: Attending
layout: page
# feature_image: 
# image_source: 
---

<ul class="nav nav-tabs nav-justified">
  <li role="presentation" class="active"><a href="#venue">Venue: Dortmund</a></li>
  <li role="presentation"><a href="#hotels">Hotels</a></li>
  <li role="presentation"><a href="#visas">Visas</a></li>
</ul>

<div class="tab-content">
<div role="tabpanel" class="tab-pane active" id="venue">

  {% include_relative include_md.html file="subpages/venue.md" %}

</div>

<div role="tabpanel" class="tab-pane" id="hotels">

  {% include_relative include_md.html file="subpages/hotels.md" %}

</div>

<div role="tabpanel" class="tab-pane" id="visas">

  {% include_relative include_md.html file="subpages/visas.md" %}

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
    if(hash != '#venue') {
      newUrl +=  '/' + hash + '/';
    }
    history.replaceState(null, null, newUrl);
  });

  $('a.link-to-tab').on('click', function() {
    let hash = $(this).attr('href');
    newUrl = url.split('#')[0];
    if(hash != '#venue') {
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
