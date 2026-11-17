# Documentation notes for DiRoots.DiCivil.Design.Releases

Found while testing documentation PR previews on a replica of this repository (`DiRoots-Mauro/DiRoots.Sandbox.DiCivilDesign.Releases`) and on the production site. None of these items is caused by the preview workflows; they are listed so they can be fixed separately.

## Site size

The `gh-pages` branch holds about 543 MiB of files, almost all images and GIFs. GitHub Pages recommends repositories and published sites below 1 GB.
- Previews are not affected: they reuse the live images, so a preview of this site measured 1.6 MiB instead of 544 MiB.
- Suggested fix: compress the largest GIFs or convert them to MP4/WebM. Largest files: `assets/images/GIFs/GP/Pipe-Trenches.gif` (60.5 MiB), `assets/images/GIFs/GP/Object-Feature-Line-Integration.gif` (45.0 MiB), `assets/images/GIFs/ET/Demonstrate-the-complete-workflow.gif` (27.0 MiB), `assets/images/GIFs/GP/Section-Reference.gif` (26.4 MiB), `assets/images/GIFs/ET/Region-based-stripping-configuration-with-different-depths.gif` (26.1 MiB).

## HTTPS is not enforced

GitHub Pages serves this site over HTTPS, but "Enforce HTTPS" is off, so `http://` requests are not redirected. The preview links always use `https://`.
- Suggested fix: Settings > Pages > enable "Enforce HTTPS".
