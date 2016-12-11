---
layout: post
title: The structure of a basic HTML document
summary: It's critical to have a solid foundation for your all of your web pages. To create that foundation, you need to know how to set up a simple HTML document. In this article, we'll go over everything you need to know to build your first web page. 
---

When I started learning HTML, I struggled to find a definitive guide for creating a bare bones HTML document. To me, a definitive guide not only explains what code should be present, but why it should be present. The why is important because the goal should be to use just the right amount of code to create a project. Enough code to enable the right features, but little enough code to keep sites light and easy to maintain. 

This article is what I wish I had when I started. I'll show you what a basic HTML document look likes and I'll explain what each piece is so you can understand why you should include it. Below is the minimum that you need to build a simple HTML5 page. This will be the base off of which you can add additional features and components.

{% highlight html linenos %}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>My First Website</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
{% endhighlight %}

## The document type declaration
The first thing you should include in every HTML document is a document type declaration. For HTML5, it looks as follows:

{% highlight html linenos %}
<!DOCTYPE html>
{% endhighlight %}

The document type declaration for HTML5 is <a href="ttps://www.w3.org/TR/html5/syntax.html#the-doctype" target="_blank" class="content-link">case-insensitive</a>, so any of the following below are the same as the above. I suggest sticking with the syntax above as it's what you'll see most often.

{% highlight html linenos %}
<!doctype html>
<!DOCTYPE HTML>
<!DoCtYpE hTmL>
{% endhighlight %}

If this document type declaration feels like it should be more complicated, don't worry, you're not missing anything. Declarations were indeed more complex with <a href="https://www.w3.org/QA/2002/04/valid-dtd-list.html" target="_blank" class="content-link">prior versions of HTML</a>, but fortunately for us, HTML5 made life much easier.

Even though it's mentioned above, it's worth reiterating that the document type declaration must be the first element in every HTML document that you create. Without this declaration, browsers will default to rendering your document in <a href="https://developer.mozilla.org/en-US/docs/Quirks_Mode_and_Standards_Mode" target="_blank" class="content-link">Quirks mode</a> instead of Standards mode (sometimes called Strict Mode). Standards mode is what you want because it ensures that all web browsers display your document in the same way. 

## The html element
After your document type declaration, you will need to create a html element using a set of opening and closing <span class="inline-code"><html></span> tags. The html element will be the parent element, or root element, for all of the other elements on the page. In terms of code, this means that all of the elements on the page will be within the opening and closing <span class="inline-code"><html></span> tags. Looking at just the tags from our example, you can see that both the <span class="inline-code"><head></span> and <span class="inline-code"><body></span> tags are nested within the <span class="inline-code"><html></span> tags.

{% highlight html linenos %}
<html lang="en">
  <head>
  </head>
  <body>
  </body>
</html>
{% endhighlight %}

On the opening <span class="inline-code"><html></span> tag, I've also included an attribute to declare the default language of the page. In this case, it's English, which is denoted by the syntax <span class="inline-code">lang="en"</span>. Declaring a default language <a href="https://www.w3.org/International/questions/qa-lang-why" target="_blank" class="content-link">enables a number of features</a> including font selection based on language, search optimization, page translation, and grammar checking. Declaring a language is not required, but it's recommended based on the feature set it enables.

## The head element
When I created my first website the head element confused me. I thought that, if content was within a tag, then it would be displayed on the resulting web page. This is the case for content between most tags, but not for the content between the opening and closing <span class="inline-code"><head></span> tags. You can think of the head element as the container for all of the information about your HTML document. This information is called metadata.

{% highlight html linenos %}
<head>
  <meta charset="utf-8">
  <title>My First Website</title>
</head>
{% endhighlight %}

There are two things you must include in the head element:

* **A character set definition.** This is done by placing a character set attribute on the <span class="inline-code">\<meta></span> tag, denoted by <span class="inline-code">charset="utf-8"</span>. If you don't define a character set, the letters and characters on your website <a href="https://www.w3.org/International/questions/qa-html-encoding-declarations.en"  target="_blank" class="content-link">may not be displayed correctly</a>. For web pages, <a href="https://www.w3.org/International/questions/qa-choosing-encodings"  target="_blank" class="content-link">UTF-8 should be used</a> because it can support many languages and can accommodate pages and forms in any mixture of languages.

* **A title for your web page.** This is done by defining a title element using the opening and closing <span class="inline-code">\<title></span> tags. The title in the example above, "My First Website", will not be displayed on the web page itself. In fact the only place you will be able to see it within the browser is at the top of a tab. The title will, however, be present in the code so search engines can display it in search results.

## The body element
The body element, created with opening and closing <span class="inline-code"><body></span> tags, should immediately follow the closing <span class="inline-code"><head></span> tag. Between the <span class="inline-code"><body></span> tags is where you put all of the content that you want to be displayed on your web page. 

{% highlight html linenos %}
<body>
  <h1>Hello World!</h1>
</body>
{% endhighlight %}

Above I've included a h1 element that says "Hello World!" in between the <span class="inline-code"><body></span> tags. If you were to copy and paste the example above into a document, save it with the ".html" extension, and open it with your favorite web browser, you would see "Hello World!" in big letters at the top of the page.

## Conclusion
Creating a basic HTML document is simple, and knowing what each element is should help you realize that maybe you don’t need a complex template like <a href="https://html5boilerplate.com/" target="_blank" class="content-link">HTML5 Boilerplate</a> to start a project. If you use the structure above for all of your web page, you'll have an excellent foundation on which you can build increasingly complex features and functionality.
