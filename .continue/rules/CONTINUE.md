# CONTINUE.md - Vigocan™ Project Guide

## 1. Project Overview
- **Description**: The official web presence and manifest repository for **Vigocan™**, a futuristic philosophical-mathematical concept/protocol blending quantum aesthetics, fractal time scaling, and mythopoetic lore ("Iteration Zero").
- **Key Technologies**:
  - HTML5 / CSS3 (Vanilla frontend with inline styles, custom SVG graphics, and responsive design)
  - JavaScript (Client-side language switcher with `localStorage` persistence and browser locale detection)
  - Cloudflare Workers / Static Assets (Configured via `wrangler.jsonc` for high-performance edge deployment)
- **High-level Architecture**: 
  - A static single-page application hosted at the edge via Cloudflare Workers assets.
  - Dual-language support (Polish and English) rendered dynamically in the DOM via client script.

## 2. Getting Started
### Prerequisites
- Node.js & npm (for managing Cloudflare Wrangler CLI if deploying/testing locally)
- Wrangler CLI (`npm install -g wrangler`)

### Installation & Local Development
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd vigocan.com
   ```
2. Test/Preview locally using Wrangler:
   ```bash
   wrangler dev
   ```
   This will spin up a local development server serving the static assets from `src/`.

### Basic Usage Examples
- Open `src/index.html` directly in any web browser to view the protocol manifesto.
- Toggle between Polish (`PL`) and English (`EN`) using the top-right navigation buttons.

### Running Tests
- *Note*: There are currently no automated unit or integration test suites configured in this repository. Testing is done manually via browser preview and Wrangler dev server.

## 3. Project Structure
```text
├── .continue/            # Continue AI configuration and rules
├── src/                  # Source files served by Cloudflare Assets
│   └── index.html        # Single-page frontend containing styles, SVGs, and text
├── README.md             # Project README
├── wrangler.jsonc        # Cloudflare Workers configuration file
├── vigocan_neon-glow_logotype.css # Additional design asset / stylesheet
└── vigocan_sygnet_logotype.svg    # Brand vector graphic asset
```

### Key Files and Roles
- **`src/index.html`**: The core entry point containing all styles, SVG sygnet graphics, Polish/English sections, and language switching logic.
- **`wrangler.jsonc`**: Cloudflare Workers deployment and routing config (`vigocan.com`).
- **`vigocan_neon-glow_logotype.css` & `vigocan_sygnet_logotype.svg`**: Standalone brand identity assets.

## 4. Development Workflow
- **Coding Standards**: Keep HTML clean, semantic, and self-contained within `src/` or modularized as design system assets. Maintain modern CSS custom properties (`:root`).
- **Deployment**: Deployed via Cloudflare Workers assets. Run production deployment using:
  ```bash
  wrangler deploy
  ```
- **Contribution Guidelines**: Ensure all additions respect the quantum-aesthetic branding, responsiveness, and multi-language requirements.

## 5. Key Concepts
- **Vigocan™ Protocol**: A mythopoetic model of reality ("Iteration Zero") involving *Wig* (pure vector of potential energy) and *Can* (stable geometric matrix).
- **Fractal Time**: Time modeled as self-similar iterations rather than a linear timeline.
- **Quantum Breath**: Key CSS keyframe animation (`quantumBreath`) applied to the SVG brand logotype representing energetic resonance.

## 6. Common Tasks
### Adding a New Language or Content Section
1. Open `src/index.html`.
2. Add a new `.lang-section` div with an appropriate ID (e.g., `lang-es`).
3. Add a corresponding language button in `.lang-switcher`:
   ```html
   <button class="lang-btn" id="btn-es" onclick="setLanguage('es')">ES</button>
   ```
4. Test locally with `wrangler dev`.

## 7. Troubleshooting
- **Assets Not Updating in Dev**: Ensure Wrangler is pointing correctly to `./src` as defined in `wrangler.jsonc`.
- **Styling Overrides**: Check both inline `<style>` tags in `src/index.html` and external stylesheets (`vigocan_neon-glow_logotype.css`).

## 8. References
- [Cloudflare Workers Documentation](https://developers.cloudflare.com/workers/)
- [Wrangler Configuration Reference](https://developers.cloudflare.com/workers/wrangler/configuration/)
