---
title: CSS Loading Strategies: Inline, External, and Code Splitting. 
date: 2025-09-21
category: css-core
difficulty: starter
sources: https://www.w3schools.com/html/html_css.asp, https://web.dev/learn/performance/optimize-resource-loading, https://developer.mozilla.org/en-US/docs/Glossary/Code_splitting
author: Christopher Urban
---

# CSS Inline

Inline refers to the use of `<style>` in your html as a means of preloading style choices for faster rendering or to prortype style choices before being placed in the CSS external script. 

This can be used to great affect when cutting down initial load times as, it reduces the amount of network requests for CSS resources. This can also improve initial load times when a users browser cache is not primed. Usually this is done in the `<head>` element to serve the purpose of faster loading. 

Unfortunately, HTML resources cannot be cached for long, or at all. Meaning subsequent pages will need to rerun the style line. So you need to be sure that the added bytes to the HTML are worth the effort. 

Inline can also refer to the use of the style attribute inside of an HTML element. Both will be shown below. 

## Example

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>h1,h2{color:#ff0000}h1{font-size:2em}h2{font-size:1.5em}</style>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1 style="color:blue;">Main Title</h1>
    <h2>Subtitle</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Praesent sit amet bibendum tortor. Aenean pellentesque, ante id convallis varius, odio est aliquet augue, ut tristique dui ligula tincidunt ante. Donec commodo risus sem, sagittis placerat augue dapibus ut. Curabitur non lacinia elit. Vestibulum vitae risus ac nisi viverra semper. Donec lobortis, lorem in pretium egestas, arcu ex feugiat sem, et iaculis ipsum dui id nisl. Vivamus finibus convallis finibus. Pellentesque ac purus neque.</p>
</body>
</html>
```

## When to Use

Use `<style>` when you need to save time on initial loads for an HTML page that would not suffer from the added bytes of code to the base HTML file. If I was having problems with my website having slow load times, I might move over critical styling that must be loaded first to a `<style>` element in the `<head>` so they are loaded before any of the CSS files need to be requested into the HTML. This is primarily an optimizing choice to make sure the aesthetic of your website can remain consistent and load faster for users. 

**Source**: [W3 Schools: HTML-CSS](https://www.w3schools.com/html/html_css.asp), [web.dev: Optimize Resource Loading](https://web.dev/learn/performance/optimize-resource-loading)


# CSS External

External refers to the act of writing your CSS on an external file from your HTML and using `<link>` or @import to bring said external file in to style your page. This is an industry standard practice. Using External CSS files allows for not only cleaner coding but also more efficient loading and processing. A website with all it's styling in the HTML is going to be very large which can be taxing for the browser to load on every opening of the application. This is why inline is only used for critical styling, to keep the overall size of the HTML file down. 

## Example

```CSS
/* Paragraph styles */
p {
  border: #333 solid 1px;
  background-color: aqua;
  margin: 1rem;
  text-align: center;
  padding: 5rem;
  font-size: 1em;
  color: #333;
  line-height: 1.6;
  margin: 10px 0;
}
```

## When to Use

External is used to avoid excessive styling in the HTML file. using the `<link>` for external CSS files is also a great method of improving loading. It inherently is loaded before other methods like @import. When using @import the CSS file must first be downloaded before imported. The same is not true, and therefore faster, using `<link>`. External use is important for projects that require great deals of styling and is currently an industry standard practice to do.

**Source**: [W3 Schools: HTML-CSS](https://www.w3schools.com/html/html_css.asp), [web.dev: Optimize Resource Loading](https://web.dev/learn/performance/optimize-resource-loading)


# CSS Code-Splitting



## Example

```CSS
/* Paragraph styles */
p {
  border: #333 solid 1px;
  background-color: aqua;
  margin: 1rem;
  text-align: center;
  padding: 5rem;
  font-size: 1em;
  color: #333;
  line-height: 1.6;
  margin: 10px 0;
}
```

## When to Use



**Source**: [W3 Schools: HTML-CSS](https://www.w3schools.com/html/html_css.asp), [web.dev: Optimize Resource Loading](https://web.dev/learn/performance/optimize-resource-loading)