# Stratify — Gemini CLI extension

Backtest Indian index option strategies on real 1-minute NIFTY options data from Gemini CLI.
Results carry P&L after real charges, return on margin, and an honesty panel (out-of-sample
split, walk-forward folds, bootstrap interval, deflated Sharpe).

```bash
gemini extensions install https://github.com/Srinath-exe/stratify-gemini-extension
export STRATIFY_API_KEY=sk_live_...   # free key: https://stratify.aeon-labs.site (Google sign-in)
gemini
```

Then just describe a trade: *"Sell a 20-delta strangle on NIFTY every Thursday, stop at 2x
credit, and show me whether it held up out of sample."*

The extension holds no code: it points Gemini CLI at the hosted MCP server
(`https://stratify-mcp.aeon-labs.site/mcp`) and ships a context file that tells the model
how to read the results honestly. Data never leaves the server; only results come back.

- Docs: https://stratify.aeon-labs.site/docs
- Privacy: https://stratify.aeon-labs.site/privacy
- Contact: https://stratify.aeon-labs.site/contact
