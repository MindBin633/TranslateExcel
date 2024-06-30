# 项目简介

这是一个将excel中的文本翻译成指定语言的项目，使用了在线大模型作为翻译的接口，实现将单元格中的内容翻译成指定语言。

# 项目配置

本项目使用DeepSeek在线模型，需要在[DeepSeek 开放平台](https://platform.deepseek.com/usage)申请API_KEY。

新用户免费送了100万的tokens。请及时使用。

在env中有以下字段：

**OPENAI_MODEL**：不需做任何更改

**OPENAI_API_KEY**：**替换为你申请到的api_key**

**OPENAI_API_BASE**：不需要做任何更改

**CONFIG_FILE_INPUT**：这里替换你需要翻译的excel文件

**CONFIG_FILE_OUTPUT**：这里替换为输出文件名称

**CONFIG_TARGET_LANG**：需要翻译成的目标语言，可以填任何语言如，中文，英语，日语等

## 环境搭建

本案例推荐使用python 3.11来搭建，其他版本应该也适用。

安装项目所需要的包

``````bash
pip install -r requirements.txt
``````

在确保你配置好了.env中的字段之后，开始运行项目

`````bash
python main.py
`````

正确运行之后你就可以看到输出了

# 待改进

一个一个单元格翻译太慢了，考虑优化提示词使返回多个翻译结果，或者使用多线程调用大模型接口实现快速翻译excel

