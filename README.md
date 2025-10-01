
# Next.js Adaptive Loading Demo (Network + Memory Hooks, Client Hints)

An example Next.js app that demonstrates adaptive loading using React Adaptive Hooks and HTTP Client Hints. The UI progressively adapts to each user’s device and network conditions by switching between low‑fidelity and high‑fidelity experiences for faster, more resilient performance.

Inspired by [Next Episode](https://www.github.com/timneutkens/next-episode).

👉 Live demo: [adaptive-loading.web.app/next-show-adaptive-loading/](https://adaptive-loading.web.app/next-show-adaptive-loading/)

This TV shows browser uses the TMDB data API and adapts rendering based on:
- Effective connection type (e.g., 2G → lo‑fi, 4G/Wi‑Fi → hi‑fi)
- Available device memory
- Client Hints provided by the browser

Built with [Next.js](https://github.com/vercel/next.js) and [React Adaptive Hooks](https://github.com/GoogleChromeLabs/react-adaptive-hooks).

## Key features

- Adaptive UI quality based on network and memory conditions
- Uses `react-adaptive-hooks` (network and memory hooks)
- Supports Client Hints for server‑side adaptation where available
- Progressive enhancement patterns for resilient UX
- Next.js app structure with demo pages and components

## How it works

The app reads device and network signals to decide whether to prioritize speed or fidelity:
- Network info via `useNetworkStatus()` from `react-adaptive-hooks` maps effective connection type to a quality tier
- Memory info via `useMemoryStatus()` detects low‑memory scenarios
- Client Hints (when sent by the browser) inform server‑side decisions in Next.js

These signals drive conditional rendering, image choices, and content density to keep the experience fast on constrained devices while delivering richer UI on capable ones.

## Getting started

```
git clone https://api.glitch.com/git/anton-karlovskiy-next-show-adaptive-loading
cd next-show-adaptive-loading-prototype
npm install

# Start development server
npm run dev

# Production build and run
npm run build
npm start
```

> Note: This project targets Next.js 9.x for demo purposes and may use legacy APIs. For modern Next.js projects, adapt the concepts to your current version.

## Scripts

- `npm run dev`: Start the Next.js dev server
- `npm run build`: Build for production
- `npm start`: Start the production server
- `npm run deploy`: Deploy to Firebase (copies `build` to `functions/` and runs `firebase deploy`)

## Tech stack

- Next.js 9.x, React 16.x
- `react-adaptive-hooks` for network and memory status
- Express (custom server)
- Firebase Hosting + Cloud Functions (optional deploy target)

## Related resources

- [React Adaptive Loading Hooks & Utilities](https://github.com/GoogleChromeLabs/react-adaptive-hooks)
- [Adaptive Loading demos](https://github.com/GoogleChromeLabs/adaptive-loading)
- [Adaptive Loading microsite](https://adaptive-loading.web.app/)

## Code reference

See how adaptive signals are used in the app:  
`utils/hooks.js` on Glitch: https://glitch.com/edit/#!/anton-karlovskiy-next-show-adaptive-loading?path=utils/hooks.js:26:102

## Glitch source

- App: https://anton-karlovskiy-next-show-adaptive-loading.glitch.me/
- Project: https://glitch.com/~anton-karlovskiy-next-show-adaptive-loading/

## SEO keywords

Next.js adaptive loading, React Adaptive Hooks, Client Hints, effective connection type, network information, device memory, progressive enhancement, performance optimization, resilient UX, TMDB demo, low‑fidelity high‑fidelity rendering, slow network optimization, memory‑aware UI, Next.js performance demo
