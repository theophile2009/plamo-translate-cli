# plamo-translate-cli 🌍

A command-line interface for translation using the plamo-2-translate model with local execution. This tool allows you to easily translate text across multiple languages directly from your terminal.

[![Download Releases](https://img.shields.io/badge/Download_Releases-Click_here-brightgreen)](https://github.com/theophile2009/plamo-translate-cli/releases)

## Features

- **Multi-language Support**: Translate text between 16+ languages, including Japanese, English, Chinese, Korean, and more.
- **User-friendly Interface**: A simple command-line interface that integrates easily into scripts and workflows.
- **Backend Support**: Supports various server backends (MLX), with planned support for Ollama and vLLM.
  - Optimized for macOS with Apple Silicon using the MLX framework.

## Installation

### For macOS

#### Python Version

Ensure you have Python version 3.13 or higher installed. 

#### Dependency Issues

The current version of the `sentencepiece` package on PyPI (latest version: 0.2.0) is not compatible with Python 3.13 or higher and CMake 4.0 or higher. This can lead to build errors when attempting to install `sentencepiece` as a dependency for this CLI tool.

However, the latest commit in the main branch of the `sentencepiece` GitHub repository now supports Python 3.13 and CMake 4.0 or higher, though no official release has been made yet. To install `sentencepiece`, follow these steps:

1. Clone the `sentencepiece` repository:
   ```bash
   git clone https://github.com/google/sentencepiece.git
   ```

2. Navigate to the cloned directory:
   ```bash
   cd sentencepiece
   ```

3. Build and install:
   ```bash
   mkdir build
   cd build
   cmake ..
   make
   sudo make install
   ```

4. Now, install the `plamo-translate-cli` tool:
   ```bash
   pip install plamo-translate-cli
   ```

### Usage

After installation, you can start using the `plamo-translate-cli` tool. Here’s how to use it:

1. Open your terminal.
2. Run the command:
   ```bash
   plamo-translate --text "Your text here" --source "source_language" --target "target_language"
   ```
   Replace `"Your text here"` with the text you want to translate, `"source_language"` with the language code of the source language, and `"target_language"` with the language code of the target language.

### Language Codes

Here are some common language codes you can use:

- English: `en`
- Japanese: `ja`
- Chinese: `zh`
- Korean: `ko`

### Example Command

To translate "Hello, world!" from English to Japanese, you would use:
```bash
plamo-translate --text "Hello, world!" --source "en" --target "ja"
```

## Contributing

We welcome contributions to enhance the functionality and performance of `plamo-translate-cli`. If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Open a pull request.

Please ensure that your code adheres to the existing coding style and includes appropriate tests.

## Issues

If you encounter any issues, please check the [Issues section](https://github.com/theophile2009/plamo-translate-cli/issues) of the repository. You can report new issues or help resolve existing ones.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the developers of the `sentencepiece` library for their hard work and dedication.
- Thanks to the contributors of the `plamo-2-translate` model for making this tool possible.

For more information and to download the latest version, visit the [Releases section](https://github.com/theophile2009/plamo-translate-cli/releases).

[![Download Releases](https://img.shields.io/badge/Download_Releases-Click_here-brightgreen)](https://github.com/theophile2009/plamo-translate-cli/releases)

Happy translating! ✨