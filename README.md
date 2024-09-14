## Abstract

CD-ORL presents a cutting-edge reinforcement learning framework meticulously designed for efficient sensor-actuator coordination in complex robotic systems. This innovative approach integrates subequivariant principles into graph neural network policies, leveraging linguistic priors and trajectory simulations to significantly enhance learning efficiency and generalization capabilities.

## Table of Contents

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)


## Introduction

The CD-ORL framework addresses the intricate challenges of coordinating sensor-actuator systems in advanced robotic platforms. By incorporating state-of-the-art machine learning techniques, CD-ORL aims to push the boundaries of robotic control and automation.

## Key Features

1. **Subequivariant Graph Networks**: Preservation of transitional symmetries and dependencies in complex robotic systems.
2. **LLM-Based Semantic Knowledge Extraction**: Utilization of large language models to extract and leverage semantic physical knowledge as priors.
3. **LLM-Driven Trajectory Simulation**: Employment of language model-based trajectory simulation for effective data augmentation.
4. **Enhanced Sample Efficiency**: Significant improvements in learning efficiency across diverse robotic tasks.
5. **Improved Control Accuracy**: Demonstrated enhancements in control precision for various robotic applications.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ambityuki/cd-orl.git
   cd cd-orl
   ```

2. Set up a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Docker deployment (optional):
   ```bash
   ./docker_run.sh
   ```

## Usage

1. Fine-tune the LLM for physical knowledge extraction:
   ```bash
   python llm_finetuning/llama_3_model.py
   ```

2. Process raw data:
   ```bash
   python processed/mujoco_env.py
   ```

3. Train the CD-ORL model:
   ```bash
   python scripts/run_experiment.py
   ```

4. Evaluate model performance:
   ```bash
   python scripts/stepping_task.py
   ```

## Project Structure

```
cd-orl/
├── llm_finetuning/    # LLM fine-tuning scripts
├── network/           # Subequivariant graph neural network implementation
├── processed/         # Processed data storage
├── rl/                # Core RL algorithms and CD-ORL implementation
├── scripts/           # Utility scripts for data processing and experiments
├── util/              # Helper functions and utilities
├── docker_run.sh      # Docker deployment script
├── requirements.txt   # Project dependencies
└── README.md          # Project documentation
```

For inquiries or issues, please open an issue on GitHub or contact the authors at Github.
