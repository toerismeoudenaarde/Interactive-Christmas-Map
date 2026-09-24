# Interactive Christmas Map Oudenaarde

Interactive Christmas map created for Toerisme Oudenaarde

## Live version

https://oudenaarde-kerst.netlify.app/

## Main files 

-index.html - map structure, markers, positions, popup texts and visual-effect classes
-style.css - visual styling, object sizes, marker glow effects and decorative snow animation
-script.js - zooming, panning, and popup positioning and popup behavior
-images/ - map, objects, and marker illustrations

## Editing text

Marker titles and texts can be edited in index.html:

data-title="..."
data-text="..."

## Editing positions

Marker positions are defined directly in index.html:

style="left: 62%; top: 29%;

Decorative object positions are defined in style.css with:

left:...%;
top:...%;

Decorative map objects are positioned in style css:

left:..%;
top:...%;

Decorative snow dots are positioned inside the snow-layer gradients:

circle at 46% 10%


## Editing sizes

Decorative object sizes use:

--object-width:...%;

Marker sizes use:

--marker-width:...%;

## Visual effects

### Marker glow

Clickable markers have a soft silver glow by default.

Selected markers can use a stronger animated golden glow.
To apply it, add the `golden-glow` class to the marker in `index.html`:


class="marker ijsbaan-marker gold-glow"

The golden glow animation is defined in style.css under:

.marker.gold-glow.img

and

@keyframes goldenChristmasGlow

Removing the gold-glow class restores the default marker appearance.

The map contains two decorative snow layers:

<div class="snow-layer snow-layer-a" aria-hidden="true"></div>

<div class="snow-layer snow-layer-b" aria-hidden="true"></div>

The layers fade alternately to create a continuous soft snow-light effect.

Snow position, sizes and opacity can be edited in style.css under:

.snow-layer.a
.snow-layer.b

Individual snow dots are positioned using percentage controls the horizontal position 
and the second controls the vertical position.

The alternating animation is controlled by:

@keyframes snowLayerA:
@keyframes snowLayerB;

/*-------*/


## Replacing images

Keep the same file name and replace the corresponding SVG or PNG 
inside the images folder.

Alternatively, update the src path in index.html.

## Deployment

The project is connected to GitHub and deployed through Netlify.

Changes pushed to the main branch are published by Netlify.

## Integration

The map can be embedded into another website using an iframe,

or the HTML, CSS, JavaScript and images can be integrated directly
by the website developer.

## Notes

The decorative glow and snow effects are purely visual and not affect marker interaction,
popup, behavior, zooming or panning.

The snow layers use `pointer-events:none`, so they do not block clickable markers. 

## Author 

Created by Julie Sinclair for Toerisme Oudenaarde, 2026




