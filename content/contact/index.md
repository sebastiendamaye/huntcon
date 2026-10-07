---
title: "Contact"
description: "Get in touch with the HUNTCON 2027 organizers"
layout: "simple"
---

Have questions about HUNTCON 2027? Reach out to us using the form below.

<form id="contact-form" action="https://script.google.com/macros/s/AKfycbwQNEnwbQtXCB7NHBCkNVH4pE5HeESVHho_e-5LSK4wGj_AOQWSWuReA1gYot8_J7Fp0w/exec" method="POST" class="mt-8 space-y-6 max-w-2xl">

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
    <div>
      <label for="contact-first" class="block text-sm font-medium mb-1">First Name <span class="text-red-400">*</span></label>
      <input type="text" id="contact-first" name="first_name" required
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
    <div>
      <label for="contact-last" class="block text-sm font-medium mb-1">Last Name <span class="text-red-400">*</span></label>
      <input type="text" id="contact-last" name="last_name" required
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
  </div>

  <div>
    <label for="contact-email" class="block text-sm font-medium mb-1">Email <span class="text-red-400">*</span></label>
    <input type="email" id="contact-email" name="email" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
  </div>

  <div>
    <label for="contact-subject" class="block text-sm font-medium mb-1">Subject <span class="text-red-400">*</span></label>
    <input type="text" id="contact-subject" name="subject" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
  </div>

  <div>
    <label for="contact-message" class="block text-sm font-medium mb-1">Message <span class="text-red-400">*</span></label>
    <textarea id="contact-message" name="message" required rows="6"
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none"></textarea>
  </div>

  <!-- Honeypot: hidden from humans, bots tend to fill it. Server-side check rejects any submission where this is non-empty. -->
  <div aria-hidden="true" style="position:absolute; left:-9999px; top:-9999px;">
    <label for="contact-website">Website</label>
    <input type="text" id="contact-website" name="website" tabindex="-1" autocomplete="off" />
  </div>

  <div class="flex gap-2 border-t border-neutral-700 pt-4">
    <input type="checkbox" id="contact-gdpr-consent" name="gdpr_consent" value="yes" required
      class="form-checkbox mt-1 shrink-0 cursor-pointer" />
    <label for="contact-gdpr-consent" class="text-sm cursor-pointer">
      I agree that HUNTCON may store and process the information provided in this form (name, email address, subject and message) to answer my message. See our <a href="/privacy/" target="_blank" class="text-cyan-400 hover:underline">Privacy Notice</a>. <span class="text-red-400">*</span>
    </label>
  </div>

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Send Message
  </button>
</form>

<div id="contact-success" class="hidden mt-8 p-6 rounded-lg border border-green-500/50 bg-green-500/10 max-w-2xl">
  <p class="text-green-400 font-semibold text-lg">Message received!</p>
  <p class="text-neutral-300 mt-2">Thank you for reaching out. We will get back to you as soon as possible.</p>
</div>

<script>
var PRIVACY_NOTICE_VERSION = 'privacy_v1';

document.getElementById('contact-form').addEventListener('submit', function(e) {
  e.preventDefault();
  var form = this;
  var button = form.querySelector('button[type="submit"]');
  button.disabled = true;
  button.textContent = 'Sending...';

  var formData = new FormData(form);
  formData.append('consent_timestamp', new Date().toISOString());
  formData.append('privacy_notice_version', PRIVACY_NOTICE_VERSION);

  fetch(form.action, {
    method: 'POST',
    body: formData,
    mode: 'no-cors',
  }).then(function() {
    form.classList.add('hidden');
    document.getElementById('contact-success').classList.remove('hidden');
  }).catch(function() {
    form.classList.add('hidden');
    document.getElementById('contact-success').classList.remove('hidden');
  });
});
</script>
