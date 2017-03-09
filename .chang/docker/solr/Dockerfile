FROM guywithnose/solr:4.2.0
MAINTAINER Kamil Politowicz <kpolitowicz@nimonik.com>

RUN mkdir ./solr/conf
COPY solr/solr.xml ./solr/
COPY solr/conf/admin-extra.html ./solr/conf/
COPY solr/conf/elevate.xml ./solr/conf/
COPY solr/conf/mapping-ISOLatin1Accent.txt ./solr/conf/
COPY solr/conf/protwords.txt ./solr/conf/
COPY solr/conf/schema.xml ./solr/conf/
COPY solr/conf/scripts.conf ./solr/conf/
COPY solr/conf/solrconfig.xml ./solr/conf/
COPY solr/conf/spellings.txt ./solr/conf/
COPY solr/conf/synonyms.txt ./solr/conf/