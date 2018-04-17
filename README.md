<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN">
<HTML lang="en">
<HEAD>
        <LINK REV="MADE" HREF="mailto:maho@riken.jp">
        <LINK REL="NEXT" HREF="index.html">
	<META HTTP-EQUIV="CONTENT-TYPE" CONTENT="text/html; charset=utf-8">
	<TITLE>THE RDM METHOD PROBLEMS IN SDPA SPARSE FORMAT</TITLE>
</HEAD>
<BODY>
<h1>THE RDM METHOD PROBLEMS IN SDPA SPARSE FORMAT</h1>
<h2>INTRODUCTION</h2>
The RDM method is promising method, using 2-RDM as a basic variable and minimize the total energy which
is a linear to the Hamiltonian with respect to so called N-representability conditions. Since N-representability condition is known
to be very hard to solve, we pose approximate N-representability conditions like P, Q, G, T1, T2 or T2'.
The total energies by this method is comprable to CCSD(T), and these SDPs are really huge, and are challenge in both mathematical programming and chemistry.<br>

<font size="5" color="#ff0000">Try them with your SDP solver!</font>
Format is the SDPA's sparse format.
You can solve problems with your SDP solver, which are available as
<a href="http://sdpa.indsys.chuo-u.ac.jp/sdpa/">SDPA, SDPA-GMP</a>,
<a href="http://sedumi.ie.lehigh.edu/">SeDuMi</a>,
<a href="http://infohost.nmt.edu/~borchers/csdp.html">CSDP</a>, and <a href="http://www.math.nus.edu.sg/~mattohkc/sdpt3.html">SDTP3</a> etc.

<h2>NOTES</h2>
All files are gzip'ed to reduce the size. For molecules' case you should add the core energy to the optimal to reproduce the results.
The rank is the twice of number of molecular orbitals and define the size of the problems. If the rank (twice # of MO)
becomes bigger, problem size becomes bigger. Not all the results of 1D hubbard model are uploaded, also I recalculated.
For the Hubbard models, you may need multiple precision version of SDP solver, like <a href="http://sdpa.indsys.chuo-u.ac.jp/sdpa/">SDPA-GMP, SDPA-QD or SDPA-DD</a>.

<h2>All data in one file</h2>
<a href="http://nakatamaho.riken.jp/rdmsdp/t2p.molecules.20170504.tar.xz">t2p.molecules.20170504.tar.xz</a>


<h2>CITATIONS (CITATION COUNT BY THE WEB OF SCIENCE)</h2>
<ul>
Problems:
<li> Variational calculation of second-order reduced density matrices by strong N-representability conditions and an accurate semidefinite programming solver
<blockquote>
Maho Nakata, Bastiaan J. Braams, Katsuki Fujisawa, Mituhiro Fukuda, Jerome K. Percus, Makoto Yamashita, and Zhengji Zhao<br>
<a href="http://link.aip.org/link/?JCPSA6/128/164113/1">Journal of chemical physics 128, 16 164113 (2008)</a> (5)<br>
DOI:10.1063/1.2911696
</blockquote>
Basics:
<li>Variational calculations of fermion second-order reduced density matrices by semidefinite programming algorithm.
<blockquote>
<em>Maho Nakata</em>, Hiroshi Nakatsuji, Masahiro Ehara, Mituhiro Fukuda, Kazuhide Nakata, and Katsuki Fujisawa<br>
<a href="http://link.aip.org/link/?jcp/114/8282">Journal of Chemical Physics, 114, 8282-8292 (2001)</a> (96)
<br>
DOI:10.1063/1.1360199
</blockquote>
</ul>

<h2>SDP PROBLEM FILES IN SDPA SPARCE FORMAT</h2>
<DIV ALIGN="CENTER"><h2>ATOMS and MOLECULES</h2></DIV>
Randomly chosen from <a href="http://link.aip.org/link/?JCPSA6/128/164113/1">Journal of chemical physics 128, 16 164113 (2008)</a>. You should add the core energy to the optimal to reproduce the paper's results.
<DIV ALIGN="CENTER">
<TABLE WIDTH="80%" BORDER=1 CELLPADDING=2 CELLSPACING=2>
<TR VALIGN=TOP>
<TD WIDTH="16%"><p>PROBLEMS (dat-s, gzip'ed) </p></TD>
<TD WIDTH="16%"><p>result (gzip'ed) </p></TD>
<TD WIDTH="16%"><p>rank</p></TD>
<TD WIDTH="16%"><p>core energy</p></TD>
<TD WIDTH="16%"><P>comment</P>
</TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqg.dat-s.gz">C.3P.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqg.result.gz">C.3P.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1.dat-s.gz">C.3P.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1.result.gz">C.3P.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1t2.dat-s.gz">C.3P.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1t2.result.gz">C.3P.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1t2p.dat-s.gz">C.3P.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="C.3P.DZ.pqgt1t2p.result.gz">C.3P.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqg.dat-s.gz">Ne.1S.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqg.result.gz">Ne.1S.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1.dat-s.gz">Ne.1S.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1.result.gz">Ne.1S.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1t2.dat-s.gz">Ne.1S.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1t2.result.gz">Ne.1S.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1t2p.dat-s.gz">Ne.1S.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="Ne.1S.DZ.pqgt1t2p.result.gz">Ne.1S.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqg.dat-s.gz">O2+.2Pig.STO6G.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqg.result.gz">O2+.2Pig.STO6G.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 3.033620918667+01 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1.dat-s.gz">O2+.2Pig.STO6G.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1.result.gz">O2+.2Pig.STO6G.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 3.033620918667e+01 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1t2.dat-s.gz">O2+.2Pig.STO6G.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1t2.result.gz">O2+.2Pig.STO6G.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 3.033620918667e+01 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1t2p.dat-s.gz">O2+.2Pig.STO6G.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="O2+.2Pig.STO6G.pqgt1t2p.result.gz">O2+.2Pig.STO6G.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 20 </P> </TD>
<TD WIDTH="16%">        <P> 3.033620918667e+01 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqg.dat-s.gz">NH.1Delta.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqg.result.gz">NH.1Delta.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 3.582091425394e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1.dat-s.gz">NH.1Delta.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1.result.gz">NH.1Delta.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 3.582091425394e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1t2.dat-s.gz">NH.1Delta.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1t2.result.gz">NH.1Delta.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 3.582091425394e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1t2p.dat-s.gz">NH.1Delta.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="NH.1Delta.DZ.pqgt1t2p.result.gz">NH.1Delta.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 3.582091425394e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqg.dat-s.gz">CH.2Pir.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqg.result.gz">CH.2Pir.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 2.835131256362e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1.dat-s.gz">CH.2Pir.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1.result.gz">CH.2Pir.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 2.835131256362e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1t2.dat-s.gz">CH.2Pir.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1t2.result.gz">CH.2Pir.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 2.835131256362e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1t2p.dat-s.gz">CH.2Pir.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="CH.2Pir.DZ.pqgt1t2p.result.gz">CH.2Pir.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 2.835131256362e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1T2' </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqg.dat-s.gz">HF.1Sigma+.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqg.result.gz">HF.1Sigma+.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 5.194757507570e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1.dat-s.gz">HF.1Sigma+.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1.result.gz">HF.1Sigma+.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 5.194757507570e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1t2.dat-s.gz">HF.1Sigma+.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1t2.result.gz">HF.1Sigma+.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 5.194757507570e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1t2p.dat-s.gz">HF.1Sigma+.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="HF.1Sigma+.DZ.pqgt1t2p.result.gz">HF.1Sigma+.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 24 </P> </TD>
<TD WIDTH="16%">        <P> 5.194757507570e+00 </P> </TD>
<TD WIDTH="16%">        <P>PQGT1T2' </P> </TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqg.dat-s.gz">F-.1S.DZ+d.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqg.result.gz">F-.1S.DZ+d.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 26 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1.dat-s.gz">F-.1S.DZ+d.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1.result.gz">F-.1S.DZ+d.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 26 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1t2.dat-s.gz">F-.1S.DZ+d.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1t2.result.gz">F-.1S.DZ+d.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 26 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1t2p.dat-s.gz">F-.1S.DZ+d.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="F-.1S.DZ+d.pqgt1t2p.result.gz">F-.1S.DZ+d.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 26 </P> </TD>
<TD WIDTH="16%">        <P> 0.0 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>

<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqg.dat-s.gz">H2O.1A1.DZ.pqg.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqg.result.gz">H2O.1A1.DZ.pqg.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 28 </P> </TD>
<TD WIDTH="16%">        <P> 9.188690490978e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQG </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1.dat-s.gz">H2O.1A1.DZ.pqgt1.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1.result.gz">H2O.1A1.DZ.pqgt1.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 28 </P> </TD>
<TD WIDTH="16%">        <P> 9.188690490978e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1t2.dat-s.gz">H2O.1A1.DZ.pqgt1t2.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1t2.result.gz">H2O.1A1.DZ.pqgt1t2.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 28 </P> </TD>
<TD WIDTH="16%">        <P> 9.188690490978e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2 </P> </TD>
</TR>
<TR VALIGN=TOP>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1t2p.dat-s.gz">H2O.1A1.DZ.pqgt1t2p.dat-s.gz</a></P> </TD>
<TD WIDTH="16%">        <P><a href="H2O.1A1.DZ.pqgt1t2p.result.gz">H2O.1A1.DZ.pqgt1t2p.result.gz</a></P> </TD>
<TD WIDTH="16%">        <P> 28 </P> </TD>
<TD WIDTH="16%">        <P> 9.188690490978e+00 </P> </TD>
<TD WIDTH="16%">        <P> PQGT1T2' </P> </TD>
</TR>


</TABLE>
</DIV>

<DIV ALIGN="CENTER"><h2>1D HUBBARD MODEL WITH HIGH CORRELATION LIMITS</h2></DIV>
From <a href="http://link.aip.org/link/?JCPSA6/128/164113/1">Journal of chemical physics 128, 16 164113 (2008)</a>. Note not all results have been uploaded, and may not all problems are solved in the referenced paper. You may need multiple precision version of SDP solver like <a href="http://sdpa.indsys.chuo-u.ac.jp/sdpa/">SDPA-GMP, SDPA-QD or SDPA-DD</a>.
<DIV ALIGN="CENTER">
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
</DIV>
</DIV>

<h2>CITATIONS (CITATION COUNT BY THE WEB OF SCIENCE)</h2>
<ul>
Problems:
<li> Variational calculation of second-order reduced density matrices by strong N-representability conditions and an accurate semidefinite programming solver
<blockquote>
Maho Nakata, Bastiaan J. Braams, Katsuki Fujisawa, Mituhiro Fukuda, Jerome K. Percus, Makoto Yamashita, and Zhengji Zhao<br>
<a href="http://link.aip.org/link/?JCPSA6/128/164113/1">Journal of chemical physics 128, 16 164113 (2008)</a> (5)<br>
DOI:10.1063/1.2911696
</blockquote>
Basics:
<li>Variational calculations of fermion second-order reduced density matrices by semidefinite programming algorithm.
<blockquote>
<em>Maho Nakata</em>, Hiroshi Nakatsuji, Masahiro Ehara, Mituhiro Fukuda, Kazuhide Nakata, and Katsuki Fujisawa<br>
<a href="http://link.aip.org/link/?jcp/114/8282">Journal of Chemical Physics, 114, 8282-8292 (2001)</a> (96)
<br>
DOI:10.1063/1.1360199
</blockquote>
</ul>

<h2>CORRESPONDANCE</h2>
Nakata, Maho: e-mail: <a href="mailto:maho@riken.jp">maho@riken.jp</a> or <a href="mailto:chat95@mac.com">chat95@mac.com</a>
<hr>
<pre>$Id: $</pre>
</BODY>
</HTML>
