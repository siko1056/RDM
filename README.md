# The RDM method problems in SDPA sparse format

> This GitHub repository is a "modern" presentation of the original RDM
> library by Nakata, Maho <[maho@riken.jp](mailto:maho@riken.jp) or
> [chat95@mac.com](mailto:chat95@mac.com) hosted at
> http://nakatamaho.riken.jp/rdmsdp/sdp_rdm.html.

## Introduction

The RDM method is promising method, using 2-RDM as a basic variable and
minimize the total energy which is a linear to the Hamiltonian with respect to
so called N-representability conditions.  Since N-representability condition is
known to be very hard to solve, we pose approximate N-representability
conditions like `P`, `Q`, `G`, `T1`, `T2`, or `T2'`.  The total energies by
this method is comparable to *CCSD(T)*, and these SDPs are really huge, and are
challenge in both mathematical programming and chemistry.

**Try them with your SDP solver!** Format is the SDPA's sparse format.
You can solve problems with your SDP solver, which are available as
[SDPA, SDPA-GMP](http://sdpa.indsys.chuo-u.ac.jp/sdpa/),
[SeDuMi](http://sedumi.ie.lehigh.edu/),
[CSDP](http://infohost.nmt.edu/~borchers/csdp.html), and
[SDTP3](http://www.math.nus.edu.sg/~mattohkc/sdpt3.html) etc.

## Notes

All files are gzip'ed to reduce the size.  For molecules' case you should add
the core energy to the optimal to reproduce the results.  The rank is the twice
of number of molecular orbitals and define the size of the problems.  If the
rank (twice # of MO) becomes bigger, problem size becomes bigger.  Not all the
results of 1D hubbard model are uploaded, also I recalculated.  For the Hubbard
models, you may need multiple precision version of SDP solver, like
[SDPA-GMP, SDPA-QD, or SDPA-DD](http://sdpa.indsys.chuo-u.ac.jp/sdpa/).

## All data in one file

- [t2p.molecules.20170504.tar.xz](http://nakatamaho.riken.jp/rdmsdp/t2p.molecules.20170504.tar.xz)


## Citations (Citation count by the web of science)

- Problems: Variational calculation of second-order reduced density matrices
  by strong N-representability conditions and an accurate semidefinite
  programming solver

  > <a id="ref1"></a>
  > Maho Nakata, Bastiaan J. Braams, Katsuki Fujisawa, Mituhiro Fukuda,
  > Jerome K. Percus, Makoto Yamashita, and Zhengji Zhao. *Journal of chemical
  > physics*, **128**, 16 164113 (2008) (5)
  > [DOI: 10.1063/1.2911696](https://doi.org/10.1063/1.2911696)

- Basics: Variational calculations of fermion second-order reduced density
  matrices by semidefinite programming algorithm.

  > <a id="ref2"></a>
  > Maho Nakata, Hiroshi Nakatsuji, Masahiro Ehara, Mituhiro Fukuda,
  > Kazuhide Nakata, and Katsuki Fujisawa. *Journal of Chemical Physics*,
  > **114**, 8282-8292 (2001) (96)
  > [DOI: 10.1063/1.1360199](https://doi.org/10.1063/1.1360199)

## SDP problem files in SDPA sparse format

### Atoms and molecules

Randomly chosen from [[1]](#ref1).  You should add the core energy to the
optimal to reproduce the paper's results.

| Problems (dat-s, gzip'ed)        |        result (gzip'ed)           | rank |     core energy    | comment  |
| -------------------------------- | --------------------------------- | :--: | -----------------: | -------- |
| C.3P.DZ.pqg.dat-s.gz             | C.3P.DZ.pqg.result.gz             |  20  | 0.0                | PQG      |
| C.3P.DZ.pqgt1.dat-s.gz           | C.3P.DZ.pqgt1.result.gz           |  20  | 0.0                | PQGT1    |
| C.3P.DZ.pqgt1t2.dat-s.gz         | C.3P.DZ.pqgt1t2.result.gz         |  20  | 0.0                | PQGT1T2  |
| C.3P.DZ.pqgt1t2p.dat-s.gz        | C.3P.DZ.pqgt1t2p.result.gz        |  20  | 0.0                | PQGT1T2' |
| Ne.1S.DZ.pqg.dat-s.gz            | Ne.1S.DZ.pqg.result.gz            |  20  | 0.0                | PQG      |
| Ne.1S.DZ.pqgt1.dat-s.gz          | Ne.1S.DZ.pqgt1.result.gz          |  20  | 0.0                | PQGT1    |
| Ne.1S.DZ.pqgt1t2.dat-s.gz        | Ne.1S.DZ.pqgt1t2.result.gz        |  20  | 0.0                | PQGT1T2  |
| Ne.1S.DZ.pqgt1t2p.dat-s.gz       | Ne.1S.DZ.pqgt1t2p.result.gz       |  20  | 0.0                | PQGT1T2' |
| O2+.2Pig.STO6G.pqg.dat-s.gz      | O2+.2Pig.STO6G.pqg.result.gz      |  20  | 3.033620918667e+01 | PQG      |
| O2+.2Pig.STO6G.pqgt1.dat-s.gz    | O2+.2Pig.STO6G.pqgt1.result.gz    |  20  | 3.033620918667e+01 | PQGT1    |
| O2+.2Pig.STO6G.pqgt1t2.dat-s.gz  | O2+.2Pig.STO6G.pqgt1t2.result.gz  |  20  | 3.033620918667e+01 | PQGT1T2  |
| O2+.2Pig.STO6G.pqgt1t2p.dat-s.gz | O2+.2Pig.STO6G.pqgt1t2p.result.gz |  20  | 3.033620918667e+01 | PQGT1T2' |
| NH.1Delta.DZ.pqg.dat-s.gz        | NH.1Delta.DZ.pqg.result.gz        |  24  | 3.582091425394e+00 | PQG      |
| NH.1Delta.DZ.pqgt1.dat-s.gz      | NH.1Delta.DZ.pqgt1.result.gz      |  24  | 3.582091425394e+00 | PQGT1    |
| NH.1Delta.DZ.pqgt1t2.dat-s.gz    | NH.1Delta.DZ.pqgt1t2.result.gz    |  24  | 3.582091425394e+00 | PQGT1T2  |
| NH.1Delta.DZ.pqgt1t2p.dat-s.gz   | NH.1Delta.DZ.pqgt1t2p.result.gz   |  24  | 3.582091425394e+00 | PQGT1T2' |
| CH.2Pir.DZ.pqg.dat-s.gz          | CH.2Pir.DZ.pqg.result.gz          |  24  | 2.835131256362e+00 | PQG      |
| CH.2Pir.DZ.pqgt1.dat-s.gz        | CH.2Pir.DZ.pqgt1.result.gz        |  24  | 2.835131256362e+00 | PQGT1    |
| CH.2Pir.DZ.pqgt1t2.dat-s.gz      | CH.2Pir.DZ.pqgt1t2.result.gz      |  24  | 2.835131256362e+00 | PQGT1T2  |
| CH.2Pir.DZ.pqgt1t2p.dat-s.gz     | CH.2Pir.DZ.pqgt1t2p.result.gz     |  24  | 2.835131256362e+00 | PQGT1T2' |
| HF.1Sigma+.DZ.pqg.dat-s.gz       | HF.1Sigma+.DZ.pqg.result.gz       |  24  | 5.194757507570e+00 | PQG      |
| HF.1Sigma+.DZ.pqgt1.dat-s.gz     | HF.1Sigma+.DZ.pqgt1.result.gz     |  24  | 5.194757507570e+00 | PQGT1    |
| HF.1Sigma+.DZ.pqgt1t2.dat-s.gz   | HF.1Sigma+.DZ.pqgt1t2.result.gz   |  24  | 5.194757507570e+00 | PQGT1T2  |
| HF.1Sigma+.DZ.pqgt1t2p.dat-s.gz  | HF.1Sigma+.DZ.pqgt1t2p.result.gz  |  24  | 5.194757507570e+00 | PQGT1T2' |
| F-.1S.DZ+d.pqg.dat-s.gz          | F-.1S.DZ+d.pqg.result.gz          |  26  | 0.0                | PQG      |
| F-.1S.DZ+d.pqgt1.dat-s.gz        | F-.1S.DZ+d.pqgt1.result.gz        |  26  | 0.0                | PQGT1    |
| F-.1S.DZ+d.pqgt1t2.dat-s.gz      | F-.1S.DZ+d.pqgt1t2.result.gz      |  26  | 0.0                | PQGT1T2  |
| F-.1S.DZ+d.pqgt1t2p.dat-s.gz     | F-.1S.DZ+d.pqgt1t2p.result.gz     |  26  | 0.0                | PQGT1T2' |
| H2O.1A1.DZ.pqg.dat-s.gz          | H2O.1A1.DZ.pqg.result.gz          |  28  | 9.188690490978e+00 | PQG      |
| H2O.1A1.DZ.pqgt1.dat-s.gz        | H2O.1A1.DZ.pqgt1.result.gz        |  28  | 9.188690490978e+00 | PQGT1    |
| H2O.1A1.DZ.pqgt1t2.dat-s.gz      | H2O.1A1.DZ.pqgt1t2.result.gz      |  28  | 9.188690490978e+00 | PQGT1T2  |
| H2O.1A1.DZ.pqgt1t2p.dat-s.gz     | H2O.1A1.DZ.pqgt1t2p.result.gz     |  28  | 9.188690490978e+00 | PQGT1T2' |


### 1D Hubbard model with high correlation limits

From [[1]](#ref1).  Note not all results have been uploaded, and may not all
problems are solved in the referenced paper.  You may need multiple precision
version of SDP solver like
[SDPA-GMP, SDPA-QD, or SDPA-DD](http://sdpa.indsys.chuo-u.ac.jp/sdpa/).

<TABLE WIDTH="80%" BORDER=1 CELLPADDING=2 CELLSPACING=2>
<TR VALIGN=TOP>
<TD WIDTH="16%"><p>PROBLEMS (dat-s, gzip'ed) </p></TD>
<TD WIDTH="16%"><p>result (gzip'ed) </p></TD>
<TD WIDTH="16%"><p>rank</p></TD>
<TD WIDTH="16%"><P>U/t</P>
<TD WIDTH="16%"><P>comment</P>
</TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqg.dat-s.gz">hubbard_X4N4p.1000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqg.result.gz">hubbard_X4N4p.1000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1.dat-s.gz">hubbard_X4N4p.1000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1.result.gz">hubbard_X4N4p.1000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1t2.dat-s.gz">hubbard_X4N4p.1000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1t2.result.gz">hubbard_X4N4p.1000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1t2p.dat-s.gz">hubbard_X4N4p.1000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.1000.0.pqgt1t2p.result.gz">hubbard_X4N4p.1000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqg.dat-s.gz">hubbard_X4N4p.10000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqg.result.gz">hubbard_X4N4p.10000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1.dat-s.gz">hubbard_X4N4p.10000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1.result.gz">hubbard_X4N4p.10000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1t2.dat-s.gz">hubbard_X4N4p.10000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1t2.result.gz">hubbard_X4N4p.10000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1t2p.dat-s.gz">hubbard_X4N4p.10000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.10000.0.pqgt1t2p.result.gz">hubbard_X4N4p.10000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqg.dat-s.gz">hubbard_X4N4p.100000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqg.result.gz">hubbard_X4N4p.100000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1.dat-s.gz">hubbard_X4N4p.100000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1.result.gz">hubbard_X4N4p.100000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1t2.dat-s.gz">hubbard_X4N4p.100000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1t2.result.gz">hubbard_X4N4p.100000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1t2p.dat-s.gz">hubbard_X4N4p.100000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X4N4p.100000.0.pqgt1t2p.result.gz">hubbard_X4N4p.100000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 8 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqg.dat-s.gz">hubbard_X6N6p.1000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqg.result.gz">hubbard_X6N6p.1000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1.dat-s.gz">hubbard_X6N6p.1000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1.result.gz">hubbard_X6N6p.1000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1t2.dat-s.gz">hubbard_X6N6p.1000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1t2.result.gz">hubbard_X6N6p.1000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1t2p.dat-s.gz">hubbard_X6N6p.1000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.1000.0.pqgt1t2p.result.gz">hubbard_X6N6p.1000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqg.dat-s.gz">hubbard_X6N6p.10000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqg.result.gz">hubbard_X6N6p.10000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1.dat-s.gz">hubbard_X6N6p.10000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1.result.gz">hubbard_X6N6p.10000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1t2.dat-s.gz">hubbard_X6N6p.10000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1t2.result.gz">hubbard_X6N6p.10000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1t2p.dat-s.gz">hubbard_X6N6p.10000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.10000.0.pqgt1t2p.result.gz">hubbard_X6N6p.10000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqg.dat-s.gz">hubbard_X6N6p.100000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqg.result.gz">hubbard_X6N6p.100000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1.dat-s.gz">hubbard_X6N6p.100000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1.result.gz">hubbard_X6N6p.100000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1t2.dat-s.gz">hubbard_X6N6p.100000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1t2.result.gz">hubbard_X6N6p.100000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1t2p.dat-s.gz">hubbard_X6N6p.100000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X6N6p.100000.0.pqgt1t2p.result.gz">hubbard_X6N6p.100000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 12 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqg.dat-s.gz">hubbard_X8N8p.1000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqg.result.gz">hubbard_X8N8p.1000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1.dat-s.gz">hubbard_X8N8p.1000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1.result.gz">hubbard_X8N8p.1000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1t2.dat-s.gz">hubbard_X8N8p.1000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1t2.result.gz">hubbard_X8N8p.1000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1t2p.dat-s.gz">hubbard_X8N8p.1000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.1000.0.pqgt1t2p.result.gz">hubbard_X8N8p.1000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=1000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqg.dat-s.gz">hubbard_X8N8p.10000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqg.result.gz">hubbard_X8N8p.10000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1.dat-s.gz">hubbard_X8N8p.10000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1.result.gz">hubbard_X8N8p.10000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1t2.dat-s.gz">hubbard_X8N8p.10000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1t2.result.gz">hubbard_X8N8p.10000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1t2p.dat-s.gz">hubbard_X8N8p.10000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.10000.0.pqgt1t2p.result.gz">hubbard_X8N8p.10000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=10000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqg.dat-s.gz">hubbard_X8N8p.100000.0.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqg.result.gz">hubbard_X8N8p.100000.0.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQG</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1.dat-s.gz">hubbard_X8N8p.100000.0.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1.result.gz">hubbard_X8N8p.100000.0.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1t2.dat-s.gz">hubbard_X8N8p.100000.0.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1t2.result.gz">hubbard_X8N8p.100000.0.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2</P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1t2p.dat-s.gz">hubbard_X8N8p.100000.0.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="hubbard_X8N8p.100000.0.pqgt1t2p.result.gz">hubbard_X8N8p.100000.0.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 16 </P> </TD>
<TD WIDTH="16%">        <P> U/t=100000.0</P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2'</P> </TD>
</TR>
</TABLE>
