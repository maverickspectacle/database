---
layout: default
title: test
permalink: /test/
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">
      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>
      <div class="entry">{{ post.excerpt }}</div>
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Testing4</a>
    </article>
  {% endfor %}
</div>

<article>

{% raw %}

<article>
  <h1>Documentation</h1>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
  
  <div class="all-questions">
    <h3 id="one">How do you smurf a murf?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="two">How do many licks does a giraffe?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="three">Which Frank is?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="four">Is fourteen enough?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="five">Is a circle an oval y/n?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="six">Many mongerals manifest mountains</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="seven">How would you like a soda drink?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="eight">I would very much like a soda drink.</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3 id="nine">Thank you for accepting the soda drink.</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
  </div>
  
</article>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
  var ToC =
    "<nav role='navigation' class='table-of-contents'>" +
      "<h2>On this page:</h2>" +
      "<ul>";

  var newLine, el, title, link;

  $("article h3").each(function() {
    el = $(this);
    title = el.text();
    link = "#" + el.attr("id");

    newLine =
      "<li>" +
        "<a href='" + link + "'>" +
          title +
        "</a>" +
      "</li>";

    ToC += newLine;
  });

  ToC +=
     "</ul>" +
    "</nav>";

  $(".all-questions").prepend(ToC);
</script>

{% endraw %}

</article>
