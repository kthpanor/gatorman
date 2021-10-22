# Environment

## Polarizable embedding

An SCF calculation with a polarizable environment is performed in VeloxChem with an input file of the form

```
@jobs
task: scf
@end

@method settings
basis: aug-cc-pvdz
potfile: pe.pot
@end

@molecule
charge: 0
multiplicity: 1
xyz:
...
@end
```

together with a potential file `pe.pot` of the form

```
@COORDINATES
6
AA
O   -0.9957202   0.0160415   1.2422556
H   -1.4542703  -0.5669741   1.8472817
H   -0.9377950  -0.4817912   0.4267562
O   -0.2432343  -1.0198566  -1.1953808
H    0.4367536  -0.3759433  -0.9973297
H   -0.5031835  -0.8251492  -2.0957959
@MULTIPOLES
ORDER 0
6
1      -0.67444408
2       0.33722206
3       0.33722206
4      -0.67444408
5       0.33722206
6       0.33722206
@POLARIZABILITIES
ORDER 1 1
6
1       5.73935090    0.00000000    0.00000000    5.73935090    0.00000000    5.73935090
2       2.30839051    0.00000000    0.00000000    2.30839051    0.00000000    2.30839051
3       2.30839051    0.00000000    0.00000000    2.30839051    0.00000000    2.30839051
4       5.73935090    0.00000000    0.00000000    5.73935090    0.00000000    5.73935090
5       2.30839051    0.00000000    0.00000000    2.30839051    0.00000000    2.30839051
6       2.30839051    0.00000000    0.00000000    2.30839051    0.00000000    2.30839051
EXCLISTS
6     3
1     2     3   
2     1     3   
3     1     2   
4     5     6   
5     4     6   
6     4     5   
```
