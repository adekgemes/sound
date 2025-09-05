# Soundness CLI

A command-line interface (CLI) tool for interacting with the **Soundness Layer testnet**.  

---

## Installation  

### Prerequisite  
- Ensure you have the **Rust toolchain** installed.  

We offer two installation methods:  
1. Using **soundnessup installer** (recommended)  
2. Building from source manually  

---

###  Quick Install via `soundnessup` (Recommended)  

The **soundnessup** tool manages your Soundness CLI installation and makes updates easy.  

#### 1. Run the installer script  
```bash
curl -sSL https://raw.githubusercontent.com/soundnesslabs/soundness-layer/main/soundnessup/install | bash
```

#### 2. Update your shell environment  
After installation, update your current shell’s `PATH` to recognize the `soundnessup` command:  

```bash
# For Bash:
source ~/.bashrc

# For Zsh:
source ~/.zshenv
```

#### 3. Install the CLI  
```bash
soundnessup install
```

#### 4. Update to the latest version  
```bash
soundnessup update
```

---

## 🛠 Usage  

### Generating a Key Pair  
```bash
soundness-cli generate-key --name my-key
```

This will:  
- Generate a new **Ed25519 key pair**  
- Store it securely in `key_store.json`  
- Display the public key in **base64 format**  

**Example output:**  
```
 Generated new key pair 'my-key'
 Public key: <base64-encoded-public-key>
```

---

### Importing a Key Pair  
If you saved your mnemonic, you can import it into `key_store.json`:  

```bash
soundness-cli import-key --name <name> --mnemonic "<mnemonic>"
```

**Example output:**  
```
 Imported key pair '<imported-key-name>'
 Public key: <base64-encoded-public-key>
```

---

### Listing Key Pairs  
To view all stored key pairs:  

```bash
soundness-cli list-keys
```

**Example output:**  
```
Available keys:
- my-key         <base64-encoded-public-key>
- imported-key   <base64-encoded-public-key>
```

---

##  Notes  
- Keys are stored locally in `key_store.json`  
- Each key is identified by its **name** and **public key**  
- Use meaningful names when generating or importing keys  

---

