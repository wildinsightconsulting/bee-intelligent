---
layout: null
title: Bee Intelligent
description: An open scientific resource for standardized, biologically contextualized bee vibroacoustic data.
---

/* Bee Intelligent — landing page styles
   Token system: see index.md design plan. Keep this file as the site's
   single shared stylesheet as new pages (/atlas/, /standards/, etc.) are
   added, rather than duplicating styles per page. */

:root {
  --paper: #F6F5F1;
  --paper-alt: #EFEDE6;
  --ink: #1C1E1B;
  --ink-soft: #55564F;
  --slate: #2F4858;
  --amber: #8A5A2B;
  --moss: #5B6E52;
  --line: #DAD6C9;

  --font-serif: 'IBM Plex Serif', Georgia, 'Times New Roman', serif;
  --font-sans: 'IBM Plex Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-mono: 'IBM Plex Mono', ui-monospace, SFMono-Regular, Menlo, monospace;

  --max-width: 1120px;
}

*, *::before, *::after {
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

@media (prefers-reduced-motion: reduce) {
  html {
    scroll-behavior: auto;
  }
}

body {
  margin: 0;
  background: var(--paper);
  color: var(--ink);
  font-family: var(--font-sans);
  font-size: 1.0625rem;
  line-height: 1.6;
  -webkit-font-smoothing: antialiased;
}

.wrap {
  max-width: var(--max-width);
  margin: 0 auto;
  padding: 0 1.75rem;
}

h1, h2, h3 {
  font-family: var(--font-serif);
  font-weight: 600;
  line-height: 1.15;
  margin: 0;
  color: var(--ink);
}

p {
  margin: 0;
}

/* Skip link */

.skip-link {
  position: absolute;
  left: -9999px;
  top: auto;
  background: var(--ink);
  color: var(--paper);
  padding: 0.75rem 1.25rem;
  z-index: 100;
  font-family: var(--font-sans);
}

.skip-link:focus {
  left: 1rem;
  top: 1rem;
}

/* Focus visibility */

a:focus-visible,
button:focus-visible {
  outline: 2px solid var(--slate);
  outline-offset: 3px;
}

/* Header */

.site-header {
  padding: 2rem 0 0;
}

.wordmark {
  font-family: var(--font-serif);
  font-weight: 600;
  font-size: 1.125rem;
  letter-spacing: 0.01em;
  color: var(--ink);
}

/* Hero */

.hero {
  padding: 3.5rem 0 4rem;
  border-bottom: 1px solid var(--line);
}

.hero h1 {
  font-size: clamp(2.5rem, 4.5vw + 1rem, 4.25rem);
  letter-spacing: -0.01em;
}

.tagline {
  font-family: var(--font-serif);
  font-style: italic;
  font-size: clamp(1.125rem, 1.2vw + 0.75rem, 1.375rem);
  color: var(--ink-soft);
  margin-top: 0.75rem;
}

.hero-wave {
  display: block;
  width: 100%;
  height: auto;
  margin: 2.75rem 0 2.5rem;
}

.wave {
  stroke-dasharray: 2400;
  stroke-dashoffset: 0;
}

@media (prefers-reduced-motion: no-preference) {
  .wave {
    animation: draw-wave 1.8s ease-out 1;
  }
  .wave-slate {
    animation-delay: 0.15s;
  }
  @keyframes draw-wave {
    from {
      stroke-dashoffset: 2400;
    }
    to {
      stroke-dashoffset: 0;
    }
  }
}

.lead {
  max-width: 62ch;
  font-size: clamp(1.0625rem, 0.5vw + 0.95rem, 1.1875rem);
  color: var(--ink-soft);
}

/* Sections grid */

.sections {
  padding: 4rem 0 4.5rem;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 3rem 2.5rem;
}

@media (max-width: 720px) {
  .grid {
    grid-template-columns: 1fr;
    gap: 2.5rem;
  }
}

.card {
  border-top: 1px solid var(--line);
  padding-top: 1.5rem;
}

.glyph {
  width: 34px;
  height: 34px;
  margin-bottom: 1rem;
}

.card h2 {
  font-size: 1.375rem;
  margin-bottom: 0.4rem;
}

.descriptor {
  font-family: var(--font-serif);
  font-style: italic;
  color: var(--ink-soft);
  font-size: 0.9375rem;
  margin-bottom: 0.85rem;
}

.card p:not(.descriptor) {
  color: var(--ink-soft);
  font-size: 0.9375rem;
  max-width: 42ch;
  margin-bottom: 1.1rem;
}

.status {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  font-family: var(--font-mono);
  font-size: 0.75rem;
  color: var(--ink-soft);
  letter-spacing: 0.02em;
}

.status-dot {
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: var(--moss);
  display: inline-block;
}

/* Footer */

.site-footer {
  border-top: 1px solid var(--line);
  background: var(--paper-alt);
  padding: 2rem 0;
}

.site-footer p {
  max-width: 60ch;
  color: var(--ink-soft);
  font-size: 0.875rem;
}
