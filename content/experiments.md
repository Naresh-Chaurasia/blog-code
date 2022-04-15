---
title: "Experiments"
date: 2022-03-30T14:13:49+05:30
draft: false
---

## Images

* https://hugo-mini-course.netlify.app/sections/optimizing/images/

**Working: static**

{{< figure src="../img/img.png" title="This is coming from static/img folder" >}}

---
 
![This is coming from static folder](../img.png)


---

img tag is causing problem.

<img src="../img.png" width="500" height="300">

---

**Not Working**

{{ $image := resources.Get "../img/img.png" }}
<img src="{{ $image.Permalink }}">

---

{{ $image := resources.Get "images/sunset.png" }}
<img src="{{ $image.Permalink }}">

---

{{ $image := resources.Get "assets/images/sunset.png" }}
<img src="{{ $image.Permalink }}">

---

{{ $asset := resources.Get "../duck.png" }}
{{ $img := $asset.Fit "600x400" }}
<img alt="Yellow Duck" src="{{ $img.RelPermalink }}" />


