<div class="mb-6">
  <div class="mb-2">
    <a class="text-blue-600 font-medium text-lg" href="{{ page.link }}">{{ page.title }}</a>
    {% if page.supplementary_materials_link %}
    <a class="text-blue-600 block text-base mb-1" href="{{ page.supplementary_materials_link }}">
      [Supplementary Materials]
    </a>
    {% endif %}
    <p class="italic">{{ page.collaboration }}</p>
  </div>
  {{ page.content }}
</div>
