---
permalink: "/gallery/"
layout: page
title:  "Gallery"
---

<section class="page-section" id="portfolio">
            <div class="container">
                <div class="text-center">
                    <h2 class="section-heading text-uppercase">Gallery</h2>
                    <p>Take a look in store and see some of our wedding photos. Below are some examples of menswear, weddings and suits we can offer you. It’s always better to come in store to see the latest styles though.</p>
                    <!--<h3 class="section-subheading text-muted">Lorem ipsum dolor sit amet consectetur.</h3>-->
                </div>
<div class="container">

  <hr class="mt-2 mb-5">

{% assign rows = site.gallery.size | divided_by: 4.0 | ceil %}
{% for i in (1..rows) %}

  <div class="row text-center text-lg-start">

  {% assign offset = forloop.index0 | times: 4 %}
  {% for image in site.gallery limit:4 offset:offset %}
    
    <div class="col-lg-3 col-md-4 col-6">
      <a class="d-block mb-4 h-100" id="single_image" href="{{ image.img }}"><img class="img-fluid img-thumbnail" src="{{ image.img }}" alt="{{ image.alt }}"/></a>
    </div>

    {% endfor %}   
  
  </div>

{% endfor %}

</div>
</div>
</section>