# Relay Networks for Everyone

**From Amplify-and-Forward to Noisy Network Coding and Beyond**

> **One question drives this book:** *What should a relay forward?*

This is a beginner-friendly, open book about relay communication and network information theory.
It is written for readers who know basic probability and digital communications but may have never studied information theory formally.

You do **not** need to understand random coding, typicality, or long proofs before starting.
If you understand the idea of

```text
received signal = transmitted signal + noise
```

you can begin here.

## Why this book?

Relay theory can look intimidating because many papers start with achievable-rate regions, auxiliary random variables, and long proofs.
This book takes the opposite route:

1. **Intuition first** — understand the communication problem before the theorem.
2. **Tiny examples second** — see the idea in a 2- or 3-node network.
3. **Equations third** — introduce only the mathematics needed for the idea.
4. **Paper figures next** — learn how to read the graphs and claims in classic papers.
5. **Code last** — reproduce small examples and build intuition experimentally.

## The main storyline

```text
Why do we need relays?
        ↓
Amplify-and-Forward (AF)
        ↓
Decode-and-Forward (DF)
        ↓
Compress-and-Forward (CF)
        ↓
Network Coding
        ↓
Noisy Network Coding (NNC)
        ↓
Short-Message / Sliding-Window NNC
        ↓
Hybrid DF + NNC
        ↓
Correlated Relay Networks
        ↓
Finite-Blocklength / One-Shot Coding
        ↓
Structured and Learned Relay Coding
```

The book keeps returning to the same question:

> **What information is worth forwarding?**

AF forwards almost everything it hears.  
DF forwards a decoded message.  
CF forwards a compressed observation.  
NNC forwards noisy evidence and lets the destination reason globally.  
Modern methods ask whether the relay can forward only the most useful representation.

## Who is this for?

This book is aimed at:

- undergraduate students entering wireless communications,
- first-year graduate students in communications or information theory,
- machine-learning researchers who want to understand relay and network coding,
- researchers who want a guided path from classic relay theory to modern open problems.

## Difficulty labels

Every section uses one of three levels:

- **Beginner** — intuition; no information-theory background required.
- **Core** — basic probability and mutual information.
- **Deep Dive** — coding theorems, proof ideas, typicality, or non-asymptotic analysis.

You can skip every **Deep Dive** section and still follow the main story.

## Planned chapters

| Part | Chapter | Main question |
|---|---|---|
| I | 1. Why Relays? | Why add an intermediate node at all? |
| I | 2. AF, DF, and CF | What are the three basic relay strategies? |
| II | 3. Information in One Picture | What does “information” mean? |
| II | 4. Mutual Information | How much does the received signal tell us? |
| II | 5. Channel Capacity | What is the maximum reliable communication rate? |
| III | 6. The Relay Channel | What limits a relay system? |
| III | 7. Network Coding | Why should intermediate nodes process information? |
| IV | 8. Noisy Network Coding | Why decode the message instead of every intermediate description? |
| IV | 9. Reading the NNC Figures | What do the famous NNC performance graphs actually show? |
| V | 10. Short-Message NNC | Can NNC work without huge decoding delay? |
| V | 11. Hybrid DF + NNC | Why should every relay always compress? |
| V | 12. Correlated Relay Observations | Are more relay observations always useful? |
| V | 13. Finite Blocklength and One-Shot Coding | What changes when packets are short? |
| VI | 14. Structured Relay Coding | Can practical structure replace abstract random coding? |
| VI | 15. Learned Relay Coding | Can a relay learn what is worth forwarding? |
| VI | 16. Open Problems | What is still unsolved? |

## How each chapter is written

Most chapters follow the same pattern:

```text
1. The problem
2. A human analogy
3. The simplest network picture
4. The classical solution
5. Why that solution is not enough
6. The next idea
7. The minimum equations you need
8. How to read the key paper figure
9. A tiny reproducible experiment
10. What to remember
11. One question leading to the next chapter
```

## Running the book locally

This repository uses **Material for MkDocs**.

```bash
python -m venv .venv

# Linux/macOS
source .venv/bin/activate

# Windows PowerShell
# .\.venv\Scripts\Activate.ps1

pip install -r requirements.txt
mkdocs serve
```

Then open the local address printed by MkDocs.

## Key papers we will eventually cover

The reading path will include classic and modern work on:

- relay channels and decode/compress-forward,
- network coding,
- noisy network coding,
- short-message and sliding-window NNC,
- hybrid decode-forward + NNC,
- correlated-noise relay networks,
- one-shot and finite-blocklength noisy networks,
- structured quantization and learned relay representations.

Each important paper will get a compact **Paper Card** explaining:

```text
Before this paper
Problem
Key idea
What the relay does
What the destination does
Main result
Main limitation
What came next
```

## Status

This book is being written in public, one chapter at a time.

The first goal is not to be encyclopedic. The goal is to make relay and network information theory understandable enough that a new reader can eventually open the original papers and know what question each theorem is answering.
