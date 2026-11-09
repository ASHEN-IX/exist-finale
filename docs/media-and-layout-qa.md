# Presentation media and layout check

Checked 9 November 2026 using Playwright CLI with local Chromium and ImageMagick. Scope: this 20-slide HTML presentation; opening the linked Next.js demo was smoke-tested, not its complete purchase flow.

## Changes

- Replaced the persona information poster on slide 4 with a generated portrait of fictional Yassine (1024 × 1536). Persona facts remain live text; the portrait is labelled fictional.
- Replaced the 244 × 311 suit thumbnail with a generated 1024 × 1536 suit concept, preserving the existing conceptual-product disclaimer.
- Copied the sharper campaign media from `../exist-campagne-nextjs/public/media/`: hero-desktop (1920 × 1080), hero-mobile (1080 × 1350), and closing-campaign (1920 × 900). Replaced the stretched 577 × 365 hero and 409 × 187 closing background. Removed the enlarged 348 × 186 decorative ribbon from the cover.
- Removed the SVG fractal-noise overlay from every slide.
- Constrained intrinsic image sizes on the persona, demo and accessories slides; reduced the demo heading and corrected the local startup directory in README.
- Displayed the full landing mockup, email and loyalty posts with `object-fit: contain`, instead of cropping away their content.

## Media assessment

Visual inspection distinguishes softness, compression artifacts, genuine surface texture, and added noise. These are qualitative judgments, not calibrated signal-to-noise measurements.

- The replaced hero, suit and closing images were visibly soft from enlargement. The replacements show clearer facial, fabric and edge detail at presentation scale.
- The 1080 × 1350 campaign posts and loyalty visuals have no prominent distracting random grain at their intended display size. Fabric weave and skin detail remain visible as normal image texture.
- The new persona and suit concepts have clean edges and backgrounds; natural texture is intentionally retained.
- The empathy map is 1024 × 572. It is sufficient as an overview, but small embedded text remains limited by the source resolution; click to zoom. Enlarging the raster cannot recover missing detail.
- The landing mockup is a 1024 × 1536 raster. Its fine text and the 850 × 1779 email are best inspected through image zoom or the live demo.
- Older thumbnail assets remain in the repository for reference. They are no longer used for the large hero, suit and closing visuals.

## Video exports found on Desktop

- `../exist-campagne-nextjs/out/EXIST_Ceremony_Reel_15s.mp4`: H.264 video at 1080 × 1920, AAC audio, 15 seconds. Full FFmpeg decode succeeds. An inspected detail frame shows visibly soft enlarged cufflinks and very low-contrast lettering; container resolution alone does not establish visual quality. Kept out of the presentation pending visual improvement.
- `../exist-campagne-nextjs/out/EXIST_Ceremony_Reel_25s.mp4`: unreadable; FFprobe reports `moov atom not found`. This export is incomplete, not a validated deliverable.
- Updated slide 10, README and speaker notes to distinguish the existing test export from a finished Reel.

## Verification

- All 20 slides captured and visually reviewed at 1920 × 1080; no JavaScript page errors or detected text crossing slide/footer bounds after the fixes.
- All 15 distinct local media references resolve. Every asset decodes without ImageMagick warnings.
- Slide titles and durations match `slides.json`: 20 slides, 1140 seconds of suggested narration.
- Interaction checks passed: persona deep link, exactly one active slide, portrait zoom and Escape, speaker notes, all 20 menu entries, menu selection, previous/next, Home/End boundaries, fullscreen, and opening the local demo in a new tab.
- All 20 slides checked at 1280 × 720, 1366 × 768 and 390 × 844. Fixed the Reel caveat’s unscaled text on narrow screens. The deck intentionally retains its 16:9 presentation format; portrait-phone text is small.
- Navigation also works with the external GSAP script blocked and reduced motion enabled.
- The local demo returned content on port 3000. This link requires the demo server to be running on the presenting computer.

## Generation

Both new images were produced with the built-in Imagegen tool. The prompts are preserved in `image-generation-prompts.md`. The original persona sheet is retained as a source asset; it is no longer the portrait shown on slide 4.
