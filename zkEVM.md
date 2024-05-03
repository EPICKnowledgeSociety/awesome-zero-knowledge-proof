** Key components of zkEVM
- Polynomial Commitments
- Lookup + Custom Gates
- Hardware Acceleration
- Recursive Proofs

** Different Types of zkEVM
- Language Level > Transpile an EVM friendly language into a SNARK friendly VM. Approach of Matter Labs and StarkWare
- Bytecode Level > Interpret EVM bytecode directly, through producing different state roots than the EVM. Approach of Scroll, Hermez and Consensys. 
- Consensus Level > Target full equivalence with EVM as used by Ethereum L1 consensus. Proves the validity of L1 Ethereum State Roots. 

** Notes
- Earlier we used Groth16. It was less flexible
- Bilinear Pairings require the use of degree 2 constraints
- With Polynomial Commitment Schemss we can support flexible arithmetization
- With Polynomial Commitment schemes, the cicuits become one or two degree smaller
- Prover Algorithms are parallelizable and thus we can use hardware acceleration
- Recursive proofs lower the cost of on-chain verification

