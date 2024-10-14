---
layout: default
title: test
permalink: /test/
---

### Test

Testing6

{% raw %}

  <h1>Documentation</h1>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
  
  <div class="all-questions">
    <h2>How do you smurf a murf?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>How do many licks does a giraffe?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>Which Frank is?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h2>Is fourteen enough?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>Is a circle an oval y/n?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>Many mongerals manifest mountains</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>How would you like a soda drink?</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>I would very much like a soda drink.</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
    
    <h3>Thank you for accepting the soda drink.</h3>
    <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  
  </div>

<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script>
var ToC =
  "<nav role='navigation' class='table-of-contents'>" +
    "<h2>On this page:</h2>" +
    "<ol>";

var newLine, el, title, link, currentH2Id = null;

// Loop through h2 and h3 elements
$("h2, h3").each(function(index) {
  el = $(this);
  title = el.text();

  // Check if the element has an id, if not, assign a unique id based on the index
  if (!el.attr("id")) {
    var newId = "section-" + index;
    el.attr("id", newId);
  }

  link = "#" + el.attr("id");

  // Check if the element is an h2
  if (el.is("h2")) {
    // Close the previous h3 list if it exists
    if (currentH2Id !== null) {
      ToC += "</ol></li>";
    }

    // Create a new list item for the h2
    newLine =
      "<li>" +
        "<a href='" + link + "'>" +
          title +
        "</a>" +
        "<ol>"; // Start a new nested list for h3s
    currentH2Id = el.attr("id");
  }

  // If the element is an h3, nest it under the last h2
  if (el.is("h3")) {
    newLine =
      "<li>" +
        "<a href='" + link + "'>" +
          title +
        "</a>" +
      "</li>";
  }

  ToC += newLine;
});

// Close the last open list
if (currentH2Id !== null) {
  ToC += "</ol></li>";
}

ToC +=
   "</ol>" +
  "</nav>";

$(".all-questions").prepend(ToC);
</script>

{% endraw %}

</article>
