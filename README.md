# skill-creator-agent

An AI agent that helps you create, test, improve, and optimize skills for Claude Code and other AI assistants. It guides you through the full skill development lifecycle — from drafting SKILL.md to running evaluations, benchmarking, and optimizing trigger descriptions.

## Run

```bash
npx @open-gitagent/gitagent run -r https://github.com/<username>/skill-creator-agent
```

## What It Can Do

- Draft new skills from scratch based on your intent
- Write SKILL.md with proper frontmatter, instructions, and bundled resources
- Generate realistic test prompts and run evaluations
- Launch an interactive eval viewer for qualitative human review
- Run quantitative benchmarks with variance analysis (pass rate, time, tokens)
- Perform blind A/B comparisons between skill versions
- Optimize skill descriptions for better triggering accuracy
- Package skills for distribution as `.skill` files

## Structure

```
skill-creator-agent/
├── agent.yaml
├── SOUL.md
├── RULES.md
├── README.md
└── skills/
    └── skill-creator/
        ├── SKILL.md
        ├── agents/
        │   ├── analyzer.md
        │   ├── comparator.md
        │   └── grader.md
        ├── assets/
        │   └── eval_review.html
        ├── eval-viewer/
        │   ├── generate_review.py
        │   └── viewer.html
        ├── references/
        │   └── schemas.md
        └── scripts/
            ├── __init__.py
            ├── aggregate_benchmark.py
            ├── generate_report.py
            ├── improve_description.py
            ├── package_skill.py
            ├── quick_validate.py
            ├── run_eval.py
            ├── run_loop.py
            └── utils.py
```

## Built with

[gitagent](https://github.com/open-gitagent/gitagent) — a git-native, framework-agnostic open standard for AI agents.
