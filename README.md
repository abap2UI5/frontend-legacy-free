# frontend-v2
Frontend of abap2UI5 (legacy-free) (optional)

## Bootstrapping

The UI5 runtime is loaded in `src/z2ui5_v2.wapa.index.html` via the standard
`sap-ui-bootstrap` script tag:

```html
<script
    id="sap-ui-bootstrap"
    src="https://sdk.openui5.org/1.142.0-legacy-free/resources/sap-ui-core.js"
    data-sap-ui-theme="sap_horizon"
    data-sap-ui-async="true"
    data-sap-ui-compat-version="edge"
    data-sap-ui-libs="sap.m"
    data-sap-ui-resource-roots='{"app_v2": "./", "z2ui5": "./cc/"}'
    data-sap-ui-frame-options="trusted"
    data-sap-ui-on-init="module:sap/ui/core/ComponentSupport"
></script>
```

Key points:

- The bootstrap loads `sap-ui-core.js` from the OpenUI5 CDN.
- Resource roots map `app_v2` to the app folder and `z2ui5` to the `cc/`
  folder, where the custom controls and runtime modules live.
- The component is started declaratively via `ComponentSupport` from the
  `<div data-sap-ui-component ...>` placeholder in the body.

## Legacy-free

This frontend targets the **legacy-free** distribution of OpenUI5
(`1.142.0-legacy-free`). The legacy-free build of UI5 ships without the
deprecated globals, jQuery plugins, and synchronous APIs that older UI5
applications still rely on. Compared to the regular distribution, it:

- Removes the global `jQuery.sap.*` namespace and other legacy globals.
- Drops synchronous module loading and synchronous XHR-based APIs.
- Requires async bootstrap (`data-sap-ui-async="true"`) and modern module
  syntax (`sap.ui.define` / `sap.ui.require`).

All custom controls and runtime code under `src/` are written against this
modern API surface, which is why this frontend is published as a separate
"v2" repository alongside the original abap2UI5 frontend.
