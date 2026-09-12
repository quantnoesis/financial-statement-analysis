# What ROE Doesn't Tell You: A Beginner's Look at 200 US Companies' Financial Health

*My first Python data project, and what it taught me about reading ratios like an analyst, not a spreadsheet.*

## Why I Started Here

I have a formal background in finance and accounting, but I'm brand new to Python. So instead of learning Python through generic tutorials, I decided to learn it by doing the kind of analysis I actually understand: financial statement ratios. I used a Kaggle dataset covering pre-calculated ratios — ROE, current ratio, debt-to-equity, and more — for the top 200 US companies, and worked through it in Google Colab.

## Step One: Just Look at the Data

Before doing anything clever, I loaded the CSV with pandas and checked the basics: what columns existed, how many rows, what data types, and quick summary statistics (mean, min, max) across all the ratios. This is a habit worth keeping regardless of the tool — you don't analyze what you haven't looked at first.

## Ranking by ROE — and a Reality Check

Return on Equity (ROE) is one of the most commonly cited profitability metrics: it tells you how efficiently a company turns shareholder equity into profit. So naturally, my first move was to sort all 200 companies by ROE and see who came out on top.

The answer: **McKesson Corporation**, by a wide margin.

If you don't know McKesson's story, this looks like a slam-dunk — a company squeezing enormous returns out of shareholder capital. But here's where the accounting background matters more than the code: McKesson has spent years aggressively buying back its own stock, which shrinks shareholder equity — sometimes down to very small or even negative levels. Since ROE is calculated as Net Income divided by Equity, a shrunken denominator can inflate the ratio dramatically, even when the underlying business performance hasn't changed all that much.

In other words: **a high ROE isn't automatically a sign of a great business — it can just as easily be a sign of financial engineering.**

## Widening the Lens: Liquidity and Leverage

To avoid over-indexing on one ratio, I pulled two more views:

- **Current Ratio** (short-term liquidity — can a company cover its near-term obligations?)
- **Debt-to-Equity** (leverage — how much debt is the company carrying relative to equity?)

Sorting by Current Ratio surfaced a different group of companies entirely from the ROE leaderboard — *[fill in: your top 10 liquidity names once you run the chart]*. That alone is worth sitting with: the "best" company depends entirely on which question you're asking. A company can be a poor ROE performer and still be extremely safe on liquidity, or vice versa.

Looking at these alongside ROE gives a much more honest picture than any single number in isolation. A company with a sky-high ROE but also very high debt-to-equity is telling a very different story than one with high ROE and conservative leverage — even if the ROE figure looks identical on paper.

## Testing the McKesson Theory Across All 200 Companies

The McKesson observation raised a question: is this a one-off, or a pattern? To check, I plotted every company's ROE against its Debt-to-Equity ratio in a single scatter chart, rather than just looking at the top 10.

*[fill in once you run the scatter chart: did the highest-ROE companies cluster at high debt-to-equity too, or was McKesson more of an outlier? A visible upward trend would support the buyback/leverage theory at scale; a scattered, no-pattern cloud would suggest McKesson's case is more unusual than systemic.]*

Either way, this is the more rigorous version of the same instinct: don't trust one ratio, and don't trust one company's story as proof of a pattern until you've checked it across the full dataset.

## The Takeaway

The biggest lesson from this project wasn't a Python lesson — it was a reminder that **ratios are shorthand, not truth.** ROE, on its own, answers "how much profit relative to equity?" but says nothing about *why* the equity is the size it is. The moment you pull in debt levels, buyback history, or industry context, the story can change completely.

For anyone with a finance background moving into data work: this is exactly the kind of judgment that a model or a script can't replicate on its own — knowing which number to be suspicious of, and why, is domain knowledge, not code.

## What's Next

This was project one of an ongoing series where I'm using Python to explore different corners of finance — next up: either rounding out this dataset further, or moving into a completely different area like credit risk, budgeting trends, or market data.

---
*Built with Python (pandas, matplotlib) in Google Colab. Dataset: "Financial Statement Data for Top 200 US Companies" via Kaggle.*
