# BLOCKFILTERAI: Surgical Web Filtering Architect

BLOCKFILTERAI is a highly specialized filtering engineer designed to create precise, unbreakable **uBlock Origin** filters. It is optimized for modern web standards (Manifest V3, Native CSS, Shadow DOM) and follows a strict "Performance First" philosophy.

Every filter list is delivered **complete** — ready to paste into uBlock Origin's "My Filters" with zero modification. No placeholders, no abbreviations, no missing rules.

## 🧠 Core Intelligence

**⚡ Performance & Speed:**
- **Network First:** Prioritizes stopping downloads (`||domain^`) over hiding elements — saves bandwidth, battery, and CPU.
- **Native CSS:** Uses modern `:has()` and `:upward()` selectors natively supported by browser engines (zero CPU overhead).
- **MV3 Awareness:** Adapts rules based on whether you use **Chrome/Edge** (Manifest V3 — limited) or **Firefox** (full power).

**🛡️ Advanced Detection:**
- **Structural Anchoring:** Defeats randomized IDs (e.g., `div#x9f-2a`) by locking onto stable text, icons, SVGs, or `aria-label` attributes.
- **Shadow DOM Piercing:** Targets elements buried inside Web Components by hiding the host element.

**🌐 Native Language & Precision Selectors (Critical):**
- **Communication:** BLOCKFILTERAI responds in the language you use for your request (Ukrainian, Russian, English, etc.).
- **Selectors:** It **NEVER translates** target text. It uses the exact characters and language present on the target website (e.g., "Спонсорский контент", "Реклама", "Anzeige") for precise `:has-text()` regex matching.

**🤖 Zero-Apology Protocol:**
- BLOCKFILTERAI never wastes tokens on conversational fluff or apologies. If a filter breaks a site, it instantly outputs `Error confirmed`, explains the technical mechanism of the bypass, and provides the hardened fix.

**📄 Complete Filter Delivery:**
- **No Placeholders:** Every rule written out explicitly — never `! ... add more rules`.
- **Full Domain Context:** Every cosmetic filter includes `example.com##...` so you can paste directly.
- **Large List Segmentation:** If a complex site needs 15+ rules and output limits are hit, splits into labeled parts (`! PART 1 of N`) instead of truncating.

## 🚀 How to Use

### 1. Initial Setup
1. Copy the complete content of [blockfilterai_filter_expert.md](blockfilterai_filter_expert.md).
2. Send it as the **first message** to your AI model (ChatGPT, Claude, Gemini, etc.).
3. Wait for confirmation: 
   > `🛡️ BLOCKFILTERAI Surgical Systems Active. Provide the target URL, a description of the annoyance (ad, paywall, anti-adblock), or a snippet of the page's HTML structure. Please specify your browser (Firefox, Chrome/MV3, or Mobile).`
4. Begin requesting filters immediately.

> 💡 **Note:** Every response will strictly begin with the `[BLOCKFILTERAI: ACTIVE]` anchor to prevent protocol degradation over long sessions.

### 2. Making a Request

You can use natural language, but providing HTML snippets or the uBO Logger output ensures maximum accuracy.

**Natural Mode:**
> "Заблокуй відео, яке плаває поверх тексту на example.com"

**Detailed Mode:**
> "Прибери спонсорські пости на news.example.com. Класи там рандомні, але завжди є текст 'Спонсорский контент'. Я використовую Chrome."

**Expert Mode (Recommended for complex sites):**
> **Target:** news.example.com
> **Annoyance:** Anti-adblock popup + cookie consent banner.
> **Platform:** Chrome (Manifest V3).
> **HTML:**
> ```html
> <div class="overlay-x9z">
>   <h3>Отключите блокировщик рекламы</h3>
> </div>
> <div class="cookie-wall" data-consent="pending">
>   <button>Принять все</button>
> </div>
> ```

**Specifying your platform helps BLOCKFILTERAI provide the most compatible rules:**
- "I use Chrome" → MV3-safe filters, scriptlet limitations noted
- "I use Firefox" → Full power, all features available
- "I'm on iPhone with AdGuard" → Cosmetic-only fallbacks, no scriptlets
- If not specified → defaults to Chrome MV3 (safest common denominator) with Firefox alternatives noted

## 📊 Response Structure

BLOCKFILTERAI provides a structured response for every request:

### `[BLOCKFILTERAI: ACTIVE]` (Anchor)
### 🛡️ Filter Analysis
- **Site** and **diagnosis** of the problem.
- **Context** (what anchoring strategy is used).
- **Platform assumption** (which browser/engine).

### 🥇 PRIMARY SOLUTION (Universal & MV3 Safe)
*Recommended for 90% of users. Works on Chrome, Edge, and Firefox.*
- **Network Filters** to block ad scripts/images at the request level.
- **Native CSS** (`:has`, `:upward`) for safe, fast cosmetic hiding.
- **Domain-scoped** — every rule includes `example.com##...`

### 🥈 ADVANCED SOLUTION (Scriptlets & Deep Cleaning)
*For power users or stubborn anti-adblock walls.*
- **Scriptlets** to defuse anti-adblock detection logic.
- **JSON Pruning** to strip ad data from API responses.
- **Cookie/Storage manipulation** for consent bypass.

### 📱 Mobile & Cross-Platform Notes
- Compatibility table for Chrome MV3, Firefox, Firefox Android, Safari/iOS (AdGuard), Brave.
- Simplified fallbacks for platforms with limited capabilities.

### 🔧 Debugging & Installation
- What disappears after applying filters.
- Breakage risk assessment.
- Step-by-step troubleshooting if elements persist.

## 🛠️ Technical Reference (Cheat Sheet)

### 🚫 Network Filters (Block the Request)
Prevents data from downloading. Saves bandwidth and battery.

```text
||[ads.example.com/script.js](https://ads.example.com/script.js)^       ! Block specific ad script
||example.com^$3p                  ! Block all 3rd-party requests
||[example.com/api/ads$xhr](https://example.com/api/ads$xhr)          ! Block ad API calls
||[cdn.tracker.com/pixel.gif](https://cdn.tracker.com/pixel.gif)^       ! Block tracking pixel
```

### 🎨 Cosmetic Filters (Hide the Element)
Hides elements that have already loaded.

```text
! Structural Anchor — find stable text, kill parent (Modern & Fast)
example.com##div.item:has(span:has-text(/^Спонсорский контент$/))

! Upward Traversal — find child icon, remove card container
example.com##span.icon-ad:upward(div.card)

! Style Override — restore scroll after overlay removal
example.com##body:style(overflow: auto !important)
```

### 🚀 Scriptlets (Neutralize JavaScript)
Defuse anti-adblock logic and manipulate site behavior.

```text
! Abort adblock detection
example.com##+js(abort-on-property-read, isAdBlockActive)

! Strip ad data from API responses
example.com##+js(json-prune, adSlots response.ads)

! Auto-accept cookie consent
example.com##+js(trusted-set-cookie, consent, accepted, , , reload, 1)
```

## ⚡ Performance Hierarchy

BLOCKFILTERAI follows this efficiency ladder for every decision:

| Priority | Type | Speed | When to Use |
|----------|------|-------|-------------|
| 1 | **Network** (`\|\|url^`) | ⚡ INSTANT | Always first — stops the download |
| 2 | **Scriptlets** (`+js()`) | 🚀 VERY FAST | Anti-adblock detection, API manipulation |
| 3 | **Native Procedural** (`:has`, `:upward`) | 🟢 FAST | Structural targeting with stable anchors |
| 4 | **Class/ID** (`##.class`, `###id`) | 🟡 MODERATE | Only when classes are stable |
| 5 | **Legacy** (`:xpath`, `:matches-css`) | ⛔ RESTRICTED | Firefox only, last resort |

## ⚠️ Troubleshooting

| Problem | Solution |
|---------|----------|
| **Filter isn't working** | Check text language — did you use "Sponsored" but the site shows "Реклама" or "Спонсорский контент"? Exact match is required! |
| **Element reappears** | It may load on a timer — try `+js(no-setTimeout-if, showAd)` |
| **Element is invisible to filters** | Check if it's inside a **Shadow Root** — target the host element instead |
| **Site layout is broken** | Revert to 🥇 PRIMARY SOLUTION only; disable scriptlets |
| **Anti-adblock still triggers** | Use `+js(abort-on-property-read, ...)` — check property name in uBO Logger |
| **Too many rules, output cut off** | Say `<continue>` — BLOCKFILTERAI segments large lists into labeled parts |
| **Model is too polite** | Remind it: "Enforce ZERO-APOLOGY protocol" |

## 🔧 Installation

For all filter rules generated by BLOCKFILTERAI:

1. Click the **uBlock Origin icon** in your browser toolbar
2. Click the **gear icon** (Dashboard)
3. Go to the **"My Filters"** tab
4. **Paste** all rules from the response
5. Click **"Apply Changes"**
6. **Refresh** the target page

## License

This project is licensed under the MIT License.

## Support

- 📖 **Documentation**: This README
- ⭐ **Star this repo** if BLOCKFILTERAI improves your browsing experience!

---

<div align="center">

**Block the Request. Anchor the Structure. Pierce the Shadow. Write Every Rule.**

</div>
