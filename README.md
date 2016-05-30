# Text
Manage text and icons
//setup
//hide
[source,cypher]
----
CREATE (neo:Database {name:'Neo4j'})
CREATE (neo)-[:SUPPORTS]->(:Language {name:'Cypher'})
----
[source,cypher]
----
MATCH (db:Database)-[:SUPPORTS]->(language:Language)
RETURN db.name as db, collect(language.name) as languages
----

//table
