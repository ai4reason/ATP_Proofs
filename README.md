# Interesting ATP Proofs
 

### Lipschitzian is uniformly continuous: 
http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ncfcont2.html#T25

E proof: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t25_ncfcont2
261 axioms, 373 initial clauses, 1534 processed, 11.2 generated, 38s, 135 proof clause steps, 36/79 initial proof flas/clauses, lots of calculation

### epsilon-delta continuity in metric spaces

for f being Function of TopSpaceMetr N, TopSpaceMetr M st f is continuous holds 
for r being Real for u being Element of N for u1 being Element of M st r > 0 & u1 = f . u holds
ex s being Real st s > 0 & for w being Element of N for w1 being Element of M st w1 = f . w & dist (u,w) < s holds dist (u1,w1) < r 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/uniform1.html#T4

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t4_uniform1

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_65-query256-ctx768-w0-coop$ less t4_uniform1


```
# Proof object clause steps            : 136
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 137
# Parsed axioms                        : 223
# Initial clauses in saturation        : 359
# Processed clauses                    : 1545
# ...remaining for further processing  : 1115
# Generated clauses                    : 4956
# ...of the previous two non-trivial   : 4528
# User time                : 9.304 s
```



### Enigma learns to count: 
for r being real number st 0 <= r & r <= 2 * PI & sin r = 1 holds r = PI / 2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos6.html#T28

E proof: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_sin_cos6
2175 proc, 30.6k generated, 27s, 185 steps, 71 clauses and 63 flas, - lots of calculation

### Another counting:

0 <= x & x < 2 * PI & cos x = 0 & not x = PI / 2 implies x = (3 / 2) * PI

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/comptrig.html#T18

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t18_comptrig

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t18_comptrig

```
# Proof object clause steps            : 185
# Proof object initial clauses used    : 66
# Proof object initial formulas used   : 58
# Proof object simplifying inferences  : 179
# Parsed axioms                        : 372
# Initial clauses in saturation        : 457
# Processed clauses                    : 4849
# ...remaining for further processing  : 2524
# Generated clauses                    : 31905
# ...of the previous two non-trivial   : 26657
# User time                : 22.328 s
```


### Convergence in metric space and in its induced topology are the same

S is_convergent_in_metrspace_to x iff S is_convergent_to x

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/frechet2.html#T28

E proof (using lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_frechet2.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l3600-e0.15+coop-mzr02$ less t28_frechet2.out

```
# Proof object clause steps            : 199
# Proof object initial clauses used    : 63
# Proof object initial formulas used   : 28
# Parsed axioms                        : 308
# Initial clauses in saturation        : 496
# Processed clauses                    : 4243
# ...remaining for further processing  : 3165
# Generated clauses                    : 26575
# ...of the previous two non-trivial   : 26184
# User time                : 12.699 s
```

### Category theory: inverse of a composed natural equivalence is the composition of inverses

for k being natural_equivalence of F1,F3 st k = e1 \`\*\` e & F1,F2 are_naturally_equivalent & F2,F3 are_naturally_equivalent holds k " = (e ") \`\*\` (e1 ")

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/functor3.html#T42

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t42_functor3.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l900-e0.15+coop-mzr02$ less t42_functor3.out 

```
# Proof object clause steps            : 263
# Proof object initial clauses used    : 64
# Proof object initial formulas used   : 32
# Proof object generating inferences   : 101
# Proof object simplifying inferences  : 744
# Parsed axioms                        : 182
# Initial clauses in saturation        : 305
# Processed clauses                    : 2299
# ...remaining for further processing  : 1230
# Generated clauses                    : 17490
# ...of the previous two non-trivial   : 15995
# User time                : 7.552 s
```

### Groups: a is in center iff its conjugacy class is {a}

a in center G iff con_class a = {a}

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_5.html#T81

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t81_group_5.out

(base) mptp@air-03:/home/yan/local/ENIGMA/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l6400-e0.15+coop-mzr02$ less t81_group_5.out

```
# Proof object clause steps            : 149
# Proof object initial clauses used    : 40
# Proof object initial formulas used   : 26
# Proof object simplifying inferences  : 127
# Parsed axioms                        : 199
# Initial clauses in saturation        : 336
# Processed clauses                    : 1888
# ...remaining for further processing  : 1269
# Generated clauses                    : 11359
# ...of the previous two non-trivial   : 10722
# User time                : 4.286 s
```

### if G/N and N are p-groups then G is also a p-group

for p being prime Nat for G being finite Group
for N being normal Subgroup of G st N is p -group & G ./. N is p -group holds
G is p -group

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/groupp_1.html#T18

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t18_groupp_1

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_45-query128-ctx768-w0-coop$ less t18_groupp_1
```
# Proof object clause steps            : 117
# Proof object initial clauses used    : 63
# Proof object initial formulas used   : 45
# Proof object simplifying inferences  : 127
# Parsed axioms                        : 256
# Initial clauses in saturation        : 394
# Processed clauses                    : 2281
# ...remaining for further processing  : 1491
# Generated clauses                    : 7090
# ...of the previous two non-trivial   : 6718
# User time                : 18.720 s
```


### Groups with sets: 
for a being Element of G for H being Subgroup of G holds ( a in H iff a * H = carr H )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_2.html#T113
E proof: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t113_group_2
217 fof axioms, 298 initial clauses, 1214 nontriv given, 8523 nontriv gener, 109 proof clause steps, 28/44 initial proof flas/clauses


### Enigma differentiates: (ln * cos) \`| Z) . x = - (tan x) 

Nice theorem about the derivation of ln(cos) proved by Enigma/lgb in loop2 (IJCAR'20 experiments):

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_4.html#T42

The E proof is at http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t42_fdiff_4.out

It takes 190 clausal inferences and 37 fof axioms (52 clauses). The original problem size is 268 axioms (348 clauses). The search took 2k nontrivial given-clause loops and generated (only) 14k nontrivial clauses.


### Another on Enigma differentiating

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos9.html#T89

((ln * arctan) \`| Z) . x = 1 / ((1 + (x ^2)) * (arctan . x)) ) )

http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t89_sin_cos9

```
% Proof object clause steps            : 143
% Proof object initial clauses used    : 62
% Proof object initial formulas used   : 45
% Parsed axioms                        : 643
% Initial clauses in saturation        : 834
% Processed clauses                    : 4037
% ...remaining for further processing  : 2341
% Generated clauses                    : 18764
% ...of the previous two non-trivial   : 16507
% User time                : 28.020 s
```

### And another

(arctan * exp_R) \`| Z) . x = (exp_R . x) / (1 + ((exp_R . x) ^2))  

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos9.html#T115

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t115_sin_cos9

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t115_sin_cos9 

```
# Proof object clause steps            : 164
# Proof object initial clauses used    : 76
# Proof object initial formulas used   : 60
# Proof object simplifying inferences  : 159
# Parsed axioms                        : 634
# Initial clauses in saturation        : 819
# Processed clauses                    : 3115
# ...remaining for further processing  : 1932
# Generated clauses                    : 23735
# ...of the previous two non-trivial   : 18126
# User time                : 20.156 s
```

### Another differentiation: (exp (arctan + arccot))' = 0

(exp_R * (arctan + arccot)) \`| Z) . x = 0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_11.html#T55

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t55_fdiff_11

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_42-query512-ctx768-w0-coop$ less t55_fdiff_11
```
# Proof object clause steps            : 103
# Proof object initial clauses used    : 52
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 115
# Parsed axioms                        : 206
# Initial clauses in saturation        : 269
# Processed clauses                    : 1903
# ...remaining for further processing  : 1307
# Generated clauses                    : 8595
# ...of the previous two non-trivial   : 7957
# User time                : 17.228 s
```

### Differentiation: (arccot * exp_R)' = - (exp_R . x) / (1 + ((exp_R . x) ^2)

((arccot * exp_R) \`| Z) . x = - ((exp_R . x) / (1 + ((exp_R . x) ^2))) ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos9.html#T116

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t116_sin_cos9

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_42-query512-ctx768-w0-coop$ less t116_sin_cos9

```
# Proof object clause steps            : 155
# Proof object initial clauses used    : 75
# Proof object initial formulas used   : 60
# Proof object simplifying inferences  : 145
# Parsed axioms                        : 511
# Initial clauses in saturation        : 695
# Processed clauses                    : 3074
# ...remaining for further processing  : 1848
# Generated clauses                    : 19709
# ...of the previous two non-trivial   : 16538
# User time                : 11.720 s
```

### Enigma integrates: integral sin+cos on \[0,pi/2\] = 2

A = [.0,(PI / 2).] implies integral ((sin + cos),A) = 2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra8.html#T70

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t70_integra8

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t70_integra8 

```
# Proof object clause steps            : 139
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 49
# Proof object simplifying inferences  : 182
# Parsed axioms                        : 555
# Initial clauses in saturation        : 789
# Processed clauses                    : 4090
# ...remaining for further processing  : 2518
# Generated clauses                    : 18537
# ...of the previous two non-trivial   : 15707
# User time                : 24.348 s
```

### Enigma integrates: integral (sin - cos) on \[0,pi\*2\] = 0

A = \[.0,(PI * 2).\] implies integral ((sin - cos),A) = 0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra8.html#T82

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t82_integra8

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t82_integra8
```
# Proof object clause steps            : 161
# Proof object initial clauses used    : 74
# Proof object initial formulas used   : 59
# Proof object simplifying inferences  : 207
# Parsed axioms                        : 568
# Initial clauses in saturation        : 821
# Processed clauses                    : 5601
# ...remaining for further processing  : 3236
# Generated clauses                    : 25826
# ...of the previous two non-trivial   : 21838
# User time                : 28.424 s
```


### Cos is increasing on pi,2pi

cos | ].PI,(2 * PI).\[ is increasing

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/comptrig.html#T22

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_comptrig

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t22_comptrig 

```
# Proof object clause steps            : 129
# Proof object initial clauses used    : 60
# Proof object initial formulas used   : 55
# Proof object simplifying inferences  : 112
# Parsed axioms                        : 347
# Initial clauses in saturation        : 439
# Processed clauses                    : 3921
# ...remaining for further processing  : 1888
# Generated clauses                    : 16932
# ...of the previous two non-trivial   : 13170
# User time                : 14.220 s
```



### Additivity of integral

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfunc5.html#T93

f is nonnegative & A c= B holds Integral (M,(f | A)) <= Integral (M,(f | B))

http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t93_mesfunc5

```
% Proof object clause steps            : 126
% Proof object initial clauses used    : 53
% Proof object initial formulas used   : 29
% Parsed axioms                        : 441
% Initial clauses in saturation        : 670
% Processed clauses                    : 3725
% ...remaining for further processing  : 2236
% Generated clauses                    : 14044
% ...of the previous two non-trivial   : 13075
```

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_4-query512-ctx768-w0-coop$ 


### Almost infinitude of primes:

Enigma can now (sort of) prove that primes are infinite: for l being Nat ex p being Prime st ( p is prime & p > l )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/newton.html#T72

The E proof is at http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t72_newton

Modulo the fact that we gave it 328 FOF axioms translated to 549 initial clauses, the proof stats seem easy:

```
% Proof object clause steps            : 83
% Proof object initial clauses used    : 42
% Proof object initial formulas used   : 38
% Parsed axioms                        : 328
% Initial clauses in saturation        : 549
% Processed clauses                    : 880
% ...remaining for further processing  : 734
% Generated clauses                    : 3135
% ...of the previous two non-trivial   : 2856
% User time                : 6.772 s
```

The only issue is that no prover could do it before and that I got the proof with only one parameterization of Enigma out of 800 :-). (l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_67-query128-ctx768-w0-solo).

The fact that it generated only 2.8k clauses during 734 nontrivial given clause loops (with 549 initial clauses) is pretty amazing (and probably the reason why this succeeded). 

### 37 is a prime number

37 is prime

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/nat_4.html#T31

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t31_nat_4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_23-query256-ctx1024-w0-coop$ less t31_nat_4
```
# Proof object clause steps            : 155
# Proof object initial clauses used    : 81
# Proof object initial formulas used   : 76
# Proof object simplifying inferences  : 159
# Parsed axioms                        : 746
# Initial clauses in saturation        : 1070
# Processed clauses                    : 3703
# ...remaining for further processing  : 2680
# Generated clauses                    : 15883
# ...of the previous two non-trivial   : 10197
# User time                : 12.860 s
```

### 43 is prime

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/nat_4.html#T32

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t32_nat_4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_50-query512-ctx1536-w0-coop$ less t32_nat_4
```
# Proof object clause steps            : 157
# Proof object initial clauses used    : 85
# Proof object initial formulas used   : 79
# Proof object simplifying inferences  : 146
# Parsed axioms                        : 931
# Initial clauses in saturation        : 1270
# Processed clauses                    : 4276
# ...remaining for further processing  : 2975
# Generated clauses                    : 14720
# ...of the previous two non-trivial   : 10484
# User time                : 10.424 s
```

Almost 1k axioms, 79 of them used in the proof, 3k processed, 10k generated - not bad.


### The radical of square-free k is k

for k being non zero Nat st k is square-free holds Radical k = k

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/moebius1.html#T57

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t57_moebius1

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_66-query512-ctx512-w0-solo$ less t57_moebius1 

```
# Proof object clause steps            : 124
# Proof object initial clauses used    : 60
# Proof object initial formulas used   : 42
# Proof object simplifying inferences  : 136
# Parsed axioms                        : 339
# Initial clauses in saturation        : 663
# Processed clauses                    : 2020
# ...remaining for further processing  : 1630
# Generated clauses                    : 14333
# ...of the previous two non-trivial   : 11883
# User time                : 26.564 s
```



### Combinatorics and counting - coefficient in binomial expansion

(a,b) In_Power 0 = <\*(1_ R)\*>

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/binom.html#T22

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_binom

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_65-query256-ctx768-w0-coop$ less t22_binom

```
# Proof object clause steps            : 180
# Proof object initial clauses used    : 75
# Proof object initial formulas used   : 57
# Proof object simplifying inferences  : 142
# Parsed axioms                        : 393
# Initial clauses in saturation        : 572
# Processed clauses                    : 3193
# ...remaining for further processing  : 2108
# Generated clauses                    : 15114
# ...of the previous two non-trivial   : 13476
# User time                : 26.104 s
```

### Counting - partial product of a constant sequence

for s being Real_Sequence st ( for n being Element of NAT st n >= 1 holds s . n = a & s . 0 = 1  ) holds
for n being Element of NAT st n >= 1 holds (Partial_Product s) . n = a |^ n

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/series_4.html#T29

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t29_series_4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_88-query512-ctx768-w0-coop$ less t29_series_4
```
# Proof object clause steps            : 168
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 46
# Proof object simplifying inferences  : 204
# Parsed axioms                        : 224
# Initial clauses in saturation        : 274
# Processed clauses                    : 3001
# ...remaining for further processing  : 1605
# Generated clauses                    : 20071
# ...of the previous two non-trivial   : 18372
# User time                : 21.936 s
```



### Topology - discrete is T_2
for T being non empty discrete TopSpace holds T is T_2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow13.html#T4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid28_60/mzr02-premsel_enigma_01_2020_T10_loop01_epoch_66-query768-ctx1536-w0-coop$ less t4_yellow13  

```
% Parsed axioms                        : 194
% Initial clauses in saturation        : 279
% Proof object clause steps            : 103
% Proof object initial clauses used    : 36
% Proof object initial formulas used   : 23
% Processed clauses                    : 3866
% ...remaining for further processing  : 1758
% Generated clauses                    : 36890
% ...of the previous two non-trivial   : 32976
```

### Topology - T1 is a disjoint union of perfect and scattered

T is T_1 implies ex A, B being Subset of T st
A \\/ B = [#] T & A misses B & A is perfect & B is scattered

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topgen_1.html#T44

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t44_topgen_1

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_66-query512-ctx512-w0-solo$ less t44_topgen_1

```
# Proof object clause steps            : 120
# Proof object initial clauses used    : 51
# Proof object initial formulas used   : 37
# Proof object simplifying inferences  : 73
# Parsed axioms                        : 159
# Initial clauses in saturation        : 211
# Processed clauses                    : 2264
# ...remaining for further processing  : 1239
# Generated clauses                    : 14833
# ...of the previous two non-trivial   : 13900
# User time                : 16.056 s
```


### Connectedness - all points are joined if some is joined to all:

for GX being TopSpace holds
( ex x being Point of GX st
for y being Point of GX holds x,y are_joined iff for x, y being Point of GX holds x,y are_joined )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/connsp_1.html#T29

```
% Proof object clause steps            : 99
% Proof object initial clauses used    : 32
% Proof object initial formulas used   : 17
% Parsed axioms                        : 74
% Initial clauses in saturation        : 99
% Processed clauses                    : 1940
% ...remaining for further processing  : 1069
% Generated clauses                    : 28829
% ...of the previous two non-trivial   : 27799
```

### Connectedness - synthesize and inverse path

ex f being Function of I[01],T st( f is continuous & f . 0 = a & f . 1 = b ) implies
ex g being Function of I[01],T st( g is continuous & g . 0 = b & g . 1 = a )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/borsuk_2.html#T15

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_borsuk_2

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t15_borsuk_2

```
# Proof object clause steps            : 117
# Proof object initial clauses used    : 57
# Proof object initial formulas used   : 39
# Proof object simplifying inferences  : 150
# Parsed axioms                        : 302
# Initial clauses in saturation        : 502
# Processed clauses                    : 2473
# ...remaining for further processing  : 1606
# Generated clauses                    : 12964
# ...of the previous two non-trivial   : 11465
# User time                : 18.620 s
```

### Two points on an arc are connected by a subarc

P is_an_arc_of p1,p2 & q1 in P & q2 in P implies
ex Q being non empty Subset of (TOP-REAL 2) st
Q is_an_arc_of q1,q2 & Q c= P 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan16.html#T23

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t23_jordan16.out

(base) mptp@air-03:/home/yan/local/ENIGMA/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l6400-e0.15+coop-mzr02$ less t23_jordan16.out

```
# Proof object clause steps            : 194
# Proof object initial clauses used    : 48
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 169
# Parsed axioms                        : 192
# Initial clauses                      : 322
# Initial clauses in saturation        : 293
# Processed clauses                    : 11023
# ...remaining for further processing  : 6247
# Generated clauses                    : 70833
# ...of the previous two non-trivial   : 64270
# User time                : 15.051 s

```

### r-circle is a subspace of r-square

for r being real number holds Tcircle ((0. (TOP-REAL 2)),r) is SubSpace of Trectangle ((- r),r,(- r),r)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/toprealb.html#T10

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_65-query256-ctx768-w0-coop$ 

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_toprealb

```
# Proof object clause steps            : 77
# Proof object initial clauses used    : 36
# Proof object initial formulas used   : 31
# Proof object simplifying inferences  : 33
# Parsed axioms                        : 425
# Initial clauses in saturation        : 692
# Processed clauses                    : 1977
# ...remaining for further processing  : 1424
# Generated clauses                    : 6616
# ...of the previous two non-trivial   : 6010
# User time                : 10.648 s
```

### Circle rotation has no fixpoint

RotateCircle (o,r,p) is without_fixpoints

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan.html#T67

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t67_jordan

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t67_jordan

```
# Proof object clause steps            : 97
# Proof object initial clauses used    : 49
# Proof object initial formulas used   : 36
# Proof object simplifying inferences  : 67
# Parsed axioms                        : 542
# Initial clauses in saturation        : 962
# Processed clauses                    : 2266
# ...remaining for further processing  : 1718
# Generated clauses                    : 7405
# ...of the previous two non-trivial   : 6846
# User time                : 13.668 s
```

### The diameter of the convex hull of A is equal to the diameter of A

for A being Subset of (TOP-REAL n) for a, ca being bounded Subset of (Euclid n) st ca = conv A & a = A holds
diameter a = diameter ca

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/simplex2.html#T15

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_simplex2

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_23-query256-ctx1024-w0-coop$ less t15_simplex2

```
# Proof object clause steps            : 104
# Proof object initial clauses used    : 51
# Proof object initial formulas used   : 28
# Proof object simplifying inferences  : 87
# Parsed axioms                        : 522
# Initial clauses in saturation        : 972
# Processed clauses                    : 2258
# ...remaining for further processing  : 1822
# Generated clauses                    : 8697
# ...of the previous two non-trivial   : 8006
# User time                : 13.708 s
```

### Affine sets are convex

for V being non empty RLSStruct for M being Subset of V st M is Affine holds M is convex

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/convex1.html#T16

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t16_convex1

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_73-query128-ctx256-w0-coop$ less t16_convex1
```
# Proof object clause steps            : 79
# Proof object initial clauses used    : 39
# Proof object initial formulas used   : 31
# Proof object simplifying inferences  : 58
# Parsed axioms                        : 294
# Initial clauses in saturation        : 390
# Processed clauses                    : 5195
# ...remaining for further processing  : 2812
# Generated clauses                    : 70324
# ...of the previous two non-trivial   : 63821
# User time                : 24.336 s
```

Relatively short proof, but nobody could get it with the 294 axioms. Even here the search was hard - 64k nontrivial generated clauses and 3k nontrivial processed.


### Constant is a continuous function to R

for X being non empty TopSpace for a being real number 
ex g being Function of X,R^1 st  ( for p being Point of X holds g . p = a ) & g is continuous

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jgraph_2.html#T20

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_jgraph_2

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ exprf.pl t20_jgraph_2

```
# Proof object clause steps            : 74
# Proof object initial clauses used    : 38
# Proof object initial formulas used   : 26
# Proof object simplifying inferences  : 35
# Parsed axioms                        : 230
# Initial clauses in saturation        : 353
# Processed clauses                    : 1542
# ...remaining for further processing  : 1158
# Generated clauses                    : 7543
# ...of the previous two non-trivial   : 6338
# User time                : 22.052 s
```


### Probability - counting with probabilities

P . ((A /\ B) /\ C) = ((P . A) * ((P .|. A) . B)) * ((P .|. (A /\ B)) . C)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/prob_2.html#T30

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t30_prob_2.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d50-l900-e0.15+coop-mzr02$ less t30_prob_2.out 
```
# Proof object clause steps            : 179
# Proof object initial clauses used    : 57
# Proof object initial formulas used   : 40
# Parsed axioms                        : 233
# Initial clauses in saturation        : 286
# Processed clauses                    : 2746
# ...remaining for further processing  : 1856
# Generated clauses                    : 12511
# ...of the previous two non-trivial   : 11325
# User time                : 3.117 s
```

### Convergence of exponentials in Banach spaces - 267-long proof

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lopban_4.html#T33

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t33_lopban_4.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l900-e0.15+coop-mzr02$ less t33_lopban_4.out 

```
# Proof object clause steps            : 267
# Proof object initial clauses used    : 76
# Proof object initial formulas used   : 33
# Parsed axioms                        : 306
# Initial clauses in saturation        : 444
# Processed clauses                    : 4012
# ...remaining for further processing  : 2859
# Generated clauses                    : 14692
# ...of the previous two non-trivial   : 13478
# User time                : 6.668 s
```

### Partial sums in normed spaces

for n being Element of NAT holds seq . n = 0. X implies
for m being Element of NAT holds (Partial_Sums ||.seq.||) . m = 0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/clopban3.html#T6

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_clopban3.out

(base) mptp@air-03:/home/yan/local/ENIGMA/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d60-l3600-e0.15+coop-mzr02$ less t6_clopban3.out

```
# Proof object clause steps            : 184
# Proof object initial clauses used    : 55
# Proof object initial formulas used   : 40
# Proof object simplifying inferences  : 134
# Parsed axioms                        : 261
# Initial clauses in saturation        : 389
# Processed clauses                    : 2914
# ...remaining for further processing  : 1846
# Generated clauses                    : 10568
# ...of the previous two non-trivial   : 9485
# User time                : 3.345 s
```

### There is a vector of norm 1 in a nontrivial normed space

for X being non trivial RealNormSpace ex w being VECTOR of X st ||.w.|| = 1

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lopban_2.html#T17

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t17_lopban_2

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_88-query512-ctx768-w0-coop$ less t17_lopban_2

```
# Proof object clause steps            : 127
# Proof object initial clauses used    : 69
# Proof object initial formulas used   : 49
# Proof object simplifying inferences  : 83
# Parsed axioms                        : 351
# Initial clauses in saturation        : 441
# Processed clauses                    : 1902
# ...remaining for further processing  : 1202
# Generated clauses                    : 9831
# ...of the previous two non-trivial   : 8526
# User time                : 10.624 s
```


### Open sets are complements of closed in complex spaces

for A being Subset of COMPLEX n holds A is closed iff A \` is open 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/seq_4.html#T132

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t132_seq_4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_88-query512-ctx768-w0-coop$ exprf.pl t132_seq_4
```
# Proof object clause steps            : 100
# Proof object initial clauses used    : 44
# Proof object initial formulas used   : 24
# Proof object simplifying inferences  : 63
# Parsed axioms                        : 532
# Initial clauses in saturation        : 1072
# Processed clauses                    : 2860
# ...remaining for further processing  : 1940
# Generated clauses                    : 10260
# ...of the previous two non-trivial   : 9599
# User time                : 11.800 s
```

### The lattice of subalgebras of a many-sorted algebra is lower/upper-bounded - 291-long proof

for U0 being non-empty MSAlgebra over S holds MSSubAlLattice U0 is bounded

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/msualg_2.html#T33

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t33_msualg_2.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d60-l700-e0.20+coop-mzr02$ less t33_msualg_2.out

```
# Proof object clause steps            : 291
# Proof object initial clauses used    : 81
# Proof object initial formulas used   : 46
# Parsed axioms                        : 255
# Initial clauses in saturation        : 475
# Processed clauses                    : 7051
# ...remaining for further processing  : 2834
# Generated clauses                    : 32864
# ...of the previous two non-trivial   : 28335
# User time                : 8.732 s
```

### Lattices: a subrelation is closed on finite joins iff it is closed on joins of pairs

for T being sup-Semilattice
for S being non empty full SubRelStr of T holds
S is join-inheriting iff for X being non empty finite Subset of S holds "\/" (X,T) in the carrier of S

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel21.html#T15

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_waybel21

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_49-query128-ctx512-w0-coop$ less t15_waybel21
```
# Proof object clause steps            : 128
# Proof object initial clauses used    : 56
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 143
# Parsed axioms                        : 193
# Initial clauses in saturation        : 303
# Processed clauses                    : 3151
# ...remaining for further processing  : 1633
# Generated clauses                    : 13852
# ...of the previous two non-trivial   : 13196
# User time                : 24.412 s
```




### Logic: A set of formulas is inconsistent iff it proves everything

for Al being QC-alphabet for X being Subset of CQC-WFF Al holds
X is Inconsistent iff for p being Element of CQC-WFF Al holds X |- p 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/henmodel.html#T6

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_henmodel

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_59-query768-ctx1024-w0-coop$ less t6_henmodel
```
# Proof object clause steps            : 76
# Proof object initial clauses used    : 35
# Proof object initial formulas used   : 21
# Proof object simplifying inferences  : 52
# Parsed axioms                        : 232
# Initial clauses in saturation        : 376
# Processed clauses                    : 3532
# ...remaining for further processing  : 2207
# Generated clauses                    : 13559
# ...of the previous two non-trivial   : 12398
# User time                : 24.872 s
```




### Topology - product of T_0 spaces is T_0

for M being non empty set
for J being non-Empty TopStruct-yielding ManySortedSet of M st ( for i being Element of M holds J . i is T_0 TopSpace ) holds
product J is T_0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow14.html#T37

mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_51-query128-ctx1024-w0-coop$ 

```
% Proof object clause steps            : 98
% Proof object initial clauses used    : 44
% Proof object initial formulas used   : 23
% Parsed axioms                        : 188
% Initial clauses in saturation        : 319
% Processed clauses                    : 2185
% ...remaining for further processing  : 1408
% Generated clauses                    : 9227
% ...of the previous two non-trivial   : 7578
% User time                : 20.956 s
```

### Rational numbers - lots of computation, many proof formulas/clauses

for p being Rational for l,m,k holds not numerator p = m * l or not denominator p = k * l 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/rat_1.html#T29

E proof with lgb: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t29_rat_1.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d30-l1800-e0.15+coop-mzr02$ less t29_rat_1.out 

```
# Proof object clause steps            : 262
# Proof object initial clauses used    : 69
# Proof object initial formulas used   : 55
# Parsed axioms                        : 222
# Initial clauses in saturation        : 277
# Processed clauses                    : 7815
# ...remaining for further processing  : 3799
# Generated clauses                    : 163747
# ...of the previous two non-trivial   : 151812
# User time                : 27.157 s
```

### Graph theory: oriented chain determines the oriented vertex sequence

for c being oriented Chain of G st c <> {} & vs1 is_oriented_vertex_seq_of c & vs2 is_oriented_vertex_seq_of c holds
vs1 = vs2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/graph_4.html#T10

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_graph_4

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_15-query128-ctx768-w0-coop$ less t10_graph_4
```
# Proof object clause steps            : 204
# Proof object initial clauses used    : 72
# Proof object initial formulas used   : 52
# Proof object simplifying inferences  : 275
# Parsed axioms                        : 368
# Initial clauses in saturation        : 543
# Processed clauses                    : 3553
# ...remaining for further processing  : 2119
# Generated clauses                    : 18342
# ...of the previous two non-trivial   : 15472
# User time                : 22.296 s
```


### Graph theory: if G has clique# <=1 its Mycielskian has clique# <= 2 

for G being with_finite_clique# SimpleGraph st clique# G = 1 holds
for D being finite Clique of (Mycielskian G) holds order D <= 2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/scmyciel.html#T108

http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t108_scmyciel

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_65-query256-ctx768-w0-coop$ less t108_scmyciel 

```
# Proof object clause steps            : 109
# Proof object initial clauses used    : 55
# Proof object initial formulas used   : 41
# Proof object simplifying inferences  : 77
# Parsed axioms                        : 341
# Initial clauses in saturation        : 528
# Processed clauses                    : 3004
# ...remaining for further processing  : 1913
# Generated clauses                    : 11251
# ...of the previous two non-trivial   : 9842
# User time                : 12.060 s
```

### Modules: linearly independent sets don't contain 0

for V being LeftMod of R for A being Subset of V st 0. R <> 1. R & A is linearly-independent 
holds not 0. V in A

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lmod_5.html#T2

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_lmod_5

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_43-query512-ctx1024-w0-coop$ less t2_lmod_5

```
# Proof object clause steps            : 126
# Proof object initial clauses used    : 72
# Proof object initial formulas used   : 38
# Proof object simplifying inferences  : 101
# Parsed axioms                        : 186
# Initial clauses in saturation        : 305
# Processed clauses                    : 2003
# ...remaining for further processing  : 1426
# Generated clauses                    : 14951
# ...of the previous two non-trivial   : 7793
# User time                : 15.924 s
```

### Orthogonal spaces: being orthogonal to the same set implies being parallel

for POS being OrtAfPl for M, K, N being Subset of POS st M \_|\_ K & N \_|\_ K holds M // N

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/analmetr.html#T65

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t65_analmetr

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_42-query512-ctx768-w0-coop$ less t65_analmetr
```
# Proof object clause steps            : 90
# Proof object initial clauses used    : 47
# Proof object initial formulas used   : 26
# Proof object simplifying inferences  : 114
# Parsed axioms                        : 148
# Initial clauses in saturation        : 239
# Processed clauses                    : 2881
# ...remaining for further processing  : 1972
# Generated clauses                    : 12430
# ...of the previous two non-trivial   : 11717
# User time                : 22.012 s
```



### Cardinalities:
1 -tuples_on D,D are_equipotent & card (1 -tuples_on D) = card D 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/card_4.html#T8

http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t8_card_4

```
% Proof object clause steps            : 90
% Proof object initial clauses used    : 35
% Proof object initial formulas used   : 20
% Parsed axioms                        : 301
% Initial clauses in saturation        : 508
% Processed clauses                    : 1262
% ...remaining for further processing  : 932
% Generated clauses                    : 6827
% ...of the previous two non-trivial   : 6260
```

### Groebner bases

for G being Subset of (Polynom-Ring (n,L)) st not 0_ (n,L) in G & ( for g being Polynomial of n,L st g in G holds
g is Monomial of n,L ) holds G is_Groebner_basis_wrt T

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/groeb_2.html#T26

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t26_groeb_2

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_23-query256-ctx1024-w0-coop$ less t26_groeb_2

```
# Proof object clause steps            : 131
# Proof object initial clauses used    : 71
# Proof object initial formulas used   : 31
# Proof object simplifying inferences  : 322
# Parsed axioms                        : 415
# Initial clauses in saturation        : 960
# Processed clauses                    : 2919
# ...remaining for further processing  : 2353
# Generated clauses                    : 8083
# ...of the previous two non-trivial   : 7578
# User time                : 24.048 s
```

### Matrices: M has full rank iff Det M <> 0

for n being Nat for K being Field for M being Matrix of n,K holds the_rank_of M = n iff Det M <> 0. K 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix13.html#T83

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t83_matrix13

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500_greed_all/l8-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_47-query256-ctx768-w0-coop$ less t83_matrix13
```
# Proof object clause steps            : 134
# Proof object initial clauses used    : 64
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 138
# Parsed axioms                        : 397
# Initial clauses in saturation        : 707
# Processed clauses                    : 1998
# ...remaining for further processing  : 1522
# Generated clauses                    : 5877
# ...of the previous two non-trivial   : 5239
# User time                : 15.120 s
```



### Divergence of locally greater function

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/limfunc2.html#T37

### Cardinalities
 X,[:X,{x}:] are_equipotent & card X = card [:X,{x}:] 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/card_2.html#T6


### Longer proof about programs and sequences with 59/663 used/initial axioms
/home/mptp/big1/bushy_np/en_gnn/convert-models/grid28_60/mzr02-premsel_enigma_01_2020_T10_loop01_epoch_66-query768-ctx1536-w0-coop/t64_compos_1
http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/compos_1.html#T64

```
% Generated clauses                    : 38354
% ...of the previous two non-trivial   : 36601
% Processed clauses                    : 5785
% ...remaining for further processing  : 3336
% Parsed axioms                        : 663
% Initial clauses in saturation        : 1212
% Proof object initial clauses used    : 78
% Proof object initial formulas used   : 59
% Proof object clause steps            : 158
```


### Longish proof in INT_5
http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/int_5.html#T3

for fp being FinSequence of INT st len fp = 1 holds Poly-INT fp = INT --> (fp . 1)

(base) mptp@air-02:~/big1/bushy_np/en_gnn/convert-models/grid1500/l5-mzr02-premsel_enigma_01_2020_T10_loop01_epoch_45-query256-ctx1536-w0-coop$ less t3_int_5

```
% Proof object clause steps            : 153
% Proof object initial clauses used    : 76
% Proof object initial formulas used   : 59
% Parsed axioms                        : 404
% Initial clauses in saturation        : 656
% Processed clauses                    : 2547
% ...remaining for further processing  : 1849
% Generated clauses                    : 11674
% ...of the previous two non-trivial   : 10831
```

### Longish proof in ORDERS_1

for R being Relation for X being set st R partially_orders X holds R |_ 2 X is Order of X

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/orders_1.html#T45

```
% Proof object clause steps            : 132
% Proof object initial clauses used    : 46
% Proof object initial formulas used   : 26
% Parsed axioms                        : 218
% Initial clauses in saturation        : 347
% Processed clauses                    : 3985
% ...remaining for further processing  : 1852
% Generated clauses                    : 30744
% ...of the previous two non-trivial   : 27676
% User time                : 22.204 s
```

