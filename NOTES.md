# Riot Vanguard Hardware Attestation Research

## Observed checks
- Vanguard queries TPM 2.0 for EK certificate and PCR[0-7]
- Expected PCR values match Secure Boot + Measured Boot chain
- Driver communicates via \\Device\\Vgk

## Potential bypass vectors
1. Hook TbSync.sys TPM communication
2. Emulate TPM 2.0 responses in kernel
3. Patch PCR quotes before sending to Riot servers

## References
- Microsoft TPM 2.0 Spec
- Vanguard kernel driver strings (extracted via IDA)

Educational purposes only. No exploits distributed.
