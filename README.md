# Raju — Developer Portfolio

A responsive, GitHub-inspired portfolio for Raju, a BCA (AI & ML) student exploring software engineering, machine learning, and agentic AI.

## Architecture

- `index.html` is the complete static site: semantic page structure, responsive CSS, and a small JavaScript layer for navigation and profile data.
- No build step, framework, backend service, or API secret is required.
- The site remains compatible with GitHub Pages at `https://rajukumar975747-art.github.io/My_potfolio/`.

## Live GitHub data

The page requests the public GitHub profile and public repositories from the unauthenticated GitHub REST API. It shows public repository count, stars across public repositories, and repository languages. The responses are cached in `localStorage` for 30 minutes, with a cached-data fallback and visible error state for rate limits or network failures. No access token is included in the page.

Contribution history is fetched from the public GitHub Contributions API (which reads GitHub's public contribution graph); the page derives the total, current streak, longest streak, and draws the activity graph locally. Its upstream API caches responses for an hour. Commit / pull request / issue totals are displayed by GitHub Stats Extended. That external image service may be unavailable or rate-limited independently of the portfolio.

## Content and links

The LinkedIn URL is retained from the existing portfolio. Project repository buttons are omitted where a public repository could not be verified. Resume download is not yet enabled because the resume PDF was not included with the available request attachments; provide the PDF and place it in this repository to add a working download.

## Deploy

Push the branch to GitHub and merge it into `main`, or publish the branch using GitHub Pages settings. For the existing project URL, keep Pages configured to deploy from the `main` branch and repository root. The site uses no build command.
