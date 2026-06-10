# altena-assets

Hot-linkable brand assets for the [altena.lovable.app](https://altena.lovable.app/) build, sourced from ALTENA's official asset pack (Rui Li, ALTENA New Material Technology (Shandong) Co., Ltd.) and optimized for web use.

## How to reference

Each file is reachable at:

```
https://raw.githubusercontent.com/MattKahn13/altena-assets/main/<directory>/<file>
```

Or via jsDelivr's GitHub mirror (CDN-cached, slightly faster outside the US):

```
https://cdn.jsdelivr.net/gh/MattKahn13/altena-assets@main/<directory>/<file>
```

## Layout

```
logo/                Brand logo, 6 variants exported from the AI master file.
hero/                Studio shots from Rui's pro shoot, web-sized.
before-after/        Before/after slider source frames (Slow_small.mp4 extract + GoPro alternates).
heating-rods/        Rod product photography + technical cross-section diagram.
about/               Factory exterior, factory interior, production-floor shots.
videos/              Install walkthroughs + product overviews + factory tour.
posters/             Poster-frame JPGs for each video (use as the <video poster=...> source).
```

## Source-of-truth mapping

For the Lovable build, see `parcelle-agency-kb/clients/altena/intake/asset-url-map.yaml` -- it maps every Lovable site slot (homepage hero, before/after slider, `/heating-rods` cross-section, etc.) to the specific URL from this repo.

## Optimization notes

- Studio JPGs were originally 13--18 MB each; resized to <=2400 px long edge, JPEG quality 88 (final size ~400--600 KB).
- Logo PNGs are direct page-renders from `阿纳logo.ai` (PyMuPDF, 150 DPI), preserving transparency.
- Videos kept at original quality from Rui's source (`.mp4` H.264, 4--30 MB each).
- Poster frames are extracted at 1 second into each video via `ffmpeg -ss 1 -vframes 1`.

## License

Assets © ALTENA New Material Technology (Shandong) Co., Ltd.

Hosted and used by Granite Springs Enterprises LLC / Parcelle Agency under engagement agreement with ALTENA (engagement opened 2026-05-07, ongoing).

For any use outside the altena.lovable.app build or successor production sites for ALTENA, contact Rui Li (Rui@altenatech.com) or Matt Kahn (mjk366@cornell.edu).
