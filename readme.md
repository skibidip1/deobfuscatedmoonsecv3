# 🌙 MoonSecV3 Deobfuscator [v3.6.4]

An advanced Lua decompiler and obfuscation pattern resolver designed specifically for **MoonSec V3** obfuscation engine.  
Built for script analysis, debugging, and educational reverse engineering purposes.

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![Lua](https://img.shields.io/badge/lua-5.1%2B-blue)
![Platform](https://img.shields.io/badge/platform-Roblox%2FLua-yellow)
![Status](https://img.shields.io/badge/status-stable-green)

---

## 🔍 Overview

MoonSecV3 is known for:
- Multi-layered control-flow flattening
- Deep stack encryption
- Dynamic AST mutation
- Remote-layer bytecode loading (via encoded calls)

**MoonSecV3-Deobf** handles all of these by:
- Pattern-matching obfuscated VM stubs
- Deconstructing bytecode call proxies
- Rebuilding AST via heuristic token analyzers
- Variable name regeneration & flow flattening

---

## 📦 Features

✅ Supports:
- ✅ Control Flow Flattening Recovery  
- ✅ Anti-AST Mutation Reversal  
- ✅ Stack Resolver + Instruction Tree Dump  
- ✅ Layered Remote Bytecode Injection Reconstructor  
- ✅ Dynamic Constant Table Restoration  
- ✅ Variable Mapping & SSA Conversion

⚠️ Coming soon:
- [ ] Layer-4 detection for experimental obfuscators
- [ ] MoonSec-C hybrid branch handler
- [ ] Optional LSP support for post-analysis in VSCode

---

## 🛠 Installation

### 🔗 Git Clone:
```bash
git clone https://github.com/skibidip1/deobfuscatedmoonsecv3.git
cd moonsecv3-deobf
```

### 📜 Lua Dependencies:
```bash
luarocks install luafilesystem
luarocks install lpeg
luarocks install bit32
```

---

## 🚀 Usage

### 🧪 Basic CLI:

```bash
lua main.lua path/to/script.lua
```

### 🧠 Advanced Flags

```bash
lua main.lua -i myfile.lua -o output.lua --deep --skip-warnings --vm-rebuild
```

| Flag            | Description                                       |
|------------------|---------------------------------------------------|
| `--deep`         | Enable recursive pattern recognition              |
| `--vm-rebuild`   | Reconstruct the full Lua VM logic (slow)          |
| `--skip-warnings`| Suppress output warnings                          |
| `--debug-flow`   | Dump execution tree per block                     |
| `--auto-repair`  | Attempt control flow realignment if broken        |

---

## 📁 Project Structure

```
moonsecv3-deobf/
├── README.md
├── main.lua
├── LICENSE
├── decompiler/
│   ├── bytecode.lua
│   ├── parser.lua
│   └── reconstruct.lua
├── utils/
│   ├── tokenizer.lua
│   └── logger.lua
├── examples/
│   └── sample_obfuscated.lua
├── output/
│   └── (generated output here)
├── docs/
│   ├── advanced.md
│   └── known_issues.md
├── assets/
│   └── terminal.png
└── installer.bat
```

---

## 💻 Sample Output

Example input:
```lua
loadstring("\x47\x61\x6d\x65\x3a...")()
```

Output (`output/deobf_sample.lua`):
```lua
function hello()
    print("Hello from deobfuscated MoonSec!")
end

hello()
```

---

## ⚠ Known Limitations

- MoonSec Pro hybrid builds using dynamic proxies are **partially supported**
- Layer 4 remote AES-decrypted bytecode loading is **not yet handled**
- Runtime-based encrypted constants will remain unresolved unless `--vm-rebuild` is enabled

---

## 📚 Developer Notes

- Deobfuscation logic based on AST rebuilding
- Parser mimics standard Lua syntax but skips invalid tokens
- Bytecode interpreter internally simulates MoonSec VM opcode flow

---

## 🧪 Debug Logs

Enable debug mode:
```bash
lua main.lua input.lua --debug-flow
```

Expected log:
```
[INFO] Script loaded.
[INFO] MoonSec V3 signature found.
[INFO] Rebuilding AST...
[WARN] Found unknown bytecode stub at block #49
[INFO] Writing output to output/final.lua
```

---

## 🔒 Disclaimer

This tool is **for educational and research purposes only**.  
We do **not condone** the unauthorized use or distribution of decrypted or reverse-engineered scripts.  
By using this tool, you agree to use it within your local environment for testing and educational use.

---

## 🖼 Screenshot

![Demo Screenshot](./assets/terminal.png)

---

## 🧠 Contributors

- `@yourusername` – Core logic
- `@moonlayer` – Bytecode resolver
- `@vmhunter` – AST pathing
- `Open Source Lua Devs` ❤️

---

## 🧪 Test Scripts

```bash
lua main.lua examples/sample_obfuscated.lua --debug-flow
```

---

## 🧩 LICENSE

MIT License – See [LICENSE](LICENSE) for details.
