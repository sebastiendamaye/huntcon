---
title: "Call for Papers"
description: "Submit your presentation for HUNTCON 2027"
layout: "simple"
---

- We invite security professionals, researchers, and practitioners to submit presentations on threat hunting topics.
- **Presentations in English are strongly recommended**, as we welcome attendees from across Europe. However, French submissions will also be accepted, since the majority of attendees will still be French-speaking.
- Each talk is allocated a **1-hour slot**, including 10 minutes for questions.
- Only PDF format is accepted for the presentation upload.
- Please wait until the confirmation message appears before leaving the page to ensure your submission is processed correctly.
- All submissions will be reviewed by the conference board. You will be notified of the outcome once the review process is complete.

<form id="cfp-form" class="mt-8 space-y-6 max-w-2xl">

  <div>
    <label for="company" class="block text-sm font-medium mb-1">Company <span class="text-red-400">*</span></label>
    <input type="text" id="company" name="company" required
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
    <label for="language" class="block text-sm font-medium mb-1">Language <span class="text-red-400">*</span></label>
    <select id="language" name="language" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none">
      <option value="English" selected>English</option>
      <option value="French">French</option>
    </select>
  </div>

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
    <p class="text-xs text-neutral-500 mt-1">Only PDF format is accepted (max 5MB)</p>
  </div>

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Submit Proposal
  </button>
</form>

<div id="cfp-success" class="hidden mt-8 p-6 rounded-lg border border-green-500/50 bg-green-500/10 max-w-2xl">
  <p class="text-green-400 font-semibold text-lg">Proposal submitted!</p>
  <p class="text-neutral-300 mt-2">Thank you for your submission. We will review your proposal and get back to you shortly.</p>
</div>

<script>
document.getElementById('upload').addEventListener('change', function(e) {
  var file = e.target.files[0];
  if (file && file.type !== 'application/pdf') {
    alert('Only PDF files are accepted.');
    e.target.value = '';
  }
  if (file && file.size > 5 * 1024 * 1024) {
    alert('File size must be under 5MB.');
    e.target.value = '';
  }
});

document.getElementById('cfp-form').addEventListener('submit', function(e) {
  e.preventDefault();
  var form = this;
  var button = form.querySelector('button[type="submit"]');
  var fileInput = document.getElementById('upload');
  var file = fileInput.files[0];

  if (!file) {
    alert('Please upload a PDF file.');
    return;
  }

  button.disabled = true;
  button.textContent = 'Uploading...';

  var reader = new FileReader();
  reader.onload = function() {
    var base64 = reader.result.split(',')[1];

    var formData = new FormData();
    formData.append('company', form.querySelector('[name="company"]').value);
    formData.append('primary_first_name', form.querySelector('[name="primary_first_name"]').value);
    formData.append('primary_last_name', form.querySelector('[name="primary_last_name"]').value);
    formData.append('primary_email', form.querySelector('[name="primary_email"]').value);
    formData.append('secondary_first_name', form.querySelector('[name="secondary_first_name"]').value);
    formData.append('secondary_last_name', form.querySelector('[name="secondary_last_name"]').value);
    formData.append('secondary_email', form.querySelector('[name="secondary_email"]').value);
    formData.append('language', form.querySelector('[name="language"]').value);
    formData.append('presentation_title', form.querySelector('[name="presentation_title"]').value);
    formData.append('presentation_description', form.querySelector('[name="presentation_description"]').value);
    formData.append('file_base64', base64);
    formData.append('file_name', file.name);

    fetch('https://script.google.com/macros/s/AKfycbwCnc_ylZHqrGm4aePJlPvHwdHYRcg4Xv3EFKXNRmWD27y0JnDykFDzsgbQtPBxA6DgVg/exec', {
      method: 'POST',
      body: formData,
      mode: 'no-cors',
    }).then(function() {
      form.classList.add('hidden');
      document.getElementById('cfp-success').classList.remove('hidden');
    }).catch(function() {
      form.classList.add('hidden');
      document.getElementById('cfp-success').classList.remove('hidden');
    });
  };
  reader.readAsDataURL(file);
});
</script>
