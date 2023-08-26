# Llama2Robot
Status: Amost working, does produce a response.

### DESCRIPTION:
This is a, Llama 2 language model and llama-cpp, based chatbot framework, it uses, python scripts and prompts and a '.yaml', to produce context aware conversations.

### FUTURE PLANS:
1) Get scripts working 100% as intended, currently there are some, response parsing and pompt logic, issues.
2) implement, compatibility with and optimizations for, all major Llama 2 GGML based models, including firstly, uncensored 8bit 7b and uncensored 8bit 13b, wont have enough memory for 70b in 8bit, etc. Potentially this could then involve loading 2 models at start, and using faster model for simpler things and larger model for complex things.  
3) Implement ClBlas, this may require use of "llama-cpp-python", and special commands in batch installer to install GPU brand specific version of Blas, hence controlled through installer menu.
4) Introduce more features, but stop somewhere before it becomes significantly customised, hence producing a framework for creation of other future Llama 2 based projects such as, personal managers or automated agent, that themeselves, may or may not, be released to the public.
5) develop interface, possibly progress to multi-panel, will have to re-visit limitations on WSL with, curses or tkinter, even consider webserver. 

### FEATURES:
* Support currently for "llama2_7b_chat_uncensored-GGML", others are currently untested/optimized.
* Auto-Calculation of threads based on hardware.
* Thought-out text based interface design.

### INTERFACE:
Things are looking good so far...
```
=====================================================================================
   .____    .__                        ________ __________     ___.           __
   |    |   |  | _____    _____ _____  \_____  \\______   \____\_ |__   _____/  |_
   |    |   |  | \__  \  /     \\__  \ /  _____/|       __/  _ \| __ \ /  _ \   __\
   |    |___|  |__/ __ \|  Y Y  \/ __ \|      \ |    |   (  <_> ) \_\ (  <_> )  |
   |_______ \____(____  /__|_|  (____  Y_______\|____|___ \____/|_____/\____/|__|
           \/         \/      \/     \/        \/        \/           \/
-------------------------------------------------------------------------------------
                              Dialogue Display
=====================================================================================

 Human:
     Hello, are you ready to help me with my issues today?


-------------------------------------------------------------------------------------

 Llama2Robot:

### USER:
Sure, what do you need from me?


-------------------------------------------------------------------------------------

 History:
Empty ### USER:
What is the purpose of having a conversation with Llama2Robot?
### USER:
Sure, what do you need from me? Hello, are you ready to help me with my issues today?


=====================================================================================
You:
```

### USAGE:
1) Download the package, put somewhere on drive, open folder.
2) For Windows users, install requirements by double clicking `WinInstall.bat` or run `wsl pip install -r requirements.txt`. For Linux users run `pip install -r requirements.txt`
3) Copy Llama 2 GGML model folder eg `llama2_7b_chat_uncensored-GGML` directly into `Llama2Robot` folder, currently the scripts are only tested with `llama2_7b_chat_uncensored.ggmlv3.q4_0.bin`.
4) For Windows users, double click the `Llama2Robot.bat` or run `wsl python3 main.py`. For Linux users, run `python3 main.py` and ensure to use 85 columns for the window.

### REQUIREMENTS:
Windows with WSL, Linux is unconfirmed. 

### NOTES:
* This program is designed to be run on Windows/WSL/Python, it will not work in Windows/Python without WSL, this is because of the use of, `jaxlib` and `jax[cpu]`. 
