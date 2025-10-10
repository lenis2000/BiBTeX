# BibTeX Formatting Guide

This document describes the formatting conventions used in `bib.bib`.

## General Conventions

### Author Names
- Use **first initial only**, followed by last name
- Format: `LastName, F.`
- Multiple authors separated by ` and `
- Examples:
  - `Knutson, A. and Tao, T.`
  - `Borga, J. and Boutillier, C. and F{\'e}ray, V. and M{\'e}liot, P.-L.`

### Titles
- **Always wrap entire title in double curly braces**: `{{Title text here}}`
- This prevents BibTeX from automatically changing capitalization
- Within the title, use single braces for proper nouns and acronyms that must preserve capitalization:
  - `{Brownian}`, `{Baxter}`, `{KPZ}`, `{Liouville}`, `{Robinson-Schensted}`, etc.
- Example: `{{The skew {Brownian} permuton: a new universality class for random constrained permutations}}`

### Special Characters
- Use LaTeX escape sequences:
  - Accented e: `\'e` → é
  - Accented a: `\"{a}` → ä
  - Accented o: `\`{o}` → ò
  - Polish l: `\l` → ł
  - Other: `\'{a}`, `\^{e}`, `\~{n}`, etc.
- Example: `F{\'e}ray, V.` → Féray, V.

### Page Ranges
- Use double hyphen `--` for page ranges (produces en-dash)
- Examples:
  - `pages = {221--260}`
  - `pages = {1359--1417}`

## Journal Abbreviations

Use heavily abbreviated journal names:

| Full Name | Abbreviation |
|-----------|-------------|
| Annals of Probability | `Ann. Probab.` |
| Duke Mathematical Journal | `Duke Math. J.` |
| Communications in Mathematical Physics | `Comm. Math. Phys.` or `Commun. Math. Phys.` |
| Probability Theory and Related Fields | `Probab. Theory Relat. Fields` or `Prob. Theory Relat. Fields` |
| Proceedings of the London Mathematical Society | `Proc. Lond. Math. Soc.` |
| Advances in Applied Mathematics | `Adv. Appl. Math.` |
| Advances in Mathematics | `Adv. Math.` |
| Journal of Mathematical Physics | `J. Math. Phys.` |
| Journal of Physics A | `J. Phys. A` or `J. Phys. A: Math. Theor.` |
| Physical Review B | `Phys. Rev. B` |
| Physical Review Letters | `Phys. Rev. Lett.` |
| Combinatorics, Probability and Computing | `Comb. Probab. Comput.` |
| Discrete Mathematics | `Discrete Math.` |
| Random Structures & Algorithms | `Random Structures \& Algorithms` or `Random Struct. Algor.` |
| Electronic Journal of Combinatorics | `Electron. J. Combin.` |
| Electronic Communications in Probability | `Electron. Commun. Probab.` |
| European Journal of Combinatorics | `European J. Combin.` |
| International Mathematics Research Notices | `Int. Math. Res. Not.` or `Intern. Math. Research Notices` |
| Transactions of the American Mathematical Society | `Trans. Amer. Math. Soc.` |
| Proceedings of the American Mathematical Society | `Proc. Amer. Math. Soc.` |
| Journal of Algebraic Combinatorics | `J. Algebraic Combin.` |
| Selecta Mathematica | `Sel. Math. New Ser.` or `Selecta Math.` |
| Forum of Mathematics, Pi | `Forum Math. Pi` |
| Studies in Applied Mathematics | `Stud. Appl. Math.` |
| Journal of Statistical Mechanics | `J. Stat. Mech.` |
| Inventiones Mathematicae | `Invent. Math.` |
| Journal of Multivariate Analysis | `J. Multivar. Anal.` |

## arXiv Preprints

### Unpublished arXiv Papers
For papers that are ONLY on arXiv (not yet published):

```bibtex
@article{AuthorYear,
  author = {LastName, F.},
  journal = {arXiv preprint},
  note = {arXiv:XXXX.XXXXX [subject.class]},
  title = {{Paper title here}},
  year = {YYYY}
}
```

Example:
```bibtex
@article{KnizelPetrov2025,
  author = {Knizel, A. and Petrov, L.},
  journal = {arXiv preprint},
  note = {arXiv:2507.22011 [math.PR]},
  title = {{Random Lozenge Waterfall: Dimensional Collapse of Gibbs Measures}},
  year = {2025}
}
```

### Published Papers with arXiv
For published papers, include BOTH journal information AND arXiv reference:

```bibtex
@article{AuthorYear,
  author = {LastName, F.},
  journal = {Journal Abbrev.},
  note = {arXiv:XXXX.XXXXX [subject.class]},
  volume = {XX},
  number = {X},
  pages = {XXX--XXX},
  title = {{Paper title}},
  year = {YYYY},
  doi = {XX.XXXX/...}
}
```

Example:
```bibtex
@article{BorgaMaazoun2022BaxterCoalescent,
  author = {Borga, J. and Maazoun, M.},
  title = {Scaling and local limits of {Baxter} permutations and
           bipolar orientations through coalescent-walk processes},
  journal = {Ann. Probab.},
  volume = {50},
  number = {4},
  pages = {1359--1417},
  year = {2022},
  doi = {10.1214/21-AOP1559},
  note = {arXiv:2008.09086 [math.PR]}
}
```

### arXiv Subject Classifications
Common subjects used:
- `[math.PR]` - Probability
- `[math.CO]` - Combinatorics
- `[math.RT]` - Representation Theory
- `[math.AG]` - Algebraic Geometry
- `[math-ph]` - Mathematical Physics
- `[cond-mat.stat-mech]` - Statistical Mechanics
- `[hep-th]` - High Energy Physics - Theory

## Entry Types

### @article
Standard for journal articles (both published and arXiv preprints)

### @book
For books. Include:
- `author` or `editor`
- `title`
- `publisher`
- `year`
- Optional: `series`, `volume`, `edition`

### @incollection
For book chapters. Include:
- `author`
- `title`
- `booktitle`
- `editor`
- `publisher`
- `pages`
- `year`

### @inproceedings
For conference proceedings. Similar to @incollection.

### @Unpublished
For unpublished work (surveys, lecture notes, etc.):

```bibtex
@Unpublished{AuthorYear,
  author = {LastName, F.},
  title = {Title of work},
  year = {YYYY},
  note = {arXiv:XXXX.XXXXX [subject]}
}
```

### @misc
For web resources, online notes, etc.:

```bibtex
@misc{AuthorYear,
  author = {LastName, F.},
  title = {{Title}},
  note = {Available at \url{https://...}},
  year = {YYYY}
}
```

Or with `howpublished`:

```bibtex
@misc{AuthorYear,
  author = {LastName, F.},
  title = {{Title}},
  howpublished = {\url{https://...}},
  note = {Available at: \url{https://...}, Accessed on: YYYY-MM-DD},
  year = {YYYY}
}
```

## Optional Fields

### DOI
Include when available:
```bibtex
doi = {10.1214/24-AOP1706}
```

### URL
Occasionally included for online resources:
```bibtex
url = {https://doi.org/...}
```

### Publisher
For books and proceedings:
```bibtex
publisher = {Cambridge University Press}
```

### Additional Notes
For translations, additional publication info, etc.:
```bibtex
note = {arXiv:2307.11885 [math.PR], to appear in Compositio Math.}
```

## Field Ordering

Typical field order (though order doesn't affect output):

1. `author`
2. `title`
3. `journal` or `booktitle`
4. `volume`
5. `number`
6. `pages`
7. `year`
8. `doi`
9. `note`
10. `publisher` (for books)
11. `url`

## Citation Keys

Citation keys typically follow these patterns:
- `AuthorYear` - single author: `Romik2006_permutations`
- `Author1Author2Year` - two authors: `RomikSniady2016`
- `Author1...AuthorNYear` - 3+ authors: `BorgaBoutillierFerayMeliot2025`
- Sometimes with descriptor: `Dyson1962_part_3_of_statistical_theory_energy_levels`
- Sometimes with topic: `BorgaMaazoun2022BaxterCoalescent`

## Special Cases

### Mathematical Symbols in Titles
Use LaTeX math mode syntax:
```bibtex
title = {{Semiclassical asymptotics of $GL_N(\mathbb{C})$ tensor products and quantum random matrices}}
```

### Multi-line Fields
Can break long fields across lines with proper indentation:
```bibtex
title = {The feasible regions for consecutive patterns of
         pattern-avoiding permutations}
```

### Ampersand in Journal Names
Escape ampersand with backslash:
```bibtex
journal = {Random Structures \& Algorithms}
```

## Example Entry (Complete)

```bibtex
@article{BorgaBoutillierFerayMeliot2025,
  author = {Borga, J. and Boutillier, C. and F{\'e}ray, V. and M{\'e}liot, P.-L.},
  doi = {10.1214/24-AOP1706},
  journal = {Ann. Probab.},
  note = {arXiv:2307.11885 [math.PR]},
  number = {1},
  pages = {299--354},
  title = {{A determinantal point process approach to scaling and local limits of random Young tableaux}},
  volume = {53},
  year = {2025}
}
```

---

## Quick Checklist for New Entries

- [ ] Author names: first initial only
- [ ] Title: wrapped in double braces `{{...}}`
- [ ] Proper nouns in title: single braces `{Name}`
- [ ] Journal: properly abbreviated
- [ ] arXiv: included in `note` field with subject classification
- [ ] Pages: use `--` for ranges
- [ ] Special characters: use LaTeX escaping
- [ ] Year: present and correct
- [ ] DOI: included if available
