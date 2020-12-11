# OHSUMED:An interactive retrieval evaluation and new large test collection for research

## About the dataset

The OHSUMED test collection is a set of 348,566 references from
MEDLINE, the on-line medical information database, consisting of
titles and/or abstracts from 270 medical journals over a five-year
period (1987-1991). The available fields are title, abstract, MeSH
indexing terms, author, source, and publication type. The National
Library of Medicine has agreed to make the MEDLINE references in the
test database available for experimentation, restricted to the
following conditions:

1. The data will not be used in any non-experimental clinical,
library, or other setting.
2.  Any human users of the data will explicitly be told that the data
is incomplete and out-of-date.

The OHSUMED document collection was obtained by William Hersh
(hersh@OHSU.EDU) and colleagues for the experiments described in the
papers below:

Hersh WR, Buckley C, Leone TJ, Hickam DH, OHSUMED: An interactive
retrieval evaluation and new large test collection for research, 
Proceedings of the 17th Annual ACM SIGIR Conference, 1994, 192-201.

Hersh WR, Hickam DH, Use of a multi-application computer workstation
in a clinical setting, Bulletin of the Medical Library Association,
1994, 82: 382-389.

## Data Fields

Here are the field definitions:

| Column Marker | Defination | Key Name | Notes (if any)
|---|---|---|---|
|.I | sequential identifier | seq_id | (important note: documents should be processed in this order)|
|.U | MEDLINE identifier (UI) | medline_ui |(<DOCNO> used for relevance judgements) |
|.M | Human-assigned MeSH terms (MH) | mesh_terms |
|.T | Title (TI)| title |
|.P | Publication type (PT) | publication_type |
|.W | Abstract (AB)| abstract |
|.A | Author (AU)| author |
|.S | Source (SO)| source |

Note: some abstracts are truncated at 250 words and some references
have no abstracts at all (titles only). We do not have access to the
full text of the documents.
    
## Pre-processing steps
    
The train test distribution is as follows. Test data size is larger than train size!

    Train:  54,710
    Test : 293,858

Check the notebook in the repo for the pre-processing details