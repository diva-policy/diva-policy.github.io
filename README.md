# DIVA project page

Built on the [Nerfies](https://nerfies.github.io) project page template
(<https://github.com/nerfies/nerfies.github.io>), which is released under
[CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/). The attribution in the
page footer is part of that license and must stay.

`index.html` is still the Nerfies page. It is kept verbatim as the working reference for
the layout: swap its text, figures and videos for ours rather than starting from a blank
file.

## What was changed on import

* **Google Analytics removed** from the `<head>`. The template's own footer asks anyone
  borrowing it to do this, since the tag reports to the Nerfies property.
* **Their demo media was not copied**, 83 MB of it: `static/videos/`,
  `static/interpolation/` and the two `interpolate_*.jpg` frames. Only `favicon.svg` was
  kept from `static/images/`. Everything under `static/css/` and `static/js/` is intact,
  which is the part that actually makes the template work.

So the video and carousel elements in `index.html` reference files that are not here.
They render as empty boxes until our own media replaces them. The sections to fill:

| element | what it was |
|---|---|
| `static/videos/teaser.mp4` | hero video under the title |
| `static/videos/steve.mp4`, `chair-tp.mp4`, `shiba.mp4`, `fullbody.mp4`, `blueshirt.mp4` | carousel of results |
| `static/videos/replay.mp4`, `dollyzoom-stacked.mp4` | side-by-side comparison blocks |
| `static/videos/matting.mp4`, `coffee.mp4`, `toby2.mp4`, `mask.mp4` | method and ablation clips |
| `static/interpolation/stacked/*.jpg` | the interpolation slider |
| `static/videos/nerfies_paper.pdf` | the paper PDF link |

## Local preview

    python -m http.server 8000 --directory paper/website

then open <http://localhost:8000>. A plain `file://` open works too, but the carousel and
slider scripts behave better over HTTP.

## Candidate media we already have

* `paper/repro/figs_regen/` holds every figure in the paper.
* `~/Desktop/vinner/` holds the rendered rollout videos and GIFs, including the paired
  transport clip and the three-way square clip.

## Published at

<https://diva-policy.github.io> — GitHub Pages, from `main` at the repository root of
`diva-policy/diva-policy.github.io`. That repository is a copy of this directory, not a
submodule: to publish a change here, copy the directory over and push.
