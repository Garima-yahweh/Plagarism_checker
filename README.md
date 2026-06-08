# Plagarism_checker
Built a token-based plagiarism detection system using rolling hashes and approximate sequence matching. Detects exact and modified code similarities, identifies longest matching segments, and generates plagiarism scores efficiently.
# Token-Based Plagiarism Detection System

## Overview

This project implements a plagiarism detection system for tokenized source code submissions. It identifies both exact and approximate similarities between two submissions using rolling hash techniques and gap-tolerant matching.

The system is designed to detect copied code even when minor modifications, insertions, or deletions have been made.

## Features

* Exact match detection using Rabin–Karp rolling hashes
* Detection of non-overlapping matching code segments
* Approximate matching with configurable gap tolerance
* Longest similar segment identification
* Similarity scoring and plagiarism flag generation
* Efficient hash-based indexing for large token streams

## Algorithm

### Exact Matching

1. Generate rolling hashes for fixed-length token windows.
2. Store hashes and their starting positions.
3. Compare hash values across submissions.
4. Verify matches and record non-overlapping exact matches.

### Approximate Matching

1. Start from detected exact matches.
2. Expand matches forward and backward.
3. Allow a limited number of gaps while preserving alignment.
4. Compute the longest approximate matching segment.

## Output

The system returns:

* Plagiarism flag (0/1)
* Total exact matched token length
* Length of the longest approximate match
* Starting index of the match in Submission 1
* Starting index of the match in Submission 2

## Technologies Used

* C++
* STL Containers
* Rolling Hashing (Rabin–Karp)
* Hash Maps
* Sequence Matching Algorithms

## Applications

* Academic plagiarism detection
* Source code similarity analysis
* Competitive programming submission comparison
* Large-scale code repository inspection

## Author

Developed as a data structures and algorithms project exploring efficient techniques for source code similarity detection.
