# Rust and NEAR Development Environment

This repository contains a Rust and NEAR development environment, pre-configured for use with GitHub Codespaces.

## Quick Start

Click the button below to open this project in a GitHub Codespace. If a Codespace doesn't exist, it will be created automatically:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/sushmitsarmah/near_redacted)

## What's Included

This development environment comes pre-configured with:

- Rust and Cargo
- NEAR CLI-RS
- cargo-near
- Support for WebAssembly compilation
- VS Code extensions for Rust development

## Getting Started

1. Click the "Open in GitHub Codespaces" button above.
2. Wait for the Codespace to finish setting up (this may take a few minutes).
3. Once the Codespace is ready, you can start developing!

### To Create Near Account inside codespace.

1. Codespace doesnt allow creation of account. So create near account in your local machine with the commands

```bash
near create-account <your-account-id.testnet> --useFaucet
```

2. Fetch the private key

```bash
near account export-account
```

3. Fetch the Public key

```bash
near account list-keys
```

4. In your codespace create the file and add the following and set the permissions

```bash
vim ~/.near-credentials/testnet/your-account-id.testnet.json

{
  "account_id": "your-account-id.testnet",
  "public_key": "ed25519:YOUR_PUBLIC_KEY",
  "private_key": "ed25519:YOUR_PRIVATE_KEY"
}

chmod 600 ~/.near-credentials/testnet/your-account-id.testnet.json
```

### Check your account state
near state your-account-id.testnet --networkId testnet


### set testnet as default
echo 'export NEAR_ENV=testnet' >> ~/.bashrc
source ~/.bashrc

## Customizing the Environment

If you need to customize the development environment, you can modify the `.devcontainer/devcontainer.json` file in this repository.

## Contributing

Feel free to open issues or submit pull requests if you have suggestions for improving this development environment.

## License

[Specify your license here]
