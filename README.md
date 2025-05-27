# Creativity in Vitro EEG Analysis

This repository contains code and data for analyzing EEG (Electroencephalography) data related to Creativity in vitro studies. The project uses Python-based tools for EEG data processing and analysis.

## Project Structure

```
.
├── bids_dataset/     # BIDS-formatted EEG dataset
├── data/
├── notebooks/        # Jupyter notebooks for analysis
└── environment.yml   # Conda environment configuration
```

## Setup

This project uses Conda for environment management. To set up the environment:

1. Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) or [Anaconda](https://www.anaconda.com/products/distribution)
2. Create the environment:
   ```bash
   conda env create -f environment.yml
   ```
3. Activate the environment:
   ```bash
   conda activate creativity-eeg
   ```

## Dependencies

The project uses the following main Python packages:
- Python 3.10
- pandas: Data manipulation and analysis
- numpy: Numerical computing
- matplotlib & seaborn: Data visualization
- scipy: Scientific computing
- jupyterlab: Interactive development environment
- mne: EEG/MEG data processing
- scikit-learn: Machine learning tools

## Usage

1. Activate the conda environment
2. Launch Jupyter Lab:
   ```bash
   jupyter lab
   ```
3. Navigate to the `notebooks/` directory to access the analysis notebooks

## Data

The project contains raw EEG data (first_dataset_raw) recorded using the OpenBCI Cyton board with the Daisy extension (14 channels total). The recordings were made as part of the project **Creativity in vitro**, which investigates how brain activity responds to lyrical and semantic patterns in music.

Lina, the participant listened to 20 repeated loops of 3 of the first six phrases of the song *Aquarela* by Toquinho. These 20 sessions were recorded consecutively in one continuous session, without restarting the OpenBCI GUI.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! To contribute:

1. Fork this repository.
2. Create a new branch for your feature or bugfix.
3. Make your changes and commit them with clear messages.
4. Push your branch to your fork.
5. Open a pull request describing your changes.

Please ensure your code is well-documented and follows best practices. If you are contributing code, try to include tests or example usage when possible. For questions or suggestions, feel free to open an issue.
