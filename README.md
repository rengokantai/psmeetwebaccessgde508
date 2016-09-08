#### psmeetwebaccessgde508
#####1
######3
Web Content Accessibility Guidelines WCAG 2.0
######5 Section 508 vs WCAG 2.0
- Level A most basic of WA features
- Level AA Biggest and most common barriers
- Level AAA Highest level of accessibility

#####2
######7
change
```
<h3>title</h3>
<p>p1</p>
<p>p2</p>
```
to
```
<h3>title</h3>
<ul>
<li>p1</li>
<li>p2</li>
</ul>
```
change
```
<p>
<strong>title</strong>
<br>paragraph
<a href="">read</a>
</p>
```
to
```
<dl>
  <dt>title</dt>
  <dd>paragraph
  <a href="">read</a>
....
</dl>
```
######8 
Level AA 1.4.3-Contrast  
The visual presentation of text and images of text has a contrast ratio of at least 4.5:1  
Foreground stands out from background  

10:12
using
```
<form novalidate>
```
native HTML5 validation balloons != accessible


13:10 explicit label, legend and fieldset  
in fieldset,first element must be legend
```
<fieldset>
<legend>name</legend>
<label>
  <input type="radio" name="" value="">value
</label>
</fieldset>
```
15:42 error prompting
```
<label for="name">Name<span class="error-message">cannot be empty</span></label>
<input name="name" required aria-invalid="true">
```
16:35 tabindex, aria-live never set tabindex>0  (only -1 and 0) -1= removed from natural tab order
```
<section id="errors" aria-live="assertive" tabindex="-1">
</section>
```

######9
```
<meta name="viewport" content="width=device-width, initial-scale=1,maximum-scale=1,user-scalable=no, shrink-to-fit=no"/>
```
05:08  
landmark nav  (only can use once per page)  
- header
- nav
- main
- footer
- aside  

