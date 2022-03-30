---
"wrangler": patch
---

fix: abort some of the fetches when we unmount the `Remote` component.
Adding abort to the `waitForPortToBeAvailable` as an option and in the `useEffect` the abort signal is called in the return which allows for graceful closing with no hanging
of the `waitForPortToBeAvailable`

fixes #375
