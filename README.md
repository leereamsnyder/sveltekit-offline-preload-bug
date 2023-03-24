# sveltekit-offline-preload-bug

This repo documents a bug that happens in extremely adverse network conditions when the root layout has a server `load()`.

1. npm install
1. npm run dev
1. Open up http://localhost:5173 in Chrome (this is most straightforward in Chrome)
1. In the command palette (CMD + SHIFT + P), choose **Go Offline**
1. Hover over the **Sverdle** link in the nav. In a flash, SvelteKit will do a hard navigation to`http://localhost:5173/sverdle`, which will fail because you're offline
