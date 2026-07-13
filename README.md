# OWO — Octopus Welfare Organisatie

De volledige website van OWO vzw, met jullie **echte logo's** verwerkt in de navigatie, hero, loader, nieuwsbrief-popup en footer.

## Wat zit erin

```
owo-website/
├── index.html          ← de volledige site (één bestand)
├── assets/
│   ├── logo-primary.svg ← koraalrode octopus (hoofdlogo, overal gebruikt)
│   ├── logo-aqua.svg    ← turquoise variant (reserve)
│   ├── logo-dark.svg    ← gouden variant (reserve)
│   └── favicon.png      ← favicon, gemaakt uit het hoofdlogo
├── vercel.json          ← configuratie voor Vercel
└── README.md
```

De site heeft alles wat je vroeg: hero, over ons, waarom octopussen, de dreiging (tijdlijn),
missie, hoe je helpt, shop met winkelwagen/verlanglijst/afrekenen/kortingscode, nieuws,
galerij, FAQ, contact, footer, plus donkere modus, NL/EN-schakelaar, doneerknop,
cookiebanner, nieuwsbrief-popup en scroll-animaties.

Wil je een andere logo-variant als hoofdlogo? Vervang de verwijzingen naar
`assets/logo-primary.svg` in `index.html` door `assets/logo-aqua.svg` of `assets/logo-dark.svg`.

---

## Online zetten via Vercel

Je hebt twee manieren. **Manier A (slepen)** is het makkelijkst en vereist niets technisch.

### Manier A — Slepen en neerzetten (aanbevolen, geen account-koppeling nodig)

1. Ga naar **https://vercel.com** en maak een gratis account aan (of log in).
2. Klik rechtsboven op **Add New… → Project**.
3. Onderaan zie je **"Deploy a template"** — negeer dat; zoek de optie om
   **een map te uploaden**. De snelste route: ga naar **https://vercel.com/new** en
   sleep de **hele map `owo-website`** in het uploadvenster.
   - Zorg dat je de **map** sleept, niet alleen `index.html`, zodat de `assets/` map meegaat.
4. Vercel detecteert automatisch dat het een statische site is (geen build nodig).
   Klik op **Deploy**.
5. Na ~20 seconden krijg je een live URL zoals `https://owo-website-xxxx.vercel.app`.

Klaar. Wil je een eigen domein (bv. `owo-octopus.org`)? Ga in het project naar
**Settings → Domains** en volg de stappen.

### Manier B — Via de Vercel CLI (voor wie de terminal gebruikt)

```bash
# 1. Installeer de CLI (eenmalig)
npm install -g vercel

# 2. Ga in de projectmap staan
cd owo-website

# 3. Deploy
vercel

# Volg de vragen (kies je account, projectnaam, standaard instellingen).
# Voor de definitieve productie-URL:
vercel --prod
```

### Manier C — Via GitHub (als je updates via Git wilt beheren)

1. Maak een GitHub-repository en push de inhoud van `owo-website/` erin.
2. Ga op Vercel naar **Add New… → Project → Import Git Repository**.
3. Selecteer je repo. Laat alle build-instellingen leeg (het is een statische site).
4. Klik **Deploy**. Elke nieuwe push naar de hoofdtak zet automatisch een update live.

---

## Belangrijk om te weten

- De site is **puur statisch** — er is geen build-stap, geen framework en geen server nodig.
  Dat maakt hosten op Vercel gratis en supersnel.
- Contactformulier, nieuwsbrief, doneren en afrekenen zijn **volledig interactief maar
  demo's**: er wordt niets echt verzonden of afgeschreven. Voor echte betalingen koppel je
  later bv. Stripe of Mollie; voor e-mails een dienst zoals Formspree of je eigen backend.
- Productafbeeldingen zijn emoji-plaatshouders, klaar om door echte foto's vervangen te worden.
