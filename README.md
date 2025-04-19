# BindForge

An AI-powered drug discovery platform that predicts and optimizes irreversible covalent inhibitors for MK2 with precision, speed, and blockchain-backed scalability.

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
├── .venv/          # Python virtual environment
└── README.md       # Project documentation
```

### Frontend Setup
```bash
cd frontend
npm install
npm run dev
```

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