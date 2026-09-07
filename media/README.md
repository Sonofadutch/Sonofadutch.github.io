# media/

Screen captures, screenshots and the link-preview image. Filenames referenced by
the pages:

| File | Used by | Size |
|---|---|---|
| `one-more-year.jpg` | home card + case study | 1280×800, 16:10 |
| `weekly-invoice.png` | home plate + case study | still of the demo |
| `concrete-online.jpg` | home card + case study | 1280×800 |
| `pentest-plus.png` | home card + case study | 1280×800 |
| `og.png` | link previews (WhatsApp, LinkedIn, email) | 1200×630 |

Until a file exists the page shows a striped placeholder with the filename on it.
Nothing breaks — the `<img>` removes itself. Drop the file in and it appears.

## What to record — the short answer

**No talking-head video.** Nobody watches it, and it dates the moment your UI
changes. What people actually watch is a **silent 10–20 second loop** of the thing
being used. One task, start to finish: open the link → make the picks → see the
result.

Rules of thumb:

- **10–20 seconds.** If it needs longer, it needs two clips.
- **No cursor hunting.** Rehearse the clicks so the movement looks decided.
- **Real data, fake names.** Nothing recognisable, no real email addresses.
- **Phone captures beat desktop captures** for anything a phone is the real target
  for — record the phone screen, drop it in a device frame if you like.
- **Under 4 MB.** GitHub Pages serves it on every page load.

Add one narrated walkthrough (90 seconds, your voice, unlisted on YouTube) for
your single strongest project only, and embed it at the bottom of that case study.
That is the ceiling. Two of them and it reads like a course.

## How to record on Windows

**ScreenToGif** (free, open source) is the standard tool for this:

```powershell
winget install NickeManarin.ScreenToGif
```

Record → select the window → stop → in the editor: **Remove duplicate frames**,
drop to **15 fps**, resize to **1280 wide**, then Save as GIF.

For a smaller file at the same quality, export **MP4** instead and swap the tag in
the page (the CSS already styles `video` the same as `img`):

```html
<video src="../media/one-more-year.mp4" autoplay muted loop playsinline></video>
```

Muted + `playsinline` matter — without them iOS refuses to autoplay.

**Phone recording:** Android has screen record in the quick settings; iPhone has it
in Control Centre. AirDrop or cable it over, then trim in ScreenToGif or
[ezgif.com](https://ezgif.com).

## The og.png

1200×630, dark background, your name and one line. It is what shows up when you
paste your link into a message — worth twenty minutes, because it is the first
thing a client sees.
