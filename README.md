# Coloring Posets and Reverse Mathematics
Ph.D. thesis of Jared Corduan

# Abstract

We study two themes from Reverse Mathematics.
The first theme involves a generalization of the infinite version of
Ramsey's theorem to arbitrary partial orderings.
We say that a partial ordering P has the (n,k)-Ramsey property, and write `RT^n_k(P)`,
if for every k-coloring of the n-element chains of P there is a homogeneous copy of P.

When P is either a linear ordering or a tree, and n≥3, the statement
`(∀k≥1)RT^n_k(P)` is well understood
from the point of view of Reverse Mathematics (Jennifer Chubb, Jeffry L. Hirst, and Timothy H. McNicholl, _Reverse mathematics, computability, and partitions of trees_, J. Symbolic Logic 74 (2009), no. 1, 201–215.).
We investigate `RT^n_k(P)` for some partial orderings which are not trees.
We show that if P is either the binary tree with multiplicities
or an amenable partial ordering, and if n≥3,
then the statement `(∀k≥1)RT^n_k(P)`
is equivalent to ACA<sub>0</sub> over RCA<sub>0</sub>.
We also classify which suborderings of
the binary tree with multiplicities have the Ramsey property.
Finally, we study the (1,k)-Ramsey property for the finite (ordinal) powers of ω.
For these orderings it makes sense to consider a first-order definition
of "an isomorphic copy of ωⁿ" and the corresponding version of
`∀k RT^1_k(ωⁿ)`
which we denote by EIndec<sup>n</sup>.
We place a lower bound on the complexity of EIndec<sup>n+1</sup> by showing that it
is provable in RCA<sub>0</sub>+B∏^0_n.
Jointly with Dorais, we show that RCA<sub>0</sub>+I∑^0_{n+1} proves EIndec<sup>n</sup>
and also that RT^1_2(ω³) is equivalent to ACA<sub>0</sub> over RCA<sub>0</sub>.

The second theme of our study involves set theoretic forcing over
models of RCA<sub>0</sub> and ACA<sub>0</sub>.
Our primary focus is on notions of forcing whose conditions are
subtrees of ω<sup><ω</sup> which are ordered by inclusion and have a simple property
that we call "persistence".
In his paper "A variant of Mathias forcing that
preserves ACA<sub>0</sub>", Dorais guides the reader through an
interesting forcing construction (François Dorais, _A variant of Mathias forcing which preserves ACA<sub>0</sub>_, Archive for Mathematical Logic 51 (2012), 751–780).
We use Dorais' framework and show that persistent notions of forcing
over models of ACA<sub>0</sub> which satisfy a particular coloring property
give rise to generic extensions which also model ACA<sub>0</sub>.
We also show that a slightly less restrictive property than persistence
suffices to guarantee that generic extensions of models of RCA<sub>0</sub>
are themselves models of RCA<sub>0</sub>.
Lastly, we work through several examples:
Harrington, random, Sacks, Silver, and Miller forcing.

## Building pdf from LaTex files

### Debian/Ubuntu

TeX Live must be installed:
```bash
sudo apt-get install texlive-full
```

Then run:
```bash
pdflatex thesis.tex
bibtex thesis.aux
makeindex thesis.idx
pdflatex thesis.tex
pdflatex thesis.tex
```

### Docker

From the repository base directory, create the container:
```bash
docker build -f docker/Dockerfile -t coloring_posets .
```
Then run the container:
```bash
docker run --rm -v $PWD:/artifacts -t coloring_posets
```
