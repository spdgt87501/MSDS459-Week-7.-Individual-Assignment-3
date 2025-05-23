# MSDS459-Week-7.-Individual-Assignment-3

Part 1 - Week 6 - Knowledge Graphs

For week 6, chapter 12 of the textbook Knowledge Graphs by Kejriwal et al., 2021 was assigned.  This chapter provides an overview of structured querying for knowledge graphs.  According to the text, two types of structured query language are applicable to knowledge graphs.  These two types are SPARQL and key-value stores (Kejriwal et al., 2021).

SPARQL is a graph-pattern matching language inspired by more traditional database query languages such as SQL (Kejriwal et al., 2021).  SPARQL is a self-referencing acronym that stands for SPARQL protocol and RDF query language (Wiki Education, n.d.).  RDF or the Resource Description Framework is a modeling language for knowledge graphs. A SPARQL query works by specifying literals in triple patterns (Kejriwal et al., 2021).
Like SQL, SPARQL allows subqueries. These can be utilized to embed one SPARQL query within another.  This allows for the specification of more detailed criteria based upon the relationships between entities within the knowledge graph (Kejriwal et al., 2021).

There have also been efforts to develop ways of storing knowledge graph data in relational databases.  These efforts seek to provide both the representational advantages of knowledge graph databases as well as benefits from a traditional relational database structure.  Structure approaches for this typically fall into one of three categories.  These are triple (vertical) table stores, property table stores, and horizontal table stores.  Triple (vertical) stores store triplets in a single three column table.  This approach is very straightforward, but queries can be very slow as the table grows.  This is because multiple references to the same object are self-referential in that they must re-reference the same table.  Such looping is computationally expensive.  Property table stores, however, use a more traditional approach common to well maintained relational databases.  Each object is unique and stored on an object’s table.  Other parts of the triple are then stored on separate tables allowing one to many relationships.  Horizontal stores utilize a separate two column table for each property.  The two columns contain data for subjects and objects for that property (Kejriwal et al., 2021).  

Key value stores get their inspiration from NoSQL.  NoSQL simply references databases that do not use SQL as their primary querying interface.  In a key value store, each key represents one unique object and is stored in a blob with no defined schema.  Since data is stored as blobs, objects are queried directly without indexing.  This data retrieval is often performed with JSON (Kejriwal et al., 2021).

References

Kejriwal, Mayank, Craig A. Knoblock, and Pedro Szekely. Knowledge graphs: Fundamentals, techniques, and applications. Cambridge, MA: The MIT Press, 2021.
Wiki Education. “What’s SPARQL?” - wiki education dashboard. Accessed May 15, 2025. https://dashboard.wikiedu.org/training/wikidata-professional/querying-wikidata/whats-sparql.
