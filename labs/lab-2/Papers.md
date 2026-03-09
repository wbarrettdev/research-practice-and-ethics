Just read abstract introduction and solution

# 1 - From Local to Global: A GraphRAG Approach to Query-Focused Summarization (April 2024)

### Which problem it addresses
Query focused Sumarization across large Coprpus of data is not curently feasible.
Sumarization tasks work well on small documents or chunks. 
Query focused sumarization (Global question) tasks like "What are the main themes in the dataset?" are not retrieval tasks (theres no specific chunks to find)
therefore RAG fails at this.

Graph rag merges these two methods by using an llm to build a graph index in two stages: 
1 - Derive an entity knowlege graph from the source documents.
2 - Pregenerate comunities

### What solution it proposes
GraphRAG, a graph based approach to question answering on large private text corpora

### How the solution differs from previous solutions
This paper is the first of its kind. it introduced the concept.

### What are the main contributions and conclusions
- gave the graphrag method itself.

# 2 - Unifying Large Language Models and Knowledge Graphs: A Roadmap (June 2023)

### Which problem it addresses
It looks at the integration of knowlege graphs with llms to overcome the challeneges of each . 

### What solution it proposes
It proves three directions to integrate Knowlege graphs directly with llms.

### How the solution differs from previous solutions
Curent solution add the knowlege graph as a external KB where as this reviews integrating the two.

### What are the main contributions and conclusions

1 - introduces a roadmap for integrating llms and KGs consisting of 3 frameworks:

    1 - KG enhanced LLMS,
    2 - LLM augnmented Knowledge Graphs,
    3 - Synergized LLMs KGs

2 - Provides a review of each if the research done in each strategy. 
3 - covers emerging tech like multimodal knowlege graphs.
4 - Summary of challenegs and future directions.

# 3 - Graph Retrieval-Augmented Generation: A Survey (December 2025)

### Which problem it addresses
It performs a comprehensive review of graphrag as of the 23rd of devember 2025
### What solution it proposes
it does not propose a solution but outlines the current state of the art.
### How the solution differs from previous solutions
it is the first review and current upto date.
### What are the main contributions and conclusions

    1 - A comprehensive systematic review of the state of the art of graph rag.

    2 - A formal definition of graph rag.
    3 - Core technologies underpinning graphrag and analyse whats currently being explored.
    4 - Delineate evaluation mechanisms, benchmarks  and insight into real wrld industry solutions. 
    5 - Talks about benchmarks and validating quality. Alkso talks about limitations around faithfulness
    6 - talks through the current graph rag implementations in idustry. (neo4j has a builder)
    7 - Future research areas
        1 - adptive graphrag (dynamically updating graphs knowlege)
        2 - multimodal KG 
        3 - Scalable and efficient retrieval mechanisms (paraleel retrieval over gigantic datasources)
        4 - lossless compression of retrieved context
        5 - standard benchmarks.

# 4 - Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks (April 2025) 

### Which problem it addresses
The basically reducing hallucinations by creating rag . 
### What solution it proposes
This is the initial RAG papaer.
### How the solution differs from previous solutions
First of its kind
### What are the main contributions and conclusions
- created the rag architecture.
- proved RAG was better than extractive qa (RAG says it in its own words.)
- changable knowlege (you can update documents)
- benchmarks
- marginalization strategy. 
    - pick one document as the source of truth
    - weighted aopprorach across multiple documents (blend multiple documenst at tokenm level)

# 5 - RAKG: Document-level Retrieval Augmented Knowledge Graph Construction  (april 2025 - Not peer reviewed) 

### Which problem it addresses
 how to build better knowlege graphs from documents. 
### What solution it proposes
it proposes RaKG - a new way to build knolewedge graph construction by addressing some tof the issuyes with 
### How the solution differs from previous solutions
It builds ontop of rag and each entitie identyified retroispective looks on the knwlege graphs to find mentions.
This allows it to build ontop of provious relationships. Regular GraphRAG didnt look back retrospectively.
### What are the main contributions and conclusions
- this one has source code. 
- improved the accuracy on the mine dataset over graphrag.
- code available here https://github.com/KnowledgeXLab/RAKG
- e2e solution for constructing knowlege graphs from documnets. 
- introduces a RAG evaluation framework in the domain of knowlege graph construction
- promising on MINE dataset


# 6 - LLM-empowered Knowledge Graph Construction: A Survey (October 2025 - not yet peer reviewed)

### Which problem it addresses
A survey into llm based knowlege graph construction/ probably more modern than others.
### What solution it proposes
it gives an overview of how llms and generative ai can bridge the gap of natural language and knowlege relationships.
### How the solution differs from previous solutions
its similar to paper 2 unifying knowlege graphs. perhaps its more modern? 
### What are the main contributions and conclusions
Very similar to other papers on the past and present of knowlege graph construction combined with llm integration. 
mnaiun acontibutions are another survey. ikt has similar. 
- Addresses that a future direction is how to integrate this knowlege graph in to reasoning. 
- dynameic dynamic updating and evolution of agent knowlege. 
- multimodal graph construction.
- overview of how llms are transforming knowlege graph construction.


# 7 - KGGen: Extracting Knowledge Graphs from Plain Text with Language Models (Feb 2025)

### Which problem it addresses
A new approach to knwolege graph constuction. cluster and de duplicate entities.
### What solution it proposes
kg-gen: knowlege graph generation from any text.
### How the solution differs from previous solutions
clusters adn de-duplicates related entities to reduce sparsity.
### What are the main contributions and conclusions
- a new way to build knowlege graphs that cluster and deduplicate
- MINE -  a benchmark to test an extractors ability to produce a useful knowlege graph from plain text.
- code is open source https://github.com/stair-lab/kg-gen/
- benchmarks to measure kggens perfomance
- demonstrate the scalability of KGGen

# 8 - LLMs for Knowledge Graph Construction and Reasoning: Recent Capabilities and Future Opportunities (May 2023)

### Which problem it addresses
we use llms to create knowlege graphs but we dont know if it does it well.
### What solution it proposes
benchmark the performance of modern llms in kg tasks like realation extraction, event detection, link prediction and QA
### How the solution differs from previous solutions
other papers are testing each in isolation. this paper takes a higher level systematic evaluation to knowlege graph conmstruction,
### What are the main contributions and conclusions
- review across consturction and reasoning. 
- VINE data set to see if lllms can extract about unencountered entities.
- AutoKG - a multi agent framwork to autonomously construct knowlege graphs.is 
-

# 9 - An Adaptive Framework Embedded With LLM for Knowledge Graph Construction (April 2025)

### Which problem it addresses
Schema guided llm based knowlege graphs consume lots of tokens because it requires embediing the full schema into the prompt.
### What solution it proposes
ACKG-LLM - spolits KG construction into three sequential subtasks
1 - extration of the triplpes without andy schema contsaints
- the llm predicts hidden relationship info
- allign the triples with the schema.
### How the solution differs from previous solutions
other attempts produce poor results when going schema free. 
waiting till the end for adding schema context reduces the token amount.
### What are the main contributions and conclusions
- this hasa a break down of data stes and when top use them. 
- mentions how paramter efficient fine tuning helps with ambiguity
- the actual contributions are:
    - ACKG-LLM: llm based graph construction framework to imporve on existing pipelines. 
    - design prompts need for knowlege graph construction.
    - use llm to predict hidden relationships

# 10 - Knowledge Graph-extended Retrieval Augmented Generation for Question Answering (April 2025)

### Which problem it addresses
basically similar to the others. we can extend the llm with a KG instead of fine tuning the model
### What solution it proposes
KG-RAG - a training free system that retrieves from a knowlegdge graph. 
### How the solution differs from previous solutions
it introduces Incontext learning and a chain of thought approach to decompose queries. 
### What are the main contributions and conclusions
combined training free approach from kaping (just fire the triples into the llm.)
with explainiablility through chain of though. the COT breaks down the questions making them explainable.

# 11 - Retrieval-Augmented Generation with Knowledge Graphs for Customer Service Question Answering (April 2024)

### Which problem it addresses
Speed up customer support using retrival methods and a chatbot.
standard rag is just chunk based and cant create relationships across historical issues.
This is proof that hybrid approaches are needed.
### What solution it proposes
the combine KG with llm by creating the knowlege graph based on historical issues. create relationshiops between issues. 
### How the solution differs from previous solutions
create a proven working in production system that has improved efficiency. not just an acedmic benchmark.

### What are the main contributions and conclusions
- dual method construction of issues go into trees and then connect them via relationshiops into a single graph. 
- use the llm to generate the graph query. 
- production deployyment.
- fallback mechanism. if graph fails use rag.


# 12 - Towards Practical GraphRAG: Efficient Knowledge Graph Construction and Hybrid Retrieval at Scale (July 2025)

### Which problem it addresses
enterprise deployment of knowledge graphs have two problems. 
1 - knowlege graph construction ios expensive. 
2 graph retireval is too slow. 
### What solution it proposes
dependency parsing  - an nlp approach rathaer than llm approach to knowledge graph cosntruction.
hybrid merging of 50/50- grapoh and rag
### How the solution differs from previous solutions
- they say you dont need llms to build the graphs. 
### What are the main contributions and conclusions
- llm free knowlege graph constructyion
- hybrid retrieval combining rag and Graphrag. 
- applied to legacy code migration
- more cost effective approach to enterprise adopption.

### What are the main contributions and conclusions

# 13 - Document Knowledge Graph to Enhance Question Answering with Retrieval Augmented Generation (Seot 2024)

### Which problem it addresses
- vector based rag only retrieves text chunks from a vector database. 
- it cant answer questions that go beyond the text content like metadata or relationships between documents. 
- as the number of documents grows this becomes a bigger problem.

### What solution it proposes
- a Document Knowlege Graph (DKG) built from document structures to extend rag. 
the KG manages document hierarchy and metadata alongside the vector database. 
- the two databases are linked so the DKG can enrich what the vector search finds.

### How the solution differs from previous solutions
- uses a structural/metadata graph rather than an entity extraction graph. rule based not llm based.
- extends rag rather than replacing it. vector search still does the heavy lifting, DKG adds context on top.

### What are the main contributions and conclusions
- concept for building a DKG using existing schema to manage document structure and metadata.
- shows how to integrate the DKG into a rag architecture alongside a vector database.
- applied to factory planning domain. funded by audi.


# 14 - Attention Is All You Need (2019)

### Which problem it addresses
it introduces the transformer architecture.
### What solution it proposes
transformers
### How the solution differs from previous solutions
made training paralell.
### What are the main contributions and conclusions
transformer architecture

# 15 - Combining LLMs and Knowledge Graphs to Reduce Hallucinations in Question Answering (september 2024)

### Which problem it addresses
halluceinations in the medical industry is bad. 
### What solution it proposes
- source code - https://git.zib.de/lpusch/cyphergenkg-gui
natural language to cypher query pipeline (cypher is neo4j)
### How the solution differs from previous solutions
all answers are grounded in the knowlegdge graph. 
### What are the main contributions and conclusions
- cypher query check functionality. 
- becnhmark dataset of biomedical questiosn.
comparison of multiple llms and the impact of multishot prompting. 