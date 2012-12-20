# Proposed BFO 1.2

This is a temporary home for files related to the [proposed BFO 1.2 release](https://docs.google.com/document/d/1QQsfTtzclBrW7PxMdyRGsaQ7pQZIYVkShgVRP5f4VNo/edit). [Please report bugs and suggest improvements!](https://github.com/ontodev/bfo/issues)

## bfo-1.2.owl

The bfo-1.2.owl file contains proposed classes and relations with logical axioms and annotations. We have yet to add `owl:previousVersion` annotations based on the [Mapping Spreadsheet](https://docs.google.com/spreadsheet/ccc?key=0AnbOUYWIQYUEdF9yb0hlUjhBUGRnVWNTVFJQX0xOUlE).

If your ontology uses [ruttenberg-bfo2.owl](http://purl.obolibrary.org/obo/bfo/2010-05-25/ruttenberg-bfo2.owl) then you should be able to replace that import with [bfo-1.2.owl](https://raw.github.com/ontodev/bfo/master/bfo-1.2.owl). IMPORTANT: This is a temporary URI for development purposes, and will be changed if the proposal is accepted! Please report any problems you may have.

Some of the IDs are new and we might want to revise them. See the [mapping spreadsheet](https://docs.google.com/spreadsheet/ccc?key=0AnbOUYWIQYUEdF9yb0hlUjhBUGRnVWNTVFJQX0xOUlE) for more information.

## ontology-metadata.owl

Many OBO ontologies use common metadata from the [Information Artifact Ontology (IAO)](http://information-artifact-ontology.googlecode.com/): see the [Ontology Metadata](http://code.google.com/p/information-artifact-ontology/wiki/OntologyMetadata) page for more information. This copy of the file makes a few minor changes, mainly replacing the ID for "generically dependent continuant" with its new ID.

## ro.owl

The [new OBO Relation Ontology](http://code.google.com/p/obo-relations/) contains many relations used by biomedical ontologies. The current version of RO imports ([MIREOTs](http://obi-ontology.org/page/MIREOT)) many classes and some relations from ruttenberg-bfo2. In this experimental version of the file:

- the ontology-metadata.owl import has been replaced
- a bfo-1.2.owl import has been added
- all MIREOTted BFO terms have been removed from ro.owl

The BFO 1.2 proposal was designed to make this work well. However there are a few terms from the [RO2005](http://www.obofoundry.org/ro/) paper that have been given RO IDs, but could now be mapped back to BFO IDs:

- map "adjacent to" from RO_0002220 to BFO_0001008
- map "derives from" from RO_0001000 to BFO_0001009

These mappings are noted in the [mapping spreadsheet](https://docs.google.com/spreadsheet/ccc?key=0AnbOUYWIQYUEdF9yb0hlUjhBUGRnVWNTVFJQX0xOUlE).

## iao

An experimental version of the [Information Artifact Ontology (IAO)](http://information-artifact-ontology.googlecode.com/), based on the iao-bfo2 development branch, replacing the ruttenberg-bfo2 import with bfo-1.2. Note that this uses a "magic" catalog-v001.xml file to modify import paths.

## obi

An experimental version of the [Ontology for Biomedical Investigations (OBI)](http://obi-ontology.org/), based on the development version, replacing the ruttenberg-bfo2 import with bfo-1.2. Note that this uses a "magic" catalog-v001.xml file to modify import paths.

