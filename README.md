# questions-and-answers-chatbot-langchain-rag
Q&A with AI - indexing input PDFs, retrieval, answering questions with augmented generation

## Install

#### 1. Clone this repository

```
git clone https://github.com/feegloo/questions-and-answers-chatbot-langchain-rag.git
```

#### 2. Generate an OpenAI API Key

https://platform.openai.com/api-keys

Click "+Create new secret key"

Name: "OpenAI-API-key-default" (choose your name)

Click "Create"

Your secret key will look like this: "sk-..."

Note: the generated key will be shown only once, and will not be available for future viewing.
Store it in a secure place, like your Password Manager.

#### 3. Install Python and Jupyter Notebook

Install Python 3.11 with Homebrew:

```
brew install python@3.11
```

At the time of writing this documentation, Python versions newer than 3.11 will not satisfy the `langchain-chroma` dependency, so we need to keep it downgraded.

Verify installation:

```
python3 --version
pip3 --version
```

Note: the Python 3 you use should come from Homebrew, not directly from the macOS version (you should never update macOS Python, as it is used internally by the system).

```
which python3
```

Should display:

```
/opt/homebrew/bin/python3   ✅ (good, Homebrew, Apple Silicon M1/M2/M3...)
/usr/local/bin/python3      ✅ (good, Homebrew, Apple Intel)
/usr/bin/python3            ⚠️ (system Python)
```


#### 4. Create a virtual environment named "v_env"

```
python3 -m venv v_env
source v_env/bin/activate
```

Now all dependencies will be installed locally inside the virtual environment.
To deactivate it later:

```
deactivate
```

Install Jupyter Notebook inside "v_env"

```
pip install notebook
```