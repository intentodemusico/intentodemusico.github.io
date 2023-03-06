# Topic engine
**Project context:** Metaculus is a forecasting challenge platform that was celebrating its 1 million predictions hackathon!
We are happy to be part of it, so this was our MVP for the challenge.
Knowledge graphs are a type of data structure, usually used on state-of-the-art query engines (such as GraphQL), having its speed advantages and insights capabilities, we found an interesting opportunity to experiment with.

**Goal:** Determine if an NLP-driven Topic Engine that identifies the most important topics in Metaculus questions and creates a knowledge graph with their key relationships could be used to improve the science of forecasting.

**Methodology:**
First, the graph is model to represent the relationships between the important entities of the Metaculus dataset structure, then a Neo4j database is setup and the extraction of the topics is executed. Finally, the new dataset with the topics included is uploaded to Neo4j and then the queries can be applied to performed analysis.

[![](https://mermaid.ink/img/pako:eNolj72qAjEQRl9lmCqCdlZbCOqKjQr-lGmGzajR3SQkE1DEd79z1-7wnVPMfLCLjrHBW6Z0h93JhqXZjrxX0ftwm8BstoCVOXCcP-DMUtNEq3Fdm0tMvoPNSzJ14mNQtRpVa1oSKixQUx_JqVj_hA3tCBtzrJw9F6DgYBmofxdftAPAKQ6cB_JOT_v8LxblzgNbbBQd5adFG77aUZV4focOG8mVp1iTI-HWk340YHOlvvD3D_eLSks?type=png)](https://mermaid.live/edit#pako:eNolj72qAjEQRl9lmCqCdlZbCOqKjQr-lGmGzajR3SQkE1DEd79z1-7wnVPMfLCLjrHBW6Z0h93JhqXZjrxX0ftwm8BstoCVOXCcP-DMUtNEq3Fdm0tMvoPNSzJ14mNQtRpVa1oSKixQUx_JqVj_hA3tCBtzrJw9F6DgYBmofxdftAPAKQ6cB_JOT_v8LxblzgNbbBQd5adFG77aUZV4focOG8mVp1iTI-HWk340YHOlvvD3D_eLSks)

First, the graph is model to represent the relationships between the important entities of the Metaculus dataset structure, then a Neo4j database is setup and the extraction of the topics is executed. Finally, the new dataset with the topics included is uploaded to Neo4j and then the queries can be applied to performed analysis.

For the Metaculus dataset, the following graph is considered as the base for the helper classes and structure in Neo4j. 

![](https://lh6.googleusercontent.com/sABrhmWjNjAcGRgh2R2LYxVWYoVRx9KxUJoAZpXSCER413nO7XVaZCMyZxI-SP9iCaV2s4pQPM38768fbHcZRFCvi0q3YzLxqp2YK2NcdJ-D0cqiIhnF3SX4EyMLKq3Bmr8zgo4lWkohSGS0EGm1aK_fH12MRhK_TOiKGnHs7cZgKdMVyFU8GiNen2QxTEu2=s2048)

Neo4j was used to model a graph of relationships between entities in the Metaculus dataset. Nodes and relationships can store data as parameters. We extracted topics from questions using the Wikifier API, generating a JSON dataset, and uploaded it to Neo4j for analysis. The number of detected topics depends on the page rank used to filter entities.

**Results:**
After uploading the dataset to Neo4j, it is possible to perform Cypher queries for analyzing the graph dynamics and structure. There are several analysis that can be perfomed with the given graph structure by using queries, such as getting analyzing the user expertise by checking his/her favorite topics, suggest subcategories by looking at the most popular topics, etc.

**Takeaways:**