<div>
  <img class="w-full rounded"
    src="{{'/assets/img/danielle-li-headshot.jpg' | prepend: site.url}}" alt="Headshot"
    style="transform: scaleX(-1);-webkit-transform: scaleX(-1);"
  >
  <div class="pt-4 mt-4">
    <div class="font-bold text-xl mb-2">Danielle Li</div>
    <div class="text-gray-700 text-base">
      <p>Associate Professor</p>
      <p>MIT Sloan</p>
    </div>
    <nav class="pt-6 text-base">
      <ul>
        {% assign pages = site.pages | where_exp: "p", "p.custom_menu_order > 0" | sort: "custom_menu_order" %}
        {% for p in pages %}
        <li>
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
        <li>
          <a href="https://mitsloan.mit.edu/faculty/directory/danielle-li"
            class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
          >
            <span class="relative">Official Website</span>
          </a>
        </li>
        <li>
          <a href="https://scholar.google.com/citations?user=loXqXPQAAAAJ&hl=en"
            class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
          >
            <span class="relative">Google Scholar</span>
          </a>
        </li>
        <li>
          <a href=/assets/docs/CV_Current.pdf
            class="py-1 transition duration-200 ease-in-out relative block font-medium hover:translate-x-2px hover:text-gray-900 text-gray-600"
          >
            <span class="relative">CV</span>
          </a>
        </li>
      </ul>
    </nav>
  </div>
</div>
