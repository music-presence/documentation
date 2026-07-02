---
title: Supported Players
description: A list of the media players supported by Music Presence.
icon: lucide/music
---

#Supported Media Players

This is the list of every media player supported by Music Presence, search your media player to see if it's supported.

If you have trouble finding your player, sort it by platform.

<div class="mp-page">
  <div class="mp-controls">
    <div class="mp-search">
      <input type="text" id="search" placeholder="Search players..." aria-label="Search players" />
    </div>

    <div class="mp-filters">
      <span class="mp-filter-label">Platform:</span>
      <button type="button" class="mp-btn" data-platform="windows"><img class="mp-filter-icon" src="../_static/images/platform/windows-11.png" alt="Windows" />Windows</button>
      <button type="button" class="mp-btn" data-platform="mac"><img class="mp-filter-icon" src="../_static/images/platform/mac-os.png" alt="Mac" />Mac</button>
      <button type="button" class="mp-btn" data-platform="linux"><img class="mp-filter-icon" src="../_static/images/platform/linux.png" alt="Linux" />Linux</button>
      <button type="button" class="mp-btn" data-platform="web"><img class="mp-filter-icon" src="../_static/images/platform/web.png" alt="Web" />Web</button>
    </div>
  </div>

  <div class="mp-grid" id="grid"></div>

  <div class="mp-no-results" id="noResults" style="display: none;">No players found with that name. Try searching for another one.</div>
</div>

<style>
.mp-page {
  margin: 1rem 0;
  background: #ffffff;
  color: #111827;
  border-radius: 16px;
  padding: 1.5rem;
  border: 1px solid #e5e7eb;
}
.mp-summary {
  margin-bottom: 1.5rem;
  line-height: 1.7;
  color: #4b5563;
}
.mp-controls {
  display: grid;
  gap: 1rem;
  margin-bottom: 1.5rem;
}
.mp-search input {
  width: 100%;
  border: 1px solid #d1d5db;
  border-radius: 12px;
  padding: 0.85rem 1rem;
  font-size: 1rem;
  background: #ffffff;
  color: #111827;
}
.mp-search input::placeholder {
  color: #6b7280;
}
.mp-filters,
.mp-sort {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.75rem;
}
.mp-filter-label {
  font-weight: 600;
  color: #111827;
}
.mp-btn {
  border: 1px solid #d1d5db;
  background: #f9fafb;
  color: #111827;
  border-radius: 999px;
  padding: 0.6rem 1rem;
  cursor: pointer;
  transition: background 0.2s, border-color 0.2s;
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}
.mp-filter-icon {
  width: 18px;
  height: 18px;
  display: inline-block;
}
.mp-btn:hover,
.mp-btn.active {
  background: #2563eb;
  color: #ffffff;
  border-color: #2563eb;
}
.mp-sort select {
  min-width: 180px;
  border: 1px solid #d1d5db;
  background: #ffffff;
  color: #111827;
  border-radius: 12px;
  padding: 0.6rem 0.75rem;
}
.mp-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 1rem;
}
.mp-card {
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 12px;
  padding: 1rem;
}
.mp-card-header {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  margin-bottom: 1rem;
}
.mp-card-logo,
.mp-card-logo-fallback {
  width: 50px;
  height: 50px;
  flex-shrink: 0;
  border-radius: 16px;
  display: grid;
  place-items: center;
  background: #eef2ff;
  color: #1e293b;
  font-weight: 700;
  font-size: 1.1rem;
}
.mp-card-logo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  border-radius: 16px;
}
.mp-card-title {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}
.mp-card-title .name {
  font-weight: 700;
}
.mp-card-title .id {
  color: #4b5563;
  font-size: 0.95rem;
}
.mp-card-name-link {
  color: #1d4ed8;
  text-decoration: underline;
}
.mp-card-name-link:hover {
  color: #1e40af;
}
.mp-platforms {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin-bottom: 1rem;
}
.mp-platform {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.3rem 0.65rem;
  border-radius: 999px;
  background: #e2e8f0;
  color: #1f2937;
  font-size: 0.88rem;
}
.mp-link {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  color: #2563eb;
  font-weight: 600;
  text-decoration: none;
}
.mp-link:hover {
  text-decoration: underline;
}
.mp-no-results {
  padding: 1.5rem;
  color: #475569;
}
.mp-footer {
  margin-top: 1.5rem;
  font-size: 0.95rem;
  color: #475569;
}
  [data-md-color-scheme="slate"] .mp-page {
    background: #1B1B1B;
    color: #e5e7eb;
    border-color: #2f2f2f;
  }
  [data-md-color-scheme="slate"] .mp-summary {
    color: #cbd5e1;
  }
  [data-md-color-scheme="slate"] .mp-search input,
  [data-md-color-scheme="slate"] .mp-sort select {
    background: #1B1B1B;
    color: #e5e7eb;
    border-color: #2f2f2f;
  }
  [data-md-color-scheme="slate"] .mp-search input::placeholder {
    color: #94a3b8;
  }
  [data-md-color-scheme="slate"] .mp-filter-label {
    color: #e5e7eb;
  }
  [data-md-color-scheme="slate"] .mp-btn {
    border-color: #2f2f2f;
    background: #242424;
    color: #e5e7eb;
  }
  [data-md-color-scheme="slate"] .mp-btn:hover,
  [data-md-color-scheme="slate"] .mp-btn.active {
    background: #2563eb;
    color: #ffffff;
    border-color: #2563eb;
  }
  [data-md-color-scheme="slate"] .mp-filter-icon {
    filter: brightness(0) invert(1);
  }
  [data-md-color-scheme="slate"] .mp-sort select {
    background: #1B1B1B;
  }
  [data-md-color-scheme="slate"] .mp-card {
    background: #1B1B1B;
    border-color: #2f2f2f;
    color: #e5e7eb;
    border-radius: 12px;
  }
  [data-md-color-scheme="slate"] .mp-card-logo,
  [data-md-color-scheme="slate"] .mp-card-logo-fallback {
    background: #242424;
    color: #e5e7eb;
  }
  .mp-platform-icon {
    width: 14px;
    height: 14px;
    vertical-align: middle;
    margin-right: 0.35rem;
    filter: none;
  }
  [data-md-color-scheme="slate"] .mp-platform-icon {
    filter: brightness(0) invert(1);
  }
  [data-md-color-scheme="default"] .mp-platform-icon {
    filter: none;
  }
  [data-md-color-scheme="slate"] .mp-card-name-link {
    color: #93c5fd;
  }
  [data-md-color-scheme="slate"] .mp-card-name-link:hover {
    color: #60a5fa;
  }
  [data-md-color-scheme="slate"] .mp-platform {
    background: #242424;
    color: #e5e7eb;
  }
  [data-md-color-scheme="slate"] .mp-no-results,
  [data-md-color-scheme="slate"] .mp-footer {
    color: #94a3b8;
  }
</style>

<script>
(function () {
  const DATA_URL = 'https://live.musicpresence.app/v3/players.json';
  const playersToRemove = ['neutron-music-player-placeholder', 'metrolist', 'outertune', 'poweramp', 'media', 'netease-cloud-music-zh-placeholder', 'kugou-zh-placeholder', 'qishui-zh-placeholder', 'qq-music-zh-placeholder', 'adamp'];
  let players = [];
  let icons = {};
  let filtered = [];
  let currentPlatform = null;

  const grid = document.getElementById('grid');
  const noResults = document.getElementById('noResults');
  const searchInput = document.getElementById('search');

  function getPlatforms(player) {
    const p = new Set();
    const s = player.sources || {};
    if (s.win_winrt || s.win_legacy) p.add('Windows');
    if (s.mac_mediaremote || s.mac_nowplaying) p.add('Mac');
    if (s.lin_mpris) p.add('Linux');
    if (s.web_domain) p.add('Web');
    if (player.experimental && player.experimental.lin_mpris_identity) p.add('Linux');
    if (player.experimental && player.experimental.win_winrt_identity) p.add('Windows');
    if (player.experimental && player.experimental.mac_mediaremote_identity) p.add('Mac');
    return Array.from(p);
  }

  function getIcon(id) {
    if (!icons[id]) return null;
    const logo = icons[id].find(i => i.label === 'logo-128');
    return logo ? logo.url : null;
  }

  function getPlatformIcon(platform) {
    const iconsMap = {
      Windows: '../_static/images/platform/windows-11.png',
      Mac: '../_static/images/platform/mac-os.png',
      Linux: '../_static/images/platform/linux.png',
      Web: '../_static/images/platform/web.png'
    };
    return iconsMap[platform] || '';
  }

  function render() {
    if (!grid || !noResults) return;

    if (!filtered.length) {
      grid.innerHTML = '';
      noResults.style.display = 'block';
      return;
    }

    noResults.style.display = 'none';
    grid.innerHTML = '';

    filtered.forEach(player => {
      const platforms = getPlatforms(player);
      const iconUrl = getIcon(player.id);

      const card = document.createElement('article');
      card.className = 'mp-card';

      const header = document.createElement('div');
      header.className = 'mp-card-header';

      const logoElement = document.createElement('div');
      if (iconUrl) {
        logoElement.className = 'mp-card-logo';
        const img = document.createElement('img');
        img.src = iconUrl;
        img.alt = `${player.name} logo`;
        img.onerror = () => {
          const fallback = document.createElement('div');
          fallback.className = 'mp-card-logo-fallback';
          fallback.textContent = player.name?.charAt(0) || '';
          logoElement.replaceWith(fallback);
        };
        logoElement.appendChild(img);
      } else {
        logoElement.className = 'mp-card-logo-fallback';
        logoElement.textContent = player.name?.charAt(0) || '';
      }

      const title = document.createElement('div');
      title.className = 'mp-card-title';
      const nameDiv = document.createElement('div');
      nameDiv.className = 'name';
      if (player.url) {
        const nameLink = document.createElement('a');
        nameLink.className = 'mp-card-name-link';
        nameLink.href = player.url;
        nameLink.target = '_blank';
        nameLink.rel = 'noopener';
        nameLink.textContent = player.name;
        nameDiv.appendChild(nameLink);
      } else {
        nameDiv.textContent = player.name;
      }
      title.appendChild(nameDiv);

      header.appendChild(logoElement);
      header.appendChild(title);
      card.appendChild(header);

      if (platforms.length) {
        const platformList = document.createElement('div');
        platformList.className = 'mp-platforms';
        platforms.forEach(pl => {
          const platformTag = document.createElement('span');
          platformTag.className = 'mp-platform';

          const platformImg = document.createElement('img');
          platformImg.className = 'mp-platform-icon';
          platformImg.src = getPlatformIcon(pl);
          platformImg.alt = pl;
          platformImg.width = 14;
          platformImg.height = 14;

          platformTag.appendChild(platformImg);
          platformTag.appendChild(document.createTextNode(pl));
          platformList.appendChild(platformTag);
        });
        card.appendChild(platformList);
      }

      grid.appendChild(card);
    });
  }

  function applyFilter() {
    if (!searchInput) return;
    const query = searchInput.value.trim().toLowerCase();
    filtered = players.filter(player => {
      const platforms = getPlatforms(player);
      const searchText = `${player.name} ${player.id} ${platforms.join(' ')}`.toLowerCase();
      if (query && !searchText.includes(query)) return false;
      if (!currentPlatform) return true;
      return platforms.map(p => p.toLowerCase()).includes(currentPlatform);
    });
    render();
  }

  function attachListeners() {
    if (searchInput) {
      searchInput.addEventListener('input', applyFilter);
      searchInput.addEventListener('keydown', event => {
        if (event.key === 'Enter') {
          event.preventDefault();
          applyFilter();
        }
      });
    }

    const filterButtons = document.querySelectorAll('.mp-filters [data-platform]');
    filterButtons.forEach(button => {
      button.addEventListener('click', event => {
        event.preventDefault();
        const platform = button.dataset.platform;
        if (currentPlatform === platform) {
          currentPlatform = null;
          button.classList.remove('active');
        } else {
          filterButtons.forEach(btn => btn.classList.remove('active'));
          button.classList.add('active');
          currentPlatform = platform;
        }
        applyFilter();
      });
    });
  }

  function init() {
    if (!grid || !noResults || !searchInput) {
      return;
    }

    fetch(DATA_URL)
      .then(response => response.json())
      .then(data => {
        players = data.players.filter(p => !playersToRemove.includes(p.id.toLowerCase()));
        icons = data.icons || {};
        filtered = [...players];
        render();
      })
      .catch(error => {
        console.error('Error loading data', error);
        if (grid) {
          grid.innerHTML = '<div class="mp-no-results">Error loading data. Please update the page.</div>';
        }
      });

    attachListeners();
  }

  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', init);
  } else {
    init();
  }
})();
</script>
