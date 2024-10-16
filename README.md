# Prompt Injection Attacks on Vision Language Models in Oncology

This repository contains the code and resources for the research project "Prompt Injection Attacks on Vision Language Models in Oncology" by Jan Clusmann et al., published in Nature Communications.

## Overview

This study investigates the vulnerability of state-of-the-art Vision-Language Models (VLMs) to prompt injection attacks in the context of medical imaging analysis. The research demonstrates that subtle prompt injection attacks can cause harmful outputs in VLMs, posing significant security risks in healthcare applications.

## Repository Contents

1. `prompt_injection_defense_ethical.py`: Python script for analyzing medical images using various LLM models including options for prompt variation.
2. `prompt_injection_defense_agent.py`: Python script for analyzing medical images using various LLM models with an agent-based approach, using the outputs from the first script and passing them again to a "supervisor model"

3. R scripts for data analysis and visualization (see `README_Visuals_Statistics.md` for details).

## Data Availability

The complete dataset used in this study, including the medical images and raw data, is available with the publication at Nature Communications under open access. Please refer to the publication for accessing the full dataset.

## Analysis Types

### 1. Prompt Injection Defense with Ethical Prompt Variation

This analysis explores the use of ethical prompts to defend against prompt injection attacks. For detailed instructions, see the section below titled "README for Ethical Prompt Analysis".

### 2. Prompt Injection Defense with Agent-based Approach

This analysis uses an agent-based system to mitigate prompt injection attacks. For detailed instructions, see the section below titled "README for Agent-based Analysis".



### 3. Data Visualization and Statistical Analysis

R scripts are provided for visualizing results and performing statistical analyses. For detailed instructions, see `README_Visuals_Statistics.md` in this repository.

## Requirements

- Python 3.7+
- R (for data visualization and statistical analysis)
- API keys for Anthropic (Claude models), OpenAI (GPT-4 models), and Reka (Reka-Core model)
- Required Python libraries: anthropic, openai, openpyxl, python-dotenv, reka, pandas
- Required R packages: dplyr, ggplot2, rstatix, openxlsx

## Citation

If you use this code or data in your research, please cite our paper:

[Citation details to be added upon publication]

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For questions or issues regarding the code, please open an issue in this repository or contact jan.clusmann@rwth-aachen.de

---

# README for Agent-based Analysis

## Setup

1. Clone this repository.
2. Install required Python libraries: `pip install anthropic openai openpyxl python-dotenv reka pandas`
3. Create three `.env` files in the project root:
   - `api_claude.env`: Contains `API_KEY_CLAUDE=your_anthropic_api_key`
   - `api_gpt4.env`: Contains `OPENAI_API_KEY=your_openai_api_key`
   - `api_reka.env`: Contains `REKA_API_KEY=your_reka_api_key`
4. Place the medical images in a folder named "Images_Mitigation" in the project root.

## Usage

Run the script with:

```
python prompt_injection_defense_agent.py
```

The script will generate an Excel file named "Mitigation_PI_revision.xlsx" with the analysis results.

---

# README for Ethical Prompt Analysis

## Setup

Follow the same setup steps as for the Agent-based Analysis.

## Usage

Run the script with:

```
python prompt_injection_defense_ethical.py
```

This script will also generate an Excel file named "Mitigation_PI_revision.xlsx" with the analysis results.

---

Remember that the complete dataset, including the medical images (90 images named "Folie1.jpg" to "Folie90.jpg"), is available with the publication at Nature Communications under open access. Please refer to the publication for accessing the full dataset for reproducibility.
