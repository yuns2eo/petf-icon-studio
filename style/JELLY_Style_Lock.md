# JELLY ICON — UNIVERSAL STYLE LOCK

## Purpose

Use this file for **every** jelly icon image, regardless of object, version (cat / dog / common), or use case.

The jelly icon set is one continuous visual family. The supplied reference images are the visual source of truth:

- `references/cat/` — cat version (pink & paw)
- `references/dog/` — dog version (teal & bone)
- `references/common/` — common version (pink & teal accent, no animal motif)

When reference images are attached, they override any wording that appears less precise. Every new icon must look like it was made in the same session as the references.

---

## What is fixed: the family style

### Canvas and composition

- 1:1 square canvas
- background: see **Background options** below (default is black)
- exactly one object (a matching set such as toothbrush + toothpaste may use two; combinations follow the **Combination rule** below)
- the object is perfectly centered and fills about 70–75% of the frame, fully visible, never cropped
- front three-quarter view, camera slightly above (about 15–20 degrees), mild telephoto perspective

### Background options

There are exactly two backgrounds. Use **BLACK** unless the request explicitly asks for white (흰 배경, 화이트 배경, white).

**BLACK (default)**

- pure solid black background (#000000), no gradient, no floor plane, no props
- only a soft glow reflection in the version color directly under the object
- no hard drop shadow

**WHITE (only when requested)**

- pure solid white background (#FFFFFF), no gradient, no floor plane, no props
- the version-color glow is replaced by a very soft, short contact shadow directly under the object, lightly tinted with the version color (pink for cat & common, teal for dog)
- no hard drop shadow, no long cast shadow
- keep the rim light subtle so the edges stay defined against white
- white parts of the object must stay readable: separate them from the background with soft grey-pink shading on their curved surfaces, never let them blend into the background
- the material, colors, motif, lighting direction, and composition do not change — only the background and the glow/shadow change

The reference images are on black. When generating on white, still attach the same references for the object style, and state the white background in the prompt.

### Material

Preserve the exact material language shown in the references:

- soft glossy jelly / soft-touch plastic body
- slightly translucent with gentle subsurface scattering, but reading as a solid colored body
- thick, puffy, inflated volumes with heavily rounded edges and no sharp corners
- crisp, long white specular highlights that follow the curved edges

Allowed secondary materials, only where the object needs them:

- clear acrylic / glass for containers whose contents must be visible (jars, pouch windows, fountains, treat balls)
- chrome / polished silver for small metal parts (rings, clips, hooks, cart frames, clock legs)
- realistic contents: kibble, jerky sticks, litter sand, sisal rope, cream plush cushion, feathers

Do not create matte surfaces, wood grain, rough textures, fully metal bodies, neon emission, or fully transparent bodies.

### Lighting

- large softbox key light from the upper left
- subtle rim light separating the object from the black background
- studio product-render quality

Do not use flat illustration, outlines, cel shading, cartoon line art, or dramatic colored lighting.

### Form language

- a real object simplified into chunky, toy-like proportions
- only the 2–4 parts that make the object recognisable
- realistic small details (barcodes, screws, stitching) are reduced to one or two cute hints at most

### Text

- default: no text, letters, or numbers on the object
- exception: an object defined by a symbol may show only that symbol (`%`, `₩`, `P`, `COUPON`, a year number), in a bold rounded sans-serif, in white or the version main color
- never add logos, brand names, or watermarks

---

## What may freely change: the object layer

The following are **not** part of the fixed style and may be specified freely in natural language:

- which object is drawn
- the object's own parts, contents, and silhouette
- which version applies (cat / dog / common) — colors and motif then come from the matching `versions/` file

Do not use the object to break the style: a new object must still be glossy jelly, centered on black, lit from the upper left, with rounded toy-like forms.

---

## Combination rule

A request may combine registered icons into one image, e.g. "a basket holding a pink coupon, 몽실이, and a pink gift box".

- one **container** icon (basket, cart, box, bowl, bed, carrier) holds up to **3 items**
- every item keeps its own registered design: shape from `library/`, colors from its version, characters from `characters/JELLY_Characters.md`
- items are scaled down to fit naturally inside or peeking out of the container, overlapping slightly, with the most important item in front
- the whole group is treated as one object for composition: centered, 70–75% of the frame, same camera, light, and background rules
- the image's glow color follows the container's version
- reference limit for combinations: up to **4 images** — the container's front image plus one front image per item; character references are always included

Do not invent new items, change any item's design to match the others, or exceed 3 items.

---

## 4-view sheet rules

The 4-view sheet is always generated **with the finished front image attached as the reference**. Never generate a 4-view from text only.

- 1:1 canvas divided into a 2×2 grid, same background as the front image (black or white), no divider lines, labels, or arrows
- top-left: front three-quarter view, same angle as the front image
- top-right: right three-quarter view, rotated about 45 degrees
- bottom-left: left-rear three-quarter view, rotated about 135 degrees
- bottom-right: back view (side view if the back is identical to the front)
- all four views at the same scale, same vertical position, same camera height and lighting

Between views, never change the shape, proportions, colors, material, number of parts, part orientation, or the motif's shape and position. Only the viewing angle changes.

---

## Non-negotiable negative rules

Never:

- use a background other than pure black (default) or pure white (only when requested), or show a floor, table, or scene
- mix version colors (teal on a cat icon, pink on a dog icon)
- add more than one motif, or the other version's motif
- add text, logos, or watermarks outside the text exception
- switch to matte, illustrated, outlined, or cel-shaded styles
- add hands, people, unregistered characters, or extra objects (only 몽실이 & 방실이 from `characters/` are allowed)
- redesign parts between the front image and the 4-view sheet

The family style is fixed. Only the object changes.

---

## Prompt assembly

Build every prompt in this order and keep each block's wording:

```
A single cute 3D icon of {object description}, rendered as a premium glossy jelly-plastic toy.

[STYLE] Soft glossy jelly / soft-touch plastic, slightly translucent with gentle subsurface scattering, thick puffy rounded forms, every edge heavily rounded, simplified toy-like proportions, crisp long white specular highlights following the curved edges.

[VERSION] {color & motif block from versions/ file}

[COMPOSITION] 1:1 square, one object only, perfectly centered, filling about 70-75% of the frame, fully visible. Front three-quarter view, camera slightly above (15-20 degrees), mild telephoto perspective.

[LIGHT] Large softbox key light from the upper left, subtle rim light, studio product render.

[BACKGROUND] — use one of the two lines
  BLACK (default): Pure solid black background (#000000), no floor, no props, no gradient. Only a soft {glow color} glow reflection under the object, no hard shadow.
  WHITE (on request): Pure solid white background (#FFFFFF), no floor, no props, no gradient. Only a very soft short contact shadow under the object, lightly tinted {glow color}, no hard or long shadow. Subtle rim light keeps the edges defined; white parts stay readable with soft shading.

[TEXT] {"No text, letters or numbers on the object." or the allowed symbol}

[NEGATIVE] matte finish, flat illustration, outline, cel shading, wood grain, rough texture, neon emission, extra objects, hands, people, logo, brand name, watermark, random text, gradient background, grey background, visible floor, hard shadow, cropped object, off-center
```

On WHITE, add to the negative: `colored glow, neon halo, white parts blending into the background, long cast shadow, off-white or cream background`.

For the 4-view sheet, start with `Use the attached front image as the exact design source. Keep the identical object.` then add the 4-view sheet rules above, the same [VERSION] block, and the negative `redesigned parts, rotated or reshaped details, different colors between views, labels, arrows, divider lines`.

---

## Generation checklist

Before generating, confirm:

1. Which version applies, and which `versions/` file was loaded? Which background — BLACK (default) or WHITE (only if asked)?
2. Which reference images from the same version are attached (2 at most, plus the front image for a 4-view)?
3. Is the object described by shape and parts only, leaving color, material, light, and background to the lock blocks?
4. Is any text on the object? If so, is it inside the text exception?
5. For a 4-view: is the finished front image attached?
