## Study Notes on zkVMs

### Difference between zkSNARKs and zkSTARks
- SNARKs require at least one interaction between prover and verifier
- STARK requires no interaction between prover and verifier
- All STARks can be considered as a special type of SNARKs
- However not all SNARKs are STARKs

### Main Components of a zkVM and their functions
- Compiler : Converts ordinary programs written in high level language (Rust, C, C++, Solidity) into VM readable code
- VM : Executed the compiled program as a machine code, without revealing any information about the program and produces the execution trace in R1CS, PLONKish, AIR formats
- Execution Trace: A series of steps of the underlying program. It will be in a format determinned by arithmetization approach and polynomial constraints.
- Arithmetisation Approach: Groth16 - RICS, Halo2 - PLONK, PLONKY2, PLONKY3 - AIR.
- Prover: Converts the execution trace into zero knowledge proofs that satisfies the polynomial constraints and shrinks the output into a few KBs
- Proof: Collection of Polynomial Commitments, Evaluation Claims, and Opening Proofs.
- Verifier: (Not part of the zkVM) Verifies the encrypted results of the executed program using a proof

### zkVM Implementations and their components
- StarkNet : Proof System (STARK), ISA(Cairo), Compiler(Proprietry), Programming Language(Cairo)
- Lita: Proof System(STARK), ISA(Valida), Compiler(LLVM), Programming Language(C,C++, Rust, Solidity)
- Risc Zero: Proof System(STARK), ISA(RISC-V), Compiler(Rust), Programming Language (Rust)
- Succinct Labs: Proof System(STARK), ISA(RISC-V/Valida), Compiler(Rust-Precompiles), Programming Language (Rust)
- Nexus: Proof System(STARK), ISA(NVM), Compiler(Rust), Programming Language (Rust)
- Polygon Miden: Proof System(STARK), ISA(Miden), Compiler(Rust), Programming Language (Rust)

### 

