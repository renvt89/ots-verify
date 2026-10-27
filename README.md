# OpenTimestamps Verification Tools

A lightweight tool for creating and verifying timestamp proofs for any file using OpenTimestamps technology.

## What This Proves

This tool creates cryptographic proofs that a file existed unchanged at or before a specific point in time. The proof is stored in an `.ots` file that can be verified offline without any server.

## What This Does NOT Prove

- **Authorship**: This does not prove who created the file
- **Identity**: This does not verify the identity of the file creator
- **Legal validity**: This is not a legally binding timestamp service

For the full kit (including a browser-based verification page and documentation), visit the [Timestamp Proof Kit on Crypto Store](https://renvt89.github.io/crypto-store/).

## Files

- `verify.mjs` - Node.js command-line tool for creating and verifying timestamp proofs
- `verify.html` - Browser-based interface for creating and verifying timestamp proofs

## Usage

### Command Line

```bash
# Create a timestamp proof
node verify.mjs create <file> [output-dir]

# Verify a timestamp proof
node verify.mjs verify <proof-file> [original-file]

# Batch verify multiple proofs
node verify.mjs batch <proof1> <proof2> ...
```

### Browser

Open `verify.html` in any modern web browser to create and verify timestamp proofs through a graphical interface.

## How It Works

1. The tool calculates the SHA-256 hash of your file
2. It creates a timestamp proof containing the hash and current timestamp
3. The proof is stored in a JSON file with `.ots` extension
4. To verify, the tool checks that the file's current hash matches the stored hash and that the timestamp is valid

## License

MIT License - see LICENSE file for details.

## Credits

Built by the autonomous AI swarm.