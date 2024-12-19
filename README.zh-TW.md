<div align="center">

英語 |[簡體中文](docs/README_zh-CN.md)\|[日本人](docs/README_ja-JP.md)

<img src="./docs/images/banner.png" width="320px"  alt="PDF2ZH"/>

<h2 id="title">PDFMathTranslate</h2>

<p>
  <!-- PyPI -->
  <a href="https://pypi.org/project/pdf2zh/">
    <img src="https://img.shields.io/pypi/v/pdf2zh"></a>
  <a href="https://pepy.tech/projects/pdf2zh">
    <img src="https://static.pepy.tech/badge/pdf2zh"></a>
  <a href="https://hub.docker.com/repository/docker/byaidu/pdf2zh">
    <img src="https://img.shields.io/docker/pulls/byaidu/pdf2zh"></a>
  <a href="https://gitcode.com/Byaidu/PDFMathTranslate/overview">
    <img src="https://gitcode.com/Byaidu/PDFMathTranslate/star/badge.svg"></a>
  <a href="https://huggingface.co/spaces/reycn/PDFMathTranslate-Docker">
    <img src="https://img.shields.io/badge/%F0%9F%A4%97-Online%20Demo-FF9E0D"></a>
  <a href="https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate">
    <img src="https://img.shields.io/badge/ModelScope-Demo-blue"></a>
  <a href="https://github.com/Byaidu/PDFMathTranslate/pulls">
    <img src="https://img.shields.io/badge/contributions-welcome-green"></a>
  <a href="https://t.me/+Z9_SgnxmsmA5NzBl">
    <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=flat-squeare&logo=telegram&logoColor=white"></a>
  <!-- License -->
  <a href="./LICENSE">
    <img src="https://img.shields.io/github/license/Byaidu/PDFMathTranslate"></a>
</p>

<a href="https://trendshift.io/repositories/12424" target="_blank"><img src="https://trendshift.io/api/badge/repositories/12424" alt="Byaidu%2FPDFMathTranslate | Trendshift" style="width: 250px; height: 55px;" width="250" height="55"/></a>

</div>

PDF科技論文翻譯及雙語比較。

-   📊 保留公式、圖表、目錄和註釋_([預覽](#preview))_.
-   🌐支持[多種語言](#language)，且多樣化[翻譯服務](#services).
-   🤖 提供[命令列工具](#usage),[互動式使用者介面](#gui)， 和[碼頭工人](#docker)

請隨時提供回饋[GitHub 問題](https://github.com/Byaidu/PDFMathTranslate/issues),[電報群](https://t.me/+Z9_SgnxmsmA5NzBl)或者[QQ群](https://qm.qq.com/q/DixZCxQej0).

<h2 id="updates">Updates</h2>

-   [2024 年 12 月 19 日.]現在支援使用非 PDF/A 文檔`-cp`_（經過[@reycn](https://github.com/reycn))_
-   [2024 年 12 月 13 日.]對後端的額外支持_（經過[@YadominJinta](https://github.com/YadominJinta))_
-   [2024 年 12 月 10 日.]翻譯器現在支援 Azure 上的 OpenAI 模型_（經過[@已達三千](https://github.com/yidasanqian))_

<h2 id="preview">Preview</h2>

<div align="center">
<img src="./docs/images/preview.gif" width="80%"/>
</div>

<h2 id="demo">Online Service 🌟</h2>

您可以使用以下演示來嘗試我們的應用程式：

-   [公共免費服務](https://pdf2zh.com/)無需安裝即可在線使用_（受到推崇的）_.
-   [演示託管在 HuggingFace 上](https://huggingface.co/spaces/reycn/PDFMathTranslate-Docker)
-   [ModelScope 上託管的演示](https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate)無需安裝。

請注意，該演示的計算資源是有限的，因此請避免濫用它們。

<h2 id="install">Installation and Usage</h2>

### 方法

對於不同的用例，我們提供了四種不同的方法來使用我們的程式：

<details open>
  <summary>1. Commandline</summary>

1.  已安裝 Python（3.8 &lt;= 版本 &lt;= 3.12）

2.  安裝我們的套件：

    ```bash
    pip install pdf2zh
    ```

3.  執行翻譯，產生文件[目前工作目錄](https://chatgpt.com/share/6745ed36-9acc-800e-8a90-59204bd13444):

    ```bash
    pdf2zh document.pdf
    ```

</details>

<details>
  <summary>2. Portable (w/o Python installed)</summary>

1.  下載[安裝程式](https://raw.githubusercontent.com/Byaidu/PDFMathTranslate/refs/heads/main/script/setup.bat)

2.  雙擊運行。

</details>

<details>
  <summary>3. Graphic user interface</summary>
1. Python installed (3.8 <= version <= 3.12)
2. Install our package:

```bash
pip install pdf2zh
```

3.  開始在瀏覽器中使用：

    ```bash
    pdf2zh -i
    ```

4.  如果您的瀏覽器沒有自動啟動，請前往

    ```bash
    http://localhost:7860/
    ```

    <img src="./docs/images/gui.gif" width="500"/>

看[圖形使用者介面文檔](./docs/README_GUI.md)了解更多詳情。

</details>

<details>
  <summary>4. Docker</summary>

1.  拉動並運行：

    ```bash
    docker pull byaidu/pdf2zh
    docker run -d -p 7860:7860 byaidu/pdf2zh
    ```

2.  在瀏覽器中開啟：

        http://localhost:7860/

對於雲端服務上的docker部署：

<div>
<a href="https://www.heroku.com/deploy?template=https://github.com/Byaidu/PDFMathTranslate">
  <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy" height="26"></a>
<a href="https://render.com/deploy">
  <img src="https://render.com/images/deploy-to-render-button.svg" alt="Deploy to Koyeb" height="26"></a>
<a href="https://zeabur.com/templates/5FQIGX?referralCode=reycn">
  <img src="https://zeabur.com/button.svg" alt="Deploy on Zeabur" height="26"></a>
<a href="https://app.koyeb.com/deploy?type=git&builder=buildpack&repository=github.com/Byaidu/PDFMathTranslate&branch=main&name=pdf-math-translate">
  <img src="https://www.koyeb.com/static/images/deploy/button.svg" alt="Deploy to Koyeb" height="26"></a>
</div>

</details>

### 無法安裝？

目前的程式需要一個AI模型（`wybxc/DocLayout-YOLO-DocStructBench-onnx`）在工作之前，有些用戶因為網路問題無法下載。如果您在下載此模型時遇到問題，我們提供使用以下環境變數的解決方法：

```shell
set HF_ENDPOINT=https://hf-mirror.com
```

如果該解決方案對您不起作用/您遇到其他問題，請參閱[常見問題](https://github.com/Byaidu/PDFMathTranslate/wiki#-faq--%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98).

<h2 id="usage">Advanced Options</h2>

在命令列中執行翻譯命令，產生翻譯後的文檔`example-mono.pdf`和雙語文件`example-dual.pdf`在目前工作目錄中。使用 Google 作為預設翻譯服務。

<img src="./docs/images/cmd.explained.png" width="580px"  alt="cmd"/>

在下表中，我們列出了所有進階選項以供參考：

| 選項             | 功能                                                                                       | 例子                                             |
| -------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------- |
| 文件             | 本地文件                                                                                     | `pdf2zh ~/local.pdf`                           |
| 連結             | 線上文件                                                                                     | `pdf2zh http://arxiv.org/paper.pdf`            |
| `-i`           | [進入圖形使用者介面](#gui)                                                                        | `pdf2zh -i`                                    |
| `-p`           | [部分文件翻譯](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#partial)  | `pdf2zh example.pdf -p 1`                      |
| `-li`          | [原始語言](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)  | `pdf2zh example.pdf -li en`                    |
| `-lo`          | [目標語言](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)  | `pdf2zh example.pdf -lo zh`                    |
| `-s`           | [翻譯服務](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#services)   | `pdf2zh example.pdf -s deepl`                  |
| `-t`           | [多執行緒](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#threads)    | `pdf2zh example.pdf -t 1`                      |
| `-o`           | 輸出方向                                                                                     | `pdf2zh example.pdf -o output`                 |
| `-f`,`-c`      | [例外情況](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#exceptions) | `pdf2zh example.pdf -f "(MS.*)"`               |
| `-cp`          | 相容模式                                                                                     | `pdf2zh example.pdf --compatible`              |
| `--share`      | 公共連結                                                                                     | `pdf2zh -i --share`                            |
| `--authorized` | 授權                                                                                       | `pdf2zh -i --authorized users.txt [auth.html]` |
| `--prompt`     | [自訂提示](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#prompt)     | `pdf2zh --prompt [prompt.txt]`                 |

詳細的解釋請參考我們的文檔[進階用法](./docs/ADVANCED.md)了解每個選項的完整清單。

<h2 id="downstream">Secondary Development (APIs)</h2>

對於下游應用，請參閱我們的文檔[介面詳情](./docs/APIS.md)欲了解更多：

-   [Python API](./docs/APIS.md#api-python)、如何在其他Python程式中使用該程式
-   [HTTP API](./docs/APIS.md#api-http), 如何與安裝了程式的伺服器進行通信

<h2 id="todo">TODOs</h2>

-   [ ] 使用基於 DocLayNet 的模型解析佈局，[槳X](https://github.com/PaddlePaddle/PaddleX/blob/17cc27ac3842e7880ca4aad92358d3ef8555429a/paddlex/repo_apis/PaddleDetection_api/object_det/official_categories.py#L81),[紙法師](https://github.com/allenai/papermage/blob/9cd4bb48cbedab45d0f7a455711438f1632abebe/README.md?plain=1#L102),[薩瑪](https://github.com/facebookresearch/sam2)

-   [ ] 修復頁面旋轉、目錄、列表格式

-   [ ] 修復舊論文中的像素公式

-   [ ] 除鍵盤中斷外的非同步重試

-   [ ] 西方語言的 Knuth–Plas 演算法

-   [ ] 支援非 PDF/A 文件

-   [ ] 的插件[所以](https://github.com/zotero/zotero)和[黑曜石](https://github.com/obsidianmd/obsidian-releases)

<h2 id="acknowledgement">Acknowledgements</h2>

-   文檔合併：[PyMuPDF](https://github.com/pymupdf/PyMuPDF)

-   文件解析：[PDFminer.6](https://github.com/pdfminer/pdfminer.six)

-   文檔擷取：[米內爾](https://github.com/opendatalab/MinerU)

-   多線程翻譯：[數學翻譯](https://github.com/SUSYUSTC/MathTranslate)

-   佈局解析：[DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)

-   文件標準：[PDF 解釋](https://zxyle.github.io/PDF-Explained/),[PDF 備忘錄](https://pdfa.org/resource/pdf-cheat-sheets/)

-   多語言字體：[去能登環球影城](https://github.com/satbyy/go-noto-universal)

<h2 id="contrib">Contributors</h2>

<a href="https://github.com/Byaidu/PDFMathTranslate/graphs/contributors">
  <img src="https://opencollective.com/PDFMathTranslate/contributors.svg?width=890&button=false" />
</a>

![Alt](https://repobeats.axiom.co/api/embed/dfa7583da5332a11468d686fbd29b92320a6a869.svg "Repobeats analytics image")

<h2 id="star_hist">Star History</h2>

<a href="https://star-history.com/#Byaidu/PDFMathTranslate&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=Byaidu/PDFMathTranslate&type=Date"/>
 </picture>
</a>
