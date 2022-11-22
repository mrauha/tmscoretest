# tmscoretest

Input for foldseek (the latest release, 915ef7ddc)
```
foldseek easy-search dir1 dir2 aln_testi.m8 tmp --alignment-type 1 --tmscore-threshold 0.0 --format-output query,target,alntmscore,u,t
```
and for USalign (Version 20220924)
```
USalign pdb1 pdb2 -m - -fast
```
The tmscore of the US-align results is the one normalized by the length of p2. 

``` 
p1->p2, tmscore, first three elements of rotation matrix, translation vector
Foldseek	7o6y_3->6zkp_A	0.764	[ 0.581  0.532 -0.616]	..	[ 1.107  2.321 -2.996]
Foldseek	6zkp_A->7o6y_3	0.764	[0.581 0.217 0.784]	..	[ 1.202 -3.749 -0.305]
US-align	7o6y_3->6zkp_A	0.722	[0.581 0.214 0.785]	..	[ 1.22  -3.659 -0.253]
US-align	6zkp_A->7o6y_3	0.691	[ 0.581  0.532 -0.616]	..	[ 1.082  2.234 -2.963]

Foldseek	7o6y_3->6g2j_A	-
Foldseek	6g2j_A->7o6y_3	-
US-align	7o6y_3->6g2j_A	0.805	[0.548 0.086 0.832]	..	[ 0.13  -3.173 -0.479]
US-align	6g2j_A->7o6y_3	0.792	[ 0.548  0.629 -0.551]	..	[ 1.661  2.311 -1.488]

Foldseek	6zkp_A->6g2j_A	0.819	[0.99  0.128 0.064]	..	[ 1.443 -0.76   0.138]
Foldseek	6g2j_A->6zkp_A	0.819	[ 0.99  -0.13  -0.058]	..	[-1.519  0.576 -0.199]
US-align	6zkp_A->6g2j_A	0.759	[ 0.99  -0.13  -0.058]	..	[-1.546  0.562 -0.23 ]
US-align	6g2j_A->6zkp_A	0.783	[0.99  0.128 0.064]	..	[ 1.473 -0.749  0.167]
```
