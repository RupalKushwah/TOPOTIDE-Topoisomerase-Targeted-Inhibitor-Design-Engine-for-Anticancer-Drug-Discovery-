# TOPOTIDE-Topoisomerase-Targeted-Inhibitor-Design-Engine-for-Anticancer-Drug-Discovery-
Human topoisomerase IIα (hTopoIIα) is a key regulator of DNA topology and an established anticancer target. ts overexpression in multiple cancers necessitates the discovery of novel and safer inhibitors.
**Project Obejctive**
**Dataset Curation ** - A curated dataset of experimentally validated hTopoIIα inhibitors was assembled to capture relevant chemical space and guide model fine-tuning toward biologically meaningful scaffolds.
**Model Development** - A recurrent neural network (RNN)–based Long Short-Term Memory (LSTM) generative model, (**TOPOTIDE**), was developed and fine-tuned on hTopoIIα inhibitors to learn structure–activity-driven SMILES representations.
**Compound Generation** - TOPOTIDE generated 500 novel molecules, which were chemically validated using RDKit, confirming syntactic correctness and structural feasibility.
**Virtual Screening & Simulation** - The validated compounds were subjected to structure-based virtual screening through: Molecular docking and Molecular dynamics simulations
at two key binding sites of hTopoIIα:
(i) ATPase domain and
(ii) Merbarone (Merbourne) binding site

**Candidate Prioritization** - Top candidates were prioritized based on binding stability, interaction profiles, and dynamic behavior, highlighting their potential as next-generation hTopoIIα inhibitors.

