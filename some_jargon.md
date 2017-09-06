1. inverted index
2. relevancy ranking

3. Features of Solr
	- Text centric
	- Read dominant
	- Document oriented
	- Flexible schema.

3. document oriented: 
	- self contained collection of fields.
	- Document oriented data doesn't contained nested field
	- Schema type is flat structured.
	- Solr is document oriented search engine.
	- In solr document structure, a field cannot contain multiple subfields but can contain multiple values.

	- Flat document structure wokrs well for the data that are already in flat structure like webpages, pdf or word.
	- To index the data that resides in Normalized form(Db), we need to denormalize the db ie. convert the related multiple table into a single table.


4. Flexible schema
	- This means the document that resides on the solr don't need to have a uniform schema.

5. index structure is defined in  Solr’s using flexible schema.xml configuration document.

6. Apache Hadoop provides an open source implementation of MapReduce, and it’s
used by the Apache Nutch open source project to build a Lucene inverted index for
web-scale search using Solr. A thorough discussion of Hadoop and Nutch is beyond
the scope of this book, but we encourage you to investigate these projects if you need
to build a web-scale search index. 
