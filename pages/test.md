---
layout: default
title: test
permalink: /test/
---

Testing7



  <h1>Documentation</h1>
  
  <p>Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...</p>  

  <div class="all-questions">
    
## How do you smurf a murf?
    
Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...  
    
### How do many licks does a giraffe?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
### Which Frank is?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
## Is fourteen enough?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas... 
    
### Is a circle an oval y/n?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...
    
### Many mongerals manifest mountains

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...  
    
### How would you like a soda drink?

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas... 
    
### I would very much like a soda drink.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...  
    
### Thank you for accepting the soda drink.

Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas...

  </div>

{% raw %}

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
