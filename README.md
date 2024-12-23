# Next.js 15 Page Component Error

This repository demonstrates a common error encountered when upgrading to Next.js 15: an invalid return type in a page component.  Next.js 15 enforces stricter React component rules, causing errors if a page component returns a plain HTML element instead of a valid JSX element.

## Bug

The `pages/about.js` file returns a simple `<p>` tag directly.  This violates Next.js 15's stricter rules, resulting in a runtime error.  The `pages/index.js` file serves as a working example that utilizes a valid JSX element. 

## Solution

The solution involves wrapping the plain HTML element in a React Fragment (`<>`) or a valid React component like a `div`.  The corrected `pages/about.js` file demonstrates this fix.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the error when navigating to `/about`.
5. Modify `pages/about.js` per the solution provided.
6. Re-run `npm run dev` and verify the error is resolved.

## Additional Notes

This error highlights the importance of properly structuring your React components in Next.js 15. Always ensure your page components return valid React elements. This may involve refactoring older code that uses plain HTML elements. 