# AgentHub Admin Panel — Specification

## Product description

AgentHub is a SaaS platform where companies rent AI agents and attach skills to them. This project is the **internal admin panel** that AgentHub's own staff use to run the platform day to day.

The admin panel is for AgentHub employees only. It is **not** customer-facing. Staff use it to look after the three things the business is built on:

- **Customers** — the companies that rent agents from AgentHub.
- **Agents** — the AI agents in the catalogue that customers can rent.
- **Skills** — the capabilities that can be attached to an agent.

The goal of this first version is a clear, single-page internal tool that lets staff see this information at a glance and move between the main areas quickly. It is a prototype built with hardcoded data, so the focus is on layout, navigation and readable screens rather than live functionality.

## Tech stack and constraints

The whole panel is a single static page. These rules are fixed and apply to every commit:

### Files

- **One `index.html` file** at the root of the repo. All markup, styling classes and scripts live in this one file.
- **No CSS file of my own.** No `styles.css` or any other stylesheet is created or linked.
- **No `style` attributes.** All visual styling is done with Tailwind utility classes on elements.

### Styling

- **Tailwind CSS from the CDN**, loaded with a `<script>` tag in the `<head>`. No local install of Tailwind.
- No other CSS libraries or icon packs that require a build step.

### Scripting

- **Vanilla JavaScript only**, written inside `index.html` in a `<script>` tag.
- **No frameworks or libraries**: no React, Vue, Alpine, jQuery or similar.
- **No build step**: no bundler, no transpiler, no npm scripts. The page must work by opening `index.html` directly in a browser or serving it with a simple static server.

### Data

- **All data is hardcoded** in the JavaScript inside `index.html`.
- **No API calls and no backend.** Nothing is fetched over the network and nothing is persisted. Reloading the page resets everything to the hardcoded state.

### Running it

- Serve the folder with any static server, for example the included `server.py`, or open `index.html` straight from the file system. Both must work with no extra setup.
