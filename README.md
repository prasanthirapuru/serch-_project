# AlgoVector – Interview Preparation

<a id="toc"></a>

## Table of Contents

**Part 1 – Interview Answers**

- [Introduction](#intro)
- [1. Explain your project in two minutes.](#q1)
- [2. What problem does AlgoVector solve?](#q2)
- [3. Explain the complete workflow of your project.](#q3)
- [4. Why did you use Selenium for web scraping?](#q4)
- [5. How did you collect and organize 2,000+ problems?](#q5)
- [6. Explain TF-IDF with a simple example.](#q6)
- [7. Explain Cosine Similarity with a simple example.](#q7)
- [8. How do TF-IDF and Cosine Similarity work together to return the top 10 results?](#q8)
- [9. What challenges did you face, and how did you solve them?](#q9)
- [10. What are the limitations of your project, and how would you improve it?](#q10)
- [Quick revision: the entire project in 5 lines](#quick)

**Part 2 – Your Interview Answer**

- [Your interview answer – AlgoVector](#your-answer)
- [One-line project summary](#one-line)

---

# Part 1 – Interview Answers

<a id="intro"></a>

Here are interview-ready answers to all 10 important AlgoVector questions, written in simple, natural English. Each answer is designed to be easy to understand and speak during an interview.

<a id="q1"></a>

## 1. Explain your project in two minutes.

Answer:

"My personal project is called AlgoVector – Semantic Search Engine for DSA Problems.

The idea for this project came from my experience practicing DSA problems. I noticed that problems were available across different coding platforms like LeetCode, GeeksforGeeks, and CSES. Whenever I wanted to find problems on a particular topic, I had to visit each website separately, which could be time-consuming.

To solve this problem, I developed AlgoVector, a search engine that collects DSA problems from multiple coding platforms and displays the top 10 relevant problems based on the user's search query.

First, I used Python and Selenium to scrape problem data from these platforms. I organized the collected data into a structured dataset containing more than 2,000 problems.

Next, I implemented the search functionality using TF-IDF and Cosine Similarity. TF-IDF converts the text into numerical representations by assigning weights to words, while Cosine Similarity measures how closely the user's query matches each problem. Based on these similarity scores, the system ranks the problems and returns the top 10 results.

For the backend, I used Flask to process search queries and return the results. On the frontend, I used HTML, CSS, and JavaScript to build a responsive web application.

One of the main challenges was collecting data from different platforms and organizing it consistently. Another challenge was finding relevant results for the user's query. I addressed the search challenge using TF-IDF and Cosine Similarity to calculate similarity scores and rank the problems.

Overall, this project helped me gain practical experience in web scraping, information retrieval, text processing, and full-stack application development."

[⬆ Back to Table of Contents](#toc)

---

<a id="q2"></a>

## 2. What problem does AlgoVector solve?

Answer:

"AlgoVector solves the problem of searching for DSA problems across multiple coding platforms.

Normally, users have to visit websites like LeetCode, GeeksforGeeks, and CSES separately to find problems on a particular topic. My application brings problems from these platforms into one place and allows users to search for relevant problems through a single interface.

This saves users the effort of searching across multiple websites individually."

[⬆ Back to Table of Contents](#toc)

---

<a id="q3"></a>

## 3. Explain the complete workflow of your project.

Answer:

"The workflow of AlgoVector consists of three main stages: data collection, search processing, and displaying the results.

First, I used Python and Selenium to collect DSA problem data from LeetCode, GeeksforGeeks, and CSES. I organized the collected data into a structured dataset containing more than 2,000 problems.

Second, when a user enters a search query, the search system uses TF-IDF to convert the query into a numerical vector. It then uses Cosine Similarity to compare the query vector with the problem representations and calculate similarity scores.

Third, the system ranks the problems based on their similarity scores and selects the top 10 results. Flask handles the backend processing and returns the results to the frontend, where they are displayed using HTML, CSS, and JavaScript."

| Stage | Detail |
|---|---|
| Data collection | Python + Selenium |
| Structured dataset | 2,000+ DSA problems |
| Search processing | TF-IDF + Cosine Similarity |
| Backend | Flask ranks and returns results |
| Frontend | HTML + CSS + JavaScript |

[⬆ Back to Table of Contents](#toc)

---

<a id="q4"></a>

## 4. Why did you use Selenium for web scraping?

Answer:

"I used Selenium because it allows Python to control a web browser and interact with web pages. It is useful for collecting information from websites where browser interaction or page rendering may be required.

In my project, Selenium helped me collect DSA problem data from multiple coding platforms. I then organized the collected information into a structured dataset for the search engine."

Possible follow-up: Why not use BeautifulSoup?

"BeautifulSoup is mainly used to parse HTML and extract information from it. Selenium can also automate a browser and interact with web pages. I chose Selenium for my data collection process because of its browser automation capabilities."

[⬆ Back to Table of Contents](#toc)

---

<a id="q5"></a>

## 5. How did you collect and organize 2,000+ problems?

Answer:

"I used Python and Selenium to collect problem data from LeetCode, GeeksforGeeks, and CSES.

After collecting the data, I organized it into a structured dataset containing more than 2,000 problems. Keeping the data in a consistent format made it easier for the search engine to process the problem text and compare it with the user's query.

This dataset acts as the collection of problems that AlgoVector searches through."

If the interviewer asks about the exact fields or storage format: explain what your code actually uses. For example, mention titles, URLs, platform names, CSV, JSON, or a database only if those are part of your implementation.

[⬆ Back to Table of Contents](#toc)

---

<a id="q6"></a>

## 6. Explain TF-IDF with a simple example.

Answer:

"TF-IDF stands for Term Frequency–Inverse Document Frequency. It is a technique used to convert text into numerical representations by assigning weights to words.

Term Frequency measures how often a word appears in a document. Inverse Document Frequency measures how informative that word is across the entire collection of documents.

For example, suppose a user searches for 'binary tree traversal.'

A problem titled 'Binary Tree Level Order Traversal' contains important words that overlap with the query. TF-IDF assigns weights to these words based on their frequency in the problem and across the dataset.

A problem about 'Dynamic Programming on Arrays' has less word overlap with the query, so its TF-IDF representation would generally be less similar.

In this way, TF-IDF helps represent the query and problem descriptions numerically so that their similarity can be calculated."

Remember:

- TF = how frequently a word appears in a document.
- IDF = how informative the word is across the collection.
- TF-IDF = the combined weight assigned to a word.

[⬆ Back to Table of Contents](#toc)

---

<a id="q7"></a>

## 7. Explain Cosine Similarity with a simple example.

Answer:

"Cosine Similarity is a technique used to measure the similarity between two numerical vectors. It calculates the cosine of the angle between them.

In AlgoVector, I use it to compare the TF-IDF vector of the user's search query with the TF-IDF vectors of the problems in the dataset.

For example, if the user searches for 'binary tree traversal,' a problem titled 'Binary Tree Level Order Traversal' would generally have a higher similarity score because its important words overlap with the query.

A problem about 'Dynamic Programming on Arrays' would generally have a lower score because it has less overlap with the query.

The system uses these scores to identify and rank the most relevant problems."

The formula is:

$$
\operatorname{CosineSimilarity}(A,B)= \frac{A\cdot B}{\|A\|\|B\|}
$$

Remember: For TF-IDF vectors, a score closer to 1 indicates greater similarity, while a score closer to 0 indicates less similarity.

[⬆ Back to Table of Contents](#toc)

---

<a id="q8"></a>

## 8. How do TF-IDF and Cosine Similarity work together to return the top 10 results?

Answer:

"TF-IDF and Cosine Similarity perform two different roles in my search engine.

First, TF-IDF converts the user's query and the problem text into numerical vectors by assigning weights to words.

Next, Cosine Similarity compares the query vector with the vectors representing the problems in the dataset. It calculates a similarity score for each problem.

The system then sorts the problems in descending order of their similarity scores and selects the top 10 results.

So, TF-IDF creates the numerical representations, and Cosine Similarity compares them to help rank the problems."

Simple example

Query: "binary tree traversal"

| Problem | Similarity |
|---|---|
| Binary Tree Level Order Traversal | More similar |
| Dynamic Programming on Arrays | Less similar |

Illustrative comparison, not measured scores from your actual dataset.

[⬆ Back to Table of Contents](#toc)

---

<a id="q9"></a>

## 9. What challenges did you face, and how did you solve them?

Answer:

"One of the main challenges I faced was collecting data from multiple coding platforms and organizing it into a consistent dataset. Since the problems came from different websites, I needed to bring the collected information into a structured format that could be processed by the search engine.

Another challenge was making the search results relevant to the user's query. To address this, I implemented TF-IDF to represent the text numerically and Cosine Similarity to compare the query with the problems.

The system uses the resulting similarity scores to rank the problems and return the top 10 results.

Through these challenges, I learned how to work with data from multiple sources and combine text-processing techniques with a web application."

Interview tip: If the interviewer asks for a specific bug or technical issue you encountered, give a real example from your development experience rather than inventing one.

[⬆ Back to Table of Contents](#toc)

---

<a id="q10"></a>

## 10. What are the limitations of your project, and how would you improve it?

Answer:

"One limitation of my current approach is that TF-IDF mainly relies on the words present in the query and problem descriptions. It may not fully understand the meaning of a query or recognize synonyms when different words express the same concept.

For example, a user might search for a concept using different wording from the problem title, and the system may not identify the relationship effectively.

To improve this, I would consider using sentence embeddings, which can represent the meaning of text and help find conceptually related problems even when the wording differs.

I would also like to expand the dataset, add filters for topics and difficulty levels, and improve the process of updating problem data.

These improvements could make AlgoVector more flexible, useful, and capable of handling a wider range of search queries."

[⬆ Back to Table of Contents](#toc)

---

<a id="quick"></a>

## Quick revision: the entire project in 5 lines

If you remember these five points, you can reconstruct most of your answers during the interview.

1. Problem: DSA problems are spread across multiple coding platforms, making them harder to find in one place.
2. Data collection: Python and Selenium collect more than 2,000 problems from LeetCode, GeeksforGeeks, and CSES.
3. Search: TF-IDF converts text into weighted numerical vectors.
4. Ranking: Cosine Similarity compares the query with the problem vectors, and the system returns the top 10 results.
5. Application: Flask handles the backend, while HTML, CSS, and JavaScript provide the responsive frontend.

Most important: Understand the difference between TF-IDF and Cosine Similarity. If you can clearly explain what each one does and how they work together, you will be prepared for many of the technical follow-up questions about AlgoVector.

[⬆ Back to Table of Contents](#toc)

---

# Part 2 – Your Interview Answer

<a id="your-answer"></a>

## Your interview answer – AlgoVector

"My personal project is called AlgoVector – Semantic Search Engine for DSA Problems.

The idea for this project came from my experience practicing DSA problems. I noticed that problems are available across different coding platforms. For example, when I wanted to find problems on LeetCode, GeeksforGeeks, and CSES, I had to visit each website separately. Similarly, when I wanted to practice a particular topic or concept, finding relevant problems across these platforms could be time-consuming.

To solve this problem, I developed AlgoVector, a search engine that collects DSA problems from different coding platforms and displays the top 10 relevant problems based on the user's search query, all in one place.

First, I used Python and Selenium to scrape problem data from LeetCode, GeeksforGeeks, and CSES. I then organized the collected data into a structured dataset containing more than 2,000 problems.

Next, I implemented the search functionality using TF-IDF and Cosine Similarity. TF-IDF converts the text into numerical representations by assigning weights to important words. Cosine Similarity then measures how closely the user's search query matches the problems in the dataset. Based on these similarity scores, the system ranks the problems and selects the top 10 results.

For the backend, I used Flask. When a user enters a search query, Flask processes it and returns the top 10 relevant problems based on their similarity scores.

On the frontend, I used HTML, CSS, and JavaScript to develop a responsive web application that allows users to search easily and view the results.

During the development, I faced a few challenges. One of the main challenges was collecting problem data from multiple coding platforms and organizing it into a consistent, structured dataset. Another challenge was making sure that the search results were relevant to the user's query. To address this, I used TF-IDF and Cosine Similarity to calculate similarity scores and rank the problems accordingly.

Overall, this project gave me practical experience in web scraping, text processing, information retrieval, similarity algorithms, and Flask application development. I also learned how to identify a real-world problem, overcome technical challenges, and combine different technologies to build an end-to-end solution."

[⬆ Back to Table of Contents](#toc)

---

<a id="one-line"></a>

## One-line project summary

"AlgoVector is a Python-based search engine that collects DSA problems from multiple coding platforms and ranks the top 10 results based on the similarity between the user's search query and the problem text."

[⬆ Back to Table of Contents](#toc)
