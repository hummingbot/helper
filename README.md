# Hummingbot Helper

![](./hummingbot-helper-logo.png)

## Overview

Welcome to the Hummingbot Helper! This repository is dedicated to exploring, testing, and refining the use of Large Language Models (LLMs) in enhancing the functionality and user experience of Hummingbot. Our primary focus is on developing preprocessing techniques and effective LLM chains to assist users in running bots and efficiently answering questions related to Hummingbot's documentation.

Hummingbot is an open-source software that enables users to create and manage automated trading bots for cryptocurrency markets. As the complexity of trading strategies and the diversity of markets grow, the need for advanced, AI-driven assistance becomes increasingly essential. This repository serves as a collaborative platform for researchers, developers, and Hummingbot enthusiasts to contribute and benefit from the integration of LLMs with Hummingbot.

Join us in this exciting journey to integrate cutting-edge LLM technologies with Hummingbot and revolutionize the way we interact with trading tools! 🚀🤖💹

## Getting Started

### Install conda

First, ensure that you have [Anaconda](https://www.anaconda.com/) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) installed on your machine. Afterwards, you should be able to run `conda` command from your path and see a response similar to:
```bash
usage: conda [-h] [-V] command ...

conda is a tool for managing and deploying applications, environments and packages.

Options:

positional arguments:
  command
    clean        Remove unused packages and caches.
    compare      Compare packages between conda environments.
```

### Clone the repo

Clone the repository to your local machine:
```bash
git clone https://github.com/hummingbot/helper.git
```

Create a new `hummingbot-helper` conda environment that install the required dependencies listed in `environment.yml`:
```bash
conda env create
```

Activate the created conda environment:
```bash
conda activate hummingbot-helper
```

* Open the `.env` file in a text editor and replace `placeholder` variables:
```bash
OPENAI_API_KEY=placeholder # replace with your OpenAPI key: sk-123...
PERSIST_DIRECTORY=placeholder # replace with the location where you want to save the vector database: /Users/your_name/helper/vector_stores
```

## Explore the notebooks

Check out the [Explain Documentation notebooks](./research_notebooks/explain_documentation/) contains a set of Jupyter notebooks. These notebooks help you create a vector database based on the current Hummingbot documentation and use it in conjunction with OpenAI models in a basic Retrieval-Augmented Generation (RAG) pipeline.

Run `jupyter notebook` to use the notebooks directly, or access them in Pycharm or VSCode. Explore them to understand the current state of our research. Feel free to modify them and experiment with your own questions.

## Run the app

After you have run through [the first notebook](./research_notebooks/explain_documentation/01_load_hummingbot_docs.ipynb) that creates a vector database based on the Hummingbot docs, you can also test out RAG-based prompts using a test Streamlit app.

Start the app with:
```bash
streamlit run main.py
```

![](./assistant-demo.png)

Note that your OpenAI API key and docs vector database needed to be present for the app to work.

## License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.

## Disclaimer

This repository is for research and educational purposes only. Any scripts or code should not be used for trading cryptocurrency without understanding the risks involved.

## Contact

For any queries or discussions, please open an issue in this repository, and we will get back to you as soon as possible.

## Contributing

We warmly welcome contributions from the community! If you have ideas, code, bug reports, or enhancements, please feel free to open an issue or submit a pull request. For detailed guidelines on how to contribute, please refer to our [Contribution Guidelines](https://hummingbot.org/developers/contributions/).
