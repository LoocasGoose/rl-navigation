# Environment Navigation with Depth-Estimated Terrain

A* should be instant. Q-learning will take about 5 min minimum for 64x64 grid. 
Note: It will take some time and ~1GB to download the model that converts image to depth map.


## ------Some markdown shenanigans------

This project implements a reinforcement learning system that:
1. Generates depth maps from single RGB images
2. Converts depth maps to navigable grid environments
3. Applies path planning algorithms to navigate through these reconstructed environments
4. Visualizes the entire process

## Project Structure

```
.
├── data/                     # Input data and intermediate results
│   ├── images/               # Input RGB images
│   ├── depth_maps/           # Generated depth maps
│   └── grid_maps/            # Processed grid environments
├── models/                   # Saved models
│   ├── depth/                # Pretrained depth estimation models
│   └── rl/                   # Trained RL agent models
├── src/                      # Source code
│   ├── depth_estimation/     # Depth map generation module
│   ├── grid_conversion/      # Depth to grid conversion module
│   ├── environments/         # RL environment implementation
│   ├── agents/               # RL agents implementation
│   ├── planning/             # Path planning algorithms
│   ├── visualization/        # Visualization utilities
│   └── utils/                # Common utilities
├── tests/                    # Test suite
├── notebooks/                # Jupyter notebooks for exploration
├── configs/                  # Configuration files
├── results/                  # Experimental results
├── scripts/                  # Utility scripts
├── pyproject.toml            # Project dependencies
├── setup.py                  # Package setup
├── .gitignore                # Git ignore patterns
├── LICENSE                   # Project license
└── README.md                 # This file
```

## Installation

```bash
# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install the package in development mode
pip install -e .
```

## Required Dependencies

- PyTorch: Deep learning framework
- OpenCV: Image processing
- Gymnasium: Reinforcement learning environments
- TIMM: PyTorch image models
- NumPy: Numerical computing
- Matplotlib: Visualization
- Pygame: Optional for interactive rendering
