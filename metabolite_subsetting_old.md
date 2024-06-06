# Retrieving metabolite information

The addition of metabolite related information to biomedical knowledge graphs is gaining importance to describe and learn about genome druggability and disease pathology for several applications such as drug repurposing or disease biomarker discovery. In this BioHackathon, we have investigated how to retrieve metabolite associations from curated databases focusing on the specific use case of drug repurposing on inborn errors of metabolism disorders.

(uniprot)=
## UniProt

Here is a link [to the intro](intro.md). Here is the link to [](uniprot) section. UniProt is a comprehensive knowledge base that focuses its metabolite content on natural products.

### Exploring genome druggability


#### Retrieving drug candidates based on activity metabolite similarity
From UniProt, retrieve all human enzymes. Then the catalytic reaction and its accession ID. With this information query RHEA to retrieve reaction participants involved in metabolic pathways, and get the ChEBI IDs from both reactants and products. Then cross IDSM Sachem with these identifiers to expand these known compounds in ChEBI with similar compounds in PubChem. In PubChem we can retrieve three types of compounds: 1. known drugs that have protein targets with which have activity (useful for link prediction); 2. ChEMBL targets with known sensibility; 3. compounds with unknown relevance.

#### Retrieving drug candidates based on structural metabolite similariy
From our user metabolite drug candidates, retrieve similar ligands in PDB.

####
Explore DBCLS databases for ligands and druggability.


### Exploring disease pathology

#### Retrieval of curated disease-metabolite associations
From IMCD, retrieve a curated dataset of metabolite-disease associations. There is other the Recon models (Leiden) data source rich on this metabolite content. 

#### Retrieval of isoforms


(pubchem)=
## PubChem

Here is a link [to the intro](intro.md). Here is the link to [](pubchem) section. PubChem is a comprehensive knowledge base that focuses its metabolite content on several curated databases such as HMDB. The large amount of data and complexity of PubChem structure make the retrieval of information tailored to the user use case. Once this is clear, PubChem offers a set of tools to help users to retrieve this information in a more systematic way.


### Exploring disease pathology

#### Retrieval of curated disease-metabolite associations
Subset human metabolites from HMDB and cross this data via JOIN or UNION with ChEBI (metabolite role).
 

## Other databases 

We also asked the Plant and Microbiome communities, if there are other databases used to retrieve metabolite-related data. The plant community is focusing mainly on sequence and phenomic data for now. The microbiome community is using KEGG (enzyme sequence list of each microbe).
MS data: they don’t know that much about MS databases for microbes. Maybe no standard database. They usually obtain metabolomics data using mass spectrometry such as GC-MS, LC-MS, CE-TOF/MS, etc. Also, "metabolite-related" data also includes metabolic pathways and enzymes and the reactions they are involved in; for pathways, KEGG or MetaCyc would work, and for predicting enzymes, DeepGO or a similar system.

