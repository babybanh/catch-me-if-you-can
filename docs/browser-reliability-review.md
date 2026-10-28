# Browser reliability review — 2026-10-27

## Intent preserved

Keep immediate movement-triggered music: 1134816 deliberately reverted an added delay. Keep the later intro-readiness fix 3f7b3b6; do not restore reverted loading-cover variants (7ac4231/e294333). Preserve gesture unlock from 5091d70.

## Changes

Decode active short WAV effects before collision and play buffers after a real gesture, retaining HTML audio fallback. Clear stale keys/joystick and stop hidden sound. Defer music, load only active SFX initially, and avoid repeated hidden tuning/unchanged HUD updates.

## Validation

7 Node regression tests; production build; desktop Chromium and mobile WebKit lifecycle/play tests; 18-pickup phase progression and restart; cold pickup handler 55 ms before and 0 ms after in one mobile WebKit run.

Mobile checks used WebKit on macOS with a 390×844 touch viewport. Cold-pickup fixtures position collectibles at the player and run the normal collision/score/audio path. Playback was checked through running audio contexts and started buffers, not recorded speaker output. These are not physical iPhone/Android tests. Occasional long cold frames also occur with SFX off; repeat on a real phone before treating overall frame smoothness as resolved.
