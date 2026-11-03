# Brand and publisher splash usage

Use for app creation, branding, icons, and splash work. [AGENTS.md](../AGENTS.md#product-and-ui) owns the common requirement and approval boundaries. This guide supplies sources and implementation examples.

## Official assets
- Canonical source: https://github.com/dustfactory/MEONJI-Brand
- Read BRAND_GUIDELINES.md; select distribution assets from svg/wordmark/ or png/wordmark/. The official original, black, and white variants are available.
- Base URL: https://cdn.jsdelivr.net/gh/dustfactory/MEONJI-Brand@main/
- Example wordmark: png/wordmark/meonji-wordmark-original-1024.png.
- Include the unmodified official distribution file in the app when needed for an offline launch. Keep its source/version identifiable; MANIFEST.json and SHA256SUMS can confirm identity. A runtime URL must not be the only way the publisher mark appears.
- Keep the original shape, proportions, transparency, and clear space. Choose an official color variant for contrast; do not redraw, recolor by runtime tint, crop, stretch, rotate, or add effects to the mark.
- master/ preserves the originals. spec/redraw/ contains a separately reconstructed specification version; do not substitute it for the distribution logo without a requested brand change.
- Publisher/copyright defaults to MEONJI and new bundle/package prefixes to com.meonji. Keep existing registered IDs and product icons.

## Apps and games: brief publisher splash
- A new app or game shows the MEONJI **wordmark**, used as the publisher's identifying mark, at cold launch before its normal entry screen.
- Align the mark to the horizontal and vertical center of the full visible viewport. Retain the asset's transparent margins and aspect ratio; do not copy old x=0.54 or fixed horizontal-shift values.
- Use a quiet solid background with sufficient contrast, continuous with the native launch background where practical. The mark is visible for about 0.9–1.0 seconds; a short fade may fit within that interval.
- Use the approved default size below, keeping the asset's clear space and proportions. Confirm visible centering and legibility on the designated device.
- Load the bundled mark without network waits. Initialization may proceed concurrently. Then enter the app's existing loading, menu, or intended deep-link flow; preserve any pending destination.
- Show once per cold launch, not on every resume, route change, or rebuild. Avoid two consecutive publisher-brand stages between the OS launch screen and app intro.
- Missing assets must not trap users on a blank splash. Continue safely and report/fix the packaging defect before delivery; do not fabricate a replacement wordmark.
- For an actual implementation change, capture the previous screen, run cold launch, observe mark/centering/duration/transition and applicable failure paths, and report real before/after images. No live launch is implied by reading these references.

### Default wordmark size (approved 2026-11-03)
Use the full visible viewport width W, before safe-area padding, with the current orientation:

| Orientation | Wordmark width | Reference viewport and width |
|---|---|---|
| Portrait, including square | W × 0.497777778 (about 49.78%) | 360 × 640 → 179.2 logical pixels |
| Landscape | W × 0.30625 (30.625%) | 640 × 360 → 196 logical pixels |

- Use CSS pixels on the web, points on iOS, dp on Android, or framework logical pixels. Scale height with the official 1162:356 aspect ratio; center the entire distribution canvas on both axes.
- These values already include the approved 30% reduction. Do not apply another 0.7 multiplier. For this splash, the approved size takes precedence over the general 256-CSS-pixel wordmark recommendation; keep the artwork unchanged.
- The mark remains visible for about one second. This sets defaults for future apps and games; changing existing apps is a separate task.

## Existing references (source inspected 2026-11-03)
- Dunk Loop: ContentView.swift, PublisherSplashScreenView / PublisherBrandMark / scheduleSplashDismissal. It uses a bundled meonji_publisher_logo and switches from publisher to game stage after 0.90 seconds.
- secret-hand-prototype: flutter_app/lib/main.dart, _MeonjiSplash / _SplashStage and _publisherHold; theme/dolus_theme.dart, DolusAssets.meonjiLogo. It uses a bundled transparent image, a plain full-bleed background, and a 900 ms publisher stage before loading.
- These projects explain the brief publisher-first flow. Their old logo artwork, tinting, and optical offsets are not the asset or placement authority for new work. The current official asset and the user's centered placement take precedence.
- Existing projects are references, not a request to retrofit or release them during a documentation task.
