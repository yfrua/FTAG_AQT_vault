# Notes

Preferences and working context observed across sessions.

- User is a physicist working hands-on in this codebase; prefers learning through real diagnostics on real outputs, not toy examples.
- Example plots in lessons: use period ADE outputs (163 fb⁻¹, better statistics); user rejected the period-A plots as "terrible".
- Workspace layout: keep everything under `lessons/` (user asked for consolidation once files sprawled at repo root). Lessons are Markdown per the current teach guideline.
- User reads plots critically — questioned stack vs fit-result consistency, which led to the SF_b/gamma degeneracy diagnosis. Encourage this; plot-reading is a strength to build on.
- Physics decisions (e.g. fixing SF_Neg_TagBin6_b, extending the delta method) belong to the user/FTAG; the agent diagnoses and documents but does not change fit models unilaterally.
- Environment: `run/setup_env.sh` before any ROOT/build command; CVMFS available; `root` from AnalysisBaseExternals.
- 2026-09-23: workspace migrated to the updated teach skill format — all docs are Obsidian-flavored Markdown (frontmatter, wikilinks, callouts, foldable quiz answers, mermaid); reference docs live in `reference/*.md` (old HTML + `style.css` removed); [[GLOSSARY]] created and is the canonical terminology for all future lessons.
