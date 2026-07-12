---
title: Supported Players
description: A list of the media players supported by Music Presence.
icon: lucide/music
hide:
    - navigation
    - toc
    - tags
---

<!-- Workaround until https://github.com/zensical/backlog/issues/120 is implemented. -->
<style>
.md-content__button {
    display: none;
}
</style>

# Supported Media Players

Browse the list of media players that are supported by Music Presence. Note that some media players might need a plugin or helper program to work and website support is currently only limited to websites in Firefox-based browsers on Linux. Read [Media Player Setup](../setup/media-player.md) for more information.

  <div class="mp-controls">
    <div class="mp-search">
      <input type="text" id="search" placeholder="Search players..." aria-label="Search players" />
    </div>
    <div class="mp-filters">
      <button type="button" class="mp-btn" data-platform="windows"><img class="mp-filter-icon" src="/_static/images/media-players/windows-11.png" alt="Windows" />Windows</button>
      <button type="button" class="mp-btn" data-platform="mac"><img class="mp-filter-icon" src="/_static/images/media-players/mac-os.png" alt="Mac" />Mac</button>
      <button type="button" class="mp-btn" data-platform="linux"><img class="mp-filter-icon" src="/_static/images/media-players/linux.png" alt="Linux" />Linux</button>
      <button type="button" class="mp-btn" data-platform="web"><img class="mp-filter-icon" src="/_static/images/media-players/web.png" alt="Web" />Web</button>
    </div>
  </div>

  <div class="mp-grid" id="grid"></div>

  <div class="mp-no-results" id="noResults" style="display: none;">No players found with that name. Try searching for another one.</div>

<style>
.mp-intro {
  max-width: 1000px;
  margin: 0 auto 1.5rem;
  padding: 0 1rem;
  line-height: 1.75;
}

.mp-summary {
  margin-bottom: 1.5rem;
  line-height: 1.7;
  color: #4b5563;
}
.mp-controls {
    margin-top: 2rem;
  display: grid;
  gap: 1rem;
  margin-bottom: 1rem;
}
.mp-search input {
  width: 100%;
  border: 1px solid #E5E7EB;
  border-radius: 12px;
  padding: 0.75em 1rem;
  font-size: 1.25em;
  background: #ffffff;
  color: #252525;
}
.mp-search input::placeholder {
  color: #7d7d7d;
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
  border: 1px solid #d5d5d5;
  background: #f9fafb;
  color: #111827;
  border-radius: 999px;
  padding: 0.4rem 0.75rem;
  cursor: pointer;
  transition: background 0.16s, border-color 0.16s;
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
}
.mp-filter-icon {
  width: 16px;
  height: 16px;
  display: inline-block;
}
.mp-btn:hover,
.mp-btn.active {
  background: #333;
  color: #ffffff;
  border-color: #333;
}
.mp-btn:hover .mp-filter-icon,
.mp-btn.active .mp-filter-icon {
    filter: brightness(0) invert(1);
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
  grid-template-columns: repeat(3, 1fr);
  gap: 0.9rem;
}

@media (max-width: 1200px) {
  .mp-grid { grid-template-columns: repeat(2, 1fr); }
}

@media (max-width: 700px) {
  .mp-grid { grid-template-columns: 1fr; }
}
.mp-card {
  background: #f8fafc;
  border: 1px solid #e5e7eb;
  border-radius: 10px;
  padding: 0.9rem;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  overflow: hidden;
}
.mp-card-header {
  display: flex;
  align-items: center;
  gap: 0.85rem;
  margin-bottom: 1rem;
}
.mp-card-logo,
 .mp-card-logo-fallback {
  width: 44px;
  height: 44px;
  flex-shrink: 0;
  border-radius: 6px;
  display: grid;
  place-items: center;
  color: #1e293b;
  font-weight: 700;
}
.mp-card-logo img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  border-radius: 0;
}
.mp-card-title {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}
.mp-card-title, .mp-card-title * {
  max-width: 100%;
  overflow: hidden;
}
.mp-player-url {
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  display: block;
  line-height: 1.2rem;
  max-width: 100%;
  word-break: keep-all;
  overflow-x: hidden;
  white-space: nowrap;
}
.mp-card-title .name {
  line-height: 1.15;
  margin: 0;
}
.mp-card-title .name div {
    font-size: 1.35em;
  font-weight: 600;
}
.mp-card-title .name a {
    color: #505050;
    text-decoration-color: #a1a1a1;
    font-size: 1em;
  font-weight: 500;
  opacity: 0.9;
  
}
.mp-card-title .name a:hover {
    color: #101010 !important;
  
}
.mp-card-title .id {
  color: #4b5563;
  font-size: 0.95rem;
}
.mp-platforms {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}
.mp-platform {
  cursor: default;
  user-select: none;
  display: inline-flex;
  align-items: center;
  gap: 0.25rem;
  padding: 0 0.45rem;
  border-radius: 999px;
  background: #f4f4f4;
  outline: 1px solid #d5d5d5;
  color: #1f2937;
  white-space: nowrap;
}
.mp-link {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  color: #5c8aee;
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

  [data-md-color-scheme="slate"] .mp-card-title .name a {
    color: #8b8b8b;
    text-decoration-color: #4e4e4e;
}
  [data-md-color-scheme="slate"] .mp-card-title .name a:hover {
    color: #8b8b8b !important;
  
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
    color: #e5e7eb58;
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
    background: #ddd;
    color: #000;
    border-color: #ddd;
  }
  [data-md-color-scheme="slate"] .mp-filter-icon {
    filter: brightness(0) invert(1);
  }
  [data-md-color-scheme="slate"] .mp-btn:hover .mp-filter-icon,
  [data-md-color-scheme="slate"] .mp-btn.active .mp-filter-icon {
    filter: none;
  }
  [data-md-color-scheme="slate"] .mp-sort select {
    background: #1B1B1B;
  }
  [data-md-color-scheme="slate"] .mp-card {
    background: #1B1B1B;
    border-color: #2f2f2f;
    color: #e8e8e8;
    border-radius: 12px;
  }
  [data-md-color-scheme="slate"] .mp-card-logo,
  [data-md-color-scheme="slate"] .mp-card-logo-fallback {
    background: #1B1B1B;
    color: #e5e7eb;
  }
  .mp-platform-icon {
    width: 15px;
    height: 15px;
    vertical-align: middle;
    margin-right: 0.25rem;
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
    outline: none;
  }
  [data-md-color-scheme="slate"] .mp-no-results,
  [data-md-color-scheme="slate"] .mp-footer {
    color: #94a3b8;
  }
</style>

<script>
(function () {
  const DATA_URL = 'https://live.musicpresence.app/v3/players.json';
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
      Windows: '/_static/images/media-players/windows-11.png',
      Mac: '/_static/images/media-players/mac-os.png',
      Linux: '/_static/images/media-players/linux.png',
      Web: '/_static/images/media-players/web.png'
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
      const nameText = document.createElement('div');
      nameText.textContent = player.name;
      nameDiv.appendChild(nameText);

      if (player.url) {
        const urlLink = document.createElement('a');
        urlLink.className = 'mp-player-url';
        urlLink.href = player.url;
        urlLink.target = '_blank';
        urlLink.rel = 'noopener';
        urlLink.textContent = player.url.replace(/^https?:\/\//, '');
        nameDiv.appendChild(urlLink);
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
          platformImg.width = 12;
          platformImg.height = 12;

          platformTag.appendChild(platformImg);
          platformTag.appendChild(document.createTextNode(pl));
          platformList.appendChild(platformTag);
        });
        card.appendChild(platformList);
      }

      grid.appendChild(card);
    });
  }

  function normalizeSearchText(text) {
    return String(text || '')
      .toLowerCase()
      .replace(/[^a-z0-9]+/g, ' ')
      .trim();
  }

  function extractSearchTerms(player) {
    const terms = [];
    if (player.name) terms.push(player.name);
    if (player.id) terms.push(player.id);
    if (player.url) terms.push(player.url);

    const platforms = getPlatforms(player);
    terms.push(...platforms);

    if (player.represents) {
      if (Array.isArray(player.represents)) {
        terms.push(...player.represents);
      } else if (typeof player.represents === 'object') {
        terms.push(...Object.values(player.represents));
      } else {
        terms.push(player.represents);
      }
    }

    if (player.sources && typeof player.sources === 'object') {
      terms.push(...Object.keys(player.sources));
      terms.push(...Object.values(player.sources));
    }

    if (player.experimental && typeof player.experimental === 'object') {
      terms.push(...Object.keys(player.experimental));
      terms.push(...Object.values(player.experimental));
    }

    return normalizeSearchText(terms.filter(Boolean).join(' '));
  }

  function applyFilter() {
    if (!searchInput) return;
    const query = normalizeSearchText(searchInput.value);
    filtered = players.filter(player => {
      const platforms = getPlatforms(player);
      const searchText = extractSearchTerms(player);
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
        players = data.players.filter(p => {
          const id = p.id.toLowerCase();
          const name = (p.name || '').toLowerCase();
          return !id.includes('placeholder') && name !== 'media';
        });
        icons = data.icons || {};
        filtered = [...players];
        render();
      })
      .catch(error => {
        console.error('Error loading data', error);
        if (grid) {
          grid.innerHTML = '<div class="mp-no-results">Error loading data. Please refresh the page.</div>';
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
