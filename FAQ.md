## Why are secure hash functions not used in zkSNARKs ?
- Classical cryptographic schemes consisted mostly of boolean operations, which makes them inefficient when evaluated inside a ZK-SNARK circuit. As an example, the Zcash circuit relied on the SHA256 hash function to create a message-authentication code to prevent malleability, for generating pseudo-random strings and for commitments. However,each invocation of SHA256 added tens of thousands of multiplication gates to ZK-SNARK circuits, making this hash the primary cost when 
 generating ZK-SNARK proofs
