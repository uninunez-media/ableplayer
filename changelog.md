# AblePlayer Changelog

## 4.6.0

### Styling
- Change default skin to "2020".
- Removed IE-specific styles.
- Fix overflowing bottom border on transcript container & set padding to fixed value.
- Remove inline CSS forcing center alignment on dialog headings.
- Improvements to dialog layout.
- Increase size of volume slider.
- Set `video` element to `display: block;` to prevent extra space after element.
- Style updates to Video Transcript Sorter tool.
- Force `iframe` to 100% max-width 100% to prevent overflowing container.
- Updated transcript & sign language container settings, settings tooltip, and settings popup.

### HTML
- Add wrapper around the left and right control containers.
- Change dialog close button from 'X' to '×', to improve alignment.
- Wrap VTS header in `thead` element.
- Add `type="button"` to big play button.

### Bug Fixes
- Fix `data-vimeo-id` loading.
- Fix failure of Safari/MacOS on getVoices for speechSynthesis.
- Improve speech initialization for Linux browsers.
- Fix loading of preferences across players.
- Replace deprecated jQuery methods: `.click`, `.focus`, `.change`, `.keydown`, `$.trim()`, and `.isNumeric`.
- Extensive removals of unused variables and unused code.
- Limit default maxwidth on transcript and sign containers to no larger than viewport.

### Accessibility
- Use `inert` to represent interactivity state of content outside of modals.
- Remove `role` and `aria-label` on transcript containers if they are not inside a dialog.
- Fix caption sizing on small viewports.
- Render volume percentage in the initial volume button state & updates.
- Fix translation rendering so Full Screen buttons are properly labeled.
- Add `aria-atomic="true"` on the speed notification container.
- `tabindex` missing from draggable toolbar, preventing focus from being sent and breaking keyboard support.
- Update visible order of draggable toolbar controls, so focus order matches visible order.

### Features
- Add support for secondary sign language locally when sourcing main video from YouTube.

### Security
- Update DOMPurify to version 3.2.6; improve validations.
- Add URL validation to src, audio description src, sign src, and track URLs.
- Add sanitization to YouTube IDs, track titles.
- Update Vimeo URL parsing.

### Internationalization
- Fixed issues in Polish, Canadian, and Indonesian translations.
- Fix translations references for full screen text strings.
- Added Malay translation.

### Release Assets
- Removed build tools, unbuilt scripts, demos, and media assets from the release archives. You will need to check out the repository to have access to these resources. Reduces the zip download from over 160 MB to under 1 MB.

### Demos & Docs
- Made demo pages responsive.
- Updated demo pages to have more similar styles to docs.
- Broke Contributing into a separate doc.
- Updated Jekyll template to add navigation to docs header.
- Updated main readme to add in-page navigation.
- Reorganized main readme.

### Contributors

The following people contributed to this release (if I missed you, please let me know!)

@terrill, @candideu, @xerc, @jbylsma, @amartincua, @zwiastunsw, @conorom, @jeanem, @joedolson, @Justryuz, @dependabot

**Full Changelog**: https://github.com/ableplayer/ableplayer/compare/v4.5.1...v4.6.0