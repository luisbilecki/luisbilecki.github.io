---
layout: single
title: "Contato"
permalink: /contact/
author_profile: false
---

<div class="under-construction terminal-page">
  <div class="terminal">
    <div class="terminal__bar">
      <span class="terminal__dot"></span>
      <span class="terminal__dot"></span>
      <span class="terminal__dot"></span>
    </div>
    <div class="terminal__body">
      <p class="terminal__prompt">luis@bilecki <span class="path">~/contact</span> $ cat links.txt</p>
      <ul class="term-links">
        <li><a href="https://github.com/luisbilecki" rel="me noopener" target="_blank"><i class="fab fa-fw fa-github" aria-hidden="true"></i> github.com/luisbilecki</a></li>
        <li><a href="https://www.linkedin.com/in/luisbilecki/" rel="me noopener" target="_blank"><i class="fab fa-fw fa-linkedin" aria-hidden="true"></i> linkedin.com/in/luisbilecki</a></li>
        <li><a href="mailto:me@luisbilecki.com"><i class="fas fa-fw fa-envelope" aria-hidden="true"></i> me@luisbilecki.com</a></li>
      </ul>

      <p class="terminal__prompt">luis@bilecki <span class="path">~/contact</span> $ ./send-message.sh</p>

      <form class="term-form" id="contact-form">
        <label for="cf-name" lang="pt-BR" data-lang="pt-br">--name (seu nome)</label>
        <label for="cf-name" lang="en" data-lang="en" hidden>--name (your name)</label>
        <label for="cf-name" lang="es" data-lang="es" hidden>--name (tu nombre)</label>
        <input type="text" id="cf-name" name="name" required>

        <label for="cf-message" lang="pt-BR" data-lang="pt-br">--message (sua mensagem)</label>
        <label for="cf-message" lang="en" data-lang="en" hidden>--message (your message)</label>
        <label for="cf-message" lang="es" data-lang="es" hidden>--message (tu mensaje)</label>
        <textarea id="cf-message" name="message" rows="5" required></textarea>

        <button type="submit">
          <span lang="pt-BR" data-lang="pt-br">enviar --to me@luisbilecki.com</span>
          <span lang="en" data-lang="en" hidden>send --to me@luisbilecki.com</span>
          <span lang="es" data-lang="es" hidden>enviar --to me@luisbilecki.com</span>
        </button>
      </form>

      <p class="terminal__prompt"><a href="{{ '/' | relative_url }}">luis@bilecki <span class="path">~/contact</span> $ cd ~</a></p>

      {% include lang-switch.html %}
    </div>
  </div>
</div>

<script>
  (function () {
    var form = document.getElementById("contact-form");
    form.addEventListener("submit", function (e) {
      e.preventDefault();
      var name = document.getElementById("cf-name").value;
      var message = document.getElementById("cf-message").value;
      var subject = encodeURIComponent("Contato via luisbilecki.com — " + name);
      var body = encodeURIComponent(message + "\n\n— " + name);
      window.location.href = "mailto:me@luisbilecki.com?subject=" + subject + "&body=" + body;
    });
  })();
</script>
