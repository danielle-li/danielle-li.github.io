<!DOCTYPE html>
<html lang="en" dir="ltr">
<head>
  {% if page.url == '/404.html' %}
  <meta name="robots" content="noindex, nofollow">
  {% endif %}
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <meta http-equiv="x-ua-compatible" content="ie=edge">
  {% if page.url == '/' %}
  <meta name="description" content="{{ site.custom_settings.description }}">
  {% endif %}
  <link rel="canonical" href="{{ page.url | replace:'index.html','' | prepend: site.url }}">
  <link rel="shortcut icon" type="image/x-icon" href="{{site.url}}/favicon.ico">
  <link rel="apple-touch-icon" sizes="180x180" href="{{site.url}}/apple-touch-icon.png">
  <link rel="icon" type="image/png" sizes="32x32" href="{{site.url}}/favicon-32x32.png">
  <link rel="icon" type="image/png" sizes="16x16" href="{{site.url}}/favicon-16x16.png">
  <link rel="manifest" href="/site.webmanifest">
  <title>
    {% if page.url == '/' %}
    {{site.custom_settings.name}}
    {% else %}
    {{page.title}} | {{site.custom_settings.name}}
    {% endif %}
  </title>

  {% if site.custom_settings.is_development %}
  <link rel="stylesheet" type="text/css" href="{{site.url | append: '/assets/css/styles.css'}}">
  {% else %}
  <link rel="stylesheet" type="text/css" href="{{site.url | append: '/assets/css/' | append: site.data.rev-manifest['styles.min.css']}}">
  {% endif %}

  </head>
  <body>
    <div id="header" class="md:static w-full h-auto lg:hidden py-4 px-12 shadow">
      {% include header.md %}
    </div>
    <div class="w-full max-w-screen-xl mx-auto px-6">
      <div class="lg:flex -mx-6">
        <div id="sidebar" class="fixed h-full w-full lg:static lg:h-auto lg:overflow-y-visible lg:block lg:border-0 lg:w-1/5 hidden pt-16">
          <div id="sidebar-wrapper" class="lg:pl-12 md:pl-6 h-full overflow-y-auto scrolling-touch lg:h-auto lg:block lg:sticky overflow-hidden">
            {% include sidebar.md %}
          </div>
        </div>
        <div id="content-wrapper"
          class="lg:px-12 md:px-6 min-h-screen w-full lg:static lg:overflow-y-scroll lg:w-3/4 pt-16 lg:max-h-screen"
        >
          <div id="content">
            {{ content }}
          </div>
        </div>
      </div>
    </div>
  </body>
</html>

<!-- Generated with Jeykll {{site.github.versions.jekyll}} at {{ 'now' | date: '%F %T' }} -->
