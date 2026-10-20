# Post templates

Copy `chrome-study.md` or `chrome-exploit-lab.md` into `_posts/YYYY-MM-DD-your-slug.md`.
Fill the date (example: `2026-10-20 20:00:00 +0900`) and title.
Use categories `[Browser, Chrome]`, tag `study` for Study or `exploit-lab` for Exploit Lab.
Push to master to trigger the existing GitHub Pages workflow.

The sidebar override is at `_includes/sidebar.html`. It lists Home / Target / Browser / Chrome / Study / Exploit Lab / About, with indentation for hierarchy. This is a static navigation tree, not a collapsible menu.
Existing tabs are not deleted: older direct URLs remain accessible, but their sidebar links are hidden.
