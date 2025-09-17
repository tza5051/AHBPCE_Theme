# AHBPCE Theme (Quarto Extension)

This repo exposes two formats:

- `va-lab-html` — for project reports
- `va-lab-html-single` — for single-file reports

## Use in any folder

Install once per folder/project:

```bash
quarto add tza5051/AHBPCE_Theme
```

Then in your `.qmd`:

```yaml
format: va-lab-html            # or va-lab-html-single
```

Render with `quarto preview MyReport.qmd`.
