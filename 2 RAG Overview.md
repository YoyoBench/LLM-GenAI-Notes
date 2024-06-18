# 2 RAG Overview

Retrieval Augmented Generation

## 2.1 

RAG 是一种将检索（Retrieval）和生成（Generation）结合起来的方法，通常用于改进文本生成任务。

RAG 模型主要包含以下两个部分：

1. **检索模块（Retriever）**：这个模块负责从一个大的知识库（例如，文档集、知识图谱、数据库等）中检索相关信息。检索模块通常基于信息检索技术，例如 TF-IDF、BM25 或者基于深度学习的检索模型（例如，基于 BERT 的双编码器模型）。
2. **生成模块（Generator）**：这个模块接收检索模块返回的相关信息，并利用这些信息来生成最终的输出文本。生成模块通常是一个预训练的语言模型（例如，GPT-3、T5 等），它可以根据输入的上下文和检索到的信息生成连贯和相关的文本。

## 2.2 Steps

1. given Q, search relevant docs from A
2. incorporate retrieved text into an updated prompt
3. generate A

1. 数据处理阶段

   1. 对原始数据进行清洗和处理。
   2. 将处理后的数据转化为检索模型可以使用的格式。
   3. 将处理后的数据存储在对应的数据库中。

2. 检索阶段

   将用户的问题输入到检索系统中，从数据库中检索相关信息。

3. 增强阶段

   对检索到的信息进行处理和增强，以便生成模型可以更好地理解和使用。

4. 生成阶段

   将增强后的信息输入到生成模型中，生成模型根据这些信息生成答案。

![检索增强生成（RAG）的工作流程：从用户查询开始，通过向量数据库检索，到填充提示，最终形成回答的全过程。](https://camo.githubusercontent.com/4d2cee300f4bdd9658f66e2e67d4ff0d492a4b6275c10b697487fc665e093dfa/68747470733a2f2f62616f79752e696f2f696d616765732f7261672f72657472696576616c2d6175676d656e7465642d67656e65726174696f6e2d7261672d66726f6d2d7468656f72792d746f2d6c616e67636861696e2d696d706c656d656e746174696f6e2f315f6b536b6561585276527a624a395372465a614d6f4f672e77656270)

2.3 RAG VS Fine-tuning

​	Fine Tuning: get a small model to perform