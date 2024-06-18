# 3 Pre-trained LLMs Categories

## 3.1 Model Sizes



## 3.2 Closed vs. Open Source

### 3.2.1 Closed Source

### 3.2.2 Open Source

​	LongChain	![img](https://github.com/datawhalechina/llm-universe/raw/main/figures/C1-4-flow_chart.png)

​	LangChain 主要由以下 6 个核心组件组成:

- **模型输入/输出（Model I/O）**：与语言模型交互的接口
- **数据连接（Data connection）**：与特定应用程序的数据进行交互的接口
- **链（Chains）**：将组件组合实现端到端应用。比如后续我们会将搭建`检索问答链`来完成检索问答。
- **记忆（Memory）**：用于链的多次运行之间持久化应用程序状态；
- **代理（Agents）**：扩展模型的推理能力。用于复杂的应用的调用序列；
- **回调（Callbacks）**：扩展模型的推理能力。用于复杂的应用的调用序列；



## 3.3 Transformers

​	![img](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/idP8oaT2QPK8TAdEt6WYEg_41e77abe4ea6457e9706e0c4fa379ff1_image.png?expiry=1718841600000&hmac=Oyi1VtNFdgGHp7D5m54aX0TJGjB2YpVXbz9kLCvfbmg)

1. encoder-only LLM

   - autoencoding

   - MLM (masked language modeling)

   - obj: reconstruct text "denosing"

2. decoder-only LLM

   - autoregressive

   - CLM (causal language modeling)

   - obj: predict next token "full language modeling"

3. encoder-decoder LLM

   - sequence-to-sequence
   - span corruption -> sentinel token
   - obj: reconstruct span

   