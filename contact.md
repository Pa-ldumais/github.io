---
layout: default
title: Contact
---

<section class="fade-in">
<h2>Contact</h2>
<p>Réponse rapide à La Tuque.</p>

<form action="https://formspree.io/f/mdummy" method="post">
<label>Nom</label><br>
<input type="text" name="name" required><br><br>

<label>Email</label><br>
<input type="email" name="email" required><br><br>

<label>Message</label><br>
<textarea name="message" rows="5" required></textarea><br><br>

<button type="submit" class="btn">Envoyer</button>
</form>

<p>Ou par courriel: <a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
</section>
