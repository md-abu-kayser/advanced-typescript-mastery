# Advanced TypeScript Mastery - Focused Problem and Production-minded Solution

<!-- MIT License -->

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](./LICENSE)

<!-- Demo Live Link -->

[![Demo](https://img.shields.io/badge/demo-GitHub%20Pages-brightgreen)](https://md-abu-kayser.github.io/advanced-typescript-mastery/)

<!-- HTML & CSS -->

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5\&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3\&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

<!-- Styling / PostCSS -->

[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/docs/)
[![PostCSS](https://img.shields.io/badge/PostCSS-efefef?logo=postcss&logoColor=black)](https://postcss.org/)
[![daisyUI](https://img.shields.io/badge/daisyUI-5A0EF8?logo=tailwindcss&logoColor=white)](https://daisyui.com/)

<!-- Fonts & Icons -->

[![Google Fonts](https://img.shields.io/badge/Google_Fonts-4285F4?logo=google&logoColor=white)](https://fonts.google.com/)
[![Font Awesome](https://img.shields.io/badge/Font_Awesome-528DD7?logo=fontawesome&logoColor=white)](https://fontawesome.com/)
[![Heroicons](https://img.shields.io/badge/Heroicons-0EA5E9?logo=heroicons&logoColor=white)](https://heroicons.com/)

<!-- Languages & Web Standards -->

[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![ECMAScript Spec](https://img.shields.io/badge/ECMAScript-262-7A0BC0?logo=ecmascript&logoColor=white)](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178c6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/docs/)

## Plain docs links

- HTML (MDN) docs: https://developer.mozilla.org/en-US/docs/Web/HTML
- CSS (MDN) docs: https://developer.mozilla.org/en-US/docs/Web/CSS
- Tailwind CSS docs: https://tailwindcss.com/docs/
- PostCSS docs / postcss.config: https://postcss.org/ (see also Tailwind PostCSS install guide)
- daisyUI docs: https://daisyui.com/
- Google Fonts docs: https://fonts.google.com/
- Font Awesome docs: https://fontawesome.com/
- Heroicons docs: https://heroicons.com/
- Node.js docs: https://nodejs.org/
- Express docs: https://expressjs.com/
- JavaScript (MDN) docs: https://developer.mozilla.org/en-US/docs/Web/JavaScript
- ECMAScript (spec, ECMA-262) docs: https://www.ecma-international.org/publications-and-standards/standards/ecma-262/
- TypeScript docs: https://www.typescriptlang.org/docs/

---

Professional, well-documented repository containing a focused TypeScript demonstration and exercise designed to showcase advanced TypeScript techniques, problem-solving skill, and clean project structure.

> Clear, concise, and practical - ideal for technical interviews, portfolio showcases, or client demonstrations.

---

## Table of Contents

- [About](#about)
- [Highlights](#highlights)
- [Repository Structure](#repository-structure)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
- [Running the Example](#running-the-example)
- [How to Read the Code](#how-to-read-the-code)
- [Recommended Development Workflow](#recommended-development-workflow)
- [Testing and Validation](#testing--validation)
- [Contributing](#contributing)
- [License](#license)
- [Contact / Maintainer](#contact--maintainer)

---

## About

This repository contains a single, focused TypeScript exercise and a minimal web runner. The goal is to demonstrate advanced TypeScript patterns, correctness, and readability in a compact, production-minded example.

The project is deliberately small so reviewers can quickly inspect architecture, types, and algorithms while still seeing professional-level documentation and usage guidance.

## Highlights

- Single-file advanced TypeScript problem: `100-advanced-ts-problem.ts` - contains the primary implementation and inline examples.
- Minimal web runner: `index.html` - lets reviewers open the solution in a browser quickly.
- Clean, intention-revealing types and comments suitable for code review or client presentation.

## Repository Structure

**Top-level files you will find:**

- `100-advanced-ts-problem.ts` - The main TypeScript source showing the advanced problem and its solution.
- `index.html` - Simple web page that can load a compiled JS bundle or demonstrate the output for quick manual inspection.
- `README.md` - this file --> professional project overview and usage instructions.

If you expand this repository into a fuller project, recommended additions include a `package.json`, a `tsconfig.json`, unit tests under a `tests/` folder, and CI configuration --> GitHub Actions.

## Prerequisites

**You only need one of these to run or preview the project locally:**

- Node.js (LTS) with npm (recommended for a development workflow)
- A TypeScript toolchain (tsc, ts-node, or esbuild) OR a modern browser for running built JS

**Optional global utilities used in the examples below (you can also use npx):**

- `http-server` (for quick local static hosting)

## Quick Start

There are two quick ways to preview the project locally: using Node/TypeScript tooling, or using a static file preview.

1. **Using ts-node (one-shot execution of the TypeScript file):**

```powershell
npm i -g ts-node typescript
```

```
npx ts-node 100-advanced-ts-problem.ts
```

2. Compile to JavaScript and open `index.html` in the browser:

```powershell
npx tsc --init --rootDir . --outDir dist --esModuleInterop --resolveJsonModule --lib es2020,dom --target es2020
npx tsc 100-advanced-ts-problem.ts --outDir dist
npx http-server -p 8080 -c-1
```

3. Open `index.html` directly in the browser (works if the page only relies on included JS/CSS and not on server-only APIs).

4. **git repo clone:**

```
git clone https://github.com/md-abu-kayser/advanced-typescript-mastery.git
```

## Running the Example

The repository is intentionally minimal. The file `100-advanced-ts-problem.ts` contains both the implementation and a small example harness. Running it with `ts-node` prints sample output to the console. Compiling with `tsc` and opening `index.html` shows the result in a browser context.

**Example expected behavior--> summary:**

- The TypeScript file demonstrates advanced typing patterns and a complete solution for the included problem.
- Example input and expected output are included in comments and in the file's sample runner function.

**Note:** Because this repository doesn't include a `package.json` by default, the Quick Start uses `npx` so reviewers can run things without modifying the repo.

## How to Read the Code

**When reviewing `100-advanced-ts-problem.ts`, look for the following:**

- Top-level type contracts describing function inputs and outputs.
- Small, well-named helper functions with single responsibilities.
- Inline comments that explain non-obvious algorithmic choices.
- A testable, decoupled `solve` (or equivalent) function that can be imported by a test harness.

If you would like, I can split the file into modules (e.g., `src/` + `lib/`) and add a `package.json` with scripts for build/test in a follow-up.

## Recommended Development Workflow

- **Add a `package.json` and dependencies:**

```powershell
npm init -y
npm i -D typescript ts-node @types/node
```

- Add a `tsconfig.json` (basic one can be created with `npx tsc --init`).
- **Add npm scripts to `package.json`:**

```json
{
  "scripts": {
    "build": "tsc",
    "start": "ts-node 100-advanced-ts-problem.ts",
    "serve": "http-server -p 8080"
  }
}
```

**These scripts standardize common tasks and make the repo friendlier to evaluators.**

## Testing and Validation

This repository is small and doesn't include a test runner by default. To add tests quickly, use Jest or Vitest.

**Example installation (Vitest):**

```powershell
npm i -D vitest @types/jest
npx vitest init
```

Write a few unit tests that import the primary exported `solve` function from `100-advanced-ts-problem.ts` and validate the example cases.

### Contributing

**Contributions are welcome. Suggested steps for a clean contribution:**

1. Fork the repository.
2. Create a topic branch for your change.
3. Add tests for any new behavior.
4. Ensure linting and type checks pass.
5. Open a pull request describing your change.

For small portfolio edits (formatting, README improvements), a direct PR is fine.

### Suggested Follow-ups (for an even stronger presentation)

- Add `package.json` with `build`, `start`, and `test` scripts.
- Add `tsconfig.json` and a basic ESLint/Prettier setup.
- Add a simple GitHub Actions workflow that runs `npm ci andand npm test` on push.
- Add a small demo GIF or screenshot showing expected output.

I can implement any of these follow-ups on request.

### License

- This project is licensed under the terms of the **[MIT License](./LICENSE)**.
- The license may be modified or replaced for client or proprietary projects if required.

---

### Contact & Maintainer

**Md Abu Kayser**  
Frontend / Full-Stack Web Developer

- **Project:** Advanced TypeScript Mastery
- **GitHub:** https://github.com/md-abu-kayser
- **Email:** abu.kayser.official@gmail.com

For inquiries related to collaboration, interviews, or client work, feel free to reach out via email or GitHub.

---

**Thank you for reviewing this project!**  
It is designed to be **clean, well-structured**, and **easy to evaluate** - ideal for technical interviews, portfolio reviews, and professional demonstrations.

---
