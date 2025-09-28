# Activity-4---Blockchain
How to run : 
# DIDLab ERC-20 DApp

A minimal decentralized application for interacting with ERC-20 tokens on DIDLab team chains.

## 🔧 Configuration

**Team Information:**
- **Team Number**: `07`
- **RPC URL**: `https://hh-07.didlab.org`
- **Chain ID**: `31343`
- **Member Address**: `0xf39Fd6e51aad88F6F4ce6aB8827279cffFb92266`
- **Token Address**: `0x5fbdb2315678afecb367f032d93f642f64180aa3`

## 🚀 How to Run

### Prerequisites
- Modern web browser (Chrome, Firefox, Edge, Safari)
- [MetaMask](https://metamask.io/) browser extension installed

### Local Development

1. **Run locally:**
   ```bash
   # Option 1: Simple file server
   python -m http.server 8000
   # Then visit: http://localhost:8000

   # Option 2: Node.js server
   npx serve .
   # Then visit: http://localhost:3000

   # Option 3: Just open in browser
   open index.html
   ```

### Quick Start
1. Open `index.html` in your browser
2. Select your team number from the dropdown
3. Enter your deployed token contract address
4. Click **"Connect & Switch Network"** - MetaMask will prompt to add your team's chain
5. Click **"Load Token"** to fetch token metadata
6. Your balance will display automatically

## 🎯 Features

### ✅ Core Requirements
- **🔗 MetaMask Integration**: Connect wallet and auto-add custom DIDLab chain
- **🪙 Token Management**: Load ERC-20 token metadata (name, symbol, decimals)
- **💰 Balance Display**: Real-time balance checking with proper decimal formatting
- **💸 Token Transfer**: Send tokens with transaction confirmation
- **🔄 Auto-Updates**: Balance refreshes automatically on Transfer events
- **📱 MetaMask Asset**: Add token to MetaMask wallet with one click

### 🌟 Extra Features
- **💾 Persistence**: Settings saved to localStorage
- **🎨 Clean UI**: Professional dark theme with responsive design
- **⚡ Real-time Events**: Automatic balance updates using contract event watching
- **🛡️ Error Handling**: Graceful error messages for common issues
- **📊 Transaction Details**: Shows hash, block number, and gas used

## 🎮 Usage Guide

### 1. Connect to Network
```
Click "Connect & Switch Network" 
→ MetaMask prompts to add DIDLab chain
→ Approve network addition and account connection
```

### 2. Load Your Token
```
Enter token address: 0x1234...
→ Click "Load Token"
→ Displays: "MyToken (MTK), 18d, 0x1234..."
→ Shows current balance: "100.5 MTK"
```

### 3. Transfer Tokens
```
Recipient: 0x5678...
Amount: 10.5
→ Click "Send"
→ MetaMask confirms transaction
→ Shows: "Submitted: 0xabcd..." 
→ Shows: "Mined in block 12345 (gas 21000)"
```

### 4. Add to MetaMask
```
Click "Add Token to MetaMask"
→ MetaMask prompts to add token
→ Token appears in your wallet assets
```

## 🏗️ Technical Stack

- **Frontend**: Vanilla HTML/CSS/JavaScript (no build step)
- **Blockchain Library**: [Viem v2.37.5](https://viem.sh/) via CDN
- **Wallet**: MetaMask integration
- **Storage**: localStorage for persistence
- **Styling**: Custom CSS with dark theme

## 📁 Project Structure

```
didlab-erc20-dapp/
├── index.html          # Main application file
├── README.md           # This file
└── screenshots/        # Demo screenshots
    ├── connected.png
    ├── token-loaded.png
    ├── transfer-success.png
    └── metamask-asset.png
```

## 🧪 Testing Checklist

- [ ] MetaMask connects and switches to correct DIDLab chain
- [ ] Token metadata loads correctly (name/symbol/decimals)
- [ ] Balance displays in human-readable format
- [ ] Transfer succeeds and shows transaction details
- [ ] Balance auto-updates after transfer
- [ ] Token can be added to MetaMask assets
- [ ] Error handling works for invalid addresses
- [ ] Settings persist after page reload

## 🔧 Development Notes

### Chain Configuration
The app supports all 12 DIDLab teams with automatic RPC and Chain ID mapping:
- Team 07: Chain ID `31343` → `https://hh-07.didlab.org`
- Other teams: Chain ID `31337-31348` → `https://hh-XX.didlab.org`

### ERC-20 ABI
Uses minimal ABI with only required functions:
- `name()`, `symbol()`, `decimals()`
- `balanceOf(address)`
- `transfer(address,uint256)`
- `Transfer` event

### Event Watching
Automatically listens for Transfer events involving the connected account and refreshes balance in real-time.

## 🐛 Troubleshooting

**MetaMask not detected:**
- Ensure MetaMask extension is installed and enabled
- Refresh the page and try again

**Network switching fails:**
- Manually add the network in MetaMask settings
- RPC: `https://hh-07.didlab.org`, Chain ID: `31343`

**Token not loading:**
- Verify the contract address is correct
- Ensure you're connected to the right network
- Check that the contract is deployed and accessible

**Transfer fails:**
- Check you have sufficient balance
- Verify recipient address is valid
- Ensure you have ETH for gas fees

## 📄 License

MIT License - see LICENSE file for details

## 👥 Team

DIDLab Team 07

Screenshots: 
<img width="1319" height="829" alt="3" src="https://github.com/user-attachments/assets/630ae1b3-2106-4aa9-a631-0469d279a021" />
<img width="1283" height="818" alt="2" src="https://github.com/user-attachments/assets/62c31140-2364-4e09-a8ae-649ef9352577" />
<img width="1303" height="815" alt="1" src="https://github.com/user-attachments/assets/336935f7-007d-4ac0-816e-804b9139a033" />
<img width="1289" height="813" alt="4" src="https://github.com/user-attachments/assets/a514793c-07d8-4afa-8c9b-098fbae6c597" />

