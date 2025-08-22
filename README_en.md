# ollama-chat-ui-vue

A front-end chat interface built with `vue3 + vite + elementUi`, enabling conversations with local large models via ollama. Currently, it supports `deepseek`'s independent thinking tags and model switching (internet search functionality will be supported in future updates).


## 🌐 Language Selection
- [中文](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README.md)
- [English](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README_en.md)

## 📋 Preparations

### 1. Install Ollama
First, you need to install the Ollama runtime environment. Official website:  
[Ollama Official Site](https://ollama.com/)

The default installation path for Ollama is the C drive (specifically C:\Users\XX\AppData\Local\Programs\Ollama, where "XX" is your current username). Since the C drive is usually the system drive, long-term use of Ollama or storing multiple models may take up a lot of system drive space, which could cause the computer to run sluggishly.

If you need to migrate Ollama to another disk to free up space on the C drive, you can refer to the following detailed tutorial:  
[Step-by-Step Guide to Moving Ollama to Another Drive](https://blog.csdn.net/xiaoxiongxia/article/details/145523060?spm=1001.2014.3001.5501)

### 2. Download a Model
After installation, open a command-line tool (CMD/PowerShell) and download a model based on your device performance and task requirements (for model options, see: [ollama Model Library](https://ollama.com/search)).

Recommended model examples:
```bash
# Lightweight model (for beginners)
ollama run deepseek-r1:1.5b

# Code-specialized model
ollama run deepseek-coder-v2:16b

# General-purpose model
ollama run qwen2.5-coder:7b
```

> Example: This guide uses `deepcoder:1.5b` for demonstration
> ```bash
> ollama run deepcoder:1.5b
> ```

The model is running successfully when you see this prompt in the command line:  
`Send a message(? for help)`  

![Model startup success](https://i-blog.csdnimg.cn/direct/0313e33227d84814ac05faeb1340465e.png)


## 🚀 Start the ollama Service
After preparing the model, start the ollama service:

1. Open a command-line tool and enter:
   ```bash
   ollama serve
   ```

2. Wait for the service to start completely.

> [!WARNING]
> If you see a "port occupied" error when running `ollama serve`, it’s usually because ollama is already running in the background. You can proceed to the next step directly.
> 
> ![Port occupation prompt](https://i-blog.csdnimg.cn/direct/e779a071bb584ac4b86f4753af09f003.png)


## 💻 Start the Front-End Project

### Environment Requirements
- **Node.js version**: Must be `v18.10.0`  
  Download link: [Node.js v18.10.0](https://nodejs.org/download/release/v18.10.0/) (recommended to download the `.msi` file for direct installation)  
  ![Node.js download page](https://i-blog.csdnimg.cn/direct/cdbb433195f04d868c8a8171764ae68d.png)


### Steps
1. After cloning the project, open the command line in the project root directory and install dependencies:
   ```bash
   npm install
   ```

2. Start the development server:
   ```bash
   npm run dev
   ```

Once started successfully, a local access address will be displayed. Example:  
![Project startup success](https://i-blog.csdnimg.cn/direct/a59d8e5b12074c9089fa784db0f90aad.png)


## ⚙️ Configuration Files
To customize settings, modify these files:
- `src/api/aiSystem/ollama.js` (API-related configurations)
- `vite.config.js` (Project build configurations; can be ignored if the project runs normally by default)


## 📸 Screenshots
![Chat interface 1](https://i-blog.csdnimg.cn/direct/1e3528ca841a48b2831ad3505ce0be33.png)  
![Chat interface 2](https://i-blog.csdnimg.cn/direct/ccf4c710207541ef98b42277b9735a1f.png)  
![Chat interface 3](https://i-blog.csdnimg.cn/direct/b06d37ded9c34069a46ae79f5c29d2b0.png)


## 🤝 Feedback & Communication
Feel free to submit issues or suggestions via [Issues](https://github.com/LovelittleBears/ollama-chat-ui-vue/issues).


## 📄 Copyright Information
This project is released under the **MIT open-source license** and is free to use.  
Development takes effort—if this content helps you, please consider giving it a Star!
