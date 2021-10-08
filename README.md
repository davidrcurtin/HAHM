# HAHM
SM + Dark Vector + Dark Higgs Madgraph5 Model


A very simple extension of the standard model involves adding a "dark" U(1) gauge group that is broken by a dark higgs vev. The "dark vector" ZD can then kinetically mix with the U(1)B gauge boson, and the "dark higgs" S (or hS) can mix with the SM doublet higgs via the higgs portal |H|2|S|2 operator. (For a more complete definition see here.) This can induce a variety of exotic higgs decays like
h  → Z ZD (if kinetic mixing dominates)
h → ZD ZD (if higgs mixing dominates)
h → S S     (if higgs mixing dominates)

S inherits its decay modes from the SM higgs, while ZD couples proportional to gauge charge, giving lepton-rich final states. Cascades like h → S S → ZDZDZDZD are also possible, giving 8 lepton final states.

This model has been studied in the literature, see e.g.Wells et al. 0801.3456, 0803.1243.

Our Exotic Higgs Decays Working Group published a large survey (1312.4992) of possible exotic higgs decay modes, which also considers decays in the SM + Dark Vector + Dark Higgs model.

To facilitate experimental study of these interesting channels we have constructed a Madgraph5 model to implement this SM extension.


Madgraph 5 Model
The model is constructed using FeynRules 2.0.23. It is originally based on the HAHM Model (https://feynrules.irmp.ucl.ac.be/wiki/HiddenAbelianHiggsModel), but has been extensively modified to correct typos
implement self-consistent derivation of all mixing angles from MZ, MZD, Mh, MhS mass eigenvalue inputs
go beyond the small-mixing-approximation
adopt a definition of mixing angles so that, for small higgs/kinetic mixing << 1, the corresponding mixing angles will also be << 1 regardless of whether the h/Z is heavier or lighter than hS/ZD, and
self-consistently modify SM relations that result from Z-ZD mixing in two different ways (shift W-mass or Weinberg angle)
It has also been combined with the Higgs Effective Theory Model (https://feynrules.irmp.ucl.ac.be/wiki/HiggsEffectiveTheory) to add the effective hgg and hγγ operators.

This MG model can also be used to generate NMSSM-type decays like h→SS→4b by setting kinetic mixing to be tiny (don't use exactly zero, it causes errors), and similarly to generate pure kinetic mixing phenomenology by setting the higgs mixing to zero.

This model has been verified to reproduce results obtained from analytical expressions for various decay widths.

* HAHM_MG5model_v1: includes pdf manual with explicit usage instructions at the end)
* HAHM_MG5model_v2: includes nonzero electron and muon yukawa couplings to simulate hs > mumu etc
* HAHM_MG5model_v3: includes nonzero muon and yukawa MASSES to properly simulate zp > mumu etc at very low zd masses
* HAHM_variableMW_v4_YUKseparate: includes Yukawa couplings for all generations of leptons

If you have questions about the model please email David Curtin (david.r.curtin@gmail.com).

0th order tip: don't set any of the mixing angles to exactly zero :). Use 10^-10 or something instead if you don't want that mixing.


Branching Ratio Tables:
In "Illuminating Dark Photons with High-Energy Colliders" (Curtin, Essig, Gori, Shelton, arXiv:1412.0018) we compute the dark photon total width and branching ratio to leptons Br(ZD->ll) including QCD corrections, using PDG experimental data for mZD < 12 GeV, and by repurposing the calculations of hep-ph/0005139 for mZD > 12 GeV. We also compute the exotic higgs decay branching ratios Br(h->ZdZ*->4l) and Br(h->ZdZd->4l).

All of these computed widths and branching ratios can be downloaded in the HiggsedDarkPhoton_BrTableData.txt file.

(See our paper for more details.)


References:
If you use this MG model in your own theory study or experimental analysis, please cite the following references:
* "Exotic Decays of the 125 GeV Higgs Boson" by Curtin, Essig, Gori, Jaiswal, Katz, Liu, Liu, McKeen, Shelton, Strassler, Surujon, Tweedie and Zhong. (arXiv:1312.4992)
* "Illuminating Dark Photons with High-Energy Colliders", by Curtin, Essig, Gori, Shelton (arXiv:1412.0018)
