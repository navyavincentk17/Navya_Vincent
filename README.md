<section
  id="main"
  class="flex flex-col md:flex-row items-center justify-center py-16 md:h-screen border-b-2"
>
  <div class="md:mx-2">
    <img
      class="object-cover w-full h-full sm:w-80 sm:h-80 sm:rounded-full"
      src="{{ page.image | relative_url | default: 'https://ik.imagekit.io/ikmedia/avif_samples/photo3_avif_6O32dW2NT.png' }}"
      alt="{{ page.description }}"
    />
  </div>
  <div class="fadeIn mx-4 w-4/5 md:w-2/5 text-center md:text-left mt-6 md:mt-0">
    <div class="prose prose-h1:mb-1">{{ page.main_content | markdownify }}</div>
    {% if site.contact_channels_section %}
    <p class="mt-4">
      {{ site.data[site.active_lang].strings.home.contact_me | default:
      site.data['en'].strings.home.contact_me}}
    </p>

    {%include contact_channels.html %} {% endif %}
  </div>
</section>
