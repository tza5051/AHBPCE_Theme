# AHBPCE Theme Usage Guide

## Installation

### Method 1: Direct from GitHub (Recommended)
```bash
# In your Quarto project folder
quarto add tza5051/AHBPCE_Theme
```

### Method 2: From Local Clone
```bash
# If you have the repo cloned locally
quarto add /path/to/AHBPCE_Theme
```

## Using the Theme

### In your `.qmd` files:

#### For Project Reports (full-featured):
```yaml
---
title: "My Analysis Report"
subtitle: "Quarterly Data Review"
author: "Your Name"
date: today
format: va-lab-html
---
```

#### For Single-File Reports (compact):
```yaml
---
title: "Quick Analysis"
author: "Your Name" 
date: today
format: va-lab-html-single
---
```

## Rendering

```bash
# Preview while working
quarto preview MyReport.qmd

# Render final version
quarto render MyReport.qmd
```

## Updating the Theme

When the theme is updated, team members can update their local copy:

```bash
# In your project folder
quarto remove tza5051/AHBPCE_Theme
quarto add tza5051/AHBPCE_Theme
```

## Team Best Practices

### 1. Consistent Front Matter
Always include these fields:
```yaml
---
title: "Descriptive Title"
subtitle: "Brief description" # optional
author: "First Last"
date: today # or specific date like "2024-03-15"
format: va-lab-html # or va-lab-html-single
execute:
  echo: false # hide code by default
  warning: false # hide warnings
---
```

### 2. Document Structure
Use consistent heading structure:
- `#` for main sections
- `##` for subsections  
- `###` for sub-subsections

### 3. Code Chunks
Use descriptive chunk labels:
```{r}
#| label: data-import
#| echo: false

# Your code here
```

### 4. Version Control Integration
- Keep `.qmd` files in your project repo
- Render and commit both `.qmd` and `.html` files
- Theme updates are automatically pulled when someone re-installs

## Troubleshooting

### Theme not updating?
```bash
quarto remove tza5051/AHBPCE_Theme
quarto add tza5051/AHBPCE_Theme
```

### Missing dependencies?
Make sure you have the latest Quarto version:
```bash
quarto --version  # should be >= 1.4.0
```

### Custom styling needed?
Add custom CSS in your document:
```yaml
---
format:
  va-lab-html:
    css: custom.css
---
```