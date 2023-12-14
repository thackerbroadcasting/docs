[![pages-build-deployment](https://github.com/thackerbroadcasting/docs/actions/workflows/pages/pages-build-deployment/badge.svg?branch=gh-pages)](https://github.com/thackerbroadcasting/docs/actions/workflows/pages/pages-build-deployment) [![Better Stack Badge](https://uptime.betterstack.com/status-badges/v1/monitor/qi7j.svg)](https://uptime.betterstack.com/?utm_source=status_badge)

# mkdocs-site

To develop this locally, do the following:

1. `git clone <repo>`
2. `cd` into the folder

Create a virtual environment with Python

3. `python3 -m venv venv`

Activate the environment

4. - Mac/Linux - `source venv/bin/activate`
   - Windows - `.\venv\Scripts\activate.bat`
5. `pip --version`
6. `code .`

Install dependencies

7. Terminal > New Terminal
8. - Mac/Linux - `pip install mkdocs-material && pip install mkdocs-rss-plugin && pip install mkdocs-git-revision-date-localized-plugin && pip install mkdocs-glightbox`
   - Windows - `pip install mkdocs-material; pip install mkdocs-rss-plugin; pip install mkdocs-git-revision-date-localized-plugin; pip install mkdocs-glightbox`

Serve the site locally

9. `mkdocs serve`
10. Open `localhost:8000`
