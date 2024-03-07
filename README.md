bellman-verifier 
Groth16 zkSNARK bellman proof verifier

Verify Groth16 proofs generated from bellman, using cloudflare/bn256 (used by go-ethereum) for the Pairing.

Usage
public, err := ParsePublicRaw(publicJson)
require.Nil(t, err)
proof, err := ParseProofRaw(proofJson)
require.Nil(t, err)
vk, err := ParseVkRaw(vkJson)
require.Nil(t, err)

v := Verify(vk, proof, public)
assert.True(t, v)