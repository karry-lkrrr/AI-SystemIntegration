## Language

- [中文](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README.md)
- [English](https://github.com/LovelittleBears/ollama-chat-ui-vue/blob/main/README_en.md)

---

## ollama-chat-ui-vue

使用`vue3 + vite + elementUi` 搭建的前端 chat,通过 ollama 可与模型对话,目前已经支持`deepseek`的独立思考标签和切换模型(联网查询后续支持)

## 前置工作

安装`ollama`,[ollama 官网地址](https://ollama.com/)
安装完`ollama`后，打开`cmd`，下载模型(模型可以看个人设备性能、任务需求选择，以下是一些参考,任选一个即可 →[模型地址](https://ollama.com/search))

![image-2025818001](https://i-blog.csdnimg.cn/direct/4a3d5b241fbc422fa6059d35e98f7736.png#pic_center)

```bash
ollama run deepseek-r1:1.5b
```
```bash
ollama run deepseek-coder-v2:16b
```
```bash
ollama run qwen2.5-coder:7b
```
等待下载完成，这里我下载的是
```bash
ollama run deepcoder:1.5b
```
当出现以下英文的时候说明运行成功，即可进行下一步
> Send a message(? for help)
![image-2025819001](https://i-blog.csdnimg.cn/direct/0313e33227d84814ac05faeb1340465e.png)
## 启动 ollama
启动前需确保
cmd 打开输入

```bash
ollama serve
```

等待服务启动
⚠️注意：在此处输入`ollama serve`时可能出现端口被占用，这是因为前面下载安装好`ollama`并运行了，直接进行下一步即可

## 启动前端 ollama-chat-ui-vue

注意：node 版本选择 [node-v18.10.0-x64.msi](https://nodejs.org/download/release/v18.10.0/).
下载地址(msi可直接安装)： 
![image-2025819002](https://i-blog.csdnimg.cn/direct/cdbb433195f04d868c8a8171764ae68d.png)

打开项目`cmd`安装依赖

```bash
npm install
```

启动项目

```bash
npm run dev
```
![image-2025819003](https://i-blog.csdnimg.cn/direct/a59d8e5b12074c9089fa784db0f90aad.png)
## 配置文件

src-api-aiSystem-ollama.js
vite.config（此处看需求，若是下载本文件运行正常可省略）

## 运行效果图

![image-2025819004](https://i-blog.csdnimg.cn/direct/1e3528ca841a48b2831ad3505ce0be33.png)

![image-2025819005](https://i-blog.csdnimg.cn/direct/ccf4c710207541ef98b42277b9735a1f.png)

![image-2025819006](https://i-blog.csdnimg.cn/direct/b06d37ded9c34069a46ae79f5c29d2b0.png)

## 欢迎 Issues 交流

## 版权信息
开发不易如果内容帮助到您，请给我们点上星星。

遵循 MIT 开源协议发布，并提供免费使用
