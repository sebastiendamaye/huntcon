---
title: "Call for Papers"
description: "Submit your presentation for HUNTCON 2027"
layout: "simple"
---

We invite security professionals, researchers, and practitioners to submit presentations on threat hunting topics.

<form id="cfp-form" action="https://formspree.io/f/placeholder" method="POST" enctype="multipart/form-data" class="mt-8 space-y-6 max-w-2xl">

  <div>
    <label for="affiliation" class="block text-sm font-medium mb-1">Affiliation (Company) <span class="text-red-400">*</span></label>
    <input type="text" id="affiliation" name="affiliation" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
  </div>

  <fieldset class="border border-neutral-700 rounded-lg p-4">
    <legend class="text-sm font-semibold px-2">Primary Speaker <span class="text-red-400">*</span></legend>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-2">
      <div>
        <label for="primary-first" class="block text-sm font-medium mb-1">First Name <span class="text-red-400">*</span></label>
        <input type="text" id="primary-first" name="primary_first_name" required
          class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
      </div>
      <div>
        <label for="primary-last" class="block text-sm font-medium mb-1">Last Name <span class="text-red-400">*</span></label>
        <input type="text" id="primary-last" name="primary_last_name" required
          class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
      </div>
    </div>
    <div class="mt-4">
      <label for="primary-email" class="block text-sm font-medium mb-1">Email <span class="text-red-400">*</span></label>
      <input type="email" id="primary-email" name="primary_email" required
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
  </fieldset>

  <fieldset class="border border-neutral-700 rounded-lg p-4">
    <legend class="text-sm font-semibold px-2">Secondary Speaker (Optional)</legend>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-2">
      <div>
        <label for="secondary-first" class="block text-sm font-medium mb-1">First Name</label>
        <input type="text" id="secondary-first" name="secondary_first_name"
          class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
      </div>
      <div>
        <label for="secondary-last" class="block text-sm font-medium mb-1">Last Name</label>
        <input type="text" id="secondary-last" name="secondary_last_name"
          class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
      </div>
    </div>
    <div class="mt-4">
      <label for="secondary-email" class="block text-sm font-medium mb-1">Email</label>
      <input type="email" id="secondary-email" name="secondary_email"
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
  </fieldset>

  <div>
    <label for="title" class="block text-sm font-medium mb-1">Presentation Title <span class="text-red-400">*</span></label>
    <input type="text" id="title" name="presentation_title" required maxlength="100"
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    <p class="text-xs text-neutral-500 mt-1">Maximum 100 characters</p>
  </div>

  <div>
    <label for="description" class="block text-sm font-medium mb-1">Presentation Description <span class="text-red-400">*</span></label>
    <textarea id="description" name="presentation_description" required rows="6"
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none"></textarea>
  </div>

  <div>
    <label for="upload" class="block text-sm font-medium mb-1">Presentation Upload (PDF only) <span class="text-red-400">*</span></label>
    <input type="file" id="upload" name="presentation_file" required accept=".pdf,application/pdf"
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 file:mr-4 file:py-2 file:px-4 file:rounded-lg file:border-0 file:bg-cyan-600 file:text-white file:font-semibold file:cursor-pointer" />
    <p class="text-xs text-neutral-500 mt-1">Only PDF format is accepted</p>
  </div>

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Submit Proposal
  </button>
</form>

<script>
document.getElementById('upload').addEventListener('change', function(e) {
  const file = e.target.files[0];
  if (file && file.type !== 'application/pdf') {
    alert('Only PDF files are accepted.');
    e.target.value = '';
  }
});
</script>
