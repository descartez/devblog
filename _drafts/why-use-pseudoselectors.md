---
layout: post
title:  "Why Use Pseudoselectors?"
date:   2015-11-7 09:44:31
categories: lessons css
---

## What are pseudoselectors?

When you have to select a particular HTML element, we use a CSS selector.
So if the HTML looks like this:

{% highlight html linenos %}

<div id="this-list" class="all-lists">
  <ul>
    <li>
      A list item.
    </li>
    <li>
      Another list item.
    </li>
  </ul>
</div>

{% endhighlight %}

A basic CSS selector looks like:

{% highlight css linenos %}

// this selects based on id's. This only works for this one thing.

#this-list {
  font-size: 2em
}

// this works on all things with the same class.
// If you want to apply the same rules to multiple
// things, this is what to do.

.all-lists {
  font-size: 2em
}

{% endhighlight %}

But what if you only want to select the first item in the list? I guess you could make that list item have a particular id. But what if the first one of every list you have needs to have the same rules applied?

If you're feeling pretty on
