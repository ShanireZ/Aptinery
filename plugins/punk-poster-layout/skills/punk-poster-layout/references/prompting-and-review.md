# Composition prompts and review

## Six structural variables

Before style words, specify:

- Focus: where the viewer looks first.
- Hierarchy: the order of title, main visual, date, explanation and CTA.
- Grouping: which content belongs together.
- Balance: how horizontal and vertical visual weight stabilizes or deliberately shifts.
- Motion: whether the eye follows a line, diagonal, curve, ring or module.
- Space: negative space, density and edge safety zones.

Size, color, contrast, alignment and space affect reading order. Proximity,
similarity and continuity support grouping. Turn these variables into positions,
proportions and paths instead of supplying only a composition name.

## General structural prompt

For 01–16 or any poster led by focus and path:

```text
Create a [ratio] poster about [theme].
Use [composition]; place [main subject] at [position], occupying [proportion].
Move the eye from [entry] along [path] to [destination].
The title "[headline]" is primary; [subtitle / date / CTA] form levels two and three.
Use [negative-space strategy], [typographic tone], [color and material].
Preserve clear alignment and edge safe zones.
Avoid [multiple focal points / random text / excessive decoration / unsafe crop].
```

Start with one primary composition and one supporting relationship at most:

```text
Use Rule of Thirds as the primary structure and S-Curve as support.
Place the product at the upper-right thirds intersection, align the title to
 the left thirds line, and connect three supporting details along an implied S.
```

## Grids and composition

Composition sets focus and reading path. A grid provides alignment, proportion,
spacing and repetition. A poster can combine a visible split, full bleed,
overlaid type or collage with invisible columns, rows, modules, baselines and gutters.

Specify column and row counts, gutters, spans, shared edges and controlled breaks:
`six columns, 24px gutters, title spans four columns, image spans three, date spans one`.
These values are adjustable starting points.

### Image-model grid template

```text
Create a [aspect ratio] poster about [theme]. Use [one composition from 17–32].
Establish an invisible [columns] × [rows] modular grid with consistent gutters.
The headline "[title]" spans [columns × rows]; [main subject] spans [columns × rows].
Place date, explanation and CTA at [module locations], sharing [left edge / baseline / margin].
Move the eye from [entry] along [path] to [destination].
Allow [a few related, controlled breaks, usually one primary break or focal cluster];
keep other content strictly aligned. Use [colors] and [typographic tone], with [negative space].
Avoid random spans, competing focal points, unsafe crops, garbled text and visible construction lines everywhere.
```

Image models treat grids as soft constraints. They can suggest structure and
visual tendencies; do not claim browser-like pixel placement guarantees.

### HTML/CSS grid template

```text
Create a poster component with aspect-ratio:[ratio]. Use an outer CSS Grid:
grid-template-columns: repeat([columns], 1fr);
grid-template-rows: repeat([rows], 1fr);
gap: clamp([minimum gutter], [responsive value], [maximum gutter]);
Place headline at grid-area:[location] and main visual at grid-area:[location].
Metadata shares one left alignment line and spacing tokens.
Use object-fit:cover and object-position to lock the crop focus.
Only [specified primary break or related focal cluster] may cross or shift grid lines.
Provide a switchable grid debugging overlay.
Preserve composition relationships on mobile instead of automatically stacking every item in one column.
```

When exploring through image prompts and rebuilding in HTML, share the same
column counts, spans, focus, hierarchy, margins and reading path.

## Image-prompt completion criteria

Integrate structure into the complete prompt instead of appending keywords.
Include:

1. Aspect ratio and purpose.
2. Primary composition and supporting relationship.
3. Main visual position, proportion and crop.
4. Title, supporting copy, date, location and CTA hierarchy.
5. Entry, path and destination.
6. Alignment, space, color, type and material.
7. Safe zones and negative constraints.

Factual copy must come verbatim from the user or authoritative brief. Do not
invent titles, dates, locations, ticketing or brand marks. Condense long titles
only with permission; otherwise retain them and avoid competing first focal points.

When text must be exact, prefer a text-free or low-text generated background
with real text added using HTML/CSS or postproduction. If the user requests a
single generated image, state that model-rendered text is not guaranteed.
Compare the actual artifact with the intended copy character by character and
report discrepancies; correct prompt text does not establish correct image text.

## HTML/CSS completion criteria

- Express the main structure with Grid or Flexbox. Reserve absolute positioning
  for explicit layers, path nodes or controlled breaks.
- Store proportions, gutters, margins, type sizes, colors and hierarchy in CSS custom properties.
- Manage crop focus across sizes with `object-fit:cover` and `object-position`.
- Match semantic DOM order to reading order; visual reordering must not reverse accessibility order.
- Keep one accessible copy of each text. Type-over-image work needs explicit
  foreground-text, image and background-text layers; mark decorative duplicates `aria-hidden="true"`.
- Provide accurate `alt` for meaningful images and empty `alt` or `aria-hidden="true"` for decoration.
- Use links for navigation CTAs, buttons for interface actions, and visible `:focus-visible` states.
- Make debugging overlays switchable and off by default in the finished output.
- Preserve semantic relationships and hierarchy responsively, without requiring
  identical geometry. Retain column counts and side-by-side layouts only while
  minimum type size, unit width, safe crops and interaction targets remain usable;
  otherwise reflow with a stated reason.
- Test narrow viewports and 200% zoom, including text, focus order, CTAs, crops and content relationships.
- Preserve text contrast with local solid backgrounds, gradients or outlines in
  dense/full-bleed work; avoid uniformly darkening the entire image.

## Preflight: prompts and specifications

For recommendations, prompts and unrendered HTML/CSS specifications, perform
preflight/spec lint only. Check verbatim factual copy, compatible primary and
supporting structures, concrete positions/proportions/paths/safe zones, complete
negative constraints and values labeled as adjustable starting points.

Without an actual artifact, mark crop, responsiveness, contrast and readability
`not tested`. Static code inspection does not verify a browser viewport.

## Artifact review: requires an actual artifact

Review only an actual generated image, rendered page or screenshot with its target
aspect ratio, viewport or output size. If either is missing, stop review and request
it. Report observable or measured evidence and measurable corrections by default.
Only an explicit review-and-fix request permits changes to the identified artifact:
report the diagnosis first, apply the fix, and rerun relevant checks. Review alone
does not authorize modification.

Check in this order. Correct structural parameters before adding vague style words.

1. Entry: at mobile-feed size, can the viewer still find the title or main visual?
2. Three levels: do title, visual and supporting information differ clearly in scale or contrast?
3. Proportions: do `60/40`, `70/30` or column spans explain visual weight?
4. Shared edges: do title, image, date and explanation share one or two alignment lines?
5. Space and gutters: do peer gaps repeat and does space isolate or emphasize content?
6. Controlled breaks: is there usually one primary break or related focal cluster?
   If title and visual each break the grid, do both serve one hierarchy?
7. Image-text hierarchy: is type clearly in front, behind or interleaved with the subject?
8. Safe crop: are faces, hands, marks, key title strokes, dates and CTAs intact?
9. Effective path: do diagonals, curves, rings and splits lead toward useful information?
10. Responsive HTML: after resizing and 200% zoom, do semantics, hierarchy,
    readability and focus order remain usable? Identical geometry is not required.
11. Accessible HTML: does DOM order match reading order, with one accessible text
    copy, correct image alternatives, CTA semantics and visible focus?

## Reliable starting points

- Uncertain, moderate content: try 03 Rule of Thirds.
- Title, image, data and explanation together: try 21 Modular Grid with an
  adjustable 4×6 starting grid, about 80% aligned elements and one primary broken-grid title.
- Two-object comparison: try 16 Vertical Split at 60/40.
- Image plus explanation: try 17 Horizontal Split at 62/38.
- Quiet, premium, sparse content: try 05 Isolated Focal Point with 65%–80% active negative space.
- Experimental composition: establish a recognizable rule, then a few related,
  controlled breaks, usually one primary break or focal cluster.
