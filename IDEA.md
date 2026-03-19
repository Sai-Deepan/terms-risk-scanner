Step 1: Cache by domain (biggest win)

If 1 user scans facebook.com:

Store result

Next 10,000 users:

Reuse result → $0 cost

This alone can reduce cost by 90%+

Step 2: Chunk + filter BEFORE LLM

Don’t send entire document.

Pipeline:

Extract text

Split into chunks

Pre-filter using:

Regex (keywords like “share”, “sell”, “renew”)

Lightweight model / rules

👉 Only send suspicious chunks to LLM

Step 3: Use cheap models first

Flow:

Cheap model → detect if risky

Expensive model → explain (only if needed)
