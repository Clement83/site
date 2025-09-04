---
title: "Freelance – Gestion d'entreprise"
---

<section class="hero reveal">
  <div class="container">
    <h1>Votre partenaire en <span class="accent">gestion d’entreprise</span></h1>
    <p class="subtitle">
      Facturation • Secrétariat • Organisation — Gagnez du temps, je m’occupe de l’administratif.
    </p>
    <a class="btn btn-primary" href="#contact">Me contacter</a>
  </div>
</section>

<section class="features reveal">
  <div class="container">
    <h2>Ce que je fais</h2>
    <div class="grid">
      <div class="card">
        <h3>Facturation & Suivi</h3>
        <p>Création des devis/factures, relances, rapprochements — process clair et traçable.</p>
      </div>
      <div class="card">
        <h3>Secrétariat</h3>
        <p>Gestion d’e-mails, rédaction, classement documentaire, préparation de dossiers.</p>
      </div>
      <div class="card">
        <h3>Organisation</h3>
        <p>Structuration des workflows, modèles, checklists, tableaux de bord simples.</p>
      </div>
    </div>
  </div>
</section>

<section class="about reveal">
  <div class="container">
    <h2>Pourquoi travailler avec moi ?</h2>
    <ul class="benefits">
      <li>🔒 Fiable & discret — respect strict de la confidentialité</li>
      <li>⚡ Réactif — vous avez une réponse rapide et claire</li>
      <li>🧩 Flexible — missions ponctuelles ou récurrentes</li>
      <li>💬 Communication simple — un seul contact, pas de jargon</li>
    </ul>
  </div>
</section>

<section id="contact" class="contact reveal">
  <div class="container">
    <h2>Contact</h2>
    <p>Un projet, une question ? Écrivez-moi :</p>

    <!-- Formulaire mailto : ouvre le client mail de l'utilisateur -->
    <form class="contact-form" action="mailto:prenom.nom@exemple.com?subject=Contact%20depuis%20le%20site" method="post" enctype="text/plain">
      <div class="row">
        <label for="name">Votre nom</label>
        <input id="name" name="Nom" type="text" required />
      </div>
      <div class="row">
        <label for="email">Votre e-mail</label>
        <input id="email" name="Email" type="email" required />
      </div>
      <div class="row">
        <label for="message">Message</label>
        <textarea id="message" name="Message" rows="5" required></textarea>
      </div>
      <button class="btn btn-primary" type="submit">Envoyer</button>
      <p class="hint">💡 Le bouton ouvre votre logiciel de messagerie (pas d’envoi côté serveur).</p>
    </form>

    <div class="alt-contact">
      <p>Ou écrivez-moi directement : <a href="mailto:prenom.nom@exemple.com">prenom.nom@exemple.com</a></p>
    </div>
  </div>
</section>

<!-- Petite animation au scroll (IntersectionObserver) -->
<script>
  (function () {
    if (!('IntersectionObserver' in window)) {
      document.querySelectorAll('.reveal').forEach(el => el.classList.add('reveal--visible'));
      return;
    }
    const io = new IntersectionObserver((entries) => {
      entries.forEach(e => {
        if (e.isIntersecting) {
          e.target.classList.add('reveal--visible');
          io.unobserve(e.target);
        }
      });
    }, { threshold: 0.1 });
    document.querySelectorAll('.reveal').forEach(el => io.observe(el));
  })();
</script>
