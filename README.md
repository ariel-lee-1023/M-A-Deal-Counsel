# M&A Deal Counsel

I help you decide whether an acquisition should proceed, on what terms, and through which sequence of work. I begin with the business change the deal is supposed to achieve. The premium needs an explanation: what this buyer can create, who will deliver it, what it will cost, and how long it will take. I compare that case with the target's stand-alone value and the alternatives to buying it.

I follow each important uncertainty across valuation, structure, diligence, financing, approvals, and integration. If an earn-out is proposed to bridge a price disagreement, I ask who controls the business during the measurement period, how the metric is calculated, and what information and remedies the seller will have. The clause must address the disagreement in a form the parties can operate. A diligence finding similarly needs a consequence for price, terms, a condition, acceptance, or walking away.

I keep the transaction's dependencies visible. A delayed approval can affect financing availability and the value of a planned integration; a structure selected for one legal advantage may require consents or create exposure elsewhere. When a fact changes, I identify the affected assumption, provision, workstream, and decision date. My recommendation distinguishes commercial choices from legal constraints and states which current authority or specialist question remains to be verified.

This Agent Skill connects acquisition strategy and execution with legal analysis through four M&A source references. The aim is a transaction whose economics, documents, timetable, and operating plan remain coherent through closing and beyond.

**Deal rationale → value → dependencies → terms → closing and integration.**

[Workflow](#how-it-works) · [Use cases](#use-it-for) · [Install](#installation) · [Examples](#example-requests) · [Repository map](#repository-layout) · [Sources](#sources-and-their-responsibilities) · [Validation](#coverage-and-validation)

## How it works

```mermaid
flowchart TD
    accTitle: Reasoning and delivery workflow
    accDescr: The task and evidence guide domain reasoning, the output and review.
    input["Proposed acquisition or changing deal fact"]
    frame["Test business purpose, standalone value and alternatives"]
    reason["Trace uncertainty across diligence, financing and approvals"]
    choice{"What consequence follows from the finding?"}
    primary["Price, structure, term or condition"]
    alternative["Accept risk, revise the plan or walk away"]
    review["Check operability, current authority and integration dependencies"]
    input --> frame --> reason --> choice
    choice --> primary
    choice --> alternative
    primary --> review
    alternative --> review
    review -.->|Revisit when evidence changes| reason
    classDef focus fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    classDef output fill:#dcfce7,stroke:#15803d,color:#14532d
    classDef decision fill:#fef3c7,stroke:#b45309,color:#78350f
    class frame,reason focus
    class primary,alternative output
    class choice,review decision
```

Deal rationale → value → dependencies → terms → closing and integration. The diagram summarizes the reasoning route; the question and available evidence determine which branches are useful.

## Use it for

- Test acquisition rationale, premium and alternatives.
- Connect diligence findings to price, terms, conditions and decisions.
- Coordinate financing, approvals, closing and integration dependencies.
- Examine how transaction provisions operate under disagreement.

## Installation

Clone the complete repository, then place it in your host's configured skill directory:

```bash
git clone https://github.com/ariel-lee-1023/M-A-Deal-Counsel.git m-a-deal-counsel
```

Keep the complete `SKILL.md` and `references/` tree together. Match the installed folder name to the `name:` field in `SKILL.md`.

## Example requests

> An earn-out bridges the price gap. Test control, measurement, information and remedies during the earn-out period.

> This approval may be delayed. Trace the consequences for financing, closing and integration.

```
m-a-deal-counsel                           # reason from the expert core
m-a-deal-counsel about <topic>             # answer using relevant source depth
m-a-deal-counsel for <book>                # open one distillation directly
```

For a live deal question, provide the jurisdiction, transaction form, parties' roles, stage, and decision needed. Load only the source depth that bears on that decision. Combine strategic/control, process/execution, and legal-doctrine sources when the issue crosses those layers; there is no minimum source count.

## Repository layout

```mermaid
flowchart LR
    accTitle: Repository structure and runtime loading
    accDescr: The canonical core routes to references, while supporting files and maintenance records have separate roles.
    root["M-A-Deal-Counsel/"]
    root --> core["SKILL.md<br/>Reasoning core and loading triggers"]
    core -->|Loads relevant depth| refs["references/<br/>Runtime reference library"]
    root --> support0["AGENTS.md<br/>Project guidance"]
    root --> support1["LICENSE<br/>License"]
    classDef runtime fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    classDef support fill:#f1f5f9,stroke:#64748b,color:#334155
    class core,refs runtime
    class support0,support1 support
```

[Expert core](SKILL.md) · [Reference library](references/) · [Project guidance](AGENTS.md) · [License](LICENSE).

The map reflects the repository’s existing architecture. Runtime references and human-facing maintenance or learning records have different loading roles.

```
SKILL.md                  # expert reasoning core + task-based loading triggers (always loaded)
references/
  reference-<slug>.md     # one dense, standalone distillation per source (loaded on demand)
```

`SKILL.md` is the expert entrypoint; root `AGENTS.md` also guides work when this repository is opened as a project. It establishes deal judgment and working voice, then loads reference depth as the task requires.

## Sources and their responsibilities

```mermaid
flowchart LR
    accTitle: Sources and their primary responsibilities
    accDescr: Task responsibilities connect the expert to its source material; groupings do not imply author agreement.
    core["Expert core and task router"]
    core --> g0["Strategy and control"]
    g0 --> s0_0["Gaughan · Corporate Restructurings"]
    classDef group0 fill:#ede9fe,stroke:#7c3aed,color:#4c1d95
    class g0,s0_0 group0
    core --> g1["Process and execution"]
    g1 --> s1_0["DePamphilis · Integrated M&amp;A"]
    classDef group1 fill:#dcfce7,stroke:#15803d,color:#14532d
    class g1,s1_0 group1
    core --> g2["Legal architecture"]
    g2 --> s2_0["Hill, Quinn &amp; Davidoff Solomon · M&amp;A Law, Theory, and Practice"]
    g2 --> s2_1["Oesterle · The Law of Mergers and Acquisitions"]
    classDef group2 fill:#fef3c7,stroke:#b45309,color:#78350f
    class g2,s2_0,s2_1 group2
    classDef focus fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    class core focus
```

Connections show primary contributions, not a required reading order or agreement among authors. Full source details and qualifications follow; source-specific depth is available in the reference library.

#### Strategy, corporate control, and restructuring
| Source | Distillation |
|---|---|
| **Mergers, Acquisitions, and Corporate Restructurings** — Patrick A. Gaughan | [`reference-gaughan-corporate-restructurings.md`](references/reference-gaughan-corporate-restructurings.md) |

#### Process, valuation, and execution
| Source | Distillation |
|---|---|
| **Mergers, Acquisitions, and Other Restructuring Activities: An Integrated Approach to Process, Tools, Cases, and Solutions**, 10th ed. — Donald M. DePamphilis | [`reference-depamphilis-integrated-ma.md`](references/reference-depamphilis-integrated-ma.md) |

#### Legal doctrine and transaction architecture
| Source | Distillation |
|---|---|
| **Mergers and Acquisitions Law, Theory, and Practice** — Claire A. Hill, Brian J. M. Quinn, and Steven Davidoff Solomon | [`reference-hill-quinn-ma-law-theory-practice.md`](references/reference-hill-quinn-ma-law-theory-practice.md) |
| **The Law of Mergers and Acquisitions**, 3rd ed. — Dale A. Oesterle | [`reference-oesterle-law-of-ma.md`](references/reference-oesterle-law-of-ma.md) |

## Coverage and validation

### What kind of distillation this is

Structure, not summary. Each reference preserves the authors' terminology and framework names, defines key terms inline, folds techniques into decision procedures, and ends with `Decision Rules & Judgment`—the authors' practical if/then discipline stated so it can be used without re-reading. Nothing is copied verbatim at length; all content is synthesized.

Each file carries an explicit **coverage note**. It identifies what is front-loaded, what was compressed, and which current-law or source-format gaps must not be silently filled by extrapolation.

### Source availability and provenance

Built with [Books-to-Skill-Refs](https://github.com/ariel-lee-1023/Books-to-Skill-Refs), which distills multiple sources into one shared, cross-referenced library. The Gaughan and DePamphilis Markdown sources were extracted directly. The Hill/Quinn and Oesterle PDFs were image-only scans, so each was rendered and OCRed in full (835 and 1,002 pages respectively), quality-checked against its title/table-of-contents pages, and then distilled. The full library is validated against the skill contract and injected-instruction scanner.

OCR can introduce recognition errors, especially in case citations, section numbers, tables, and older typefaces. The two OCR-derived references preserve frameworks and decision rules rather than relying on character-perfect quotations. Consult the original scan and current primary authority before quoting or relying on any text, citation, filing threshold, legal standard, or statutory interpretation.

## Limits

### Scope

Strong on transaction rationale, M&A process architecture, corporate-control dynamics, valuation and premium discipline, consideration, financing, governance, integration, divestitures, distressed transactions, and cross-border issue spotting.

Thinner on current jurisdiction-specific corporate, securities, competition, tax, accounting, employment, data, and sectoral law, plus current deal terms and financing markets. `SKILL.md` instructs the agent to **name the gap and verify rather than extrapolate** when a question is current, local, or outside the corpus, and to mark which part of an answer rests on the library versus current verification.

## License

[MIT](LICENSE)—covering the original work here: the skill structure, expert core, loading guidance, README, and distillation text as written.

The underlying sources retain their own terms and are not relicensed. The reference files are structural summaries of frameworks, terminology, and decision rules, not reproductions. Check the individual source before redistributing or building on it.
