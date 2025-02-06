# UltraService 

## 简介

UltraService 是一个基于 Python 的轻量级 Web 框架，旨在帮助开发者快速构建小而全的异步 Web 服务。它结合了 Tornado 的高性能异步处理能力和 PyWebIO 的简洁交互式界面，支持 HTTPS，适合用于快速开发和部署小型 Web 应用。

## 特性

- **异步处理**：基于 Tornado 的异步 I/O 模型，支持高并发请求处理。
- **简洁易用**：集成 PyWebIO，提供简洁的 API 快速构建交互式 Web 界面。
- **HTTPS 支持**：内置 HTTPS 支持，确保数据传输的安全性。
- **轻量级**：代码简洁，依赖少，易于集成到现有项目中。
- **快速开发**：提供丰富的示例和模板，帮助开发者快速上手。



## 快速开始

以下是一个简单的示例，展示如何使用 UltraService创建Web服务来相应一个HTTP/POST请求：

```python
import tornado.gen
from core.ultraservice import UltraService, CallHandler

class Service(UltraService):

    @CallHandler.route("/hello")
    async def _hello(self, data: dict):
        await tornado.gen.sleep(3)
        return "hello, world!"
```

### 运行服务

```
python main.py
```



## 作者

- **Feng Song** - [GitHub](https://github.com/franksongfeng)

## 致谢

- [Tornado](https://www.tornadoweb.org/) - 高性能 Python Web 框架。
- [PyWebIO](https://pywebio.readthedocs.io/) - 用于构建交互式 Web 应用的 Python 库。
