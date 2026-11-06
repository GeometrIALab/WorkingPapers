# Templates

Reusable material for preparing and circulating GeometrIA Lab working papers.

| File | Purpose |
|---|---|
| [expert-collaboration-invitation.md](expert-collaboration-invitation.md) | Email template for inviting an expert to inspect and develop a working paper as a coauthor (step 2 of the [standard procedure](../README.md#standard-procedure-authorship-and-human-certification)). Replace each bracketed field before sending. |
| [stamp_wm.py](stamp_wm.py) | Adds the diagonal "WORKING PAPER" watermark to every page of a PDF, for papers compiled without it. |

## Watermarking a PDF

`stamp_wm.py` draws the same watermark as the LaTeX `draftwatermark` package used in our working papers: Latin Modern letters in light gray at 45 degrees, centred on each page and placed underneath the text. The letter shapes are stored in the script itself, so it needs no fonts or other files, and it works for any page size or orientation.

```bash
pip install pypdf
python3 templates/stamp_wm.py paper.pdf            # writes paper_WP.pdf
python3 templates/stamp_wm.py paper.pdf out.pdf
```

The original PDF is left unchanged. The colour, size and angle can be adjusted with the `GRAY`, `SIZE` and `ANGLE` settings at the top of the script; the text itself is fixed.
