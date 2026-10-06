# Component types (v0.1)

Six types, coded A–F. A paper decomposes into an **ordered list** of
components; most papers yield 6–12 (a long Methods section may split into
C1, C2, …).

| Code | Type | Definition | Typical content |
|------|------|------------|-----------------|
| A | `MotivationProblem` | Why the work exists | Research gap, problem statement, motivating examples |
| B | `LiteratureReview` | How the work positions itself | Survey of related work, critical commentary |
| C | `MethodStrategy` | What was done, in principle | Models, algorithms, experimental design, protocols |
| D | `ProcessResults` | What happened | Empirical results, observations, measurements |
| E | `ConclusionExtensions` | What it means, what is next | Conclusions, limitations, future work |
| F | `AppendicesArtifacts` | Supporting materials | Datasets, code, proofs, supplementary figures |

An optional seventh type, `ContributionStatement` (G), may hold explicit
"who did what" sections; otherwise contributor roles attach directly to
components A–F via a CRediT subset (see the schema draft).

Boundary rule of thumb: one component per coherent section or sub-section.
When in doubt, prefer splitting a long heterogeneous section over merging
two distinct rhetorical moves.
