# Virtual Try-On Skill

虚拟换装 - 使用 AI 技术将服装合成到人物图像上。

## 推荐方案

### WeShopAI Virtual Try-On ⭐

实测可用，免费，无需 GPU。

```python
from gradio_client import Client, handle_file
import os

os.environ['HTTP_PROXY'] = 'http://127.0.0.1:7897'
os.environ['HTTPS_PROXY'] = 'http://127.0.0.1:7897'

client = Client("WeShopAI/WeShopAI-Virtual-Try-On", verbose=False)

result = client.predict(
    main_image=handle_file("person.jpg"),
    background_image=handle_file("garment.jpg"),
    api_name="/generate_image"
)
```

## 安装

```bash
# 复制到 Hermes skills 目录
cp -r . ~/.hermes/skills/image-processing/virtual-try-on/
```

## 详细文档

见 [SKILL.md](./SKILL.md)
