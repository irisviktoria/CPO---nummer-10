# CPO nummer 10 — App instructies

## Mappenstructuur in je GitHub repo

```
/
├── index.html          ← de app
├── manifest.json       ← PWA instellingen
├── sw.js               ← service worker (offline)
├── icon-192.png        ← app icoon (maak zelf, 192x192px)
├── icon-512.png        ← app icoon (maak zelf, 512x512px)
├── images/
│   ├── 3D_tekening_6-10.png
│   ├── Steen_Neo_Barok.png
│   ├── moodboard_keuken.png    ← hernoem je moodboard foto
│   ├── keuken_3d.png           ← hernoem je 3D keuken foto
│   └── plattegronden/
│       ├── begane-grond.jpg
│       └── eerste-verdieping.jpg
└── docs/
    ├── C24001_SIT-01_Situatie.pdf
    └── begroting.xlsx
```

---

## Plattegronden toevoegen

1. Zet je afbeelding in `/images/plattegronden/`
2. Open `index.html`, zoek naar `<!-- VOEG HIER JE PLATTEGRONDEN TOE -->`
3. Verwijder de `<!--` en `-->` commentaar-tekens rondom het voorbeeld
4. Pas de bestandsnaam en titel aan

---

## Moodboard foto's toevoegen

Zet je afbeeldingen in `/images/` en voeg ze toe in de moodboard sectie:

```html
<div class="mood-item" onclick="openLightbox(this)">
  <img src="images/jouw-foto.jpg" alt="Omschrijving">
</div>
```

Wil je een brede foto (volle breedte)? Gebruik `class="mood-item wide"`.

---

## Document toevoegen

Zet het bestand in `/docs/` en kopieer dit blok in de documenten sectie:

```html
<a class="doc-item" href="docs/jouw-bestand.pdf" target="_blank">
  <div class="doc-icon">📄</div>
  <div>
    <div class="doc-name">Naam van document</div>
    <div class="doc-meta">Datum · Omschrijving</div>
  </div>
  <div class="doc-arrow">›</div>
</a>
```

---

## Contact toevoegen

In de contacten sectie, kopieer dit blok:

```html
<div class="contact-card">
  <div class="contact-avatar">🔨</div>
  <div style="flex:1">
    <div class="contact-name">Naam</div>
    <div class="contact-role">Rol (bijv. Aannemer)</div>
    <div class="contact-detail">Telefoonnummer of adres</div>
    <div class="contact-actions">
      <a class="btn-contact" href="tel:0600000000">📞 Bellen</a>
      <a class="btn-contact" href="mailto:info@voorbeeld.nl">✉️ Mail</a>
    </div>
  </div>
</div>
```

---

## Planning aanpassen

Zoek in `index.html` de tijdlijn sectie. Elke stap heeft een klasse:
- `class="timeline-item done"` → afgerond (groen vinkje)
- `class="timeline-item active"` → huidige stap (roze)
- `class="timeline-item"` → nog te doen (grijs)

---

## Begroting bedragen invullen

Zoek de begroting sectie en pas de `€ —` bedragen aan naar jouw cijfers.

---

## App icoon maken

Je hebt twee PNG-bestanden nodig: `icon-192.png` en `icon-512.png`.
Maak ze op https://favicon.io of gebruik een foto van je huis.

---

## Voortgangsfoto's later zichtbaar voor anderen

Foto's die je uploadt via de app staan alleen op jouw telefoon (localStorage).
Wil je ze later voor anderen zichtbaar maken?

1. Stuur de foto naar jezelf
2. Upload hem naar `/images/voortgang/` in je GitHub repo
3. Voeg de naam toe aan de plattegronden of moodboard sectie

---

## GitHub Pages instellen

1. Ga naar je repository → Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: `main`, folder: `/ (root)`
4. Sla op → je app is live op `https://jouwusername.github.io/jouw-repo/`
