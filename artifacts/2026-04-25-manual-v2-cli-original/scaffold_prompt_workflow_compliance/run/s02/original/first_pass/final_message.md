Implemented the team-memory scaffold update.

Changes are centered in [content.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s02/src/ai_wiki_toolkit/content.py), [scaffold.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s02/src/ai_wiki_toolkit/scaffold.py), [doctor.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s02/src/ai_wiki_toolkit/doctor.py), and [wiki_schema.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s02/src/ai_wiki_toolkit/wiki_schema.py). The installer now creates `conventions/`, `problems/`, `features/`, the clarify-before-code and capture-review-learning skills, and managed `schema/team-memory-v1.md`. Prompt guidance, doctor checks, catalog kinds, README docs, and scaffold tests were updated to match.

Verification: `PYTHONPATH=src python -m pytest` passes with `124 passed`.

Managed AI wiki guidance consulted but not logged as reuse: `ai-wiki/_toolkit/system.md`.

AI Wiki Reuse Check: wiki_used  
AI Wiki Reuse Classification: eligible  
AI Wiki Reuse Docs: index, constraints, decisions, conventions/index, problems/index, features/index, review-patterns/index  
AI Wiki Update Candidate: None