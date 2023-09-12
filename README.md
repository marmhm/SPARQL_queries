# representative_queries
To start read the notbook "**collect_semantically_representitive_queries.ipynb**".

In this notebook, I've documented the procedures I've undertaken to put into action our discussed approach for gathering representative queries concerning Bio2RDF logs. This includes actions like clustering queries by their similarity, evaluating query complexity, and gaining insights into complexity distribution. 


# Code for profiling paper

link to presentation:

 https://docs.google.com/presentation/d/1RXceHE59gw2YfzfJZhaElSRb3rIPDr-1/edit?usp=sharing&ouid=103705832009765615891&rtpof=true&sd=true

## In this paper we profile sparql logs of bio2rdf and wikidata and collect representative queries.

Method:

- delete http parameters such as &format ,...
- get unique queries (does not handle the white spaces)
- add prefixes
- parse queries
- get normalized queries
- get unique queries from normalized verion and parsed tree(to handle white space problem)
- profile table: Keyword count in queries
(SELECT, Ask, Describe, Construct, Distinct, Limit, Offset, Order By, Filter, And, Union, Opt, Graph, Not Exists, Minus, Exists, Count, Max, Min, Avg, Sum, Group By, Having)
- calculate informativness,
- get distributaion of triple patterns
- cluster queries based on their similarity
- define semantic metrics


Next steps:
1. Evaluation:
- learn about composite Error Estimation
- Is this measure estimates syntactic features 
- learn if you could compare your work with this. (Is it applicable?)
2. To define semantic features:
- learn about the work in NLP to calculate semantic similarity of text data
- wordnet and clustering based on that
3. To normalize queries:
q1: <NL>  :population ?p
q2:   ?c     :population ?p
normalized query: ?var1 :population ?var2
we can map NL to a variable and then we have identifies queries that are very similar, but they are about different instances of same type

4. Share the code


