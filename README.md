# portfolio-data

Resume of Himalay Cherukuri shredded into mapped JSON for a portfolio website (Data Analysis / Data Science first).

Rebuild: put the resume PDF at `source/resume.pdf`, then run `python scripts/run_all.py`
(needs Python 3; uses `pdftotext` if installed, otherwise `pip install pypdf`).

| Script | Output (build/ is private, data/ is public) |
|---|---|
| 01_extract.py | build/raw.txt (layout text) |
| 02_sections.py | build/sections.json (sections + public contact only; phone/street/ZIP dropped) |
| 03_roles.py | build/roles.json (company, title, location, dates) |
| 04_bullets.py | build/bullets.json (bullet text, regex metrics, Environment tools) |
| 05_skills.py | build/skills_raw.json (skills grouped; usage per bullet/role) |
| 06_tag.py | build/tagged.json (tags, primary category, focus_score) |
| 07_build_map.py | data/resume_map.json, data/skills.json |
| 08_summary.py | data/summary.json (hand-written one-liners, headline, About) |

See DESIGN_SPEC.md for the JSON schema and the intended site.
