# tRNA Unique Substring Finder — UCSC bioinformatics coursework

A Python program from my biomolecular engineering degree at UC Santa Cruz.
Given a set of tRNA sequences in FASTA format, it finds, for each tRNA, the
**essential unique substrings**: the shortest pieces of sequence that appear in
that tRNA and in no other tRNA in the set.

## How it works

1. **Read** each FASTA record and clean out alignment characters (`.`, `_`, `-`).
2. **Build** the set of every substring of each tRNA.
3. **Find uniques**: substrings of one tRNA that appear in none of the others
   (set difference against the union of all other tRNAs' substrings).
4. **Keep only essentials**: drop any unique substring that still contains a
   shorter unique substring, so only the minimal ones remain.
5. **Print** each essential substring under the tRNA sequence, offset with dots
   to show where it occurs.

## Note on the file

`findUnique.py` in this repository is a PDF printout of the program, not a
runnable script.

## What it shows

Set-based thinking, careful handling of substrings and positions, and a
class-based design in Python. It is an early programming project, not a
finance tool.

## My current work

These days I apply the same habit of separating signal from noise to
quantitative macro research:

- [FedWatch](https://github.com/puvanat21exls/fedwatch-fomc-realtime): a
  pre-registered study of whether real-time macro data predicts FOMC decisions
- [CRE Watchtower](https://github.com/puvanat21exls/cre-watchtower-bank-stress):
  commercial real estate stress across US regional banks
- [What Drives Bitcoin?](https://github.com/puvanat21exls/bitcoin-drivers-study)
