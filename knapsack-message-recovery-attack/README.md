# A message recovery attack on the NTRU-HPS system in Sagemath

This is the implemention of a message recovery attack on NTRU based on the Shortest Vector Problem (SVP), that is applicable to all variants of the NTRU-HPS cryptosystem. Assuming knowledge of $k$ coefficients of the ternary plaintext $m(x) \in$ \{-1, 0, 1\} ${}^N$ or $k_1$ coefficients of $m(x)$ and $k_2$ coefficients of the unknown nonce $r(x) \in$ \{-1, 0, 1\} ${}^N$, we reduce the decryption of the message to finding a short vector in a specifically chosen lattice that encodes a modular compact knapsack instance with coefficients in \{-1,0,1\}. 


### The attack
We construct a special basis using the $k$ known message coefficients and then we reduce it using the [FLATTER](https://github.com/keeganryan/flatter) reduce algorithm to get the solution of the modular compact knapsack system. This vector is essentially the nonce $r$ which is then used to reconstruct the full message $m$. 

The implementation of this attack can be found in `attack.ipynb`.

### Alternative Attack

We implement an alternative version of the previous attack, where we construct a special basis using the $k_1$ known message coefficients, we remove from the basis the columns indicated by the $k_2$ known coeffcients of $r$ and then we reduce it with [FLATTER](https://github.com/keeganryan/flatter) to get the solution of the system. We add the $k_2$ known coefficients of r(x) in the solution vector. This vector is again the nonce $r$ which is then used to reconstruct the full message $m$. 

The implementation of this attack can be found in `attack_-101.ipynb`.

`attack_0.ipynb` and `attack_01.ipynb` hold variations of the alternative attack, where only coefficients with value $0$ in the first case, and $0$ or $1$ in the second case, are inside the known coefficient list. 


## Authors

* E. Poimenidou (epoimeni@csd.auth.gr)
* K. A. Draziotis (drazioti@gmail.com)

## License

This project is licensed under the GPLv2 License
