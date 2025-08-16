RGT-SC

> A lightweight, single-file React web app for calculating and explaining scores for a talent show–style competition, with a transparency view for the underlying formulas and a fairness notice.




---

📖 Overview

RGT-SC is a client-side scoring calculator that runs entirely in the browser from a single index.html. It mounts a React component named TalentCalculator and includes a dedicated “transparency” view that explains calculation logic & formulas alongside a fairness notice for results interpretation. This makes it suitable for small events or communities that want a quick, auditable way to aggregate inputs and display results without a backend.


---

✨ Features

Single-page React app — mounts TalentCalculator via ReactDOM.render.

Transparency view — labeled “Calculation Logic & Formulas,” with a call-to-action like “Explore the full calculation logic behind Rustic Got Talent.”

Fairness disclaimer — explicitly notes that statistical indicators are not 100% accurate and should be double-checked by management.

Audience input support — strings such as “Add Audience Member” and “Audience Member” indicate an audience contribution workflow.

Zero backend — static hosting ready; everything is contained in index.html.


> Note: Text keys such as t.formulaResults suggest a simple text dictionary that can be adapted for localization if desired.




---

🚀 Installation

You can run the app locally or host it on any static host.

Option A — Open the file locally

1. Download or clone the repository.


2. Open index.html in a modern browser (Chrome, Edge, Firefox).



Option B — Serve with a tiny local web server (recommended)

Some browser policies work best when files are served over http:// instead of file://.

Python 3 (any OS):

python -m http.server 5173
# then open http://localhost:5173/index.html

Node (via serve):

npm i -g serve
serve .
# then open the printed local URL, e.g. http://localhost:3000

Option C — Deploy to GitHub Pages

1. In the repo: Settings → Pages.


2. Source: Deploy from a branch, select main, folder /root.


3. Save — Pages will publish your site at https://<your-username>.github.io/RGT-SC/.




---

🛠️ Usage

1. Open the app in your browser.


2. Use the UI to add audience members and enter inputs as prompted.


3. View results and switch to the Transparency / Formulas view to understand how values are derived.


4. Use the Back to Calculator control to return to the main calculator interface.



> The exact field labels and steps are defined inside index.html. Since the app is entirely client-side, customization typically means editing strings and simple React state/logic in that file.




---

📦 Technologies

HTML (100%)

React & ReactDOM (via CDN) — used to render the TalentCalculator component.

May include inline JSX compiled in-browser (commonly via Babel Standalone) within index.html.



---

🔧 Configuration

No runtime configuration or environment variables are required.
If you want to translate or change interface text, look for the UI string dictionary (e.g., keys like t.formulaResults) inside index.html and edit as needed.


---

✅ Requirements

A modern desktop browser.

No backend, database, or build step required.



---

🗂️ Repository Structure

RGT-SC/
└── index.html        # Single-file React app containing UI, logic, and strings

Root — Static site root; can be deployed to any static host.
index.html — The entire app: React component(s), UI text, logic, and mount code.


---

🔗 Flow Chart (conceptual)

flowchart LR
  U[User] --> UI[React UI: TalentCalculator]
  UI -->|inputs| S[App State]
  S --> C[Scoring & Fairness Logic]
  C --> R[Results & Indicators]
  UI <-->|toggle| T[Transparency: Formulas View]

Illustrates a typical SSA (single-script app) flow inferred from the code strings: inputs feed state, state drives calculations, results are rendered, and a toggle exposes a transparency page for formulas.


---

🤝 Contributing

1. Fork the repo.


2. Create a feature branch: git checkout -b feat/your-feature.


3. Commit: git commit -m "feat: add your feature".


4. Push: git push origin feat/your-feature.


5. Open a Pull Request with a clear description and screenshots/GIFs if applicable.



> Suggestions: add unit tests in a future tests/ folder, extract core logic into plain functions for easier testing, and consider breaking the single file into components if the app grows.




---

📄 Documentation

All app code and UI text are in index.html. Add a /docs folder or a Wiki for extended documentation (e.g., formula derivations, scoring policies, and moderation guidelines).


---

❤️ Acknowledgements

Branding: Rustic Kingdom.

Developer: Adham.

Producing party: Monolith Developments.



---


ℹ️ Repository Facts

Owner: Monolith Community

Default branch: main (single branch)

Tags/Releases: none yet

Issues/PRs: none open

Stars/Forks: 0 / 0 (at time of writing)

Languages: HTML 100%



---

📜 License

This project is licensed under the MIT License — see the LICENSE file for details.
