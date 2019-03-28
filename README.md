# Theme Accessibility

Making your WordPress theme accessible has multiple benefits. Not only do you make it more friendly to the various devices and environments that people of all abilities use on a daily basis but search engines also reward efforts to make sites accessible.

## Description

In this lesson, we'll go over a few basic things that can be incorporated into any theme to make it more accessibility friendly. It will not be a exhaustive list of all the things that can be done for accessibility, but it will give you a good start.

## Prerequisite Skills

To get the most from this lesson you should be able to:

*   Add content in the WordPress editor
*   Comfortably write HTML, at least a little
*   Create WordPress page template files (e.g., single.php)
*   Be able to use browser developer tools such as the inspector

## Objectives

Improve accessibility of themes through:

*   Using HTML headings to define content hierarchy only
*   Using links for links
*   Using buttons for actions
*   Including alt attributes on images
*   Allowing for keyboard navigation
*   Avoiding target="_blank" in links

## Assets

*   [WordPress Theme Accessibility Guidelines](https://make.wordpress.org/themes/handbook/review/accessibility/) (resource)

## Screening Questions

*   Have you created a custom page template or theme?
*   Are you comfortable with HTML and/or template tags?
*   Do you want to improve an existing theme's accessibility?

## Teacher Notes

*   If you have a Mac, consider enabling the Voice Over feature in System Preferences > Accessibility to demonstrate a screen reader.

## Hands-on Walk-through

Doing the following will not make your theme perfectly accessible, but it will make it significantly better for many users. Making these steps a regular practice will improve the internet for everybody.

### Use HTML Headings for Content Hierarchy Only

An HTML-only document is highly accessible. With only text for content, the HTML heading tags help separate sections and identify different levels of information. It's when we add styling and actions that we can interfere with the native HTML accessibility. A great place to begin working on site accessibility then is right in the editor when adding content. Rather than adding an `<h5>` tag because it makes text look the way you'd like it to, use heading tags as they were intended - as levels in an outline. And since the page title gets an `<h1>` tag, you should only use `<h2>` through `<h6>` within the text on the page itself. Getting text to look the way you'd like (such as bold, bigger, or centered) is the function of CSS, not HTML heading tags. If you're not familiar with CSS and how to do that, there's a separate lesson covering an [Intro to CSS](https://make.wordpress.org/training/handbook/theme-school/intro-to-css/).

### Use Links for Links

It seems self-evident that you should use links for links, but many links are styled to look like buttons - hence the confusion. While a sighted user might not be able to tell the difference between a link and a button if they have the same styling, a screen reader or search engine will find them quite different. If you click on it and it takes you somewhere (another page for instance), it's a link and should be created that way. Also, avoid `target="_blank"` in your links. It can be confusing to all types of users, especially for visually impaired folks. They can wind up with all sorts of open tabs that they don't even know about. Leave the control of whether the link opens in the same window or in another tab in the hands of users. Example:

<pre><a href="https://wordpress.org">WordPress.org</a></pre>

### Use Buttons for Actions

Buttons differ from links in that they DO something. They submit a form, send a message, or reset a page. Buttons are a native HTML feature that are easily used from a keyboard. Browsers and search engines know what to do with them. Example:

<pre><button type="submit">Submit</button></pre>

### Include ALT Attributes on Images

Images can be used for a variety of purposes. They can set a mood, convey information, or provide a visual shortcut for recognition (such as icons). Screen readers and search engines can't tell what `IMG_8792.jpg` is supposed to convey. And poor connections, filename typos, blockers, or other issues may keep your images from being downloaded or displayed. You need to provide some text-based information to help out when images can't be seen. That's what the ALT attribute is for - alternative text. Including an ALT attribute on every image is a best practice. If an image is really just decorative and provides no value then including an empty ALT attribute (`alt=""`) will convey that it should be ignored. Example:

<pre><img src="https://unsplash.com/?photo=6xh7H5tWj9c" alt="orange smoggy sunset over a never ending city" /></pre>

### Allow for Keyboard Navigation

Many users use the keyboard either primarily or exclusively to navigate websites. When creating a theme, this behavior should be accounted for in the design and code. A user should be able to reach everything on the page using the keyboard. It is expected that the TAB key will move you forward and the SHIFT+TAB keys will move you back. When that doesn't happen, it can cause trouble and forms can be especially problematic. It is also a best practice that there is some visual confirmation of where the "focus" is every time you tab. Controlling the focus of your web page goes a long way towards making keyboard navigation pleasant. Tabs will follow your HTML code from top to bottom unless you've done something to override that. The same caution holds for CSS, don't override the `:focus` element unless you've accounted for the impacts on accessibility.

## Summary

Taking these five steps and incorporating them into the websites you work on will go a long way towards covering the needs of most users. They may not produce a perfectly accessible site, but your site will be better than many.

## Exercises

### Review Headings for Content Organization

Check your site's content to see how the heading tags are used. Do they follow an orderly sequence where `<h2>` tags are followed by `<h3>` tags? Or are the tags used arbitrarily and out of sequence? Are they ever used for styling rather than structure?

*   Use your browser's inspector feature to check heading tags on various websites. Do they follow this guideline?

### Check for ALT Attributes on Your Web Page

Use a free ALT attribute checker service to review the images on your web page (e.g., [http://www.contentforest.com/seo-tools/image-alt-checker](http://www.contentforest.com/seo-tools/image-alt-checker)).

*   Do you have any idea what the images are based on the ALT attribute text?
*   Does the ALT attribute text give a fair approximation of what the image was meant to convey?

### Navigate a Web Page Using Only the Keyboard

Using a theme you are working with or a general web page, try to navigate the site using only the TAB and SHIFT+TAB keys. Start with your cursor in the browser's address bar.

*   Can you get through the navigation menus?
*   Do you go to the content or the sidebar first?
*   What about a form? Can you tell which field has the focus? What about the submit button?

## Quiz

**The ______ attribute on images helps convey the meaning of an image to visually-impaired people.**

1.  title
2.  target
3.  alt
4.  href

**Answer:** 3. alt attribute 

**Headings such as H3 or H4 should be used for...**

1.  Emphasizing text
2.  Organizing content
3.  Making text look good
4.  Making lists

**Answer:** 2. Organizing content 

**Following these steps is everything you need to do to make your theme accessibility-ready.**

1.  True
2.  False

**Answer:** 2\. False. It's a good start, but there's much more that can be learned about accessibility.
