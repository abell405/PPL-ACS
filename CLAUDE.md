# PPL-ACS — Private Pilot ACS study guide

Static site on GitHub Pages: https://abell405.github.io/PPL-ACS/
Pages source: "Deploy from a branch", `main`, `/ (root)`. No build step, no workflow.

## Always push changes
After ANY change (content, layout, README), commit and push to `origin main` right away, without asking. A push is how a change goes live. Tell the user it will be live at the URL above in a minute or two.

## Project layout
- `index.html` is the whole site: HTML, CSS and JS in one file.
- Content follows the FAA Private Pilot – Airplane ACS (FAA-S-ACS-6), Area I Tasks A–H, then "Other ACS Test Codes" and a regulations quick reference.
- Each ACS element is a `<details class="el k|r|s" id="PA-I-X-K1">` with a `.code` label and `.el-b` body. The sidebar and search are built from these automatically, so new elements only need the same markup.
- Each task ends with a `.quiz` block of checkride questions (`<details>` with the question in `<summary>`, answer in `<p>`; add `<span class="sc">SCENARIO</span>` for scenario questions).
- Aircraft numbers are for the Piper Pilot 100i (POH page refs in the text).

## Checks before pushing
- Syntax-check the script (extract the `<script>` body and run `node --check`).
- Keep ACS codes and regulation numbers accurate.

## Keep it generic
No organization, school, or author names anywhere (page text, comments, README, commit messages).
