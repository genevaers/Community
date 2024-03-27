# GenevaERS and Accessibility

This statement expresses why accessibility is important and what has been done to address accessibility, and guidelines for future contributions.

It is important for the GenevaERS project to follow accessibility best practices so that people with diverse abilities can still participate in the project.

There are three areas of GenevaERS that need to be considered for accessibility.
-	Documentation
-	Workbench
-	Performance Engine

## GenevaERS Documentation

GenevaERS's documentation is available via web browser, so the basic principles of web accessibility are to be considered.

### Basic principles of web accessibility

The following page has a good description of the concept of accessibility.

[W3 Web Accessibility Initiative](https://www.w3.org/WAI/fundamentals/accessibility-intro/)  

To summarize, accessibility is about enabling access for people with disabilities, or enabling access with assistive technology, such as screen readers.

There are four principles that a web site should adhere to:
### Perceivable
The website should be screen reader software compatible.  
All non-text items must have a text alternative.  
Colour contrast should be considered. Low contrast (may suit people with dyslexia) vs high contrast (may suit people with vision impairment).  
Consider fonts. Sans serif fonts are easier to read.  
### Operable
Simple and consistent navigation.  
Provide a sitemap that helps support accessibility by ensuring there are multiple ways to navigate across pages within your website.  
Avoid unnecessary animations.  
### Understandable
Organised in a simple structure.  
Use plain, direct language.  
### Robust
HTML that can be parsed by assistive technologies.  

### How they are applied to GenevaERS documentation website

The documentation is mostly developed using Markdown, which Jekyll converts to HTML. HTML can be added inline in the Markdown too. Markdown generates simple HTML markup, and simple HTML markup can be easily read by assistive technology.  
The font used is a sans serif font.  
The language code is generated in the opening HTML element (used by screen readers).  
We have included the plugin jekyll-sitemap to generate a sitemap.  
The Website has a simple layout using heading hierarchies.  
The Markdown will contain alt text in images.  

### Guidelines to follow when adding new content

1. Use Headings To Outline Your Content.  
Assistive technology users can navigate pages by headings, so use Markdown’s heading formatting options to create a logical structure.
2. New Images should have a meaningful description in alt text.  
An alternate description should clearly and concisely describe the content of the image and the context of why it was included.
3. Use Plain Language.  
This helps everyone understand the content, including neurodivergent people, and those whose first language is not English.
4. Avoid animated images.  
If required use the picture element to load the image in a paused state.
5. Use descriptive link names.  
Some forms of assistive technology can navigate through a list of links on a page. The links should give enough information, so navigation is easy.

### Additional points

1)	Investigate implementing a toggle for dark mode.
2)	Consider how the syntax diagram images could be more accessible.


## Workbench accessibility

Eclipse. Input required here.

## Mainframe accessibility

The Performance Engine is driven by JCL on the mainframe.  Assistive technology products, such as screen-readers, function with the user interfaces found in z/OS. Consult the assistive technology documentation for specific information when using it to access z/OS interfaces.

## References

https://www.w3.org/WAI/fundamentals/accessibility-intro/

http://www.goring.org/resources/accessibility.html

https://blog.hubspot.com/website/web-accessibility
