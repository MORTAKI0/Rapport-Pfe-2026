# Professor Report Review Fixes Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Apply the supervisor's page-specific review remarks to Chapters I–III of the PFE report, improving academic formulation, visual explanation, section hierarchy, and comparative analysis without changing the validated technical substance.

**Architecture:** Changes are limited to LaTeX report content. Each supervisor remark is handled as an independent task with a fresh read of the affected section, a focused edit, static verification, and a separate commit to `main`. Existing factual boundaries remain unchanged: Java code-truth is authoritative for Java, Angular claims remain conservative, and no unverified project history is invented.

**Tech Stack:** LaTeX, TikZ, tabularx/longtable, GitHub.

**Spec:** Supervisor feedback provided on 2026-08-27 in the PFE RAPPORT review conversation.

## Global Constraints

- Preserve the current five-chapter structure.
- Preserve the report reference date and previously validated chronology unless directly relevant to a requested correction.
- Do not invent a historical Gantt artifact; if no original forecast is found, label any reconstruction explicitly.
- Preserve the distinction between agents, deterministic services, tools, and human governance.
- Keep Angular implementation claims conservative unless supported by audited code.
- Each task must end with a separate GitHub commit.

---

### Task 1: Chapter I objectives and title hierarchy

**Files:**
- Modify: `chapitre1/contexte_general.tex`
- Modify: `chapitre1/integration_azure_exigences.tex`

- [ ] Re-read the current objective section and the Azure supplement hierarchy.
- [ ] Rewrite specific objectives as result-oriented statements, capitalized and ordered chronologically.
- [ ] Replace the technology-activity wording with an implementation-result wording.
- [ ] Remove the unnecessary subsection title that currently becomes 1.8.1 while preserving its content.
- [ ] Verify objective order and heading hierarchy.
- [ ] Commit.

### Task 2: Forecast Gantt and visual legend

**Files:**
- Modify: `chapitre1/contexte_general.tex`

- [ ] Search Jira, Confluence, Drive, and repository history for an original forecast planning artifact.
- [ ] If an original forecast is found, add it with source-faithful dates.
- [ ] If none is found, add a clearly labelled reconstructed forecast only from documented initial milestones; do not present it as an archived original.
- [ ] Convert the retrospective Gantt legend from prose into a visual legend directly below the table.
- [ ] Verify that forecast and retrospective views are explicitly distinguished.
- [ ] Commit.

### Task 3: Introduce iterations/increments section

**Files:**
- Modify: `chapitre1/contexte_general.tex`

- [ ] Re-read the section transition into the iteration table.
- [ ] Add a short academic paragraph explaining what the table represents and why it is useful.
- [ ] Verify that it does not repeat the Gantt explanation.
- [ ] Commit.

### Task 4: Convert technical cycle paragraph into a visual iterative schema

**Files:**
- Modify: `chapitre1/contexte_general.tex`

- [ ] Replace the sentence-only cycle with a TikZ loop covering observation, requirement, design, implementation, verification, scenario/demo, and feedback.
- [ ] Keep a short explanatory paragraph below the diagram.
- [ ] Verify figure label/caption and flow direction.
- [ ] Commit.

### Task 5: Chapter II manual process and traceability analysis

**Files:**
- Modify: `chapitre2/etat_art_migration.tex`

- [ ] Re-read the manual-process subsection.
- [ ] Convert the manual migration loop into a visual diagram.
- [ ] Expand the analysis of dispersed state, evidence, decisions, and their effect on reproducibility, auditability, parallel follow-up, and handover.
- [ ] Verify that the critique remains qualitative and does not invent measurements.
- [ ] Commit.

### Task 6: Chapter II comparison and ecosystem interpretation

**Files:**
- Modify: `chapitre2/etat_art_migration.tex`

- [ ] Add an introductory paragraph before the comparative table.
- [ ] Add an analytical paragraph after the table comparing the families with the Migration Factory.
- [ ] Add an introductory/explanatory paragraph before the positioning map.
- [ ] Expand the interpretation of deterministic migration, AI-assisted modernization/repair, multi-agent orchestration, and standards/protocols.
- [ ] Verify that external approaches are represented consistently with the current bibliography.
- [ ] Commit.

### Task 7: Merge Chapter II positioning and enterprise-model integration sections

**Files:**
- Modify: `chapitre2/etat_art_migration.tex`
- Modify or retire integration path for: `chapitre2/modeles_manages_entreprise.tex`
- Modify: `main.tex`

- [ ] Re-read the end of Chapter II and the managed-model supplement.
- [ ] Merge both into one coherent top-level section on Migration Factory positioning and enterprise integration choices.
- [ ] Preserve Azure content as an architectural positioning decision, not a detached second conclusion.
- [ ] Remove the now-redundant injected standalone section from the chapter inclusion path.
- [ ] Verify section numbering and conclusion placement.
- [ ] Commit.

### Task 8: Strengthen Chapter III introduction and section openings

**Files:**
- Modify: `chapitre3/conception_architecture_sma.tex`

- [ ] Expand the chapter introduction to explain the transition from conceptual state of the art to project-specific design decisions.
- [ ] Add an introductory/explanatory paragraph to 3.1 before the viewpoints table.
- [ ] Add an introductory/explanatory paragraph to 3.2 before the selected SMA model.
- [ ] Verify that the new text adds rationale rather than repeating tables.
- [ ] Commit.

### Task 9: Flatten 3.2.1/3.2.2 and deepen repository-specialization rationale

**Files:**
- Modify: `chapitre3/conception_architecture_sma.tex`

- [ ] Remove the two nested subsection headings under 3.2.
- [ ] Integrate their content into a continuous argument under `Choix du modèle SMA`.
- [ ] Expand the rationale for two specialized repositories: runtime/toolchain independence, dependency models, validation cycles, failure modes, coupling reduction, maintenance, and independent evolution.
- [ ] Verify that the shared architectural principles remain explicit.
- [ ] Commit.

### Task 10: Final static review

**Files:**
- Review: `main.tex`, Chapters I–III and supplements touched above.

- [ ] Check duplicate headings, section numbering risks, references, labels, captions, and stale prose.
- [ ] Check that every supervisor remark is mapped to a completed change.
- [ ] Report compilation as unverified unless a real LaTeX build is run successfully.
