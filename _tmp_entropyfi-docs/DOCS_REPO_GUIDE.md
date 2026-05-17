# Entropyfi Docs Repository Setup

## Repository Structure

```
entropy-docs/
├── README.md                          # Main entry point
├── INDEX.md                           # Complete TOC & navigation
│
├── entropyfi-1.0/
│   ├── prediction-market.md           # Main game mechanics
│   └── sponsorship.md                 # Pool sponsorship guide
│
├── entropyfi-50-50/
│   ├── overview.md                    # 50,50 products intro
│   ├── cope-free-hedge.md             # Hedge strategy (create this)
│   ├── rekt-free-leverage.md          # Leverage strategy (create this)
│   └── vsq-tutorial.md                # Live example (create this)
│
├── token/
│   ├── erp-market.md                  # Token trading (create this)
│   ├── tokenomics.md                  # Distribution (create this)
│   └── vault-inc-staking.md           # Staking guide (create this)
│
├── developers/
│   ├── deployed-contracts.md          # All contract addresses
│   ├── game-logic.md                  # Settlement mechanics (create this)
│   ├── pool-tokens.md                 # Token design (create this)
│   └── token-nav.md                   # NAV calculation (create this)
│
├── getting-started/
│   └── testnet-tokens.md              # Testnet setup (create this)
│
└── community/
    └── join.md                        # Community links (create this)
```

## Files Included

**Already Created:**
- ✅ README.md
- ✅ INDEX.md
- ✅ entropyfi-1.0/prediction-market.md
- ✅ entropyfi-1.0/sponsorship.md
- ✅ entropyfi-50-50/overview.md
- ✅ developers/deployed-contracts.md

**Still Needed (Optional - From Your Original Docs):**
- ⬜ entropyfi-50-50/cope-free-hedge.md
- ⬜ entropyfi-50-50/rekt-free-leverage.md
- ⬜ entropyfi-50-50/vsq-tutorial.md
- ⬜ token/erp-market.md
- ⬜ token/tokenomics.md
- ⬜ token/vault-inc-staking.md
- ⬜ developers/game-logic.md
- ⬜ developers/pool-tokens.md
- ⬜ developers/token-nav.md
- ⬜ getting-started/testnet-tokens.md
- ⬜ community/join.md

## How to Use This Repository

### Option 1: Upload to GitHub (Recommended)

```bash
# Create new repo on GitHub named 'entropy-docs'
# Then locally:

git clone https://github.com/YOUR_ORG/entropy-docs.git
cd entropy-docs

# Copy all markdown files from entropy-docs/ directory

git add .
git commit -m "Initial commit: Entropyfi documentation"
git push origin main
```

### Option 2: Setup with GitBook (Like Original)

1. Create new GitBook space
2. Import this repository
3. GitBook will auto-generate navigation from file structure
4. Configure sidebar in gitbook.json

Example gitbook.json:
```json
{
  "root": "./",
  "structure": {
    "readme": "README.md",
    "summary": "INDEX.md"
  }
}
```

### Option 3: Self-Hosted (MkDocs, Docusaurus, etc.)

These docs are plain markdown and work with any documentation generator:

```bash
# MkDocs
mkdocs new . && mkdocs serve

# Docusaurus
docusaurus start

# Hugo
hugo serve
```

## File Format Notes

All files use:
- **Markdown** (.md)
- **GitHub-flavored markdown** (GFM)
- **Heading hierarchy**: H1 (title), H2 (sections), H3 (subsections)
- **Code blocks** for contract addresses and formulas
- **Tables** for reference data
- **Links** for cross-navigation

## Content Guidelines

When adding new files:

1. **Keep it simple** — No fluff, no AI speak
2. **Use examples** — Every concept should have a concrete example
3. **Link generously** — Cross-link to related topics
4. **Update INDEX.md** — Add new pages to TOC
5. **Name consistently** — kebab-case.md for file names

## What's Inside Each Section

### Getting Started
- Basic setup
- Testnet token claiming
- First prediction walkthrough

### Entropyfi 1.0
- Core prediction market mechanics
- How sponsorship works
- Yield generation flow

### Entropyfi (50,50)
- Rebase token strategy
- Soft Leverage vs (9,9)
- Live example (VSQ)

### Token ($ERP)
- Trading pairs and venues
- Vesting schedule
- Staking mechanics
- Governance role

### Developers
- Complete contract reference
- Settlement logic
- Pool token math
- NAV calculations

### Community
- Discord link
- Telegram link
- Twitter
- Email/contact

## Updating the Docs

To add new content:

1. Create .md file in appropriate folder
2. Add section to INDEX.md TOC
3. Add links from README.md or parent pages
4. Test all links locally
5. Commit and push

## Deployment

### With GitHub Pages

```bash
# Automatically published if you:
# 1. Enable GitHub Pages in repo settings
# 2. Choose "main branch /docs folder"
# 3. Build with Jekyll or Docusaurus
```

### With GitBook

```bash
# Link GitHub repo to GitBook
# GitBook auto-syncs on each push to main
# Published at: https://app.gitbook.com/o/YOUR_ORG/s/entropy-docs
```

### With Vercel (Docusaurus)

```bash
# Connect GitHub repo
# Vercel auto-deploys on push
# Custom domain supported
```

## Maintenance

- **Update quarterly** — Keep contract addresses current
- **Monitor GitHub issues** — Users will request clarifications
- **Link to Medium** — Reference key posts
- **Archive old versions** — Use Git branches for past docs

## SEO & Discovery

For best discoverability:

1. Add keywords to README.md
2. Use descriptive headings (H1, H2, H3)
3. Internal links (cross-linking)
4. Meta descriptions in Jekyll/Docusaurus frontmatter
5. Sitemap.xml (auto-generated by most platforms)

---

## Quick Start

1. **Download** all files from `/entropy-docs/` directory
2. **Create GitHub repo** called `entropy-docs`
3. **Push files** with: `git add . && git commit -m "Initial docs" && git push`
4. **Share URL** with team/community
5. **Monitor feedback** for gaps and improvements

## File Manifest

| File | Lines | Content |
|---|---|---|
| README.md | 140 | Welcome & quick links |
| INDEX.md | 230 | TOC & learning paths |
| prediction-market.md | 350 | Full game guide |
| sponsorship.md | 240 | Sponsor mechanics |
| overview.md | 290 | 50,50 intro |
| deployed-contracts.md | 400+ | Contract reference |

**Total:** 6 files, 1,650+ lines of documentation

---

**Status:** Ready to deploy. Just upload files to your GitHub repo and share the link!
