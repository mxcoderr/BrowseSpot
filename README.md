# BrowseSpot
Browse Spot - a lightweight search engine written in Rust. 

**Pros**:

1.not a metasearch engine

a full-fledged search engine with its own databaseбnot just a metasearch engine unlike SearxNG and many other search engines (I still don't see the point of metasearch engines - all they do is spit out links to other search engines, so it's basically just search-engine advertising)

2. No AI - predictable, transparent search

 without AI and not agent-ready (LLM developers: using BrowseSpot is contraindicated for your models.)

3. written in Rust

neither Python, nor PHP, nor Ruby,Rust only (I don't get why other search engines use Python or PHP - a search engine is a project that needs high performance)


**Downsides**:

1. a project in the early stages of development

Small community; there may be bugs,other problems

2. The style in which this README is written might seem too bold or clunky to some, but I’m leaving it as is.


## How it works

1. The user enters a query, for example: `youtube`.
2. BrowseSpot searches its own database for matching site names.
3. Candidate matches are identified using a trigram alghoritm instead of a linear scan.
4. The candidates are ranked using the Levenshtein distance algorithm.
5. Only results with a similarity score of **50% or higher** are considered valid matches.
6. The top **N** results are returned to the user.

## Stack used
**Frontend**: Vue, JavaScript (Sorry, I'm not very good at TypeScript.)
**Backend**: Rust,Axum 
