# BindForge

An AI-powered drug discovery platform that predicts and optimizes irreversible covalent inhibitors for MK2 with precision, speed, and blockchain-backed scalability.

https://github.com/user-attachments/assets/40c4266c-5430-45d4-a579-94b1a67ebfdb

## Description

BindForge is an intelligent platform that revolutionizes covalent drug design by combining AI-driven molecular docking with blockchain-powered scalability. Specializing in irreversible inhibitors for MAPKAPK2 (MK2), it enhances binding predictions, optimizes warhead chemistry, and validates cysteine-targeted covalent bonds. Using AutoDock Vina/Glide and ML-based refinement, it provides real-time feedback for in-silico molecular optimization before lab synthesis. Built on Solana's Eliza framework, BindForge ensures secure, auditable, and high-throughput simulations—accelerating NeuraViva's R&D pipeline. From predictive modeling to blockchain-backed drug discovery, BindForge bridges computational precision and pharmaceutical innovation, delivering faster, smarter covalent therapies.

## Key Features

- **AI-Augmented Covalent Docking**: Precision targeting of specific cysteine residues
- **Cysteine Warhead Optimization**: Smart selection and design of reactive groups
- **Real-Time In-Silico Feedback**: Immediate guidance for molecular refinement
- **Solana-Powered Scalability**: Blockchain-based distribution of computational tasks
- **End-to-End Inhibitor Design**: Complete workflow from concept to validated candidate

## Project Setup

### Directory Structure

```
BindForge/
├── frontend/       # React-based user interface
├── backend/        # FastAPI-based API server
│   ├── utils/      # Utility functions
│   │   └── cid_store.py  # IPFS CID storage on Solana
│   ├── .env        # Environment variables
│   └── .env.sample # Sample environment configuration
├── .venv/          # Python virtual environment
└── README.md       # Project documentation
```

### Prerequisites

- Node.js (v16+)
- Python 3.8+
- Solana CLI tools
- Pinata API account for IPFS storage

### Environment Setup

1. Clone the repository:

```bash
git clone https://github.com/your-username/BindForge.git
cd BindForge
```

2. Create a `.env` file in the backend directory using the provided `.env.sample` as a template:

```bash
cd backend
cp .env.sample .env
```

3. Register for a Pinata account at https://pinata.cloud/ and obtain your API key and secret.
   Update the `.env` file with your Pinata credentials:

```
API_KEY=your_api_key
API_SECRET=your_secret_key
JWT=your_jwt_token
```

4. Generate a Solana keypair (if using Solana functionality):

```bash
solana-keygen new --outfile ~/{path_to_bindforge_folder}/BindForge/id.json
```

5. Update the `KEYPAIR_PATH` in `backend/utils/cid_store.py` if your keypair is stored in a different location:

```python
# Line to modify in cid_store.py
KEYPAIR_PATH = os.path.expanduser("~/{path_to_bindforge_folder}/BindForge/id.json")  # Update with your path
```

6. Fund your Solana account for testing (on devnet):

```bash
solana airdrop 1 $(solana address)
```

### Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

Access the frontend at http://localhost:3000

### Backend Setup

```bash
# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate

# Install dependencies
cd backend
pip install -r requirements.txt

# Run the backend server
uvicorn main:app --reload
```

The API will be available at http://localhost:8000

### Enabling Solana Integration

Set `USE_SOLANA=true` in your `.env` file to enable Solana blockchain integration.
