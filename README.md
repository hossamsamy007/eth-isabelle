# Formalization of Ethereum Virtual Machine in Lem

This repository contains

* a Keccak-256 implementation in Isabelle/HOL `KEC.thy` (to be ported to Lem)
* a RLP implementation (in progress) `RLP.thy`
* an EVM implementation in Lem `lem/evm.lem`
* a relational semantics that captures the callee's nondeterministic behavior `RelationalSem.thy`
* some example verified contracts in `example`
* a parser that parses hex code and emits an Isabelle/HOL expression representing the program `parser/hexparser.rb`

When you see `\<Rightarrow>` in the source, try using the [Isabelle2016](https://isabelle.in.tum.de/index.html) interface.  There you see `⇒` instead.

## Lem?

[Lem](https://www.cl.cam.ac.uk/~pes20/lem/) is a language that can be translated into Coq, Isabelle/HOL, HOL4, OCaml, HTML and LaTeX.

## Prerequisites

* [Isabelle 2016](https://isabelle.in.tum.de/installation.html)
* [lem](http://www.cl.cam.ac.uk/~pes20/lem/built-doc/lem-manual.html#installation)
* [OCaml](http://www.ocaml.org/) 4.02.3
* [opam](https://opam.ocaml.org/) 1.2.2
* yojson: use `opam install yojson`
* bignum: use `opam install bignum`
* easy-format: use `opam install easy-format`

## Makefile goals

* `make deed` produces a verified PDF document for the Deed contract in `output/document.pdf`.
* `make doc` produces `output/document.pdf` as well as `lem/*.pdf`.
* `make lem-thy` compiles the Lem sources into Isabelle/HOL
* `make lem-pdf` compiles some of the Lem sources into PDF through LaTeX
* `make all-isabelle` checks all Isabelle/HOL sources (but not the ones compiled from Lem)
* `make` does everything above

## Links

* For a bigger picture, see [overview of Yoichi's formal verification efforts on smart contracts](https://github.com/pirapira/ethereum-formal-verification-overview/blob/master/README.md#formal-verification-of-ethereum-contracts-yoichis-attempts)
* For updates, visit [a gitter channel](https://gitter.im/ethereum/formal-methods)
