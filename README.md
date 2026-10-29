# ClinixPro by RYDE Labs: online demo

Static HTML build of ClinixPro: the clinic workspace (appointments, patient records, dental chart,
prescriptions, inventory, billing, reminders, patient portal) and the public "Find a doctor" site.

There is no server. Each visitor's data is saved only in their own browser (localStorage).
"Find a doctor" also looks up real clinics near the chosen place from OpenStreetMap.

## Pages
- `#/welcome`: ClinixPro home (patients and clinics)
- `#/find`: find a doctor on the map
- `/<clinic-name>` (for example `/relief-dental`): a clinic's own page
- `#/login`: sign-in. Platform admin `admin@clinixpro.com`; the demo clinic has one-click accounts (password `demo1234`)
- `#/platform`: platform admin, where clinics are added
- `#/clinic-admin`: a clinic's admin page; `#/inventory`: its stock room

## Publish on GitHub Pages
1. Create a new repository on GitHub (for example `clinixpro`).
2. Upload **everything in this folder** (including the hidden `.nojekyll` file) to the repository root.
3. In the repository, open **Settings → Pages**, set **Source** to *Deploy from a branch*,
   pick branch `main` and folder `/ (root)`, then **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

Clinic addresses such as `/relief-dental` work because GitHub Pages serves `404.html` (a copy of the app) for unknown
paths, and the app forwards them to `#/relief-dental`. With a custom domain the address is `clinixpro.com/relief-dental`.
Any static host that serves `404.html` for unknown paths works the same way.
