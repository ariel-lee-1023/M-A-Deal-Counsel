# M&A Deal Counsel

An Agent Skill that turns an agent into a senior, deal-oriented **M&A counsel and transaction strategist**—capable of transaction framing, strategic analysis, process design, diligence-to-term-sheet reasoning, valuation/consideration discipline, regulatory issue spotting, governance analysis, integration planning, and restructuring comparison.

It distills two complementary M&A texts: one focused on corporate control, strategic rationale, governance, and restructuring; the other on the integrated process, tools, valuation, structuring, and execution of a deal.

## Layout

```
SKILL.md                  # router + operating stance + cross-book topic index (always loaded)
references/
  reference-<slug>.md     # one dense, standalone distillation per source (loaded on demand)
```

`SKILL.md` is the only file an agent loads automatically. It routes to the reference files, which cost nothing until opened.

## Sources

### Strategy, corporate control, and restructuring
| Source | Distillation |
|---|---|
| **Mergers, Acquisitions, and Corporate Restructurings** — Patrick A. Gaughan | [`reference-gaughan-corporate-restructurings.md`](references/reference-gaughan-corporate-restructurings.md) |

### Process, valuation, and execution
| Source | Distillation |
|---|---|
| **Mergers, Acquisitions, and Other Restructuring Activities: An Integrated Approach to Process, Tools, Cases, and Solutions**, 10th ed. — Donald M. DePamphilis | [`reference-depamphilis-integrated-ma.md`](references/reference-depamphilis-integrated-ma.md) |

## Install

Clone into your agent's skill directory. For Claude Code:

```bash
git clone https://github.com/ariel-lee-1023/M-A-Deal-Counsel.git ~/.claude/skills/m-a-deal-counsel
```

Other hosts use different roots—for example `~/.copilot/skills/`, `~/.agents/skills/`, or `.claude/skills/` for project scope. Keep the directory name `m-a-deal-counsel` to match `name:` in `SKILL.md`.

## Usage

```
m-a-deal-counsel                           # router — pick the right source(s)
m-a-deal-counsel about <topic>             # topic index → the relevant reference files
m-a-deal-counsel for <book>                # open one distillation directly
```

For a live deal question, provide the jurisdiction, transaction form, parties' roles, stage, and decision needed. Most substantive responses should draw on both sources: the strategic/control lens and the process/execution lens.

## What kind of distillation this is

Structure, not summary. Each reference preserves the authors' terminology and framework names, defines key terms inline, folds techniques into decision procedures, and ends with `Decision Rules & Judgment`—the authors' practical if/then discipline stated so it can be used without re-reading. Nothing is copied verbatim at length; all content is synthesized.

Each file carries an explicit **coverage note**. It identifies what is front-loaded, what was compressed, and which current-law or source-format gaps must not be silently filled by extrapolation.

## Scope

Strong on transaction rationale, M&A process architecture, corporate-control dynamics, valuation and premium discipline, consideration, financing, governance, integration, divestitures, distressed transactions, and cross-border issue spotting.

Thinner on current jurisdiction-specific corporate, securities, competition, tax, accounting, employment, data, and sectoral law; current deal terms and financing markets; and the two image-only scanned sources noted below. `SKILL.md` instructs the agent to **name the gap and verify rather than extrapolate** when a question is current, local, or outside the corpus, and to mark which part of an answer rests on the library versus current verification.

## Source availability and provenance

Built with [Books-to-Skill-Refs](https://github.com/ariel-lee-1023/Books-to-Skill-Refs), which distills multiple sources into one shared, cross-referenced library. The included Markdown sources were extracted and validated against the skill's library contract and injected-instruction scanner.

The supplied PDFs *Mergers and Acquisitions Law, Theory, and Practice* (Hill, Quinn et al.) and *The Law of Mergers and Acquisitions* (Oesterle et al.) are image-only scans with no usable text layer, so their contents are not represented in the agent-loaded materials. OCR a reliable copy (or provide a text/Markdown conversion) before folding either into a new reference file and updating the router/topic index.

## License

[MIT](LICENSE)—covering the original work here: the skill structure, router, topic index, README, and distillation text as written.

The underlying sources retain their own terms and are not relicensed. The reference files are structural summaries of frameworks, terminology, and decision rules, not reproductions. Check the individual source before redistributing or building on it.
