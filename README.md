# phd-attacks

This repository contains the code developed throughout my PhD research.

This repository serves as a central collection of the implementations, experiments and computational tools developed as part of my doctoral work.

# Attacks

### Message Recovery Attack in NTRU using VFK lattices
In this attack, we use a reduction from the NTRU-lattice to a Voronoi First Kind (VFK) lattice, enabling the use of a polynomial Closest Vector Problem (CVP) exact algorithm that is necessary for successful message recovery. We consider three use cases for our attack, each one based on a specific hypothesis concerning knowledge of some bits of the polynomial $u(x)=-kh(x)\star r(x)$, for some integer $k$.

### Enhancement Attack
An enhancement of one of the use cases of NTRU-VFK attack, where we calculate the target vector differently and we solve CVP without the use of VFK lattices. There, we get similar results to the VFK reduction, but we get the results much faster.

### Knapsack Message Recovery Attack
In the second attack, we have a practical Shortest Vector Problem (SVP) message-recovery attack on NTRU-HPS under partial plaintext leakage. Assuming that a random subset of the coefficients of both the message $m$ and/or the ephemeral key $r$ are known, we construct a linear system of modular equations whose underlying structure corresponds to a modular knapsack problem. We then, reduce this problem to an instance of the SVP on a suitably defined lattice and we solve the modular knapsack instance, successfully recovering the message $m$.


# Published Papers

### Journal 1
Message Recovery Attack in NTRU through VFK Lattices, Eirini Poimenidou, Marios Adamoudis, Konstantinos A. Draziotis and Kostas Tsichlas, Acta Informatica, vol. 63, 2026, Springer, doi: https://doi.org/10.1007/s00236-025-00512-z
### Journal 2
Message recovery attack in NTRU via knapsack, Eirini Poimenidou and Konstantinos A. Draziotis, to appear in Applicable Algebra in Engineering, Communication and Computing, 2026, Springer, doi: https://doi.org/10.1007/s00200-026-00751-8
### Conference 1 
Towards Message Recovery in NTRU Encryption with Auxiliary Data, Marios Adamoudis, Konstantinos A. Draziotis and Eirini Poimenidou, Number-Theoretic Methods in Cryptology, LNCS 14966, pages 314-329, 2025, Springer Nature Switzerland, doi: https://doi.org/10.1007/978-3-031-82380-0\_11