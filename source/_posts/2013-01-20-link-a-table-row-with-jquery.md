---
layout: post
title: "Link a Table Row with jQuery"
date: 2013-01-20 11:41
comments: true
categories: 
- jQuery
---

Since I had to do this lately and didn't found a tutorial which was up to date I decided to write one by myself. If you google this task the great post of Imar Spaanjaars [How Do I Make a Full Table Row Clickable Using jQuery?](http://imar.spaanjaars.com/549/how-do-i-make-a-full-table-row-clickable-using-jquery) is one of the top results, so I´d like to show a quite similar but simplified version of this example. (just to provide and alternative attempt not a better one, to make this clear!)

I also use a table with 3 rows which are all linked to different sites. Imar solves the solution by using an additional column in which he provides the links as a fallback for old browsers and hides them with jQuery.

``` html
<tr>
  <td><a href="http://www.google.com/">http://www.google.com/</a></td>
  <td>1</td>
  <td>2</td>
  <td>3</td>
</tr>
<tr>
  <td><a href="http://www.yahoo.com/">http://www.yahoo.com/</a></td>
  <td>4</td>
  <td>5</td>
  <td>6</td>
</tr>
```

If you don't care about old browsers I think there is a shorter method. Instead of using and additional `<td>` I want to link the table row `<tr>` explicitly like:

``` html
<tr url="http://www.google.at">
  <td>1</td>
  <td>2</td>
  <td>3</td>
</tr>
<tr url="http://www.yahoo.at">
  <td>4</td>
  <td>5</td>
  <td>6</td>
</tr>
```

To trigger the url when clicking at a table row you can use the `live()` event of jQuery like this:

``` javascript
    $(function () {
      $("table tr").live("click",function() { 
        location.href = $(this).attr("url");
      });
    });
``` 

To communicate to your user that a table row is clickable you might want to use some css:

``` css
.Pointer {
  cursor: pointer;
}
``` 

The whole code:

[https://gist.github.com/4524458](https://gist.github.com/4524458)

