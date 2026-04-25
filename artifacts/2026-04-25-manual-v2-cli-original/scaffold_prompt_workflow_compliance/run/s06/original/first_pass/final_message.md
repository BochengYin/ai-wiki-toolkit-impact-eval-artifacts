Implemented the team coding memory scaffold.

Key changes:
- Added starter `conventions/`, `problems/`, and `features/` areas in [content.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s06/src/ai_wiki_toolkit/content.py:54) and installer directory creation in [scaffold.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s06/src/ai_wiki_toolkit/scaffold.py:126).
- Added repo-local starter skills for `ai-wiki-clarify-before-code` and `ai-wiki-capture-review-learning`.
- Added managed `schema/team-memory-v1.md` guidance and refreshed managed prompt/system workflow text.
- Updated doctor checks for the new areas, schema, and prompt guidance in [doctor.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s06/src/ai_wiki_toolkit/doctor.py:100).
- Updated catalog classification for convention, problem, and feature docs in [wiki_schema.py](<eval-root>/scaffold_prompt_workflow_compliance/workspaces/20260425-160315/slots/s06/src/ai_wiki_toolkit/wiki_schema.py:44).
- Updated README and scaffold/compatibility tests.

Verification:
- `PYTHONPATH=src python -m pytest`  
- `124 passed in 0.82s`
- `git diff --check`

Managed routing from `ai-wiki/_toolkit/system.md` guided the workflow; it was cited here but not logged as a reuse event because `_toolkit/**` docs are managed.

AI Wiki Reuse Evidence: wiki_used  
AI Wiki Eligibility: eligible  
AI Wiki Reuse Docs: index, conventions/index, decisions, review-patterns/index, problems/index, features/index  
AI Wiki Material Effects: changed_plan, reused_convention, avoided_retry  
AI Wiki Missed Memory: none known  
AI Wiki Update Candidate: None