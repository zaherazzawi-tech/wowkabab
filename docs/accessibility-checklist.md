# Our Accessibility Checklist (WCAG 2.2 AA)

The standard courts and lawyers use is **WCAG 2.2 Level AA** — 56 rules total.
This is the plain-English version, sorted by when to check it.
The numbers in parentheses are the official rule numbers (proof we're following the real standard).

---

## PART 1 — Check EVERY time Claude builds or changes anything

**The Big 3 (the stuff that gets people sued):**

- [ ] **Real buttons and links.** Every clickable thing is a real `<button>` or `<a>` tag, never a styled div. (4.1.2, 2.1.1)
- [ ] **Every form box has a label.** Name, email, search — each input has a visible label attached to it. Placeholder text alone doesn't count. (1.3.1, 3.3.2)
- [ ] **Focus outline stays ON.** Tab through the page with keyboard only. You must always SEE which thing is selected. (2.4.7) And the selected thing can't be hidden behind a sticky header or cookie banner. (2.4.11)

**Also check:**

- [ ] **Every image has alt text.** Describes what's in it ("Lamb döner wrap cut in half"). Decorative-only images get empty alt: `alt=""`. (1.1.1)
- [ ] **Keyboard can do everything.** Anything a mouse can do, Tab + Enter can do. No getting stuck. (2.1.1, 2.1.2)
- [ ] **Text is readable.** Dark enough against its background — 4.5:1 contrast minimum (a free checker tool tells you this in 2 seconds). (1.4.3)
- [ ] **Headings in order.** One h1 per page, then h2, then h3. No skipping levels, no picking headings for looks. (1.3.1, 2.4.6)
- [ ] **Links say where they go.** "See our menu" — not "click here." (2.4.4)
- [ ] **Tap targets big enough.** Buttons/links at least 24×24 pixels so fingers can hit them. (2.5.8)
- [ ] **Color isn't the only signal.** If something is marked in red, it's also marked with text or an icon. (1.4.1)
- [ ] **Nothing flashes** more than 3 times per second. (2.3.1)
- [ ] **Page zooms to 200%** without breaking or cutting text off. (1.4.4, 1.4.10)

---

## PART 2 — Check only when we ADD these things later

**When we add online ordering / any forms:**
- [ ] Error messages say WHAT is wrong and WHERE ("Email is missing the @") (3.3.1, 3.3.3)
- [ ] Before taking money: user can review and fix their order first (3.3.4)
- [ ] Don't make people re-type info they already entered (3.3.7)
- [ ] Login (if any) can't require a puzzle or memory test — password + "show password" is fine (3.3.8)

**When we add video:**
- [ ] Captions on every video (1.2.2)
- [ ] No audio that auto-plays for more than 3 seconds (1.4.2)

**When we add animations / carousels:**
- [ ] Anything moving can be paused (2.2.2)
- [ ] Respect the visitor's "reduce motion" phone setting (already done on our page)

**When we add popups / menus that open:**
- [ ] Esc key closes them, and keyboard focus goes into and back out of them properly (2.1.2, 2.4.3)

---

## PART 3 — Before we publish any update (5-minute routine)

1. **Mouse in drawer.** Tab through the whole page. Can you see where you are? Can you reach and press everything?
2. **Run axe DevTools** (free Chrome extension) — fix anything red.
3. **Phone check.** Zoom in. Does it still work?
4. **New images?** Check the alt text.
5. **New text?** Run the contrast checker.

---

## PART 4 — Monthly / ongoing (the lawsuit-defense paper trail)

- [ ] Screenshot/save the axe scan results with the date — keep in a folder
- [ ] Keep a simple log: what we fixed and when
- [ ] Accessibility statement page stays up, with a working email for problems
- [ ] If someone emails about an access problem: respond fast, fix it, save the emails
- [ ] Once a real audit is affordable (~when the site makes money): get a third-party manual audit, keep the report

---

## The magic words to paste into Claude every session

> Build this to WCAG 2.2 AA: semantic HTML, real buttons and links only,
> every input has a connected visible label, visible focus styles kept on,
> 4.5:1 text contrast minimum, fully keyboard operable, alt text on all
> meaningful images, respect prefers-reduced-motion, no ARIA where a
> native element works.

---

## Free tools

| Tool | What for |
|---|---|
| axe DevTools (Chrome extension) | Scans page, lists failures |
| WebAIM Contrast Checker | Is this text dark enough? |
| WAVE (wave.webaim.org) | Second-opinion scanner |
| Your own keyboard | The test scanners can't do |
| VoiceOver (Mac/iPhone, built in) / NVDA (Windows, free) | Hear the page like a blind visitor does |

**Remember:** scanners catch roughly a third of problems. The keyboard test and screen reader test catch the rest. Do all three.
