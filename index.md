---
layout: single
title: "Luís Felipe Bilecki"
permalink: /
author_profile: false
---

<div class="under-construction">
  <p class="monogram">LFB</p>
  <p class="uc-status">Luís Felipe Bilecki</p>

  <p class="uc-message" lang="pt-BR" data-lang="pt-br">Página em construção.</p>
  <p class="uc-message" lang="en" data-lang="en" hidden>Page under construction.</p>
  <p class="uc-message" lang="es" data-lang="es" hidden>Página en construcción.</p>

  <div class="lang-switch" role="group" aria-label="Idioma / Language / Idioma">
    <button type="button" data-set-lang="pt-br" aria-pressed="true">PT-BR</button>
    <button type="button" data-set-lang="en" aria-pressed="false">EN</button>
    <button type="button" data-set-lang="es" aria-pressed="false">ES</button>
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
