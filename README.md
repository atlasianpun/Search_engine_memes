### README

# Meme Search Engine

## Project Overview

This project aims to create a specialized search engine for memes, enabling users to access meme-related information easily. Our approach involved web crawling, indexing, and implementing advanced search algorithms to provide relevant results.

## Features

1. **Web Crawling**
   - Used Apache Nutch for efficient web crawling.
   - Crawled 93 seed URLs from various sources including Reddit, 9gag, and KnowYourMeme.

2. **Indexing**
   - Utilized Apache Solr for indexing the crawled data.
   - Implemented PageRank and HITS algorithms for ranking web pages.

3. **Clustering**
   - Applied KMeans for flat clustering.
   - Used Agglomerative clustering (single-link and complete-link) for hierarchical clustering.

4. **Query Expansion and Relevance Feedback**
   - Implemented Rocchio Algorithm for relevance feedback.
   - Used association, metric, and scalar clustering for pseudo-relevance feedback.

5. **User Interface**
   - Developed a search form with options for different ranking methods.
   - Compared results with Google and Bing using embedded iframes.

## Architecture

The architecture leverages Apache Nutch for crawling, Apache Solr for indexing, and various algorithms for ranking and clustering to enhance the search results. The user interface is designed to compare the results from our search engine with those from Google and Bing.

## Challenges and Solutions

1. **Crawling Efficiency**
   - Initial use of Scrapy was inefficient, resolved by switching to Apache Nutch.

2. **Result Clustering**
   - Clustering results before ranking was infeasible, refined approach by using clustering after PageRank and HITS.

3. **Scalability**
   - Managed scaling issues by optimizing the crawling and indexing processes.

## Learnings

- Gained in-depth knowledge of information retrieval, including web crawling, indexing, ranking, clustering, and query expansion.
- Found that clustering and query expansion significantly improve result relevance.

## Technologies Used

- **Apache Nutch**: Web crawling
- **Apache Solr**: Indexing and searching
- **Python**: Programming and algorithm implementation
- **Scikit-learn**: Clustering and dimensionality reduction
- **NetworkX**: Graph-based algorithms
- **Fastcluster**: Hierarchical clustering

## How to Run

1. **Set Up Environment**
   - Install Apache Nutch and Apache Solr.
   - Set up a local server for Solr at `localhost:8983`.

2. **Crawl and Index Data**
   - Use Nutch to crawl the seed URLs.
   - Index the crawled data using Solr.

3. **Run the Search Engine**
   - Execute the provided scripts to run PageRank, HITS, and clustering algorithms.
   - Use the user interface to enter queries and view results.

4. **Compare Results**
   - Use the UI to compare results with those from Google and Bing.

## Repository Structure

- `crawling/`: Scripts and data for web crawling.
- `indexing/`: Scripts for indexing using Solr.
- `ranking/`: Implementation of PageRank and HITS algorithms.
- `clustering/`: Scripts for KMeans and hierarchical clustering.
- `query_expansion/`: Implementation of Rocchio algorithm and pseudo-relevance feedback.
- `ui/`: User interface code for the search engine.
- `docs/`: Documentation and report files.

## License

This project is licensed under the MIT License.

For more details, refer to the [project report](./docs/final_report_sE.pdf).
