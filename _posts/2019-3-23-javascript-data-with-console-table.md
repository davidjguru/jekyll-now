---
layout: post
title: 'JavaScript: Data with console.table()'
permalink: /blog/javascript-data-with-console-table
published: true
date: 2019-03-23
author: davidjguru
categories: [JavaScript]
sitemap: true
---
| ![Picture from Unsplash, by @denisolvr]({{ site.baseurl }}/images/davidjguru_drupal_8_javascript_image_from_unsplash.jpeg) |
|:--:|
| *Picture from Unsplash, user Denis Oliveira @denisolvr* |


I would like to write down a quick and little trick to get information from an HTML - based web view through Javascript. It’s a useful tip for those who work daily with web technologies and want to do element listings or maybe locate a specific element within [the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model){:target="_blank"}
<!--more-->

## Introduction
I was recently working on a web project based on Drupal 8 for the regional government of Andalucia (an internal platform for helping Social Services users) and when rendering in the browser, there were several errors and problems with broken links to images (due to permissions /sites/default/files/ within Drupal).

| ![davidjguru Drupal 8 web cau Regional Government]({{ site.baseurl }}/images/davidjguru_drupal_8_web_cau.png) |
|:--:|
| *Web Site of the User Support Center (CAU, in Spanish) in Social Affairs, Andalucia* |

The point is that I wanted to get a quick view of the elements and in an orderly fashion, so I needed a segmented view of the HTML document tree. For that I took a function called console.table(), a way to sort values and display them in a tabbed way, filtering them through one of their attributes.

```javascript      
console.table(data, columns);
```

This function show data as a table, ok -Just what I need-.
First takes a mandatory argument: data, wich must be an array or an object, and a additional parameter called columns. It shows data as a table in the console. Each element in the array (or property if data is an object) will be a row in the final table.

## Example

```javascript
// We have to ensure all the document is loaded previously
window.onload = function() {

// Shows data in a table format, Get all the paragraphs
let paragraphs = document.getElementsByTagName("p");
console.table(paragraphs, "innerText");

}

```

| ![davidjguru Drupal 8 Using console.table Javascript]({{ site.baseurl }}/images/davidjguru_drupal_8_web_cau_console_table.png) |
|:--:|
| *Gettings all the paragraphs in the CAU website through console.table* |

Get more info about console.table at [developer.mozilla.org](https://developer.mozilla.org/en-US/docs/Web/API/Console/table){:target="_blank"}

## :wq!

Greetings. wq!    :-*
