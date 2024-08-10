# Question-Answer-generation-using-Llama-Index-on-Mac
# Question-Answer Generation using Llama-Index on Mac

## Working with Llama-Index on Mac: PDF Documentation Q&A

### Initial Arrangements
1. **Ensure you have Python 3 upgraded.**
2. **Create a new folder on your Mac, for example, `llama`, and create a new file in it with a name of your choice and the `.ipynb` extension. Example: `llama.ipynb`.**
3. **Create another folder inside the `llama` folder and name it `data`. Insert the PDF file you want to work on into this `data` folder. The directory structure will look like this:**

    ```
    llama/
    │
    ├── llama.ipynb        # Your Jupyter Notebook file
    │
    └── data/              # Folder containing your data files
        └── your_file.pdf  # The PDF file you want to work on
    ```

    This structure ensures that the Notebook (`llama.ipynb`) and the PDF file you want to process (`your_file.pdf`) are organized within the `llama` project folder.

4. **Open the `llama` folder in any code editor.**

### Creating and Activating a Virtual Environment
1. **Navigate to the `llama` directory using the `cd` command from the terminal. Example:**

    ```sh
    cd /path_to_llama
    ```

2. **Create a new virtual environment and activate it using the following commands:**

    ```sh
    pip install virtualenv
    virtualenv venv
    source venv/bin/activate
    ```

    The virtual environment is activated. To verify, you should see the terminal prompt start with `(.venv)`. Example: `(.venv) name@names-MacBook-Air llama`.

### Starting Ollama and Running the Respective Model (Llama Index)
1. **Open another tab or window in the same terminal with the virtual environment activated, including the path. Run:**

    ```sh
    ollama start
    ```

2. **If you encounter a port address unavailable or already in use error (Error: listen tcp 127.0.0.1:11434: bind: address already in use), kill the port using:**

    ```sh
    killall ollama
    ```

3. **Then start Ollama again using:**

    ```sh
    ollama start
    ```

    It should start without any errors.

4. **Next, open another tab or window in the same terminal with the virtual environment activated and the path included. Run:**

    ```sh
    ollama run llama3
    ```

    This will download `llama3` via Ollama. Wait until the installation is successful, until the 'send a message' line pops up/shows in the terminal where you ran the `ollama run llama3` command.
