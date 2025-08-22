# Ollama-chat-ui-vue

这是一个基于`vue3 + vite + elementUi`构建的前端聊天界面，通过`ollama`可与本地大模型对话。目前已支持`deepseek`独立思考标签及模型切换功能（联网查询功能将在后续支持）。

## 🌐 语言选择
- [中文](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README.md)
- [English](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README_en.md)

## 📋 前置准备

### 1. 安装 ollama
首先需要安装 ollama 运行环境，官方地址：  
[ollama 官网](https://ollama.com/)

如果你是刚接触 Ollama，想了解它的基本信息、功能特点等内容，可以参考这篇详细的介绍教程：[Ollama 介绍教程](https://blog.csdn.net/TINGlkrrr/article/details/150492201?spm=1011.2415.3001.5331)，帮助你快速认识和上手这个工具。

Ollama 安装的默认路径为 C 盘（具体路径为 C:\Users\XX\AppData\Local\Programs\Ollama，其中“XX”为当前用户名）。由于 C 盘通常是系统盘，若长期使用 Ollama 或存储较多模型，可能会占用大量系统盘空间，进而导致电脑运行卡顿。

若需要将 Ollama 迁移到其他磁盘以释放 C 盘空间，可参考以下详细教程：  
[Ollama 移动到其他盘的具体操作步骤](https://blog.csdn.net/xiaoxiongxia/article/details/145523060?spm=1001.2014.3001.5501)。

### 2. 下载模型
安装完成后，打开命令行工具（CMD/PowerShell），根据设备性能和任务需求选择并下载模型（模型列表参考：[ollama 模型库](https://ollama.com/search)）。

推荐模型示例：
```bash
# 轻量模型（适合入门）
ollama run deepseek-r1:1.5b

# 代码专用模型
ollama run deepseek-coder-v2:16b

# 通用模型
ollama run qwen2.5-coder:7b
```

> 示例：本文以 `deepcoder:1.5b` 为例演示
> ```bash
> ollama run deepcoder:1.5b
> ```

当命令行出现以下提示时，说明模型运行成功：  
`Send a message(? for help)`  

![模型启动成功示意](https://i-blog.csdnimg.cn/direct/0313e33227d84814ac05faeb1340465e.png)


## 🚀 启动 ollama 服务
模型准备完成后，需启动 ollama 服务：

1. 打开命令行工具，输入以下命令：
   ```bash
   ollama serve
   ```

2. 等待服务启动完成即可。

> [!WARNING]
> 若执行 `ollama serve` 时提示端口被占用，通常是因为之前已启动过 ollama 服务，直接进行下一步即可。
> 
> ![端口占用提示](https://i-blog.csdnimg.cn/direct/e779a071bb584ac4b86f4753af09f003.png)


## 💻 启动前端项目

### 环境要求
- **Node.js 版本**：必须为 `v18.10.0`  
  下载地址：[Node.js v18.10.0](https://nodejs.org/download/release/v18.10.0/)（推荐下载 `.msi` 格式直接安装）  
  ![Node.js 下载页示意](https://i-blog.csdnimg.cn/direct/cdbb433195f04d868c8a8171764ae68d.png)


### 操作步骤
1. 克隆项目后，在项目根目录打开命令行，安装依赖：
   ```bash
   npm install
   ```

2. 启动开发服务器：
   ```bash
   npm run dev
   ```

启动成功后会显示本地访问地址，示例：  
![项目启动成功示意](https://i-blog.csdnimg.cn/direct/a59d8e5b12074c9089fa784db0f90aad.png)


## ⚙️ 配置文件说明
如需自定义配置，可修改以下文件：
- `src/api/aiSystem/ollama.js`（接口相关配置）
- `vite.config.js`（项目构建配置，若默认运行正常可忽略）


## 📸 运行效果展示
![聊天界面展示1](https://i-blog.csdnimg.cn/direct/1e3528ca841a48b2831ad3505ce0be33.png)  
![聊天界面展示2](https://i-blog.csdnimg.cn/direct/ccf4c710207541ef98b42277b9735a1f.png)  
![聊天界面展示3](https://i-blog.csdnimg.cn/direct/b06d37ded9c34069a46ae79f5c29d2b0.png)


## 🤝 交流与反馈
欢迎通过 [Issues](https://github.com/LovelittleBears/ollama-chat-ui-vue/issues) 提交问题或建议。


## 📄 版权信息
本项目遵循 **MIT 开源协议** 发布，可免费使用。  
开发不易，若内容对您有帮助，欢迎点亮 Star 支持！
