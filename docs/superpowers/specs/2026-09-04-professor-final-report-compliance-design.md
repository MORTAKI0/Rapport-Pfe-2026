# Final Professor + EMSI Compliance Design

## Goal

Bring the PFE report into final alignment with the professor's review points 6–14 and the EMSI Rabat PFE writing guide, while preserving all previously validated technical facts and the five-chapter structure.

## Non-negotiable factual boundaries

- Java/Spring Boot remains the most mature implementation.
- The Java trajectory is progressive: Spring Boot 2.1 -> 2.7 -> 3.5 -> 4.0 with Java versions adapted by stage.
- Angular 18 -> 19 and 19 -> 20 are the validated/sealed transitions supported by the retained execution evidence.
- Angular 20 -> 21 is prepared but not started.
- Angular 11 -> 21 is a target trajectory, not a demonstrated end-to-end result.
- Reviewer acceptance never means a patch is automatically applied; sensitive repair remains governed and human approval remains required.
- No generic time, cost, or productivity gain may be claimed without representative quantitative evidence.

## Professor feedback mapping

### 6. Resume

Rewrite the French Resume to make the actually demonstrated results explicit.

Required structure:
1. Context/problem and project objective.
2. Immediately highlight the main contribution: a governed multi-agent architecture.
3. Method/delivery approach in concise form.
4. Concrete results actually demonstrated.
5. Short conclusion/limitation.

Remove the detailed agent-role enumeration and the detailed deterministic-service enumeration. Replace them with the professor's core idea: critical operations remain under deterministic control and human supervision.

Concrete results to state:
- operational Java/Spring Boot progressive trajectory;
- three successive Java demonstrations from CLI proof-of-concept to full-stack Control Tower;
- isolated workspaces, Maven validation, governed repair, supervision and traceability in the mature Java implementation;
- Angular 18 -> 19 and 19 -> 20 executed and sealed;
- 20 -> 21 prepared but not started;
- resulting ability to structure migrations stage by stage and tie decisions to evidence.

The negative quantitative limitation must remain secondary, not dominate the conclusion.

### 7. Keywords

Use at most five keywords, alphabetically ordered, in French, English and Arabic.

French target set:
- Angular
- Java/Spring Boot
- migration logicielle
- systèmes multi-agents
- traçabilité

English target set:
- Angular
- Java/Spring Boot
- multi-agent systems
- software migration
- traceability

Arabic must be a faithful equivalent set of five terms.

### 8. General conclusion

Open by recalling the problem the project sought to solve before restating the objective. Then keep the flow:
problem -> objective/contribution -> concrete Java/Angular results -> limitations -> perspectives.

### 9. Remove 5.6.1

Remove the subsection heading "Évaluation de l'intégration Azure OpenAI" while keeping and integrating its content into the surrounding qualitative analysis with a transition paragraph.

### 10. Remove 2.3.1 and 2.3.2

Flatten "Notions à distinguer" and "Modèles d'organisation" into Section 2.3. Add a proper introduction before Table 2.2 and a transition into the organization-model discussion.

### 11. Remove 2.2.1

Remove the subsection heading "Définition" under Systèmes multi-agents. The definition becomes the opening of Section 2.2.

### 12. Remove 1.3.1, 1.3.2, 1.3.3

Flatten the three subsections under "Problématique traitée" into a coherent continuous section. Preserve the figure and the final research question, but connect them with prose instead of nested headings.

### 13. Add text before 4.7.2 table

Before the "Difficultés techniques et corrections" table, add a short paragraph explaining that the table synthesizes representative engineering obstacles, their causes, and the corrective decisions used to stabilize the prototypes.

### 14. IEEE references

Move from manually formatted references to BibTeX with IEEEtran style while preserving the existing citation keys used throughout the report. Online sources must carry consultation dates. Add the cite package for IEEE-style numeric citation grouping.

## EMSI guide compliance

### Page format

- A4 portrait.
- Margins: top 2.5 cm, bottom 2.5 cm, left 3 cm, right 2.5 cm.
- Body text line spacing: 1.5.
- Body text remains justified by normal LaTeX paragraph layout.
- Preliminary pages retain Roman numbering; main content retains Arabic numbering.

### Resume/Abstract/Arabic summary

- French Resume: 150–300 words.
- Abstract: faithful English translation of the final French Resume.
- Arabic summary: faithful Arabic translation of the same content.
- Five keywords maximum in each language.
- The three summaries must contain the same factual results and limitations.

### Figures and tables

- Figures remain centered with captions below.
- Table captions must appear above tables.
- Every figure and table should be introduced/cited in prose before its appearance when a natural introduction is missing.
- Keep existing labels and references stable wherever possible to avoid broken cross-references.

### Bibliography

Use:

```latex
\usepackage{cite}
...
\bibliographystyle{IEEEtran}
\bibliography{references}
```

Create `references.bib` with the current keys and normalize books, articles, standards, conference papers and online documentation to IEEE-compatible BibTeX entries.

## Scope guardrails

- Do not redesign the cover or chapter visual identity.
- Do not change the five-chapter organization.
- Do not invent experiments, metrics, dates or migration successes.
- Do not enlarge claims about Angular.
- Do not remove existing technical evidence merely to shorten the report.
- Prefer short transitional prose when flattening headings so the report remains readable.
- Preserve current figure numbering and table numbering as much as possible.

## Verification

After implementation:
- scan all professor-targeted headings to ensure removed numbering is gone;
- verify the three summaries are factually aligned and each keyword list contains five items;
- verify no forbidden old Resume phrases remain;
- verify the General Conclusion begins with the problem;
- verify `IEEEtran` + `references.bib` are wired into `main.tex`/`bibliographie.tex`;
- scan for stale manual `\bibitem` usage;
- scan ordinary table environments for captions still below their tabular content;
- check all `\cite{...}` keys are present in `references.bib`;
- report PDF compilation separately: do not claim successful compilation unless an actual LaTeX build is executed successfully.
