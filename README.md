
# CEP Phase Noise Analysis

Supplementary code for the critical review of:

> R. Lemons et al., "Carrier-envelope phase stabilization of an
> Er:Yb:glass laser via a feed-forward technique,"
> Opt. Lett. 44(22), 5610–5613 (2019).

## What this code does

Reconstructs the phase noise spectral density S_phi(f) from the
f_OOL curve of Lemons et al. Fig. 3, integrates it using the
paper's own Eq. 4 to reproduce (or attempt to reproduce) the
reported 3.5 mrad / 2.9 as headline metrics, and converts the
result to an Allan deviation sigma_y(tau).

## How to run

Install dependencies:
    pip install numpy scipy matplotlib

Run:
    python cep_noise_analysis.py

Before running, fill in the ANCHOR_PND array at the top of the
script with values read from the blue f_OOL curve in Lemons Fig. 3
at the seven frequencies in ANCHOR_F (1, 10, 100, 1k, 10k, 100k,
1M Hz). The y-axis units are rad Hz^{-1/2}.

## Key result

The reconstructed model integrates to ~45 mrad over 1 Hz to 3 MHz,
versus the paper's reported 3.5 mrad. The discrepancy and its
analysis are discussed in the review paper.

## Dependencies

- Python 3.8+
- numpy, scipy, matplotlib
