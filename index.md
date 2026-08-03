---
layout: single
title: "Luís Felipe Bilecki"
permalink: /
author_profile: false
---

<div class="under-construction">
  <div class="terminal">
    <div class="terminal__bar">
      <span class="terminal__dot"></span>
      <span class="terminal__dot"></span>
      <span class="terminal__dot"></span>
    </div>
    <div class="terminal__body">
      <p class="terminal__prompt">luis@bilecki <span class="path">~</span> $ whoami</p>
      <p class="terminal__output">Luís Felipe Bilecki — Senior Software Engineer</p>

      <p class="terminal__prompt">luis@bilecki <span class="path">~</span> $ status --lang=pt-br</p>
      <p class="terminal__output" lang="pt-BR" data-lang="pt-br"><span class="status">[building]</span> Página em construção.<span class="cursor"></span></p>
      <p class="terminal__output" lang="en" data-lang="en" hidden><span class="status">[building]</span> Page under construction.<span class="cursor"></span></p>
      <p class="terminal__output" lang="es" data-lang="es" hidden><span class="status">[building]</span> Página en construcción.<span class="cursor"></span></p>

      <div class="lang-switch" role="group" aria-label="Idioma / Language / Idioma">
        <button type="button" data-set-lang="pt-br" aria-pressed="true">pt-br</button>
        <button type="button" data-set-lang="en" aria-pressed="false">en</button>
        <button type="button" data-set-lang="es" aria-pressed="false">es</button>
      </div>
    </div>
  </div>
</div>

<script>
  (function () {
    var buttons = document.querySelectorAll("[data-set-lang]");
    var messages = document.querySelectorAll("[data-lang]");

    function setLang(lang) {
      messages.forEach(function (el) {
        el.hidden = el.getAttribute("data-lang") !== lang;
      });
      buttons.forEach(function (btn) {
        btn.setAttribute("aria-pressed", btn.getAttribute("data-set-lang") === lang);
      });
      document.documentElement.setAttribute("lang", lang === "pt-br" ? "pt-BR" : lang);
    }

    buttons.forEach(function (btn) {
      btn.addEventListener("click", function () {
        setLang(btn.getAttribute("data-set-lang"));
      });
    });
  })();
</script>
