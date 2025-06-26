# BLOCKFILTERAI: Web Filtering Engineer

BLOCKFILTERAI is a highly specialized filtering engineer with dual-mode intelligence, designed to create precise uBlock Origin filters from both natural language descriptions and technical specifications.

## Available Version

### **Filter Expert** ([blockfilterai_filter_expert.md](blockfilterai_filter_expert.md)) 🧠 DUAL-MODE

Enhanced web filtering system featuring:

**🎨 Natural Language Understanding:**
- Transform "annoying popups" into precise filters
- Extract filtering needs from user frustrations
- Understand browsing pain points
- Automatic filter design from descriptions
- User-centered blocking solutions

**🚫 Network Filtering:**
- Domain and URL pattern blocking
- Request type filtering
- Third-party isolation
- Whitelist exceptions

**🎭 Cosmetic Filtering:**
- CSS selector engineering
- Element hiding and removal
- Procedural content filtering
- DOM manipulation

**⚡ Performance Optimization:**
- Minimal selector complexity
- Efficient pattern matching
- Resource usage monitoring
- Filter consolidation

**🧠 Dual-Mode Intelligence:**
- Seamless switching between natural and technical requests
- 4-layer web filtering analysis
- User experience-focused solutions
- Technical precision when needed

## How to Use BLOCKFILTERAI

### Initial Setup

1. Copy the complete content of [blockfilterai_filter_expert.md](blockfilterai_filter_expert.md)
2. Send as first message to your AI model
3. Wait for "BLOCKFILTERAI Filter Expert initialized" response
4. Describe annoyances naturally OR provide technical specifications

### Dual-Mode Requests

**Natural Language Mode:**
```
I'm tired of those annoying newsletter popups that block the 
content on news sites. They appear after scrolling and force 
me to either subscribe or close them, which ruins my reading.
```

**Technical Mode:**
```
<target>
<div class="newsletter-modal" id="subscribe-popup">
  <form class="signup-form">...</form>
</div>
</target>

<context>
news.example.com/articles/*
</context>
```

**Mixed Mode:**
```
Block those irritating cookie consent banners that take up 
the bottom of the screen. They usually have buttons like 
"Accept" and "Settings" and appear on first visit.
```

### Natural Language Examples

**User Frustration Description:**
```
YouTube video ads are driving me crazy. I just want to watch 
content without waiting through 15-30 second ads that I can't 
skip. The pre-roll ads are the worst, but the mid-video 
interruptions are annoying too.
```

**Browsing Experience Problem:**
```
News websites load so slowly because of all the tracking and 
analytics scripts. The content jumps around as ads load, 
making it impossible to read. Sometimes my browser even 
freezes because of all this junk.
```

**Privacy Concern:**
```
I don't like how websites seem to know everywhere I've been. 
Those creepy ads that follow me across sites are unsettling. 
I want to browse without feeling watched and tracked.
```

### Technical Request Examples

**Element Blocking:**
```
<target>
<div class="ad-banner" id="top-ad">
  <img src="/ads/banner.jpg">
</div>
</target>

<context>
example.com/articles/*
</context>

<requirements>
Fast execution, no false positives
</requirements>
```

**Network Blocking:**
```
<target>
Block all requests to tracking.example.com
</target>

<context>
Third-party requests only
</context>

<requirements>
Complete blocking, preserve site functionality
</requirements>
```

## Dual-Mode Intelligence

### 🎨 **Problem Translation System**

**User Frustrations → Technical Filters:**
- "Annoying popups" → Overlay and modal blocking filters
- "Slow-loading pages" → Resource and script blocking
- "Video ads" → Media request blocking and player modification
- "Content keeps moving" → Layout shift prevention
- "Privacy concerns" → Tracker and fingerprinting protection

**Context Understanding:**
- Site category awareness (news, shopping, social media)
- User goals (reading, watching, browsing)
- Frequency of issues (first-time, persistent)
- Impact severity (annoyance vs breakage)

### 📐 **4-Layer Filtering Analysis**

**Layer 1: Surface Problem**
What the user explicitly mentions as annoying

**Layer 2: Technical Root Cause**
Underlying web elements causing the issue

**Layer 3: User Experience Impact**
How the content affects browsing flow and satisfaction

**Layer 4: Optimal Filter Solution**
Best technical approach for maximum effectiveness

## Technical Reference

### 🚫 **Network Filter Syntax**

**Basic Patterns:**
```
||domain.com^              # Block domain
||domain.com/path/*        # Block path
||domain.com^$third-party  # Third-party only
@@||domain.com^            # Whitelist
```

**Advanced Options:**
```
$script         # Scripts only
$image          # Images only
$xhr            # AJAX requests
$domain=site.com # Specific domain
$~third-party   # First-party only
```

### 🎨 **Cosmetic Filter Syntax**

**Selectors:**
```
##.class                   # Class selector
###id                      # ID selector
##div[attr="value"]        # Attribute selector
##div > .child             # Child selector
##div:has-text(/regex/)    # Text matching
```

**Actions:**
```
##element:remove()         # Remove from DOM
##element:style(prop)      # Apply CSS
##element:has(child)       # Conditional hiding
```

### ⚡ **Performance Patterns**

**Optimal Selectors:**
```
GOOD:  ###specific-id
GOOD:  ##.unique-class
BAD:   ##div > div > div > span
BAD:   ##*[class*="ad"]
```

**Filter Efficiency:**
- ID selectors: Fastest
- Class selectors: Fast
- Complex selectors: Slower
- Procedural filters: Slowest

## Enhanced Filter Categories

### Ad Blocking (Visual Cleanup)
- Display banners → Clean visual experience
- Video ads → Uninterrupted viewing
- Native advertising → Pure content focus
- Popups/popunders → Distraction-free browsing

### Privacy Protection (Security)
- Analytics scripts → Behavior protection
- Tracking pixels → Movement privacy
- Fingerprinting → Identity protection
- Social widgets → Platform isolation

### Annoyance Removal (Workflow)
- Cookie notices → Streamlined access
- Newsletter popups → Focused reading
- Chat widgets → Clean interface
- Notification prompts → Distraction-free browsing

### Performance Optimization (Speed)
- Heavy resources → Bandwidth saving
- Unnecessary scripts → Processing efficiency
- Redundant content → Clean loading
- Slow third-parties → Speed optimization

## Best Practices

### 📋 **For Natural Language Requests**

**Describe Your Frustration:**
- Explain what annoys you about websites
- Mention specific sites where it happens
- Describe how it affects your browsing
- Explain what you'd like to experience instead

**Examples:**
- "Popups that ask for my email"
- "Videos that autoplay with sound"
- "Sticky headers that take up screen space"
- "Content that moves around while loading"

### 🔧 **For Technical Requests**

**Provide Detailed Information:**
- HTML structure when possible
- Domain and page patterns
- Performance requirements
- Functionality considerations

**Format:**
- Use the target, context, requirements format
- Include HTML snippets when available
- Specify domain scope
- Mention any side-effect concerns

## Enhanced Priority System

### Response Format

Every response includes user-centered prioritized options:

```
## UNDERSTANDING YOUR PROBLEM:
User Impact: [How the content affects browsing]
Technical Cause: [What's creating the annoyance]
Site Context: [Where this typically happens]

🥇 **BEST CHOICE (User-Friendly):**
[Most reliable and simple filter]
Why: [User benefit explanation]

🥈 **ALTERNATIVE (Performance-Focused):**
[Faster or lighter option]
Why: [Performance advantages]

🥉 **ADVANCED (Comprehensive):**
[Complete but complex solution]
Why: [Full coverage explanation]

## QUICK CHOICE:
- Want immediate relief? → Use 🥇
- Page loading slowly? → Try 🥈
- Nothing else worked? → Use 🥉

## IMPACT SUMMARY:
- Annoyance eliminated: [What improves]
- Performance impact: [Speed effect]
- Side effects: [Any functionality changes]
```

## Troubleshooting

### Dual-Mode Diagnostics

**Natural Language Issues:**
- "Filter isn't blocking the ads" → Check for new patterns or format changes
- "Site looks broken after filtering" → Check for over-aggressive selectors
- "Still getting popups sometimes" → Check for dynamic injection techniques
- "Page performance worse after filtering" → Check for excessive procedural filters

**Technical Diagnostics:**
- Selector specificity analysis
- Filter syntax verification
- DOM structure examination
- Network request pattern analysis
- Performance impact measurement

### Common Solutions

- **Problem:** Elements returning after being blocked
  **Solution:** Target parent elements or use scriptlet injection

- **Problem:** Page functionality broken
  **Solution:** Use more specific selectors and add exceptions

- **Problem:** Ads bypassing filters
  **Solution:** Update patterns and use multiple filter types

## Success Metrics

### ✅ **Dual Excellence**

**User Experience Improvement:**
- Annoyance elimination success rate
- Browsing flow improvement
- Performance perception enhancement
- Overall satisfaction increase

**Technical Excellence:**
- 99.9% blocking accuracy
- <0.1% false positive rate
- <50ms performance impact
- Cross-browser compatibility
- Update resilience

## Getting Started

### For Natural Language Users

1. **Initialize BLOCKFILTERAI** (send instruction as first message)
2. **Describe your browsing frustrations** naturally
3. **Explain where and how they occur**
4. **Receive user-centered filtering solutions**
5. **Test and provide feedback** for refinement

### For Technical Users

1. **Initialize BLOCKFILTERAI** (send instruction as first message)
2. **Provide element code or filter specifications**
3. **Specify context and requirements**
4. **Receive optimized technical filters**
5. **Implement and verify effectiveness**

Remember: BLOCKFILTERAI understands both "these popups are annoying" AND "block div.modal-popup on example.com"

---

**🛡️ Engineering the user-centric ad-free web**

## License

This project is licensed under the MIT License - see the [LICENSE](../LICENSE) file for details.

## Support

- 📖 **Documentation**: This README and instruction file
- 🐛 **Issues**: Report problems via GitHub Issues
- 💬 **Discussions**: Share filters and experiences
- ⭐ **Star this repo** if BLOCKFILTERAI improves your browsing!

---

<div align="center">

**Made with ❤️ for the ad-blocking community**

</div>
