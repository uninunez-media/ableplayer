# AblePlayer Changelog

## 4.7.0

### Styling

- New default theme with modernized layout and variables for colors.
  - This summarizes a large number of individually small changes to the layour of AblePlayer elements.
- Removed many instances of positioning imposed from JS so that more positioning is controllable from CSS.
- Significant improvements to responsive desgin and behaviors.

### Features

- Add support for synchronized sign language sourced from YouTube
- Allow modal dialogs to be closed by clicking on the modal overlay.
- Support toggling the transcript area when using a pre-defined transcript area.
- Allow non-standard support for single character hours value in VTT timestamp formats.

### Bug fixes

- Fix window resizing issue in sign language windows.
- Reset scroll position after closing fullscreen to prevent unexpected shift of position.
- Remove deprecated `modestbranding` parameter from YouTube player params.
- Add `origin` property to YouTube player params.
- Reduce fullscreen timeout from 1000ms to 100ms. Ensures the resize method executes when leaving fullscreen quickly.
- Track active media so focus is sent to correct player after refreshing controls.
- Change modal dialog positioning to fixed to prevent unexpected shifts of position.
- Properly disable `transcript` with `data-include-transcript="false"`
- Cookie referred to wrong variable when setting sign language data.
- Prevent scrolling of background content when modals are active.
- Allow the audio description text panel to show when there is both a VTT and a described video.
- Handle `data-skin` set to invalid value.
- Prevent floating windows from being positioned above the top of the viewport.
- Ensure last block of captions in transcript are wrapped in `.able-transcript-block`.
- Use `outerHeight` in several places where `height` was used so calculations account for whole element height.
- Fix unwanted lines generated in lyrics mode.
- Verify the target transcript div exists before setting the external div flag.
- Support the default value for the `kind` attribute on `source` when omitted.

### Accessibility

- Ensure all Able Player controls meet WCAG SC 2.5.8 by being a minimum of 24px by 24px.
- Make visible alerts dismissible
- Extend default period of visibility for expiring alerts to 20 seconds.
- Improve accessibility of draggable containers when using a screen reader. More predictable keyboard handling & audible feedback.

### Internationalization

- Change all translation files from JS containing a JSON object to `.json`.
- Add `ms` and `pl` to list of supported languages.
- Add several new strings to translation files. (Translations needed.)

### Build tools & Code clean up

- Change `ableplayer.dist.js` build to remove comments, reducing the dist file size by about 150Kb.
- Simplify if/else statements. Use ternary or swithc where appropriate or collapse arguments.
- Reformat if/else statements to remove line breaks before `else`.
- Remove `$ableColumnLeft` - unused and unidentified variable.
- Remove unneeed -moz and -mix prefixed fullscreen properties.
- Only create a single alertBox container and move in DOM as needed instead of managing three separate containers.
- Add new prototype to set the text for buttons.
- Add new prototype to set icons for buttons.
- Make use of existing `ucfirst` prototype.
- Remove `number.isInteger` polyfill (already unused).
- Remove tests for `svg` support.
- Remove remaining IE compatibility supports.
- Replace `e.which` with `e.key`.
- Remove obsolete Safari keycodes.
- Add prototype for syncing sign language video.
- Remove unused prototype `AblePlayer.prototype.isCloseToCorner`.
- Remove unused `mediaType` argument from AccessibleSlider prototype.

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