===============
DSpace
===============

Metadata Mapping
================

This metadata mapping maps Dspace QDC to Primo VE DublinCore Expanded based on the
`Mapping to the Display, Facets, and Search Sections in the Primo VE Record <https://knowledge.exlibrisgroup.com/Primo/Product_Documentation/020Primo_VE/050Other_Configuration/Mapping_to_the_Display%2C_Facets%2C_and_Search_Sections_in_the_Primo_VE_Record#Dublin_Core_2>`_
and the `Configuring Import Profiles for Primo VE <https://knowledge.exlibrisgroup.com/Primo/Product_Documentation/020Primo_VE/045Loading_Records_from_External_Sources_into_Primo_VE/Configuring_Import_Profiles_for_Primo_VE>`_ documentation.

Metadata as mapped as QDC so it is easy to isolate the publication date (Regular Dublin Core has multiple dc:date values that are hard to distinguish).

+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| QDC                       | Primo VE Expanded DublinCore                                                                 | Display Field | Facets Field           | Search Field          |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:title                  | dc:title                                                                                     | Title         |                        | Title                 |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:identifier             | dc:identifier                                                                                |               |                        | General               |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dcterms:issued            | dc:date                                                                                      | Creation Date | Creation Date          | Creation Date         |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:creator                | dc:creator                                                                                   | Creator       | Creator & Contributors | Creator & Contributor |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:subject                | dc:subject                                                                                   | Subjects      | Topic                  | Subjects              |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dcterms:abstract          | dcterms:abstract                                                                             | Description   | Description            |                       |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+
| dc:contributor            | dcterms:contributor                                                                          | Contributor   | Creator & Contributors | Creator & Contributor |
+---------------------------+----------------------------------------------------------------------------------------------+---------------+------------------------+-----------------------+

Discovery Import Profile
========================

* root element tag: `ListRecords`
* record elements tag: `record`
* xpath to the identifier tag: `record/header/identifier/text()`
* base-url: `https://trace.tennessee.edu/server/oai/request`
* metadata format: `qdc`


Normalization Rules
===================

.. code-block:: xml
    :name: Sample XML Record
    :caption: Sample XML Record

    <record>
        <header>
            <identifier>oai:trace.tennessee.edu:20.500.14382/28564</identifier>
            <datestamp>2026-04-13T18:10:47Z</datestamp>
            <setSpec>com_20.500.14382_utk-grad</setSpec>
            <setSpec>com_20.500.14382_utk-coll</setSpec>
            <setSpec>col_20.500.14382_utk_graddiss</setSpec>
        </header>
        <metadata>
            <qdc:qualifieddc
                xsi:schemaLocation="http://purl.org/dc/elements/1.1/ http://dublincore.org/schemas/xmls/qdc/2006/01/06/dc.xsd http://purl.org/dc/terms/ http://dublincore.org/schemas/xmls/qdc/2006/01/06/dcterms.xsd http://dspace.org/qualifieddc/ http://www.ukoln.ac.uk/metadata/dcmi/xmlschema/qualifieddc.xsd"
                xmlns:qdc="http://dspace.org/qualifieddc/"
                xmlns:dc="http://purl.org/dc/elements/1.1/"
                xmlns:dcterms="http://purl.org/dc/terms/"
                xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
                xmlns:doc="http://www.lyncode.com/xoai">
                <dc:title>Carbon Footprint and Cost Minimization for Grid Systems Through Day-ahead
                    Order and Battery Size Optimization</dc:title>
                <dc:creator>Pourkhalili, Omid</dc:creator>
                <dc:contributor>Rapinder Sawhney</dc:contributor>
                <dc:contributor>John E. Kobza</dc:contributor>
                <dc:contributor>Andrew J. Yu</dc:contributor>
                <dc:contributor>Russell Zaretzki</dc:contributor>
                <dc:subject>Battery modeling</dc:subject>
                <dc:subject>Simulation optimization</dc:subject>
                <dc:subject>Grid systems</dc:subject>
                <dc:subject>lithium-ion battery</dc:subject>
                <dc:subject>Renewable energies</dc:subject>
                <dc:subject>polynomial regression</dc:subject>
                <dcterms:abstract>&lt;p&gt;We modeled the problem of peak hours day-ahead order for
                    smart grid companies integrating renewable energy and power storage systems.
                    This results in optimizing day-ahead order, battery storage size, and
                    consequently lowering the use of fossil fuels and emissions. The utility-scale
                    power storage can balance the difference between the day-ahead forecasts and
                    real-time consumer demand through energy arbitrage and transmission deferral for
                    peaking capacity. We define system parameters and their associated costs and run
                    a suggested algorithm to minimize the grid operating cost by optimizing
                    day-ahead order amount and battery storage capacity. The model is designed to
                    prioritize and take power resources depending on their availability and
                    associated costs in real-time. The resources include day-ahead reserve, wind
                    power, utility-scale storage system, and two-stage real-time power, which can be
                    adjusted by users based on their available resources. Multiple comparisons on a
                    finite feasible set of discrete decision variables through simulation
                    optimization provide us with the optimal day-ahead order and battery size.
                    Furthermore, the model will be tested and validated based on data provided by
                    the U.S Energy Information Association. The model can be used by grid operators
                    to evaluate their potential savings, can be used by energy regulatory agencies
                    for simulating and examining their rules and policies, and can be used by state
                    and local air pollution control agencies to evaluate the impact of different
                    energy resources such as batteries on power
                    generation.&lt;/p&gt;</dcterms:abstract>
                <dcterms:issued>2022-08-01T00:00:00Z</dcterms:issued>
                <dc:type>dissertation</dc:type>
                <dc:identifier>https://trace.tennessee.edu/handle/20.500.14382/28564</dc:identifier>
            </qdc:qualifieddc>
        </metadata>
    </record>

.. code-block:: rst
    :name: Copy title
    :caption: Copy title

    rule "Copy title"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='title']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='title']" to "dc"."title"
    end

.. code-block:: rst
    :name: Copy creator(s)
    :caption: Copy creator(s)

    rule "Copy creator(s)"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='creator']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='creator']" to "dc"."creator"
    end

.. code-block:: rst
    :name: Copy contributors
    :caption: Copy contributors

    rule "Copy contributors"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='contributor']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='contributor']" to "dcterms"."contributor"
    end

.. code-block:: rst
    :name: Copy identifier
    :caption: Copy identifier

    rule "Copy identifier"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='identifier']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='identifier']" to "dc"."identifier"
    end

.. code-block:: rst
    :name: Copy date published
    :caption: Copy date published

    rule "Copy date published"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/terms/' and local-name()='issued']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/terms/' and local-name()='issued']" to "dc"."date"
    end

.. code-block::
    :name: Copy subjects
    :caption: Copy subjects

    rule "Copy subjects"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='subject']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/elements/1.1/' and local-name()='subject']" to "dc"."subject"
    end

.. code-block::
    :name: Copy abstract
    :caption: Copy abstract

    rule "Copy abstract"
        when
            exist "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/terms/' and local-name()='abstract']"
        then
            copy "//*[local-name()='record']/*[local-name()='metadata']/*[namespace-uri()='http://dspace.org/qualifieddc/' and local-name()='qualifieddc']/*[namespace-uri()='http://purl.org/dc/terms/' and local-name()='abstract']" to "dcterms"."abstract"
    end

Normalized Record Post Import
=============================

A sample record as XML:

.. code-block:: xml
    :name: Sample XML
    :caption: A sample ETD as XML

  <record xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:dc="http://purl.org/dc/elements/1.1/">
  <dcterms:abstract>&lt;p>The limen is defined as the transitional threshold between two fixed states in cultural rites of passage or between two dissimilar spaces in architecture. The study of rites of passage provides an analogy from which principles can be drawn for the design of a transformative space. The characteristics that define liminal space include layering, dissolution, blurring, and ambiguity and have the ability to transform the occupant of that space as they move through it. The experience of liminal space poses a discontinuity and leads the occupant to question their surroundings, thus leading to heightened awareness of the space as a transformative threshold between distinct spaces.&lt;/p>
&lt;p>The design of a ballpark, a building type associated with ritual, will be the vehicle for the exploration of the design of liminal space. Attention to the individual ritualistic acts of attending a ballgame can heighten the perception of the fan and their movement through a transitional space which transforms them from their everyday life. Additionally, a blurring of the space of the fan with the space of the player and a blurring of the space of the city and the space of the game will further heighten the ambiguity. Through an analysis of precedents that address both liminal space as transformative threshold and the liminality present in the ballpark, the design of the ballpark will create a transformative space for both the player and the fan which is based in history and advances the perception of the threshold as transformative.&lt;/p></dcterms:abstract>
  <dc:date>2008-05-01T00:00:00Z</dc:date>
  <dc:identifier>https://trace.tennessee.edu/handle/20.500.14382/40681</dc:identifier>
  <dcterms:contributor>Brian Ambroziak</dcterms:contributor>
  <dcterms:contributor>Theodore Shelton</dcterms:contributor>
  <dcterms:contributor>Barbara Klinkhammer</dcterms:contributor>
  <dc:creator>Zimmerman, Patrick Troy</dc:creator>
  <dc:title>Liminal Space in Architecture: Threshold and Transition</dc:title>
  </record>
