# 🧼 Stylelint Configuration

This folder contains my personal configuration for [Stylelint](https://stylelint.io/) tailored for SCSS projects that may also include [Tailwind CSS](https://tailwindcss.com/).

---

## 📦 Dependencies

To use this configuration, install the following packages:

```
npm install --save-dev stylelint stylelint-config-standard-scss stylelint-order postcss-scss
```

## ⚙️ About This Config

**File:** `.stylelintrc.json`

Key features:

- Uses postcss-scss for SCSS support.
- Extends stylelint-config-standard-scss.
- Includes stylelint-order for organizing CSS properties.
- Ignores compiled or utility CSS files (like Tailwind output and Live Sass generated files).

## 🚀 Usage

Copy the `.stylelintrc.json` file to the root of your project.

To lint your files:

```
npx stylelint 'assets/scss/**/*.scss'
```

## 🔁 Property Order

This config enforces a logical CSS property order, focusing on layout first (flex/grid), followed by box model, typography, background, effects, and interaction.

Example (simplified):

```
display: flex;
align-items: center;
position: relative;
margin: 1rem;
padding: 2rem;
font-size: 1rem;
background-color: #f9f9f9;
transition: all 0.3s ease;
```

## 🛠 Tools Used
> ⚠️ Note: This config is designed to work alongside the following tools:

- Live Sass Compiler (VS Code) – Compiles SCSS to CSS locally.
- Tailwind CSS CLI – Generates utility CSS files via CLI.

Because of these tools, the following folders are ignored in linting:

```
"ignoreFiles": [
  "assets/css/**/*.css",
  "assets/tailwindcss/*.css"
]
```

## 🧾 Notes

- Tailwind-generated files (assets/tailwindcss/*.css) and compiled SCSS (assets/css/**/*.css) are intentionally ignored.
- Some default rules are disabled to better fit real-world SCSS and Tailwind projects.

## 📁 Files

`.stylelintrc.json` – Main config
`README.md` – This file