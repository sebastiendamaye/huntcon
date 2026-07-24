---
title: "Registration"
description: "Register for HUNTCON 2027"
layout: "simple"
---

Register to attend HUNTCON 2027. Participation is free but registration is mandatory.

<form id="registration-form" action="https://formspree.io/f/placeholder" method="POST" class="mt-8 space-y-6 max-w-2xl">

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
    <label class="block text-sm font-medium mb-2">Participation Mode <span class="text-red-400">*</span></label>
    <div class="space-y-2">
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="radio" name="mode" value="attendee" required
          class="text-cyan-500 focus:ring-cyan-500" onchange="toggleTopics()" checked />
        <span>Attendee only</span>
      </label>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="radio" name="mode" value="round_table" required
          class="text-cyan-500 focus:ring-cyan-500" onchange="toggleTopics()" />
        <span>Participant to a Round Table</span>
      </label>
    </div>
  </div>

  <div id="topics-section" class="hidden border border-neutral-700 rounded-lg p-4">
    <label class="block text-sm font-medium mb-2">Round Table Topics <span class="text-red-400">*</span> <span class="text-xs text-neutral-500">(select at least one)</span></label>
    <div class="space-y-2">
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="threat_hunting_frameworks"
          class="text-cyan-500 focus:ring-cyan-500 rounded" />
        <span>Threat Hunting Frameworks</span>
      </label>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="ai_threat_hunting"
          class="text-cyan-500 focus:ring-cyan-500 rounded" />
        <span>AI Applied to Threat Hunting</span>
      </label>
      <label class="flex items-center gap-2 cursor-pointer">
        <input type="checkbox" name="topics" value="vibe_hunting"
          class="text-cyan-500 focus:ring-cyan-500 rounded" />
        <span>Vibe Hunting</span>
      </label>
    </div>
  </div>

  <button type="submit"
    class="px-8 py-3 rounded-lg bg-gradient-to-r from-cyan-500 to-violet-600 text-white font-semibold hover:opacity-90 transition-opacity cursor-pointer">
    Register
  </button>
</form>

<script>
function toggleTopics() {
  const mode = document.querySelector('input[name="mode"]:checked').value;
  const topicsSection = document.getElementById('topics-section');
  const checkboxes = topicsSection.querySelectorAll('input[type="checkbox"]');

  if (mode === 'round_table') {
    topicsSection.classList.remove('hidden');
    checkboxes.forEach(cb => cb.removeAttribute('disabled'));
  } else {
    topicsSection.classList.add('hidden');
    checkboxes.forEach(cb => {
      cb.checked = false;
      cb.setAttribute('disabled', 'disabled');
    });
  }
}

document.getElementById('registration-form').addEventListener('submit', function(e) {
  const mode = document.querySelector('input[name="mode"]:checked').value;
  if (mode === 'round_table') {
    const checked = document.querySelectorAll('#topics-section input[type="checkbox"]:checked');
    if (checked.length === 0) {
      e.preventDefault();
      alert('Please select at least one round table topic.');
    }
  }
});
</script>
