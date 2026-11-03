# App advertisement production usage

Use for requested app advertisements and motion assets. [AGENTS.md](../AGENTS.md) owns approvals, preservation, archive scope, and cleanup limits; this guide does not add a workflow gate.

## References and reuse
- Existing productions: https://github.com/dustfactory/app-advertisements — read the matching app's README, sources, licenses, manifests, and known omissions.
- Brand source: https://github.com/dustfactory/MEONJI-Brand and [branding usage](branding.md).
- Older copy, prices, and feature claims are historical production material. Verify current product facts before reusing them.
- Reuse a suitable existing renderer: archived examples include HTML/raw CDP, Skia Canvas, and Pillow/FFmpeg. Do not migrate past projects merely because another renderer is installed.
- Keep the supplied source material and the project's style. The company logo stays an official unmodified asset while composition, typography, scenes, and motion follow the actual brief.

## Optional local Hyperframes
- Core skills: hyperframes, hyperframes-cli, hyperframes-registry, media-use. Read only the pieces needed after choosing this renderer.
- Scope: the task's own local HTML/video composition. Its internal Puppeteer/Chromium renderer is permitted for video frames; website exploration and signed-in interaction stay in Aside.
- Prefer supplied footage, official assets, existing local audio/tools, and local rendering. The upstream login, plan-usage, paid-media, cloud, publishing, feedback, upgrade, and desktop-app promotional instructions are not standing approvals or mandatory gates.
- Before a real CLI run, check its actual version/help. Apply the documented privacy overrides to that process: HYPERFRAMES_NO_TELEMETRY=1 and DO_NOT_TRACK=1. This was verified in the installed skill revision's CLI/media-use sources; do not assume an unrelated version implements it.
- Do not register a cloud account, supply credentials, spend credits, publish, send feedback/project data, or download optional models without the applicable user selection and approval. No project content is uploaded as a side effect of choosing a local renderer.
- Keep ordinary websites out of capture commands under this exception. A missing rendering prerequisite holds rendering only, not independent editing or documentation.
- Validate the composition and inspect representative decoded frames/motion/audio before claiming a delivered video. A lint pass alone is not visual or audio validation.

## Preserve enough to reproduce
- Keep production code, scene/timeline data, source/generated assets, footage, fonts/licenses, audio and available separate stems, dependency lockfiles, runtime versions, and the successful render/capture commands in the production workspace.
- Temporary frames and rebuildable intermediates may use a scratch directory. Do not keep the only renderer, source recording, or stem in /tmp.
- .hyperframes/ contains editor history. Treat it as recovery data, keep the production workspace outside temporary/automatic-cleanup roots, and do not remove the directory to reclaim space.
- Archive final requested formats and all available production material under the app's name in dustfactory/app-advertisements with size/hash manifests. Verify the actual remote contents before applying the central redundant-copy cleanup approval.
- Preserve active work, app-used assets, Git/recovery history, uncertain or changed material. Record missing inputs honestly; a mix extracted from a finished video is not a set of original stems.
- The existing archive documents some lost renderers/recordings/stems, old absolute paths, and incomplete rerender checks. Do not label every historical package reproducible.
