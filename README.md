# Gen-AI-With-Deep-Seek-R1

## Overview

The **Gen-AI-App** is a Streamlit-based application designed to provide an interactive interface for AI-powered coding assistance. It leverages advanced language models to help users debug, document, and design solutions for their programming needs. The project consists of two separate applications, `app.py` and `app2.py`, each offering unique functionalities.

## Features

### Common Features
- **Interactive Chat Interface**: Users can interact with the AI assistant in a conversational manner.
- **Streamlit Integration**: Provides a visually appealing and user-friendly interface.
- **Customizable Models**: Allows users to select different AI models for their needs.
- **Session Management**: Maintains a log of user and AI messages for context-aware responses.

### `app.py` Features
- **AI Coding Assistant**: Offers concise and correct solutions to coding problems.
- **Debugging Support**: Provides strategic print statements for debugging.
- **Model Selection**: Supports multiple models like `deepseek-r1:1.5b` and `deepseek-r1:3b`.
- **Custom Styling**: Includes custom CSS for a dark-themed interface.

### `app2.py` Features
- **Extended Functionality**: (Add specific features of `app2.py` here if available.)
- **Additional Model Support**: (Mention any additional models or configurations supported in `app2.py`.)

## Project Structure

```
gen-ai-app/
│
├── app.py               # Main application file for AI coding assistant
├── app2.py              # Secondary application with extended functionality
├── requirements.txt     # Python dependencies
├── README.md            # Project documentation
```

## Requirements

The project requires the following Python libraries:

- `streamlit`
- `langchain`
- `ollama`

Install the dependencies using:

```bash
pip install -r requirements.txt
```

## Usage

### Running the Applications

#### `app.py`
To run the main application, execute the following command in your terminal:

```bash
streamlit run app.py
```

#### `app2.py`
To run the secondary application, execute:

```bash
streamlit run app2.py
```

### Interacting with the Application

1. **Select a Model**: Use the sidebar to choose the desired AI model.
2. **Ask Questions**: Type your coding questions or debugging issues in the input box.
3. **View Responses**: The AI assistant will provide solutions or suggestions in the chat interface.

### Example Interaction

#### User Input:
```
How do I fix a KeyError in Python?
```

#### AI Response:
```
A KeyError occurs when you try to access a key that doesn't exist in a dictionary. To fix it, you can:
1. Use the `.get()` method to provide a default value.
2. Check if the key exists using the `in` keyword before accessing it.
Example:
```
```python
my_dict = {"a": 1, "b": 2}
key = "c"
value = my_dict.get(key, "default_value")
print(value)  # Output: default_value
```

## Customization

### Modifying the System Prompt
The system prompt in `app.py` can be customized to change the behavior of the AI assistant. Update the `system_prompt` variable in the code:

```python
system_prompt = SystemMessagePromptTemplate.from_template(
    "You are an expert AI coding assistant. Provide concise, correct solutions "
    "with strategic print statements for debugging. Always respond in English."
)
```

### Adding New Models
To add support for additional models, update the `selected_model` options in the sidebar configuration:

```python
selected_model = st.selectbox(
    "Select Model",
    ["deepseek-r1:1.5b", "deepseek-r1:3b", "new-model-name"],
    index=0
)
```

## Future Enhancements

- Add support for more advanced AI models.
- Implement a feedback mechanism for users to rate AI responses.
- Extend `app2.py` with additional features like code generation or testing.
- Create a deployment pipeline for hosting the application on cloud platforms.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments

- Built with [Streamlit](https://streamlit.io/)
- Powered by [LangChain](https://python.langchain.com/) and [Ollama](https://ollama.ai/)