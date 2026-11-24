<div align="center">

<img src="https://raw.githubusercontent.com/Studio1HQ/Studio1HQ/main/assets/banners/velt-auth0.webp" alt="Velt Comments with Auth0: Figma-style comments, live cursors and presence with Auth0 login" width="100%" />

<br />
<br />

# Velt Comments with Auth0

### Figma-style comments, live cursors and presence with Auth0 login

A React and Vite app that identifies Auth0 users in Velt. It adds Figma-style comments, live cursors and presence to a small dashboard.

<br />

[![Built by Studio1](https://img.shields.io/badge/Built_by_Studio1-f97316?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxNjAgMTYwIiBmaWxsPSJub25lIj48cGF0aCBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTAgMzVDMCAxNi42ODA3IDE0LjA3NDQgMS42NDg0NCAzMiAwLjEyNjk1M1YxNDFINTEuMDUyM0M1Mi40MzA4IDEzNy4zNDQgNTQuNzQ0NiAxMzMuNjg5IDU3Ljk5MzggMTMwLjAzM0M2MS4xNDQ2IDEyNi41MDggNjQuNjg5MiAxMjMuNDQgNjguNjI3NyAxMjAuODI5QzcyLjU2NjIgMTE4LjM0OSA3Ni4zNTY5IDExNi43ODIgODAgMTE2LjEyOVY4Ni43NTQ0Qzc1LjQ3MDggODcuOTI5MiA3MS4zODQ2IDg5LjY5MTkgNjcuNzQxNSA5Mi4wNDE1QzY0IDk0LjUyMjUgNjAuNzUwOCA5Ny40NiA1Ny45OTM4IDEwMC44NTRDNTYuNTM0NSAxMDIuNzIgNTUuMjU0NSAxMDQuNjU5IDU0LjE1MzkgMTA2LjY3MVYwSDEyNUMxNDQuMzMgMCAxNjAgMTUuNjY5OSAxNjAgMzVWMTI1QzE2MCAxNDQuMzMgMTQ0LjMzIDE2MCAxMjUgMTYwSDEyNFYxOEgxMDQuOTQ4QzEwMy41NjkgMjEuNjgxNiAxMDEuMjU1IDI1LjM2MjggOTguMDA2MiAyOS4wNDQ0Qzk0Ljg1NTQgMzIuNTk0MiA5MS4zMTA4IDM1LjY4NDEgODcuMzcyMyAzOC4zMTRDODMuNDMzOCA0MC44MTIgNzkuNjQzMSA0Mi4zODk2IDc2IDQzLjA0NzRWNzIuNjMwNEM4MC41MjkyIDcxLjQ0NzMgODQuNjE1NCA2OS42NzI0IDg4LjI1ODUgNjcuMzA1N0M5MiA2NC44MDc2IDk1LjI0OTIgNjEuODQ5MSA5OC4wMDYyIDU4LjQzMDdDOTkuNDY1NSA1Ni41NTEzIDEwMC43NDUgNTQuNTk4NiAxMDEuODQ2IDUyLjU3MjNWMTYwSDM1QzE1LjY3IDE2MCAwIDE0NC4zMyAwIDEyNVYzNVoiIGZpbGw9IiNmZmZmZmYiLz48L3N2Zz4K)](https://studio1hq.com)
[![Built with Velt](https://img.shields.io/badge/Built_with_Velt-141414?style=for-the-badge)](https://velt.dev)
[![Live demo](https://img.shields.io/badge/Live_demo-1c1917?style=for-the-badge&logo=vercel&logoColor=white)](https://velt-auth0.vercel.app)
[![Watch on YouTube](https://img.shields.io/badge/Watch_on_YouTube-ff0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtu.be/_-nZDj-y8Yw?si=ewExjiKHcSx3mn2G)

[Velt docs](https://docs.velt.dev) &nbsp;·&nbsp; [Velt](https://velt.dev) &nbsp;·&nbsp; [More examples](https://github.com/Studio1HQ) &nbsp;·&nbsp; [studio1hq.com](https://studio1hq.com)

</div>

<br />

## Overview

This is a small React app that adds real-time collaboration to an Auth0-protected dashboard with [Velt](https://velt.dev). Auth0 handles login. Velt handles the collaboration layer: comments, live cursors and presence.

The Auth0 user is passed to Velt with `useIdentify`, so every comment, cursor and avatar carries the logged-in user's name, email and photo. A video walkthrough is on [YouTube](https://youtu.be/_-nZDj-y8Yw?si=ewExjiKHcSx3mn2G), and the repo includes `public/demo.webm`.

## Features

- **Auth0 login**: Login and logout through the Auth0 React SDK.
- **User identity in Velt**: `useIdentify` maps the Auth0 profile to the Velt user.
- **Comments**: `VeltComments` in popover mode, with comment threads tied to elements on the page such as cards and buttons.
- **Live cursors**: `VeltCursor` shows teammates' cursors in real time.
- **Presence**: `VeltPresence` shows who is online, with avatars and names.
- **Document setup**: `useSetDocument` scopes comments to the dashboard document.

## Tech stack

| Layer | Tool |
| --- | --- |
| Framework | [React](https://react.dev) with [Vite](https://vitejs.dev) and TypeScript |
| Routing | [TanStack Router](https://tanstack.com/router) |
| Auth | [Auth0](https://auth0.com) (`@auth0/auth0-react`) |
| Collaboration | [Velt](https://velt.dev) (`@veltdev/react`) |
| Styling | [Tailwind CSS](https://tailwindcss.com) |
| Charts | [Chart.js](https://www.chartjs.org) |
| Deployment | [Vercel](https://vercel.com) |

## Getting started

### Prerequisites

- Node.js 18 or later
- npm or yarn
- A Velt account ([velt.dev](https://velt.dev)) and API key from the [Velt console](https://console.velt.dev)
- An Auth0 tenant ([auth0.com](https://auth0.com)) with a single page application

### Installation

```bash
git clone https://github.com/Studio1HQ/velt-auth0.git
cd velt-auth0
npm install
```

### Environment variables

Create a `.env.local` file in the project root.

| Variable | Description |
| --- | --- |
| `VITE_VELT_API_KEY` | Velt API key from the Velt console. |
| `VITE_AUTH0_DOMAIN` | Your Auth0 tenant domain. |
| `VITE_AUTH0_CLIENT_ID` | Client ID of your Auth0 application. |

### Run

```bash
npm run dev
```

Open `http://localhost:5173`. Other scripts: `npm run build`, `npm run preview`, `npm run lint`.

## How it works

```text
src/
├── components/
│   ├── layout.tsx           VeltProvider and VeltComments
│   └── shared/header.tsx    Auth0 login, useIdentify, VeltPresence, VeltCursor
├── routes/                  root, index and dashboard routes (dashboard calls useSetDocument)
├── main.tsx                 Auth0Provider setup
└── lib/utils.ts
```

- `main.tsx` wraps the app in `Auth0Provider` with your domain and client ID.
- `layout.tsx` wraps the app in `VeltProvider` with the Velt API key.
- `header.tsx` reads the user from `useAuth0()` and calls `useIdentify` with the user ID, name, email and photo.
- Toggle comments, leave a comment on a page element, and open the app in a second browser to see cursors, avatars and threads sync instantly.

## Resources

- [Demo video on YouTube](https://youtu.be/_-nZDj-y8Yw?si=ewExjiKHcSx3mn2G): walkthrough of the app.
- [Live demo](https://velt-auth0.vercel.app): the deployed app.
- [Velt documentation](https://docs.velt.dev): SDK guides.
- [Velt](https://velt.dev): product site.
- [Auth0 React SDK quickstart](https://auth0.com/docs/quickstart/spa/react): Auth0 setup.

<br />

---

<div align="center">

<a href="https://studio1hq.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-dark.svg" />
    <img src="https://raw.githubusercontent.com/Studio1HQ/website/main/brand/studio1-logo-on-light.svg" alt="Studio1" width="160" />
  </picture>
</a>

Built by **[Studio1](https://studio1hq.com)**, the technical content and DevRel partner for devtool teams. Made with [Velt](https://velt.dev).<br />
Browse more open-source examples at [github.com/Studio1HQ](https://github.com/Studio1HQ).

[![Website](https://img.shields.io/badge/studio1hq.com-0b0807?style=for-the-badge&logo=googlechrome&logoColor=white)](https://studio1hq.com)
[![Book a call](https://img.shields.io/badge/Book_a_strategy_call-f97316?style=for-the-badge&logo=googlecalendar&logoColor=white)](https://cal.com/studio1/collab)
[![X](https://img.shields.io/badge/%40Studio1HQ-141414?style=for-the-badge&logo=x&logoColor=white)](https://x.com/Studio1HQ)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0a66c2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/company/studio1hq/)

<sub><a href="https://studio1hq.com">studio1hq.com</a> · Technical content, docs, video and DevRel for devtools</sub>

</div>
