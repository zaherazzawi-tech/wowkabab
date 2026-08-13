# Wow Kabab — Testing Checklist (Things YOU Should Be Able To Do)

Not code review — these are actions you physically perform. If you can't do one, the page fails.

---

## TEST 1 — The Keyboard Test (5 min, do every update)
Put the mouse away. Only Tab, Shift+Tab, and Enter.

- [ ] Press Tab once on page load → a "Skip to main content" link appears top-left
- [ ] Press Enter on it → you jump past the nav
- [ ] Keep tabbing → an amber outline is ALWAYS visible on whatever's selected
- [ ] The order makes sense: skip link → logo → Menu → Why Us → Find Us → Call → Directions → Maps → phone
- [ ] Enter on "Call to order" → phone app opens (on a phone)
- [ ] Enter on "Get directions" → page scrolls to Find Us
- [ ] You never get stuck anywhere

**Fail = any moment where you can't tell where you are, or can't reach something.**

## TEST 2 — The Scanner Test (2 min)
1. Open the page in Chrome
2. Install "axe DevTools" extension (free)
3. Right-click page → Inspect → axe DevTools tab → Scan
- [ ] Zero critical/serious issues
- [ ] Screenshot the result with the date visible → save to a "compliance" folder (this is lawsuit-defense evidence)

## TEST 3 — The Zoom Test (2 min)
- [ ] Ctrl/Cmd + "+" to 200% → all text readable, nothing overlaps or cut off
- [ ] Push to 400% → page stacks into one column, NO sideways scrolling
- [ ] On your phone: everything readable, buttons easy to tap with a thumb

## TEST 4 — The Screen Reader Test (10 min, do before publishing)
The one that actually tells you if a blind customer can use the site.

**iPhone:** Settings → Accessibility → VoiceOver → On. Swipe right to move through items, double-tap to activate.
**Mac:** Cmd+F5. **Windows:** download NVDA (free).

- [ ] Every element reads out something that makes sense
- [ ] "Call to order" announces as a LINK with that name — not "clickable" or silence
- [ ] Headings announce as headings ("The Menu, heading level 2")
- [ ] The spit graphic is SKIPPED entirely (it's decoration — silence is correct)
- [ ] Close your eyes for the whole page. Could you find the phone number and address? That's the real test.

## TEST 5 — The Squint Test (1 min)
- [ ] Squint hard at the page. Can you still read every piece of text? Blurry-but-readable = contrast is OK. Anything that vanishes = too light.
- [ ] Confirm with WebAIM Contrast Checker on any color pair you're unsure about

## TEST 6 — The Phone-a-Friend Test (whenever possible)
- [ ] Hand your phone to someone over 60. Say "find the phone number and call the shop." Watch silently. Wherever they stumble is your bug list.

---

## When to run what

| Situation | Tests |
|---|---|
| Any change to the page | 1 + 2 |
| Before publishing | 1 + 2 + 3 + 4 + 5 |
| Monthly while live | 2, save the screenshot |
| Added a form / new page | Everything, plus trigger every form error on purpose |

## The pass rule
The site passes when a blind person, a keyboard-only person, and a zoomed-in grandpa can all order a kebab without help.
