# indeng242_final
This is the repo for the final project of INDENG242, 2020 Fall.

## Goal: 

Predict brand ranking using word embedding, and compare with other benchmarks (e.g. word frequency).

## Current Status:

DV: Interbrand brand ranking (`interbrand_brand2rankvalue.json`) from 2000 to 2019 (only use the part 2001-2019, since there are only ~80 brands on the list in 2000, whereas all other years have 100 brands). The rank is therefore from 1 to 101, with 101 denoting out-of-list brands. We will consider only brands that have appeared in the Interbrand list in at least one year.

IV:

- dynamic word embedding (Yao et al. 2018 WSDM): time-indexed word embedding, trained on New York Times articles from 1996-2019
- word frequency / ratio (`interbrand_brand2freq.json`): from 1996-2019

Models:

1. rank_t+1 (or whether on the list in t+1) ~ wordvec_t
2. rank_t+1 ~ freq_t + freq_t-1 + ... + freq_t-4
3. rank_t+1 ~ ratio_t + ratio_t-1 + ... + ratio_t-4
4. rank_t+1 ~ rank_t

Results: 4 >> 1 > 2 ~ 3

## Moving Forward

1. autoregression model
2. product satefy

## Housekeeping Notes

- Checkout branches
- Avoid deleting codes
- Clear outputs before pushing
- Make pull requests to all team members
