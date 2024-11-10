## Study Notes on zkVMs

### Difference between zkSNARKs and zkSTARks
- SNARKs require at least one interaction between prover and verifier
- STARK requires no interaction between prover and verifier
- All STARks can be considered as a special type of SNARKs
- However not all SNARKs are STARKs

### Main Components of a zkVM and their functions
- Compiler : Converts ordinary programs written in high level language into VM readable code
- VM : Executed the compiled program as a machine code, without revealing any information about the program and the execution trace
- Prover: Converts the execution trace into zero knowledge proofs and shrinks the output into a few KBs as SNARK or STARK proof
- Verifier: (Not part of the zkVM) Verifies the encrypted results of the executed program using a proof

### zkVM Implementations and their components
- StarkNet : Proof System (STARK), ISA(Cairo), Compiler(Proprietry), Programming Language(Cairo)
- Lita: Proof System(STARK), ISA(Valida), Compiler(LLVM), Programming Language(C,C++, Rust, Solidity)
- Risc Zero: Proof System(STARK), ISA(RISC-V), 
- Succinct Labs: Proof System(STARK), ISA(RISC-V/Valida), 
- Nexus: Proof System(STARK), ISA(NVM), 
- Polygon Miden: Proof System(STARK), ISA(Miden)

