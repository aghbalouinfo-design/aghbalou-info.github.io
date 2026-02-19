# GEMINI.md - Info-Aghbalou Project Context

## Project Overview
**Info-Aghbalou** (also known as "Hub Pédagogique Informatique") is a static website platform designed for educational purposes, specifically for teaching Information Technology. It serves as a centralized hub for students to access lessons, resources, and interactive activities, and for teachers to utilize classroom management tools.

The project is structured as a Single-Page Application (SPA) in its main entry point, using JavaScript to dynamically inject content into a core layout.

### Main Technologies
- **Frontend:** HTML5, CSS3, JavaScript (Vanilla).
- **Styling:** [Tailwind CSS](https://tailwindcss.com/) (loaded via CDN).
- **Interactive Tools:** Custom JS-based components (timers, pickers, mind maps).
- **Deployment:** GitHub Pages (configured via `CNAME` for `aghbalou-info.github.io`).

---

## Directory Structure
- `/`: Core application files and individual lesson/tool HTML pages.
- `/app/`: Additional application entry point (wrapper for Google Script).
- `/dashmangement/`: Teacher-specific tools (Dashboard, Timer, Student Picker).
- `/Images/`: Educational diagrams, icons, and pedagogical assets.

---

## Key Files
- `index.html`: The main entry point. It contains the navigation logic and a large `lessonData` object that stores the content for multiple modules and lessons.
- `LECON1.html`: A representative lesson page (Information, Treatment, and IT).
- `dashmangement/dash.html`: A teacher dashboard featuring a classroom countdown timer and a random student picker.
- `Mindmap.html`: Interactive mind map component.
- `timer.html` & `timer-style.html`: Specialized countdown timer implementations.
- `CNAME`: Configuration for GitHub Pages custom domain.

---

## Development Conventions
- **Static First:** The project relies on static HTML/JS/CSS. There is no backend server; data is either hardcoded in JS objects or fetched from external scripts/Google Scripts.
- **SPA Pattern:** `index.html` uses a `navigateTo(view)` function to swap content within the `#page-content-container` without reloading the page.
- **Styling:** Consistent use of Tailwind CSS classes for layout and styling. Custom CSS is embedded within `<style>` tags in HTML files.
- **Language:** The primary content language is French.

---

## Usage & Deployment
- **Local Development:** Simply open `index.html` in any modern web browser. No build step is required.
- **Deployment:** Push changes to the `main` branch of the GitHub repository. GitHub Pages will automatically serve the content at `https://aghbalou-info.github.io/`.
- **Management:** Teacher tools can be accessed via `dashmangement/dash.html`.

---

## TODO / Future Improvements
- [ ] Refactor `lessonData` from `index.html` into external JSON files for easier maintenance.
- [ ] Consolidate redundant CSS/JS across multiple timer-related files.
- [ ] Implement a proper build system (e.g., Vite) if the project grows in complexity.
