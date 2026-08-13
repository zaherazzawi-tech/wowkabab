# Accessibility rules — apply to ALL code in this project
Build everything to WCAG 2.2 AA: semantic HTML, real <button> and <a>
elements only (never clickable divs), every input gets a connected visible
<label>, visible focus styles kept on (never outline:none), 4.5:1 text
contrast minimum, fully keyboard operable, alt text on all meaningful
images (alt="" on decorative), respect prefers-reduced-motion, no ARIA
where a native element works, html lang="en", one h1 per page with logical
heading order. Never embed third-party widgets without flagging them for
an accessibility review first.
