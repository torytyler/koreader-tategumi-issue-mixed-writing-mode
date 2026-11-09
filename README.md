# Reproducer assets: mixed-writing-mode page overlap (koreader-tategumi)

Attachments for m-tky/koreader-tategumi issue "Vertical body is laid out on the
preceding horizontal title page, and full-page illustrations are painted over
the text page".

- `fixtures/` - minimal, copyright-free EPUBs that reproduce the page merge.
  * `fixture_a_...epub`: horizontal title page followed by a vertical body whose
    first element is the publisher's `keep-space` spacer image.
    Stock engine: the body's first columns land on the title page (page 1).
    Patched engine: the body starts on page 2.
  * `fixture_b_...epub`: vertical text page followed by a horizontal
    full-page illustration page (expected-behaviour guard).
- `patches/` - `fix.patch` applies to m-tky/crengine @ 7b0f2a4;
  `koreader-side.patch` applies to m-tky/koreader-tategumi @ ec1c43d
  (regression spec + divergence-ledger note).
- `screenshots/` - before/after renders at 600x800, plus the original
  macOS screenshots of the report.

No book content is redistributed here beyond the single pages visible in the
screenshots.
