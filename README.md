# Interesting ATP Proofs

These are so far proofs found by E ([8],[9],[13]) using versions of ENIGMA ([1],[2],[3],[4],[5],[12],[18]) trained in several iterations from scratch on the Mizar/MPTP/Mizar40 ([10],[11],[14]) bushy problems. We also use E's auto-schedule, many E strategies invented by BliStr/Tune ([15],[16],[17]), Malarea/ATPBoost-style ([6],[7]) premise selection (using lgb,gnn,xgb,rnn and transformer [6],[19],[20],[21]) for some runs and heuristic premise minimization based on the structure of subproblems. There are 57880 toplevel Mizar problems we try to prove.

#### Time progress - total ATP-proved problems (using human-supplied premises and/or trained/heuristic premise selectors): 

- 38k (65.65%) proved by June (reported on July 2nd at IJCAR'20: https://youtu.be/XojOEpZfH4Y?t=673 )
- 40k (69.11%) proved by end of September
- 40268 (69.57%) proved by end of October
- 40628 (70.19%) proved by November 10 (heuristic premise minimization started to be used)
- 40909 (70.68%) proved by November 11 (more heuristic premise minimization)
- 40994 (70.83%) proved by November 12
- 41169 (71.13%) proved by November 12 (300s runs of Vampire add 175)
- 41222 (71.23%) by Nov 13
- 41304 (71.36%) by Nov 16 (more Vampire)
- 41499 (71.70%) by Nov 24 (more E with second round of heuristic premise minimization)
- 41659 (71.97%) by Nov 25 (more Vampire)
- 41792 (72.20%) by Nov 27 (more E with second round of heuristic premise minimization)
- 42050 (72.65%) by Dec 2
- 42172 (72.86%) by Dec 6 (more E with heuristic premise minimization)
- 42206 (72.92%) by Dec 7 (more Vampire)
- 42275 (73.04%) by Jan 1 2021 (blistr runs on gnn -1 predictions)
- 42325 (73.13%) by Jan 2 2021 (blistr runs on gnn -3, 0, 1 predictions)
- 42424 (73.30%) by Jan 4 2021 (blistr runs on combined predictions produced by Cezary)
- 42471 (73.38%) by Jan 6 2021 (more blistr runs on combined predictions produced by Cezary)
- 42519 (73.46%) by Jan 10 2021 (started enigma runs on all training predictions)
- 42826 (73.99%) by May 14 2021 (further Vampire/Deepire runs after the hammering eval - FroCoS paper)

#### Time progress in the hammering setting (ATP-proved problems when using trained premise selectors):
This evaluation is done using a 90/5/5 training/development/holdout split of the 58k (52125/2896/2896) problems. 
The training set is used for training premise selection and internal guidance (ENIGMA), the development set for choosing the best methods and their combinations and portfolios, and the holdout set for the ultimate evaluation of the methods.

- 1690 (58.36%) on holdout by Feb 1 by a 420s portfolio designed by robust greedy cover on the devel set where it solves 60.4%


[1]: https://doi.org/10.1007/978-3-030-51054-1_29
[2]: https://doi.org/10.1007/978-3-030-29436-6_12
[3]: https://doi.org/10.1007/978-3-030-29026-9_21
[4]: https://doi.org/10.1007/978-3-319-96812-4_11
[5]: http://arxiv.org/abs/1701.06532
[6]: https://doi.org/10.1007/978-3-319-94205-6_37
[7]: https://doi.org/10.1007/978-3-540-71070-7_37
[8]: https://doi.org/10.1007/978-3-030-29436-6_29
[9]: https://doi.org/10.1007/978-3-642-45221-5_49
[10]: https://doi.org/10.1007/978-3-319-20615-8_17
[11]: https://doi.org/10.1007/s10817-006-9032-3
[12]: https://doi.org/10.4230/LIPIcs.ITP.2019.34
[13]: http://content.iospress.com/articles/ai-communications/aic260
[14]: https://doi.org/10.1007/s10817-015-9330-8
[15]: https://easychair.org/publications/paper/FJD
[16]: https://doi.org/10.1145/3018610.3018619
[17]: https://doi.org/10.3233/AIC-180761
[18]: https://arxiv.org/abs/2107.06750
[19]: https://doi.org/10.3233/FAIA200244
[20]: https://easychair.org/publications/paper/g38n
[21]: https://doi.org/10.1007/978-3-030-53518-6_24

## Table of Contents  

- [Lipschitzian is uniformly continuous:](#lipschitzian-is-uniformly-continuous)
- [Metric spaces: Two compact sets with Hausdorff distance 0 are equal](#metric-spaces-two-compact-sets-with-hausdorff-distance-0-are-equal)
- [Matric spaces: relation of point distances to distance of compact sets - 440 step proof from 82 premises](#matric-spaces-relation-of-point-distances-to-distance-of-compact-sets---440-step-proof-from-82-premises)
- [epsilon-delta continuity in metric spaces](#epsilon-delta-continuity-in-metric-spaces)
- [Enigma learns to count:](#enigma-learns-to-count)
- [Another counting:](#another-counting)
- [Massive counting in trigonometry - 445-long proof from 83 formulas](#massive-counting-in-trigonometry---445-long-proof-from-83-formulas)
- [Another trig counting - 619-long proof from 83 formulas and 1025 initial axioms](#another-trig-counting---619-long-proof-from-83-formulas-and-1025-initial-axioms)
- [Another trig counting - 224 steps and 54 formulas](#another-trig-counting---224-steps-and-54-formulas)
- [Trig counting - Arg x &lt; PI &amp; Arg y &lt; PI implies Arg (x + y) &lt; PI (343-long ATP proof from 56 premises)](#trig-counting---arg-x--pi--arg-y--pi-implies-arg-x--y--pi-343-long-atp-proof-from-56-premises)
- [Counting: e^(2<em>pi</em>n*i) = 1](#counting-e2pini--1)
- [Counting/algebra: 0 &lt; n &amp; 1 &lt; r implies 1 &lt; r ^ n](#countingalgebra-0--n--1--r-implies-1--r--n)
- [Counting/algebra: Division with remainder: (n div k) div i = n div (k * i)](#countingalgebra-division-with-remainder-n-div-k-div-i--n-div-k--i)
- [Counting/algebra: n mod 2 = 0 iff (n -' 1) mod 2 = 1 - large alternative proof using 51 premises](#countingalgebra-n-mod-2--0-iff-n---1-mod-2--1---large-alternative-proof-using-51-premises)
- [List editing set-theory style](#list-editing-set-theory-style)
- [Lists: sum of a sequence is preserved under reversal in AC contexts](#lists-sum-of-a-sequence-is-preserved-under-reversal-in-ac-contexts)
- [Permutations set-theory style - the Mizar proof has 144 lines](#permutations-set-theory-style---the-mizar-proof-has-144-lines)
- [Dyadic numbers](#dyadic-numbers)
- [Matroids: maximal independent subsets](#matroids-maximal-independent-subsets)
- [Convergence in metric space and in its induced topology are the same](#convergence-in-metric-space-and-in-its-induced-topology-are-the-same)
- [Convergence of a real sequence is the same in the real metric space](#convergence-of-a-real-sequence-is-the-same-in-the-real-metric-space)
- [Convergence: if a whole sequence is &lt;= p then its limit &lt;= p](#convergence-if-a-whole-sequence-is--p-then-its-limit--p)
- [Convergence: limit of a sequence bounded between two sequences with the same limit - simple alternative proof](#convergence-limit-of-a-sequence-bounded-between-two-sequences-with-the-same-limit---simple-alternative-proof)
- [Topology: In compact spaces, Cauchy nets are convergent](#topology-in-compact-spaces-cauchy-nets-are-convergent)
- [Topology: equivalent condition on homeomorphism: bijection plus images of open are open](#topology-equivalent-condition-on-homeomorphism-bijection-plus-images-of-open-are-open)
- [Lattices: lower bounded up-complete L where SupMap L is upper adjoint is continuous](#lattices-lower-bounded-up-complete-l-where-supmap-l-is-upper-adjoint-is-continuous)
- [Lattices: equivalent condition on being prime in a semillatice](#lattices-equivalent-condition-on-being-prime-in-a-semillatice)
- [Lattices: Dual of a complete-distributive poset is complete-dsitributive ; 377-long ATP proof from 35 premises](#lattices-dual-of-a-complete-distributive-poset-is-complete-dsitributive--377-long-atp-proof-from-35-premises)
- [Monster proof in continuous lattices relating a weight of an infinite T0 topological space to the weight of the semilattice formed by the inclusion poset of its topology](#monster-proof-in-continuous-lattices-relating-a-weight-of-an-infinite-t0-topological-space-to-the-weight-of-the-semilattice-formed-by-the-inclusion-poset-of-its-topology)
- [Continuous lattices: Proposition 2.1 of <a href="https://www.amazon.com/Compendium-Continuous-Lattices-G-Gierz/dp/3642676804" rel="nofollow">CCL</a> (p. 112), 1 &lt;=&gt; 6 ; 1039-long ATP proof](#continuous-lattices-proposition-21-of-ccl-p-112-1--6--1039-long-atp-proof)
- [Continuous lattices: Exercise 2.16 of <a href="https://www.amazon.com/Compendium-Continuous-Lattices-G-Gierz/dp/3642676804" rel="nofollow">CCL</a> (p. 156), 1 &lt;=&gt; 2 ; 563-long ATP proof from 30 premises](#continuous-lattices-exercise-216-of-ccl-p-156-1--2--563-long-atp-proof-from-30-premises)
- [Lattices - concept lattices isomorphism](#lattices---concept-lattices-isomorphism)
- [Category theory: inverse of a composed natural equivalence is the composition of inverses](#category-theory-inverse-of-a-composed-natural-equivalence-is-the-composition-of-inverses)
- [Groups: a is in center iff its conjugacy class is {a}](#groups-a-is-in-center-iff-its-conjugacy-class-is-a)
- [card (con_class a) = Index (Normalizer {a})](#card-con_class-a--index-normalizer-a)
- [if G/N and N are p-groups then G is also a p-group](#if-gn-and-n-are-p-groups-then-g-is-also-a-p-group)
- [Index of the unit subgroup of G is equal to the cardinality of G](#index-of-the-unit-subgroup-of-g-is-equal-to-the-cardinality-of-g)
- [Index of the intersection of subgroups with relatively prime indices](#index-of-the-intersection-of-subgroups-with-relatively-prime-indices)
- [Groups: The Jordan-Holder property of a composition series is preserved under equivalence ; 297-long ATP proof using 44 premises](#groups-the-jordan-holder-property-of-a-composition-series-is-preserved-under-equivalence--297-long-atp-proof-using-44-premises)
- [Groups: a commutative group is solvable](#groups-a-commutative-group-is-solvable)
- [Groups: analogy between abelian additive and commutative multiplicative groups](#groups-analogy-between-abelian-additive-and-commutative-multiplicative-groups)
- [Groups with sets:](#groups-with-sets)
- [Rings: commutative rings are fields iff ideals are trivial](#rings-commutative-rings-are-fields-iff-ideals-are-trivial)
- [Vector spaces: dimension of a 2-element vector space is 1 ; 336-long ATP proof from 42 premises, 70-line proof in Mizar](#vector-spaces-dimension-of-a-2-element-vector-space-is-1--336-long-atp-proof-from-42-premises-70-line-proof-in-mizar)
- [Vector spaces: Explicit formula for linear combination of two (or 1 or 0) vectors](#vector-spaces-explicit-formula-for-linear-combination-of-two-or-1-or-0-vectors)
- [Enigma differentiates: (ln * cos) `| Z) . x = - (tan x)](#enigma-differentiates-ln--cos--z--x----tan-x)
- [Another on Enigma differentiating](#another-on-enigma-differentiating)
- [And another](#and-another)
- [Another differentiation: (exp (arctan + arccot))' = 0](#another-differentiation-exp-arctan--arccot--0)
- [Differentiation: (arccot * exp_R)' = - (exp_R . x) / (1 + ((exp_R . x) ^2)](#differentiation-arccot--exp_r----exp_r--x--1--exp_r--x-2)
- [Differentiantion: (- (exp_R * arccot)) `| Z) . x = (exp_R . (arccot . x)) / (1 + (x ^2))](#differentiantion---exp_r--arccot--z--x--exp_r--arccot--x--1--x-2)
- [Differentiation: (sin * ln)' = (cos (log (number_e,x))) / x](#differentiation-sin--ln--cos-log-number_ex--x)
- [Differentiation: - (cos * ln)' = (sin (log (number_e,x))) / x](#differentiation---cos--ln--sin-log-number_ex--x)
- [Differentiation: (sin * arctan)' . x  = (cos . (arctan . x)) / (1 + (x ^2))](#differentiation-sin--arctan--x---cos--arctan--x--1--x-2)
- [Differentiation: (cos * ln)' x = - (sin . (ln . x)) / x](#differentiation-cos--ln-x----sin--ln--x--x)
- [Differentiation: (exp_R * cos)'  x = - (exp_R  (cos . x)) * sin x](#differentiation-exp_r--cos--x----exp_r--cos--x--sin-x)
- [Differentiation: (- (cot * ln))' x = 1 / (x * (sin (ln x))^2 )](#differentiation---cot--ln-x--1--x--sin-ln-x2-)
- [Differentiation: (- (cot * exp_R))' x = (exp_R x) / (sin (exp_R x))^2](#differentiation---cot--exp_r-x--exp_r-x--sin-exp_r-x2)
- [Differentiation: (- (exp_R * cot))' x = (exp_R (cot x)) / (sin x) ^2](#differentiation---exp_r--cot-x--exp_r-cot-x--sin-x-2)
- [Differentiation: cos'' = -cos](#differentiation-cos---cos)
- [Enigma integrates: integral sin+cos on [0,pi/2] = 2](#enigma-integrates-integral-sincos-on-0pi2--2)
- [Enigma integrates: integral (sin - cos) on [0,pi*2] = 0](#enigma-integrates-integral-sin---cos-on-0pi2--0)
- [Integral: E computes the definite integral of sin * cos on [2n*pi, (2n+1)*pi] using 62 premises and 268 inferences](#integral-e-computes-the-definite-integral-of-sin--cos-on-2npi-2n1pi-using-62-premises-and-268-inferences)
- [Cos is increasing on pi,2pi](#cos-is-increasing-on-pi2pi)
- [Additivity of integral](#additivity-of-integral)
- [Integral of absolute value](#integral-of-absolute-value)
- [Integral: if volume A is non zero then there is a element of the division set with non zero volume](#integral-if-volume-a-is-non-zero-then-there-is-a-element-of-the-division-set-with-non-zero-volume)
- [Integral: equivalent condition on integrability by limits of upper and lower sums being equal](#integral-equivalent-condition-on-integrability-by-limits-of-upper-and-lower-sums-being-equal)
- [Integral: chi (A,A) is integrable & integral chi (A,A) = vol A (486-long ATP proof from 63 premises)](#integral-chi-aa-is-integrable--integral-chi-aa--vol-a-486-long-atp-proof-from-63-premises)
- [Integral: Lebesgue's Bounded Convergence Theorem (1190-long ATP proof from 51 premises)](#integral-lebesgues-bounded-convergence-theorem-1190-long-atp-proof-from-51-premises)
- [Monster proof about partial sums in Lebesgue measure theory - the proof takes 150 Mizar lines](#monster-proof-about-partial-sums-in-lebesgue-measure-theory---the-proof-takes-150-mizar-lines)
- [Measure theory - limit of partial sums](#measure-theory---limit-of-partial-sums)
- [Sum of the zero^p series - lp spaces](#sum-of-the-zerop-series---lp-spaces)
- [Dynkin systems generated by intersection-closed sets are intersection-closed](#dynkin-systems-generated-by-intersection-closed-sets-are-intersection-closed)
- [Infinity of { k : k &gt; n }](#infinity-of--k--k--n-)
- [Almost infinitude of primes:](#almost-infinitude-of-primes)
- [Fibonacci numbers - alternative proof (no induction needed) of  tau ^ n + tau ^ (n + 1) = tau ^ (n + 2)](#fibonacci-numbers---alternative-proof-no-induction-needed-of--tau--n--tau--n--1--tau--n--2)
- [Fibonacci numbers - much simpler alternative proof of the (probably over-simplified) Mizar version of Carmichael's theorem](#fibonacci-numbers---much-simpler-alternative-proof-of-the-probably-over-simplified-mizar-version-of-carmichaels-theorem)
- [Fibonacci and Lucas numbers](#fibonacci-and-lucas-numbers)
- [37 is a prime number](#37-is-a-prime-number)
- [43 is prime](#43-is-prime)
- [163 is prime](#163-is-prime)
- [17 is prime](#17-is-prime)
- [Massive counting ATP-style: Enumerate all numbers smaller than 64](#massive-counting-atp-style-enumerate-all-numbers-smaller-than-64)
- [Number theory: { a: a < m } is a complete residue system for m](#number-theory--a-a--m--is-a-complete-residue-system-for-m)
- [The radical of square-free k is k](#the-radical-of-square-free-k-is-k)
- [Combinatorics and counting - coefficient in binomial expansion](#combinatorics-and-counting---coefficient-in-binomial-expansion)
- [Counting - partial product of a constant sequence](#counting---partial-product-of-a-constant-sequence)
- [Topology - discrete is T_2](#topology---discrete-is-t_2)
- [Topology: T 1/2 is T0](#topology-t-12-is-t0)
- [Topology - The Hausdorff condition (T_2) is preserved under homeomorphism](#topology---the-hausdorff-condition-t_2-is-preserved-under-homeomorphism)
- [Topology: the union of finitely many compact sets is compact](#topology-the-union-of-finitely-many-compact-sets-is-compact)
- [Topology - alternative condition on local compactness](#topology---alternative-condition-on-local-compactness)
- [Topology: alternative proof of length 290 using 45 axioms about characterizations of open functions from R^m](#topology-alternative-proof-of-length-290-using-45-axioms-about-characterizations-of-open-functions-from-rm)
- [Topology - Characterization of Separated Subspaces by Weakly Separated ones.](#topology---characterization-of-separated-subspaces-by-weakly-separated-ones)
- [Topology - T1 is a disjoint union of perfect and scattered](#topology---t1-is-a-disjoint-union-of-perfect-and-scattered)
- [Topology - much shorter alternative proof in second-countable spaces proposed by premise selection](#topology---much-shorter-alternative-proof-in-second-countable-spaces-proposed-by-premise-selection)
- [Connectedness - all points are joined if some is joined to all:](#connectedness---all-points-are-joined-if-some-is-joined-to-all)
- [Connectedness - synthesize and inverse path](#connectedness---synthesize-and-inverse-path)
- [Two points on an arc are connected by a subarc](#two-points-on-an-arc-are-connected-by-a-subarc)
- [Construct an internal point on an arc](#construct-an-internal-point-on-an-arc)
- [Intermediate value theorem](#intermediate-value-theorem)
- [Image of an upper bound of a closed interval is an upper bound of the image under a continuous bijection](#image-of-an-upper-bound-of-a-closed-interval-is-an-upper-bound-of-the-image-under-a-continuous-bijection)
- [X is locally connected iff components of open sets are open](#x-is-locally-connected-iff-components-of-open-sets-are-open)
- [Real plane: Simple closed curves are pathwise connected](#real-plane-simple-closed-curves-are-pathwise-connected)
- [Real plane: order of points](#real-plane-order-of-points)
- [Real plane: Extremality in cells - 250-line long proof in Mizar, 415 ATP steps from 31 premises](#real-plane-extremality-in-cells---250-line-long-proof-in-mizar-415-atp-steps-from-31-premises)
- [Topology: correspondence of two notions of homotopy - 420-long proof from 64 premises](#topology-correspondence-of-two-notions-of-homotopy---420-long-proof-from-64-premises)
- [Any two simple closed curves are homeomorphic](#any-two-simple-closed-curves-are-homeomorphic)
- [The union of the unbounded components of the empty set is the whole R^n](#the-union-of-the-unbounded-components-of-the-empty-set-is-the-whole-rn)
- [Characterization of open functions from R to R^m](#characterization-of-open-functions-from-r-to-rm)
- [Characterization of continuous functions from R to R^m](#characterization-of-continuous-functions-from-r-to-rm)
- [Characterization of continuous functions from R^m to R](#characterization-of-continuous-functions-from-rm-to-r)
- [Continuity in topology derived from a metric space](#continuity-in-topology-derived-from-a-metric-space)
- [r-circle is a subspace of r-square](#r-circle-is-a-subspace-of-r-square)
- [Circle rotation has no fixpoint](#circle-rotation-has-no-fixpoint)
- [The diameter of the convex hull of A is equal to the diameter of A](#the-diameter-of-the-convex-hull-of-a-is-equal-to-the-diameter-of-a)
- [A set in R^n is bounded iff its convex hull is bounded](#a-set-in-rn-is-bounded-iff-its-convex-hull-is-bounded)
- [Affine sets are convex](#affine-sets-are-convex)
- [Constant is a continuous function to R](#constant-is-a-continuous-function-to-r)
- [Quotient of even functions is an even function](#quotient-of-even-functions-is-an-even-function)
- [Probability - counting with probabilities](#probability---counting-with-probabilities)
- [Probability: probability of (disjoint) unions - 360-long E proof](#probability-probability-of-disjoint-unions---360-long-e-proof)
- [Pythagorean theorem in inner product spaces](#pythagorean-theorem-in-inner-product-spaces)
- [In a unitary space you can inscribe a ball around any point inside a bigger ball](#in-a-unitary-space-you-can-inscribe-a-ball-around-any-point-inside-a-bigger-ball)
- [The union of the sphere and the open ball is the closed ball](#the-union-of-the-sphere-and-the-open-ball-is-the-closed-ball)
- [Balls are preserved under mirroring](#balls-are-preserved-under-mirroring)
- [Convergence of exponentials in Banach spaces - 267-long proof](#convergence-of-exponentials-in-banach-spaces---267-long-proof)
- [Partial sums in normed spaces](#partial-sums-in-normed-spaces)
- [A derived sequence of n-th roots of a sequence that eventually grows above 0 is not summable](#a-derived-sequence-of-n-th-roots-of-a-sequence-that-eventually-grows-above-0-is-not-summable)
- [Complex sequences - alternative proof than in Mizar](#complex-sequences---alternative-proof-than-in-mizar)
- [Real sequences: characterization of a lower bound - 55-line long Mizar proof](#real-sequences-characterization-of-a-lower-bound---55-line-long-mizar-proof)
- [Real sequences - growth rate: Big_Omega (f + g) = Big_Omega max (f,g) - alternative proof than in Mizar](#real-sequences---growth-rate-big_omega-f--g--big_omega-max-fg---alternative-proof-than-in-mizar)
- [There is a vector of norm 1 in a nontrivial normed space](#there-is-a-vector-of-norm-1-in-a-nontrivial-normed-space)
- [A point that is not in a closed set has a non-zero distance to it.](#a-point-that-is-not-in-a-closed-set-has-a-non-zero-distance-to-it)
- [Open sets are complements of closed in complex spaces](#open-sets-are-complements-of-closed-in-complex-spaces)
- [First isomorphism theorem for universal algebras](#first-isomorphism-theorem-for-universal-algebras)
- [The lattice of subalgebras of a many-sorted algebra is lower/upper-bounded - 291-long proof](#the-lattice-of-subalgebras-of-a-many-sorted-algebra-is-lowerupper-bounded---291-long-proof)
- [Lattices: a subrelation is closed on finite joins iff it is closed on joins of pairs](#lattices-a-subrelation-is-closed-on-finite-joins-iff-it-is-closed-on-joins-of-pairs)
- [Lattices: The image of a monotone function on a lower-bounded poset is lower-bounded](#lattices-the-image-of-a-monotone-function-on-a-lower-bounded-poset-is-lower-bounded)
- [Lattices: element is irreducible iff it is in every finite set of which it is the infimum](#lattices-element-is-irreducible-iff-it-is-in-every-finite-set-of-which-it-is-the-infimum)
- [Products of semilattices have infima](#products-of-semilattices-have-infima)
- [Boolean posets: inclusion poset of a subset family of X is a full subrelation of the boolean poset on X - 50-line proof in Mizar](#boolean-posets-inclusion-poset-of-a-subset-family-of-x-is-a-full-subrelation-of-the-boolean-poset-on-x---50-line-proof-in-mizar)
- [Relations: being quasi-ordered and Dickson is preserverd under iso ; 464-long ATP proof from 37 premises, 70-line Mizar proof](#relations-being-quasi-ordered-and-dickson-is-preserverd-under-iso--464-long-atp-proof-from-37-premises-70-line-mizar-proof)
- [Logic: A set of formulas is inconsistent iff it proves everything](#logic-a-set-of-formulas-is-inconsistent-iff-it-proves-everything)
- [Logic: Long inductive proof about free variables](#logic-long-inductive-proof-about-free-variables)
- [Topology - product of T_0 spaces is T_0](#topology---product-of-t_0-spaces-is-t_0)
- [Rational numbers - lots of computation, many proof formulas/clauses](#rational-numbers---lots-of-computation-many-proof-formulasclauses)
- [Graph theory: oriented chain determines the oriented vertex sequence](#graph-theory-oriented-chain-determines-the-oriented-vertex-sequence)
- [Graph theory: if G has clique# &lt;=1 its Mycielskian has clique# &lt;= 2](#graph-theory-if-g-has-clique-1-its-mycielskian-has-clique--2)
- [Graph algorithms: lexicografic breadth-first search labels the whole graph](#graph-algorithms-lexicografic-breadth-first-search-labels-the-whole-graph)
- [Modules: linearly independent sets don't contain 0](#modules-linearly-independent-sets-dont-contain-0)
- [Orthogonal spaces: being orthogonal to the same set implies being parallel](#orthogonal-spaces-being-orthogonal-to-the-same-set-implies-being-parallel)
- [Orthogonal spaces: translational is satisfying_des - alternative proof](#orthogonal-spaces-translational-is-satisfying_des---alternative-proof)
- [Lines in Euclidean Space: Being parallel is transitive](#lines-in-euclidean-space-being-parallel-is-transitive)
- [Ordinals: If A is a limit ordinal so is B + A](#ordinals-if-a-is-a-limit-ordinal-so-is-b--a)
- [Cardinals: cofinality of omega = omega - alternative proof from 38 premises](#cardinals-cofinality-of-omega--omega---alternative-proof-from-38-premises)
- [Cardinal arithmetics - exp (M+N) = exp M * exp N](#cardinal-arithmetics---exp-mn--exp-m--exp-n)
- [Cardinalities:](#cardinalities)
- [Cardinals and (ultra)filters: Filters that extend the Frechet Filter contain only sets of the same cardinality.](#cardinals-and-ultrafilters-filters-that-extend-the-frechet-filter-contain-only-sets-of-the-same-cardinality)
- [Combinatorial consequence of regularity - alternative short proof based on a nontrivial previous lemma](#combinatorial-consequence-of-regularity---alternative-short-proof-based-on-a-nontrivial-previous-lemma)
- [Groebner bases](#groebner-bases)
- [Groebner bases - reduction](#groebner-bases---reduction)
- [Groebner basis -  G is Groebner basis wrt T iff for f being non-zero Polynomial of n,L st f in G -Ideal holdsf has_a_Standard_Representation_of G,T](#groebner-basis----g-is-groebner-basis-wrt-t-iff-for-f-being-non-zero-polynomial-of-nl-st-f-in-g--ideal-holdsf-has_a_standard_representation_of-gt)
- [Matrices: M has full rank iff Det M &lt;&gt; 0](#matrices-m-has-full-rank-iff-det-m--0)
- [Matrices: The determinant of an empty matrix is 1 . 366-inference proof using 80 axioms.](#matrices-the-determinant-of-an-empty-matrix-is-1--366-inference-proof-using-80-axioms)
- [Matrices: formula for computing the determinant of a 2x2 matrix - short alternative proof](#matrices-formula-for-computing-the-determinant-of-a-2x2-matrix---short-alternative-proof)
- [Matrices: a linear transformation given by an n x m matrix M is onto iff the rank of M is m  (552-long ATP proof using 80 premises)](#matrices-a-linear-transformation-given-by-an-n-x-m-matrix-m-is-onto-iff-the-rank-of-m-is-m--552-long-atp-proof-using-80-premises)
- [Matrices: The shape of rotation matrices in R^1 (444-long ATP proof from 80 premises)](#matrices-the-shape-of-rotation-matrices-in-r1-444-long-atp-proof-from-80-premises)
- [Matrices: explicit form for a square 3-matrix - 158-line proof in Mizar](#matrices-explicit-form-for-a-square-3-matrix---158-line-proof-in-mizar)
- [Matrices: A 1-dimensional square matrix is its own transposition](#matrices-a-1-dimensional-square-matrix-is-its-own-transposition)
- [Matrices: a constant square matrix is it own transposition](#matrices-a-constant-square-matrix-is-it-own-transposition)
- [Matrices and theri permutations](#matrices-and-theri-permutations)
- [Matrices: monster proof - 210-line long in Mizar](#matrices-monster-proof---210-line-long-in-mizar)
- [Matrices: longish proof about swapping lines - 64 lines in Mizar](#matrices-longish-proof-about-swapping-lines---64-lines-in-mizar)
- [Divergence of locally greater function](#divergence-of-locally-greater-function)
- [Cardinalities](#cardinalities-1)
- [Longer proof about programs and sequences with 59/663 used/initial axioms](#longer-proof-about-programs-and-sequences-with-59663-usedinitial-axioms)
- [Longish about sequences on goboard (in the proof of Jordan)](#longish-about-sequences-on-goboard-in-the-proof-of-jordan)
- [Monster proof about the length of special circular sequences - 80 lines in Mizar and 70 ATP axioms](#monster-proof-about-the-length-of-special-circular-sequences---80-lines-in-mizar-and-70-atp-axioms)
- [Longish proof in INT_5](#longish-proof-in-int_5)
- [Longish proof in ORDERS_1](#longish-proof-in-orders_1)


  

### Lipschitzian is uniformly continuous: 
http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ncfcont2.html#T25

E proof: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t25_ncfcont2
261 axioms, 373 initial clauses, 1534 processed, 11.2 generated, 38s, 135 proof clause steps, 36/79 initial proof flas/clauses, lots of calculation

### Metric spaces: Two compact sets with Hausdorff distance 0 are equal

for M being non empty MetrSpace
for P, Q being non empty Subset of (TopSpaceMetr M) st P is compact & Q is compact & HausDist (P,Q) = 0 holds
P = Q

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/hausdorf.html#T37

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t37_hausdorf

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_389-query256-ctx768-w0-coop/t37_hausdorf
```
# Proof object clause steps            : 314
# Proof object initial clauses used    : 84
# Proof object initial formulas used   : 59
# Proof object simplifying inferences  : 247
# Parsed axioms                        : 160
# Initial clauses in saturation        : 242
# Processed clauses                    : 1901
# ...remaining for further processing  : 1313
# Generated clauses                    : 9664
# ...of the previous two non-trivial   : 8376
# User time                : 24.207 s
```


### Matric spaces: relation of point distances to distance of compact sets - 440 step proof from 82 premises

for M being non empty MetrSpace
for P, Q being Subset of (TopSpaceMetr M) st P is compact & Q is compact holds
for x1, x2 being Point of M st x1 in P & x2 in Q holds
( min_dist_min (P,Q) <= dist (x1,x2) & dist (x1,x2) <= max_dist_max (P,Q) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/weierstr.html#T34

E proof (gnn - gpu server trained on minimized data) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t34_weierstr

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.l10i2e132m1q128c512_minms1/t34_weierstr
```
# Proof object clause steps            : 440
# Proof object initial clauses used    : 111
# Proof object initial formulas used   : 82
# Proof object simplifying inferences  : 324
# Parsed axioms                        : 155
# Initial clauses in saturation        : 247
# Processed clauses                    : 5576
# ...remaining for further processing  : 3309
# Generated clauses                    : 40708
# ...of the previous two non-trivial   : 39793
# User time                : 25.266 s
```


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

### Massive counting in trigonometry - 445-long proof from 83 formulas

for x being set st x in \[.(- (PI / 2)),(- (PI / 4)).\] holds
cosec . x in \[.(- (sqrt 2)),(- 1).\]

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sincos10.html#T35

E proof (gnn) with lgb premise selection (0.5k1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t35_sincos10

/local1/mptp/convert_models/grid8bb1_60/mzr02-epoch1_mizar_8_96ffb007719f4afdb4a1e67b65c3d8cb_24-query1024-ctx1024-w0-solo--0.5k1-rest/t35_sincos10
```
# Proof object clause steps            : 445
# Proof object initial clauses used    : 103
# Proof object initial formulas used   : 83
# Proof object simplifying inferences  : 235
# Parsed axioms                        : 437
# Initial clauses in saturation        : 612
# Processed clauses                    : 3092
# ...remaining for further processing  : 1882
# Generated clauses                    : 21182
# ...of the previous two non-trivial   : 18616
# User time                : 24.423 s
```

### Another trig counting - 619-long proof from 83 formulas and 1025 initial axioms

for x being set st x in \[.(- (sqrt 2)),(- 1).\] holds
arcsec2 . x in \[.((3 / 4) * PI),PI.\]

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sincos10.html#T86

E proof (3-phase parental+lgb+gnn-server) using 83 of the 1025 human-supplied premises (bushy): 
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t86_sincos10

/local1/mptp/parents/out2/2pb3l8-query1024-ctx2048-w0-coop-srv-local1-f1711-jj1-zar-parents_nothr_gnnm2_0.2_0.005.all/t86_sincos10
```
# Proof object clause steps            : 619
# Proof object initial clauses used    : 97
# Proof object initial formulas used   : 83
# Proof object simplifying inferences  : 362
# Parsed axioms                        : 1025
# Initial clauses in saturation        : 1226
# Processed clauses                    : 12531
# ...remaining for further processing  : 5344
# Generated clauses                    : 143631
# ...of the previous two non-trivial   : 108660
# User time                : 59.713 s
```


### Another trig counting - 224 steps and 54 formulas

for x being set st x in \[.(- 1),1.\] holds
arccot . x in \[.(PI / 4),((3 / 4) * PI).\]

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos9.html#T50

E proof (gnn) with lgb premise selection (0.5k1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t50_sin_cos9

/local1/mptp/convert_models/grid8bb1_60/mzr02-epoch1_mizar_8_96ffb007719f4afdb4a1e67b65c3d8cb_24-query1024-ctx1024-w0-solo--0.5k1-rest/t50_sin_cos9
```
# Proof object clause steps            : 224
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 54
# Proof object simplifying inferences  : 126
# Parsed axioms                        : 677
# Initial clauses in saturation        : 868
# Processed clauses                    : 4938
# ...remaining for further processing  : 2955
# Generated clauses                    : 30734
# ...of the previous two non-trivial   : 26103
# User time                : 37.275 s
```

### Trig counting - Arg x < PI & Arg y < PI implies Arg (x + y) < PI (343-long ATP proof from 56 premises)

for x, y being complex number st Arg x < PI & Arg y < PI holds
Arg (x + y) < PI

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/complex2.html#T20

E proof (gnn - gpu server) with heuristic premise selection (subproblem mnimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_complex2

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub5.l10e49m2q512c1024/t20_complex2
```
# Proof object clause steps            : 343
# Proof object initial clauses used    : 68
# Proof object initial formulas used   : 56
# Proof object simplifying inferences  : 257
# Parsed axioms                        : 74
# Initial clauses in saturation        : 105
# Processed clauses                    : 4177
# ...remaining for further processing  : 1323
# Generated clauses                    : 104097
# ...of the previous two non-trivial   : 100665
# User time                : 23.393 s
```



### Counting: e^(2\*pi\*n\*i) = 1

for n being Element of NAT holds exp (((2 \* PI) \* n) \* \<i\>) = 1

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/sin_cos3.html#T28

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_sin_cos3

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_35-query512-ctx768-w0-coop/t28_sin_cos3
```
# Proof object clause steps            : 212
# Proof object initial clauses used    : 53
# Proof object initial formulas used   : 48
# Proof object simplifying inferences  : 159
# Parsed axioms                        : 178
# Initial clauses in saturation        : 179
# Processed clauses                    : 2834
# ...remaining for further processing  : 1301
# Generated clauses                    : 33232
# ...of the previous two non-trivial   : 30047
# User time                : 45.267 s
```


### Counting/algebra: 0 < n & 1 < r implies 1 < r ^ n

for r being real number
for n being Nat st 0 < n & 1 < r holds
1 < r |^ n

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/pepin.html#T65

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t65_pepin

/nfs/urbanjo3/air/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_15-query256-ctx512-w0-coop/t65_pepin
```
# Proof object clause steps            : 148
# Proof object initial clauses used    : 44
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 95
# Parsed axioms                        : 157
# Initial clauses in saturation        : 186
# Processed clauses                    : 1411
# ...remaining for further processing  : 821
# Generated clauses                    : 9877
# ...of the previous two non-trivial   : 8667
# User time                : 17.126 s
```

### Counting/algebra: Division with remainder: (n div k) div i = n div (k * i)

for n, k, i being Nat holds (n div k) div i = n div (k * i)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/nat_2.html#T27

We cannot replay the original proof yet, but an alternative proof was found using a seemingly very similar theorem about positive integers: http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/pre_ff.html#T5 (whch has quite a different proof).

The alternative proof is however still nontrivial - possibly because of the need to move between different definitions.

E proof (blistr) with gnn premise selection (0): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t27_nat_2

/local1/mptp/gnn_pred_train_big_knn512_all.probs_out_all/gnn_pred_train_big_knn512_all.probs.eprotokoll_atpstr_my_fdfa75aeb82cfb954998cf278fcefc11586a3a4bs2__preds__0/t27_nat_2
```
# Proof object clause steps            : 111
# Proof object initial clauses used    : 27
# Proof object initial formulas used   : 23
# Proof object simplifying inferences  : 39
# Parsed axioms                        : 125
# Initial clauses in saturation        : 169
# Processed clauses                    : 7053
# ...remaining for further processing  : 5298
# Generated clauses                    : 101854
# ...of the previous two non-trivial   : 100586
# User time                : 1.565 s
```

### Counting/algebra: n mod 2 = 0 iff (n -' 1) mod 2 = 1 - large alternative proof using 51 premises

for n being Nat st n > 0 holds n mod 2 = 0 iff (n -' 1) mod 2 = 1 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/nat_2.html#T18

E proof (blistr) with knn premise selection (256): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t18_nat_2

/local1/mptp/miz60-cek-out/train-n.5knn.2-probs_out/train-n.5knn.2.emzr03s2__preds__256/t18_nat_2
```
# Proof object clause steps            : 227
# Proof object initial clauses used    : 58
# Proof object initial formulas used   : 51
# Proof object simplifying inferences  : 145
# Parsed axioms                        : 257
# Initial clauses in saturation        : 424
# Processed clauses                    : 4807
# ...remaining for further processing  : 3835
# Generated clauses                    : 13913
# ...of the previous two non-trivial   : 13485
# User time                : 0.823 s
```

### List editing set-theory style

for p1, p2, p3, q being Element of D holds Replace (<\*p1,p2,p3\*>,3,q) = <\*p1,p2,q\*>

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/finseq_7.html#T17

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t17_finseq_7

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_79-query768-ctx1536-w0-solo/t17_finseq_7
```
# Proof object clause steps            : 148
# Proof object initial clauses used    : 59
# Proof object initial formulas used   : 47
# Proof object simplifying inferences  : 142
# Parsed axioms                        : 194
# Initial clauses in saturation        : 243
# Processed clauses                    : 2213
# ...remaining for further processing  : 1080
# Generated clauses                    : 16633
# ...of the previous two non-trivial   : 15781
# User time                : 52.697 s
```

### Lists: sum of a sequence is preserved under reversal in AC contexts

for V being non empty Abelian add-associative right_zeroed addLoopStr
for p being FinSequence of the carrier of V holds Sum p = Sum (Rev p)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/polynom3.html#T2

E proof (gnn - gpu server trained on minimized proofs) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_polynom3

The proof uses 38 premises. Note that the inductive step is however not invented here - the instantiated scheme is supplied is a premise.

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.l10i2e132m1q128c512_minms1/t2_polynom3
```
# Proof object clause steps            : 230
# Proof object initial clauses used    : 56
# Proof object initial formulas used   : 38
# Proof object simplifying inferences  : 101
# Parsed axioms                        : 180
# Initial clauses in saturation        : 291
# Processed clauses                    : 1927
# ...remaining for further processing  : 1223
# Generated clauses                    : 11706
# ...of the previous two non-trivial   : 10893
# User time                : 4.846 s
```


### Permutations set-theory style - the Mizar proof has 144 lines

for f being FinSequence st  f = <\*1,2\*> or f = <\*2,1\*>  holds
f is Permutation of Seg 2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_7.html#T2

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_matrix_7

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_31-query256-ctx768-w0-coop/t2_matrix_7
```
# Proof object clause steps            : 193
# Proof object initial clauses used    : 51
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 180
# Parsed axioms                        : 99
# Initial clauses in saturation        : 163
# Processed clauses                    : 3026
# ...remaining for further processing  : 1458
# Generated clauses                    : 18434
# ...of the previous two non-trivial   : 16563
# User time                : 33.684 s
```

### Dyadic numbers 

dyadic 1 = {0,(1 / 2),1}

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/urysohn1.html#T3

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t3_urysohn1

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_51-query128-ctx256-w0-solo/t3_urysohn1
```
# Proof object clause steps            : 151
# Proof object initial clauses used    : 60
# Proof object initial formulas used   : 49
# Proof object simplifying inferences  : 139
# Parsed axioms                        : 146
# Initial clauses in saturation        : 178
# Processed clauses                    : 1379
# ...remaining for further processing  : 759
# Generated clauses                    : 9272
# ...of the previous two non-trivial   : 7858
# User time                : 14.307 s
```

### Matroids: maximal independent subsets

for M being finite-degree Matroid
for C being Subset of M
for A being independent Subset of M holds
( A is_maximal_independent_in C iff ( A c= C & card A = Rnk C ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matroid0.html#T19

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t19_matroid0

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t19_matroid0
```
# Proof object clause steps            : 121
# Proof object initial clauses used    : 36
# Proof object initial formulas used   : 16
# Proof object simplifying inferences  : 87
# Parsed axioms                        : 94
# Initial clauses in saturation        : 136
# Processed clauses                    : 484
# ...remaining for further processing  : 385
# Generated clauses                    : 1846
# ...of the previous two non-trivial   : 1701
# User time                : 13.764 s
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

### Convergence of a real sequence is the same in the real metric space

for s being Real_Sequence
for S being sequence of RealSpace st s = S holds
( s is convergent implies S is convergent ) & ( S is convergent implies s is convergent ) & ( s is convergent implies lim s = lim S )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topmetr3.html#T4

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t4_topmetr3

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_37-query256-ctx768-w0-solo/t4_topmetr3
```
# Proof object clause steps            : 293
# Proof object initial clauses used    : 81
# Proof object initial formulas used   : 43
# Proof object simplifying inferences  : 295
# Parsed axioms                        : 74
# Initial clauses in saturation        : 137
# Processed clauses                    : 2225
# ...remaining for further processing  : 943
# Generated clauses                    : 8820
# ...of the previous two non-trivial   : 7935
# User time                : 72.666 s
```

### Convergence: if a whole sequence is <= p then its limit <= p

for seq being ExtREAL_sequence
for p being ext-real number st seq is convergent & ( for k being Nat holds seq . k <= p ) holds
lim seq <= p

53-line proof in Mizar. The ATP proof uses 59 axioms.

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfunc9.html#T9

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t9_mesfunc9

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_57-query768-ctx1024-w0-solo/t9_mesfunc9
```
# Proof object clause steps            : 251
# Proof object initial clauses used    : 75
# Proof object initial formulas used   : 59
# Proof object simplifying inferences  : 112
# Parsed axioms                        : 159
# Initial clauses in saturation        : 247
# Processed clauses                    : 3194
# ...remaining for further processing  : 2067
# Generated clauses                    : 29250
# ...of the previous two non-trivial   : 28403
# User time                : 116.084 s
```

### Convergence: limit of a sequence bounded between two sequences with the same limit - simple alternative proof

for seq, seq9, seq1 being Real_Sequence st seq is convergent & seq9 is convergent & ( for n being Element of NAT holds
 seq . n <= seq1 . n & seq1 . n <= seq9 . n  ) & lim seq = lim seq9 holds
lim seq1 = lim seq

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/seq_2.html#T20

The original proof has 49 lines and we cannot replay it yet. But a simple alternative proof was found going via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/seq_2.html#T19 and http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/seq_2.html#T18 .

E proof (blistr) with knn premise selection (256): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_seq_2

/local1/mptp/miz60-cek-out/train-n.5knn.2-probs_out/train-n.5knn.2.emzr02s2__preds__256/t20_seq_2
```
# Proof object clause steps            : 64
# Proof object initial clauses used    : 24
# Proof object initial formulas used   : 8
# Proof object simplifying inferences  : 76
# Parsed axioms                        : 257
# Initial clauses in saturation        : 495
# Processed clauses                    : 2635
# ...remaining for further processing  : 1794
# Generated clauses                    : 13481
# ...of the previous two non-trivial   : 12481
# User time                : 0.814 s
```


### Topology: In compact spaces, Cauchy nets are convergent

for T being non empty TopSpace holds
( T is compact iff for N being net of T st N is Cauchy holds
N is convergent )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow19.html#T36

E proof (gnn) with lgb premise selection (0.05): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t36_yellow19

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop--0.05/t36_yellow19
```
# Proof object clause steps            : 203
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 35
# Proof object simplifying inferences  : 128
# Parsed axioms                        : 106
# Initial clauses in saturation        : 191
# Processed clauses                    : 1561
# ...remaining for further processing  : 915
# Generated clauses                    : 6659
# ...of the previous two non-trivial   : 5759
# User time                : 17.906 s
```

### Topology: equivalent condition on homeomorphism: bijection plus images of open are open

for S, T being non empty TopStruct
for f being Function of S,T holds
  f is being_homeomorphism 
  iff  
  dom f = [#] S & rng f = [#] T & f is one-to-one 
  & for P being Subset of S holds P is open iff f .: P is open 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topgrp_1.html#T25

E proof (gnn - gpu server) with Mizar40 minimized premise selection : http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t25_topgrp_1__0

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All.l10e49m1q128c512_m40/t25_topgrp_1__0
```
# Proof object clause steps            : 198
# Proof object initial clauses used    : 55
# Proof object initial formulas used   : 28
# Proof object simplifying inferences  : 175
# Parsed axioms                        : 39
# Initial clauses in saturation        : 95
# Processed clauses                    : 945
# ...remaining for further processing  : 609
# Generated clauses                    : 4161
# ...of the previous two non-trivial   : 3947
# User time                : 2.306 s
```





### Lattices: lower bounded up-complete L where SupMap L is upper adjoint is continuous

for L being lower-bounded up-complete LATTICE st SupMap L is upper_adjoint holds
L is continuous

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel_5.html#T4

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t4_waybel_5

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_389-query256-ctx768-w0-coop/t4_waybel_5
```
# Proof object clause steps            : 269
# Proof object initial clauses used    : 80
# Proof object initial formulas used   : 44
# Proof object simplifying inferences  : 179
# Parsed axioms                        : 169
# Initial clauses in saturation        : 275
# Processed clauses                    : 2203
# ...remaining for further processing  : 1457
# Generated clauses                    : 10456
# ...of the previous two non-trivial   : 9609
# User time                : 34.533 s
```

### Lattices: equivalent condition on being prime in a semillatice

389-long proof in 26s using 3-phase ENIGMA.

for L being Semilattice
for l being Element of L holds
l is prime iff for A being non empty finite Subset of L st l >= inf A holds ex a being Element of L st
a in A & l >= a 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel_6.html#T22

E proof (3-phase parental+lgb+gnn-server) using 37 of the 258 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_waybel_6

/local1/mptp/parents/out2/2pl10r3b_e39s30q256c768f1711_parents_froc_gnn_m2_0.01.train/t22_waybel_6
```
# Proof object clause steps            : 389
# Proof object initial clauses used    : 78
# Proof object initial formulas used   : 37
# Proof object simplifying inferences  : 444
# Parsed axioms                        : 258
# Initial clauses in saturation        : 497
# Processed clauses                    : 4584
# ...remaining for further processing  : 2366
# Generated clauses                    : 35102
# ...of the previous two non-trivial   : 14443
# User time                : 22.559 s
```



### Lattices: Dual of a complete-distributive poset is complete-dsitributive ; 377-long ATP proof from 35 premises

for L being non empty Poset holds
 L is completely-distributive iff L opp is completely-distributive 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow_7.html#T51

E proof (mzr03) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t51_yellow_7

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr03s30_minms1/t51_yellow_7
```
# Proof object clause steps            : 377
# Proof object initial clauses used    : 66
# Proof object initial formulas used   : 35
# Proof object simplifying inferences  : 435
# Parsed axioms                        : 35
# Initial clauses in saturation        : 83
# Processed clauses                    : 5130
# ...remaining for further processing  : 3906
# Generated clauses                    : 7451
# ...of the previous two non-trivial   : 7607
# User time                : 2.315 s
```


### Monster proof in continuous lattices relating a weight of an infinite T0 topological space to the weight of the semilattice formed by the inclusion poset of its topology

for T being non empty T_0 TopSpace
for L1 being lower-bounded continuous sup-Semilattice st InclPoset the topology of T = L1 & T is infinite holds
weight T = CLweight L1

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel31.html#T6

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_waybel31

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t6_waybel31
```
# Proof object clause steps            : 363
# Proof object initial clauses used    : 76
# Proof object initial formulas used   : 39
# Proof object simplifying inferences  : 525
# Parsed axioms                        : 124
# Initial clauses in saturation        : 201
# Processed clauses                    : 5785
# ...remaining for further processing  : 2300
# Generated clauses                    : 32260
# ...of the previous two non-trivial   : 29920
# User time                : 57.930 s
```

### Continuous lattices: Proposition 2.1 of [CCL](https://www.amazon.com/Compendium-Continuous-Lattices-G-Gierz/dp/3642676804) (p. 112), 1 <=> 6 ; 1039-long ATP proof

for S, T being complete Scott TopLattice
for f being Function of S,T st S is algebraic & T is algebraic holds
f is continuous iff for x being Element of S
for k being Element of T st k in the carrier of CompactSublatt T holds
( k <= f . x iff ex j being Element of S st
 j in the carrier of CompactSublatt S & j <= x & k <= f . j  ) 


http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel17.html#T27

E proof (mzr03) with heuristic premise selection (subproof minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t27_waybel17

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr03s30_minms1/t27_waybel17
```
# Proof object clause steps            : 1039
# Proof object initial clauses used    : 111
# Proof object initial formulas used   : 6
# Proof object simplifying inferences  : 4865
# Parsed axioms                        : 10
# Initial clauses in saturation        : 124
# Processed clauses                    : 3491
# ...remaining for further processing  : 2289
# Generated clauses                    : 14655
# ...of the previous two non-trivial   : 13195
# User time                : 2.515 s
```

### Continuous lattices: Exercise 2.16 of [CCL](https://www.amazon.com/Compendium-Continuous-Lattices-G-Gierz/dp/3642676804) (p. 156), 1 <=> 2 ; 563-long ATP proof from 30 premises

for N being complete Lawson meet-continuous TopLattice holds
N is algebraic iff  N is with_open_semilattices & InclPoset sigma N is algebraic  


http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel30.html#T40

E proof (mzr03) with heuristic premise selection (subproof minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t40_waybel30

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr03s30_minms1/t40_waybel30
```
# Proof object clause steps            : 563
# Proof object initial clauses used    : 81
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 792
# Parsed axioms                        : 32
# Initial clauses in saturation        : 115
# Processed clauses                    : 1038
# ...remaining for further processing  : 901
# Generated clauses                    : 1415
# ...of the previous two non-trivial   : 1386
# User time                : 0.325 s
```



### Lattices - concept lattices isomorphism 

for L being complete Lattice holds ConceptLattice (Context L),L are_isomorphic

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/conlat_2.html#T15

The proof needs to invent two functions to show that lattices are isomorphic (http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/conlat_2.html#T14) .

E proof (gnn - gpu server) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_conlat_2

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.e339m1q256c512/t15_conlat_2
```
# Proof object clause steps            : 249
# Proof object initial clauses used    : 63
# Proof object initial formulas used   : 43
# Proof object simplifying inferences  : 152
# Parsed axioms                        : 98
# Initial clauses in saturation        : 183
# Processed clauses                    : 3783
# ...remaining for further processing  : 1885
# Generated clauses                    : 34331
# ...of the previous two non-trivial   : 26553
# User time                : 21.605 s
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

### card (con_class a) = Index (Normalizer {a})

for G being Group
for a being Element of G holds card (con_class a) = Index (Normalizer {a})

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_3.html#T132

E proof (gnn) using lgb premise selection with 0.005 threshold: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t132_group_3

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_57-query768-ctx1024-w0-solo/t132_group_3
```
# Proof object clause steps            : 134
# Proof object initial clauses used    : 51
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 75
# Parsed axioms                        : 121
# Initial clauses in saturation        : 164
# Processed clauses                    : 1821
# ...remaining for further processing  : 1037
# Generated clauses                    : 18626
# ...of the previous two non-trivial   : 17954
# User time                : 30.063 s
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

### Index of the unit subgroup of G is equal to the cardinality of G

for G being Group holds Index ((1). G) = card G

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_2.html#T152

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t152_group_2

Premise selection with lgb, 0.005

(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__0.005$ less t152_group_2
```
# Proof object clause steps            : 100
# Proof object initial clauses used    : 44
# Proof object initial formulas used   : 28
# Proof object simplifying inferences  : 51
# Parsed axioms                        : 106
# Initial clauses in saturation        : 171
# Processed clauses                    : 2175
# ...remaining for further processing  : 1161
# Generated clauses                    : 11307
# ...of the previous two non-trivial   : 9579
# User time                : 19.164 s
```


### Index of the intersection of subgroups with relatively prime indices 

for A, B being Subgroup of C
for D being Subgroup of A st D = A /\ B holds
for E being Subgroup of B st E = A /\ B holds
for F being Subgroup of C st F = A /\ B & index (C,A), index (C,B) are_relative_prime holds
( index (C,B) = index (A,D) & index (C,A) = index (B,E) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_8.html#T21

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t21_group_8

used lgb premise selection (0.005) to prune 265 axioms to 147

(base) mptp@air-02:~/big2/convert_models/grid8bb1$ less mzr02-premsel_enigma_01_2020_T30_loop02_epoch_29-query256-ctx512-w0-solo/t21_group_8 

```
# Proof object clause steps            : 112
# Proof object initial clauses used    : 43
# Proof object initial formulas used   : 25
# Proof object simplifying inferences  : 213
# Parsed axioms                        : 147
# Initial clauses in saturation        : 190
# Processed clauses                    : 1325
# ...remaining for further processing  : 812
# Generated clauses                    : 5371
# ...of the previous two non-trivial   : 5122
# User time                : 25.997 s
```

Combines reasoning about numbers and groups and their intersections. The Mizar proof has almost 70 lines.


### Groups: The Jordan-Holder property of a composition series is preserved under equivalence ; 297-long ATP proof using 44 premises

for O being set
for G being GroupWithOperators of O
for s1, s2 being CompositionSeries of G st s1 is_equivalent_with s2 & s1 is jordan_holder holds
s2 is jordan_holder

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_9.html#T115

The Mizar proof has 68 lines. The proof requires noticing the series permutation and using it to transfer the J-H properties.

E proof (mzr16) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t115_group_9

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub5.emzr16s30_minms1/t115_group_9
```
# Proof object clause steps            : 297
# Proof object initial clauses used    : 79
# Proof object initial formulas used   : 44
# Proof object simplifying inferences  : 413
# Parsed axioms                        : 71
# Initial clauses in saturation        : 186
# Processed clauses                    : 12661
# ...remaining for further processing  : 7209
# Generated clauses                    : 65614
# ...of the previous two non-trivial   : 57695
# User time                : 7.819 s
```


### Groups: a commutative group is solvable

for G being strict commutative Group holds G is solvable

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/grsolv_1.html#T7

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t7_grsolv_1

The proof needs to assemble the ("obvious") sequence of subgroups.

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop/t7_grsolv_1
```
# Proof object clause steps            : 232
# Proof object initial clauses used    : 68
# Proof object initial formulas used   : 44
# Proof object simplifying inferences  : 143
# Parsed axioms                        : 150
# Initial clauses in saturation        : 255
# Processed clauses                    : 2619
# ...remaining for further processing  : 1522
# Generated clauses                    : 10868
# ...of the previous two non-trivial   : 9541
# User time                : 30.885 s
```

### Groups: analogy between abelian additive and commutative multiplicative groups

for B being AbGroup holds multMagma(# the carrier of B, the addF of B #) is commutative Group

The proof needs to suggest the neutral and inverse elements in the dual setting.

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/vectsp_1.html#T35

E proof (gnn - gpu server trained on minimized proofs) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t35_vectsp_1

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.l10i2e132m1q128c512_minms1/t35_vectsp_1
```
# Proof object clause steps            : 227
# Proof object initial clauses used    : 45
# Proof object initial formulas used   : 24
# Proof object simplifying inferences  : 177
# Parsed axioms                        : 56
# Initial clauses in saturation        : 106
# Processed clauses                    : 1469
# ...remaining for further processing  : 644
# Generated clauses                    : 27747
# ...of the previous two non-trivial   : 26936
# User time                : 14.530 s
```



### Groups with sets: 
for a being Element of G for H being Subgroup of G holds ( a in H iff a * H = carr H )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/group_2.html#T113
E proof: http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t113_group_2
217 fof axioms, 298 initial clauses, 1214 nontriv given, 8523 nontriv gener, 109 proof clause steps, 28/44 initial proof flas/clauses

### Rings: commutative rings are fields iff ideals are trivial

493-long proof in 67s using 3-phase ENIGMA.

for R being non degenerated comRing holds
R is Field iff for I being Ideal of R holds I = {(0. R)} or I = the carrier of R 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ideal_1.html#T22

E proof (3-phase parental+lgb+gnn-server) using 48 of the 416 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_ideal_1

The parental guidance filtered out about60k of the 130k generated clauses.

Then the fast lgb model filtered out 37k of the 67k remaining generated clauses:
```
grep skipped t22_ideal_1 | perl -ne 'm/(\d+) clauses/ or die; $n+=$1; END {print $n,"\n"}' 
37213
```

The gnn gpu server then evaluated the remaining 30k generated clauses, thus allowing 4481 nontrivial given clause loops in 67s:
```
(base) mptp@air-02:~/big2/parents/out2/2pl10r3b_e39s30q1024c1536f1711_parents_froc_gnn_m2_0.01.train$ grep Sendin t22_ideal_1 | perl -ne 'm/query=(\d+)/ or die; $n+=$1; END {print $n,"\n"}' 
30380
```

/local1/mptp/parents/out2/2pl10r3b_e39s30q1024c1536f1711_parents_froc_gnn_m2_0.01.train/t22_ideal_1
```
# Proof object clause steps            : 493
# Proof object initial clauses used    : 93
# Proof object initial formulas used   : 48
# Proof object simplifying inferences  : 690
# Parsed axioms                        : 416
# Initial clauses in saturation        : 699
# Processed clauses                    : 8744
# ...remaining for further processing  : 4481
# Generated clauses                    : 129096
# ...of the previous two non-trivial   : 67594
# User time                : 66.896 s
```



### Vector spaces: dimension of a 2-element vector space is 1 ; 336-long ATP proof from 42 premises, 70-line proof in Mizar

for F being Field
for V being VectSp of F st card (\[#\] V) = 2 holds
dim V = 1

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ranknull.html#T6

E proof (mzr03) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_ranknull

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr03s30_minms1/t6_ranknull
```
# Proof object clause steps            : 336
# Proof object initial clauses used    : 81
# Proof object initial formulas used   : 36
# Proof object simplifying inferences  : 1146
# Parsed axioms                        : 42
# Initial clauses in saturation        : 111
# Processed clauses                    : 13467
# ...remaining for further processing  : 6398
# Generated clauses                    : 16810
# ...of the previous two non-trivial   : 17934
# User time                : 2.549 s
```

### Vector spaces: Explicit formula for linear combination of two (or 1 or 0) vectors

441-long proof in 95s using 3-phase ENIGMA.

for V being RealLinearSpace
for v1, v2 being VECTOR of V st v1 <> v2 holds
for l being Linear_Combination of {v1,v2} holds Sum l = ((l . v1) * v1) + ((l . v2) * v2)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/rlvect_2.html#T33

E proof (3-phase parental+lgb+gnn-server) using 68 of the 396 human-supplied premises (bushy): 
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t33_rlvect_2

/local1/mptp/parents/out2/2pb3l8-query1024-ctx2048-w0-coop-srv-local1-f1711-jj1-zar-parents_nothr_gnnm2_0.2_0.005.all/t33_rlvect_2
```
# Proof object clause steps            : 441
# Proof object initial clauses used    : 96
# Proof object initial formulas used   : 68
# Proof object simplifying inferences  : 658
# Parsed axioms                        : 396
# Initial clauses in saturation        : 603
# Processed clauses                    : 14724
# ...remaining for further processing  : 6028
# Generated clauses                    : 132625
# ...of the previous two non-trivial   : 91692
# User time                : 95.050 s
```


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

### Differentiantion: (- (exp_R * arccot)) `| Z) . x = (exp_R . (arccot . x)) / (1 + (x ^2))

(- (exp_R * arccot) `| Z) . x = (exp_R . (arccot . x)) / (1 + (x ^2))

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integr13.html#T50

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t50_integr13

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_53-query128-ctx256-w0-coop/t50_integr13

```
# Proof object clause steps            : 217
# Proof object initial clauses used    : 83
# Proof object initial formulas used   : 64
# Proof object simplifying inferences  : 253
# Parsed axioms                        : 159
# Initial clauses in saturation        : 222
# Processed clauses                    : 3217
# ...remaining for further processing  : 1926
# Generated clauses                    : 20619
# ...of the previous two non-trivial   : 19748
# User time                : 48.307 s
```



### Differentiation: (sin * ln)' = (cos (log (number_e,x))) / x 

(sin * ln) \`| Z) . x = (cos . (log (number_e,x))) / x )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_6.html#T49

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t49_fdiff_6

Used lgb premise selection with 160 premises

(base) mptp@air-02:/scratch/mptp/bhardpredo2/preds__160$ less t49_fdiff_6

```
# Proof object clause steps            : 189
# Proof object initial clauses used    : 79
# Proof object initial formulas used   : 54
# Proof object simplifying inferences  : 215
# Parsed axioms                        : 161
# Initial clauses in saturation        : 211
# Processed clauses                    : 1856
# ...remaining for further processing  : 1354
# Generated clauses                    : 8219
# ...of the previous two non-trivial   : 7820
# User time                : 12.896 s
```

### Differentiation: - (cos * ln)' = (sin (log (number_e,x))) / x

719-long proof in 94s using 3-phase ENIGMA.

Quite a bit longer than the above proof because of starting with all human-supplied axioms instead of using premise selection.

((- (cos * ln)) \`| Z) . x = (sin . (log (number_e,x))) / x  

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_6.html#T50

E proof (3-phase parental+lgb+gnn-server) using 87 of the 268 human-supplied premises (bushy):
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t50_fdiff_6

/local1/mptp/parents/out2/2pb3l8-query1024-ctx2048-w0-coop-srv-local1-f1711-jj1-zar-parents_nothr_gnnm2_0.2_0.005.all/t50_fdiff_6
```
# Proof object clause steps            : 719
# Proof object initial clauses used    : 116
# Proof object initial formulas used   : 87
# Proof object simplifying inferences  : 699
# Parsed axioms                        : 268
# Initial clauses in saturation        : 347
# Processed clauses                    : 19661
# ...remaining for further processing  : 7361
# Generated clauses                    : 170556
# ...of the previous two non-trivial   : 103430
# User time                : 93.885 s
```


### Differentiation: (sin * arctan)' . x  = (cos . (arctan . x)) / (1 + (x ^2))

for Z being open Subset of REAL st Z c= dom (sin * arctan) & Z c= ].(- 1),1.\[ holds
( sin * arctan is_differentiable_on Z & ( for x being Real st x in Z holds
((sin * arctan) \`| Z) . x = (cos . (arctan . x)) / (1 + (x ^2)) ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_11.html#T13

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t13_fdiff_11

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t13_fdiff_11
```
# Proof object clause steps            : 216
# Proof object initial clauses used    : 66
# Proof object initial formulas used   : 48
# Proof object simplifying inferences  : 154
# Parsed axioms                        : 157
# Initial clauses in saturation        : 204
# Processed clauses                    : 2042
# ...remaining for further processing  : 1225
# Generated clauses                    : 9027
# ...of the previous two non-trivial   : 8328
# User time                : 27.829 s
```

### Differentiation: (cos * ln)' x = - (sin . (ln . x)) / x

((cos * ln) \`| Z) . x = - ((sin . (ln . x)) / x) ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_7.html#T33

E proof (gnn) with lgb premise selection (0.05): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t33_fdiff_7

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_339-query256-ctx512-w0-coop--0.05/t33_fdiff_7
```
# Proof object clause steps            : 238
# Proof object initial clauses used    : 65
# Proof object initial formulas used   : 48
# Proof object simplifying inferences  : 174
# Parsed axioms                        : 104
# Initial clauses in saturation        : 157
# Processed clauses                    : 3611
# ...remaining for further processing  : 1712
# Generated clauses                    : 31842
# ...of the previous two non-trivial   : 30734
# User time                : 51.808 s
```

### Differentiation: (exp_R * cos)'  x = - (exp_R  (cos . x)) * sin x


((exp_R * cos) \`| Z) . x = - ((exp_R . (cos . x)) * (sin . x)) ) )


http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fdiff_7.html#T36

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t36_fdiff_7

/local1/mptp/convert_models/grid8bb1_60/l5-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_137-query256-ctx768-w0-coop/t36_fdiff_7
```
# Proof object clause steps            : 224
# Proof object initial clauses used    : 62
# Proof object initial formulas used   : 45
# Proof object simplifying inferences  : 154
# Parsed axioms                        : 101
# Initial clauses in saturation        : 142
# Processed clauses                    : 2217
# ...remaining for further processing  : 1284
# Generated clauses                    : 14192
# ...of the previous two non-trivial   : 13287
# User time                : 28.404 s
```

### Differentiation: (- (cot * ln))' x = 1 / (x * (sin (ln x))^2 )

338-long proof in 17s using 2-phase ENIGMA.

((- (cot * ln)) \`| Z) . x = 1 / (x * ((sin . (ln . x)) ^2)) 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integr13.html#T27

E proof (2-phase lgb+gnn-server) using 51 of the 471 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t27_integr13

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.devel/t27_integr13

The fast lgb model filtered out 19702 of the 39k generated clauses:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.devel$ grep skipped t27_integr13 | perl -ne 'm/(\d+) clauses/ or die; $n+=$1; END {print $n,"\n"}' 
19702
```

The gnn gpu server then evaluated the remaining 19614 generated clauses, thus allowing 3904 nontrivial given clause loops in 18s:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.devel$ grep Sendin t27_integr13 | perl -ne 'm/query=(\d+)/ or die; $n+=$1; END {print $n,"\n"}' 
19614
```

```
# Proof object clause steps            : 338
# Proof object initial clauses used    : 68
# Proof object initial formulas used   : 51
# Proof object simplifying inferences  : 301
# Parsed axioms                        : 471
# Initial clauses in saturation        : 557
# Processed clauses                    : 6772
# ...remaining for further processing  : 3904
# Generated clauses                    : 40830
# ...of the previous two non-trivial   : 38826
# User time                : 17.858 s
```

### Differentiation: (- (cot * exp_R))' x = (exp_R x) / (sin (exp_R x))^2

401-long proof in 55s using 3-phase ENIGMA.

((- (cot * exp_R)) \`| Z) . x = (exp_R . x) / ((sin . (exp_R . x)) ^2) ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integr13.html#T31

E proof (3-phase parental+lgb+gnn-server) using 60 of the 321 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t31_integr13

The parental filtering filtered out more than half of the 90k generated clauses. 

The fast lgb model filtered out 17674 of the remaining 40k generated clauses.

The gnn gpu server then evaluated the remaining 22716 generated clauses, thus allowing 5471 nontrivial given clause loops in 55s.

/local1/mptp/parents/out2/2pl10r3b_e39s30q256c768f1711_parents_froc_gnn_m2_0.01.train/t31_integr13
```
# Proof object clause steps            : 401
# Proof object initial clauses used    : 84
# Proof object initial formulas used   : 60
# Proof object simplifying inferences  : 322
# Parsed axioms                        : 321
# Initial clauses in saturation        : 391
# Processed clauses                    : 12027
# ...remaining for further processing  : 5471
# Generated clauses                    : 87564
# ...of the previous two non-trivial   : 40397
# User time                : 55.338 s
```

### Differentiation: (- (exp_R * cot))' x = (exp_R (cot x)) / (sin x) ^2

543-long proof in 39s using 2-phase ENIGMA.

((- (exp_R * cot)) \`| Z) . x = (exp_R . (cot . x)) / ((sin . x) ^2) 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integr13.html#T23

E proof (2-phase lgb+gnn-server) using 57 of the 390 human-supplied premises (bushy): 
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t23_integr13

The fast lgb model filtered out 68k of the 106k nontrivial generated clauses:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep skipped t23_integr13 | perl -ne 'm/(\d+) clauses/ or die; $n+=$1;$c++; END {print "$c,$n\n"}'
100,68068
```

The gnn gpu server then evaluated the remaining 38k generated clauses (in 100 rounds), thus allowing 6849 nontrivial given clause loops in 39s:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep Sendin t23_integr13 | perl -ne 'm/query=(\d+)/ or die; $c++; $n+=$1; END {print "$c,$n\n"}'
100,38089
```

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train/t23_integr13
```
# Proof object clause steps            : 543
# Proof object initial clauses used    : 80
# Proof object initial formulas used   : 57
# Proof object simplifying inferences  : 579
# Parsed axioms                        : 390
# Initial clauses in saturation        : 465
# Processed clauses                    : 15343
# ...remaining for further processing  : 6849
# Generated clauses                    : 112913
# ...of the previous two non-trivial   : 105693
# User time                : 39.359 s
```

### Differentiation: cos'' = -cos

303-long proof in 83s using 2-phase ENIGMA.

for x being Real
for Z being open Subset of REAL st x in Z holds
((diff (cos,Z)) . 2) . x = - (cos . x)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/hfdiff_1.html#T12

E proof (2-phase lgb+gnn-server) using 67 of the 339 human-supplied premises (bushy): 
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t12_hfdiff_1

Fast lgb filtering:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep skipped t12_hfdiff_1 | perl -ne 'm/(\d+) clauses/ or die; $n+=$1;$c++; END {print "$c,$n\n"}'
225,197161
```

GNN gpu server evaluations:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep Sendin t12_hfdiff_1 | perl -ne 'm/query=(\d+)/ or die; $c++; $n+=$1; END {print "$c,$n\n"}'
225,73462
```

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train/t12_hfdiff_1
```
# Proof object clause steps            : 303
# Proof object initial clauses used    : 84
# Proof object initial formulas used   : 67
# Proof object simplifying inferences  : 200
# Parsed axioms                        : 339
# Initial clauses in saturation        : 459
# Processed clauses                    : 15911
# ...remaining for further processing  : 6164
# Generated clauses                    : 274617
# ...of the previous two non-trivial   : 270164
# User time                : 83.391 s
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

### Integral: E computes the definite integral of sin * cos on \[2n\*pi, (2n+1)\*pi] using 62 premises and 268 inferences

for A being non empty closed_interval Subset of REAL
for n being Element of NAT st A = \[. 2 * n * PI, ((2 * n) + 1) * PI .] holds
integral (sin (#) cos,A) = 0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra8.html#T95

This is also a proof from alternative premises.

E proof (blistr) with knn premise selection (128): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t95_integra8

/local1/mptp/miz60-cek-out/test-n.5knn.2-probs_out/test-n.5knn.2.eprotokoll_atpstr_my_5fce846ef89413a220d0951fb615d42ded72b119s2__preds__128/t95_integra8
```
# Proof object clause steps            : 268
# Proof object initial clauses used    : 73
# Proof object initial formulas used   : 62
# Proof object simplifying inferences  : 206
# Parsed axioms                        : 129
# Initial clauses in saturation        : 193
# Processed clauses                    : 8365
# ...remaining for further processing  : 3389
# Generated clauses                    : 44511
# ...of the previous two non-trivial   : 39319
# User time                : 1.242 s
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

### Integral of absolute value

|.(Integral (M,f)).| <= Integral (M,|.f.|)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfunc5.html#T101

E proof (gnn) with lgb premise selection (0.05): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t101_mesfunc5

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_243-query128-ctx512-w0-coop--0.05/t101_mesfunc5
```
# Proof object clause steps            : 218
# Proof object initial clauses used    : 68
# Proof object initial formulas used   : 38
# Proof object simplifying inferences  : 273
# Parsed axioms                        : 156
# Initial clauses in saturation        : 210
# Processed clauses                    : 1754
# ...remaining for further processing  : 1127
# Generated clauses                    : 8019
# ...of the previous two non-trivial   : 7874
# User time                : 34.050 s
```

### Integral: if volume A is non zero then there is a element of the division set with non zero volume

291-long proof in 34s using 3-phase ENIGMA.

for A being non empty closed_interval Subset of REAL
for D being Division of A st vol A <> 0 holds
ex i being Element of NAT st i in dom D & vol (divset (D,i)) > 0 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra3.html#T2

E proof (3-phase parental+lgb+gnn-server) using 68 of the 444 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_integra3

/local1/mptp/parents/out2/2pl10r3b_e39s30q256c768f1711_parents_froc_gnn_m2_0.01.train/t2_integra3
```
# Proof object clause steps            : 291
# Proof object initial clauses used    : 86
# Proof object initial formulas used   : 68
# Proof object simplifying inferences  : 189
# Parsed axioms                        : 444
# Initial clauses in saturation        : 689
# Processed clauses                    : 8173
# ...remaining for further processing  : 4198
# Generated clauses                    : 60303
# ...of the previous two non-trivial   : 26971
# User time                : 34.239 s
```

### Integral: equivalent condition on integrability by limits of upper and lower sums being equal

431-long proof in 84s using 3-phase ENIGMA.

for A being non empty closed_interval Subset of REAL
for f being Function of A,REAL st f | A is bounded holds
f is integrable iff for T being DivSequence of A st delta T is convergent & lim (delta T) = 0 holds
lim (upper_sum (f,T)) - lim (lower_sum (f,T)) = 0 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra4.html#T12

E proof (3-phase parental+lgb+gnn-server) using 52 of the 419 human-supplied premises (bushy):
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t12_integra4

/local1/mptp/parents/out2/2pl10r3b_e39s30q1024c1536f1711_parents_froc_gnn_m2_0.01.train/t12_integra4
```
# Proof object clause steps            : 431
# Proof object initial clauses used    : 79
# Proof object initial formulas used   : 52
# Proof object simplifying inferences  : 429
# Parsed axioms                        : 419
# Initial clauses in saturation        : 752
# Processed clauses                    : 18395
# ...remaining for further processing  : 5151
# Generated clauses                    : 228028
# ...of the previous two non-trivial   : 85780
# User time                : 84.198 s
```



### Integral: chi (A,A) is integrable & integral chi (A,A) = vol A (486-long ATP proof from 63 premises)

for A being non empty closed_interval Subset of REAL holds
 chi (A,A) is integrable & integral (chi (A,A)) = vol A 

78-line proof in Mizar: http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/integra4.html#T2

E proof (2-phase lgb+gnn-server) using 63 of the 486 human-supplied premises (bushy):
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_integra4

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.train/t2_integra4

The fast lgb model filtered out 63k of the 99k nontrivial generated clauses:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.train$ grep skipped t2_integra4 | perl -ne 'm/(\d+) clauses/ or die; $n+=$1; END {print $n,"\n"}' 
62820
```

```
# Proof object clause steps            : 486
# Proof object initial clauses used    : 88
# Proof object initial formulas used   : 63
# Proof object simplifying inferences  : 334
# Parsed axioms                        : 486
# Initial clauses in saturation        : 884
# Processed clauses                    : 12161
# ...remaining for further processing  : 5749
# Generated clauses                    : 120176
# ...of the previous two non-trivial   : 98640
# User time                : 41.426 s
```

### Integral: Lebesgue's Bounded Convergence Theorem (1190-long ATP proof from 51 premises)

Suppose {f_n} is a uniformly bounded sequence of measurable functions that converges pointwise to f. 

Then f_n and f are integrable and integral f is equal to the limit of the integrals of f_n.

```
for X being non empty set
for S being SigmaField of X
for M being sigma_Measure of S
for E being Element of S
for F being with_the_same_dom Functional_Sequence of X,REAL 
st M . E < +infty & E = dom (F . 0) 
   &  for n being Nat holds F . n is_measurable_on E  
   & F is uniformly_bounded 
   &  for x being Element of X st x in E holds F # x is convergent 
holds
   for n being Nat holds F . n is_integrable_on M  
   & lim F is_integrable_on M 
   & ex I being ExtREAL_sequence 
     st
      for n being Nat holds I . n = Integral (M,(F . n))  
      & I is convergent 
      & lim I = Integral (M,(lim F)) 
```

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfun9c.html#T49

Note that the Mizar proof is mostly relying on a related previous formulation of the theorem that has much longer Mizar proof: http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfun10.html#T19 . 

I.e., the ATP proof - even if very long - is not the "full proof" of the theorem, but rather a proof of a minor corollary.

E proof (mzr03) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t49_mesfun9c

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub5.emzr03s120_minms1/t49_mesfun9c
```
# Proof object clause steps            : 1190
# Proof object initial clauses used    : 134
# Proof object initial formulas used   : 51
# Proof object simplifying inferences  : 1944
# Parsed axioms                        : 62
# Initial clauses in saturation        : 166
# Processed clauses                    : 37217
# ...remaining for further processing  : 19138
# Generated clauses                    : 53892
# ...of the previous two non-trivial   : 54636
# User time                : 88.283 s
```



### Monster proof about partial sums in Lebesgue measure theory - the proof takes 150 Mizar lines

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfunc9.html#T33

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t33_mesfunc9

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_37-query256-ctx768-w0-solo/t33_mesfunc9
```
# Proof object clause steps            : 201
# Proof object initial clauses used    : 77
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 281
# Parsed axioms                        : 70
# Initial clauses in saturation        : 129
# Processed clauses                    : 2081
# ...remaining for further processing  : 968
# Generated clauses                    : 6522
# ...of the previous two non-trivial   : 6381
# User time                : 49.017 s
```

### Measure theory - limit of partial sums

for X being non empty set
for F being Functional_Sequence of X,ExtREAL
for f being PartFunc of X,ExtREAL
for x being Element of X st F is additive & F is with_the_same_dom & dom f c= dom (F . 0) & x in dom f & F # x is summable & f . x = Sum (F # x) holds
f . x = lim ((Partial_Sums F) # x)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mesfunc9.html#T34

E proof (gnn - gpu server) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t34_mesfunc9

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.e339m1q256c512/t34_mesfunc9
```
# Proof object clause steps            : 407
# Proof object initial clauses used    : 87
# Proof object initial formulas used   : 41
# Proof object simplifying inferences  : 352
# Parsed axioms                        : 120
# Initial clauses in saturation        : 201
# Processed clauses                    : 4479
# ...remaining for further processing  : 2187
# Generated clauses                    : 34518
# ...of the previous two non-trivial   : 30214
# User time                : 17.835 s
```

### Sum of the zero^p series - lp spaces

for p being Real st p >= 1 holds
for rseq being Real_Sequence st ( for n being Element of NAT holds rseq . n = 0 ) holds
( rseq rto_power p is summable & (Sum (rseq rto_power p)) to_power (1 / p) = 0 )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lp_space.html#T11

E proof (gnn - gpu server) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t11_lp_space

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.e339m1q256c512/t11_lp_space
```
# Proof object clause steps            : 289
# Proof object initial clauses used    : 89
# Proof object initial formulas used   : 67
# Proof object simplifying inferences  : 177
# Parsed axioms                        : 154
# Initial clauses in saturation        : 223
# Processed clauses                    : 2147
# ...remaining for further processing  : 1346
# Generated clauses                    : 14925
# ...of the previous two non-trivial   : 13746
# User time                : 6.487 s
```


### Dynkin systems generated by intersection-closed sets are intersection-closed

for Omega being non empty set
for E being Subset-Family of Omega
for X, Y being Subset of Omega st X in generated_Dynkin_System E & Y in generated_Dynkin_System E & E is intersection_stable holds
X /\ Y in generated_Dynkin_System E

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/dynkin.html#T22

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_dynkin

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_85-query256-ctx768-w0-solo/t22_dynkin
```
# Proof object clause steps            : 81
# Proof object initial clauses used    : 35
# Proof object initial formulas used   : 22
# Proof object simplifying inferences  : 45
# Parsed axioms                        : 60
# Initial clauses in saturation        : 100
# Processed clauses                    : 1639
# ...remaining for further processing  : 739
# Generated clauses                    : 12123
# ...of the previous two non-trivial   : 11938
# User time                : 32.702 s
```

### Infinity of { k : k > n }

for n being Nat holds { k where k is Element of NAT : k > n } is infinite

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/pre_circ.html#T23

E proof (gnn) with lgb premise selection (160): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t23_pre_circ

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_243-query128-ctx512-w0-coop--160/t23_pre_circ
```
# Proof object clause steps            : 198
# Proof object initial clauses used    : 54
# Proof object initial formulas used   : 47
# Proof object simplifying inferences  : 69
# Parsed axioms                        : 161
# Initial clauses in saturation        : 256
# Processed clauses                    : 1395
# ...remaining for further processing  : 891
# Generated clauses                    : 4728
# ...of the previous two non-trivial   : 4420
# User time                : 8.126 s
```



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

### Fibonacci numbers - alternative proof (no induction needed) of  tau ^ n + tau ^ (n + 1) = tau ^ (n + 2)

for n being Nat holds (tau to_power n) + (tau to_power (n + 1)) = tau to_power (n + 2)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fib_num3.html#T9

The premise selector proposed using tau ^ 2 = tau + 1 (http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fib_num.html#E17) , from which the theorem easily follows.

E proof (blistr) with gnn premise selection (-1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t9_fib_num3

/local1/mptp/gnn_pred_train_big_knn512_all.probs_out_all/gnn_pred_train_big_knn512_all.probs.eprotokoll_atpstr_my_5fce846ef89413a220d0951fb615d42ded72b119s2__preds__-1/t9_fib_num3
```
# Proof object clause steps            : 116
# Proof object initial clauses used    : 37
# Proof object initial formulas used   : 33
# Proof object simplifying inferences  : 48
# Parsed axioms                        : 193
# Initial clauses in saturation        : 291
# Processed clauses                    : 8013
# ...remaining for further processing  : 3294
# Generated clauses                    : 44110
# ...of the previous two non-trivial   : 37945
# User time                : 1.175 s
```

### Fibonacci numbers - much simpler alternative proof of the (probably over-simplified) Mizar version of Carmichael's theorem

for m being Nat
for n being non empty Nat st m is prime & n is prime & m divides Fib n holds
for r being Nat st r < n & r <> 0 holds
not m divides Fib r

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fib_num2.html#T69

The original Mizar proof has 122 lines, uses induction and we cannot so far replay it. However much simpler proof was found from different 32 premises, probably due to incorrect oversimplification of the Mizar version of the theorem. It goes via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fib_num.html#T5 which says that (Fib m) gcd (Fib n) = Fib (m gcd n) . Since n is prime and r < n, n gcd r = 1 and thus (Fib n) gcd (Fib r) = 1 and m cannot divide Fib r .

E proof (blistr) with knn premise selection (128): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t69_fib_num2

/local1/mptp/miz60-cek-out/train-n.5knn.2-probs_out/train-n.5knn.2.eprotokoll_atpstr_my_fdfa75aeb82cfb954998cf278fcefc11586a3a4bs2__preds__128/t69_fib_num2
```
# Proof object clause steps            : 159
# Proof object initial clauses used    : 45
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 67
# Parsed axioms                        : 129
# Initial clauses in saturation        : 229
# Processed clauses                    : 4911
# ...remaining for further processing  : 4214
# Generated clauses                    : 83196
# ...of the previous two non-trivial   : 82332
# User time                : 1.399 s
```


### Fibonacci and Lucas numbers

Fib (2 * n) = (Fib n) * (Lucas n)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/fib_num3.html#T28

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_fib_num3

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query256-ctx768-w0-coop/t28_fib_num3
```
# Proof object clause steps            : 85
# Proof object initial clauses used    : 42
# Proof object initial formulas used   : 40
# Proof object simplifying inferences  : 56
# Parsed axioms                        : 191
# Initial clauses in saturation        : 218
# Processed clauses                    : 2002
# ...remaining for further processing  : 982
# Generated clauses                    : 22797
# ...of the previous two non-trivial   : 20240
# User time                : 27.958 s
```


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

### 163 is prime

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/nat_4.html#T35

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t35_nat_4

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_67-query256-ctx1024-w0-coop/t35_nat_4
```
# Proof object clause steps            : 235
# Proof object initial clauses used    : 79
# Proof object initial formulas used   : 74
# Proof object simplifying inferences  : 128
# Parsed axioms                        : 617
# Initial clauses in saturation        : 745
# Processed clauses                    : 3202
# ...remaining for further processing  : 2089
# Generated clauses                    : 15514
# ...of the previous two non-trivial   : 13074
# User time                : 37.363 s
```

826 axioms before premise selection, 74 used in the proof, 2k processed, 13k generated.

### 17 is prime  

259-long proof with a lot of computation from 1k initial axioms in 11s using 2-phase ENIGMA

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/pepin.html#T60

E proof (2-phase lgb+gnn-server) using 68 of the 1005 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t60_pepin

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.train/t60_pepin

The fast lgb model filtered out 34113 of the 52440 generated clauses (leaving the rest for the gnn server):
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c768f1711.train$ grep skipped t60_pepin | perl -ne 'm/(\d+) clauses/ or die; $n+=$1; END {print $n,"\n"}' 
34113
```

```
# Proof object clause steps            : 259
# Proof object initial clauses used    : 72
# Proof object initial formulas used   : 68
# Proof object simplifying inferences  : 153
# Parsed axioms                        : 1005
# Initial clauses in saturation        : 1131
# Processed clauses                    : 8817
# ...remaining for further processing  : 4439
# Generated clauses                    : 64129
# ...of the previous two non-trivial   : 52440
# User time                : 11.351 s
```


### Massive counting ATP-style: Enumerate all numbers smaller than 64

for x being set holds x in Seg 64 implies x = 1 or ... or x = 64

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/descip_1.html#T23

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t23_descip_1

This used premise selection - lgb, 0.005. The original bushy problem has almost 5k axioms about relations between these numbers: http://grid01.ciirc.cvut.cz/~mptp/enigma_prob/t23_descip_1 .

(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__0.005$ less t23_descip_1 
```
# Proof object clause steps            : 426
# Proof object initial clauses used    : 208
# Proof object initial formulas used   : 142
# Proof object simplifying inferences  : 522
# Parsed axioms                        : 227
# Initial clauses in saturation        : 488
# Processed clauses                    : 2329
# ...remaining for further processing  : 1574
# Generated clauses                    : 17384
# ...of the previous two non-trivial   : 16490
# User time                : 26.140 s
```

### Number theory: { a: a < m } is a complete residue system for m

395-long proof in 49s using 2-phase ENIGMA. 62-line proof in Mizar.

for m being Element of NAT holds { a where a is Element of NAT : a < m } is_CRS_of m

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/int_4.html#T48

E proof (2-phase lgb+gnn-server) using 72 of the 448 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t48_int_4

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train/t48_int_4
```
# Proof object clause steps            : 395
# Proof object initial clauses used    : 93
# Proof object initial formulas used   : 72
# Proof object simplifying inferences  : 205
# Parsed axioms                        : 448
# Initial clauses in saturation        : 697
# Processed clauses                    : 17066
# ...remaining for further processing  : 7530
# Generated clauses                    : 106868
# ...of the previous two non-trivial   : 102790
# User time                : 49.447 s
```

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

### Topology: T 1/2 is T0

for T being non empty TopSpace st T is T_1/2 holds T is T_0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topgen_4.html#T47

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t47_topgen_4

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop/t47_topgen_4
```
# Proof object clause steps            : 231
# Proof object initial clauses used    : 56
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 75
# Parsed axioms                        : 156
# Initial clauses in saturation        : 227
# Processed clauses                    : 3769
# ...remaining for further processing  : 2036
# Generated clauses                    : 26149
# ...of the previous two non-trivial   : 24945
# User time                : 101.646 s
```

55 line proof in Mizar.

### Topology - The Hausdorff condition (T_2) is preserved under homeomorphism

for M, N being non empty TopSpace st M is Hausdorff & M,N are_homeomorphic holds
N is Hausdorff

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/mfold_2.html#T10

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_mfold_2

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t10_mfold_2
```
# Proof object clause steps            : 154
# Proof object initial clauses used    : 46
# Proof object initial formulas used   : 25
# Proof object simplifying inferences  : 57
# Parsed axioms                        : 153
# Initial clauses in saturation        : 264
# Processed clauses                    : 2545
# ...remaining for further processing  : 1642
# Generated clauses                    : 11068
# ...of the previous two non-trivial   : 10305
# User time                : 31.682 s
```

### Topology: the union of finitely many compact sets is compact

for T being TopSpace
for F being finite Subset-Family of T st ( for X being Subset of T st X in F holds
X is compact ) holds
union F is compact

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topreal6.html#T20

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_topreal6

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_389-query256-ctx768-w0-coop/t20_topreal6
```
# Proof object clause steps            : 198
# Proof object initial clauses used    : 48
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 106
# Parsed axioms                        : 85
# Initial clauses in saturation        : 110
# Processed clauses                    : 2262
# ...remaining for further processing  : 1140
# Generated clauses                    : 16438
# ...of the previous two non-trivial   : 15026
# User time                : 39.156 s
```

### Topology - alternative condition on local compactness

for T being non empty TopSpace st T is regular holds
( T is locally-compact iff for x being Point of T ex Y being Subset of T st
( x in Int Y & Y is compact ) )

The proof needs to construct a nontrivial witness. The RNN-based premise selection is pretty precise (23 out of the 24 suggestions used).

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow_8.html#T28

E proof (gnn - gpu server) with rnn premise selection (trained on clusters): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_yellow_8__2

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/General_Topology.l10e49m1q128c512_rnn1cl/t28_yellow_8__2
```
# Proof object clause steps            : 160
# Proof object initial clauses used    : 45
# Proof object initial formulas used   : 23
# Proof object simplifying inferences  : 55
# Parsed axioms                        : 24
# Initial clauses in saturation        : 55
# Processed clauses                    : 4883
# ...remaining for further processing  : 1727
# Generated clauses                    : 82258
# ...of the previous two non-trivial   : 80064
# User time                : 46.567 s
```

### Topology: alternative proof of length 290 using 45 axioms about characterizations of open functions from R^m

for m being Nat
for f being Function of (TOP-REAL m),R^1 holds
 f is open iff for p being Point of (TOP-REAL m)
for r being real positive number ex s being real positive number st \].(f . p) - s,(f . p) + s.\[ c= f .: Ball (p,r) 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tops_4__4.html#T13

E proof (gnn - gpu server) with xgb premise selection (64, trained on clusters): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t13_tops_4__4

The found ATP proof goes via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tops_4.html#T6 instead of following the Mizar proof.


/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/General_Topology.l10e49m1q128c512_xgb1cl/t13_tops_4__4
```
# Proof object clause steps            : 290
# Proof object initial clauses used    : 77
# Proof object initial formulas used   : 45
# Proof object simplifying inferences  : 310
# Parsed axioms                        : 65
# Initial clauses in saturation        : 133
# Processed clauses                    : 3155
# ...remaining for further processing  : 1512
# Generated clauses                    : 10033
# ...of the previous two non-trivial   : 8630
# User time                : 7.602 s
```


### Topology - Characterization of Separated Subspaces by Weakly Separated ones.

for X being non empty TopSpace
for X1, X2 being non empty SubSpace of X holds
( X1,X2 are_separated iff ex Y1, Y2 being non empty SubSpace of X st
( Y1,Y2 are_weakly_separated & X1 is SubSpace of Y1 & X2 is SubSpace of Y2 & ( Y1 misses Y2 or Y1 meet Y2 misses X1 union X2 ) ) )

The RNN-based premise selection is pretty precise (21 out of the 21 suggestions used).

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tsep_1.html#T92

E proof (gnn - gpu server) with rnn premise selection (trained on clusters): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t92_tsep_1__3

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/General_Topology.l10e49m1q128c512_rnn1cl/t92_tsep_1__3
```
# Proof object clause steps            : 181
# Proof object initial clauses used    : 53
# Proof object initial formulas used   : 21
# Proof object simplifying inferences  : 212
# Parsed axioms                        : 21
# Initial clauses in saturation        : 73
# Processed clauses                    : 945
# ...remaining for further processing  : 591
# Generated clauses                    : 8991
# ...of the previous two non-trivial   : 8941
# User time                : 8.981 s
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

### Topology - much shorter alternative proof in second-countable spaces proposed by premise selection

for T being non empty TopSpace st T is second-countable holds
for F being Subset-Family of T st F is Cover of T & F is open holds
ex G being Subset-Family of T st
( G c= F & G is Cover of T & G is countable )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/compl_sp.html#T34

The original Mizar proof has 76 lines and many dependencies.

E proof (gnn - gpu server) with rnn premise selection (trained on clusters): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t34_compl_sp__1

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/General_Topology.l10e49m1q128c512_rnn1cl/t34_compl_sp__1
```
# Proof object clause steps            : 60
# Proof object initial clauses used    : 23
# Proof object initial formulas used   : 8
# Proof object simplifying inferences  : 30
# Parsed axioms                        : 8
# Initial clauses in saturation        : 28
# Processed clauses                    : 61
# ...remaining for further processing  : 57
# Generated clauses                    : 44
# ...of the previous two non-trivial   : 40
# User time                : 0.032 s
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

### Construct an internal point on an arc

332-long proof in 53s using 3-phase ENIGMA.

for n being Element of NAT
for P being Subset of TOP-REAL n
for p1, p2 being Point of TOP-REAL n st P is_an_arc_of p1,p2 holds
ex p3 being Point of TOP-REAL n st p3 in P & p3 <> p1 & p3 <> p2 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan6.html#T42

E proof (3-phase parental+lgb+gnn-server) using 73 of the 309 human-supplied premises (bushy): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t42_jordan6

/local1/mptp/parents/out2/2pl10r3b_e39s30q1024c1536f1711_parents_froc_gnn_m2_0.01.train/t42_jordan6
```
# Proof object clause steps            : 332
# Proof object initial clauses used    : 95
# Proof object initial formulas used   : 73
# Proof object simplifying inferences  : 139
# Parsed axioms                        : 309
# Initial clauses in saturation        : 479
# Processed clauses                    : 8236
# ...remaining for further processing  : 4806
# Generated clauses                    : 107526
# ...of the previous two non-trivial   : 36054
# User time                : 53.280 s
```


### Intermediate value theorem

for ra, rb, a, b being real number st ra < rb holds
for f being continuous Function of (Closed-Interval-TSpace (ra,rb)),R^1
for d being real number st f . ra = a & f . rb = b & a > d & d > b holds
ex rc being Element of REAL st
( f . rc = d & ra < rc & rc < rb )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topreal5.html#T7


E proof (gnn) using lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t7_topreal5

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l5-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_79-query256-ctx512-w0-coop/t7_topreal5
```
# Proof object clause steps            : 208
# Proof object initial clauses used    : 71
# Proof object initial formulas used   : 49
# Proof object simplifying inferences  : 207
# Parsed axioms                        : 108
# Initial clauses in saturation        : 151
# Processed clauses                    : 3097
# ...remaining for further processing  : 1835
# Generated clauses                    : 22073
# ...of the previous two non-trivial   : 20731
# User time                : 18.623 s
```

### Image of an upper bound of a closed interval is an upper bound of the image under a continuous bijection 

478-long proof in 38s using 2-phase ENIGMA and 4.9k nontrivial given clause loops.

for a, b, c, d being Real
for f being Function of Closed-Interval-TSpace (a,b),Closed-Interval-TSpace (c,d)
for P, Q being non empty Subset of Closed-Interval-TSpace (a,b)
for PP, QQ being Subset of R^1 st a < b & c < d & PP = P & QQ = Q & f is continuous & f is one-to-one & PP is compact & f . a = c & f . b = d & f .: P = Q holds f . (upper_bound ([#] PP)) = upper_bound ([#] QQ)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan5a.html#T18

E proof (2-phase lgb+gnn-server) using 73 of the 450 human-supplied premises (bushy):
http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t18_jordan5a

Fast lgb filtering:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep skipped t18_jordan5a | perl -ne 'm/(\d+) clauses/ or die; $n+=$1;$c++; END {print "$c,$n\n"}'
77,54180
```

GNN gpu-server evaluations:
```
(base) mptp@air-02:~/big2/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train$ grep Sendin t18_jordan5a | perl -ne 'm/query=(\d+)/ or die; $c++; $n+=$1; END {print "$c,$n\n"}'
77,28753
```

/local1/mptp/parents/out2/2pb30.1_l10r3b_e39s60q1024c1536f1711.train/t18_jordan5a
```
# Proof object clause steps            : 478
# Proof object initial clauses used    : 109
# Proof object initial formulas used   : 73
# Proof object simplifying inferences  : 340
# Parsed axioms                        : 450
# Initial clauses in saturation        : 750
# Processed clauses                    : 8516
# ...remaining for further processing  : 4877
# Generated clauses                    : 85596
# ...of the previous two non-trivial   : 82183
# User time                : 38.360 s
```



### X is locally connected iff components of open sets are open

for X being non empty TopSpace holds
X is locally_connected iff for A being non empty Subset of X
for B being Subset of X st A is open & B is_a_component_of A holds
B is open 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/connsp_2.html#T18

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t18_connsp_2

Done with premise selection - lgb 0.005

(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__0.005$ less t18_connsp_2
```
# Proof object clause steps            : 110
# Proof object initial clauses used    : 52
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 103
# Parsed axioms                        : 96
# Initial clauses in saturation        : 161
# Processed clauses                    : 1177
# ...remaining for further processing  : 802
# Generated clauses                    : 5814
# ...of the previous two non-trivial   : 5425
# User time                : 18.408 s
```

### Real plane: Simple closed curves are pathwise connected

for T being SubSpace of TOP-REAL 2 st the carrier of T is Simple_closed_curve holds
T is pathwise_connected

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topalg_3.html#T10

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_topalg_3

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_85-query512-ctx1024-w0-coop/t10_topalg_3
```
# Proof object clause steps            : 146
# Proof object initial clauses used    : 68
# Proof object initial formulas used   : 48
# Proof object simplifying inferences  : 143
# Parsed axioms                        : 147
# Initial clauses in saturation        : 246
# Processed clauses                    : 2403
# ...remaining for further processing  : 1501
# Generated clauses                    : 13198
# ...of the previous two non-trivial   : 12471
# User time                : 33.870 s
```

### Real plane: order of points

for p1, p2, p3, p4 being Point of (TOP-REAL 2)
for P being non empty compact Subset of (TOP-REAL 2)
for f being Function of (TOP-REAL 2),(TOP-REAL 2) st P = circle (0,0,1) & f = Sq_Circ holds
( p1,p2,p3,p4 are_in_this_order_on rectangle ((- 1),1,(- 1),1) iff f . p1,f . p2,f . p3,f . p4 are_in_this_order_on P )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jgraph_6.html#T78

E proof (gnn - gpu server) with premise selection (subproblem minimized): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t78_jgraph_6

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub3.l10e49m1q512c1024/t78_jgraph_6
```
# Proof object clause steps            : 474
# Proof object initial clauses used    : 58
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 821
# Parsed axioms                        : 42
# Initial clauses in saturation        : 108
# Processed clauses                    : 17993
# ...remaining for further processing  : 5420
# Generated clauses                    : 41791
# ...of the previous two non-trivial   : 37773
# User time                : 32.591 s
```

### Real plane: Extremality in cells - 250-line long proof in Mizar, 415 ATP steps from 31 premises

for i, j being Element of NAT
for G being Go-board
for p being Point of (TOP-REAL 2) st 1 <= i & i + 1 <= len G & 1 <= j & j + 1 <= width G & p in Values G & p in cell (G,i,j) holds
p is_extremal_in cell (G,i,j)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan9.html#T21

E proof (mzr03) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t21_jordan9

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr03s30_minms1/t21_jordan9
```
# Proof object clause steps            : 415
# Proof object initial clauses used    : 69
# Proof object initial formulas used   : 31
# Proof object simplifying inferences  : 366
# Parsed axioms                        : 37
# Initial clauses in saturation        : 86
# Processed clauses                    : 2309
# ...remaining for further processing  : 1382
# Generated clauses                    : 6562
# ...of the previous two non-trivial   : 4855
# User time                : 0.941 s
```



### Topology: correspondence of two notions of homotopy - 420-long proof from 64 premises

for T being non empty TopStruct
for c1, c2 being with_endpoints Curve of T
for a, b being Point of T
for p1, p2 being Path of a,b st c1 = p1 & c2 = p2 & a,b are_connected holds
( c1,c2 are_homotopic iff p1,p2 are_homotopic )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/topalg_6.html#T34

E proof (gnn - gpu server trained on mimimized proofs) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t34_topalg_6

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.l10i2e132m1q128c512_minms1/t34_topalg_6
```
# Proof object clause steps            : 420
# Proof object initial clauses used    : 104
# Proof object initial formulas used   : 64
# Proof object simplifying inferences  : 394
# Parsed axioms                        : 192
# Initial clauses in saturation        : 357
# Processed clauses                    : 4993
# ...remaining for further processing  : 2851
# Generated clauses                    : 24584
# ...of the previous two non-trivial   : 21872
# User time                : 12.718 s
```



### Any two simple closed curves are homeomorphic

for S, T being being_simple_closed_curve SubSpace of TOP-REAL 2 holds S,T are_homeomorphic

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/toprealb.html#T11

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t11_toprealb

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t11_toprealb
```
# Proof object clause steps            : 231
# Proof object initial clauses used    : 59
# Proof object initial formulas used   : 41
# Proof object simplifying inferences  : 154
# Parsed axioms                        : 238
# Initial clauses in saturation        : 463
# Processed clauses                    : 2305
# ...remaining for further processing  : 1663
# Generated clauses                    : 11917
# ...of the previous two non-trivial   : 10578
# User time                : 33.921 s
```

### The union of the unbounded components of the empty set is the whole R^n

UBD ({} (TOP-REAL n)) = REAL n

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan2c.html#T36

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t36_jordan2c

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t36_jordan2c
```
# Proof object clause steps            : 176
# Proof object initial clauses used    : 53
# Proof object initial formulas used   : 44
# Proof object simplifying inferences  : 51
# Parsed axioms                        : 275
# Initial clauses in saturation        : 474
# Processed clauses                    : 3443
# ...remaining for further processing  : 2069
# Generated clauses                    : 16654
# ...of the previous two non-trivial   : 15363
# User time                : 29.805 s
```

### Characterization of open functions from R to R^m

for m being Nat
for f being Function of R^1,(TOP-REAL m) holds
( f is open iff for p being Point of R^1
for r being real positive number ex s being real positive number st Ball ((f . p),s) c= f .: ].(p - r),(p + r).[ )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tops_4.html#T14

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t14_tops_4

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t14_tops_4
```
# Proof object clause steps            : 279
# Proof object initial clauses used    : 77
# Proof object initial formulas used   : 46
# Proof object simplifying inferences  : 297
# Parsed axioms                        : 105
# Initial clauses in saturation        : 182
# Processed clauses                    : 3711
# ...remaining for further processing  : 1786
# Generated clauses                    : 14030
# ...of the previous two non-trivial   : 13538
# User time                : 53.590 s
```

### Characterization of continuous functions from R to R^m

for f being Function of R^1,(TOP-REAL m) holds
( f is continuous iff for p being Point of R^1
for r being real positive number ex s being real positive number st f .: ].(p - s),(p + s).[ c= Ball ((f . p),r) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tops_4.html#T25

E proof (gnn) with lgb premise selection (96): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t25_tops_4

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_47-query128-ctx256-w0-coop--96/t25_tops_4
```
# Proof object clause steps            : 309
# Proof object initial clauses used    : 77
# Proof object initial formulas used   : 44
# Proof object simplifying inferences  : 326
# Parsed axioms                        : 97
# Initial clauses in saturation        : 175
# Processed clauses                    : 4540
# ...remaining for further processing  : 2210
# Generated clauses                    : 13961
# ...of the previous two non-trivial   : 12761
# User time                : 52.875 s
```



### Characterization of continuous functions from R^m to R

for m being Nat
for f being Function of (TOP-REAL m),R^1 holds
( f is continuous iff for p being Point of (TOP-REAL m)
for r being real positive number ex s being real positive number st f .: (Ball (p,s)) c= ].((f . p) - r),((f . p) + r).[ )


http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/tops_4.html#T24

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t24_tops_4

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t24_tops_4
```
# Proof object clause steps            : 299
# Proof object initial clauses used    : 82
# Proof object initial formulas used   : 52
# Proof object simplifying inferences  : 299
# Parsed axioms                        : 101
# Initial clauses in saturation        : 173
# Processed clauses                    : 2722
# ...remaining for further processing  : 1478
# Generated clauses                    : 7257
# ...of the previous two non-trivial   : 6984
# User time                : 22.307 s
```

### Continuity in topology derived from a metric space

for N, M being non empty MetrSpace
for f being Function of (TopSpaceMetr N),(TopSpaceMetr M) st ( for r being real number
for u being Element of N
for u1 being Element of M st r > 0 & u1 = f . u holds
ex s being real number st
 s > 0 &  for w being Element of N
for w1 being Element of M st w1 = f . w & dist (u,w) < s holds
dist (u1,w1) < r )   holds
f is continuous

60-line proof in Mizar.

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/uniform1.html#T3

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t3_uniform1

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_57-query768-ctx1024-w0-solo/t3_uniform1
```
# Proof object clause steps            : 261
# Proof object initial clauses used    : 74
# Proof object initial formulas used   : 39
# Proof object simplifying inferences  : 184
# Parsed axioms                        : 63
# Initial clauses in saturation        : 123
# Processed clauses                    : 2212
# ...remaining for further processing  : 1236
# Generated clauses                    : 15875
# ...of the previous two non-trivial   : 15669
# User time                : 83.349 s
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

### A set in R^n is bounded iff its convex hull is bounded

for A being Subset of TOP-REAL n holds A is bounded iff conv A is bounded 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/simplex2.html#T14

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t14_simplex2

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_57-query768-ctx1024-w0-solo/t14_simplex2
```
# Proof object clause steps            : 151
# Proof object initial clauses used    : 71
# Proof object initial formulas used   : 50
# Proof object simplifying inferences  : 133
# Parsed axioms                        : 256
# Initial clauses in saturation        : 408
# Processed clauses                    : 5122
# ...remaining for further processing  : 2257
# Generated clauses                    : 25346
# ...of the previous two non-trivial   : 23418
# User time                : 46.871 s
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

### Quotient of even functions is an even function

F is even & G is even & (dom F) /\ (dom G) is symmetrical holds
F /" G is even

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/funct_8.html#T53

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t53_funct_8

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx512-w0-solo/t53_funct_8
```
# Proof object clause steps            : 137
# Proof object initial clauses used    : 44
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 205
# Parsed axioms                        : 129
# Initial clauses in saturation        : 167
# Processed clauses                    : 2831
# ...remaining for further processing  : 798
# Generated clauses                    : 12109
# ...of the previous two non-trivial   : 11516
# User time                : 37.214 s
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

### Probability: probability of (disjoint) unions - 360-long E proof

for Omega being non empty set
for Sigma being SigmaField of Omega
for P being Probability of Sigma
for FSeq being FinSequence of Sigma holds
( P . (Union FSeq) <= Sum (P * FSeq) & ( FSeq is disjoint_valued implies P . (Union FSeq) = Sum (P * FSeq) ) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/prob_3.html#T65

E proof (gnn - gpu server) with lgb premise selection (subproblem mnimized): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t65_prob_3

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub3.l10e49m1q512c1024/t65_prob_3
```
# Proof object clause steps            : 360
# Proof object initial clauses used    : 69
# Proof object initial formulas used   : 25
# Proof object simplifying inferences  : 442
# Parsed axioms                        : 31
# Initial clauses in saturation        : 107
# Processed clauses                    : 5456
# ...remaining for further processing  : 2496
# Generated clauses                    : 13829
# ...of the previous two non-trivial   : 12610
# User time                : 23.763 s
```



### Pythagorean theorem in inner product spaces

for X being RealUnitarySpace
for x, y being Point of X st x,y are_orthogonal holds
||.(x + y).|| ^2 = (||.x.|| ^2) + (||.y.|| ^2)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/bhsp_5.html#T6

E proof (lgb): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_bhsp_5.out

(base) mptp@air-03:/home/yan/1911-MIZAR40-ETF-IJCAR/00RESULTS/mizar40-all-T30/Enigma+mizar40-all-T10+mega-VHSLCAXPh2e15+lgb-t150-d80-l8000-e0.15+coop-mzr02$ less t6_bhsp_5.out 

```
# Proof object clause steps            : 181
# Proof object initial clauses used    : 51
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 210
# Parsed axioms                        : 342
# Initial clauses in saturation        : 440
# Processed clauses                    : 8804
# ...remaining for further processing  : 4119
# Generated clauses                    : 65094
# ...of the previous two non-trivial   : 60807
# User time                : 28.629 s
```

### In a unitary space you can inscribe a ball around any point inside a bigger ball

for V being RealUnitarySpace
for v, u being Point of V
for r being Real st u in Ball (v,r) holds
ex p being Real st ( p > 0 & Ball (u,p) c= Ball (v,r) )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/rusub_5.html#T35

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t35_rusub_5

used lgb premise selection with 0.005 threshold

(base) mptp@air-02:~/big2/convert_models/grid8bb1/mzr02-premsel_enigma_01_2020_T30_loop02_epoch_29-query128-ctx256-w0-coop$ less t35_rusub_5

```
# Proof object clause steps            : 58
# Proof object initial clauses used    : 35
# Proof object initial formulas used   : 18
# Proof object simplifying inferences  : 65
# Parsed axioms                        : 100
# Initial clauses in saturation        : 137
# Processed clauses                    : 883
# ...remaining for further processing  : 568
# Generated clauses                    : 4071
# ...of the previous two non-trivial   : 3786
# User time                : 18.970 s
```

Shortish proof, but previously unobtainable - needs the existential witness for p.

### The union of the sphere and the open ball is the closed ball

for r being real number
for M being MetrStruct
for p being Element of M holds (Sphere (p,r)) \/ (Ball (p,r)) = cl_Ball (p,r)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/metric_1.html#T16

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t16_metric_1

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx512-w0-solo/t16_metric_1
```
# Proof object clause steps            : 56
# Proof object initial clauses used    : 28
# Proof object initial formulas used   : 23
# Proof object simplifying inferences  : 26
# Parsed axioms                        : 130
# Initial clauses in saturation        : 184
# Processed clauses                    : 840
# ...remaining for further processing  : 491
# Generated clauses                    : 2924
# ...of the previous two non-trivial   : 2555
# User time                : 12.498 s
```

### Balls are preserved under mirroring

for X being RealNormSpace
for x being Point of X
for r being real number holds Ball ((0. X),r) = (- 1) * (Ball ((0. X),r))

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lopban_6.html#T11

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t11_lopban_6

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t11_lopban_6
```
# Proof object clause steps            : 182
# Proof object initial clauses used    : 50
# Proof object initial formulas used   : 27
# Proof object simplifying inferences  : 119
# Parsed axioms                        : 99
# Initial clauses in saturation        : 156
# Processed clauses                    : 4489
# ...remaining for further processing  : 1662
# Generated clauses                    : 21371
# ...of the previous two non-trivial   : 20273
# User time                : 57.618 s
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

### A derived sequence of n-th roots of a sequence that eventually grows above 0 is not summable

for s1, s being Real_Sequence st ( for n being Element of NAT holds s1 . n = n -root ((abs s) . n) ) & ex m being Element of NAT st
for n being Element of NAT st m <= n holds
s1 . n >= 1 holds not s is summable

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t41_series_1

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t41_series_1
```
# Proof object clause steps            : 229
# Proof object initial clauses used    : 70
# Proof object initial formulas used   : 54
# Proof object simplifying inferences  : 181
# Parsed axioms                        : 105
# Initial clauses in saturation        : 149
# Processed clauses                    : 2031
# ...remaining for further processing  : 1127
# Generated clauses                    : 8574
# ...of the previous two non-trivial   : 7925
# User time                : 22.182 s
```

### Complex sequences - alternative proof than in Mizar

for seq being Complex_Sequence st seq is absolutely_summable & Sum |.seq.| = 0 holds
for n being Element of NAT holds seq . n = 0c

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/csspace2.html#T13

The alternative ATP proof found goes instead via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/rsspace.html#T17 :

for rseq being Real_Sequence st ( for n being Element of NAT holds 0 <= rseq . n ) & rseq is summable & Sum rseq = 0 holds
for n being Element of NAT holds rseq . n = 0

E proof (gnn) with lgb premise selection (128+knn+miz): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t13_csspace2

/nfs/urbanjo3/air/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop--128k/t13_csspace2
```
# Proof object clause steps            : 96
# Proof object initial clauses used    : 33
# Proof object initial formulas used   : 24
# Proof object simplifying inferences  : 49
# Parsed axioms                        : 129
# Initial clauses in saturation        : 177
# Processed clauses                    : 625
# ...remaining for further processing  : 453
# Generated clauses                    : 1661
# ...of the previous two non-trivial   : 1488
# User time                : 8.843 s
```


### Real sequences: characterization of a lower bound - 55-line long Mizar proof

seq is bounded_below implies (r = lower_bound seq iff (for n holds r <=
  seq.n) & for s st 0<s holds ex k st seq.k < r+s )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/rinfsup1.html#T8

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t8_rinfsup1

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t8_rinfsup1
```
# Proof object clause steps            : 244
# Proof object initial clauses used    : 60
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 250
# Parsed axioms                        : 75
# Initial clauses in saturation        : 117
# Processed clauses                    : 2458
# ...remaining for further processing  : 1463
# Generated clauses                    : 10972
# ...of the previous two non-trivial   : 10477
# User time                : 30.389 s
```

### Real sequences - growth rate: Big_Omega (f + g) = Big_Omega max (f,g) - alternative proof than in Mizar

for f, g being eventually-nonnegative Real_Sequence holds Big_Omega (f + g) = Big_Omega (max (f,g))

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/asympt_0.html#T26


The alternative ATP proof found goes instead via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/asympt_0.html#T19 and http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/asympt_0.html#T9


for f, g being eventually-nonnegative Real_Sequence holds f in Big_Omega g iff g in Big_Oh f 

for f, g being eventually-nonnegative Real_Sequence holds Big_Oh (f + g) = Big_Oh (max (f,g))


E proof (gnn) with lgb premise selection (128+knn+miz): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t26_asympt_0

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop--128k/t26_asympt_0
```
# Proof object clause steps            : 82
# Proof object initial clauses used    : 33
# Proof object initial formulas used   : 13
# Proof object simplifying inferences  : 46
# Parsed axioms                        : 129
# Initial clauses in saturation        : 211
# Processed clauses                    : 483
# ...remaining for further processing  : 394
# Generated clauses                    : 1227
# ...of the previous two non-trivial   : 1128
# User time                : 13.164 s
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

### A point that is not in a closed set has a non-zero distance to it.

for A being Subset of (COMPLEX n) st not x in A & A <> {} & A is closed holds
dist (x,A) > 0

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/seq_4.html#T117

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t117_seq_4

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_35-query512-ctx768-w0-coop/t117_seq_4
```
# Proof object clause steps            : 279
# Proof object initial clauses used    : 74
# Proof object initial formulas used   : 56
# Proof object simplifying inferences  : 165
# Parsed axioms                        : 295
# Initial clauses in saturation        : 515
# Processed clauses                    : 3362
# ...remaining for further processing  : 2148
# Generated clauses                    : 12813
# ...of the previous two non-trivial   : 10954
# User time                : 22.065 s
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

### First isomorphism theorem for universal algebras

for U1, U2 being Universal_Algebra
for f being Function of U1,U2 st f is_epimorphism U1,U2 holds
HomQuot f is_isomorphism QuotUnivAlg (U1,(Cng f)),U2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/alg_1.html#T20

https://en.wikipedia.org/wiki/Isomorphism_theorems#First_isomorphism_theorem

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_alg_1

(base) mptp@grid02:~/local1/bushy_np/grid8bb1_60$ less l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_75-query128-ctx1024-w0-coop/t20_alg_1

```
# Proof object clause steps            : 171
# Proof object initial clauses used    : 82
# Proof object initial formulas used   : 47
# Proof object simplifying inferences  : 253
# Parsed axioms                        : 105
# Initial clauses in saturation        : 189
# Processed clauses                    : 1387
# ...remaining for further processing  : 981
# Generated clauses                    : 7955
# ...of the previous two non-trivial   : 7515
# User time                : 41.830 s
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

### Lattices: The image of a monotone function on a lower-bounded poset is lower-bounded

for S being non empty lower-bounded Poset
for T being non empty Poset
for f being monotone Function of S,T holds Image f is lower-bounded

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lattice8.html#T6

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t6_lattice8

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t6_lattice8
```
# Proof object clause steps            : 181
# Proof object initial clauses used    : 46
# Proof object initial formulas used   : 26
# Proof object simplifying inferences  : 146
# Parsed axioms                        : 132
# Initial clauses in saturation        : 222
# Processed clauses                    : 2041
# ...remaining for further processing  : 1081
# Generated clauses                    : 12917
# ...of the previous two non-trivial   : 11883
# User time                : 31.147 s
```


### Lattices: element is irreducible iff it is in every finite set of which it is the infimum

for L being Semilattice
for x being Element of L holds
( x is irreducible iff for A being non empty finite Subset of L st x = inf A holds
x in A )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/waybel_6.html#T11

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t11_waybel_6

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_15-query256-ctx512-w0-coop/t11_waybel_6
```
# Proof object clause steps            : 189
# Proof object initial clauses used    : 55
# Proof object initial formulas used   : 34
# Proof object simplifying inferences  : 210
# Parsed axioms                        : 85
# Initial clauses in saturation        : 164
# Processed clauses                    : 1210
# ...remaining for further processing  : 683
# Generated clauses                    : 10675
# ...of the previous two non-trivial   : 10152
# User time                : 37.125 s
```

### Products of semilattices have infima

for I being non empty set
for J being RelStr-yielding non-Empty reflexive-yielding ManySortedSet of I st ( for i being Element of I holds J . i is Semilattice ) holds product J is with_infima

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lfuzzy_0.html#T10

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_lfuzzy_0

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t10_lfuzzy_0
```
# Proof object clause steps            : 152
# Proof object initial clauses used    : 41
# Proof object initial formulas used   : 17
# Proof object simplifying inferences  : 115
# Parsed axioms                        : 101
# Initial clauses in saturation        : 190
# Processed clauses                    : 2236
# ...remaining for further processing  : 1238
# Generated clauses                    : 9417
# ...of the previous two non-trivial   : 8716
# User time                : 34.571 s
```


### Boolean posets: inclusion poset of a subset family of X is a full subrelation of the boolean poset on X - 50-line proof in Mizar

for Y being Subset-Family of X holds InclPoset Y is full SubRelStr of BoolePoset X

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/yellow_1.html#T5

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t5_yellow_1

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t5_yellow_1
```
# Proof object clause steps            : 207
# Proof object initial clauses used    : 55
# Proof object initial formulas used   : 38
# Proof object simplifying inferences  : 145
# Parsed axioms                        : 192
# Initial clauses in saturation        : 302
# Processed clauses                    : 3025
# ...remaining for further processing  : 1463
# Generated clauses                    : 15635
# ...of the previous two non-trivial   : 14276
# User time                : 49.800 s
```

### Relations: being quasi-ordered and Dickson is preserverd under iso ; 464-long ATP proof from 37 premises, 70-line Mizar proof

for R, S being RelStr st R,S are_isomorphic & R is Dickson & R is quasi_ordered holds
 S is quasi_ordered & S is Dickson 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/dickson.html#T38

E proof (mzr25) with heuristic premise selection (subproblem minimized): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t38_dickson

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub4.emzr25s30_minms1/t38_dickson
```
# Proof object clause steps            : 464
# Proof object initial clauses used    : 71
# Proof object initial formulas used   : 37
# Proof object simplifying inferences  : 382
# Parsed axioms                        : 41
# Initial clauses in saturation        : 99
# Processed clauses                    : 7519
# ...remaining for further processing  : 3715
# Generated clauses                    : 14945
# ...of the previous two non-trivial   : 14153
# User time                : 3.971 s
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

### Logic: Long inductive proof about free variables

for H being ZF-formula holds Free H c= variables_in H

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/zf_lang1.html#T151

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t151_zf_lang1

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_79-query768-ctx1536-w0-solo/t151_zf_lang1
```
# Proof object clause steps            : 552
# Proof object initial clauses used    : 117
# Proof object initial formulas used   : 26
# Proof object simplifying inferences  : 445
# Parsed axioms                        : 174
# Initial clauses in saturation        : 294
# Processed clauses                    : 2596
# ...remaining for further processing  : 1328
# Generated clauses                    : 17824
# ...of the previous two non-trivial   : 17302
# User time                : 57.532 s
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

### Graph algorithms: lexicografic breadth-first search labels the whole graph

for G being finite \_Graph holds (LexBFS:CSeq G) .Lifespan() = G .order()

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/lexbfs.html#T37

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t37_lexbfs

Used premise selection with lgb (0.005).

(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__0.005$ less t37_lexbfs 
```
# Proof object clause steps            : 120
# Proof object initial clauses used    : 53
# Proof object initial formulas used   : 41
# Proof object simplifying inferences  : 139
# Parsed axioms                        : 272
# Initial clauses in saturation        : 360
# Processed clauses                    : 2497
# ...remaining for further processing  : 1470
# Generated clauses                    : 11798
# ...of the previous two non-trivial   : 10553
# User time                : 27.340 s
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

### Orthogonal spaces: translational is satisfying_des - alternative proof 

for X being OrtAfPl st Af X is translational holds X is satisfying_des

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/conmetr.html#T8

E proof (blistr) with gnn premise selection (-1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t8_conmetr

The premise selector discovered http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/translac.html#T4 as a useful lemma. We were not able to replay the original proof.

/local1/mptp/gnn_pred_train_big_knn512_all.probs_out/gnn_pred_train_big_knn512_all.probs.epar_mzt_s30__preds__-1/t8_conmetr

```
# Proof object clause steps            : 95
# Proof object initial clauses used    : 28
# Proof object initial formulas used   : 9
# Proof object simplifying inferences  : 180
# Parsed axioms                        : 149
# Initial clauses in saturation        : 73
# Processed clauses                    : 707
# ...remaining for further processing  : 694
# Generated clauses                    : 707
# ...of the previous two non-trivial   : 684
# User time                : 0.071 s
```


### Lines in Euclidean Space: Being parallel is transitive

for n being Element of NAT
for L0, L1, L2 being Element of line_of_REAL n st L0 // L1 & L1 // L2 holds
L0 // L2

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/euclidlp.html#T60

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t60_euclidlp

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t60_euclidlp
```
# Proof object clause steps            : 199
# Proof object initial clauses used    : 52
# Proof object initial formulas used   : 30
# Proof object simplifying inferences  : 99
# Parsed axioms                        : 152
# Initial clauses in saturation        : 197
# Processed clauses                    : 2683
# ...remaining for further processing  : 1812
# Generated clauses                    : 12553
# ...of the previous two non-trivial   : 12071
# User time                : 53.259 s
```

### Ordinals: If A is a limit ordinal so is B + A

for A, B being Ordinal st A <> {} & A is limit_ordinal holds
B +^ A is limit_ordinal

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ordinal3.html#T29

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t29_ordinal3

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_339-query256-ctx512-w0-coop--0.05/t29_ordinal3
```
# Proof object clause steps            : 186
# Proof object initial clauses used    : 43
# Proof object initial formulas used   : 32
# Proof object simplifying inferences  : 76
# Parsed axioms                        : 67
# Initial clauses in saturation        : 100
# Processed clauses                    : 2185
# ...remaining for further processing  : 1387
# Generated clauses                    : 34837
# ...of the previous two non-trivial   : 33257
# User time                : 49.832 s
```

### Cardinals: cofinality of omega = omega - alternative proof from 38 premises

cf omega = omega

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/card_5.html#T22

We cannot replay the original proof (using essentially induction over finite sets) yet. The alternative proof goes via theorem http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/ordinal4.html#T38 saying that the cofinality of a limit ordinal is also limit, plus the definition of omega as the smallest limit ordinal.

E proof (auto-schedule) with knn premise selection (256): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t22_card_5

/local1/mptp/miz60-cek-out/test-mix-nklg-5221-probs_out/test-mix-nklg-5221-probs.eautosm1__preds__256/t22_card_5
```
# Proof object clause steps            : 166
# Proof object initial clauses used    : 41
# Proof object initial formulas used   : 38
# Proof object simplifying inferences  : 51
# Parsed axioms                        : 257
# Initial clauses in saturation        : 451
# Processed clauses                    : 7975
# ...remaining for further processing  : 2889
# Generated clauses                    : 20662
# ...of the previous two non-trivial   : 18357
# User time                : 30.864 s
```


### Cardinal arithmetics - exp (M+N) = exp M * exp N

for K, M, N being Cardinal holds exp (K,(M +\` N)) = (exp (K,M)) \*\` (exp (K,N))

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/card_2.html#T28

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t28_card_2

This used premise selection with lgb - 192 premises. The proof (and search) seems short now, but was not found by any other method before.

(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__192$ exprf.pl t28_card_2
```
# Proof object clause steps            : 47
# Proof object initial clauses used    : 19
# Proof object initial formulas used   : 14
# Proof object simplifying inferences  : 25
# Parsed axioms                        : 193
# Initial clauses in saturation        : 274
# Processed clauses                    : 770
# ...remaining for further processing  : 527
# Generated clauses                    : 10703
# ...of the previous two non-trivial   : 9585
# User time                : 10.484 s
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

### Cardinals and (ultra)filters: Filters that extend the Frechet Filter contain only sets of the same cardinality.

for X being infinite set
for F being Filter of X st Frechet_Filter X c= F holds
F is uniform

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/card_fil.html#T20

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_card_fil

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t20_card_fil
```
# Proof object clause steps            : 103
# Proof object initial clauses used    : 29
# Proof object initial formulas used   : 25
# Proof object simplifying inferences  : 39
# Parsed axioms                        : 109
# Initial clauses in saturation        : 140
# Processed clauses                    : 1685
# ...remaining for further processing  : 925
# Generated clauses                    : 15861
# ...of the previous two non-trivial   : 14344
# User time                : 22.678 s
```

### Combinatorial consequence of regularity - alternative short proof based on a nontrivial previous lemma

for X1, X2, X3, X4, X5, X6 being set holds
not X1 in X2 or not X2 in X3 or not X3 in X4 or not X4 in X5 or not X5 in X6 or not X6 in X1 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/xregular.html#T10

The alternative ATP proof found goes instead via http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/xregular.html#T6:

for X being non empty set ex Y being set st
Y in X & ( for Y1, Y2, Y3, Y4, Y5 being set st Y1 in Y2 & Y2 in Y3 & Y3 in Y4 & Y4 in Y5 & Y5 in Y holds
Y1 misses X ) 

E proof (gnn) with lgb premise selection (0.5k1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t10_xregular

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop--0.5k1/t10_xregular
```
# Proof object clause steps            : 39
# Proof object initial clauses used    : 12
# Proof object initial formulas used   : 5
# Proof object simplifying inferences  : 7
# Parsed axioms                        : 19
# Initial clauses in saturation        : 107
# Processed clauses                    : 323
# ...remaining for further processing  : 310
# Generated clauses                    : 2855
# ...of the previous two non-trivial   : 2421
# User time                : 21.116 s
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

### Groebner bases - reduction

for P being non empty Subset of (Polynom-Ring (n,L)) st PolyRedRel (P,T) is with_Church-Rosser_property holds
for f being Polynomial of n,L st f in P -Ideal holds
PolyRedRel (P,T) reduces f, 0_ (n,L)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/groeb_1.html#T15

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_groeb_1

/local1/mptp/convert_models/grid8bb1_60/l5-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_137-query256-ctx768-w0-coop/t15_groeb_1
```
# Proof object clause steps            : 308
# Proof object initial clauses used    : 99
# Proof object initial formulas used   : 43
# Proof object simplifying inferences  : 360
# Parsed axioms                        : 150
# Initial clauses in saturation        : 339
# Processed clauses                    : 3995
# ...remaining for further processing  : 2525
# Generated clauses                    : 13053
# ...of the previous two non-trivial   : 11745
# User time                : 44.274 s
```

### Groebner basis -  G is Groebner basis wrt T iff for f being non-zero Polynomial of n,L st f in G -Ideal holdsf has_a_Standard_Representation_of G,T

very long ENIGMA proof - 716 clause steps and 1725 simplifications

for n being Element of NAT
for T being connected admissible TermOrder of n
for L being non empty non degenerated right_complementable almost_left_invertible associative commutative well-unital distributive Abelian add-associative right_zeroed doubleLoopStr
for G being non empty Subset of (Polynom-Ring (n,L)) holds
( G is_Groebner_basis_wrt T iff for f being non-zero Polynomial of n,L st f in G -Ideal holds
f has_a_Standard_Representation_of G,T )

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/groeb_2.html#T40

E proof (gnn - gpu server) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t40_groeb_2

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_uns2.l8oe23m1q256c1024/t40_groeb_2
```
# Proof object clause steps            : 716
# Proof object initial clauses used    : 138
# Proof object initial formulas used   : 45
# Proof object simplifying inferences  : 1725
# Parsed axioms                        : 121
# Initial clauses in saturation        : 338
# Processed clauses                    : 6265
# ...remaining for further processing  : 4080
# Generated clauses                    : 27498
# ...of the previous two non-trivial   : 26464
# User time                : 54.240 s
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

### Matrices: The determinant of an empty matrix is 1 . 366-inference proof using 80 axioms.

for K being Field for A being Matrix of 0 ,K holds Det A = 1. K

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrixr2.html#T41

E proof (gnn-gpu60) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t41_matrixr2

/local/mptp/bushy_np/en_gnn/convert-models/gpu_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop-srv/t41_matrixr2
```
# Proof object clause steps            : 366
# Proof object initial clauses used    : 112
# Proof object initial formulas used   : 80
# Proof object simplifying inferences  : 204
# Parsed axioms                        : 256
# Initial clauses in saturation        : 417
# Processed clauses                    : 5719
# ...remaining for further processing  : 3148
# Generated clauses                    : 28834
# ...of the previous two non-trivial   : 26191
# User time                : 49.181 s
```

### Matrices: formula for computing the determinant of a 2x2 matrix - short alternative proof

for K being Field
for a, b, c, d being Element of K holds Det ((a,b) ]\[ (c,d)) = (a * d) - (b * c)

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_9.html#T13

We cannot replay the original proof yet, but an easy alternative proof was found by combining previous theorems http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_7.html#T12 and http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_2.html#T6 .

E proof (blistr) with gnn premise selection (1): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t13_matrix_9

/local1/mptp/gnn_pred_train_big_knn512_all.probs_out_all/gnn_pred_train_big_knn512_all.probs.emzr02s2__preds__1/t13_matrix_9
```
# Proof object clause steps            : 66
# Proof object initial clauses used    : 27
# Proof object initial formulas used   : 8
# Proof object simplifying inferences  : 22
# Parsed axioms                        : 47
# Initial clauses in saturation        : 94
# Processed clauses                    : 226
# ...remaining for further processing  : 180
# Generated clauses                    : 1367
# ...of the previous two non-trivial   : 1320
# User time                : 0.191 s
```



### Matrices: a linear transformation given by an n x m matrix M is onto iff the rank of M is m  (552-long ATP proof using 80 premises)

for n, m being Nat
for M being Matrix of n,m,F_Real holds
Mx2Tran M is onto iff the_rank_of M = m 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrtop1.html#T41

E proof (mzr16) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t41_matrtop1

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub5.emzr16s30_minms1/t41_matrtop1
```
# Proof object clause steps            : 552
# Proof object initial clauses used    : 135
# Proof object initial formulas used   : 80
# Proof object simplifying inferences  : 1081
# Parsed axioms                        : 99
# Initial clauses in saturation        : 191
# Processed clauses                    : 18477
# ...remaining for further processing  : 8294
# Generated clauses                    : 32997
# ...of the previous two non-trivial   : 33139
# User time                : 13.292 s
```

### Matrices: The shape of rotation matrices in R^1 (444-long ATP proof from 80 premises)

for n being Nat
for p, q being Point of (TOP-REAL n) st n = 1 & |.p.| = |.q.| holds
ex f being additive homogeneous Function of TOP-REAL n,TOP-REAL n st
 f is rotation & f . p = q & ( AutMt f = AxialSymmetry (n,n) or AutMt f = 1. (F_Real,n) ) 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrtop3.html#T40

E proof (mzr03) with heuristic premise selection (subproblem minimization): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t40_matrtop3

/local1/mptp/convert_models/gpu_cl1_60s_tl1_fc_jjfix/All_minsub5.emzr03s30_minms1/t40_matrtop3
```
# Proof object clause steps            : 444
# Proof object initial clauses used    : 104
# Proof object initial formulas used   : 80
# Proof object simplifying inferences  : 355
# Parsed axioms                        : 122
# Initial clauses in saturation        : 206
# Processed clauses                    : 36782
# ...remaining for further processing  : 14567
# Generated clauses                    : 50921
# ...of the previous two non-trivial   : 45617
# User time                : 16.123 s
```


### Matrices: explicit form for a square 3-matrix - 158-line proof in Mizar

for A being Matrix of 3,D holds A = <*<*(A * (1,1)),(A * (1,2)),(A * (1,3))*>,<*(A * (2,1)),(A * (2,2)),(A * (2,3))*>,<*(A * (3,1)),(A * (3,2)),(A * (3,3))*>*>

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrixr2.html#T37

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t37_matrixr2

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_15-query256-ctx512-w0-coop/t37_matrixr2
```
# Proof object clause steps            : 273
# Proof object initial clauses used    : 54
# Proof object initial formulas used   : 37
# Proof object simplifying inferences  : 254
# Parsed axioms                        : 117
# Initial clauses in saturation        : 172
# Processed clauses                    : 2761
# ...remaining for further processing  : 1523
# Generated clauses                    : 10779
# ...of the previous two non-trivial   : 9069
# User time                : 44.426 s
```

### Matrices: A 1-dimensional square matrix is its own transposition

for D being non empty set
for x being Element of D holds <\*<\*x\*>\*> = <\*<\*x\*>\*> @

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrlin.html#T15

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t15_matrlin

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_55-query512-ctx768-w0-coop/t15_matrlin
```
# Proof object clause steps            : 234
# Proof object initial clauses used    : 60
# Proof object initial formulas used   : 47
# Proof object simplifying inferences  : 134
# Parsed axioms                        : 156
# Initial clauses in saturation        : 263
# Processed clauses                    : 2636
# ...remaining for further processing  : 1507
# Generated clauses                    : 13998
# ...of the previous two non-trivial   : 13003
# User time                : 36.119 s
```

### Matrices: a constant square matrix is it own transposition

for n being Nat
for K being Field
for a being Element of K holds ((n,n) --> a) @ = (n,n) --> a

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_6.html#T20

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_matrix_6

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_69-query128-ctx256-w0-coop/t20_matrix_6
```
# Proof object clause steps            : 193
# Proof object initial clauses used    : 35
# Proof object initial formulas used   : 20
# Proof object simplifying inferences  : 55
# Parsed axioms                        : 82
# Initial clauses in saturation        : 136
# Processed clauses                    : 3393
# ...remaining for further processing  : 1652
# Generated clauses                    : 20201
# ...of the previous two non-trivial   : 19621
# User time                : 58.337 s
```

### Matrices and theri permutations

for K being Field
for a, b, c, d, e, f, g, h, i being Element of K
for M being Matrix of 3,K st M = <*<*a,b,c*>,<*d,e,f*>,<*g,h,i*>*> holds
for p being Element of Permutations 3 st p = <*1,2,3*> holds
Path_matrix (p,M) = <*a,e,i*>

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix_9.html#T20

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t20_matrix_9

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_389-query256-ctx768-w0-coop/t20_matrix_9
```
# Proof object clause steps            : 326
# Proof object initial clauses used    : 86
# Proof object initial formulas used   : 47
# Proof object simplifying inferences  : 323
# Parsed axioms                        : 135
# Initial clauses in saturation        : 216
# Processed clauses                    : 3270
# ...remaining for further processing  : 1603
# Generated clauses                    : 18943
# ...of the previous two non-trivial   : 16718
# User time                : 51.856 s
```

### Matrices: monster proof - 210-line long in Mizar

for n being Element of NAT, i0 being Nat, A being Matrix of n,K st
1<=i0 & i0<=n & A = SwapDiagonal(K,n,i0) holds for i,j being Nat st 1<=i & i<=n
& 1<=j & j<=n holds (i0<>1 implies (i=1 & j=i0 implies A*(i,j)=1.K) & (i=i0 & j=
1 implies A*(i,j)=1.K)& (i=1 & j=1 implies A*(i,j)=0.K)& (i=i0 & j=i0 implies A
\*(i,j)=0.K)& (not ((i=1 or i=i0) &(j=1 or j=i0)) implies (i=j implies A*(i,j)=
  1.K)& (i<>j implies A*(i,j)=0.K)))

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix14.html#T43

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t43_matrix14

/local1/mptp/convert_models/grid8bb1_60/l8-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_339-query256-ctx512-w0-coop/t43_matrix14
```
# Proof object clause steps            : 422
# Proof object initial clauses used    : 89
# Proof object initial formulas used   : 45
# Proof object simplifying inferences  : 626
# Parsed axioms                        : 225
# Initial clauses in saturation        : 335
# Processed clauses                    : 4737
# ...remaining for further processing  : 2730
# Generated clauses                    : 31589
# ...of the previous two non-trivial   : 29946
# User time                : 58.137 s
```

### Matrices: longish proof about swapping lines - 64 lines in Mizar

for m, n, l, k being Nat for K being Field
for M, M1 being Matrix of n,m,K
for i being Nat st l in dom M & k in dom M & i in dom M & M1 = InterchangeLine (M,l,k) holds
( i = l implies Line (M1,i) = Line (M,k) ) & ( i = k implies Line (M1,i) = Line (M,l) ) & ( i <> l & i <> k implies Line (M1,i) = Line (M,i) ) 

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/matrix12.html#T2

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t2_matrix12

/local1/mptp/convert_models/grid8bb1_120/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_49-query128-ctx512-w0-coop/t2_matrix12
```
# Proof object clause steps            : 369
# Proof object initial clauses used    : 76
# Proof object initial formulas used   : 36
# Proof object simplifying inferences  : 378
# Parsed axioms                        : 93
# Initial clauses in saturation        : 159
# Processed clauses                    : 4155
# ...remaining for further processing  : 1961
# Generated clauses                    : 19303
# ...of the previous two non-trivial   : 18922
# User time                : 111.848 s
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

### Longish about sequences on goboard (in the proof of Jordan)

for h being non constant standard special_circular_sequence holds n_e_n h <> n_e_s h

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/jordan5d.html#T49

E proof (gnn): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t49_jordan5d

Premise selection used (lgb, 0.005)
(base) mptp@air-02:/scratch/mptp/bhardpredo1/preds__0.005$ less t49_jordan5d
```
# Proof object clause steps            : 161
# Proof object initial clauses used    : 74
# Proof object initial formulas used   : 58
# Proof object simplifying inferences  : 196
# Parsed axioms                        : 255
# Initial clauses in saturation        : 369
# Processed clauses                    : 2017
# ...remaining for further processing  : 1434
# Generated clauses                    : 6398
# ...of the previous two non-trivial   : 6038
# User time                : 17.904 s
```

### Monster proof about the length of special circular sequences - 80 lines in Mizar and 70 ATP axioms

for f being non constant standard special_circular_sequence holds len f > 4

http://grid01.ciirc.cvut.cz/~mptp/7.13.01_4.181.1147/html/goboard7.html#T34

E proof (gnn) with lgb premise selection (0.005): http://grid01.ciirc.cvut.cz/~mptp/enigma_prf/t34_goboard7

/local1/mptp/convert_models/grid8bb1_60/l10-mzr02-premsel_enigma_01_2020_T30_loop02_epoch_35-query512-ctx768-w0-coop/t34_goboard7
```
# Proof object clause steps            : 483
# Proof object initial clauses used    : 88
# Proof object initial formulas used   : 70
# Proof object simplifying inferences  : 1007
# Parsed axioms                        : 237
# Initial clauses in saturation        : 334
# Processed clauses                    : 4393
# ...remaining for further processing  : 2307
# Generated clauses                    : 34712
# ...of the previous two non-trivial   : 25672
# User time                : 52.273 s
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

