# Dashboards

This folder stores Home Assistant dashboard YAML exports and related diagnostics.

- `hoefijzer.yaml` is the import source for the UI-managed Hoefijzer dashboard.
- `dashboard140.yaml` is another UI-managed dashboard export.
- `energy_diagnostics.json` is the Home Assistant energy dashboard diagnostics export.

## Importing the Hoefijzer dashboard

Home Assistant dashboards registered in `configuration.yaml` with `mode: yaml`
cannot be edited in the user interface. The Hoefijzer dashboard is therefore not
registered there anymore. Import it once as a storage-mode dashboard:

1. Restart Home Assistant after deploying `configuration.yaml`.
2. Go to **Settings > Dashboards** and add a dashboard named `Hoefijzer` with
   URL `hoefijzer-dashboard` and icon `mdi:home-lightning-bolt`.
3. Open the new dashboard, choose **Edit dashboard > Raw configuration editor**,
   paste the contents of `hoefijzer.yaml`, and save.

From then on, edit the dashboard in the Home Assistant user interface. Changes
made there are stored by Home Assistant and are not written back to this YAML
export automatically.
