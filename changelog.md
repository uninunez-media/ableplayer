# AblePlayer Changelog

## 4.6.0

### Styling
- Change default skin to "2020".
- Removed IE-specific styles.
- Fix overflowing bottom border on transcript container & set padding to fixed value.
- Remove inline CSS forcing center alignment on dialog headings.
- Improvements to dialog layout.
- Increase size of volume slider.

### HTML
- Add wrapper around the left and right control containers.
- Change dialog close button from 'X' to '×', to improve alignment.

### Bug Fixes
- Fix `data-vimeo-id` loading.
- Fix failure of Safari/MacOS on getVoices for speechSynthesis.
- Improve speech initialization for Linux browsers.
- Fix loading of preferences across players.
- Replace deprecated jQuery methods: `.click`, `.focus`, `.change`, `.keydown`, `$.trim()`, and `.isNumeric`.
- Extensive removals of unused variables and unused code.

### Accessibility
- Use `inert` to represent interactivity state of content outside of modals.
- Remove `role` and `aria-label` on transcript containers if they are not inside a dialog.
- Fix caption sizing on small viewports.
- Render volume percentage in the initial volume button state & updates.
- Fix translation rendering so Full Screen buttons are properly labeled.
- Add `aria-atomic="true"` on the speed notification container.

### Features
- Add support for secondary sign language locally when sourcing main video from YouTube.

### Security
- Update DOMPurify to version 3.2.6; improve validations.
- Add URL validation to src and track URLs.

### Internationalization
- Fixed issues in Polish, Canadian, and Indonesian translations.
- Fix translations references for full screen text strings.
- Added Malay translation.

### Release Assets

- Removed build tools, unbuilt scripts, demos, and media assets from the release archives. You will need to check out the repository to have access to these resources.

### Contributors

The following people contributed to this release:

TBD