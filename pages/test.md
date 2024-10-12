---
layout: default
title: test
permalink: /test/
---

<div class="posts">
  {% for post in site.posts %}
    <article class="post">

      <h1><a href="{{ site.baseurl }}{{ post.url }}">{{ post.title }}</a></h1>

      <div class="entry">
        {{ post.excerpt }}
      </div>

      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Testing2</a>
    </article>
  {% endfor %}
</div>

<html>

<article>
  <h1>Documentation</h1>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <div class="all-questions">
  
  <h3>How do you smurf a murf?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>How do many licks does a giraffe?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>Which Frank is?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>Is fourteen enough?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>Is a circle an oval y/n?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>Many mongerals manifest mountains</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>How would you like a soda drink?</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>I would very much like a soda drink.</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p>  
  
  <h3>Thank you for accepting the soda drink.</h3>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum tortor quam, feugiat vitae, ultricies eget, tempor sit amet, ante. Donec eu libero sit amet quam egestas semper. Aenean ultricies mi vitae est. Mauris placerat eleifend leo.</p> 
    
  </div>
  
</article>

<style>

body {
  background: #eee;
  padding: 20px;
}

article {
  max-width: 50em;
  background: white;
  padding: 2em;
  margin: 1em auto;
}

.table-of-contents {
  float: right;
  width: 40%;
  background: #eee;
  font-size: 0.8em;
  padding: 1em 2em;
  margin: 0 0 0.5em 0.5em;
}
.table-of-contents ul {
  padding: 0;
}
.table-of-contents li {
  margin: 0 0 0.25em 0;
}
.table-of-contents a {
  text-decoration: none;
}
.table-of-contents a:hover,
.table-of-contents a:active {
  text-decoration: underline;
}

h3:target {
  animation: highlight 1s ease;
}

@keyframes highlight {
  from { background: yellow; }
  to { background: white; }
}
  
</style>

<script>

var ToC =
  "<nav role='navigation' class='table-of-contents'>" +
    "<h2>On this page:</h2>" +
    "<ul>";

var newLine, el, title, link, idCounter = 1;

$("article h3").each(function() {
  el = $(this);
  title = el.text();
  
  // If the <h3> doesn't have an id, assign one
  if (!el.attr("id")) {
    el.attr("id", "section-" + idCounter);
    idCounter++;
  }

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

</html>
