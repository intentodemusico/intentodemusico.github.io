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
The NLP-driven Topic Engine proved to be a useful tool for analyzing the Metaculus dataset. By creating a knowledge graph with key relationships between important entities, we were able to gain insights into the dynamics and structure of the data.

After uploading the dataset to Neo4j, we were able to perform Cypher queries to analyze the graph. We could analyze user expertise by checking their favorite topics, suggest subcategories by looking at the most popular topics, and more.

For example, we could query the graph to identify the most popular topics in the dataset, and use that information to suggest subcategories or improve the tagging system for questions. We could also analyze the relationships between topics, such as identifying which topics tend to co-occur in questions, and use that information to improve forecasting models.

Overall, the NLP-driven Topic Engine proved to be a valuable tool for analyzing the Metaculus dataset and improving the science of forecasting. By identifying key topics and relationships between entities, we were able to gain insights that could be used to make more accurate predictions and improve forecasting models.

**Takeaways:**    
NLP-driven Topic Engines can be used to extract important topics from datasets, and create a knowledge graph with their key relationships. This can be useful in improving data analysis and decision-making.

Neo4j is a powerful graph database that can be used to model complex relationships between entities in a dataset. It provides a range of tools for querying and analyzing the graph structure, which can help to gain insights into the data.

By using the Wikifier API to extract topics from questions in the Metaculus dataset, the project team was able to generate a JSON dataset, which was then uploaded to Neo4j for analysis. This demonstrates how APIs can be leveraged to extract valuable data from existing datasets.

The project provides several potential applications of the generated graph, such as analyzing user expertise by checking their favorite topics, or suggesting subcategories by looking at the most popular topics. This demonstrates the potential usefulness of a knowledge graph in understanding the dynamics of a dataset.