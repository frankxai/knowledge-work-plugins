# Visual Prompt Library

Tested prompt patterns organized by use case. Each entry includes the base prompt, key variables to swap, and a negative prompt.

---

## Blog Hero Images

### Dark Premium Tech
```
Dark premium 3D render, [subject concept] visualized as glowing holographic interface,
floating above sleek obsidian surface, dramatic [accent color] and [accent color 2]
lighting against deep navy background, volumetric light rays, depth of field on
background elements, cinematic composition, highly detailed, 8K quality, no text,
no humans, no chrome robot figures
```
**Variables**: subject concept (e.g., "AI workflow", "data architecture", "content strategy"),
accent colors (cyan + gold, purple + orange, green + white)
**Negative**: chrome robots, stock photos, single color saturation, flat design, blurry

---

### Dark Premium Abstract
```
Cinematic macro photography, abstract [concept] represented as [metaphor],
deep [primary color] tones with [accent color] light leaks, intricate detail,
high contrast, bokeh background, professional product photography lighting,
editorial quality, no text, no people
```
**Variables**: concept (memory, velocity, connection), metaphor (crystal lattice, liquid
metal threads, light refraction), primary + accent colors
**Negative**: clipart, vector illustration, flat colors, generic

---

### Light Editorial
```
Clean editorial photography, [subject or object] on minimalist [surface description],
soft natural light from [direction], white and [warm/cool tone] palette,
shallow depth of field, lifestyle photography aesthetic, high resolution,
professional composition, no text
```
**Variables**: subject (open laptop, notebook, objects relevant to topic), surface (marble
desk, wooden table, white backdrop), light direction (left, overhead, window)
**Negative**: dark tones, dramatic lighting, 3D render style

---

## Social Media Images

### LinkedIn (1200×627)

```
Professional editorial photograph, [subject], clean background in [color palette],
high contrast composition, bold visual metaphor for [topic], works as thumbnail,
modern business aesthetic, 16:9 ratio framing, readable at small sizes, no text
```
**Variables**: subject (person at computer, abstract concept object, industry tool),
color palette (blues + white, dark + gold), topic keyword
**Negative**: cluttered, low contrast, small details, faces (unless portrait)

---

### Twitter/X (1600×900)
```
Bold graphic design, [concept] represented as [strong visual], [color 1] and [color 2]
high contrast palette, dynamic diagonal composition, punchy and attention-grabbing,
no text, scroll-stopping thumbnail quality, 16:9 widescreen
```
**Variables**: concept, strong visual (explosion of icons, fragmented grid, single
powerful object), colors (maximum 2 dominant)
**Negative**: subtle, soft, pastel, complex details, text

---

### Instagram (1:1 or 4:5)
```
[Style] composition, [subject] in center frame, [color palette] tones,
[mood] atmosphere, square or portrait format, high resolution,
visually cohesive with series aesthetic, no text overlaid
```
**Variables**: style (editorial, 3D render, illustration), subject, palette, mood
**Negative**: landscape orientation forced to square, off-brand colors

---

## Newsletter Headers (1200×400)

```
Wide-format editorial banner, [topic theme] visualized as [horizontal composition],
[color palette], clean uncluttered center area for text overlay, wide letterbox format,
premium feel, 3:1 aspect ratio, minimal but impactful
```
**Variables**: topic theme, horizontal composition (panoramic cityscape, technology
landscape, abstract band), palette
**Negative**: tall elements, heavy center content (needs text space), busy patterns

---

## Thumbnails (1280×720)

```
High-contrast YouTube thumbnail style, [main subject] in bold [color palette],
dramatic lighting, clear focal point readable at 120px width, no text,
striking composition, cinematic crop, thumbnail-optimized visual weight
```
**Variables**: main subject, color palette (bold contrasts work best)
**Negative**: soft contrast, detailed backgrounds, small elements, pastel tones

---

## Product Heroes

### Dark Premium Product
```
Premium product photography style, [product type] centered in frame,
dark [surface material] backdrop, [accent color] rim lighting on edges,
dramatic shadows, floating or elevated presentation, luxurious materials,
commercial photography quality, square format, no background clutter
```
**Variables**: product type, surface material (matte black, textured slate, obsidian),
accent color (gold, cyan, white)
**Negative**: white background, flat lay, lifestyle context, multiple products

---

### Light Workshop / Editorial
```
Clean product photography, [product type] on [neutral surface],
soft overcast studio lighting, minimal shadows, white or light gray background,
Scandinavian aesthetic, professional commercial photography, 1:1 format
```
**Variables**: product type, neutral surface (white paper, light wood, frosted glass)
**Negative**: dark tones, dramatic shadows, colored backgrounds

---

## Profile / Avatar (1:1)

### Creator Portrait (Abstract)
```
Abstract portrait concept, [representing theme] expressed as [visual metaphor],
circular composition, [brand color palette], premium editorial quality,
identity-forward without literal face, avatar-appropriate size readability
```
**Variables**: theme (creator, architect, builder), visual metaphor (constellation of
nodes, geometric facets, light burst), palette
**Negative**: actual photographic face, text, too complex for small display

---

## Prompt Intensifiers

Add to any prompt to raise quality:

| Intensifier | Effect |
|-------------|--------|
| `highly detailed, 8K quality` | Max resolution and detail |
| `cinematic composition` | Dramatic framing |
| `professional commercial photography` | Editorial polish |
| `award-winning photography` | Elevated standard signal |
| `sharp focus, no blur` | Forces crisp output |
| `studio lighting` | Clean professional light |
| `rule of thirds` | Strong composition |

## Universal Negative Prompts

Always consider adding:
```
no text, no watermarks, no signatures, no blurry elements, no distorted anatomy,
no low resolution, no artifacts, no pixelation, no oversaturation
```

For tech/AI imagery specifically:
```
no chrome robots, no generic brain imagery, no circuit board clichés,
no neon on black (unless intentional), no single-color saturation
```
