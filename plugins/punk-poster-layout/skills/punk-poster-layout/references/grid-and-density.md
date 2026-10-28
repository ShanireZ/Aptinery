# Compositions 17–32: regions, grids, image-text relationships and density

The colors, typefaces, materials, cinematic treatment and graphic/editorial style
words in these examples preserve source-article guidance. Carry them forward
only when the user or upstream workflow supplies the matching style. Otherwise
retain the structure and parameterize or omit style fields; do not independently
select external style atoms.

Ratios, grid counts, proportions, offsets, gutters and dimensions are adjustable
starting examples, not fixed requirements. Adapt to the supplied aspect ratio,
content quantity, minimum type size and unit width, crop safety and medium.
State the values actually used.

Use this catalog for multiple information types, precise grids, image/type priority, sequential panels and experimental structures. Image models treat grids as tendencies; HTML/CSS must encode columns, rows, spans, gutters, alignment lines and crop focus.

## 17 | Horizontal Split

Stack image/text or two scenes across a horizontal division to establish sequence and context.

- Reading path: Usually descend from the upper visual into lower explanation; text can also introduce an image.
- Suitable for: Film, travel, lectures, product explanations, data plus images.
- Pitfall: Keep the division away from faces and text midlines; use proportions to show hierarchy.
- Tags: horizontal split composition, stacked panels, image-text division, 62/38 layout

Image-model prompt:

```text
Portrait 3:4 poster split horizontally: the top 62% contains [subject/scene], the bottom 38% is a solid information area with "[title]", date and explanation. Relate the clear division to the horizon or a structural line. Avoid cutting a key subject at the boundary.
Keywords: horizontal split composition, stacked panels, image-text division, 62/38 layout.
```

HTML/CSS prompt:

```text
Use display:grid and grid-template-rows:62% 38%. Give the image region overflow:hidden and object-fit:cover; use an internal 2-column grid for information. The title may slightly cross the division with a contrast background.
```

## 18 | Horizontal Bands

Layer horizontal color or content bands to create beats, chapters and lateral speed.

- Reading path: Start at the strongest band and move through size, color or numbering.
- Suitable for: Music, transport, sports, timetables, event series, information-dense posters.
- Pitfall: Vary emphasis between bands and keep paragraph line lengths readable.
- Tags: horizontal band composition, striped layout, stacked information bars, rhythmic widths

Image-model prompt:

```text
Portrait poster made of 4–6 unequal horizontal content bands. Give "[title]" the largest, highest-contrast band; span [subject] across two adjacent bands; distribute date, location and numbering in narrower bands. Create rhythm and lateral speed; avoid equal-sized, equally strong bands.
Keywords: horizontal band composition, striped layout, stacked information bars, rhythmic widths.
```

HTML/CSS prompt:

```text
Use unequal grid-template-rows such as 10% 24% 12% 36% 18%. Give each band its own background and alignment; span the visual with grid-row. Adjust text line-height to band height with clamp().
```

## 19 | Single-Column Grid

Place all information in one continuous main column, using margins, paragraph spacing and type size to establish reading order.

- Reading path: Read linearly from column top to bottom, like a short text.
- Suitable for: Manifestos, literature, scholarship, talks, minimal product explanations.
- Pitfall: A poster is not a paper page: line length, paragraph count and type size must work at distance.
- Tags: single-column grid, manuscript grid, linear reading, generous margins

Image-model prompt:

```text
Portrait typographic poster with one narrow, clear main column. Put "[title]" in 2–4 lines at the top, then short body copy and date along the same left edge. Use generous margins, consistent baseline rhythm and a quiet, rational tone. Avoid long small-type paragraphs and overwide lines.
Keywords: single-column grid, manuscript grid, linear reading, generous margins.
```

HTML/CSS prompt:

```text
Inside the poster use max-inline-size:62%, margin-inline:auto, display:flex and flex-direction:column. Share one text left edge; limit body max-width:28ch and use a fixed line-height for baseline rhythm.
```

## 20 | Multi-Column Grid

Use multiple vertical columns and deliberate spans for complex image/text hierarchy.

- Reading path: Wide-spanning elements establish priority, then column lines organize details.
- Suitable for: Editorial posters, conferences, timetables, exhibition catalogs, data and explanations.
- Pitfall: Repeat column widths and gutters rather than assigning random spans to every item.
- Tags: multi-column grid, editorial layout, column span, consistent gutters

Image-model prompt:

```text
Portrait 3:4 editorial poster with 4 equal columns and clear gutters. "[title]" spans 3 columns, [subject] spans 2–4, and date/explanation each occupy 1. Establish hierarchy through spans, left alignment and rigorous rhythm. Avoid arbitrary spans.
Keywords: multi-column grid, editorial layout, column span, consistent gutters.
```

HTML/CSS prompt:

```text
Use display:grid; grid-template-columns:repeat(4,1fr); column-gap:clamp(8px,2vw,20px). Set title grid-column:1/4, visual optionally 2/5, and each metadata group to 1 column. Use grid line numbers consistently.
```

## 21 | Modular Grid

Cross columns and rows into reusable modules for systematic, high-density image, text and numbering.

- Reading path: Read large spanning elements first, then scan local groups of modules.
- Suitable for: Swiss design, information design, schedules, exhibitions, visual series.
- Pitfall: The grid expresses relationships; every line need not be drawn.
- Tags: modular grid, matrix layout, spanning modules, systematic hierarchy

Image-model prompt:

```text
Portrait information poster on a 4-column × 6-row modular grid. Let "[title]" span 3×2 modules and [subject] 2×3; put numbering and detail in smaller modules. Repeat margins and gutters for a systematic hierarchy, with local crossings where useful. Hide most construction lines.
Keywords: modular grid, matrix layout, spanning modules, systematic hierarchy.
```

HTML/CSS prompt:

```text
Use display:grid; grid-template-columns:repeat(4,1fr); grid-template-rows:repeat(6,1fr); gap:10px. Define every block with grid-area. Show the grid in debug mode; retain only a few separators in the finished output.
```

## 22 | Swiss Grid

Combine a strict grid, flush-left sans-serif type, asymmetric space and objective photography for clear internationalist communication.

- Reading path: Enter through a large sans-serif title, then follow left edges and module relationships.
- Suitable for: Design exhibitions, architecture, concerts, cultural institutions, rational technology brands.
- Pitfall: Red circles and Helvetica alone do not establish Swiss structure or hierarchy.
- Tags: Swiss grid, International Typographic Style, flush left ragged right, asymmetric grid

Image-model prompt:

```text
Portrait cultural poster on an asymmetric Swiss grid. Set "[title]" sans-serif, flush left and ragged right, aligned to 4–6 columns. Offset one high-contrast geometric form or objective visual; use restrained red/black/off-white and functional hierarchy. Avoid centered fullness and decoration as a substitute for structure.
Keywords: Swiss grid, International Typographic Style, flush left ragged right, asymmetric grid.
```

HTML/CSS prompt:

```text
Use a 6-column grid, all text text-align:left, title spanning 4 columns and metadata 2. Use one accent color and 1px rules; choose system sans-serif and limit font weights.
```

## 23 | Bento / Hierarchical Grid

Use different-sized rectangular cards with shared spacing and corner radii; card area expresses priority.

- Reading path: Read the largest card first, then jump through adjacent smaller cards.
- Suitable for: Technology, product features, data, service bundles, implemented HTML pages.
- Pitfall: Keep peer cards consistent in meaning and spacing rather than assembling arbitrary rectangles.
- Tags: bento grid, hierarchical cards, variable-span modules, dashboard composition

Image-model prompt:

```text
Portrait technology poster on a Bento hierarchy. Put "[title]" and [subject] in the largest card; place benefits, numbers, date and CTA in 3–5 smaller cards. Vary spans with consistent gutters for dashboard-like clarity. Avoid many equally weighted small cells.
Keywords: bento grid, hierarchical cards, variable-span modules, dashboard composition.
```

HTML/CSS prompt:

```text
Use display:grid; grid-template-columns:repeat(4,1fr); grid-auto-rows:1fr. Set the main card to grid-column:span 3 and grid-row:span 3; use span 1/2 for supporting cards. Share gap, border-radius and padding tokens.
```

## 24 | Checkerboard

Alternate images and text in a regular matrix, using reversals, repetition and correspondence for rhythm.

- Reading path: Jump between light/dark or image/text cells; perceive the whole before details.
- Suitable for: Product series, portfolios, event lineups, comparisons, fashion.
- Pitfall: Avoid excessively small cells; retain one deliberate focal exception.
- Tags: checkerboard composition, alternating tiles, image-text rhythm, one deliberate break

Image-model prompt:

```text
Portrait poster on a 3×4 checkerboard of images, color blocks and text. Let "[title]" occupy or break 2–3 adjacent cells; keep repeated light/dark reversal elsewhere. Ordered with one clear focal break. Avoid equally complex cells everywhere.
Keywords: checkerboard composition, alternating tiles, image-text rhythm, one deliberate break.
```

HTML/CSS prompt:

```text
Use a 3-column × 4-row grid; reverse foreground/background with :nth-child(even) and set title grid-column:span 2. Retain 3 columns on small screens only while minimum unit width, type size and readable line length hold. Otherwise reduce columns or reflow, preserving alternation, correspondences, semantic DOM order and primary focus.
```

## 25 | Full-Bleed Hero

Fill the canvas with one image, overlaying text or placing it in a local safe zone for atmosphere and immersion.

- Reading path: Sense the whole image first, then enter details through a high-contrast title.
- Suitable for: Film, travel, fashion, photography, product atmosphere, people.
- Pitfall: Keep type off complex textures and manage crop focus across sizes.
- Tags: full-bleed hero image, immersive poster, type overlay, controlled crop

Image-model prompt:

```text
Portrait 3:4 poster with one rich [scene/subject] image extending to all four edges. Put "[title]" in a low-texture, high-contrast safe zone and keep supporting copy in one compact cluster. Cinematic and immersive with intentional crop. Avoid text over faces or clutter.
Keywords: full-bleed hero image, immersive poster, type overlay, controlled crop.
```

HTML/CSS prompt:

```text
Position img absolutely at inset:0; width:100%; height:100%; object-fit:cover. Set focal point with object-position. Add a local gradient mask rather than darkening the entire image; limit text width in the safe zone.
```

## 26 | Typographic Dominant

Treat the headline as the main visual through scale, weight, tracking, line breaks and cropping.

- Reading path: Recognize huge keywords first, then find details in letterform gaps or edges.
- Suitable for: Opinions, manifestos, music, promotions, social causes, work without images.
- Pitfall: Oversized does not mean everything bold; preserve meaning and recognition through line breaks.
- Tags: big type poster, typographic dominant composition, oversized headline, cropped letterforms

Image-model prompt:

```text
Portrait type-only poster where "[title]" is the sole main visual. Use oversized sans-serif or display type occupying 60%–85%, with intentional letterform cropping beyond edges. Fit subtitle/date into negative spaces in very small type. High contrast and rhythm. Avoid random word breaks and too many typefaces.
Keywords: big type poster, typographic dominant composition, oversized headline, cropped letterforms.
```

HTML/CSS prompt:

```text
Use font-size:clamp(72px,24vw,260px), line-height:.78 and letter-spacing:-.07em. Set container overflow:hidden. Control breaks with max-inline-size and deliberate <br>; position metadata in negative space.
```

## 27 | Type over Image

Share image and typography in one space, using occlusion, interleaving and contrast to form an integrated visual.

- Reading path: Image and title enter together; foreground/background hierarchy explains their relationship.
- Suitable for: Fashion, portraits, magazines, film, music, cultural events.
- Pitfall: Make type clearly in front, behind or interleaved; blanket translucency often muddies hierarchy.
- Tags: type over image, interleaved typography, foreground-background layering, editorial poster

Image-model prompt:

```text
Portrait poster with [person/subject] centered and oversized "[title]" crossing the image. Put some letterforms in front and let the subject hide others for explicit image-text depth. Keep text legible and edges clean. Avoid whole translucent text lines and covering faces or key information.
Keywords: type over image, interleaved typography, foreground-background layering, editorial poster.
```

HTML/CSS prompt:

```text
Create background-text, image and foreground-text z-index layers. Use two visual title copies but only one accessible copy; mark decorative duplicates aria-hidden="true". Use a transparent PNG or clip-path for the subject rather than relying only on opacity.
```

## 28 | Diptych / Triptych

Divide one theme into two or three continuous panels, expressing time, comparison or perspectives through repetition and variation.

- Reading path: Move horizontally or vertically between panels and compare changes within shared structure.
- Suitable for: Narratives, before/after, product series, ensembles, film, photo exhibitions.
- Pitfall: Each panel needs a common variable; unrelated adjacent images do not form a triptych.
- Tags: triptych composition, sequential panels, repeated framing, variation within a system

Image-model prompt:

```text
Portrait poster divided into three narrow sequential panels showing three moments/views/states of [one theme]. Share crop, tone and horizon rules. Let "[title]" span all panels or occupy a shared bottom band. Repeat with variation; avoid merely joining unrelated images.
Keywords: triptych composition, sequential panels, repeated framing, variation within a system.
```

HTML/CSS prompt:

```text
Use grid-template-columns:repeat(3,1fr) and a shared gap. Give panel images the same aspect-ratio and object-position rules. The title may use grid-column:1/-1; mark states with data-state.
```

## 29 | Overlapping Collage

Overlap and rotate images, paper, texture and type for handmade, remembered or subcultural expression.

- Reading path: Enter through the highest-contrast layer and jump across occlusion edges, guided by hierarchy rather than a grid.
- Suitable for: Music, youth culture, magazines, art, retro work, handmade brands.
- Pitfall: Random rotation is not collage; unify material, palette or narrative cues.
- Tags: overlapping collage, torn paper layers, controlled rotation, layered ephemera

Image-model prompt:

```text
Portrait collage with 4–7 layers of photos, torn paper, color blocks, stamps and "[title]" overlapping. Restrict rotation to a few directions. Keep one main image largest and other layers subordinate, with unified paper grain and limited colors. Avoid equally dominant layers or unrelated material piles.
Keywords: overlapping collage, torn paper layers, controlled rotation, layered ephemera.
```

HTML/CSS prompt:

```text
Use a position:relative container; absolute layers with transform:translate/rotate. Restrict rotation to -8deg/0deg/6deg. Use box-shadow and mix-blend-mode cautiously for paper effects and define z-index tokens.
```

## 30 | Broken Grid

Establish a perceptible grid, then let a few key elements cross, shift or overflow it for emphasis. Usually one primary break or focal cluster suffices; the source example allows title and visual as two related breaks serving one hierarchy.

- Reading path: The grid establishes expectation; the break attracts attention by departing from it.
- Suitable for: Avant-garde culture, design exhibitions, technology, experimental editing, portfolios.
- Pitfall: A break needs an underlying grid; shifting every element creates disorder.
- Tags: broken grid, intentional misalignment, controlled disruption, visible underlying structure

Image-model prompt:

```text
Experimental portrait poster with a clear 5-column grid and repeated alignment lines. Let "[title]" cross two column lines and [subject] cross one module boundary, forming a related focal cluster. Keep other information aligned; create focus with a few controlled offsets. Avoid randomly floating everything.
Keywords: broken grid, intentional misalignment, controlled disruption, visible underlying structure.
```

HTML/CSS prompt:

```text
Use an underlying 5-column Grid. Keep about 80% of elements on grid lines. Let the primary break or related focal cluster span columns and translateX(8%–15%). Avoid absolute positioning for everything; show a grid overlay when debugging.
```

## 31 | Repetition & Pattern

Repeat a shape, image or word to establish rhythm, then make one difference the focus.

- Reading path: Perceive the pattern, then immediately detect the exception.
- Suitable for: Product series, groups, music, sports, data, conceptual communication.
- Pitfall: Many unchanged repeats become background noise; the difference must serve the theme.
- Tags: repetition and pattern, rhythmic grid, one anomaly, pattern interruption

Image-model prompt:

```text
Portrait poster repeating [shape/subject/word] 12–30 times in a regular array with shared size and spacing. Change one item’s color, direction or size and relate it to "[title]" for a strong rhythm and clear focus. Avoid multiple simultaneous exceptions.
Keywords: repetition and pattern, rhythmic grid, one anomaly, pattern interruption.
```

HTML/CSS prompt:

```text
Use CSS Grid with repeat(auto-fit,minmax()) for the array. Inherit shared cell styles and change one variable only through .is-anomaly. Give the title and anomalous cell the same accent color.
```

## 32 | Dense All-Over

Cover the canvas densely, using overall texture, local contrast and multiple scales for maximalist impact.

- Reading path: Sense overall density first, then find a local entry through the largest scale or strongest color contrast.
- Suitable for: Festivals, underground music, trends, retro advertising, large event lineups.
- Pitfall: Density still needs hierarchy and a clear entry for title, date and CTA.
- Tags: dense all-over composition, maximalist poster, multi-scale hierarchy, controlled visual density

Image-model prompt:

```text
Portrait maximalist poster densely covered with graphics, texture, short words and information. Preserve clear scale hierarchy: oversized "[title]" is the entry, medium [subject] is secondary, and small type/patterns form the base texture. Unify complexity with a limited palette. Avoid equal-sized elements and unreadable key dates.
Keywords: dense all-over composition, maximalist poster, multi-scale hierarchy, controlled visual density.
```

HTML/CSS prompt:

```text
Combine CSS Grid and absolute layers: background pattern, information matrix and oversized title. Limit to 3 type scales and no more than 4 colors. Use solid backgrounds or outlines for key text to meet WCAG contrast.
```
