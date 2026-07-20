===============
Digital Commons
===============

Unique Fields from Digital Commons
==================================

Here are the results of a schema analysis from variety.js that lists the unique fields available in qdc.

+----------------------------------------------+--------------------------------------+-------------+------------------------+
| key                                          | types                                | occurrences | percents               |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| _id                                          | ObjectId                             | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata                                     | Object                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc                           | Object                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.@xmlns:dc                 | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.@xmlns:oai_dc             | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.@xmlns:xsi                | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.@xsi:schemaLocation       | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:title                  | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| oai_provider                                 | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| record_id                                    | String                               | 36974       | 100.000000000000000000 |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:identifier             | String (36672),Array (136)           | 36808       | 99.551035863038890739  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:datecreated            | String                               | 33023       | 89.314112619678695637  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:creator                | String (24970),Array (3542)          | 28512       | 77.113647427922330735  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:subject                | Array (13831),String (12434)         | 26265       | 71.036403959539129005  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:type                   | String (22454),null (73)             | 22527       | 60.926597068210092800  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:descriptionabstract    | String (17323),null (25)             | 17348       | 46.919456915670473052  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:contributor            | Array (10511),String (1961),null (1) | 12473       | 33.734516146481311694  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:thesisdegreediscipline | String                               | 11461       | 30.997457672959377817  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:thesisdegreelevel      | String                               | 10612       | 28.701249526694432745  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:thesisdegreename       | String                               | 10601       | 28.671498891112673135  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:description            | Array (451),String (6000),null (1)   | 6452        | 17.450100070319685130  |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:dateavailable          | String                               | 2088        | 5.647211554065018291   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:descriptionnote        | String (402),null (6)                | 408         | 1.103478119759831122   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:rights                 | String                               | 222         | 0.600421918104614094   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:rightslicense          | String                               | 88          | 0.238005084654081239   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:coveragespatial        | String                               | 69          | 0.186617623194677340   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:publisher              | String                               | 69          | 0.186617623194677340   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:coveragespatiallat     | String                               | 4           | 0.010818412938821876   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+
| metadata.oai_dc:dc.dc:coveragespatiallong    | String                               | 4           | 0.010818412938821876   |
+----------------------------------------------+--------------------------------------+-------------+------------------------+

Metadata Mapping
================

This metadata mapping maps Digital Commons QDC to Primo VE DublinCore Expanded based on the
`Mapping to the Display, Facets, and Search Sections in the Primo VE Record <https://knowledge.exlibrisgroup.com/Primo/Product_Documentation/020Primo_VE/050Other_Configuration/Mapping_to_the_Display%2C_Facets%2C_and_Search_Sections_in_the_Primo_VE_Record#Dublin_Core_2>`_
and the `Configuring Import Profiles for Primo VE <https://knowledge.exlibrisgroup.com/Primo/Product_Documentation/020Primo_VE/045Loading_Records_from_External_Sources_into_Primo_VE/Configuring_Import_Profiles_for_Primo_VE>`_ documentation.

Metadata as mapped as QDC so that theses advisors are searchable and viewable in the Primo record.  This is not possible
with simple dc.

+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| QDC                       | Primo VE Expanded DublinCore                                                                 | Display Field | Facets Field           | Search Field          |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:title                  | dc:title                                                                                     | Title         |                        | Title                 |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:identifier             | dc:identifier                                                                                |               |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:datecreated            | dc:date                                                                                      | Creation Date | Creation Date          | Creation Date         |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:creator                | dc:creator                                                                                   | Creator       | Creator & Contributors | Creator & Contributor |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:subject                | dc:subject                                                                                   | Subjects      | Topic                  | Subjects              |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:type                   | dc:subject                                                                                   | Subjects      | Topic                  | Subjects              |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:descriptionabstract    | dcterms:abstract                                                                             | Description   | Description            |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:contributor            | dcterms:contributor                                                                          | Contributor   | Creator & Contributors | Creator & Contributor |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:thesisdegreediscipline | dcterms:subject                                                                              | Subjects      | Topic                  | Subjects              |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:thesisdegreelevel      | if this field exists, map discovery:resourceType field to dissertationselse:  text_resources |               |                        |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:thesisdegreename       | dcterms:description                                                                          | Description   | Description            |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:description            | dc:description                                                                               | Description   | Description            |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:dateavailable          | dcterms:date                                                                                 |               |                        | Creation Date         |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:descriptionnote        | dcterms:description                                                                          | Description   | Description            |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:rights                 | dc:rights                                                                                    | Rights        |                        |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:rightslicense          | dcterms:rights                                                                               | Rights        |                        |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:coveragespatial        | dcterms:coverage                                                                             |               |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:publisher              | dcterms:publisher                                                                            | Publisher     |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:coveragespatiallat     | dcterms:spatial                                                                              |               |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:coveragespatiallong    | dcterms:spatial                                                                              |               |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+

Discovery Import Profile
========================

* root element tag: `ListRecords`
* record elements tag: `record`
* xpath to the identifier tag: `record/header/identifier/text()`
* base-url: `https://dpla.lib.utk.edu/repox/OAIHandler`
* metadata format: `oai_qdc`


Normalization Rules
===================

.. code-block:: xml
    :name: Sample XML Record
    :caption: Sample XML Record

    <record>
    <header>
    <identifier>oai:trace.tennessee.edu:utk_gradthes-1127</identifier>
    <datestamp>2010-02-01T23:31:58Z</datestamp>
    <setSpec>publication:utk_gradthes</setSpec>
    <setSpec>publication:utk-coll</setSpec>
    <setSpec>publication:utk-grad</setSpec>
    </header>
    <metadata>
    <oai_dc:dc xmlns:oai_dc="http://www.openarchives.org/OAI/2.0/oai_dc/" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="http://www.bepress.com/OAI/2.0/qualified-dublin-core/ https://resources.bepress.com/assets/xsd/oai_qualified_dc.xsd">
    <dc:title>
    The Relations of the Cherokee Indians with the English in America Prior to 1763
    </dc:title>
    <dc:creator>Buchanan, David P.</dc:creator>
    <dc:date.created>1923-12-01T08:00:00Z</dc:date.created>
    <dc:thesis.degree.level>Thesis</dc:thesis.degree.level>
    <dc:thesis.degree.name>Master of Arts</dc:thesis.degree.name>
    <dc:contributor>ARRAY(0x7f7024cfef58)</dc:contributor>
    <dc:subject>Political History</dc:subject>
    <dc:subject>Social History</dc:subject>
    <dc:subject>United States History</dc:subject>
    <dc:description.abstract>
    Thesis (M.A.) at University of Tennessee from 1923 describing relations between the Cherokee and English prior to 1763. This thesis by David Buchanan contains detailed accounts of the Cherokee nation before colonization of the Cherokee territories in the Appalachian region as well as interactions between the English army and settlers.
    </dc:description.abstract>
    <dc:identifier>https://trace.tennessee.edu/utk_gradthes/98</dc:identifier>
    </oai_dc:dc>
    </metadata>
    </record>

.. code-block:: rst
    :name: Copy First Title
    :caption: Copy First Title

    rule "copy first title"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='title']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='title'][1]" to "dc"."title"
    end

.. code-block:: rst
    :name: Copy identifiers
    :caption: Copy identifiers

    rule "copy identifiers"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='identifier']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='identifier']" to "dc"."identifier"
    end

.. code-block:: rst
    :name: Copy date created
    :caption: Copy date created

    rule "copy date created"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='date.created']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='date.created']" to "dc"."date"
    end

.. code-block:: rst
    :name: Copy Creators
    :caption: Copy Creators

    rule "copy creators"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='creator']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='creator']" to "dc"."creator"
    end

.. code-block:: rst
    :name: Copy subjects to subject
    :caption: Copy subjects to subject

    rule "copy subjects"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='subject']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='subject']" to "dc"."subject"
    end

.. code-block::
    :name: Copy types to subject since they aren't types
    :caption: Copy type to subject since they aren't types

    rule "copy types to subject"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='type']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='type']" to "dc"."subject"
    end

.. code-block::
    :name: Copy descriptionabstracts to dcterms abstract
    :caption: Copy descriptionabstracts to dcterms abstract

    rule "copy descriptionabstracts"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description.abstract']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description.abstract']" to "dcterms"."abstract"
    end

.. code-block::
    :name: Copy thesisdegreediscipline
    :caption: Copy thesisdegreediscipline

    rule "copy thesisdegreediscipline"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.discipline']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.discipline']" to "dcterms"."subject"
    end

.. code-block::
    :name: Determine resource type
    :caption: Determine resource type

    rule "determine if etd"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.level']"
        then
            set "dissertations" in "discovery"."resourceType"
    end

    rule "determine if not etd"
        when
            not exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.level']"
        then
            set "articles" in "discovery"."resourceType"
    end

.. code-block::
    :name: Copy thesisdegreename to description
    :caption: Copy thesisdegreename to description

    rule "Copy thesisdegreename"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.name']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='thesis.degree.name']" to "dcterms"."description"
    end

.. code-block::
    :name: Copy description to description
    :caption: Copy description to description

    rule "Copy description"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description']" to "dc"."description"
    end

.. code-block::
    :name: Copy dcdateavailable to dcterms:date
    :caption: Copy dcdateavailable to dcterms:date

    rule "Copy dcdateavailable to dcterms:date"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='date.available']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='date.available']" to "dcterms"."date"
    end

.. code-block::
    :name: Copy description to dc:descriptionnote
    :caption: Copy description to dc:descriptionnote

    rule "Copy description to dc:descriptionnote"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description.note']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='description.note']" to "dcterms"."description"
    end

.. code-block::
    :name: Copy rights
    :caption: Copy rights

    rule "Copy rights"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='rights']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='rights']" to "dc"."rights"
    end

    rule "Copy rightslicense"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='rights.license']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='rights.license']" to "dcterms"."rights"
    end

.. code-block::
    :name: Copy coveragespatial
    :caption: Copy coveragespatial

    rule "Copy coveragespatial"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial']" to "dcterms"."spatial"
    end

    rule "Copy coveragespatiallat"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial.lat']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial.lat']" to "dcterms"."spatial"
    end

    rule "Copy coveragespatiallong"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial.long']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='coverage.spatial.long']" to "dcterms"."spatial"
    end

.. code-block::
    :name: Copy publisher
    :caption: Copy publisher

    rule "Copy publisher"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='publisher']"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='publisher']" to "dc"."publisher"
    end

.. code-block::
    :name: Copy contributors if contributor does not contain Array
    :caption: Copy contributors if contributor does not contain Array

    rule "Copy contributors if not Array"
        when
            exist "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='contributor'][not(contains(text(), 'ARRAY'))]"
        then
            copy "/record/metadata[1]/*[namespace-uri()='http://www.openarchives.org/OAI/2.0/oai_dc/' and local-name()='dc'][1]/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='contributor']" to "dcterms"."contributor"
    end

Normalized Record Post Import
=============================

A sample record as XML:

.. code-block:: xml
    :name: Sample XML
    :caption: A sample ETD as XML

    <record>
    <header>
    <identifier>oai:trace.tennessee.edu:utk_gradthes-6890</identifier>
    <datestamp>2020-02-13T02:30:08Z</datestamp>
    <setSpec>publication:utk-coll</setSpec>
    <setSpec>publication:utk_gradthes</setSpec>
    <setSpec>publication:utk-grad</setSpec>
    </header>
    <metadata>
    <oai_dc:dc xsi:schemaLocation="http://www.bepress.com/OAI/2.0/qualified-dublin-core/ https://resources.bepress.com/assets/xsd/oai_qualified_dc.xsd">
    <dc:title>
    STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS
    </dc:title>
    <dc:creator>Singh, Vikram</dc:creator>
    <dc:date.created>2019-05-01T07:00:00Z</dc:date.created>
    <dc:thesis.degree.level>Thesis</dc:thesis.degree.level>
    <dc:thesis.degree.name>Master of Science</dc:thesis.degree.name>
    <dc:thesis.degree.discipline>Nuclear Engineering</dc:thesis.degree.discipline>
    <dc:contributor>Belle Upadhyaya</dc:contributor>
    <dc:contributor>Ondřej Chvála, Laurence Miller, Lawrence Heilbronn</dc:contributor>
    <dc:subject>molten-salt reactor</dc:subject>
    <dc:subject>dynamics</dc:subject>
    <dc:subject>modeling</dc:subject>
    <dc:subject>fission product poisoning</dc:subject>
    <dc:subject>load-following</dc:subject>
    <dc:subject>sensitivity analysis</dc:subject>
    <dc:description.abstract>
    Molten-Salt Reactors (MSR) are a Gen-IV reactor concept being investigated by companies and institutions alike. These reactors are considerably different from the current fleet of Light-Water Reactors and outside the experience base of most Nuclear Engineers. The fluid nature of the fuel leads to delayed temperature and reactivity feedback effects unique to each reactor design that need to be characterized to determine operability and safety limits. Moreover, the design space under consideration encompasses various fuel-cycles, neutron spectra, and materials. This requires a modeling methodology that can be applied to the breadth of designs under development and is the subject of ongoing research at the University of Tennessee. This thesis presents a dynamic modeling approach that was validated against experimental data from the Molten-Salt Reactor Experiment. The developed lumped-parameter models are nonlinear and represent time rate of change in mass and energy in all parts of the reactor. Reactivity feedbacks arising from changes in temperature and neutron poison concentrations are taken into account. These models can be used to study both the time and frequency response to perturbations caused during normal operating conditions and during anomalies resulting from failure of certain components. The thesis incorporates material published in a series of journal articles and conference proceedings. The validated modeling approach is detailed, and all equations and parameters of interest are listed. Three reactor systems are modeled, namely the Molten-Salt Reactor Experiment, two-fluid Molten-Salt Breeder Reactor, and a plant-level model based on the Molten-Salt Demonstration Reactor. Application of the models to studying operational anomalies, dynamic effects of xenon and samarium neutron poisons, parametric sensitivity analysis, and load-following are also presented. From the investigated perturbations for the presented designs, it is found that these systems are stable and self-regulating. Modeling results suggest that well-designed MSRs with adequate negative feedback exhibit excellent load-following characteristics that can be leveraged to engineer control systems offering a great deal of autonomy.
    </dc:description.abstract>
    <dc:description.note>
    </dc:description.note>
    <dc:identifier>https://trace.tennessee.edu/utk_gradthes/5482</dc:identifier>
    </oai_dc:dc>
    </metadata>
    </record>

The same record nomalized as JSON:

.. code-block:: json
    :name: Primo Normalized Record
    :caption: The record normalized in Primo.

    {
        "display": {
            "source": ["UTK_DigitalCommons_TRACE"],
            "type": ["dissertation"],
            "title": ["STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS"],
            "subject": ["Nuclear Engineering", "molten-salt reactor", "dynamics", "modeling", "fission product poisoning", "load-following", "sensitivity analysis"],
            "identifier": ["https://trace.tennessee.edu/utk_gradthes/5482"],
            "creator": ["Singh, Vikram"],
            "description": ["Portions of this document were previous published in journal articles and conference proceedings. This material has been incorporated here with permission from the publishers. The first page of each chapter presents a brief background on the work carried out by the author and his colleagues, and provides references to the published articles.", "Master of Science", "Molten-Salt Reactors (MSR) are a Gen-IV reactor concept being investigated by companies and institutions alike. These reactors are considerably different from the current fleet of Light-Water Reactors and outside the experience base of most Nuclear Engineers. The fluid nature of the fuel leads to delayed temperature and reactivity feedback effects unique to each reactor design that need to be characterized to determine operability and safety limits. Moreover, the design space under consideration encompasses various fuel-cycles, neutron spectra, and materials. This requires a modeling methodology that can be applied to the breadth of designs under development and is the subject of ongoing research at the University of Tennessee. This thesis presents a dynamic modeling approach that was validated against experimental data from the Molten-Salt Reactor Experiment. The developed lumped-parameter models are nonlinear and represent time rate of change in mass and energy in all parts of the reactor. Reactivity feedbacks arising from changes in temperature and neutron poison concentrations are taken into account. These models can be used to study both the time and frequency response to perturbations caused during normal operating conditions and during anomalies resulting from failure of certain components. The thesis incorporates material published in a series of journal articles and conference proceedings. The validated modeling approach is detailed, and all equations and parameters of interest are listed. Three reactor systems are modeled, namely the Molten-Salt Reactor Experiment, two-fluid Molten-Salt Breeder Reactor, and a plant-level model based on the Molten-Salt Demonstration Reactor. Application of the models to studying operational anomalies, dynamic effects of xenon and samarium neutron poisons, parametric sensitivity analysis, and load-following are also presented. From the investigated perturbations for the presented designs, it is found that these systems are stable and self-regulating. Modeling results suggest that well-designed MSRs with adequate negative feedback exhibit excellent load-following characteristics that can be leveraged to engineer control systems offering a great deal of autonomy."],
            "mms": ["9925897935302311"],
            "contributor": ["Belle Upadhyaya", "Ondřej Chvála, Laurence Miller, Lawrence Heilbronn"],
            "version": ["0"]
        },
        "control": {
            "sourcerecordid": ["9925897935302311"],
            "recordid": ["alma9925897935302311"],
            "sourceid": "alma",
            "originalsourceid": ["urn:dpla.lib.utk.edu.utk_tracerepox:f9ed25be-aef2-4b5e-b842-9aabab6f50f6"],
            "sourcesystem": ["Other"],
            "sourceformat": ["DC"],
            "score": ["1.0"]
        },
        "addata": {
            "au": ["Singh, Vikram"],
            "aucorp": ["Belle Upadhyaya", "Ondřej Chvála, Laurence Miller, Lawrence Heilbronn"],
            "abstract": ["Molten-Salt Reactors (MSR) are a Gen-IV reactor concept being investigated by companies and institutions alike. These reactors are considerably different from the current fleet of Light-Water Reactors and outside the experience base of most Nuclear Engineers. The fluid nature of the fuel leads to delayed temperature and reactivity feedback effects unique to each reactor design that need to be characterized to determine operability and safety limits. Moreover, the design space under consideration encompasses various fuel-cycles, neutron spectra, and materials. This requires a modeling methodology that can be applied to the breadth of designs under development and is the subject of ongoing research at the University of Tennessee. This thesis presents a dynamic modeling approach that was validated against experimental data from the Molten-Salt Reactor Experiment. The developed lumped-parameter models are nonlinear and represent time rate of change in mass and energy in all parts of the reactor. Reactivity feedbacks arising from changes in temperature and neutron poison concentrations are taken into account. These models can be used to study both the time and frequency response to perturbations caused during normal operating conditions and during anomalies resulting from failure of certain components. The thesis incorporates material published in a series of journal articles and conference proceedings. The validated modeling approach is detailed, and all equations and parameters of interest are listed. Three reactor systems are modeled, namely the Molten-Salt Reactor Experiment, two-fluid Molten-Salt Breeder Reactor, and a plant-level model based on the Molten-Salt Demonstration Reactor. Application of the models to studying operational anomalies, dynamic effects of xenon and samarium neutron poisons, parametric sensitivity analysis, and load-following are also presented. From the investigated perturbations for the presented designs, it is found that these systems are stable and self-regulating. Modeling results suggest that well-designed MSRs with adequate negative feedback exhibit excellent load-following characteristics that can be leveraged to engineer control systems offering a great deal of autonomy."],
            "format": ["dissertation"],
            "genre": ["dissertation"],
            "ristype": ["thes"],
            "btitle": ["STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS"]
        },
        "sort": {
            "title": ["STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS"],
            "author": ["Singh, Vikram"]
        },
        "search": {
            "rtype": "dissertations",
            "general": "https://trace.tennessee.edu/utk_gradthes/5482",
            "creator": "Singh, Vikram",
            "contributor": ["Ondřej Chvála, Laurence Miller, Lawrence Heilbronn", "Belle Upadhyaya"],
            "sort_title": "STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS",
            "subject": ["sensitivity analysis", "load-following", "fission product poisoning", "modeling", "dynamics", "molten-salt reactor", "Nuclear Engineering"],
            "description": ["Molten-Salt Reactors (MSR) are a Gen-IV reactor concept being investigated by companies and institutions alike. These reactors are considerably different from the current fleet of Light-Water Reactors and outside the experience base of most Nuclear Engineers. The fluid nature of the fuel leads to delayed temperature and reactivity feedback effects unique to each reactor design that need to be characterized to determine operability and safety limits. Moreover, the design space under consideration encompasses various fuel-cycles, neutron spectra, and materials. This requires a modeling methodology that can be applied to the breadth of designs under development and is the subject of ongoing research at the University of Tennessee. This thesis presents a dynamic modeling approach that was validated against experimental data from the Molten-Salt Reactor Experiment. The developed lumped-parameter models are nonlinear and represent time rate of change in mass and energy in all parts of the reactor. Reactivity feedbacks arising from changes in temperature and neutron poison concentrations are taken into account. These models can be used to study both the time and frequency response to perturbations caused during normal operating conditions and during anomalies resulting from failure of certain components. The thesis incorporates material published in a series of journal articles and conference proceedings. The validated modeling approach is detailed, and all equations and parameters of interest are listed. Three reactor systems are modeled, namely the Molten-Salt Reactor Experiment, two-fluid Molten-Salt Breeder Reactor, and a plant-level model based on the Molten-Salt Demonstration Reactor. Application of the models to studying operational anomalies, dynamic effects of xenon and samarium neutron poisons, parametric sensitivity analysis, and load-following are also presented. From the investigated perturbations for the presented designs, it is found that these systems are stable and self-regulating. Modeling results suggest that well-designed MSRs with adequate negative feedback exhibit excellent load-following characteristics that can be leveraged to engineer control systems offering a great deal of autonomy.", "Master of Science", "Portions of this document were previous published in journal articles and conference proceedings. This material has been incorporated here with permission from the publishers. The first page of each chapter presents a brief background on the work carried out by the author and his colleagues, and provides references to the published articles."],
            "journal_title": "STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS",
            "title": "STUDY OF THE DYNAMIC BEHAVIOR OF MOLTEN-SALT REACTORS",
            "source_code": "UTK_DigitalCommons_TRACE",
            "facet_creatorcontrib": ["Singh, Vikram", "Ondřej Chvála, Laurence Miller, Lawrence Heilbronn", "Belle Upadhyaya"],
            "sort_author": "Singh, Vikram"
        },
        "delivery": {
            "bestlocation": null,
            "holding": null,
            "electronicServices": [{
                "adaptorid": "ALMA_01",
                "ilsApiId": "urn:dpla.lib.utk.edu.utk_tracerepox:f9ed25be-aef2-4b5e-b842-9aabab6f50f6",
                "serviceUrl": "https://trace.tennessee.edu/utk_gradthes/5482",
                "licenceUrl": null,
                "licenceExist": "false",
                "packageName": "Link to Resource",
                "availiability": null,
                "authNote": null,
                "publicNote": null,
                "serviceNotAvailable": null,
                "serviceNotAvailableReason": null,
                "relatedTitle": null,
                "numberOfFiles": 0,
                "hasAccess": false,
                "serviceType": "ELECTRONIC",
                "fileType": null,
                "pdfFilesUrl": null,
                "serviceDescription": null,
                "researchFileList": null,
                "researchLinksList": null,
                "@id": null
            }],
            "quickAccessService": null,
            "deliveryCategory": ["Remote Search Resource"],
            "serviceMode": ["Viewit"],
            "availability": ["ext_not_restricted"],
            "availabilityLinks": ["directlink"],
            "availabilityLinksUrl": ["https://trace.tennessee.edu/utk_gradthes/5482"],
            "displayedAvailability": "ext_not_restricted",
            "displayLocation": null,
            "additionalLocations": null,
            "physicalItemTextCodes": null,
            "feDisplayOtherLocations": null,
            "almaInstitutionsList": [],
            "recordInstitutionCode": null,
            "recordOwner": "01UTN_KNOXVILLE",
            "GetIt1": [{
                "category": "Remote Search Resource",
                "links": [{
                    "isLinktoOnline": true,
                    "getItTabText": "service_viewit",
                    "adaptorid": "ALMA_01",
                    "ilsApiId": "urn:dpla.lib.utk.edu.utk_tracerepox:f9ed25be-aef2-4b5e-b842-9aabab6f50f6",
                    "link": "https://trace.tennessee.edu/utk_gradthes/5482",
                    "inst4opac": "",
                    "displayText": null,
                    "@id": "_:0"
                }]
            }],
            "physicalServiceId": null,
            "link": [{
                "displayLabel": "Link to Resource",
                "linkURL": "https://trace.tennessee.edu/utk_gradthes/5482",
                "linkType": "addlink",
                "publicNote": null,
                "@id": "_:0"
            }, {
                "displayLabel": "thumbnail",
                "linkURL": "",
                "linkType": "http://purl.org/pnx/linkType/thumbnail",
                "publicNote": null,
                "@id": "_:0"
            }],
            "hasD": null
        }
    }