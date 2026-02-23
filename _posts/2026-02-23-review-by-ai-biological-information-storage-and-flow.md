---
layout: post
title: "Review by AI: Biological Information Storage and Flow"
date: 2026-02-23 17:05:00 -0500
categories: Blog
---

The foundational paradigm of molecular biology, the central dogma, has traditionally been defined as the unidirectional transfer of sequential information from DNA to RNA and subsequently to proteins. This linear interpretation, while sufficient for early genomic studies, is increasingly viewed as a simplification of a much more sophisticated, non-linear information-processing system. In contemporary systems biology and synthetic engineering, the DNA-RNA-protein axis is conceptualized as a robust computational substrate characterized by recursive feedback loops, high-density knowledge storage, and adaptive responses to environmental inputs.1 This biological architecture does not merely transmit data; it performs complex logic, maintains memory across generations, and exhibits a level of robustness that rivals, and in some aspects surpasses, artificial neural network architectures.4 By examining the molecular information theory underpinning these processes, we can elucidate how life operates at the theoretical limits of channel capacity while maintaining functional persistence in stochastic environments.7

## Molecular Information Theory and the Physics of Genetic Coding

The application of Shannon’s information theory to biological systems provides the mathematical rigor necessary to quantify the choices inherent in molecular recognition and signaling. Genetic information is stored digitally in a four-letter nucleotide alphabet (), providing a stable blueprint for the assembly of amino acid sequences.3 The fundamental metric of this system is the bit, representing the amount of information required to select between two equally probable states. For a DNA sequence, each position theoretically carries 2 bits of information, although evolutionary constraints and redundancy patterns suggest a balance between information density and error tolerance that approaches theoretical optima for noisy communication channels.11

## Channel Capacity and Signaling Fidelity

One of the most critical parameters in assessing the central dogma as an information flow system is channel capacity, which defines the maximum rate at which information can be reliably transmitted over a noisy medium. In the context of intracellular signaling, such as the transduction of environmental cues via G-protein-coupled receptors (GPCRs), early estimations suggested a limited capacity of approximately 1 bit per cell—essentially a binary "yes or no" response.7 However, recent high-resolution measurements of muscarinic receptor-induced calcium responses in single cells indicate that the intrinsic capacity of these pathways is significantly higher, often exceeding 2 bits.7 This suggests that a single signaling pathway can resolve at least four distinct concentration levels of an agonist, enabling the cell to mount highly nuanced responses to quantitative shifts in its environment.7
The fidelity of this information flow is maintained through molecular machines that operate close to the Shannon limit. Research into protein-DNA interactions has shown that the average information contained in DNA binding sites is often calibrated to the efficiency of the protein binding process, frequently reaching approximately 70% of the theoretical maximum.8 This high efficiency implies that biological systems have evolved to minimize energy dissipation while maximizing information gain, a principle that is vital for the survival of organisms in resource-constrained environments.14

## Dimensionality and Renormalization in Protein Folding

The transition from the linear, digital information of DNA to the functional, three-dimensional world of proteins involves a complex mapping process defined by dramatic expansions and reductions in dimensionality. The "toy model" of self-referring matter developed by Tsvi Tlusty serves as a useful framework for understanding this transition. In this model, a linear "gene" encodes the edge configuration of a spatial network of firing vertices.3 The mapping from DNA to protein (Map ) represents a dimensional expansion, where a simple sequence specifies a vast number of degrees of freedom related to three-dimensional coordinates, force fields, and conformational trajectories.3
Conversely, the functionality of the resulting protein is often governed by a small cluster of residues—the binding site—representing a drastic dimensional reduction or renormalization (Map ).3 The physical properties of the entire protein are integrated into a few effective parameters, such as binding affinity or catalytic rate. This reduction is not merely a loss of information but a focusing of "analogue" continuous dynamics back into a discrete functional output that can then refer back to the DNA (Map ) to close a feedback loop.3 This recursive mapping between the digital world of nucleic acids and the analogue world of protein chemistry forms the basis for all biological computation.3

Information Metric
	Biological Manifestation
	Theoretical Limit / Value

DNA Information Density
	Nucleotide sequence bit-rate
	~2 bits per position 11

GPCR Channel Capacity
	Agonist concentration resolution
	> 2 bits 7

Protein Specification
	Fold specification footprint
	 bits/site 15

Binding Dimensionality
	Independent molecular contacts
	~24 dimensions (EcoRI) 13

Information Efficiency
	Protein-DNA binding efficiency
	~70% of Shannon limit 8

## Architectures of Molecular Memory and Cellular Knowledge Storage

"Knowledge storage" in biological systems is not confined to the static archive of the genome. Rather, it is distributed across a hierarchy of memory systems that allow cells to record and retrieve information about their past environments.16 This multi-layered memory architecture is essential for developmental programs and adaptive responses, ensuring that transient signals are converted into sustained physiological states.16

## Cis and Trans Feedback Loops

The maintenance of cellular memory is primarily achieved through two distinct yet frequently coupled mechanisms: cis-feedback and trans-feedback loops.16
Cis-feedback loops involve physical modifications that are tethered to the DNA molecule itself, often referred to as "read-write" propagation.16 A quintessential example is DNA methylation (5mC), where the primary writer enzyme, DNMT1, is recruited to hemi-methylated DNA on the parental strand during the S phase of the cell cycle to methylate the newly synthesized daughter strand.16 This ensures that the epigenetic state is inherited across cell divisions. Similarly, histone modifications, such as the repressive H3K9me3 mark, utilize self-propagating feedback loops where writer enzymes like SUV39H1 recognize their own products via reader domains, effectively "spreading" or maintaining the mark locally.16
Trans-feedback loops, in contrast, store environmental information in the steady-state concentration of diffusible factors within the cell.16 These systems typically rely on gene regulatory networks (GRNs) where proteins, such as transcription factors, regulate their own expression or the expression of other factors to sustain a specific attractor state.16 For instance, the Nanog transcription factor in pluripotent stem cells forms an auto-regulatory loop that maintains the cell's identity even after the initial signals that established that identity have faded.16 In many repressive systems, cis and trans mechanisms are intertwined; for example, in S. pombe, small RNAs (trans-factors) cooperate with chromatin modifiers (cis-factors) to establish and maintain heterochromatin over specific genomic loci for dozens of generations.16

## Synthetic Recording via CRISPR and Retrons

The ability to engineer biological memory has been revolutionized by the repurposing of the CRISPR-Cas system as a dynamic writing tool. Unlike traditional DNA writing, which often produces random mutational outcomes, engineered systems like the Retro-Cascorder allow for the chronological recording of transcriptional events directly into the genome.20 This device utilizes engineered RNA barcodes based on prokaryotic retrons, which are reverse-transcribed by a cognate reverse transcriptase (RT) into a specific DNA "receipt" of transcription.20 These receipts are then integrated into a CRISPR array by the Cas1-Cas2 complex.20
The architectural genius of the CRISPR array lies in its linear, unidirectional expansion. New spacers (the integrated receipts) are typically added at the leader-proximal end, shifting older spacers further away.20 This physical arrangement ensures that the temporal order of gene expression events is mirrored in the linear order of DNA spacers. By sequencing these arrays at the end of an experiment, researchers can reconstruct the history of a cell's interactions with its environment—such as exposure to light, nutrients, or pollutants—without needing to destroy the cells for time-point snapshots.18

Memory System Type
	Physical Mechanism
	Persistence Characteristics

Cis-Epigenetic
	DNA/Histone modifications
	Heritable for 30+ divisions 16

Trans-Regulatory
	TF concentration/GRN attractors
	Stable until metabolic perturbation 16

CRISPR Spacer
	Sequential DNA integration
	Permanent archival record 18

Retron RT-DNA
	RNA-to-DNA conversion
	Intermediate "transcriptional receipt" 20

DNA Origami
	Nanoscale 3D patterning
	High-density encrypted storage 22

## Gene Regulatory Networks as Computational Substrates

The interaction between molecular components within the central dogma forms gene regulatory networks (GRNs) that act as the cell's computational engine.23 These networks integrate endogenous and environmental cues to determine the differentiation, development, and survival strategies of the organism.25

## Topological Motifs and Logic Gates

The structure of GRNs is not random but follows a hierarchical, scale-free topology characterized by the prevalence of specific network motifs.24 These motifs serve as the fundamental building blocks of biological logic. The most prominent is the feed-forward loop (FFL), wherein a master regulator activates an intermediate regulator, and both together modulate a target gene.24 Information-theoretic simulations suggest that FFLs maximize information flow in noisy environments by using correlated fluctuations to filter out transient perturbations.27
Synthetic biology has extended these natural motifs to create a comprehensive toolkit of biological logic gates. Using Hill equation-based modeling, researchers can design synthetic gene regulatory mechanisms (GRMs) that execute Boolean operations such as AND, OR, NOR, and NIMPLY.28 For example, a biological AND gate can be engineered using multiple transcription units where all signals must be present to initiate the expression of a reporter gene.28 These gates can be layered to perform complex computations, such as the spatial band-filtering of morphogen gradients to produce precise patterns in a tissue domain.28

## GRNs and the Reservoir Computing Paradigm

A provocative insight from recent computational biology research is that the functional architecture of GRNs, such as that of E. coli, fits within the paradigm of reservoir computing.6 Reservoir computing is a framework for neural computation where a fixed, non-linear network (the reservoir) maps input signals into a high-dimensional state space, which is then decoded by a simple readout layer.6 In the case of E. coli, the intricate web of biochemical interactions acts as the reservoir, allowing the cell to process environmental inputs into complex physiological outputs with remarkable efficiency.6
Furthermore, GRNs have been shown capable of associative learning through mechanisms formally equivalent to Hebbian learning in neural networks.31 By pairing an unconditioned stimulus (UCS) with a neutral stimulus (NS) that does not initially elicit a response, researchers have demonstrated that GRNs can be "trained" to associate the two, eventually resulting in the NS becoming a conditioned stimulus (CS) that triggers the response independently.32 This process of associative conditioning typically increases the "causal emergence" of the network—a metric derived from Integrated Information Decomposition () that measures the extent to which the whole system behaves as a unified, emergent agent.32

Network Attribute
	Biological Manifestation (GRN)
	Computational Analogue

Core Node
	Gene / Promoter complex
	Artificial Neuron / Perceptron

Interaction weight
	Transcription factor affinity
	Synaptic weight

Information Transfer
	Diffusible proteins / RNA
	Vectorized data flow

Learning Rule
	Evolutionary selection / Hebbian-like
	Backpropagation / Gradient Descent

Global Structure
	Hierarchical scale-free 24
	Layered or Recurrent Topology

## Comparative Analysis: Biological Circuits vs. Artificial Neural Networks

While artificial neural networks (ANNs) have achieved unprecedented success in digital computation, biological information systems—particularly those based on the central dogma—exhibit unique properties of robustness, energy efficiency, and adaptive memory that remain elusive in silicon.5

## Robustness, Noise, and Canalization

The hallmark of biological computation is its ability to operate reliably in the presence of extreme biochemical noise and environmental stochasticity.35 Unlike ANNs, which often prioritize high-precision weights that can be sensitive to perturbations, biological circuits utilize "sloppy" random connectivity and potential energy landscapes to ensure stability.34 In the developmental biology of multicellular organisms, this property is termed "canalization," referring to the ability of a GRN to produce a uniform phenotype even in the face of genetic variation or changing temperatures.24
Topological stability is often analyzed using the concept of a potential landscape, where functional cellular states correspond to basins of attraction.37 For a bistable toggle switch, the robustness of a state is proportional to the height of the potential energy barrier that a cell must cross to spontaneously switch states.37 As the unbinding rates of proteins from their DNA targets decrease relative to their synthesis rates, these barriers become higher, effectively shielding the "memory" of the switch from thermal fluctuations and shot noise inherent in low-copy-number molecular regimes.9

## Architectural Bottlenecks: The Hourglass Principle

Both biological and neural systems frequently employ an "hourglass" or "bow-tie" architecture to manage high-dimensional data.34 In this design, a diverse array of inputs is condensed into a narrow "waist" of common protocols or intermediates before being expanded again into a diverse set of outputs.34
For example, the metabolic network of a cell reduces thousands of different nutrient inputs into 12 core intermediates (such as pyruvate or acetyl-CoA), which then serve as the universal building blocks for synthesizing the entire proteome and lipidome.34 Similarly, in the immune system, the vast diversity of potential molecular pathogens is reduced to signals detected by a limited set of toll-like receptors and interleukins to coordinate a systemic response.34 In neural networks, this process is analogous to autoencoders or dimensional reduction layers that filter out noise and irrelevant variations to focus on essential features, thereby enhancing the system's ability to generalize to novel situations.34

Feature
	Artificial Neural Network (ANN)
	Biological Circuit (DNA-RNA-Protein)

Speed
	Megahertz / Gigahertz (Electricity)
	Millihertz (Biochemical reaction) 41

Energy Consumption
	High (Watts to Kilowatts)
	Extremely Low (picoWatts/cell) 33

Learning Phase
	Explicit Training vs. Inference
	Continual, concurrent with function 33

State Persistence
	Static weights
	Dynamic basins of attraction 37

Memory Loss
	Catastrophic forgetting
	Evotype buffering / phenotypic canalization 35

## Synthetic Circuit Design and Advanced Logic Implementation

The field of synthetic biology has transitioned from building isolated logic gates to designing complex sequential circuits and finite state machines that can execute multi-step programs within living cells.4

## The Evolution of the JK-Latch and Memory Devices

The construction of the synthetic biological JK-Latch represents a milestone in engineering sequential logic.45 While the basic toggle switch (RS-Latch) provides simple memory, the JK-Latch is a more advanced device where all entries of its truth table are defined, including the "toggle" state.45 Designers have utilized two primary strategies for its implementation:
Rational Design: This approach mirrors digital electronics by utilizing two positive feedback loops from the outputs back to synergistically activated promoters, requiring four two-regulated promoters and specific parts like araC, luxR-luxI, and λ-cro.45
Computational Evolution: Using Monte Carlo Simulated Annealing, researchers have evolved novel topologies that optimize parameters to meet the JK-Latch requirements with higher efficiency.45 The evolved version often requires fewer regulated promoters (e.g., three instead of four) by leveraging cross-layer feedback between distant components of the circuit.45

## CAD Platforms for Genetic Circuit Automation

The complexity of designing these circuits has necessitated the development of sophisticated computer-aided design (CAD) tools, such as Cello 2.0.46 Cello provides a complete design automation pipeline that allows users to specify desired circuit behavior using the Verilog hardware description language.46 The software then performs:
Logic Synthesis: Converting Verilog into a technology-independent Boolean gate netlist.
Technology Mapping: Selecting specific characterized biological parts (promoters, repressors, ribozymes) from a library to implement the netlist.46
Genome Placement: Determining the physical location of genetic elements within the host genome according to formal rules that minimize interference.47
Crucially, modern tools like Cello 2.0 and iBioSim account for "context effects" such as promoter interference, metabolic burden, and cell-to-cell variability.48 By scoring circuits based on their predicted output distributions rather than just median parameters, these systems ensure that synthetic devices function robustly across different growth conditions and genetic backgrounds.46

## The Central Dogma as an Environmental Response Substrate

Living systems utilize the central dogma not just for homeostasis but to navigate and transform their environments.25 This "info-autopoiesis" involves the continuous transformation of endogenous semantic information into exogenous syntactic structures, such as the creation of specialized metabolic enzymes in response to specific sugars.24

## Spatial Patterning and Positional Information Interpretation

In multicellular development, the central dogma serves as the substrate for spatial computation.28 Cells must interpret their position within a tissue to differentiate correctly. This is achieved by sensing orthogonal morphogen gradients, which act as high-dimensional environmental inputs.28 Engineered GRMs can be designed to interpret these signals and produce stable spatial patterns, such as the "French Flag" model or more complex characters.28
These spatial computers utilize Hill equation building blocks to integrate multiple inputs. For instance, AND-gate logic is implemented by multiplying Hill terms in the numerator of the rate equation, ensuring that multiple positive regulators must be present for gene expression.28 Conversely, OR-gate logic combines terms through summation and multiplication, allowing either signal to drive the output.28 This continuous, non-linear modeling allows for the systematic design of circuits that can interpret complex positional cues to organize body structures or synthetic biomaterials.28

## Genomic Foundation Models: Life-Code and Multi-Omics

The future of understanding the central dogma as a computational substrate lies in integrated multi-omics modeling.53 Foundation models such as Life-Code attempt to co-represent DNA, RNA, and protein sequences within a single latent embedding space.53 By reverse-transcribing RNA and reverse-translating amino acids back into a unified nucleotide-based sequence format, Life-Code can capture the complex interactions between coding and non-coding regions using masked language modeling.53
This approach enables the transfer of knowledge across different biological functions, allowing the model to learn regulatory motifs, translational signals, and protein folding patterns simultaneously.15 Benchmarking these foundation models on large-scale datasets like NABench—which curates millions of sequences to predict functional fitness—is becoming the gold standard for assessing our ability to "read" and "write" the computational language of life.56

Modeling Approach
	Core Technology
	Primary Application

Differential Equations (ODEs)
	Mass-action kinetics / Hill equations
	Dynamic simulation of small circuits 59

Boolean Networks
	Logical state transitions
	Large-scale qualitative GRN mapping 24

Graph Neural Networks (GNNs)
	Latent node/edge representations
	Inference of TF-target relationships 23

Transformer-based Models
	Attention mechanisms / Unified omics
	Sequence-to-function fitness prediction 53

Potential Landscape Analysis
	Steady-state probability distributions
	Robustness and stability assessment 37

## Thermodynamic and Information-Theoretic Limits of Biological Systems

Biological computation is ultimately constrained by the physical laws of thermodynamics and the statistical limits of information transmission.11

## Energy-Information Conversion in Protein Folding

The specification of a protein's functional fold is a major information-theoretic challenge. Evolved proteins contain approximately  bits per site of information relative to a random sequence, which is nearly identical to the information required to select the folded state from the myriad of possible unfolded configurations—a result that quantifies the "information footprint" of natural selection.15 The energy-to-information conversion efficiency of this process is roughly 50%, an impressive figure when compared to the sub-1% efficiency of most human-made electronic processors.15 This efficiency is essential for the cell, as gaining each bit of information requires dissipating energy as heat (), placing a fundamental floor on the metabolic cost of cellular "thinking".14

## Saturation Effects and Decision Entropy

In high-stress environments, biological systems often utilize saturation as a control mechanism to minimize decision entropy.65 Information-theoretic analysis of the UV damage response in E. coli demonstrates that when a master regulator like RecA is active, it drives the integrator signal (CII) either far above its activation threshold or far below it.65 This effectively "preempts" the decision space, compressing continuous environmental signals into a highly biased, near-deterministic outcome (98% lysogenic or 85% lytic).65 This saturation-dependent control reduces the predictive value of individual intermediate components while maximizing the robustness of the global population response, illustrating how life manages information efficiency through non-linear thresholding.65

## Future Directions: DNA as a Computational and Archival Medium

The investigation of the central dogma has paved the way for the development of entirely new computational technologies that utilize biological molecules as substrates for non-biological tasks.17

## Ultra-Dense Data Storage and Molecular Encryption

DNA's extreme data density—storing up to 215 petabytes per gram—and its millennial longevity make it an ideal candidate for archival storage.22 Beyond simple sequence-based storage, researchers at Arizona State University have developed "shape-based" storage systems.22 In this paradigm, information is encoded in the precise 3D arrangement of DNA origami structures.22 These structures act as physical letters in an alphabet that can be read using high-speed electronic sensors or super-resolution microscopy.22 This "molecular code" offers powerful encryption, as the information is impossible to retrieve without the correct reference patterns and specialized reading tools.22

## In Vivo Biocomputing and Nano-Robotics

The synergy between DNA, RNA, and protein components is being harnessed to create autonomous nanocomputing agents (NCAs) for therapeutic applications.68 These agents can be programmed to sense a combination of disease biomarkers as inputs and execute a logical decision to release a drug payload only when specific conditions are met.42 For example, protein logic gates integrated into nano-robots can monitor the surface proteins of circulating cells and selectively target abnormal cells while sparing healthy tissue.66 Furthermore, the development of "neuron-on-a-chip" platforms, which integrate lab-grown brain organoids with silicon microchips, represents the most advanced frontier of biocomputing, offering the potential for neuromorphic learning systems that consume electricity equal only to a light bulb.42

## Conclusion

The exploration of the central dogma as a robust system for information flow and knowledge storage reveals a biological architecture of unparalleled complexity and resilience. By moving beyond a linear sequence to a recursive, feedback-driven model, we find that life operates at the theoretical frontier of information theory, utilizing cis and trans feedback loops to maintain cellular memory and developmental trajectories across generations.3 The topological similarities between gene regulatory networks and neural networks, coupled with the emergent properties of causal agency and associative learning, suggest that the principles of intelligence are deeply embedded in the molecular fabric of the cell.6 As synthetic biology continues to advance, the ability to program these biological substrates using sophisticated CAD tools and to leverage the extreme data density of DNA for archival storage will likely transform both our technological capabilities and our fundamental understanding of the logic of living matter.22

## Works cited

Development of the Central Dogma Concept Inventory (CDCI) Assessment Tool - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC4909347/
5. How to Interpret Biological Model Figures: Information flow - LabXchange, accessed February 20, 2026, https://www.labxchange.org/library/pathway/lx-pathway:5d529e8d-0042-46f4-a79e-3ab067c14610/items/lb:LabXchange:d4447b11:html:1/59948
Self-referring DNA and protein: a remark on physical and ..., accessed February 20, 2026, https://royalsocietypublishing.org/rsta/article/374/2063/20150070/115208/Self-referring-DNA-and-protein-a-remark-on
From Toggle Switches To Synthetic Multicellular Systems The Evolution Of Genetic Circuit Design - Hilaris Publisher, accessed February 20, 2026, https://www.hilarispublisher.com/open-access/impact-of-polymorphism-and-particle-size-on-the-bioavailability-of-active-pharmaceutical-ingredients-115341.html
Difference between ANN and BNN - GeeksforGeeks, accessed February 20, 2026, https://www.geeksforgeeks.org/machine-learning/difference-between-ann-and-bnn/
Structural determinants of soft memory in recurrent biological networks - arXiv, accessed February 20, 2026, https://arxiv.org/html/2502.13872v1
High capacity in G protein-coupled receptor signaling - PMC - NIH, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC5830429/
A brief review of molecular information theory - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC3220916/
Noisy active matter - arXiv, accessed February 20, 2026, https://arxiv.org/html/2508.16031v1
Information theory applications for biological sequence analysis - Oxford Academic, accessed February 20, 2026, https://academic.oup.com/bib/article/15/3/376/183705
The Genetic Code Paradox: Extreme Conservation Despite Demonstrated Flexibility - arXiv, accessed February 20, 2026, https://arxiv.org/html/2507.01139v1
Claude Shannon: Biologist [information theory used in biology] - ResearchGate, accessed February 20, 2026, https://www.researchgate.net/publication/3246170_Claude_Shannon_Biologist_information_theory_used_in_biology
A brief review of molecular information theory | Request PDF - ResearchGate, accessed February 20, 2026, https://www.researchgate.net/publication/51824105_A_brief_review_of_molecular_information_theory
Brief Review of Molecular Information Theory | Cytognomix, accessed February 20, 2026, https://www.cytognomix.com/wp-content/uploads/2014/04/BriefReviewOfMolecularInformationTheory-1.pdf
Molecular information theory meets protein folding - NASA Technical Reports Server (NTRS), accessed February 20, 2026, https://ntrs.nasa.gov/api/citations/20230002642/downloads/Molecular_information_theory_meets_protein_folding.pdf
The epigenetic circle: feedback loops in the maintenance of cellular ..., accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC12366239/
Beyond Silicon: The Advent of Biomolecular Computing ..., accessed February 20, 2026, https://www.biotech-asia.org/vol20no4/beyond-silicon-the-advent-of-biomolecular-computing/
Emerging applications for DNA writers and molecular recorders - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC6995688/
Transcription and DNA-Protein Binding - Biological Modeling, accessed February 20, 2026, https://biologicalmodeling.org/motifs/transcription
Recording gene expression order in DNA by CRISPR addition of ..., accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC9357182/
Recording Biological Information with CRISPR–Cas Systems - ETH Research Collection, accessed February 20, 2026, https://www.research-collection.ethz.ch/bitstreams/255a8580-ccd3-4dc6-912f-a5ec993e6417/download
DNA provides a solution to our enormous data storage problem - ASU News, accessed February 20, 2026, https://news.asu.edu/20260128-science-and-technology-dna-shapes-designed-store-and-protect-information
Analysis of Gene Regulatory Networks from Gene Expression Using Graph Neural Networks - arXiv.org, accessed February 20, 2026, https://arxiv.org/pdf/2409.13664
Gene regulatory network - Wikipedia, accessed February 20, 2026, https://en.wikipedia.org/wiki/Gene_regulatory_network
Machine learning methods for gene regulatory network inference - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC12449054/
Q&A: How do gene regulatory networks control environmental responses in plants? - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC5894133/
Cross Talk and Interference Enhance Information Capacity of a Signaling Pathway - NIH, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC3870809/
Automatic design of gene regulatory mechanisms for spatial pattern ..., accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC10402059/
The switch‐liker's guide to plant synthetic gene circuits - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC11887007/
Engineering robust and tunable spatial structures with synthetic gene circuits - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC5314756/
Associative memory in gene regulation networks - ePrints Soton, accessed February 20, 2026, https://eprints.soton.ac.uk/339763/
(PDF) Associative conditioning in gene regulatory network models ..., accessed February 20, 2026, https://www.researchgate.net/publication/393539997_Associative_conditioning_in_gene_regulatory_network_models_increases_integrative_causal_emergence
What is the difference between biological and artificial neural networks?, accessed February 20, 2026, https://psychology.stackexchange.com/questions/7880/what-is-the-difference-between-biological-and-artificial-neural-networks
Circuit design in biology and machine learning. I. Random networks and dimensional reduction | Evolution | Oxford Academic, accessed February 20, 2026, https://academic.oup.com/evolut/article/79/8/1403/8152771
Mechanisms of robustness in gene regulatory networks involved in neural development, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC9940843/
Stochastic gene expression and its consequences - PMC - NIH, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC3118044/
Potential Energy Landscape and Robustness of a Gene Regulatory Network: Toggle Switch, accessed February 20, 2026, https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.0030060
Learning stochastic processes with intrinsic noise from cross-sectional biological data | PNAS, accessed February 20, 2026, https://www.pnas.org/doi/10.1073/pnas.2420621122
Biological Robustness: Paradigms, Mechanisms, and Systems Principles - PMC - NIH, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC3350086/
Limits to positional information in boundary-driven systems - arXiv.org, accessed February 20, 2026, https://arxiv.org/html/2405.04381v2
Synthetic biological toggle circuits that respond within seconds and teach us new biology - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC8434798/
Biological Computation: Convergence of Molecular Logic, Neuromorphic Architecture, and Systems Theory | by Faruk Alpay, accessed February 20, 2026, https://lightcapai.medium.com/biological-computation-convergence-of-molecular-logic-neuromorphic-architecture-and-systems-b59213181794
This video gives a great rundown on the similarities and difference between biological neurons & and neural networks... and why we still can't make computers as powerful as brains. : r/IsaacArthur - Reddit, accessed February 20, 2026, https://www.reddit.com/r/IsaacArthur/comments/10zt32o/this_video_gives_a_great_rundown_on_the/
Genetic circuits in synthetic biology: broadening the toolbox of regulatory devices - Frontiers, accessed February 20, 2026, https://www.frontiersin.org/journals/synthetic-biology/articles/10.3389/fsybi.2025.1548572/full
Computational design of digital and memory biological devices - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC2553324/
MIT Open Access Articles Genetic circuit design automation with Cello 2.0, accessed February 20, 2026, https://dspace.mit.edu/bitstream/handle/1721.1/148592/Cello%202.0%20Manuscript.pdf?sequence=2&isAllowed=y
(PDF) Genetic circuit design automation with Cello 2.0 - ResearchGate, accessed February 20, 2026, https://www.researchgate.net/publication/358801979_Genetic_circuit_design_automation_with_Cello_20
Robustness and reproducibility of simple and complex synthetic logic circuit designs using a DBTL loop - Oxford Academic, accessed February 20, 2026, https://academic.oup.com/synbio/article/8/1/ysad005/7091610
Automated Design of Robust Genetic Circuits: Structural Variants and Parameter Uncertainty, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC8689692/
Programming Escherichia coli to function as a digital display, accessed February 20, 2026, https://d-nb.info/1261920783/34
iBioSim | Documentation - Genetic Logic Lab, accessed February 20, 2026, https://geneticlogiclab.org/ibiosim.github.io/
The Central Dogma of Information - MDPI, accessed February 20, 2026, https://www.mdpi.com/2078-2489/13/8/365
Life-Code: Central Dogma Modeling with Multi-Omics Sequence Unification - arXiv.org, accessed February 20, 2026, https://arxiv.org/html/2502.07299v1
Artificial Intelligence-Assisted Omics Techniques in Plant Defense: Recent Advancements and Future Prospects - CABI Digital Library, accessed February 20, 2026, https://www.cabidigitallibrary.org/doi/10.1079/9781800628649.0007
Biomedical Foundation Model: A Survey - arXiv, accessed February 20, 2026, https://arxiv.org/html/2503.02104v1
NABench: Large-Scale Benchmarks of Nucleotide Foundation Models for Fitness Prediction, accessed February 20, 2026, https://arxiv.org/html/2511.02888v1
j-andrews7/awesome-bioinformatics-benchmarks - GitHub, accessed February 20, 2026, https://github.com/j-andrews7/awesome-bioinformatics-benchmarks
Comparison of state-of-the-art error-correction coding for sequence-based DNA data storage - bioRxiv.org, accessed February 20, 2026, https://www.biorxiv.org/content/10.1101/2025.07.11.664297v1.full.pdf
Construction of Gene Regulatory Networks Using Recurrent Neural Networks and Swarm Intelligence - PMC - PubMed Central, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC4889854/
Exploring Synthetic Biology with a Genetic Toggle Switch Simulator! - Reddit, accessed February 20, 2026, https://www.reddit.com/r/biology/comments/1jc0s7m/exploring_synthetic_biology_with_a_genetic_toggle/
A Review of Modeling Techniques for Genetic Regulatory Networks - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC3592506/
Deep learning-based cell-specific gene regulatory networks inferred from single-cell multiome data - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC11879466/
GT-GRN: a graph transformer framework for enhanced gene regulatory network inference via multimodal embedding of expression data and existing network knowledge - Oxford Academic, accessed February 20, 2026, https://academic.oup.com/bib/article/26/6/bbaf584/8317403
Stability and Robustness of Unbalanced Genetic Toggle Switches in the Presence of Scarce Resources - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC8064337/
Hierarchical Preemption: A Novel Information-Theoretic Control Mechanism in Lambda Phage Decision-Making - arXiv, accessed February 20, 2026, https://arxiv.org/html/2512.22415
How Biocomputing Can Transform the World Around Us. - MedReport Foundation, accessed February 20, 2026, https://www.medreport.foundation/post/how-biocomputing-can-transform-the-world-around-us
Bio-Computing & DNA Data Storage - Human-Centered Change and Innovation, accessed February 20, 2026, https://bradenkelley.com/2025/12/bio-computing-dna-data-storage/
Autonomous Nucleic Acid and Protein Nanocomputing Agents Engineered to Operate in Living Cells | ACS Nano - ACS Publications, accessed February 20, 2026, https://pubs.acs.org/doi/10.1021/acsnano.4c13663
Autonomous Nucleic Acid and Protein Nanocomputing Agents Engineered to Operate in Living Cells - PMC, accessed February 20, 2026, https://pmc.ncbi.nlm.nih.gov/articles/PMC11757000/

---

*Source note: This blog post is an AI-generated review by ChatGPT 5.2 Deep Research.*
