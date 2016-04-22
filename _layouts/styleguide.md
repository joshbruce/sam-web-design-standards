<!DOCTYPE html>
<!--[if lt IE 9]><html class="lt-ie9"><![endif]-->
<!--[if gt IE 8]><!--><html lang="en"><!--<![endif]-->

  <head>
    {% include head.html %}
  </head>

  <body class="{{ page.title | slugify }}">

  	{% include navbar.html %}

  	{% include sidenav.html %}

    <div class="main-content" id="main-content">
      <div class="styleguide-content usa-content">
        <h1 id="{{ page.title | slugify }}">{{ page.title }}</h1>
        <p class="usa-font-lead">{{ page.lead }}</p>
        {{ content }}
      </div>

      {% capture my-include %}{% include acronyms.md %}{% endcapture %}
      {{ my-include | markdownify }}

      <footer class="usa-styleguide-footer">
        {% include footer.html %}
      </footer>
    </div>
    {% include analytics.html %}

    {% include scripts.html %}

    <script src="{{ site.baseurl }}/assets/js/vendor/uswds.min.js"></script>

  </body>

</html>