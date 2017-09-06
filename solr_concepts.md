solrcloud vs solr
====================
You may have heard of SolrCloud and wondered what the difference is between Solr 4
and SolrCloud. Technically, SolrCloud is the code name for a subset of features in
Solr 4 that makes it easier to configure and run a scalable, fault-tolerant cluster of
Solr servers. Think of SolrCloud as a way to configure a distributed installation of Solr 4.
Also, SolrCloud doesn’t have anything to do with running Solr in a cloud-computing
environment like Amazon EC2, although you can run Solr in the cloud. We presume
that the “cloud” part of the name reflects the underlying goal of the SolrCloud feature
set to enable elastic scalability, high availability, and the ease of use we’ve all come
to expect from cloud-based services. We cover SolrCloud in depth in chapter 13.



Install solr
===========
1. Download and extract
2. Move to opt
3. Create $SOLR_PATH variable to /opt/solr don't create $SOLR_HOME as it is use by solr by default
4. ./solr start


solr core
===========
consist of config files + lucene index files + solr transaction log file.
For our case, we can use document for one core, video for one core, audio for onee core.


- Generally solr core are defined in `solr.xml` file, from 4.4 core are autodiscovered.

- Solr also provide `core admin api` to create update and delete core programatically.


- Each solr has one and only one home directory that contains all cores.


- global java system property `solr.solr.home` set the location of solr home directory

- `solrconfig.xml` is the main configuration file to configure solr.

- `schema.xml` is the main config file that governs index.



Some concepts
=========
1. Every piece of data submitted to Solr for processing is a document
2. A document could be a newspaper article, a resume or social profile, or, in an extreme case, an entire book.
3. Solr accomplishes all of this by using an index that maps content to documents instead of mapping documents to content as in a traditional database model. This
inverted index is at the heart of how search engines work.


4. Solr’s default operator
While the default configuration in Solr assumes that a term or phrase by itself is an
optional term, this is configurable on a per-query basis using the q.op URL parameter
with many of Solr’s query handlers.
/select/?q=new house&q.op=OR versus /select?q=new house&q.op=AND
Note that if you change the default operator from OR to AND, this will switch to requir-
ing all terms specified without an explicit Boolean operator. If the default operator is
OR for the query new house, then only one of the terms is required. If the default oper-
ator is AND for the same query, then both the terms new and house are required. You
can also explicitly specify the operator between the terms (such as new AND home or
new OR home) to override the default operator. 
