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
landmark nav  (main can use once per page)  
- header
- nav
- main
- footer
- aside  

06:20  
aria-label
```
aria-label="site"
aria-label="page"
```

######10
Visually hidden text(only readers can show)
```
sr-only: bootstrap
show-for-sr:foundation
```
pure css
```
.hidden{
  border:0;
  clip:rect(1px,1px,1px,1px);
  height:1px;
  overflow:hidden;
  padding:0;
  positionLabsolute;
  width:1px;
}
```

09:14  skip link css
```
.skip{
  left:100%;
  position:absolute;
}
.skip:focus{
//show link
left:50%;
}
```
######11 Forms table
use div and span to replace table layout
```
<div class="prod">
  <div class="row top">
    <span>top</span>
  </div>
  <div class="row">
    <span>content</span>
  </div>
</div>
```
04:40 scope
```
<tr>
  <th scope="col"></th>
</tr>
```

######14
01:23  
Anyembedded media using <iframe> should have a label via the title attribute
######15
00:34  
For icon,we need to add text or else readers cannot recognize.
```
<span class="icon icon-chrome"><span class="hidden">chrome</span></span>
```

######17
Accessible SVG  
- add role="img"
- use the <title>
- use aira-labelledby referening <title>  

example
```
<svg role="img" aria-labelledby="ke">
  <title id="ke">ke</title>
</svg>
```


######23
```
aria-hidden="true"
```
