---
title: "Registration"
description: "Register for HUNTCON 2027"
layout: "simple"
---

Register to attend HUNTCON 2027. Participation is free but registration is mandatory.

<form id="registration-form" action="https://script.google.com/macros/s/AKfycbyJ2nz-woupO7Y07qzJvbUyWgjN5PxiTmbw4unMlhpZhHKn5qmlYrgqJ8KhBU4s6vigBg/exec" method="POST" class="mt-8 space-y-6 max-w-2xl">

  <div>
    <label for="reg-affiliation" class="block text-sm font-medium mb-1">Affiliation (Company) <span class="text-red-400">*</span></label>
    <input type="text" id="reg-affiliation" name="affiliation" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
  </div>

  <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
    <div>
      <label for="reg-first" class="block text-sm font-medium mb-1">First Name <span class="text-red-400">*</span></label>
      <input type="text" id="reg-first" name="first_name" required
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
    <div>
      <label for="reg-last" class="block text-sm font-medium mb-1">Last Name <span class="text-red-400">*</span></label>
      <input type="text" id="reg-last" name="last_name" required
        class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
    </div>
  </div>

  <div>
    <label for="reg-email" class="block text-sm font-medium mb-1">Email <span class="text-red-400">*</span></label>
    <input type="email" id="reg-email" name="email" required
      class="w-full px-4 py-2 rounded-lg bg-neutral-800 border border-neutral-700 text-neutral-100 focus:border-cyan-500 focus:ring-1 focus:ring-cyan-500 outline-none" />
  </div>

  <div>
    <label class="block text-sm font-medium mb-2">Want to actively contribute? (optional)</label>
    <div class="space-y-2">
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="role" value="speaker"
          class="form-checkbox" onchange="toggleRoles()" />
        <span>Speaker</span>
      </label>
      <p id="speaker-note" class="hidden text-sm text-neutral-400 ml-6">(Please also use the <a href="/cfp/" class="text-cyan-400 hover:underline">Call for Papers</a> form to submit your presentation)</p>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="role" value="round_table"
          class="form-checkbox" onchange="toggleRoles()" />
        <span>Participant to a Round Table</span>
      </label>
    </div>
  </div>

  <div id="topics-section" class="hidden border border-neutral-700 rounded-lg p-4">
    <label class="block text-sm font-medium mb-2">Round Table Topics <span class="text-red-400">*</span> <span class="text-xs text-neutral-500">(select at least one)</span></label>
    <div class="space-y-2">
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="threat_hunting_frameworks"
          class="form-checkbox" />
        <span>Threat Hunting Frameworks</span>
      </label>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="ai_threat_hunting"
          class="form-checkbox" />
        <span>AI Applied to Threat Hunting</span>
      </label>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="vibe_hunting"
          class="form-checkbox" />
        <span>Vibe Hunting</span>
      </label>
    </div>
  </div>

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Register
  </button>
</form>

<div id="registration-success" class="hidden mt-8 p-6 rounded-lg border border-green-500/50 bg-green-500/10 max-w-2xl">
  <p class="text-green-400 font-semibold text-lg">Registration confirmed!</p>
  <p class="text-neutral-300 mt-2">Thank you for registering. We look forward to seeing you at HUNTCON 2027.</p>
</div>

<script>
function toggleRoles() {
  const speakerChecked = document.querySelector('input[name="role"][value="speaker"]').checked;
  const roundTableChecked = document.querySelector('input[name="role"][value="round_table"]').checked;
  const topicsSection = document.getElementById('topics-section');
  const topicCheckboxes = topicsSection.querySelectorAll('input[type="checkbox"]');
  const speakerNote = document.getElementById('speaker-note');

  if (roundTableChecked) {
    topicsSection.classList.remove('hidden');
    topicCheckboxes.forEach(cb => cb.removeAttribute('disabled'));
  } else {
    topicsSection.classList.add('hidden');
    topicCheckboxes.forEach(cb => {
      cb.checked = false;
      cb.setAttribute('disabled', 'disabled');
    });
  }

  if (speakerChecked) {
    speakerNote.classList.remove('hidden');
  } else {
    speakerNote.classList.add('hidden');
  }
}

document.getElementById('registration-form').addEventListener('submit', function(e) {
  e.preventDefault();
  var form = this;

  const roundTableChecked = document.querySelector('input[name="role"][value="round_table"]').checked;
  if (roundTableChecked) {
    const checked = document.querySelectorAll('#topics-section input[type="checkbox"]:checked');
    if (checked.length === 0) {
      alert('Please select at least one round table topic.');
      return;
    }
  }

  var button = form.querySelector('button[type="submit"]');
  button.disabled = true;
  button.textContent = 'Submitting...';

  fetch(form.action, {
    method: 'POST',
    body: new FormData(form),
    mode: 'no-cors',
  }).then(function() {
    form.classList.add('hidden');
    document.getElementById('registration-success').classList.remove('hidden');
  }).catch(function() {
    form.classList.add('hidden');
    document.getElementById('registration-success').classList.remove('hidden');
  });
});
</script>
