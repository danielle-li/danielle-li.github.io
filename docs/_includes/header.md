<ul class="flex">
  <li class="flex flex-shrink-0 flex-grow font-bold text-xl mr-12 md:block hidden">
    Danielle Li
  </li>
  {% assign pages = site.pages | where_exp: "p", "p.custom_menu_order > 0" | sort: "custom_menu_order" %}
  {% for p in pages %}
  <li class="mr-6">
    {% if p.url == page.url %}
    <a href="{{p.url | prepend: site.url}}"
    class="py-1 transition duration-200 ease-in-out relative block font-medium text-blue-600"
    >
    <span class="relative">{{p.title}}</span>
    </a>
    {% else %}
    <a href="{{p.url | prepend: site.url}}"
    class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
    >
    <span class="relative">{{p.title}}</span>
    </a>
    {% endif %}
  </li>
  {% endfor %}
  <li class="mr-6">
    <a href="http://mitsloan.mit.edu/faculty-and-research/faculty-directory/detail/?id=47297"
    class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
    >
    <span class="relative">Official Website</span>
    </a>
  </li>
  <li class="mr-6">
    <a href="https://scholar.google.com/citations?user=loXqXPQAAAAJ&hl=en"
    class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
    >
    <span class="relative">Google Scholar</span>
    </a>
  </li>
  <li class="mr-6">
    <a href="https://docs.google.com/viewer?a=v&pid=sites&srcid=ZGVmYXVsdGRvbWFpbnxkYW5pZWxsZWxpfGd4OjNlZDljZTQ4NTJmODMzNGQ"
    class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
    >
    <span class="relative">CV</span>
    </a>
  </li>
  </div>
</ul>
