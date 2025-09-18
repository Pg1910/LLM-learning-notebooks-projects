# LLM Learning Notebooks & Projects

A collection of Jupyter notebooks demonstrating various aspects of Large Language Model (LLM) applications using Cohere's API, including text embeddings, visualization, and text generation.

## 📁 Project Structure

```
LLM-learning-notebooks-projects/
├── text-generation/
│   ├── t1.ipynb          # Text Embeddings & Visualization
│   ├── t2.ipynb          # Chatbot Development
│   └── t3.ipynb          # Text Generation with Temperature Control
├── .env.example          # Environment variables template
├── .gitignore           # Git ignore file
└── README.md            # This file
```

## 📊 Notebooks Overview

### t1.ipynb - Text Embeddings & Visualization
- **Purpose**: Demonstrates how to work with text embeddings using Cohere's Embed API
- **Features**:
  - Dataset preparation and sampling
  - Text-to-embeddings conversion
  - Principal Component Analysis (PCA) for dimensionality reduction
  - Interactive visualizations:
    - Cosine similarity heatmap
    - 2D scatter plots with intent clustering
    - Interactive Altair visualizations
- **Key Libraries**: `pandas`, `numpy`, `sklearn`, `matplotlib`, `seaborn`, `altair`

### t2.ipynb - Chatbot Development
- **Purpose**: Building a conversational chatbot using Cohere's Chat endpoint
- **Features**:
  - Simple chat implementation
  - Context maintenance across conversations
  - Response generation and handling
- **Key Libraries**: `cohere`

### t3.ipynb - Text Generation with Temperature Control
- **Purpose**: Exploring text generation parameters and their effects
- **Features**:
  - Temperature parameter experimentation
  - Multiple response generation
  - Creativity vs. predictability analysis
- **Key Libraries**: `cohere`

## 🚀 Getting Started

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook or JupyterLab
- Cohere API key (get one at [cohere.ai](https://cohere.ai))

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/LLM-learning-notebooks-projects.git
   cd LLM-learning-notebooks-projects
   ```

2. **Install required packages:**
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn altair cohere jupyter
   ```

3. **Set up environment variables:**
   ```bash
   # Copy the example environment file
   cp .env.example .env
   
   # Edit .env and add your Cohere API key
   # COHERE_API_KEY=your-actual-api-key-here
   ```

4. **Start Jupyter:**
   ```bash
   jupyter notebook
   # or
   jupyter lab
   ```

### API Key Setup

**Important**: Never commit your actual API key to version control!

1. Get your API key from [Cohere Dashboard](https://dashboard.cohere.ai/)
2. Create a `.env` file in the project root
3. Add your key: `COHERE_API_KEY=your-actual-key-here`

The notebooks are configured to read from environment variables for security.

## 📈 Key Features & Learning Outcomes

### Text Embeddings (t1.ipynb)
- Learn how to convert text to high-dimensional vector representations
- Understand similarity measurements using cosine similarity
- Master dimensionality reduction techniques with PCA
- Create compelling visualizations to understand embedding spaces
- Explore clustering patterns in semantic space

### Chatbot Development (t2.ipynb)
- Implement conversational AI using modern LLM APIs
- Handle chat context and conversation flow
- Understand message formatting and response processing

### Generation Control (t3.ipynb)
- Experiment with temperature and other generation parameters
- Understand the trade-off between creativity and consistency
- Learn prompt engineering techniques

## 🛠 Technologies Used

- **Cohere API**: For embeddings, chat, and text generation
- **Python Data Stack**: `pandas`, `numpy` for data manipulation
- **Machine Learning**: `scikit-learn` for PCA and similarity calculations
- **Visualization**: `matplotlib`, `seaborn`, `altair` for various plot types
- **Development**: Jupyter notebooks for interactive development

## 📝 Usage Examples

### Running Embeddings Analysis
```python
# Load and prepare your text data
df = load_your_data()

# Generate embeddings
embeddings = get_embeddings(df['text_column'].tolist())

# Visualize with heatmap
create_similarity_heatmap(embeddings)

# Create 2D visualization
plot_2d_embeddings(embeddings, labels)
```

### Using the Chatbot
```python
# Initialize client
co = cohere.ClientV2(api_key)

# Send message
response = co.chat(
    model="command-r-plus",
    messages=[{'role': 'user', 'content': 'Hello!'}]
)
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Useful Resources

- [Cohere Documentation](https://docs.cohere.ai/)
- [Cohere Python SDK](https://github.com/cohere-ai/cohere-python)
- [Text Embeddings Guide](https://docs.cohere.ai/docs/embeddings)
- [Jupyter Notebook Documentation](https://jupyter-notebook.readthedocs.io/)

## 💡 Tips for Usage

1. **Start with small datasets** when experimenting with embeddings
2. **Monitor API usage** to avoid unexpected costs
3. **Experiment with different temperature values** for varied generation styles
4. **Use environment variables** for all sensitive configuration
5. **Version control your experiments** but not your data or keys

## 🐛 Common Issues

### API Key Issues
- Ensure your `.env` file is in the project root
- Check that the API key is valid and has sufficient credits
- Restart your Jupyter kernel after changing environment variables

### Visualization Issues
- Install all required packages: `pip install matplotlib seaborn altair`
- For Altair charts, ensure you have a supported browser
- Increase figure size if plots appear too small

### Memory Issues
- Use smaller datasets for initial experiments
- Consider using `sample()` to work with data subsets
- Clear large variables when no longer needed

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Common Issues](#-common-issues) section
2. Review the [Cohere Documentation](https://docs.cohere.ai/)
3. Open an issue in this repository
4. Join the [Cohere Discord Community](https://discord.gg/co-mmunity)

---

**Happy Learning!** 🎉

*This project is for educational purposes and demonstrates practical applications of modern NLP and LLM technologies.*