# Homology Modelling of *Burkholderia cepacia* Biphenyl-2,3-Dioxygenase

**Course:** BEC-108 Bioinformatics · IIT Roorkee  
**Author:** Nithish Ravikkumar (23123028) · B.Tech Engineering Physics

---

## Overview

This project constructs a **3D homology model** of the *B. cepacia* biphenyl-2,3-dioxygenase (BPDO) α-subunit (BphA) and uses it to analyse the active-site accommodation of three **polychlorinated biphenyl (PCB)** congeners. Targeted *in silico* mutagenesis is performed to improve binding of a sterically restricted congener.

## Workflow

1. **Sequence retrieval** — Target: UniProt Q46372 (*B. cepacia* BphA)
2. **Homology modelling** — SWISS-MODEL, template PDB: 2XSH (Chain A)
3. **Model validation** — Ramachandran plot, residue-level energy profiling
4. **Ligand preparation** — 3D structures of 22DCB, 33DCB, 44DCB
5. **Manual docking** — PyMOL; ligands positioned near catalytic Fe(II)
6. **Interaction analysis** — Fe–ligand distances, residues within 4 Å, clash detection (PyMOL + Python)
7. **In silico mutagenesis** — PHE227→ALA via PyMOL Mutagenesis Wizard

## Key Results

| Congener | Pattern | Fe–Ligand Distance | Accommodation |
|----------|---------|--------------------|---------------|
| 22DCB | *ortho* | 2.352 Å | Favourable |
| 33DCB | *meta* | 3.331 Å | Restricted |
| 44DCB | *para* | 2.637 Å | Moderate |

- Active-site residues identified: **PHE227, PHE376, PHE382, TRP390, HIS233, HIS239, ASP386**
- **PHE227→ALA** mutation reduced 33DCB Fe–ligand distance from 3.331 Å → ~2.7 Å

## Files

```
├── bpha.png               # Homology model visualization
├── active site.png        # Active-site architecture
├── 22dcb.png              # 22DCB docking
├── 33dcb_distance.png     # 33DCB docking
├── 44dcb_final.png        # 44DCB docking
├── mutant.png             # PHE227→ALA mutant
├── report.tex             # LaTeX source
└── README.md
```

## Tools Used

- [SWISS-MODEL](https://swissmodel.expasy.org) — homology modelling
- [PyMOL](https://pymol.org) — visualisation, docking, mutagenesis
- Python — automated distance/clash extraction
