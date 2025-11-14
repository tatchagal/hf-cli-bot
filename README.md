# hf-cli-bot
CLI Chat Lab Assignment
Last login: Mon Nov 10 08:18:41 on ttys000

The default interactive shell is now zsh.
To update your account to use zsh, please run `chsh -s /bin/zsh`.
For more details, please visit https://support.apple.com/kb/HT208050.
Tatums-MBP:~ tatumgalvin$ python3 --version
Python 3.9.6
Tatums-MBP:~ tatumgalvin$ mkdir -p ~/hf-cli-bot
Tatums-MBP:~ tatumgalvin$ cd ~/hf-cli-bot
Tatums-MBP:hf-cli-bot tatumgalvin$ 
Tatums-MBP:hf-cli-bot tatumgalvin$ python3 -m venv .venv
source .venv/bin/activate

python -m pip install --upgrade pip wheel
Tatums-MBP:hf-cli-bot tatumgalvin$ source .venv/bin/activate
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ python -m pip install --upgrade pip wheel
Requirement already satisfied: pip in ./.venv/lib/python3.9/site-packages (21.2.4)
Collecting pip
  Downloading pip-25.3-py3-none-any.whl (1.8 MB)
     |████████████████████████████████| 1.8 MB 2.8 MB/s 
Collecting wheel
  Downloading wheel-0.45.1-py3-none-any.whl (72 kB)
     |████████████████████████████████| 72 kB 4.0 MB/s 
Installing collected packages: wheel, pip
  Attempting uninstall: pip
    Found existing installation: pip 21.2.4
    Uninstalling pip-21.2.4:
      Successfully uninstalled pip-21.2.4
Successfully installed pip-25.3 wheel-0.45.1
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ pip install llama-cpp-python
Collecting llama-cpp-python
  Downloading llama_cpp_python-0.3.16.tar.gz (50.7 MB)
     ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 50.7/50.7 MB 2.8 MB/s  0:00:18
  Installing build dependencies ... done
  Getting requirements to build wheel ... done
  Installing backend dependencies ... done
  Preparing metadata (pyproject.toml) ... done
Collecting typing-extensions>=4.5.0 (from llama-cpp-python)
  Using cached typing_extensions-4.15.0-py3-none-any.whl.metadata (3.3 kB)
Collecting numpy>=1.20.0 (from llama-cpp-python)
  Downloading numpy-2.0.2-cp39-cp39-macosx_14_0_arm64.whl.metadata (60 kB)
Collecting diskcache>=5.6.1 (from llama-cpp-python)
  Downloading diskcache-5.6.3-py3-none-any.whl.metadata (20 kB)
Collecting jinja2>=2.11.3 (from llama-cpp-python)
  Downloading jinja2-3.1.6-py3-none-any.whl.metadata (2.9 kB)
Collecting MarkupSafe>=2.0 (from jinja2>=2.11.3->llama-cpp-python)
  Downloading markupsafe-3.0.3-cp39-cp39-macosx_11_0_arm64.whl.metadata (2.7 kB)
Downloading diskcache-5.6.3-py3-none-any.whl (45 kB)
Downloading jinja2-3.1.6-py3-none-any.whl (134 kB)
Downloading markupsafe-3.0.3-cp39-cp39-macosx_11_0_arm64.whl (12 kB)
Downloading numpy-2.0.2-cp39-cp39-macosx_14_0_arm64.whl (5.3 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 5.3/5.3 MB 1.6 MB/s  0:00:03
Using cached typing_extensions-4.15.0-py3-none-any.whl (44 kB)
Building wheels for collected packages: llama-cpp-python
  Building wheel for llama-cpp-python (pyproject.toml) ... done
  Created wheel for llama-cpp-python: filename=llama_cpp_python-0.3.16-cp39-cp39-macosx_14_0_arm64.whl size=3887501 sha256=3b39021d1d74fda4b1a235732e8cbe11280bfcf204386cd9d385fba7ad85aa9c
  Stored in directory: /Users/tatumgalvin/Library/Caches/pip/wheels/ed/84/6b/b1835931df9c9dae425cd755cef11e002e101c173fb5a4cc1d
Successfully built llama-cpp-python
Installing collected packages: typing-extensions, numpy, MarkupSafe, diskcache, jinja2, llama-cpp-python
Successfully installed MarkupSafe-3.0.3 diskcache-5.6.3 jinja2-3.1.6 llama-cpp-python-0.3.16 numpy-2.0.2 typing-extensions-4.15.0
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ mkdir -p models
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ mkdir -p models/qwen2.5-0.5b
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd models/qwen2.5-0.5b
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ brew install wget
-bash: brew: command not found
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ wget https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct-GGUF/resolve/main/qwen2.5-0.5b-instruct-q4_k_m.gguf -O qwen2.5b-q4_k_m.gguf
-bash: wget: command not found
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ brew install wget
-bash: brew: command not found
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ curl -L \
>  https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct-GGUF/resolve/main/qwen2.5-0.5b-instruct-q4_k_m.gguf \
>  -o qwen2.5b-q4_k_m.gguf
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100  1353  100  1353    0     0   6428      0 --:--:-- --:--:-- --:--:--  6412
100  468M  100  468M    0     0  3134k      0  0:02:33  0:02:33 --:--:-- 2817k
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ nano cli_chatbot.py
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ import sys
-bash: import: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ from pathlib import Path
-bash: from: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ from llama_cpp import Llama
-bash: from: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ nano cli_chatbot.py
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ #!/usr/bin/env python3
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ import sys
-bash: import: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ from pathlib import Path
-bash: from: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ from llama_cpp import Llama
-bash: from: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # --- model path (pick Qwen OR TinyLlama) ---
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # If you used Qwen Option A:
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ MODEL_PATH = Path("models/qwen2.5-0.5b/qwen2.5b-q4_k_m.gguf")
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # If you used TinyLlama Option B instead, comment the line above
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # and uncomment this:
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # MODEL_PATH = Path("models/tinyllama-1.1b/tinyllama-1.1b-q4_k_m.gguf")
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # --- hyperparameters you can tweak ---
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ N_CTX = 4096          # context window tokens
-bash: N_CTX: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ N_THREADS = 4         # number of CPU threads (can set = number of cores)
-bash: N_THREADS: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ N_BATCH = 256         # token batch size
-bash: N_BATCH: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # --- system prompt (style/behavior) ---
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ SYSTEM_PROMPT = (
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     "You are a helpful teaching assistant. "
-bash: You are a helpful teaching assistant. : command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     "Keep answers concise and clear, and add clarifying steps when appropriate."
-bash: Keep answers concise and clear, and add clarifying steps when appropriate.: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ )
-bash: syntax error near unexpected token `)'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ print(f"Loading model: {MODEL_PATH} …", file=sys.stderr)
-bash: syntax error near unexpected token `f"Loading model: {MODEL_PATH} …",'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ llm = Llama(
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     model_path=str(MODEL_PATH),
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     n_ctx=N_CTX,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     n_threads=N_THREADS,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     n_batch=N_BATCH,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     verbose=False,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ )
-bash: syntax error near unexpected token `)'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ # chat history
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ history = [
-bash: history: =: numeric argument required
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     {"role": "system", "content": SYSTEM_PROMPT},
-bash: {role:: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ ]
-bash: ]: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ print("\nCLI chatbot ready. Type 'exit' or 'quit' to leave.\n")
-bash: syntax error near unexpected token `"\nCLI chatbot ready. Type 'exit' or 'quit' to leave.\n"'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ while True:
>     try:
>         user = input("you › ").strip()
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     except (EOFError, KeyboardInterrupt):
-bash: syntax error near unexpected token `EOFError,'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         print("\nbye! 👋")
-bash: syntax error near unexpected token `"\nbye! 👋"'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         break
-bash: break: only meaningful in a `for', `while', or `until' loop
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     if not user:
>         continue
> 
>     if user.lower() in {"exit", "quit"}:
-bash: syntax error near unexpected token `in'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         print("bye! 👋")
-bash: syntax error near unexpected token `"bye! 👋"'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         break
-bash: break: only meaningful in a `for', `while', or `until' loop
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     # add user message to history
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     history.append({"role": "user", "content": user})
-bash: syntax error near unexpected token `{"role":'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     # stream tokens as they're generated
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     stream = llm.create_chat_completion(
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         messages=history,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         stream=True,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         temperature=0.7,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         top_p=0.95,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         max_tokens=512,
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     )
-bash: syntax error near unexpected token `)'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     print("bot › ", end="", flush=True)
-bash: syntax error near unexpected token `"bot › ",'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     assistant_reply_chunks = []
-bash: assistant_reply_chunks: command not found
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     for chunk in stream:
>         delta = chunk["choices"][0]["delta"]
-bash: syntax error near unexpected token `delta'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         token = delta.get("content", "")
-bash: syntax error near unexpected token `('
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$         if token:
>             assistant_reply_chunks.append(token)
-bash: syntax error near unexpected token `token'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$             print(token, end="", flush=True)
-bash: syntax error near unexpected token `token,'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ 
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     print()  # newline after streaming
> 
>     assistant_reply = "".join(assistant_reply_chunks)
-bash: syntax error near unexpected token `assistant_reply'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$     history.append({"role": "assistant", "content": assistant_reply})
-bash: syntax error near unexpected token `{"role":'
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ chmod +x cli_chatbot.py
chmod: cli_chatbot.py: No such file or directory
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ nano cli_chatbot.py
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ ls
models
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd models/qwen2.5-0.5b
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ ls
qwen2.5b-q4_k_m.gguf
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ python cli_chatbot.py
/Users/tatumgalvin/hf-cli-bot/.venv/bin/python: can't open file '/Users/tatumgalvin/hf-cli-bot/models/qwen2.5-0.5b/cli_chatbot.py': [Errno 2] No such file or directory
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ 
(.venv) Tatums-MBP:qwen2.5-0.5b tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ nano cli_chatbot.py
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ cd ~/hf-cli-bot
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ ls
cli_chatbot.py	models
(.venv) Tatums-MBP:hf-cli-bot tatumgalvin$ python cli_chatbot.py
Loading model: models/qwen2.5-0.5b/qwen2.5b-q4_k_m.gguf …
llama_context: n_ctx_per_seq (4096) < n_ctx_train (32768) -- the full capacity of the model will not be utilized
ggml_metal_init: skipping kernel_get_rows_bf16                     (not supported)
ggml_metal_init: skipping kernel_set_rows_bf16                     (not supported)
ggml_metal_init: skipping kernel_mul_mv_bf16_f32                   (not supported)
ggml_metal_init: skipping kernel_mul_mv_bf16_f32_c4                (not supported)
ggml_metal_init: skipping kernel_mul_mv_bf16_f32_1row              (not supported)
ggml_metal_init: skipping kernel_mul_mv_bf16_f32_l4                (not supported)
ggml_metal_init: skipping kernel_mul_mv_bf16_bf16                  (not supported)
ggml_metal_init: skipping kernel_mul_mv_id_bf16_f32                (not supported)
ggml_metal_init: skipping kernel_mul_mm_bf16_f32                   (not supported)
ggml_metal_init: skipping kernel_mul_mm_id_bf16_f16                (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h64           (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h80           (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h96           (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h112          (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h128          (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h192          (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_hk192_hv128   (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_h256          (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_bf16_hk576_hv512   (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_h64       (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_h96       (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_h128      (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_h192      (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_hk192_hv128 (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_h256      (not supported)
ggml_metal_init: skipping kernel_flash_attn_ext_vec_bf16_hk576_hv512 (not supported)
ggml_metal_init: skipping kernel_cpy_f32_bf16                      (not supported)
ggml_metal_init: skipping kernel_cpy_bf16_f32                      (not supported)
ggml_metal_init: skipping kernel_cpy_bf16_bf16                     (not supported)

CLI chatbot ready. Type 'exit' or 'quit' to leave.

you › cd ~/hf-cli-bot
bot › The command `cd ~/hf-cli-bot` is used to change the current directory to the specified path. Here's a step-by-step explanation:

1. Open your terminal or command prompt.
2. Type `cd` and press `Enter`.

The `cd` command stands for "change directory" and it allows you to navigate through your file system.

3. Type `/` and press `Enter`.

This will change your current directory to the `/` directory, which typically represents your home directory.

So, the complete command line would look something like this:

```
cd /
```
you › what is the name of the current president?
bot › The name of the current president is Joe Biden, as of my last update in October 2023.
you › exit
bye! 👋
