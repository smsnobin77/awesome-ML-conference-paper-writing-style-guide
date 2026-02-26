# Awesome ML Conference Paper Writing Style Guide

A curated guide to ML paper writing style guide — structure, style, examples, checklists, and templates for NeurIPS / ICML / ICLR / ACL / AAAI / CVPR (and beyond).

## Table of contents
- [Structural and Formatting Rules](#Structural-and-Formatting-Rules)
- [Citations and References](#Citations-and-References)
- [Figures and Tables](#Figures-and-Tables)
- [LaTeX and Formatting Requirements](#LaTeX-and-Formatting-Requirements)
- [Limitations and Ethics Statements](#Limitations-and-Ethics-Statements)
- [Conference Templates](#Conference-Templates)

## Structural and Formatting Rules

1. **Heading capitalization**
   - **NeurIPS**: All headings should be **lower case** (a.k.a. sentence case, down style) — except for the first word and proper nouns — flush left, and bold. *Example:* Methodology and results
   - **ACL**: All headings should be in **title case** (a.k.a. up style, headline style), flush left, and bold. *Example:* Methodology and Results
   - **ICML**: Section and Subsection (**title case**, bold, numbered, flush left): *Example:* Methodology and Results; Subsubsection (**small caps**, content words capitalized, numbered, flush left): <span style="font-variant: small-caps;">Methodology and Results</span> 
   - **CVPR**: Same as NeurIPS — headings use **sentence case** (down style), flush left, and bold. *Example:* Methodology and results
   - **ICLR**: First-level headings are written in **small caps**, flush left. *Example:* <span style="font-variant: small-caps;">Methodology and Results</span>
   - **AAAI**: Same as ACL — headings use **title case** (headline style), flush left, and bold. *Example:* Methodology and Results
  
2. **Page limit**
   - **NeurIPS**: 9 pages of main text for submission (figures/tables included in those 9); references don’t count. If accepted, you get +1 page (10 pages) for camera-ready. Appendix allowed and unlimited.
   - **CVPR**: 8 pages total for main text (including figures/tables) in the CVPR style; additional pages for references only are allowed. Appendix allowed and unlimited (Same as NeurIPS).
   - **ICML**: 8 pages for the main body (submission), excluding references and appendices; appendices and references are unlimited in pages but the entire PDF ≤ 10 MB. For the final version you may add +1 page (i.e., 9 pages of main body).
   - **ACL**: Long papers: up to 8 pages of content for review, plus unlimited references; final versions get +1 page (up to 9). Short papers: 4 pages for review; final gets +1 (to 5). Appendix allowed and unlimited (Same as NeurIPS).
   - **ICLR**: Submission: main text ≤ 9 pages. During discussion & camera-ready: main text limit increases to 10 pages. References do not count; over-limit is desk-rejected. Appendix allowed and unlimited (Same as NeurIPS).
   - **AAAI**: Up to 7 pages of technical content, plus additional pages solely for references (submission). Proceedings allocation remains 7 content pages (+refs). AAAI allows a technical appendix during review, but for camera-ready the supplementary is not included in AAAI’s proceedings. 

## Citations and References

**Where to put citations:**
   - If you name the authors … “Smith et al. (2024) …”
   - If multiple works support the sentence … “(Doe, 2021; …)”
   - If different clauses are supported by different papers … split the sentence.
   - **Tips**
     - Be **consistent** (style, ordering, and format) within the paper.
     - **Cite close to the claim**: place the citation right where the reader needs it—after the author name (textual) or after the claim (parenthetical). If a sentence mixes multiple claims/sources, split it.
    
## Figures and Tables

**Caption conventions:**
   - **ACL/AAAI:** captions **below** both figures and tables.
   - **NeurIPS/ICML/ICLR/CVPR/WACV:** figures → **below**; tables → **above**.
   - **Tips**
        - When in doubt, follow the **current year’s** official template/author kit for that venue. Some details can change year to year.

## LaTeX and Formatting Requirements
- **NeurIPS**:
	- Citations: natbib is loaded by default; you can opt-out with \usepackage[nonatbib]{neurips_2024} (the nonatbib option). 
	- Tables: strongly recommend booktabs. 
	- Math fonts: don’t use \bbold; use AMS fonts (amsfonts / amssymb). 
	- Figures: use graphicx and specify widths as a fraction of \linewidth. 
- **ACL**:
	- Base fonts: \usepackage{times}; txfonts/newtx acceptable alternatives. 
	- Figures: use graphicx. 
	- Citations: style is based on natbib (supports \citet, \citep, etc.). 
	- Hyperlinks: DOIs/URLs appear as hyperlinks (uses hyperref). 
	- BST: ships an ACL bibliography style (acl_natbib.bst). 
- **CVPR**:
	- Cross-refs: template tells you to use \cref{...} (from cleveref) for figures/tables/equations/sections. 
	- Figures: show \usepackage{graphicx} and \includegraphics[width=...]{...} usage. 
	- Notes: The author kit does not publish a ban list like AAAI; it focuses on style compliance (two-column, numbered refs, etc.). References are numeric and listed in 9-pt Times. 
- **ICLR**:
	- Citations: use natbib for in-text citations. 
	- Figures: use graphicx with width set as a multiple of \linewidth. 
	- Style/BST files: the kit provides iclr2025_conference.sty and iclr2025_conference.bst. 
- **AAAI**:
	- Required packages: aaai, times, helvet, courier in the preamble. 
	- What’s not allowed / restricted:
		- No embedded links or bookmarks → effectively no hyperref in the proceedings PDFs. 
		- titlesec is not allowed; spacing hacks and page-layout changes (e.g., \parindent, \parskip, etc.) are flagged. 
		- Do not use [T1]fontenc (they suggest CM-Super if you need Type-1 CM). 
		- Must compile with pdfLaTeX; no .ps/.eps figures (use .pdf/.png/.jpg). 
		- Single .tex source file (excluding .bib); \input not allowed. 
	- Fonts: Times/Nimbus for text (no Computer Modern for body text). 
	- BST: use aaai.bst.

## Limitations and Ethics Statements

   - **ACL:** Limitations **required** (before references, not counted); Ethics **optional** (before references, not counted).  
   - **ICLR:** Limitations **not required**; Ethics statement **optional/encouraged** (before references, not counted).  
   - **NeurIPS:** Limitations **optional/encouraged**; no dedicated ethics section — **mandatory paper checklist** appears after references (not counted).  
   - **CVPR:** Limitations **not required** (encouraged to discuss); no dedicated ethics section — add **IRB/ethics note** if applicable (paper or supplementary).  
   - **AAAI:** Limitations **not required**; Ethics statement **optional** (unnumbered, before acknowledgments/references, counts as content).  

## Conference Templates
- [NeurIPS](https://www.overleaf.com/latex/templates/neurips-2024/tpsbbrdqcmsh)
- [ICML](https://www.overleaf.com/latex/templates/icml2025-template/dhxrkcgkvnkt)
- [ICLR](https://www.overleaf.com/latex/templates/template-for-iclr-2025-conference-submission/gqzkdyycxtvt)
- [ACL](https://www.overleaf.com/latex/templates/association-for-computational-linguistics-acl-conference/jvxskxpnznfj)
- [AAAI](https://www.overleaf.com/latex/templates/aaai-press-latex-template/jymjdgdpdmxp)
- [CVPR](https://www.overleaf.com/latex/templates/cvpr-2026-submission-template/rdtrwgypxxzb)

## Contributing

Please read the [contributing.md](contributing.md) before submitting a pull request.

## Citation

If you find this repository useful, please consider citing it as:

```bibtex
@misc{sarwar2026awesome-ml-style-guide,
  author       = {Sarwar, Nobin},
  title        = {{Awesome ML Conference Paper Writing Style Guide}},
  year         = {2026},
  howpublished = {\url{https://github.com/smsnobin77/awesome-ML-conference-paper-writing-style-guide}},
  note         = {GitHub repository}
}
```

## License

This project is dedicated to the public domain under the Creative Commons CC0 1.0 Universal license.
