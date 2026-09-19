# Fineline

**Upload a contract and Fineline scans for the five clauses most likely to leave a freelancer exposed.**

Fineline is a contract risk scanner built for freelancers. Most freelancers sign client contracts without a lawyer, and a handful of clause types cause most of the trouble. Fineline reads an uploaded contract and flags those clauses in plain language, so you know what to question before you sign.

> Fineline was originally named Redline. It was renamed to avoid naming collisions with existing legal tech products.

> **Important:** Fineline flags potential risks. It is not legal advice and does not replace a lawyer. See [Limitations](#limitations).

## What Fineline flags

| Risk | Why it matters to a freelancer |
|---|---|
| **Auto-renewal clauses** | The contract can renew automatically unless you cancel inside a set window, locking you into another term. |
| **Unlimited liability** | Nothing caps what you could owe if something goes wrong, which can far exceed what you were paid. |
| **IP assignment** | Ownership of your work can transfer to the client, sometimes including tools or material you created before the engagement. |
| **Non-competes** | You may be restricted from working with other clients, during or after the engagement. |
| **Unilateral termination rights** | One side, often the client, can end the agreement without giving you the same right or without paying for work done. |

## How it works

1. **Upload** a contract.
2. **Read.** Fineline extracts the contract text. [DESCRIBE: supported file types, for example PDF, DOCX, plain text]
3. **Analyze.** The contract is checked against the five risk categories using Anthropic's Claude for the risk-analysis logic.
4. **Review.** Fineline reports what it found for each category. [DESCRIBE: the output format, for example flagged clause text, a plain-language explanation, and a severity or status indicator]

## Screenshots

[ADD: upload screen and results screen]

## Built with

- Built on [Replit](https://replit.com)
- [Claude](https://www.anthropic.com/claude) (Anthropic) for contract risk analysis
- [ADD: language, framework, and any libraries]

## Getting started

[FILL IN based on how the project runs. A typical structure:]

```bash
git clone https://github.com/elyse-deq/fineline.git
cd fineline
# [install dependencies]
# [set environment variables, for example your Anthropic API key]
# [start the app]
```

Configuration:

| Variable | Purpose |
|---|---|
| `[ANTHROPIC_API_KEY]` | [Key used for the Claude analysis. Never commit it.] |

Add your keys to a local `.env` file or to Replit Secrets, and make sure `.env` is listed in `.gitignore`.

## Privacy and data handling

Contracts are sensitive documents. [DESCRIBE how Fineline handles them: whether files are stored, how long, whether contract text is logged, and how a user can delete their data.]

Recommended practices for anyone running or forking this project:

- Do not log or store contract text unless you have to.
- Delete uploaded files after analysis.
- Do not commit real contracts, and use public samples for testing.
- Tell users plainly what is sent to the analysis service.

## Limitations

- **Not legal advice.** Fineline points out clauses worth a closer look. It cannot judge how a clause applies to your situation, your jurisdiction, or your negotiating position.
- **It can miss things or misread them.** Language models can overlook a clause, misinterpret unusual wording, or flag something that is harmless. A "nothing found" result does not mean a contract is safe.
- **Five categories only.** Other risky terms, such as payment timing, scope creep, or indemnification, are outside what Fineline checks today.
- **Always read the whole contract,** and consider having a lawyer review anything high-stakes.

## Possible next steps

These are ideas, not commitments. Edit this list to match your plans.

- Test the five checks against a public labeled contract dataset such as CUAD and publish the results
- Highlight flagged clauses directly on the uploaded document
- Suggest alternative wording or negotiation points for each flag
- Cover more clause types

## Contributing

[DESCRIBE how people can report issues or suggest changes, or remove this section.]

## License

[CHOOSE A LICENSE, for example MIT, and add a LICENSE file. Without one, the default is all rights reserved.]

## Author

Built by [Elyse](https://elysedequina.org). GitHub: [@elyse-deq](https://github.com/elyse-deq)
