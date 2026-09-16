# Awesome Chinese Repos — Project Guide

## Mission

Curate and maintain a high-quality list of Chinese open-source projects that provides real value to the international developer community. The goal is to become the top "awesome-*" list bridging China's open-source ecosystem with the world.

## Repository Structure

```
README.md          — The main curated list (THE product)
CONTRIBUTING.md    — Contribution guidelines
CLAUDE.md          — This file: AI assistant rules & update strategy
LICENSE            — CC0-1.0
```

## Inclusion Criteria

Every project in the list MUST satisfy ALL of:

1. **Chinese origin**: Built by Chinese developers, teams, or companies
2. **Open source**: On GitHub with a recognized license
3. **Quality**: 500+ stars, actively maintained, reasonably documented
4. **International appeal**: Solves problems international devs care about
5. **Non-political**: No politically sensitive content whatsoever

### README Language Rule

- **Primary focus**: Repos whose default README is in Chinese — these are the hidden gems
- **Also included**: Chinese-team repos with English READMEs — mark with `[EN]` tag
- The `[EN]` tag helps readers know they can read the docs directly

### What makes a repo "interesting to internationals"?

High priority:
- AI/ML models and tools (China leads in many areas)
- Enterprise-grade systems showing scalable architecture patterns
- Developer tools solving universal problems
- Unique ecosystems (WeChat Mini Programs, China-specific infra)
- High-quality learning resources with novel teaching approaches

Low priority (usually skip):
- Region-locked services (Chinese government API wrappers, etc.)
- Niche Chinese-market-only business tools
- Repos with very similar functionality to existing entries

## Daily Update Strategy

When performing daily updates, follow this rotation:

### Search Strategy (rotate daily)

**Day 1 — Trending & New**: Search GitHub trending for Chinese repos, check recently created high-growth repos
**Day 2 — Deep Category Dive**: Pick one category, do exhaustive search for missing gems
**Day 3 — Quality Audit**: Verify existing entries still meet criteria (archived? stars dropped? description accurate?)
**Day 4 — AI/ML Focus**: China's AI ecosystem moves fast — dedicated search for new models, tools, frameworks
**Day 5 — Community & Ecosystem**: Search for repos mentioned in Chinese tech blogs, Juejin, SegmentFault, CSDN
**Day 6 — Cross-pollination**: Look at other awesome-* lists for Chinese repos they missed or we missed
**Day 7 — Metadata & Polish**: Update star counts, fix broken links, improve descriptions, enhance formatting

### Search Commands

```bash
# Trending Chinese repos
gh search repos "中文" --sort stars --order desc --limit 30
gh search repos "管理系统" --sort stars --order desc --limit 20
gh search repos "工具" --sort stars --order desc --limit 20 --language go

# Category-specific searches
gh search repos "大模型 中文" --sort stars --order desc --limit 20
gh search repos "小程序" --sort stars --order desc --limit 20
gh search repos "爬虫" --sort stars --order desc --limit 20
gh search repos "面试" --sort stars --order desc --limit 20

# Recently created high-growth repos
gh search repos "中文" --sort stars --order desc --created ">YYYY-MM-DD" --limit 20
```

### Update Workflow

1. Search for candidates using the day's strategy
2. For each candidate:
   - Check star count (must be 500+)
   - Verify Chinese origin (check author profile, repo language)
   - Read README to assess quality and international appeal
   - Check it's not a duplicate of existing entries
   - Write a clear, accurate English description
3. Add qualified repos to the appropriate category
4. Remove any repos that no longer meet criteria (archived, deleted, etc.)
5. Commit changes with descriptive message

### Evolution Rules

- **Add categories** when 3+ new repos don't fit existing ones
- **Merge categories** when a category has fewer than 2 entries for 30+ days
- **Reorder entries** within categories by star count (descending)
- **Update descriptions** when a repo's focus has significantly shifted
- **Graduate repos**: If a repo moves from Chinese to English README, add `[EN]` tag (don't remove it)

## Writing Style

- Descriptions: 1-2 sentences, English, factual, highlighting what makes the project notable
- No marketing language, no superlatives unless earned (e.g., "most-starred" is factual)
- Focus on what the project DOES, not who made it (unless the origin matters, e.g., "by Alibaba")
- Technical accuracy over impressiveness

## Commit Messages

Format: `update: [action] [category/scope]`

Examples:
- `update: add 3 new AI repos (ChatGLM3, Qwen2.5, Yi-34B)`
- `update: remove archived repo shuzheng/zheng`
- `update: refresh star counts and fix broken links`
- `update: add new WeChat Ecosystem category`

## Quality Metrics (self-tracking)

Track these in commit messages when doing audits:
- Total repos listed
- Repos added / removed this update
- Broken links fixed
- Categories added / merged
