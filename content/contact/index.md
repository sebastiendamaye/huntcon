---
title: "Contact"
description: "Get in touch with the HUNTCON 2027 organizers"
layout: "simple"
---

Have questions about HUNTCON 2027? Reach out to us using the form below.

<form id="contact-form" action="https://formspree.io/f/placeholder" method="POST" class="mt-8 space-y-6 max-w-2xl">
  <input type="hidden" name="_to" value="sebastien.damaye@se.com" />

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

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Send Message
  </button>
</form>

<p class="mt-6 text-sm text-neutral-500">
  Or email us directly at <a href="mailto:sebastien.damaye@se.com" class="text-cyan-400 hover:underline">sebastien.damaye@se.com</a>
</p>
