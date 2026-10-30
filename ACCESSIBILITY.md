# Accessibility notes and publishing checklist

This starter is **designed with WCAG 2.2 Level AA in mind**. It is **not a WCAG certification** or a guarantee of conformance after you add your content. Automated checks can find some problems; assistive-technology and manual testing are still necessary.

## Built-in features

- Semantic HTML: `header`, `nav`, `main`, `section`, `article`, `footer`, and ordered headings.
- A visible-on-focus **Skip to content** link on every page.
- One `h1` per page, followed by section headings in order.
- Keyboard-operable tiles, links, and mobile navigation using native anchor and button elements.
- Strong, visible keyboard focus outlines. Links can be recognized by text, underlines, borders, and labels rather than color alone.
- Mobile menu announces expanded/collapsed state via `aria-expanded`, references its navigation region with `aria-controls`, and closes with Escape (returning focus to the button).
- Navigation works **without JavaScript**: its links remain visible on small screens if scripts do not run.
- Decorative shapes and arrows are hidden from assistive technologies with `aria-hidden="true"`.
- Text uses dark gray or black against white/off-white; saturated red, yellow and blue are mostly decorative accents.
- Layout reflows from multiple columns to one column on narrow screens. No fixed-height content containers.
- Respects `prefers-reduced-motion`. Does not use auto-playing media, timed content, flashing, parallax, or hover-only controls.
- No remote fonts or third-party scripts are needed to render the site.

## Your checklist when replacing placeholders

1. **Headings:** Keep one meaningful `h1` per page, then use `h2`, `h3`, etc. without skipping levels simply to change appearance.
2. **Links:** Use descriptive link text, e.g. “View curriculum design project,” not repeated “click here.” Don't insert `href="#"` placeholder links.
3. **Images:** For meaningful images, supply concise alt text describing their **purpose in context**: `<img src="assets/example.jpg" alt="...">`. For purely decorative images use `alt=""`. Don't put important text inside images.
4. **Documents:** Make linked PDFs accessible (headings, tagged structure, sensible reading order, meaningful links). Provide an HTML alternative when appropriate.
5. **Video and audio:** Add accurate captions, transcripts, and audio description when required.
6. **Color:** If you customize the theme, check contrast again. WCAG AA calls for **4.5:1** for ordinary text, **3:1** for large text, and **3:1** for important interface graphics/boundaries. Don't communicate status or importance through color alone.
7. **Text zoom and reflow:** Test zoom to 200% and 400%, a 320 CSS-pixel viewport, and increased line/word/letter spacing; no text or functionality should be clipped or obscured.
8. **Keyboard:** Tab from the beginning to the end of every page. Verify visible focus; no keyboard traps. Use Enter to activate tiles and buttons; confirm the mobile menu can be opened, closed, and dismissed with Escape.
9. **Screen readers:** Test at minimum with NVDA + Firefox or Chrome (Windows), and VoiceOver + Safari (macOS/iOS), if available. Check landmarks, headings, link names, current page, and mobile navigation announcements.
10. **Automated checks:** Run WAVE, axe DevTools, or Lighthouse accessibility checks on every published page; manually review reported issues and address them.

## References

- W3C WCAG 2.2: https://www.w3.org/TR/WCAG22/
- W3C accessibility evaluation overview: https://www.w3.org/WAI/test-evaluate/
- W3C Quick Reference: https://www.w3.org/WAI/WCAG22/quickref/

## How to edit colors

The top of `css/styles.css` has `--red`, `--yellow`, `--blue`, `--ink`, `--muted`, `--focus` and other tokens. Keep the focus ring highly visible against the local background. The accent bars are decorative; titles and labels remain readable in monochrome.
