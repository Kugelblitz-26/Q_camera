# Advanced Compton Camera Reconstruction with Physical Simulation

This project implements state-of-the-art Compton camera reconstruction using deep learning with physically accurate simulation data. The implementation includes multiple advanced CNN architectures trained on datasets generated with proper Compton scattering physics.

## 🚀 Features

- **Physically Accurate Simulation**: Klein-Nishina cross-sections and Compton kinematics
- **Advanced CNN Architectures**: ResNet, Attention, DenseNet, and Vision Transformer inspired models
- **Comprehensive Training Pipeline**: Cross-validation, hyperparameter tuning, and evaluation
- **Multiple Dataset Configurations**: Single, dual, triple, and quintuple source scenarios
- **Complete Evaluation Framework**: Performance metrics, visualizations, and model comparison

## 📋 Prerequisites

```bash
pip install numpy pandas torch torchvision scikit-learn matplotlib seaborn tqdm
```

## 🛠️ Project Structure

```
├── physical_dataset_generator.py    # Physically accurate Compton simulation
├── dataset_generator.py            # Basic dataset generation (legacy)
├── improved_qcam.py               # Enhanced CNN architectures
├── model_comparison.py            # Model comparison framework
├── training_pipeline.py           # Complete training pipeline
├── run_full_pipeline.py           # Orchestration script
└── README.md                     # This file
```

## 🔧 Usage

### 1. Generate Physical Datasets

```bash
# Generate physically accurate datasets
python physical_dataset_generator.py --generate-all --output-dir data

# Visualize physical dataset properties
python physical_dataset_generator.py --visualize --photon-energy 1.0
```

### 2. Train Models

```bash
# Train all advanced CNN architectures
python training_pipeline.py

# Compare different architectures
python model_comparison.py
```

### 3. Run Complete Pipeline

```bash
# Execute the entire workflow
python run_full_pipeline.py
```

## ⚙️ Physical Simulation Details

The `PhysicalComptonSimulator` implements:

- **Klein-Nishina Cross-Section**: Accurate Compton scattering angular distribution
- **Compton Kinematics**: Proper energy-momentum conservation
- **Exponential Attenuation**: Realistic photon propagation through matter
- **Energy Conservation**: Scattered photon + recoil electron energy equals incident energy

### Key Physics Parameters:

- **Incident Photon Energy**: 1.0 MeV (configurable)
- **Compton Attenuation Coefficient**: 0.05 mm⁻¹
- **Photoelectric Absorption Coefficient**: 0.08 mm⁻¹
- **Electron Rest Mass**: 0.511 MeV/c²

## 🧠 Model Architectures

### 1. Advanced ResNet CNN
- Residual connections for deeper networks
- Batch normalization and dropout
- Adaptive average pooling

### 2. Attention-Based CNN
- Attention mechanisms to focus on important features
- Multi-scale feature extraction
- Channel-wise attention modules

### 3. Dense CNN
- Dense connections for feature reuse
- Growth rate optimization
- Transition layers for downsampling

### 4. Vision Transformer Inspired
- Patch-based feature extraction
- Self-attention mechanisms
- Transformer encoder layers

## 📊 Evaluation Metrics

- **Mean Absolute Error (MAE)**: Average localization error
- **Per-Axis MAE**: X and Y coordinate errors separately
- **R² Score**: Variance explained by the model
- **Cross-Validation**: Robust performance estimation
- **Residual Analysis**: Error distribution examination

## 📈 Output Files

- `data/SIM_events_physical_*.csv` - Generated physical datasets
- `best_*.pth` - Trained model checkpoints
- `training_history_*.png` - Training curves
- `evaluation_results_*.png` - Performance visualizations
- `model_comparison_results.png` - Architecture comparison
- `physical_dataset_visualization.png` - Physics validation plots

## 🎯 Applications

This implementation is suitable for:
- Medical imaging (SPECT/PET alternatives)
- Nuclear security and safeguards
- Astrophysical observations
- Material science applications
- Research in gamma-ray detection

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 📚 References

- Klein-Nishina formula for Compton scattering
- Advanced CNN architectures for computer vision
- Compton camera reconstruction algorithms
- Deep learning for physics applications

---

**Note**: This project is actively maintained. For questions, suggestions, or issues, please open an issue on GitHub.
