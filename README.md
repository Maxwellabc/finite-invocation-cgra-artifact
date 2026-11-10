# Finite-invocation CGRA verification artifact

Source code, frozen inputs, and archived verification evidence for *Finite-Invocation Mapping and Configuration for Tokenized CGRAs*.

## Reproduce

Download `cgra_artifact_source.zip` from this repository and extract it. Enter the extracted `cgra_artifact` directory, then run with CPython 3.9 or later

```sh
python3 -I -B reproduce.py
python3 -B optional_d_mapper/verify.py
```

The first command runs six portable verification packages and preserves fresh logs in an exclusively created output directory. The second validates 1,460 pinned members and independently replays three accepted plus seventeen rejected mapper candidates. Both commands run without network access. The saved measurements have separate timing records from fresh verification.

## Included source and evidence

- Exact packet-window, tight-prefix, optional-idle, and global-fence sensitivity verification source, proofs, frozen expected results, and independent enumeration.
- Application and physical true-return checks against archived native traces, including all 39 main confirmation runs and original cost/failure ledgers.
- Deterministic mapper, polynomial router, independent legality checker, and intermediate lowerer source. Optional fresh fixed-II mapping commands are documented inside `optional_d_mapper/README.md`.
- All eleven adapted ISCAS85 graphs, the hardware contract, frozen protocol, original and successor receipts, three accepted candidates and seventeen rejected candidates.
- Deterministic PDF/SVG vector-figure scripts and plotting data. See `figures/README.md`.

The complete successor comparison accepts 3/11 graphs, versus 1/11 for original D. All 121 successor attempts remain included, with 82 UNKNOWN, three successes, eleven timeouts, seventeen illegal candidates and eight crashes. The frozen cell aggregator reports mixed-failure cells as UNKNOWN. Attempt-level results remain available. The EPFL test suite has zero development reads.

## Scope

The portable native packages verify archived traces. Rebuilding and executing the complete native simulator requires the upstream project and its pinned environment. The optional mapper entry does not implement the archived external controller's resource supervision. General source equivalence, whole-network liveness, warm restart and a complete public-mapper flow comparison remain open.

The known-reset setting elision builds on state-based redundancy elimination. The existing two-tree implementation covers terminal windows on contiguous no-idle streams. General windows and optional idle use separate scan-based verification. Static optima apply within the declared model and certified domain.

## Public dependencies and benchmarks

The hardware base is [VectorCGRA commit 8060b2b](https://github.com/tancheng/VectorCGRA/tree/8060b2b365890a1b3a056cef59b7c2ced35f024b). Placement comparisons use [SAT-MapIt commit 82c3099](https://github.com/CristianTirelli/SAT-MapIt/tree/82c30993b087fb1b836f7e5d485bcc6db04b6fe7). ISCAS85 preprocessing inputs come from the fixed [mockturtle benchmark directory](https://github.com/lsils/mockturtle/tree/420f0271ab9f63a1644bf465ab47c970c173bd7b/experiments/benchmarks). Input and preprocessing hashes are in the archive's `benchmark_manifest.json`. External projects retain their own licenses.

## Archive integrity

SHA-256 of `cgra_artifact_source.zip`

```text
6c6efe907ebd7bb2bd26228b60a1c7512f919fd11dff00fb3bf32c814094c7c7
```

The release archive was extracted independently. All six verification packages and all twenty accepted/rejected candidate replays passed. Its figure source reproduced the eight PDF/SVG assets byte for byte. The archive contains no portal credentials, author account state or private absolute paths.
