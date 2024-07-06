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
- Unsloth
- Other LLM Tools

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
|**舉例**|`llama3` `gemma2` `phi3`|`gpt4o` `sonnet`|

---

![w:1200](/asset/img/history.png)

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
> `B` = `Billion` 十億，代表模型參數(Parameters)數量，例如 GPT-3 為 `175B`

---

![bg left:30%](https://picsum.photos/720?image=936)

# **O**llama - CLI
###

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
###

>其他指令操作可參考[線上說明](https://github.com/ollama/ollama?tab=readme-ov-file#cli-reference)

---

![bg right:30%](https://picsum.photos/720?image=933)

# **O**llama - API

###

```sh
# 使用 curl 呼叫 API

curl -X POST http://localhost:11434/api/generate -d '{
  "model": "llama3",
  "prompt":"Why is the sky blue?"
 }'
```

###

- 詳細 API 端點資訊請 [參考文件](https://github.com/ollama/ollama/blob/main/docs/api.md)
- 也可使用 `Postman` 或 `*.http` 測試

###

>💡其他應用程式可透過 API 與 model 互動

---

![bg right:50%](https://picsum.photos/720?image=970)

# Open Web**UI**

https://openwebui.com/

- 支援 Ollama = 可用開源 LLM
- 支援 OpenAI = 可用 GPT4o
- 類似 ChatGPT，學習曲線低
- 支援檔案上傳、檔案管理保存
- 支援RAG，可搜尋網頁或檔案
- 可自訂 AI 模型(類似GPTs)
- 支援語音輸入與輸出
- 支援多模型提問
- 可上傳自訓練模型(GGUF)

---

<!-- _class: invert -->

![bg fit](../asset/img/demoOpenWebUI.png)

---

![bg left:20%](https://picsum.photos/720?image=912)

# RAG **vs** Fine-Tuning

🧑‍🎨`小明`收藏了整套哈利波特，整套閱讀過，大概知道章節與內容

👩‍🦰`小美`熟讀了整套哈利波特，內容到背如流，後來將書捐贈出售

👨`小華`請教🧑‍🎨`小明`哈利波特問題，🧑‍🎨`小明`快速翻閱書籍找到答案

👨`小華`請教👩‍🦰`小美`哈利波特問題，👩‍🦰`小美`不加思索立刻回答

🧑‍🎨`小明`就是 **RAG** (Retrieval-Augmented Generation)

👩‍🦰`小美`就是 **Fine-Tuning**

###

>直到 J.K.羅琳 決定推出哈利波特前傳系列叢書.... 🧑‍🎨 vs 👩‍🦰

---

![bg right:40%](https://picsum.photos/720?image=915)

![w:400](../asset/img/unsloth.png)

https://unsloth.ai/

- 快速微調和訓練 LLM 的開源工具
- 訓練速度較其它工具快，使用記憶體低
- 支援 `NVIDIA` `AMD` `Intel` 等 GPU
- 在 Google Colab 即可免費訓練*
- GGUF 可導入 OpenWebUI 使用

###

> *⚠️僅限單CPU，模型也不能太大

---

<!-- _class: invert -->

![bg fit](../asset/img/demoUnsloth.png)

---

![bg right:50%](https://picsum.photos/720?image=949)

# Fine-**Tuning**