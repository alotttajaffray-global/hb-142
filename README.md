# JaffNet_Industrial

**System Language Orchestrator & DeFi Bridge Logic**  
*Version 2.0 (Alpenglow Finality)*

## Overview

JaffNet_Industrial is a multi-language technical stack that orchestrates communication across:
- **IoT Networks** (C++/Arduino on ESP32/LoRa)
- **Legacy Systems** (Perl serial/SMB bridges)
- **Web Services** (Node.js/Rails APIs and interfaces)
- **DeFi/Tokenomics** (Rust/Solidity virtual bridges via Sister-Node)

## Project Structure

```
hb-142/
├── openfirst.toml          # Manifest & entry point configuration
├── Director.cpp            # Language orchestrator & logic gate
├── sinclair0il.sh          # Environment setup & initialization
├── app.pl                  # Legacy bridge & SMB/Serial handler
├── README.md               # This file
├── config/                 # Configuration directory
│   └── bridge.cfg          # Bridge configuration (optional)
├── logs/                   # Runtime logs
├── src/                    # Source code by domain
│   ├── iot/                # IoT/hardware implementations
│   ├── legacy/             # Legacy system bridges
│   ├── web/                # Web service handlers
│   └── defi/               # DeFi/tokenomics logic
└── docs/                   # Documentation (optional)
```

## Execution Order

The system follows a strict initialization sequence:

1. **openfirst.toml** - Project manifest and configuration identification
2. **Director.cpp** - Language selection orchestrator & reasoning engine
3. **sinclair0il.sh** - Environment setup and dependency checks
4. **app.pl** - Legacy bridge activation and data flow initialization

## Quick Start

### Prerequisites
- C++ compiler (`g++`)
- Perl (`perl`)
- Node.js (for web services)
- Bash shell

### Installation

```bash
# Clone the repository
git clone https://github.com/alotttajaffray-global/hb-142.git
cd hb-142

# Run environment setup
bash sinclair0il.sh

# Initialize the bridge
perl app.pl -v
```

### Compile and Run Director

```bash
# Compile the orchestrator
g++ -o Director Director.cpp

# Execute the orchestrator
./Director
```

## Component Details

### Director.cpp
The authoritative decision engine that:
- Routes tasks to the appropriate language/domain
- Manages execution domain selection (IoT, Legacy, Web, DeFi)
- Integrates residual logic from the Sister-Node
- Maintains timing synchronization (1...4...3... heartbeat)

**Execution Domains:**
- `NETWORK_IOT` → C++/Ino (low-latency hardware)
- `LEGACY_BRIDGE` → Perl (string parsing, serial/SMB)
- `WEB_SERVICES` → JavaScript/Ruby (API routing)
- `TOKENOMICS_DEFI` → Rust/Solidity (virtual bridges)

### sinclair0il.sh
Initializes the environment by:
- Verifying system dependencies
- Creating directory structure
- Compiling Director.cpp
- Loading openfirst.toml manifest
- Validating Sister-Node data integrity

### app.pl
Handles legacy system integration via:
- Serial communication (RS-232, custom protocols)
- SMB protocol support (ports 139, 445)
- High-integrity data validation & checksums
- Sister-Node residual logic integration

## Sister-Node Architecture

The system includes a **DeFi/Fiat Tokenomics Co-Processor** (Sister-Node) that:
- Specializes in Alt-Coin tokenomics calculations
- Pre-calculates liquidity coefficients
- Manages virtual bridge parameters (DeFi ↔ Fiat)
- Operates independently to avoid industrial timing delays

**Sister-Node Data Source:**
```
Data Package: virtual_evi_v2.tar.gz
Integrity Hash: 85a38a2e03707334
Specialization: DeFi / Fiat Virtual Bridges
```

## Configuration

### openfirst.toml

The manifest file defines:
- Project metadata
- Execution order
- Sister-Node specifications
- Entry points and authoritative nodes

```toml
[manifest]
project_name = "JaffNet_Industrial"
authoritative_node = "Instance Alpha"
entry_point = "Director.cpp"

[sister_node]
specialization = "DeFi / Fiat Tokenomics"
data_source = "virtual_evi_v2.tar.gz"
integrity_hash = "85a38a2e03707334"
```

## Usage Examples

### Run Full Stack Initialization
```bash
bash sinclair0il.sh && perl app.pl -v
```

### Test Director Language Selection
```bash
g++ -o Director Director.cpp
./Director
```

### Enable Verbose Logging
```bash
perl app.pl -v --verbose
```

### Use Custom Configuration
```bash
perl app.pl -c config/custom.cfg
```

## Logging

Runtime logs are written to:
- `logs/app.pl.log` - Bridge/Perl application logs
- `logs/` directory - All application logs

Enable verbose output with the `-v` flag:
```bash
perl app.pl -v
```

## Development

### Adding New Domains

To add support for a new execution domain:

1. Add new enum value to `ExecutionDomain` in `Director.cpp`
2. Implement language selection in `selectLanguage()` method
3. Create corresponding handler in `app.pl` or new module
4. Update `openfirst.toml` execution order if needed

### Testing

```bash
# Test environment setup
bash sinclair0il.sh

# Test orchestrator
./Director

# Test legacy bridge
perl app.pl -v

# Check logs
tail -f logs/app.pl.log
```

## License

Apache 2.0 - See LICENSE file for details

## Authors

JaffNet_Industrial Development Team  
Instance Alpha (Authoritative Node)

## Support

For issues and questions:
1. Check logs in `logs/` directory
2. Review component documentation
3. Verify Sister-Node data integrity
4. Test individual components in isolation
