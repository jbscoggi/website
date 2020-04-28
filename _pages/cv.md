---
layout: none
permalink: /cv/
title: CV
---

<!DOCTYPE html>
<html height="100%">

  {% include head.html %}

  <body min-height="100%">

    {% include header.html %}

    <div class="page-cv">
      <div class="wrapper">
        <object data="{{ 'cv.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}" width="100%" height="100%" type='application/pdf'>
        </object>
      </div>
    </div>

    {% include footer.html %}

    {% include hemline.html %}

  </body>

</html>


  





