# jQuery

jQuery is still incredibly prevalent in websites, as the most popular JS library.

While web frameworks are rising in popularity, most of the webpages that we know of today were built with jQuery or have some indirect dependency on it.

## Rise in prominence

jQuery's widespread adoption was driven by its ability to overcome different competing browsers, which had differing support for JS features.

Its biggest use case was to accomplish DOM manipulation and AJAX calls, and it grew to include different plugins for other commonly used functionalities.

```js
// Using vanilla JavaScript to add a new list item to a ul element
const addButton = document.getElementById("addButton");
addButton.addEventListener("click", function () {
  const ul = document.getElementById("myList");
  const li = document.createElement("li");
  li.textContent = "New Item (Vanilla JS)";
  ul.appendChild(li);
});
```

```html
<!-- Include jQuery library -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

<script>
  // Using jQuery to add a new list item to a ul element
  $("#addButton").click(function () {
    const ul = $("#myList");
    const li = $("<li>").text("New Item (jQuery)");
    ul.append(li);
  });
</script>
```

```js
const xhr = new XMLHttpRequest();
xhr.open("GET", "https://api.example.com/data", true);

xhr.onload = function () {
  if (xhr.status >= 200 && xhr.status < 300) {
    const response = JSON.parse(xhr.responseText);
    console.log("Data fetched (Vanilla JS):", response);
  } else {
    console.error("Request failed (Vanilla JS)");
  }
};

xhr.onerror = function () {
  console.error("Network error (Vanilla JS)");
};

xhr.send();
```

```html
<!-- Include jQuery library -->
<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>

<script>
  $.ajax({
    url: "https://api.example.com/data",
    method: "GET",
    success: function (response) {
      console.log("Data fetched (jQuery):", response);
    },
    error: function () {
      console.error("Request failed (jQuery)");
    },
  });
</script>
```

Code snippets generated by ChatGPT on 2023-08-18

## Decline in popularity

As developers are increasingly adopting web frameworks like React, it's less common to need to work with jQuery.

StackOverflow's 2022 Developer survey lists jQuery (29.21%, 3rd), behind Node.js (46.31%, 1st) and React.js (44.31%, 2nd) for Web frameworks and technologies.

In contrast, just 2 years ago in 2020 jQuery (43.3%, 1st) was ahead of React.js (35.9%, 2nd) and Angular (25.1%, 3rd).

However, do note that the 2022 survey combines both Web Technologies and Frameworks, which used to be separate categories.

As a comparison among just Web frameworks in 2022, jQuery still ranks above Angular (20.39%).

https://survey.stackoverflow.co/2020/#technology-web-frameworks
https://survey.stackoverflow.co/2022/#most-popular-technologies-webframe-prof

jQuery's decline in popular is only eventual as these Javascript frameworks mature, and creating new paradigms for developers so they do not have to rely on direct DOM manipulation which was one of jQuery's biggest selling points.

In addition to this, our modern browser development has been following W3C standards much more closely, ensuring that the same set of features are available across different browsers.

This can be seen by how `querySelector` and `fetch` API have been implemented by our browsers, allowing us to work easily with DOM selection and AJAX calls natively in vanilla JS so we no longer have to rely on 3rd party libraries to achieve them.

## Unshakable prominence

Despite the decrease in popularity for the adoption of jQuery, it still holds a top spot as the most used JS library.

While new websites are being built with new technologies, existing websites that require jQuery will still continue to do so, as developers will avoid breaking changes.

Even if jQuery is not being used in a website, it is possible that the 3rd party libraries have a dependence on it, creating an indirect dependence.

https://www.wappalyzer.com/technologies/javascript-libraries/

### Bootstrap

Bootstrap is a popular CSS Framework by Twitter.

JS is used to achieve interactive behaviour such as to expand and collapse dropdown menus, as well as displaying popover elements.

Prior to Bootstrap 5, users are required to include jQuery in order for Bootstrap to function correctly.

This is known as an indirect dependency, since users might not actually use jQuery directly but only include it as part of the setup for Bootstrap.

As of Bootstrap 5, the plugins have been rewritten and no longer depend on jQuery, and have been modularised so users can pick and choose which ones to include.

#### Bootstrap 3/4: jQuery required

https://getbootstrap.com/docs/3.3/getting-started/#whats-included
https://getbootstrap.com/docs/4.0/getting-started/introduction/#js

#### Bootstrap 5: jQuery no longer necessary

https://getbootstrap.com/docs/5.0/getting-started/javascript/#still-want-to-use-jquery-its-possible

# Appendix

## Indirect dependencies

Can talk about how Wappalyzer's 2nd most used JS library is core-js, which is inevitably installed since a lot of other packages also depend on it.