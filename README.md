# SRT Subtitle Splitter

## 简介

该脚本用于从 SRT 文件中提取字幕文本，并根据翻译后的文本生成新的 SRT 文件。它适用于需要处理和翻译字幕的用户，提供了简单的接口来提取和创建字幕文件。

## 功能

1. **提取字幕文本**：从指定的 SRT 文件中提取所有字幕文本，并保存到一个文本文件中。
2. **生成翻译后的 SRT 文件**：根据提取的字幕和翻译后的文本生成新的 SRT 文件。

## 文件结构

- `1.srt`：待处理的 SRT 文件（请根据需要替换为你的文件名）。
- `extracted_text.txt`：提取的字幕文本输出文件。
- `translated_text.txt`：翻译后的文本文件（用户需手动提供）。
- `translated_1.srt`：生成的翻译后的 SRT 文件。

## 使用说明

### 环境要求

- Python 3.x

### 使用步骤

1. 将待处理的 SRT 文件命名为 `1.srt` 并放置在脚本所在的目录中。
2. 创建一个包含翻译后的字幕文本的文件，命名为 `translated_text.txt`，并放置在同一目录中。
3. 运行脚本：

   ```
   python main.py
   ```

4. 脚本将提取字幕文本并保存到 `extracted_text.txt`，然后生成翻译后的 SRT 文件 `translated_1.srt`。

### 示例
同时该脚本支持将srt文件的字幕以文本形式导出，运行第一遍即可导出文本，翻译玩文本后，再运行一遍之后即可合并原字幕（再执行一切操作之前，请备份！！！）

假设 `1.srt` 文件内容如下：

```
1
00:00:01,000 --> 00:00:05,000
Hello, world!

2
00:00:06,000 --> 00:00:10,000
This is a subtitle example.
```

在 `translated_text.txt` 中，你可以提供翻译后的文本：

```
你好，世界！
这是一个字幕示例。
```

运行脚本后，将生成 `translated_1.srt`，内容如下：

```
1
00:00:01,000 --> 00:00:05,000
你好，世界！

2
00:00:06,000 --> 00:00:10,000
这是一个字幕示例。
```

## 注意事项

- 确保 SRT 文件和翻译文本文件的编码为 UTF-8。
- 翻译文本的行数应与提取的字幕行数相匹配，以确保生成的 SRT 文件正确。

## 许可证

本项目使用 MIT 许可证。有关详细信息，请查看 [LICENSE](LICENSE) 文件。

## 贡献

欢迎任何形式的贡献！请提交问题或拉取请求。
