# POETAI: Ukrainian Poetry Engineering Specialist

POETAI is a highly specialized poetry engineering system designed to create technically flawless Ukrainian verse. It operates under the strict **InstructDojo Cybernetic Architecture**, treating poetry not just as art, but as mathematical prosody.

## ✅ Tested & Verified Models

POETAI has been tested across the Google Gemini model family. **General rule: the newer the model, the better it handles complex prosodic tasks.**

| Model | Status | Poetry Quality | Meter Accuracy | Notes |
|:------|:-------|:---------------|:---------------|:------|
| **Gemini 3.1 Pro** | ✅ Best | ⭐⭐⭐⭐⭐ | Excellent | Best-in-class. Exceptional prosodic precision, cultural depth, and linguistic purity. Newest model = best results. |
| **Gemini 2.5 Pro** | ✅ Verified | ⭐⭐⭐⭐⭐ | Excellent | Fully recommended. Handles complex meters, sound symbolism, and linguistic purity flawlessly. |
| **Gemini 2.5 Flash** | ✅ Verified | ⭐⭐⭐⭐ | Very Good | Works well for most requests. Occasional minor stress placement issues on complex forms. |
| **Gemini 3 Flash** | ⚠️ Functional | ⭐⭐⭐ | Acceptable | Works, but may produce meter inconsistencies, occasional stress errors, or blacklisted word usage. Review output carefully. |

> 💡 **The newer the model, the better.** Each generation improves prosodic understanding, stress placement accuracy, and adherence to the prompt's safety systems. Always prefer the latest available Pro model.

### Recommended Setup

| Use Case | Recommended Model | Why |
|:---------|:------------------|:----|
| Production-quality poetry | Gemini 3.1 Pro / 2.5 Pro | Consistent meter, perfect stress, linguistic purity |
| Quick drafts / experimentation | Gemini 2.5 Flash | Fast, reliable, minor imperfections acceptable |
| Budget / high-volume | Gemini 3 Flash | Functional but requires manual review |

> ⚠️ **Flash model note:** The prompt's built-in safety systems (vocabulary blacklist, stress verification, completion checklist) help catch errors, but Flash-tier models may skip verification steps. Always review meter manually when using Flash models — see [Verification Tools](#-verification-tools) below.

---

## 🔍 Verification Tools

After generating poetry, you can verify its technical quality using external analysis tools.

### Poetrum — Поетична лабораторія

**🔗 [https://poetrum.com/](https://poetrum.com/)**

Poetrum (Поетична лабораторія) is a free online service for writing and analyzing Ukrainian verse. Use it to independently verify POETAI's output.

**What Poetrum checks:**

| Feature | What It Analyzes | Why It Matters |
|:--------|:-----------------|:---------------|
| **Meter detection** | Identifies the metrical pattern (iamb, trochee, etc.) | Confirms POETAI maintained a single meter throughout |
| **Stress mapping** | Shows stressed/unstressed syllables per line | Catches any stress errors the model may have made |
| **Syllable count** | Counts syllables per line | Verifies line length consistency |
| **Rhyme analysis** | Identifies rhyme scheme and rhyme quality | Confirms rhyme pattern matches the specification |
| **Rhythm visualization** | Visual stress pattern diagram | Makes meter breaks immediately visible |

**Recommended verification workflow:**
```text
1. Generate poem with POETAI
2. Copy ONLY the Ukrainian verse
3. Paste into Poetrum → [https://poetrum.com/](https://poetrum.com/)
4. Compare Poetrum's analysis with POETAI's self-reported PROSODIC ANALYSIS
5. If discrepancies found → point out the exact word to POETAI
```

---

## Core Architecture

### **Poetry Master** ([poetai_poetry_master.md](poetai_poetry_master.md)) 🧠

An uncompromising prosody engine featuring:

**🛡️ InstructDojo Cybernetic Standards:**
- **Response Anchor:** `[POETAI: ACTIVE]` ensures the AI never breaks character.
- **Zero-Apology Protocol:** If you point out a metrical flaw, the AI instantly confirms the error and rewrites the line without conversational fluff.
- **Mandatory Pre-Computation:** Outputs an `**Analysis:**` block to plan the meter and sound symbolism *before* writing a single word.
- **Anti-Lazy Rules:** Delivers the full poem at once. Zero placeholders.

**🌉 The Language Bridge (Non-Negotiable):**
- **POETRY:** 100% pure Ukrainian (no Russian calques, no Surzhyk).
- **COMMUNICATION & ANALYSIS:** Strict Technical English for optimal LLM compliance.

**📐 Technical Precision:**
- **Mathematical Prosody:** Single meter enforcement and pre-delivery stress checks on every strong beat.
- **Vocabulary Safety System:** Built-in blacklist of words that cause LLM stress errors (e.g., *вікно, зима, піч*), preferring fixed-stress alternatives.

---

## How to Use POETAI

### Initial Setup

1. Copy the complete content of [poetai_poetry_master.md](poetai_poetry_master.md).
2. Send to your AI model as the **first message** (see [Tested Models](#-tested--verified-models)).
3. Wait for the initialization response: 
   > `🛡️ POETAI Prosody Systems Active. Provide the theme, desired mood, preferred meter...`
4. Use natural language OR technical specifications.

### Input Examples

**Natural Language Mode:**
> "I want a poem that feels like morning dew on spider webs, delicate and shimmering with hope."

**Technical Mode:**
> "Create an Amphibrach tetrameter poem about freedom. Rhyme: ABAB. Use hard consonants for a powerful feel."

---

## Response Structure

POETAI uses a strict, visually distinct format:

```markdown
[POETAI: ACTIVE]

**Analysis:** The vision requires a delicate, awakening atmosphere. I will use Amphibrach tetrameter for a flowing rhythm, pairing it with soft consonants (л, м, н) and an AABB rhyme scheme.

Прокинеться сонце в колисці із хмар,
Розсипле проміння, мов золото в дар.
Роса на павутинні — мов сльози нічні,
Зникають у ранковій, ясний тишині.

✅ Ukrainian poetry complete

PROSODIC ANALYSIS:
- Meter: Amphibrach Tetrameter (∪ — ∪ | ∪ — ∪...)
- Rhyme: AABB (Paired rhyme)
- Sound symbolism: Dominance of soft 'S' and 'L' sounds to evoke delicacy.
- Stress verification: All strong beats confirmed on natural stresses.

CULTURAL NOTES:
- Imagery: Personification of the sun (folk tradition).
- Authenticity: Verified pure Ukrainian lexicon.
```

> 🔍 **Verify this output:** Copy the Ukrainian verse into [Poetrum](https://poetrum.com/) to independently confirm meter and stress accuracy.

---

## Dual-Mode Intelligence Matrix

### 🎨 **Emotion → Technique Translation**

POETAI automatically translates feelings into prosodic specifications:

| Emotion | Meter | Consonants | Vowels | Imagery |
|:--------|:------|:-----------|:-------|:--------|
| **Gentle** | Amphibrach | Soft: Л, М, Н | І, Е | Nature, dew, light |
| **Powerful** | Trochaic | Strong: Р, Д, З, Г | А, О | National symbols, strength |
| **Sad** | Slow Iambic | Heavy consonants | О, У | Loss, memory, homeland |
| **Nostalgic** | Folk Amphibrach | Melodic: С, Х, Ш | О, У, И | Village, traditions, grandmother |

### 🔒 **Technical Safety Systems**

Built-in safeguards that prevent common LLM poetry errors:

| System | What It Does | Why It Matters |
|:-------|:-------------|:---------------|
| **Vocabulary Blacklist** | Blocks specific words (e.g., "піч", "чарівна") | LLMs misplace stress on these words |
| **Fixed Stress Preference** | Prioritizes words whose stress doesn't shift | Prevents meter breaks during declension |
| **Single Meter Rule** | Forbids mixing meters within one poem | Ensures rhythmic consistency |
| **Caesura Enforcement** | Requires mid-line pause in lines of 11–12 syllables | Prevents rhythmically awkward long lines |

---

## Troubleshooting

| Problem | Likely Cause | Solution |
|:--------|:-------------|:---------|
| Meter breaks mid-poem | Model used a word with shifting stress | Point out the word. The Zero-Apology Protocol will fix it instantly. Verify with [Poetrum](https://poetrum.com/). |
| Russian words appear | Model defaulted to common Slavic roots | Point it out; model will replace with pure Ukrainian. |
| Output feels generic | Insufficient mood description | Provide more emotional detail: colors, textures, atmosphere. |
| AI apologizes or chats | Protocol degradation | Remind it: "Enforce Zero-Apology Protocol and Response Anchor." |
| Flash model skips verification | Flash-tier limits | Verify manually via [Poetrum](https://poetrum.com/) or switch to a Pro model. |

---

**🎭 Від серця до серця, від думки до рими**

---

## License

This project is licensed under the MIT License.

## Support

* 📖 **Documentation**: This README and instruction file
* 🔍 **Poetry Verification**: [Poetrum — Поетична лабораторія](https://poetrum.com/)
* ⭐ **Star this repo** if POETAI helps you create beautiful Ukrainian verse!

---

<div align="center">

**Made with ❤️ for the Ukrainian poetry community**

</div>
