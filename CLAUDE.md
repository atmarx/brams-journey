# Project Context for Claude

## What This Is

"From Inflammation to Healing: Bram's Journey" — a free, open-source health resource disguised as a narrative. It follows Bram, a 45-year-old contractor who develops severe joint pain and inflammation from toxic mold exposure and achieves complete recovery through environmental remediation, anti-inflammatory protocols, movement therapy, and natural medicine.

**Target audience:** Contractors and blue-collar workers. The content addresses both physical health challenges AND the cultural barriers to seeking help in trades environments (stigma around "weakness," distrust of doctors, "tough it out" mentality).

**Format:** MkDocs site with Material theme. Originally written as a LaTeX book, converted to web format for accessibility.

## Project Philosophy

- **Free forever.** No paywalls. Target audience (struggling workers) least able to pay.
- **Comprehensive over sparse.** More citations, more explanation, more troubleshooting — not less.
- **Practical over academic.** Real-world applicability matters more than theoretical completeness.
- **Credibility through honesty.** Bram's skepticism of the medical establishment rings true because there's no commercial motive.

## File Structure

```
docs/
├── index.md                    # Home page
├── disclaimers.md              # Medical/legal disclaimers (thorough)
├── journey/                    # Bram's narrative (11 chapters + epilogue)
│   ├── index.md
│   ├── chapter-1-when-did-it-start.md
│   └── ... through chapter-9 + epilogue
├── exercises/                  # 28 exercise files total
│   ├── index.md               # Exercise hub
│   ├── daily-8.md             # Overview of foundation stretches
│   ├── invisible-8.md         # Overview of workplace exercises
│   ├── office-worker.md       # Office adaptation overview
│   ├── [8 Daily 8 exercises]  # Individual stretch pages
│   ├── [8 Invisible 8 exercises]  # Individual workplace exercise pages
│   └── [8 Office adaptations] # Individual office exercise pages
├── protocols/                  # Treatment protocols
│   ├── anti-inflammatory-diet.md
│   ├── supplements.md
│   ├── cannabis.md
│   └── mushrooms.md
└── resources/                  # Quick references
    ├── 30-day-starter.md
    ├── meal-planning.md
    ├── supplement-schedule.md
    ├── tracking-templates.md
    ├── mold-remediation.md
    └── further-reading.md
```

## Key Conventions

### Admonitions (callout boxes)

We use MkDocs Material admonitions consistently:

```markdown
!!! warning "Title"
    Content for warnings, cautions

!!! tip "Title"  
    Content for tips, insights

!!! success "Title"
    Content for success stories

!!! info "Title"
    Content for general information
```

### Troubleshooting Sections

All 16 individual exercise files use **collapsible dropdowns** for troubleshooting:

```markdown
??? question "Problem: Description of issue"
    **Cause:** Why this happens
    
    **Solutions:**
    
    - Solution one
    - Solution two
    
    **Timeline:** How long to expect improvement
```

This keeps pages scannable while providing deep detail for those who need it.

### Jeff Cavaliere Attribution

We reference Jeff Cavaliere (AthleanX) in 4 exercise files with attributed quotes in tip boxes:

- cat-cow.md — spinal articulation cue
- 90-90-hip-stretch.md — hip mobility insight
- hip-flexor-stretch.md — posterior pelvic tilt cue  
- calf-hamstring-stretch.md — flat back rule

**Status:** Permission email drafted, sending January 2025. Quotes are attributed and educational — should be fine, but we're being respectful.

### Image Placeholders

All 28 exercise files have image placeholders on line 3:

```markdown
![Descriptive alt text](../images/exercises/exercise-name.jpg)
```

Images directory exists but is empty. This is the main pre-launch task.

## Tech Stack

- **MkDocs** with **Material theme**
- Custom CSS in `docs/stylesheets/extra.css`
- GitHub Actions workflow for auto-deploy (`.github/workflows/deploy.yml`)
- Deploys via FTPS to web host

### Local Development

```bash
pip install mkdocs-material
mkdocs serve          # Live preview at localhost:8000
mkdocs build          # Build to /site
```

## Outstanding Tasks

### Before Launch
- [ ] Add images to 28 exercise files
- [ ] Final proofread
- [ ] Create favicon
- [ ] Deploy

### After Launch  
- [ ] Send Jeff Cavaliere permission email
- [ ] Create About/Support page (user's story, "buy me a coffee" link)
- [ ] Consider Vitaglo.com informal referral (small NY health food store)

### Maybe Later
- [ ] Spanish translation
- [ ] Audio/podcast version
- [ ] Video exercise demos
- [ ] Print-on-demand book option

## Content Notes

### Tone
- Warm but not saccharine
- Technically precise but accessible
- Respects the reader's intelligence
- Acknowledges difficulty without catastrophizing
- Blue-collar voice — practical, no-BS, but also vulnerable when appropriate

### Bram's Character
- 45-year-old general contractor
- Initially dismissive of "alternative" medicine
- Transforms through necessity, not ideology
- Teaches others what he learned
- Voice: experienced tradesman who's been humbled and emerged wiser

### Medical Content
- Extensively cited where possible
- Honest about what's established vs. emerging
- Clear disclaimers throughout
- Never promises cures — presents options and evidence

## Session History

This project was developed across multiple Claude sessions:
1. Initial LaTeX book writing
2. Conversion to MkDocs (53 files)
3. Troubleshooting format standardization (dropdowns)
4. Consistency audit and polish
5. GitHub Actions setup

Transcripts available in `/mnt/transcripts/` if running in Claude.ai environment.

## Questions?

If you're a future Claude instance working on this: the human (Andrew) prefers accuracy over speed, likes comprehensive answers, and wants you to ask clarifying questions rather than make assumptions. He'll explicitly tell you when to make changes vs. when to just advise.

The project matters to him personally — it's meant to help real people, not just be a portfolio piece.
