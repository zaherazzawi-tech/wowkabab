# WCAG 2.2 Level AA — All 56 Rules, Plain English
### Source: the official W3C standard (w3.org/TR/WCAG22), translated into normal words with kebab-shop examples

The 56 rules = 32 "Level A" rules (the basics) + 24 "Level AA" rules (the standard courts use).
They're organized under 4 big ideas, called **POUR**:

1. **Perceivable** — people can SEE or HEAR your content (or have it read aloud)
2. **Operable** — people can USE your site (click, tap, keyboard)
3. **Understandable** — people can FIGURE OUT your site
4. **Robust** — screen readers and other tools can READ your code

---

# 1. PERCEIVABLE — "Can they take in the content?"

**1.1.1 Non-text Content (A)** — Every image gets a text description (alt text).
*Example: your döner photo needs alt="lamb döner wrap cut in half". Decoration-only images get empty alt="" so screen readers skip them. Our spit graphic does this.*

**1.2.1 Audio-only / Video-only (A)** — A recording of just audio needs a transcript; a silent video needs a text description.
*Example: if you post a voice message about holiday hours, also write it out.*

**1.2.2 Captions, Prerecorded (A)** — Videos with sound need captions.
*Example: a "how we carve the döner" video needs subtitles.*

**1.2.3 Audio Description or Alternative (A)** — Video needs either a text version or narration describing what's on screen.
*Example: same video — a paragraph describing what happens covers this.*

**1.2.4 Captions, Live (AA)** — Live streams need live captions.
*You'll probably never do this. Skip.*

**1.2.5 Audio Description, Prerecorded (AA)** — If important stuff in a video is visual-only (no one says it out loud), add narration describing it.
*Example: if the video shows prices on screen but nobody reads them aloud, add a voiceover or don't show info that way.*

**1.3.1 Info and Relationships (A)** — Structure must be in the CODE, not just the look.
*Example: your menu headings must be real `<h2>` tags, not just big bold text. Labels must be real `<label>` tags. This is how a blind user's software knows what's a heading vs a paragraph vs a form field. ONE OF THE BIG ONES.*

**1.3.2 Meaningful Sequence (A)** — The reading order in the code matches the visual order.
*Example: screen reader reads menu item name, THEN price — not all names then all prices scrambled.*

**1.3.3 Sensory Characteristics (A)** — Don't give directions that only work if you can see.
*Example: never say "click the red button on the right." Say "click the 'Call to order' button."*

**1.3.4 Orientation (AA)** — Site works in portrait AND landscape.
*Example: don't lock the page to vertical-only on phones.*

**1.3.5 Identify Input Purpose (AA)** — Common form fields (name, email, phone) are marked in code so the browser can autofill them.
*Example: when you add an order form, the phone field gets `autocomplete="tel"`. Helps people who struggle with typing.*

**1.4.1 Use of Color (A)** — Color is never the ONLY way info is shown.
*Example: don't mark spicy items with just a red name. Add a 🌶 icon or the word "spicy" — colorblind people can't see the red.*

**1.4.2 Audio Control (A)** — No sound that auto-plays for more than 3 seconds without a pause button.
*Example: no background music auto-playing on your page. Just don't.*

**1.4.3 Contrast Minimum (AA)** — Text must be dark enough against its background: 4.5:1 ratio (3:1 for big text).
*Example: light gray text on white = fail. Use the free WebAIM checker — takes 5 seconds. ONE OF THE BIG ONES.*

**1.4.4 Resize Text (AA)** — Page still works when text is zoomed to 200%.
*Example: grandpa zooms in to read your prices — nothing gets cut off or overlaps.*

**1.4.5 Images of Text (AA)** — Use real text, not pictures of text.
*Example: don't upload your menu as a JPG photo. Screen readers can't read a picture, and it turns to blur when zoomed. Type the menu out as real text. (Your logo is the exception — logos are fine.)*

**1.4.10 Reflow (AA)** — At 400% zoom (or on a tiny screen), content stacks into one column, no sideways scrolling.
*Example: our page already does this — sections stack on mobile.*

**1.4.11 Non-text Contrast (AA)** — Buttons, icons, and form box borders also need 3:1 contrast so people can see WHERE they are.
*Example: a pale gray search box outline on white = invisible to low-vision users.*

**1.4.12 Text Spacing (AA)** — If a user forces wider line/letter spacing (some dyslexic users do), nothing breaks or gets cut off.
*Example: don't build boxes with fixed heights that chop text when it grows.*

**1.4.13 Content on Hover or Focus (AA)** — Popups that appear on hover can be dismissed, don't vanish when you move toward them, and stay until dismissed.
*Example: if hovering a menu item shows an ingredients tooltip, the user must be able to move their mouse onto it without it disappearing.*

---

# 2. OPERABLE — "Can they actually use it?"

**2.1.1 Keyboard (A)** — Everything works with just a keyboard.
*Example: Tab to the Call button, press Enter, it works. People with tremors, injuries, or no mouse depend on this. ONE OF THE BIG ONES.*

**2.1.2 No Keyboard Trap (A)** — Keyboard users can always Tab OUT of anything.
*Example: if a popup opens and Tab just cycles inside it forever with no Esc — that's a trap. Site is now unusable for them.*

**2.1.4 Character Key Shortcuts (A)** — If you make single-letter keyboard shortcuts, they can be turned off.
*Example: voice-control users say words that type letters — a "press M for menu" shortcut fires by accident. You won't build shortcuts; skip.*

**2.2.1 Timing Adjustable (A)** — No countdown timers unless the user can extend or turn them off.
*Example: when you add online ordering, don't kick people out of a cart after 5 minutes. Slow readers and screen reader users need more time.*

**2.2.2 Pause, Stop, Hide (A)** — Anything that moves for more than 5 seconds has a pause.
*Example: an auto-scrolling photo carousel needs a pause button. Our spit shimmer is fine (subtle + honors reduce-motion), but a rotating banner would need controls.*

**2.3.1 Three Flashes (A)** — Nothing flashes more than 3 times per second.
*Can trigger seizures. Just never make anything flash.*

**2.4.1 Bypass Blocks (A)** — A "skip to content" link so keyboard users don't Tab through the whole menu on every page.
*Our page has one — press Tab once when it loads and you'll see it appear.*

**2.4.2 Page Titled (A)** — Every page has a browser-tab title that says what it is.
*Ours: "Sultan Grill — Char-Grilled Kebabs". Not "Home" or "Untitled".*

**2.4.3 Focus Order (A)** — Tabbing moves through the page in a sensible order.
*Example: Tab goes logo → menu links → call button. Not jumping randomly from footer to header.*

**2.4.4 Link Purpose (A)** — Link text says where it goes.
*Example: "Open in Google Maps" — never "click here". Blind users pull up a list of ALL links on a page; ten "click here"s is useless.*

**2.4.5 Multiple Ways (AA)** — More than one way to find a page (menu + search, or menu + sitemap).
*Only matters once you have multiple pages. One page = automatically satisfied.*

**2.4.6 Headings and Labels (AA)** — Headings and labels actually describe what's under them.
*Example: the section listing food is called "The Menu", not "Check It Out".*

**2.4.7 Focus Visible (AA)** — You can SEE which element is selected when tabbing.
*The glowy outline. Never remove it. Ours is styled amber. ONE OF THE BIG ONES.*

**2.4.11 Focus Not Obscured (AA)** — The selected element isn't completely hidden behind a sticky header, cookie bar, or chat bubble.
*Example: if you add a sticky "Order Now" bar, make sure tabbing doesn't land things underneath it.*

**2.5.1 Pointer Gestures (A)** — No feature requires swiping or two-finger gestures — there's always a plain tap alternative.
*Example: a photo gallery you swipe through also needs next/prev buttons.*

**2.5.2 Pointer Cancellation (A)** — Actions fire when you RELEASE a click/tap, not when you press down, so people can slide off to cancel.
*Normal buttons do this automatically. Only breaks if you build weird custom stuff.*

**2.5.3 Label in Name (A)** — The visible text on a button matches its name in code.
*Example: a button showing "Call to order" must be named that in code too — a voice-control user says "click call to order" and it must work.*

**2.5.4 Motion Actuation (A)** — Nothing requires shaking or tilting the phone.
*You will never do this. Skip.*

**2.5.7 Dragging Movements (AA)** — Anything drag-and-drop also works with plain clicks.
*Example: reordering items in a cart by dragging needs up/down buttons too.*

**2.5.8 Target Size Minimum (AA)** — Tap targets are at least 24×24 pixels (or have space around them).
*Example: tiny social media icons crammed together = people with tremors hit the wrong one. Make buttons finger-sized.*

---

# 3. UNDERSTANDABLE — "Can they figure it out?"

**3.1.1 Language of Page (A)** — Code declares the page language.
*Ours has `<html lang="en">`. One line. Tells screen readers to use English pronunciation.*

**3.1.2 Language of Parts (AA)** — Text in another language is marked in code.
*Example: a Turkish phrase on the page gets `lang="tr"` so it's pronounced right, not mangled.*

**3.2.1 On Focus (A)** — Just tabbing ONTO something doesn't trigger anything.
*Example: tabbing onto a dropdown doesn't auto-open a new page. Surprises disorient people.*

**3.2.2 On Input (A)** — Selecting an option doesn't auto-submit or jump pages without warning.
*Example: picking "pickup" vs "delivery" shouldn't instantly reload the page mid-form.*

**3.2.3 Consistent Navigation (AA)** — Menu is in the same place, same order, on every page.
*Matters when you add more pages. Don't shuffle the nav around.*

**3.2.4 Consistent Identification (AA)** — The same thing is called the same name everywhere.
*Example: don't call it "Cart" on one page and "Basket" on another.*

**3.2.6 Consistent Help (A)** — If pages have a help/contact link, it's in the same spot on every page.
*Example: phone number in the footer on every page, same position.*

**3.3.1 Error Identification (A)** — When a form catches a mistake, it says WHICH field and WHAT'S wrong, in text.
*Example: "Phone number is missing" next to the phone field. Not just a red outline (colorblind users can't see it) and not just "Error."*

**3.3.2 Labels or Instructions (A)** — Every input has a visible label.
*Placeholder text that disappears when you type does NOT count. ONE OF THE BIG ONES.*

**3.3.3 Error Suggestion (AA)** — If the site knows how to fix the error, it says so.
*Example: "Email is missing the @ symbol" — not just "invalid email."*

**3.3.4 Error Prevention — Legal/Money (AA)** — Before charging money: let people review and fix their order first.
*Example: online ordering shows an order summary with an edit option before "Pay."*

**3.3.7 Redundant Entry (A)** — Don't make people type the same info twice in one process.
*Example: if delivery address = billing address, offer a "same as above" checkbox. Memory issues + tremors make retyping painful.*

**3.3.8 Accessible Authentication (AA)** — Logins can't require puzzles or memorizing things.
*Example: no "type the 3rd letter of your password" and no puzzle CAPTCHAs as the only option. Password + paste allowed + "show password" = fine.*

---

# 4. ROBUST — "Can software read your code?"

**4.1.2 Name, Role, Value (A)** — Every control tells assistive software what it IS, what it's CALLED, and its STATE.
*This is the "real buttons" rule. A real `<button>` announces "button" automatically. A styled div announces NOTHING — a blind user's software just says "clickable" or worse, stays silent. THE BIGGEST ONE. Most lawsuits cite this.*

**4.1.3 Status Messages (AA)** — Messages that appear without a page reload get announced to screen readers.
*Example: "Added to cart ✓" pops up — a blind user must HEAR that, not sit wondering if the click worked. Done with one code attribute (`role="status"`).*

---

# The cheat-sheet version

For your one-page kebab site TODAY, only ~15 of these actually apply, and the page already passes them. The rest activate when you add: **forms** (3.3.x), **ordering/payment** (3.3.4, 2.2.1), **video** (1.2.x), **more pages** (3.2.3, 3.2.4, 2.4.5), **galleries/carousels** (2.2.2, 2.5.1).

The Big 5 that cause most lawsuits:
1. **4.1.2** — real buttons
2. **1.1.1** — alt text
3. **1.4.3** — contrast
4. **3.3.2 / 1.3.1** — labeled forms
5. **2.4.7 / 2.1.1** — visible focus + keyboard works
