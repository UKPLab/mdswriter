# MDS_Writer_

MDSWriter is a software for manually creating multi-document summarization corpora and a platform for developing complex annotation tasks spanning multiple steps. 

_(Christian M. Meyer, Darina Benikova, Margot Mieskes, Iryna Gurevych)_

<!--
Please use the following citation:

```
@InProceedings{smith:20xx:CONFERENCE_TITLE,
  author    = {Smith, John},
  title     = {My Paper Title},
  booktitle = {Proceedings of the 20XX Conference on XXXX},
  month     = {Month Name},
  year      = {20xx},
  address   = {Gotham City, USA},
  publisher = {Association for XXX},
  pages     = {XXXX--XXXX},
  url       = {http://xxxx.xxx}
}
```
-->

> **Abstract:** In this paper, we present MDS_Writer_, a novel open-source annotation tool for creating multi-document summarization corpora. A major innovation of our tool is that we divide the complex summarization task into multiple steps which enables us to efficiently guide the annotators and to record all their intermediate results and user–system interaction data. This allows evaluating the individual components of a complex summarization system and learning from the human composition process. MDS_Writer_ is highly flexible and can be adapted to multiple other tasks.


Contact person: **Christian M. Meyer**, http://www.ukp.tu-darmstadt.de/people/meyer

Don't hesitate to send us an e-mail or report an issue, if something is broken (and it shouldn't be) or if you have further questions.

For license information, see LICENSE.txt and NOTICE.txt files.


## Documentation and Tutorial

* **Video tutorial** explaining our initial setup: http://www.youtube.com/
* **Screenshots** of the proposed seven steps for multi-document summarization: doc/screenshot_*
* Corresponding **annotation guidelines**: doc/annotation_guidelines.pdf
* Installation guide: _see below_


## Requirements

* Java 7 and higher
* J2EE platform with JavaServer Pages (JSP) and WebSocket implementations (e.g., Apache Tomcat 7 and higher)
* Maven
* MySQL database (or other SQL database)


## Installation

* Install Java, Maven, Tomcat, and MySQL.
* Download the source code from GitHub.
* Import the empty schema from doc/mdswriter_schema.sql to your database.
* Update src/main/webapp/META-INF/context.xml with your database settings.
* Update src/main/webapp/js/st.js: Set the SERVER_URL variable to the URL the software will be depolyed to.
* Build the software using 
```
mvn package
```
* Deploy the war file  from target/ to your application server.
* Open http://localhost:8080/mdswriter (or accordingly) and try to log in using admin1:admin2.
* Test if everything works and then import your own data into the schema.
