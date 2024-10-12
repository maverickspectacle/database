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
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Testing3</a>
    </article>
  {% endfor %}
</div>

<article>
  <h1>Documentation</h1>
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>

  <div class="all-questions">
    <h3>How do you smurf a murf?</h3>
    <p>Pellentesque habitant morbi tristique senectus...</p>
    <!-- More questions here -->
  </div>
</article>

<style>
  body { background: #eee; padding: 20px; }
  article { max-width: 50em; background: white; padding: 2em; margin: 1em auto; }
  .table-of-contents { float: right; width: 40%; background: #eee; font-size: 0.8em; padding: 1em 2em; margin: 0 0 0.5em 0.5em; }
  .table-of-contents ul { padding: 0; }
  .table-of-contents li { margin: 0 0 0.25em 0; }
  .table-of-contents a { text-decoration: none; }
  .table-of-contents a:hover, .table-of-contents a:active { text-decoration: underline; }
  h3:target { animation: highlight 1s ease; }
  @keyframes highlight { from { background: yellow; } to { background: white; } }
</style>

{% raw %}
<script>
  var ToC = "<nav role='navigation' class='table-of-contents'><h2>On this page:</h2><ul>";
  var newLine, el, title, link, idCounter = 1;

  $("article h3").each(function() {
    el = $(this);
    title = el.text();
    
    // Assign an ID if the h3 doesn't have one
    if (!el.attr("id")) {
      el.attr("id", "section-" + idCounter);
      idCounter++;
    }
    
    link = "#" + el.attr("id");

    // Create the list item for the ToC
    newLine = "<li><a href='" + link + "'>" + title + "</a></li>";
    
    // Append the new line to the ToC
    ToC += newLine;
  });

  // Close the ToC structure
  ToC += "</ul></nav>";

  // Prepend the ToC to the .all-questions div
  $(".all-questions").prepend(ToC);
</script>
{% endraw %}
