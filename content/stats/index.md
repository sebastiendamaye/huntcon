---
title: "Registration Statistics"
description: "HUNTCON 2027 registration statistics"
layout: "simple"
---

<div id="stats-loading" class="text-neutral-400">Loading statistics...</div>
<div id="stats-error" class="hidden text-red-400"></div>

<div id="stats-content" class="hidden space-y-8">

  <div class="p-6 rounded-lg border border-neutral-700 bg-neutral-800/50">
    <p class="text-sm text-neutral-400 uppercase tracking-wider">Total Registrations</p>
    <p id="stat-total" class="text-4xl font-bold text-cyan-400 mt-1"></p>
  </div>

  <div>
    <h2 class="text-2xl font-bold mb-4">Roles</h2>
    <table class="w-full text-left border-collapse">
      <thead>
        <tr class="border-b border-neutral-700">
          <th class="py-2 pr-4 text-neutral-400 font-medium">Role</th>
          <th class="py-2 text-neutral-400 font-medium">Count</th>
        </tr>
      </thead>
      <tbody id="roles-tbody"></tbody>
    </table>
  </div>

  <div>
    <h2 class="text-2xl font-bold mb-4">Round Table Topics</h2>
    <table class="w-full text-left border-collapse">
      <thead>
        <tr class="border-b border-neutral-700">
          <th class="py-2 pr-4 text-neutral-400 font-medium">Topic</th>
          <th class="py-2 text-neutral-400 font-medium">Participants</th>
        </tr>
      </thead>
      <tbody id="topics-tbody"></tbody>
    </table>
  </div>

</div>

<script>
(function() {
  var STATS_URL = 'https://script.google.com/macros/s/AKfycbyJ2nz-woupO7Y07qzJvbUyWgjN5PxiTmbw4unMlhpZhHKn5qmlYrgqJ8KhBU4s6vigBg/exec';

  fetch(STATS_URL)
    .then(function(r) { return r.json(); })
    .then(function(data) {
      document.getElementById('stats-loading').classList.add('hidden');
      document.getElementById('stats-content').classList.remove('hidden');

      document.getElementById('stat-total').textContent = data.total;

      var rolesBody = document.getElementById('roles-tbody');
      var roles = [
        { label: 'Speakers', key: 'speakers' },
        { label: 'Round Table Participants', key: 'round_table' },
        { label: 'Exhibitors', key: 'exhibitors' }
      ];
      roles.forEach(function(role) {
        var tr = document.createElement('tr');
        tr.className = 'border-b border-neutral-700/50';
        tr.innerHTML = '<td class="py-2 pr-4">' + role.label + '</td><td class="py-2 font-mono">' + (data.roles[role.key] || 0) + '</td>';
        rolesBody.appendChild(tr);
      });

      var topicsBody = document.getElementById('topics-tbody');
      var topics = data.topics || {};
      Object.keys(topics).forEach(function(topic) {
        var tr = document.createElement('tr');
        tr.className = 'border-b border-neutral-700/50';
        tr.innerHTML = '<td class="py-2 pr-4">' + topic + '</td><td class="py-2 font-mono">' + topics[topic] + '</td>';
        topicsBody.appendChild(tr);
      });
    })
    .catch(function(err) {
      document.getElementById('stats-loading').classList.add('hidden');
      document.getElementById('stats-error').classList.remove('hidden');
      document.getElementById('stats-error').textContent = 'Failed to load statistics.';
    });
})();
</script>
