# Topological Knot Indexer

TopologicalKnotIndexer develops small, focused tools and datasets for
identifying knots and links. The primary target is distinguishing knots with
at most 11 crossings by combining diagram conversions with several knot
invariants.

Each repository is an independent checkout. Nested Git submodules are not
required. Clone only the repositories you need, or use the GitHub CLI to clone
all public organization repositories:

```bash
gh repo list TopologicalKnotIndexer --limit 100 --visibility public --json nameWithOwner \
  --jq '.[].nameWithOwner' | xargs -n1 gh repo clone
```

For the definition of planar diagram (PD) notation, see the
[Knot Atlas description](https://katlas.org/wiki/Planar_Diagrams).

## Reusable Python packages

- [link-rep](https://pypi.org/project/link-rep/) represents composite links.
- [prime-link-knot-10](https://pypi.org/project/prime-link-knot-10/) provides
  prime knots and links through 10 crossings and their compositions.
- [group-diagram-combination](https://pypi.org/project/group-diagram-combination/)
  generates compatible edge combinations for complete bipartite graphs.
- [pd-code-components](https://pypi.org/project/pd-code-components/) finds all
  components of a link from its PD code.
- [pd-code-sanity](https://pypi.org/project/pd-code-sanity/) performs lightweight
  structural validation of list-based PD codes.
- [pd-code-to-diagram](https://pypi.org/project/pd-code-to-diagram/) computes a
  planar layout for a PD code.
- [pd-code-strong-sanity](https://pypi.org/project/pd-code-strong-sanity/)
  performs stronger PD-code validation.
- [pd-code-connected-sum](https://pypi.org/project/pd-code-connected-sum/)
  constructs the connected sum of two PD codes.
- [com-link-gen-10](https://pypi.org/project/com-link-gen-10/) enumerates
  serialized composite links made from prime knots and links through 10
  crossings.
- [pd-code-delete-nugatory](https://pypi.org/project/pd-code-delete-nugatory/)
  removes nugatory crossings from knot or link PD codes.
- [pd-code-de-r1](https://pypi.org/project/pd-code-de-r1/) applies all available
  Reidemeister-I reductions.
- [pd-code-reverse-component](https://pypi.org/project/pd-code-reverse-component/)
  reverses the orientation of a selected link component.
- [pd-code-mirror](https://pypi.org/project/pd-code-mirror/) constructs the
  mirror of a knot or link PD code.
- [javakh-interface](https://pypi.org/project/javakh-interface/) calls JavaKh to
  calculate Khovanov homology from a PD code; a Java runtime is required.
- [link-khovanov](https://pypi.org/project/link-khovanov/) calculates Khovanov
  homology for all orientations of a link.

These links describe existing releases. Repository maintenance does not
publish new PyPI versions automatically.

## Datasets

Standard PD codes in these datasets are not mirrored solely according to the
sign of their writhe. The combined `hybrid_knot_indexer` pipeline performs the
required normalization when comparing invariants.

- [Composite-knot PD codes](https://github.com/TopologicalKnotIndexer/com_pd_code_list/blob/main/data/com_pd_code_list.txt)
- [Prime-link PD codes through 11 crossings](https://github.com/TopologicalKnotIndexer/link_pd_code_list/blob/main/data/pd_code_list.txt)
- [Writhes of common standard PD codes](https://github.com/TopologicalKnotIndexer/writhe_list/blob/main/data/writhe_list.txt)
- [Mirrored HOMFLY-PT polynomial registry](https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/HOMFLY-PT-reg.txt)
- [Khovanov homology registry](https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/khovanov-reg.txt)
- [Complement-volume registry](https://github.com/TopologicalKnotIndexer/conflict_lab/blob/main/volume_info_list-reg.txt)
- [Common non-hyperbolic prime-knot names](https://github.com/TopologicalKnotIndexer/non_hyperbolic_knot_list/blob/main/data/non_hyperbolic_knot_list.txt)

## Analysis

The [`conflict_lab`](https://github.com/TopologicalKnotIndexer/conflict_lab)
repository compares how well Khovanov homology, the HOMFLY-PT polynomial, and
hyperbolic volume distinguish knots with at most 11 crossings. Its report also
states the assumptions and limitations of those comparisons.

## Main applications

- [PD-code component calculator](https://ggn-2015.github.io/pd_code_cc_tool/):
  browser-based connected-component analysis.
- [`hybrid_knot_indexer`](https://github.com/TopologicalKnotIndexer/hybrid_knot_indexer):
  infers knot names from molecular coordinates by combining Khovanov homology
  and the HOMFLY-PT polynomial; requires a JDK.
- [`khovanov-indexer`](https://github.com/TopologicalKnotIndexer/khovanov-indexer):
  indexes a PD code by Khovanov homology; requires a JDK.
- [`khovanov-indexer-pipeline`](https://github.com/TopologicalKnotIndexer/khovanov-indexer-pipeline):
  converts molecular input and indexes it by Khovanov homology; requires a JDK.
- [`HOMFLY-PT-indexer`](https://github.com/TopologicalKnotIndexer/HOMFLY-PT-indexer):
  indexes a PD code by its HOMFLY-PT polynomial; requires SageMath.
- [`volume_indexer`](https://github.com/TopologicalKnotIndexer/volume_indexer):
  uses knot-complement volume and the non-hyperbolic registry; requires
  SnapPy.
- [`pd_code_to_diagram`](https://github.com/TopologicalKnotIndexer/pd_code_to_diagram):
  converts a PD code to a 3D spatial representation or 2D layout in C++.
- [`LinkRep`](https://github.com/TopologicalKnotIndexer/LinkRep): serializes and
  manipulates composite knots and links in pure Python.

## Native and specialist tools

- [`cppkh`](https://github.com/TopologicalKnotIndexer/cppkh): standalone C++14
  integer Khovanov homology engine derived from the JavaKh computation path.
- [`quick_cppkh`](https://github.com/TopologicalKnotIndexer/quick_cppkh): races
  direct `cppkh` against PD simplification followed by `cppkh`, using tracked
  ordinary dependency snapshots and no nested clones.
- [`cpp-pd-code-simplify`](https://github.com/TopologicalKnotIndexer/cpp-pd-code-simplify):
  dependency-free C++17 PD-code simplifier with a differential Python model.
- [`cpp_knot_indexer`](https://github.com/TopologicalKnotIndexer/cpp_knot_indexer):
  pure C++17 PD-code lookup using HOMFLY-PT and integral Khovanov tables.
- [`knot-indexer-lab`](https://github.com/TopologicalKnotIndexer/knot-indexer-lab):
  self-contained C++17 web server for PD-code and 3D-coordinate knot lookup.
- [`link-pd-code`](https://github.com/TopologicalKnotIndexer/link-pd-code):
  robust C++17 projection of ordered 3D link coordinates to validated PD codes.
- [`n-parallel`](https://github.com/TopologicalKnotIndexer/n-parallel): pure
  Python construction of `n` parallel diagram components; this is a parallel
  or doubling operation, not a general `(p,q)` cable constructor.
- [`pd_to_diagram`](https://github.com/TopologicalKnotIndexer/pd_to_diagram):
  experimental simulated-annealing search for routed PD-code grid layouts.
- [`khovanov-solver-legacy`](https://github.com/TopologicalKnotIndexer/khovanov-solver-legacy):
  portable reproducibility wrapper around the bundled original JavaKh v2
  classes. New native applications should prefer `cppkh`.
