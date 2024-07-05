---
marp: true
paginate: true
footer: Edge `AI`
---

<!-- _class: invert -->

![bg](https://picsum.photos/720?image=202&blur=5)


# Edge AI ✨
###
```powershell
🤖 AI processing on local devices
```

##### `OAD` **brian_li**

---

![bg left:60%](https://picsum.photos/720?image=998)

# **A**genda

- Edge AI
- Open Source Model
- Ollama
- Open WebUI
- Fine-Tuning

---

![bg right:50%](https://picsum.photos/720?image=967)

# Edge **AI**

###### 允許數據在**本地**進行處理，而不需傳輸到雲端服務
###
- 低延遲：即時反應
- 安全性：本地處理數據
- 可靠性：網絡中斷仍可運行
###
⚠️ 性能表現依賴本地設備

---

![bg left:30%](https://picsum.photos/720?image=953)

# Open Source **vs** Close Models

|特點|開源模型|閉源模型|
|:-:|:-:|:-:|
|**可用性**|免費、公開|需購買或授權|
|**擴充性**|可自由修改、擴展|依賴提供者|
|**透明度**|高，公開源碼|低，不公開|
|**安全性**|可檢查漏洞|依賴提供者|
|**社群支援**|大量社群、更新快|無|
|**依賴性**|不依賴單一提供者|高度依賴提供者|
|**舉例**|llama3、gemma2、phi3|gpt4o、sonnet|

---

![bg right:50%](https://picsum.photos/720?image=988)

# **O**llama ![h:100](/asset/img/ollama.png)

https://ollama.com/

- 一個開源工具
- 允許在本地運行各種開源 LLM
- 支援 GPU 加速 (如果有)
- 允許微調模型或創建自定義模型
- 支援 CLI 操作
- 提供 REST API

---

# 常見**開源**模型

|![h:100](/asset/img/meta.png)|![h:100](/asset/img/mistrel.png)|![h:120](/asset/img/gemma.webp)|![h:180](/asset/img/phi3.png)|![h:100](/asset/img/qwen.png)|
|:-:|:-:|:-:|:-:|:-:|
|Meta|Mistrel AI|Google|Microsoft|Alibaba|
|**llama3**|**mistral**|**gemma2**|**phi3**|**qwen2**|
|`8B` `70B`|`7B`|`9B` `27B`|`3B` `14B`|`0.5B` `1.5B` `7B` `72B`|
###
> `B` = `Billion` 表示模型參數(Parameters)，越高表現越佳，GPT-3 為 `175B`
---

![bg left:30%](https://picsum.photos/720?image=936)

# **O**llama - CLI

```sh
# 檢視版本
ollama -v

# 下載模型，如需指定參數請用例如 llama3:8b
ollama pull llama3

# 與 AI 互動
ollama run llama3 "Why is the sky blue?"

# 其他指令查詢
ollama -h
```

---

![bg right:50%](https://picsum.photos/720?image=970)

# Open Web**UI**

---

![bg right:50%](https://picsum.photos/720?image=959)

# Demo

---

![bg right:50%](https://picsum.photos/720?image=949)

# Fine-**Tuning**