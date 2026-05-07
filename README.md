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
