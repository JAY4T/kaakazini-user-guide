<!DOCTYPE html>
<html lang="{{ page.lang | default: site.lang | default: 'en' }}">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <meta name="description" content="{{ page.description | default: site.description | default: 'KaaKazini User Guide' | escape }}">

  <title>{% if page.title %}{{ page.title | escape }} | {% endif %}{{ site.title | default: 'KaaKazini User Guide' | escape }}</title>

  <!-- KaaKazini logo in the browser tab -->
  <link rel="icon" type="image/png" href="{{ '/assets/images/kazika.jpg' | relative_url }}">
  <link rel="apple-touch-icon" href="{{ '/assets/images/kazika.jpg' | relative_url }}">

  <!-- Custom stylesheet -->
  <link rel="stylesheet" href="{{ '/assets/css/style.css' | relative_url }}">
</head>

<body>
  <!-- Navigation bar -->
  <nav class="site-nav" aria-label="Main navigation">
    <a class="nav-brand" href="{{ '/' | relative_url }}" aria-label="KaaKazini User Guide home">
      <img
        src="{{ '/assets/images/kazika.jpg' | relative_url }}"
        alt="KaaKazini logo"
        class="nav-logo"
      >
      <span>KaaKazini</span>
    </a>

    <a class="nav-guide-link" href="{{ '/' | relative_url }}">User Guide</a>
  </nav>

  <!-- Page header -->
  <header class="page-header">
    <a class="header-logo-link" href="{{ '/' | relative_url }}" aria-label="KaaKazini home">
      <img
        src="{{ '/assets/images/kaakazini-logo.png' | relative_url }}"
        alt="KaaKazini logo"
        class="header-logo"
      >
    </a>

    <h1 class="project-name">
      {{ site.title | default: 'KaaKazini User Guide' | escape }}
    </h1>

    {% if site.description %}
      <p class="project-tagline">{{ site.description | escape }}</p>
    {% endif %}
  </header>

  <!-- Main content -->
  <main class="main-content">
    {{ content }}

    <footer class="site-footer">
      <span class="site-footer-owner">KaaKazini User Guide</span>
      <span class="site-footer-credits">Built to help users navigate KaaKazini.</span>
    </footer>
  </main>
</body>
</html>