# Final Professor + EMSI Compliance Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Apply the professor's final review points 6–14 and the EMSI Rabat PFE guide across the complete report without changing validated technical facts.

**Architecture:** The work is a report-wide editorial and LaTeX compliance pass. It preserves the five-chapter structure and existing evidence, flattens only the requested heading levels, rewrites the three summaries from one frozen French source, makes the conclusion problem-first, normalizes table presentation, and migrates references to BibTeX/IEEEtran.

**Tech Stack:** LaTeX, BibTeX, IEEEtran, GitHub.

**Spec:** `docs/superpowers/specs/2026-09-04-professor-final-report-compliance-design.md`

## Global Constraints

- Preserve the validated Java/Spring Boot and Angular evidence boundaries from the spec.
- Keep Angular 11–21 as an objective, not a completed result.
- Keep 20–21 prepared but not started.
- Do not invent quantitative gains.
- Preserve existing labels and references where possible.
- Work directly on `main`, as explicitly established for this report workflow.
- Commit logically distinct groups of changes separately.

---

### Task 1: Rewrite and synchronize the three summaries

**Files:**
- Modify: `intros/resume.tex`
- Modify: `intros/abstract.tex`
- Modify: `intros/resume_arabe.tex`

- [ ] Re-read the three current summaries and Chapter V result statements.
- [ ] Rewrite the French Resume to 150–300 words using the exact result hierarchy in the spec.
- [ ] Remove the two detailed enumerations explicitly rejected by the professor.
- [ ] Put the main governed-SMA contribution before the architecture/method paragraph.
- [ ] Make the concrete Java and Angular results explicit before mentioning quantitative limits.
- [ ] Reduce French keywords to five alphabetically ordered items.
- [ ] Rewrite the English Abstract as a faithful translation of the frozen French content; use five alphabetically ordered keywords.
- [ ] Rewrite the Arabic summary to the same factual structure and five equivalent keywords.
- [ ] Verify the three versions make identical maturity claims.
- [ ] Commit.

### Task 2: Make the General Conclusion problem-first

**Files:**
- Modify: `conclusion_generale.tex`

- [ ] Re-read the General Introduction problem statement and current conclusion.
- [ ] Replace the opening with a concise recall of the problem to be solved.
- [ ] Follow with objective/contribution, then preserve the validated Java/Angular results, limitations and categorized perspectives.
- [ ] Remove any duplicated or weaker opening prose created by the reordering.
- [ ] Verify no Angular overclaim is introduced.
- [ ] Commit.

### Task 3: Flatten the requested Chapter I hierarchy

**Files:**
- Modify: `chapitre1/contexte_general.tex`

- [ ] Remove the subsection headings corresponding to 1.3.1, 1.3.2 and 1.3.3.
- [ ] Keep all substantive content and Figure 1.x evidence in the same order.
- [ ] Add transitions so the section reads as one argument: coordination problem -> limits of monolithic/single-agent approach -> retained architecture -> research question.
- [ ] Verify the final research question remains visually distinct.
- [ ] Commit.

### Task 4: Flatten the requested Chapter II hierarchy

**Files:**
- Modify: `chapitre2/etat_art_migration.tex`

- [ ] Remove subsection heading 2.2.1 (`Définition`).
- [ ] Keep the definition as the opening of `Systèmes multi-agents`.
- [ ] Remove subsection headings 2.3.1 (`Notions à distinguer`) and 2.3.2 (`Modèles d'organisation`).
- [ ] Add an introductory paragraph immediately before Table 2.2 explaining why the four concepts are distinguished.
- [ ] Add a transition after Table 2.2 into the organization-model discussion.
- [ ] Verify Table 2.2 still has a natural textual introduction before appearance.
- [ ] Commit.

### Task 5: Flatten 5.6.1 and strengthen 4.7.2 introduction

**Files:**
- Modify: `chapitre5/evaluation_resultats.tex`
- Modify: `chapitre4/architecture_implementation_systeme.tex`

- [ ] Remove the `Évaluation de l'intégration Azure OpenAI` subsection heading while preserving its content.
- [ ] Add a transition that introduces Azure evaluation as a specific dimension of the qualitative analysis.
- [ ] Add a concise introductory paragraph before the Chapter IV `Difficultés techniques et corrections` table.
- [ ] Verify heading numbering no longer exposes 5.6.1.
- [ ] Commit.

### Task 6: Apply EMSI page and summary-format rules

**Files:**
- Modify: `main.tex`
- Modify: `intros/resume_arabe.tex` if local summary formatting still overrides body rules incorrectly.

- [ ] Change margins to top 2.5 cm, bottom 2.5 cm, left 3 cm, right 2.5 cm.
- [ ] Change body line spacing to 1.5.
- [ ] Keep list-of-figures/list-of-tables local compacting isolated inside groups.
- [ ] Ensure the Arabic summary restores the report's 1.5 spacing after its local block.
- [ ] Add `\usepackage{cite}` before `hyperref`.
- [ ] Commit.

### Task 7: Normalize table-caption placement and pre-introductions

**Files:**
- Review/modify: `chapitre1/contexte_general.tex`
- Review/modify: `chapitre1/integration_azure_exigences.tex`
- Review/modify: `chapitre2/etat_art_migration.tex`
- Review/modify: `chapitre2/modeles_manages_entreprise.tex`
- Review/modify: `chapitre3/conception_architecture_sma.tex`
- Review/modify: `chapitre3/passerelle_modeles_azure.tex`
- Review/modify: `chapitre4/architecture_implementation_systeme.tex`
- Review/modify: `chapitre4/integration_azure_openai.tex`
- Review/modify: `chapitre5/evaluation_resultats.tex`

- [ ] For every ordinary `table` float, move `\caption` and `\label` before the `tabularx`/tabular body.
- [ ] Leave `longtable` captions at the top.
- [ ] For each figure/table that appears without a natural prior textual introduction, add one concise sentence before the float; do not add redundant prose where an introduction already exists.
- [ ] Preserve labels and captions verbatim unless a professor-requested wording change requires otherwise.
- [ ] Verify figures still keep captions below.
- [ ] Commit.

### Task 8: Convert bibliography to IEEE BibTeX

**Files:**
- Create: `references.bib`
- Modify: `bibliographie.tex`
- Review: all `\cite{...}` usages across report files.

- [ ] Convert every current `\bibitem` key into an equivalent BibTeX entry with the same key.
- [ ] Use appropriate entry types for books, articles/conference papers, standards and online documentation.
- [ ] Preserve current source titles, authors/organizations, years and URLs unless a verified correction is necessary.
- [ ] Add consultation date metadata to online documentation/web entries.
- [ ] Replace manual `thebibliography` content with `\bibliographystyle{IEEEtran}` and `\bibliography{references}` while preserving the bibliography TOC entry.
- [ ] Verify every citation key used in the report exists exactly once in `references.bib`.
- [ ] Verify no manual `\bibitem` remains active.
- [ ] Commit.

### Task 9: Three-pass final audit

**Files:**
- Review all report source files included by `main.tex`.

- [ ] Pass 1 — professor feedback: verify points 6–14 line by line.
- [ ] Pass 2 — factual consistency: compare Resume/Abstract/Arabic, Introduction, Chapters I/IV/V and General Conclusion for Java/Angular maturity claims, dates and result wording.
- [ ] Pass 3 — EMSI compliance: margins, 1.5 spacing, 150–300-word French Resume, max-five keywords, hierarchy, table captions, figure/table introductions, IEEE/BibTeX wiring and bibliography keys.
- [ ] Search for stale removed headings and forbidden Resume phrases.
- [ ] Search for stale future-final-report wording, duplicated conclusions and contradictory Angular claims.
- [ ] If a real LaTeX build environment is available, compile and inspect the PDF; otherwise explicitly report compilation as unverified.
- [ ] Commit any final corrections found by the audit.
