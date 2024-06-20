# ArtiMuse AI

## Description
ArtiMuse AI leverages advanced AI technologies to convert textual descriptions into both narrative text and corresponding visual imagery. This tool integrates capabilities from OpenAI's GPT models and Hugging Face's Stable Diffusion models to provide a seamless generation of enriched content. It is designed to assist creative professionals, marketers, and content creators in automating the creation of digital content.

## Features
- **Dynamic Text to Image Conversion**: Utilizes Stable Diffusion models to transform textual prompts into high-quality images.
- **Enhanced Text Generation**: Incorporates OpenAI's GPT models to create detailed and contextually relevant narratives based on initial user inputs.
- **Streamlit Web Interface**: Offers an interactive web interface for easy submission of prompts and real-time viewing of generated outputs.
- **Flexible Deployment**: Configured to run both locally and over the cloud with Pyngrok tunneling for easy access.

## Installation
Ensure you have Python installed and then run the following commands to install necessary libraries:
```bash
pip install streamlit pyngrok openai diffusers transformers scipy ftfy accelerate safetensors langchain python-dotenv google-search-results Pillow stability-sdk
pip install git+https://github.com/huggingface/diffusers
```

## Configuration
Before running the application, set up the necessary environment variables:
```bash
export OPENAI_API_KEY='your-openai-api-key'
export SERPAPI_API_KEY='your-serpapi-api-key'
export STABILITY_HOST='grpc.stability.ai:443'
export STABILITY_KEY='your-stability-key'
```

## Running the Application
To run ArtiMuse AI, execute the following commands:
```bash
streamlit run app.py &>/dev/null &
npx localtunnel --port 8501
```
This will start the Streamlit app and expose it using a localtunnel, making it accessible via a web URL.

## Detailed Usage Guide
### Starting the App
Navigate to the localtunnel URL displayed in your command prompt to access the Streamlit interface.

### Interface Overview
- **Sidebar**: Input fields for entering the text prompts.
- **Main Area**: Displays the generated text and images.

### Generating Content
1. **Input Prompts**: Enter the desired text in the sidebar fields.
2. **Select Model**: Choose the AI model for image generation.
3. **Generate Content**: Click the "Generate Blog" button to start content generation.

### Viewing Results
The AI-generated text and corresponding images will be displayed in the main area of the interface.

## Code Overview
The `app.py` file contains all necessary code to configure and run the application. Key components include:
- **API Key Configuration**: Sets up necessary API keys for accessing AI models.
- **Streamlit Configuration**: Defines the layout and elements of the web interface.
- **Image Generation Function**: Handles the creation of images based on textual prompts using selected AI models.
- **Main Loop**: Captures input from the user interface, processes it through the AI models, and displays the results.

## Contributing
Feel free to fork this project, make improvements, and submit pull requests. We appreciate contributions to enhance functionality or documentation.

## License
ArtiMuse AI is open-sourced under the MIT License.

## Contact
For questions or support, please contact tahafarag111@gmail.com.
