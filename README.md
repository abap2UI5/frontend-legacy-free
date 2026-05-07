# frontend-v2
Frontend of abap2UI5 (legacy-free) (optional)

This frontend is bootstrapped from the new **legacy-free** distribution of
OpenUI5 (`1.142.0-legacy-free`). The legacy-free build ships without the
deprecated globals, jQuery plugins, and synchronous APIs that older UI5
applications still rely on:

- No `jQuery.sap.*` namespace and other legacy globals.
- No synchronous module loading or synchronous XHR-based APIs.
- Async bootstrap and modern module syntax (`sap.ui.define` /
  `sap.ui.require`) only.

## Why this matters – the future of UI5

The legacy-free distribution is the path SAP and the OpenUI5 community are
taking toward UI5 2.x. With UI5 2.x, all of the deprecated APIs that have
been marked for removal over the last years are finally dropped, and any
application that still depends on them will simply stop working. Customers
who keep building against the classic distribution will, sooner or later,
have to do a migration project – the legacy-free build is essentially a
preview of what that target looks like today.

By trying out this **v2** frontend, customers get a few concrete benefits:

- **Future-proof apps.** Your abap2UI5 apps already run on the API surface
  that UI5 2.x will enforce, so there is no big-bang migration ahead.
- **Smaller and faster.** The legacy-free core ships without jQuery and the
  old compatibility layers, which means a smaller download and a faster
  initial load – noticeable especially on mobile and on slow networks.
- **Cleaner foundation.** Modern async patterns, no hidden globals, fewer
  surprises in the browser console, and better alignment with current web
  standards.
- **Early feedback loop.** Issues you find now can still influence both
  abap2UI5 and the upstream UI5 roadmap, instead of being discovered after
  a forced upgrade.

In short: this version is optional today, but it is the direction the whole
UI5 ecosystem is heading. Adopting it early keeps your abap2UI5 projects
aligned with where SAP is taking the platform – with less technical debt
and a smoother ride into UI5 2.x.
