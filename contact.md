---
layout: page
title: Contact
permalink: /contact/
description: Tell Meta Limits a little about your books and we will help you find the right bookkeeping service.
page_class: contact-page
---

<div class="contact-layout">
  <section class="contact-intro">
    <h2>Start with what you know</h2>
    <p>Estimates are completely fine. A few details help us understand where to begin:</p>
    <ul>
      <li>Bookkeeping platform</li>
      <li>Approximate monthly transactions</li>
      <li>Number of bank and card accounts</li>
      <li>Whether prior months are up to date</li>
    </ul>
    <p>Prefer email? Write to <a href="mailto:hello@metalimits.com">hello@metalimits.com</a>.</p>
  </section>

  <form class="scope-form" id="scope-review">
    <label for="name">Your name</label>
    <input id="name" name="name" type="text" autocomplete="name" required />

    <label for="email">Email</label>
    <input id="email" name="email" type="email" autocomplete="email" required />

    <label for="business">Business name</label>
    <input id="business" name="business" type="text" autocomplete="organization" />

    <label for="looking-for">How can we help?</label>
    <select id="looking-for" name="looking-for">
      <option value="Monthly bookkeeping, not sure which tier">Monthly bookkeeping, not sure which tier</option>
      <option value="Monthly bookkeeping, I know which tier">Monthly bookkeeping, I know which tier</option>
      <option value="Catch-up or cleanup">Catch-up or cleanup</option>
      <option value="Both monthly bookkeeping and catch-up">Both monthly bookkeeping and catch-up</option>
      <option value="Something else">Something else</option>
    </select>

    <label for="message">Tell us a little about your books</label>
    <textarea id="message" name="message" rows="5" required></textarea>

    <button type="submit">Start the conversation</button>
    <p class="form-note">Your email app will open with these details ready to send.</p>
  </form>
</div>

<script>
  document.getElementById("scope-review").addEventListener("submit", function (event) {
    event.preventDefault();
    var form = event.currentTarget;
    var body = [
      "Name: " + form.name.value,
      "Email: " + form.email.value,
      "Business: " + form.business.value,
      "Need: " + form["looking-for"].value,
      "",
      form.message.value
    ].join("\n");
    window.location.href =
      "mailto:hello@metalimits.com?subject=" +
      encodeURIComponent("Bookkeeping inquiry") +
      "&body=" +
      encodeURIComponent(body);
  });
</script>
