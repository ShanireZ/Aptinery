# Compositions 01–16: focus, balance, geometry and motion

The colors, typefaces, materials, cinematic treatment and graphic/editorial style
words in these examples preserve source-article guidance. Carry them forward
only when the user or upstream workflow supplies the matching style. Otherwise
retain the structure and parameterize or omit style fields; do not independently
select external style atoms.

Ratios, grid counts, proportions, offsets, gutters and dimensions are adjustable
starting examples, not fixed requirements. Adapt to the supplied aspect ratio,
content quantity, minimum type size and unit width, crop safety and medium.
State the values actually used.

Use this catalog for one protagonist, strong symbolic structures, clear reading paths and two-region splits. Replace bracketed fields and integrate the chosen structure into the complete task prompt.

## 01 | Axial Symmetry

Arrange major elements around one central axis, with similar visual weight on both sides for solemnity, stability and ceremony.

- Reading path: Top title → central visual → bottom information, down the axis.
- Suitable for: Brand launches, exhibitions, luxury, ceremonies, one protagonist.
- Pitfall: Avoid mechanically mirroring every detail; dense information can become rigid.
- Tags: axial symmetry, centered composition, mirrored balance, central focal point

Image-model prompt:

```text
Portrait 3:4 poster about [theme]. Center the headline "[title]" at the top and [subject] on the vertical axis. Layer subtitle, date and credit along the same centerline. Balance margins and negative space with near-mirrored visual weight, strong contrast and three clear levels; flat graphic design. Avoid competing focal points, random offsets and meaningless decoration.
Keywords: axial symmetry, centered composition, mirrored balance, central focal point.
```

HTML/CSS prompt:

```text
Use an aspect-ratio:3/4 container; display:grid with one column and three rows, place-items:center. Draw a hideable axis with ::before. Center title, visual and metadata within inline-size limits; use equal horizontal padding.
```

## 02 | Asymmetrical Balance

Exchange visual weight through size, brightness, density and distance, balancing different shapes with deliberate tension.

- Reading path: Enter through the large form; a smaller high-contrast block on the opposite side supplies counterweight.
- Suitable for: Cultural posters, design exhibitions, fashion, technology, contemporary brands.
- Pitfall: An offset alone is not balance; the other side needs sufficient contrast or density.
- Tags: asymmetrical balance, visual counterweight, offset focal point, dynamic equilibrium

Image-model prompt:

```text
Portrait poster about [theme], using asymmetrical balance. Offset a large [subject] to one side; balance it with a smaller, higher-contrast title "[title]" and information group opposite. Use clear alignment lines and unequal negative space with stable visual weight, in a modern editorial treatment. Avoid scattered placement and equally dominant sides.
Keywords: asymmetrical balance, visual counterweight, offset focal point, dynamic equilibrium.
```

HTML/CSS prompt:

```text
Use an invisible 5×6 CSS Grid. Span the visual across 3 columns and 4 rows; place text in 2 columns on the diagonal opposite. Control scale with clamp(), offset with align-self:end and justify-self:start, and retain one shared alignment line.
```

## 03 | Rule of Thirds

Divide the canvas into thirds horizontally and vertically; place the focus near a line or intersection for stable, natural offset.

- Reading path: Reach the visual at a thirds intersection, then follow division lines into title and information.
- Suitable for: Photography-led posters, people, products, events, web heroes.
- Pitfall: Preserve subject direction, text space and safe crops over exact intersection placement.
- Tags: rule of thirds, thirds intersection, off-center focal point, directional negative space

Image-model prompt:

```text
Portrait 3:4 poster using Rule of Thirds. Place the visual center of [subject] near the upper-right thirds intersection, align "[title]" along the left thirds line, and preserve broad space in the subject’s viewing direction. Use clear hierarchy and intentional cropping. Avoid crowding every item into intersections or unbalanced margins.
Keywords: rule of thirds, thirds intersection, off-center focal point, directional negative space.
```

HTML/CSS prompt:

```text
Use a 3-column × 3-row CSS Grid. Position the visual with grid-column:2/4 and grid-row:1/3; align the title along the first vertical division. Show thirds with repeating-linear-gradient during debugging and turn it off when finished.
```

## 04 | Golden Spiral

Use progressively smaller rectangles and arcs to organize focus and rhythm. Treat it as a proportional sketch, not a compulsory aesthetic law.

- Reading path: From the broad outer area, tighten along an arc toward the inner focus.
- Suitable for: Art, nature, film, narrative products, conceptual posters.
- Pitfall: Keep spiral guides out of finished artwork; content hierarchy takes priority.
- Tags: golden spiral composition, Fibonacci proportion, progressive scale, converging focal point

Image-model prompt:

```text
Portrait concept poster about [theme], arranged around an implied golden spiral. A large visual enters from outside; "[title]" and supporting elements decrease in scale along an arc toward [key subject] at the inner focus. Move from broad to tight spacing. Hide mathematical guides and preserve readability.
Keywords: golden spiral composition, Fibonacci proportion, progressive scale, converging focal point.
```

HTML/CSS prompt:

```text
Use nested absolute-positioned rectangles at approximately 61.8% of the preceding size. Suggest arcs through border-radius and pseudo-elements, with content anchors near the smallest rectangle. Store the ratio in CSS custom properties rather than hard-coding decorative lines.
```

## 05 | Isolated Focal Point

Use extensive active negative space to isolate one small, distinct focus; sparseness sets the tone.

- Reading path: Isolation draws the eye to one point, then nearby minimal text.
- Suitable for: Premium brands, art exhibitions, poetry, fragrance, quiet product communication.
- Pitfall: Space is more than shrinking content; the focus needs contrast, texture or meaning.
- Tags: macro white space, isolated focal point, low-density layout, restrained typography

Image-model prompt:

```text
Minimal portrait poster about [theme]. Preserve 65%–80% active negative space. Place one small, recognizable [subject] low or off-center, with "[title]" nearby and little metadata in restrained type. Quiet, premium and precise. Avoid filling space or adding multiple decorative points.
Keywords: macro white space, isolated focal point, low-density layout, restrained typography.
```

HTML/CSS prompt:

```text
Use one position:relative container. Set visual inline-size:18%–28%, positioned at 60%–75% of the height. Group text and visual into one small cluster, leave the rest open, and use generous padding and max-width.
```

## 06 | Edge-Anchored

Push the subject toward an edge and crop deliberately; off-canvas continuation creates scale and tension.

- Reading path: Enter through the large cropped form and follow its orientation or edge toward text.
- Suitable for: Fashion, portraits, product close-ups, social covers, forceful communication.
- Pitfall: Protect faces, joints, text and key product structure with safe zones.
- Tags: edge-anchored composition, intentional crop, off-canvas continuation, edge tension

Image-model prompt:

```text
Portrait 3:4 poster. Anchor [subject] to the right edge with an intentional crop beyond the canvas, occupying about 55%–70%. Place "[title]" in a narrow information band at the opposite edge with clear safe space. Create scale and off-canvas continuation; avoid unsafe cuts or crowding all four edges.
Keywords: edge-anchored composition, intentional crop, off-canvas continuation, edge tension.
```

HTML/CSS prompt:

```text
Use overflow:hidden. Position the visual absolutely with inline-size:70% and inset-inline-end:-16%. Keep text in the opposite safe zone. Control responsive crop focus with object-position.
```

## 07 | Triangular Hierarchy

Arrange elements as a stable triangle: the apex emphasizes and the base supports a natural three-level hierarchy.

- Reading path: Apex focus → descend along the sides → base information, or converge from base to apex.
- Suitable for: Ensembles, film, forums, authoritative themes, clearly layered launches.
- Pitfall: A stronger focus outside the triangle collapses the structure.
- Tags: triangular composition, pyramid hierarchy, stable base, apex focal point

Image-model prompt:

```text
Portrait poster about [theme], arranging [visual or group] as a stable triangle/pyramid. Put the key subject or "[title]" at the apex, spread supporting elements downward at both sides, and place date and location along the base. Decrease scale through three levels, with a low center of gravity and solemn tone. Avoid a stronger focus outside the triangle.
Keywords: triangular composition, pyramid hierarchy, stable base, apex focal point.
```

HTML/CSS prompt:

```text
Use a 3-column × 4-row CSS Grid. Put the key element in the middle column, rows 1–2; supporting elements at both sides in row 3; metadata across the bottom. A hideable guide triangle can use clip-path:polygon().
```

## 08 | Inverted Triangle

Suspend weight in a broad top narrowing downward, creating instability, pressure, speed or danger.

- Reading path: Funnel a broad upper area toward a lower point and conclusion.
- Suitable for: Avant-garde art, music, suspense, warnings, countercultural events.
- Pitfall: Avoid reliable, comfortable themes, and protect bottom text from the apex.
- Tags: inverted triangle composition, top-heavy balance, downward convergence, suspended tension

Image-model prompt:

```text
Experimental portrait poster using an inverted triangle. Place a broad "[title]" and graphics in the upper half, progressively narrow downward, and aim the final point at [date/CTA]. Use a high center of gravity, pressure, tension and falling motion. Avoid cramped bottom information and a calm, reassuring brand tone.
Keywords: inverted triangle composition, top-heavy balance, downward convergence, suspended tension.
```

HTML/CSS prompt:

```text
Make upper content 100% wide, middle 66%, and bottom focus 20%. Narrow stages with grid-template-rows and justify-self:center. Use clip-path:polygon(0 0,100% 0,50% 100%) for the background form.
```

## 09 | Concentric

Repeat rings, frames or shapes around a common center to emphasize focus, echoes and inward depth.

- Reading path: Outer rings establish the field, then converge layer by layer toward the center.
- Suitable for: Music, technology, sound waves, communities, anniversaries, abstract themes.
- Pitfall: Keep center text away from rings; too many rings cause noise or dizziness.
- Tags: concentric composition, nested rings, central convergence, rhythmic intervals

Image-model prompt:

```text
Portrait poster with 4–7 concentric circles or frames around central [visual], varying size and line weight rhythmically. Place "[title]" at the center or intersecting one ring; distribute supporting information along the outer ring. Suggest focus, sound waves and echoes. Avoid ring lines over text or identical line weights.
Keywords: concentric composition, nested rings, central convergence, rhythmic intervals.
```

HTML/CSS prompt:

```text
Use place-items:center with multiple absolute-positioned elements, geometrically increasing inset, and border-radius:50% or rectangular frames. Control ring size, weight and opacity with CSS variables; give text the highest z-index.
```

## 10 | Frame within Frame

Use borders, windows or nested containers to repeatedly define the viewing area, creating exhibition character and depth.

- Reading path: Read the outer frame, pass through inner frames to the subject, then read outside annotations.
- Suitable for: Art exhibitions, architecture, archives, photography, retro print, art-book covers.
- Pitfall: Frame hierarchy must not compete with type; an undersized inner frame looks like a thumbnail.
- Tags: frame within frame, nested borders, contained focal area, gallery layout

Image-model prompt:

```text
Portrait cultural poster with nested frames. A thin outer frame defines the safe zone, an offset middle window crops [subject], and a small inner frame anchors "[title]". Keep numbering and notes outside the frame for an archive/exhibition effect. Vary border weights and avoid squeezing body copy.
Keywords: frame within frame, nested borders, contained focal area, gallery layout.
```

HTML/CSS prompt:

```text
Use three nested containers with separate padding and border. Offset the middle by 4%–8%; use object-fit:cover for the visual. Prefer outline-offset over stacked box-shadow for clear boundaries.
```

## 11 | Diagonal Tension

A strong diagonal axis breaks horizontal stability and establishes speed, conflict and direction.

- Reading path: Cross from one corner toward its opposite; information follows or cuts against the axis.
- Suitable for: Sports, music, promotions, technology, calls to action, youth culture.
- Pitfall: Keep body text readable; aim the diagonal at useful information rather than outside the canvas.
- Tags: diagonal composition, dynamic axis, directional tension, kinetic layout

Image-model prompt:

```text
Portrait poster organized along a strong lower-left to upper-right diagonal. Place [subject] on the axis; align "[title]" with it or cut across it in the opposite direction. Keep secondary information horizontal. Create speed and tension without rotating every text block or drawing attention away from key information.
Keywords: diagonal composition, dynamic axis, directional tension, kinetic layout.
```

HTML/CSS prompt:

```text
Create a broad ::before band with position:absolute and transform:rotate(-24deg) scale(1.4). Anchor key elements at points along the diagonal; keep body text transform:none.
```

## 12 | Radial Burst

Radiate lines, shapes or people outward from one shared center for concentrated energy.

- Reading path: Lock onto the center, expand outward, then return to central text.
- Suitable for: Festivals, promotions, celebrations, sports, manifestos, emotional events.
- Pitfall: Use one center only; dense rays interfere with small type.
- Tags: radial burst composition, radiating lines, explosive focal point, centrifugal energy

Image-model prompt:

```text
Portrait 3:4 poster with [visual/title] as the sole radiation center. Alternate thick and thin rays, text or shapes toward the edges. Keep "[title]" compact and high-contrast in the center; weaken edge details. Energetic, festive or declarative. Avoid multiple radiation centers and rays crossing small text.
Keywords: radial burst composition, radiating lines, explosive focal point, centrifugal energy.
```

HTML/CSS prompt:

```text
Generate rays with repeating-conic-gradient(). Center content with place-items:center; lower the ray layer’s opacity below text and give center text a solid background or isolation:isolate.
```

## 13 | Z-Path

Arrange upper-left, upper-right, lower-left and lower-right anchors into a zigzag for sequential reading of limited information.

- Reading path: Upper-left title → upper-right visual → lower-left explanation → lower-right CTA.
- Suitable for: Events, product heroes, courses, launches, social ads.
- Pitfall: The Z is layout scaffolding, not a universal eye-movement law.
- Tags: Z-pattern composition, corner anchors, sequential visual path, diagonal handoff

Image-model prompt:

```text
Portrait information poster with a clear Z reading path: "[title]" at upper left, [subject] at upper right, short explanation at lower left, date/CTA at lower right. Suggest two horizontal strokes and a diagonal handoff with contrast, fine lines or subject direction; do not draw a literal Z. Avoid equal emphasis at every corner.
Keywords: Z-pattern composition, corner anchors, sequential visual path, diagonal handoff.
```

HTML/CSS prompt:

```text
Use a 2-column × 2-row grid with one cluster at each corner. Suggest a low-contrast path with pseudo-elements or element orientation. Give the lower-right CTA the strongest color contrast without exceeding headline scale.
```

## 14 | S-Curve

Connect focal nodes through a soft reversing curve for flow, elegance and gradual narrative.

- Reading path: Enter on one upper side, cross the center, finish on the opposite lower side.
- Suitable for: Beauty, fashion, dance, nature, drinks, elegant narratives.
- Pitfall: Each turn needs an information node; avoid an unrelated decorative curve.
- Tags: S-curve composition, serpentine flow, graceful movement, sequential nodes

Image-model prompt:

```text
Portrait poster placing [visual] and 3 information nodes around an implied S-curve. Put "[title]" at the upper entry, cross the canvas center in the middle, and end at date/CTA on the opposite lower side. Alternate open and tight space for flowing continuity. Avoid decorative curves without nodes.
Keywords: S-curve composition, serpentine flow, graceful movement, sequential nodes.
```

HTML/CSS prompt:

```text
Use an SVG path or two large arc pseudo-elements. Attach three nodes with absolute positioning and percentage coordinates; keep body text horizontal. On narrow screens or at 200% zoom, scale the whole only if type size, safe crops and interaction targets remain usable. Otherwise reflow nodes in semantic DOM order, preserving entry, turn, destination and adjacency without requiring identical geometry.
```

## 15 | L-Shaped Anchor

Intersect a vertical and horizontal information band at a corner, supporting the main visual like a bracket.

- Reading path: Descend along the vertical rail, turn along the horizontal rail, then enter the enclosed visual.
- Suitable for: Architecture, exhibitions, catalogs, rational brands, space and industry.
- Pitfall: Give the arms different lengths; closing all four sides becomes Frame within Frame.
- Tags: L-shaped composition, corner anchor, edge rails, open field

Image-model prompt:

```text
Portrait poster with an L-shaped structure: a left information rail meets a bottom headline band at the lower-left corner. Place [subject] in the open upper-right field and "[title]" along the bottom. Rational, architectural, with clear edge alignment. Keep the other sides open.
Keywords: L-shaped composition, corner anchor, edge rails, open field.
```

HTML/CSS prompt:

```text
Use grid-template-columns:18% 1fr and grid-template-rows:1fr 18%. Place the vertical rail in column 1, bottom rail across both columns, and visual upper right. Vertical type may use writing-mode:vertical-rl.
```

## 16 | Vertical Split

Divide the canvas vertically into equal or hierarchical regions for comparison, questions/answers, before/after or two themes.

- Reading path: Read the stronger side first, then cross the seam to its counterpart.
- Suitable for: Product comparisons, pairs, before/after changes, competing views, collaborations.
- Pitfall: Relate both sides explicitly; 50/50 can erase hierarchy.
- Tags: vertical split composition, dual-panel layout, juxtaposition, 60/40 balance

Image-model prompt:

```text
Portrait poster split vertically, showing [subject A] left and [subject B] right with contrasting color/material. Let "[title]" cross the seam or split across both sides. Use a 60/40 hierarchy and a clear juxtaposition. Avoid unrelated halves or equal emphasis without a focus.
Keywords: vertical split composition, dual-panel layout, juxtaposition, 60/40 balance.
```

HTML/CSS prompt:

```text
Use a 5-column CSS Grid: 3 columns left, 2 right. Give each side its own background and content wrapper. A seam-crossing title uses grid-column:2/5 and z-index:2. Keep side-by-side on narrow screens only while minimum unit width, type size and safe crops hold; otherwise stack or sequence regions while retaining A/B semantic order, comparison and 60/40 hierarchy.
```
