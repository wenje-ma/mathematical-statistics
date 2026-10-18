# Mathematical Statistics

> Mathematical statistics lecture notes and 18 weeks of fully worked homework, bilingual (Chinese/English), covering sampling distributions through hypothesis testing.

The course follows the textbook **《数理统计》 (Mathematical Statistics) by Zhao Ying (赵颖), Wang Dianpeng (王典朋), Kong Xiangshun (孔祥顺) & Yu Jun (虞俊)**, Beijing Institute of Technology Press — one of China's "14th Five-Year Plan" planned textbooks.

## Repository structure

```
mathematical-statistics/
├── cn/
│   ├── notes.md              # Chinese lecture notes (single file, 722 lines)
│   └── homework/
│       └── week1.md … week18.md
├── en/
│   ├── notes.md              # Complete English translation (722 lines, aligned)
│   └── homework/
│       └── week1.md … week18.md
└── textbooks/
    ├── mathematical-statistics.pdf           # Textbook scan
    └── mathematical-statistics_ocr.pdf       # OCR (searchable) copy
```

## The notes

`notes.md` is a single reference file organized as **8 chapters** with `##` headings:

1. Introduction and basic concepts
2. Sampling distributions (order statistics and common sampling distributions)
3. Exponential families and sufficient, complete statistics
4. Point estimation (method of moments and maximum likelihood)
5. Criteria for evaluating estimators
6. UMVUE and the Cramér–Rao inequality
7. Interval estimation
8. Hypothesis testing

This is one of the densest repositories in the series: 147 definitions, 79 theorems, and ~1,000 displayed equations, all bold-tagged with mathematics in `$…$` / `$$…$$`.

## The homework

Each `homework/weekN.md` follows the series-wide format:

1. **Toolbox** — a blockquote restating the definitions needed (e.g. unbiasedness, efficiency, consistency);
2. **Problems** — the assigned exercises;
3. **Solutions** — complete derivations ending with `$\blacksquare$`.

There are **18 weeks** (90 fully solved problems) in each language. Typical problem: finding $c$ so that $c\sum (X_{i+1}-X_i)^2$ is an unbiased estimator of $\sigma^2$.

## Bilingual layout

- `cn/` — authoritative Chinese version.
- `en/` — complete parallel English translation; files share identical names and line counts.

## The `textbooks/` folder

The two PDFs are the scanned textbook and its OCR copy — **external reference material**, not compiled from the notes. There is no build system; everything is plain Markdown rendered with GitHub's LaTeX support.

## Related repositories

Other course-notes repositories in the same series: [probability](https://github.com/wenje-ma/probability), [real-analysis](https://github.com/wenje-ma/real-analysis), [numerical-calculation-methods](https://github.com/wenje-ma/numerical-calculation-methods), and the full list on the [profile page](https://github.com/wenje-ma).
