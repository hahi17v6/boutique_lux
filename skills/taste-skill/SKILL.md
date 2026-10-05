---
name: taste-skill
description: Anti-slop design framework for AI agents (by Leonxlnx). Enforces premium UI taste, refined typography, structured visual hierarchy, and tunable design dials (DESIGN_VARIANCE, MOTION_INTENSITY, VISUAL_DENSITY) to prevent generic template layouts.
metadata:
  author: Leonxlnx
  version: "2.0.0"
  argument-hint: <framework-or-component>
---

# TASTE-SKILL (v2.0) — ANTI-SLOP FRONTEND DESIGN FRAMEWORK

> **Goal:** Eliminate generic AI-generated frontend slop (repetitive card rows, purple/blue glow gradients, nested container boxes, weak hierarchy). Inject high-end art direction, distinctive typography, and intentional craft into every interface.

---

## 1. THE CONFIGURABLE DESIGN DIALS

Always configure these three global dials for any visual frontend task:

* **`DESIGN_VARIANCE` (Scale 1–10, Default: 8)**
  * `1` = Strict conventional corporate grid.
  * `10` = Asymmetric, editorial, avant-garde layout architecture.
* **`MOTION_INTENSITY` (Scale 1–10, Default: 6)**
  * `1` = Minimal static CSS transitions.
  * `10` = Rich micro-interactions, spring physics, scroll-driven reveals, hover elevations.
* **`VISUAL_DENSITY` (Scale 1–10, Default: 4)**
  * `1` = Extremely airy, high-luxury editorial breathing room.
  * `10` = Compact data-dense analytical dashboard.

---

## 2. THE ANTI-SLOP DIRECTIVES

### ❌ What to BAN (AI Slop Signals)
1. **Generic Purple/Blue Neon Blobs:** No uninspired dark-mode glowing blobs without brand context.
2. **Cards-Inside-Cards-Inside-Cards:** Never nest bordered card containers within bordered cards.
3. **Pill & Chip Overload:** Do not clutter headers with fake technical badges (e.g. `[01 SYNC_OK]`, `v2.4.0 BETA`).
4. **Weak Headline Copy:** No cliché hero copy like *"Elevate Your Workflow with Next-Gen Synergy"*.
5. **Default System Fonts:** No unstyled browser defaults (`Times New Roman`, raw `Arial`).

### ✅ What to ENFORCE (Taste & Craft)
1. **Distinctive Typography Pairings:** Combine an assertive Display/Heading typeface (e.g. `Syne`, `Outfit`, `Space Grotesk`, `Monument`) with a ultra-legible geometric body font (`Inter`, `Helvetica Neue`).
2. **Curated Color Tokens:** Define strict HSL/Hex variables for backgrounds, surfaces, primary text, secondary text, subtle borders, and a signature accent color.
3. **Asymmetric Bento & Grid Cadence:** Organize content with varying card sizes, split-screens, and full-bleed media frames.
4. **Polished Hover & Focus States:** Every interactive element must provide smooth visual feedback (`transform: translateY(-2px)`, subtle box-shadow glow, border illumination).
5. **Accessibility & WCAG AA:** Contrast ratios strictly $\ge 4.5:1$ for readable text.

---

## 3. APPLIED DESIGN TOKENS (TORNADO LUXURY STREETWEAR PATTERN)

```css
:root {
  --taste-bg-main: #0A0A0A;
  --taste-bg-surface: #141414;
  --taste-text-primary: #FFFFFF;
  --taste-text-secondary: #A0A0A0;
  --taste-accent-gold: #D4AF37;
  --taste-border: #262626;
  --taste-radius-sm: 4px;
  --taste-radius-md: 8px;
  --taste-transition: 300ms cubic-bezier(0.4, 0, 0.2, 1);
}
```

---

## 4. WORKFLOW FOR AI AGENTS

1. **Read Guidelines:** Inspect the active project tokens and design system.
2. **Setup Variables:** Ensure CSS variables or Tailwind tokens are properly loaded.
3. **Execute Design:** Code responsive layouts with mobile-first priority.
4. **Audit Taste:** Verify that no AI-slop anti-patterns (nested boxes, generic gradients, crowded labels) are present.
