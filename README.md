# MDAM Lab website

Source for **[mdamlab.ca](https://mdamlab.ca)**, the website of the Multifunctional Design & Additive Manufacturing Lab at the University of Alberta.

The site is built with [Jekyll](https://jekyllrb.com/) and hosted free on **GitHub Pages**. Every change pushed to the `main` branch is rebuilt and published automatically, usually within a minute or two.

- **Updating content** (news, people, publications, software): see [CONTENT-GUIDE.md](CONTENT-GUIDE.md). You can do all of it in the GitHub web editor, with no software to install.
- **Changing the design**: everything visual is in [assets/css/main.css](assets/css/main.css). Colours and fonts are set once at the top of that file.

## How the site is organised

| Path | What it is |
|---|---|
| `_config.yml` | Site name, contact email, address, and so on |
| `_data/navigation.yml` | The menu across the top (includes the external **Employees** link to the intranet) |
| `_data/team.yml` | People: current members and alumni |
| `_data/publications.yml` | Journal articles, conference papers, books, chapters and patents |
| `_data/software.yml` | Software pages and download links |
| `_data/teaching.yml` | Courses |
| `_data/partners.yml` | Partner and funder logos |
| `_data/funding.yml` | Funding programs listed on the Join Us page |
| `_posts/` | News items, one Markdown file per item |
| `research.html` | Research page (text and figures) |
| `index.html` | Home page |
| `assets/images/` | All images, in one folder per section |
| `_layouts/`, `_includes/` | Page templates; rarely need changing |

## Previewing locally (optional)

You only need this to see changes before you publish them.

1. Install Ruby: on Windows use [RubyInstaller](https://rubyinstaller.org/) (choose "Ruby+Devkit"); on macOS use `brew install ruby`.
2. In this folder, run `gem install bundler` and then `bundle install`.
3. Run `bundle exec jekyll serve`, then open <http://localhost:4000>.

## Hosting set-up (one-time)

1. In the GitHub repository, open **Settings → Pages**.
2. Under *Build and deployment*, set **Source** to *Deploy from a branch*, then choose branch `main` and folder `/ (root)`.
3. Under *Custom domain*, enter `mdamlab.ca` and save. Once the DNS check passes, tick **Enforce HTTPS**.
4. At the domain registrar, set the DNS records:
   - `A` records for `@` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `CNAME` record for `www` → `<github-username>.github.io`
5. Optional but recommended: verify the domain under your GitHub account (**Settings → Pages → Verified domains**). This stops anyone else from claiming it.

The `CNAME` file in this repository tells GitHub Pages which domain to serve.
