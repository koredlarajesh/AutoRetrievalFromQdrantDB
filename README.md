AutoRetrieval from a Vector Database , i used here qdrantdb

This notebook shows how to perform auto-retrieval in LlamaIndex.

Many popular vector dbs support a set of metadata filters in addition to a query string for semantic search. 
Given a natural language query, we first use the LLM to infer a set of metadata filters as well as the right query string to pass 
to the vector db (either can also be blank). This overall query bundle is then executed against the vector db.


This allows for more dynamic, expressive forms of retrieval beyond top-k semantic search. The relevant context for a given query 
may only require filtering on a metadata tag, or require a joint combination of filtering + semantic search within the filtered set, or just raw semantic search.
