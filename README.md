# Waleed Khalid: night sky portfolio

A single static page with no libraries, drawn in WebGL. The sky (Milky Way by night, clouds by day) is painted once
into a panorama at startup. Each landscape is real 3D terrain, lit by the sun or moon, rendered once in the background
when its scene is first chosen; water, the road and embers are drawn live on top. Every frame, that panorama is resolved into pixel-sharp stars at the full
resolution of the screen, and about 45,000 brighter stars and a mountain horizon are drawn on top.

The sky reads left to right as a career timeline in four chapters. Bright stars joined by lines are projects.
The timeline along the bottom lists every project in order; scrolling or the arrow keys move through them.

Visitors can pick a scene (Mountains, Sea, Forest, Lava or Drive) and switch between night and day with the controls
at the top right. Their choice is remembered in their own browser.

## Put it on GitHub Pages

1. Create a public repository named `<your-username>.github.io`.
2. Upload `index.html` (and this README) to the root of the `main` branch.
3. In the repository, open Settings, then Pages. Choose "Deploy from a branch", pick `main` and `/ (root)`, and save.
4. The site appears at `https://<your-username>.github.io/` within a minute or two.

## Change the content

The CV text is a verbatim copy of the master profile. All projects live in the `SKY` array near the top of the script in `index.html`, in time order. Each chapter has a
name, a year range and a position in the sky (`az`, `alt` in degrees). Each star has a name, a topic (`area`), an
offset from the chapter centre (`d`), a brightness (`mag`, lower is brighter), a line of context (`where`), a few
facts and the tech used. The order of stars in the array is the order of the timeline. The plain CV view is built
from the same array.

## Notes

- If WebGL is not available, the page shows the plain CV automatically.
- Visitors who prefer reduced motion get a still sky that only redraws when they move it.
- Visited stars are remembered in the visitor's own browser only.
