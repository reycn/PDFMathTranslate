<div align="center">

英语 |[简体中文](docs/README_zh-CN.md)\|[日本人](docs/README_ja-JP.md)

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

PDF scientific paper translation and bilingual comparison.

-   📊 保留公式、图表、目录和注释_([预览](#preview))_.
-   🌐支持[多种语言](#language)，且多样化[翻译服务](#services).
-   🤖 提供[命令行工具](#usage),[交互式用户界面](#gui)， 和[码头工人](#docker)

请随时提供反馈[GitHub 问题](https://github.com/Byaidu/PDFMathTranslate/issues),[电报群](https://t.me/+Z9_SgnxmsmA5NzBl)或者[QQ群](https://qm.qq.com/q/DixZCxQej0).

<h2 id="updates">Updates</h2>

-   [2024 年 12 月 19 日.]现在支持使用非 PDF/A 文档`-cp`_（经过[@reycn](https://github.com/reycn))_
-   [2024 年 12 月 13 日.]对后端的额外支持_（经过[@YadominJinta](https://github.com/YadominJinta))_
-   [2024 年 12 月 10 日.]翻译器现在支持 Azure 上的 OpenAI 模型_（经过[@yidasanqian](https://github.com/yidasanqian))_

<h2 id="preview">Preview</h2>

<div align="center">
<img src="./docs/images/preview.gif" width="80%"/>
</div>

<h2 id="demo">Online Service 🌟</h2>

您可以使用以下演示来尝试我们的应用程序：

-   [公共免费服务](https://pdf2zh.com/)无需安装即可在线使用_（受到推崇的）_.
-   [演示托管在 HuggingFace 上](https://huggingface.co/spaces/reycn/PDFMathTranslate-Docker)
-   [ModelScope 上托管的演示](https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate)无需安装。

请注意，该演示的计算资源是有限的，因此请避免滥用它们。

<h2 id="install">Installation and Usage</h2>

### 方法

对于不同的用例，我们提供了四种不同的方法来使用我们的程序：

<details open>
  <summary>1. Commandline</summary>

1.  已安装 Python（3.8 &lt;= 版本 &lt;= 3.12）

2.  安装我们的包：

    ```bash
    pip install pdf2zh
    ```

3.  执行翻译，生成文件[当前工作目录](https://chatgpt.com/share/6745ed36-9acc-800e-8a90-59204bd13444):

    ```bash
    pdf2zh document.pdf
    ```

</details>

<details>
  <summary>2. Portable (w/o Python installed)</summary>

1.  下载[安装程序](https://raw.githubusercontent.com/Byaidu/PDFMathTranslate/refs/heads/main/script/setup.bat)

2.  双击运行。

</details>

<details>
  <summary>3. Graphic user interface</summary>
1. Python installed (3.8 <= version <= 3.12)
2. Install our package:

```bash
pip install pdf2zh
```

3.  开始在浏览器中使用：

    ```bash
    pdf2zh -i
    ```

4.  如果您的浏览器没有自动启动，请转到

    ```bash
    http://localhost:7860/
    ```

    <img src="./docs/images/gui.gif" width="500"/>

看[图形用户界面文档](./docs/README_GUI.md)了解更多详情。

</details>

<details>
  <summary>4. Docker</summary>

1.  拉动并运行：

    ```bash
    docker pull byaidu/pdf2zh
    docker run -d -p 7860:7860 byaidu/pdf2zh
    ```

2.  在浏览器中打开：

        http://localhost:7860/

对于云服务上的docker部署：

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

### 无法安装？

目前的程序需要一个AI模型（`wybxc/DocLayout-YOLO-DocStructBench-onnx`）在工作之前，有些用户由于网络问题无法下载。如果您在下载此模型时遇到问题，我们提供使用以下环境变量的解决方法：

```shell
set HF_ENDPOINT=https://hf-mirror.com
```

如果该解决方案对您不起作用/您遇到其他问题，请参阅[常见问题](https://github.com/Byaidu/PDFMathTranslate/wiki#-faq--%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98).

<h2 id="usage">Advanced Options</h2>

在命令行中执行翻译命令，生成翻译后的文档`example-mono.pdf`和双语文件`example-dual.pdf`在当前工作目录中。使用 Google 作为默认翻译服务。

<img src="./docs/images/cmd.explained.png" width="580px"  alt="cmd"/>

在下表中，我们列出了所有高级选项以供参考：

| 选项             | 功能                                                                                       | 例子                                             |
| -------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------- |
| 文件             | 本地文件                                                                                     | `pdf2zh ~/local.pdf`                           |
| 链接             | 在线文件                                                                                     | `pdf2zh http://arxiv.org/paper.pdf`            |
| `-i`           | [进入图形用户界面](#gui)                                                                         | `pdf2zh -i`                                    |
| `-p`           | [部分文件翻译](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#partial)  | `pdf2zh example.pdf -p 1`                      |
| `-li`          | [源语言](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)   | `pdf2zh example.pdf -li en`                    |
| `-lo`          | [目标语言](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)  | `pdf2zh example.pdf -lo zh`                    |
| `-s`           | [翻译服务](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#services)   | `pdf2zh example.pdf -s deepl`                  |
| `-t`           | [多线程](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#threads)     | `pdf2zh example.pdf -t 1`                      |
| `-o`           | 输出方向                                                                                     | `pdf2zh example.pdf -o output`                 |
| `-f`,`-c`      | [例外情况](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#exceptions) | `pdf2zh example.pdf -f "(MS.*)"`               |
| `-cp`          | 兼容模式                                                                                     | `pdf2zh example.pdf --compatible`              |
| `--share`      | 公共链接                                                                                     | `pdf2zh -i --share`                            |
| `--authorized` | 授权                                                                                       | `pdf2zh -i --authorized users.txt [auth.html]` |
| `--prompt`     | [自定义提示](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#prompt)    | `pdf2zh --prompt [prompt.txt]`                 |

详细的解释请参考我们的文档[高级用法](./docs/ADVANCED.md)了解每个选项的完整列表。

<h2 id="downstream">Secondary Development (APIs)</h2>

对于下游应用，请参阅我们的文档[接口详情](./docs/APIS.md)欲了解更多信息：

-   [Python API](./docs/APIS.md#api-python)、如何在其他Python程序中使用该程序
-   [HTTP API](./docs/APIS.md#api-http), 如何与安装了程序的服务器进行通信

<h2 id="todo">TODOs</h2>

-   [ ] Parse layout with DocLayNet based models, [桨X](https://github.com/PaddlePaddle/PaddleX/blob/17cc27ac3842e7880ca4aad92358d3ef8555429a/paddlex/repo_apis/PaddleDetection_api/object_det/official_categories.py#L81),[纸法师](https://github.com/allenai/papermage/blob/9cd4bb48cbedab45d0f7a455711438f1632abebe/README.md?plain=1#L102),[萨玛](https://github.com/facebookresearch/sam2)

-   [ ] 修复页面旋转、目录、列表格式

-   [ ] 修复旧论文中的像素公式

-   [ ] 除键盘中断外的异步重试

-   [ ] 西方语言的 Knuth–Plas 算法

-   [ ] 支持非 PDF/A 文件

-   [ ] 的插件[所以](https://github.com/zotero/zotero)和[黑曜石](https://github.com/obsidianmd/obsidian-releases)

<h2 id="acknowledgement">Acknowledgements</h2>

-   文档合并：[PyMuPDF](https://github.com/pymupdf/PyMuPDF)

-   文档解析：[PDFminer.6](https://github.com/pdfminer/pdfminer.six)

-   文档提取：[米内尔](https://github.com/opendatalab/MinerU)

-   多线程翻译：[数学翻译](https://github.com/SUSYUSTC/MathTranslate)

-   布局解析：[DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)

-   文件标准：[PDF 解释](https://zxyle.github.io/PDF-Explained/),[PDF 备忘单](https://pdfa.org/resource/pdf-cheat-sheets/)

-   多语言字体：[去能登环球影城](https://github.com/satbyy/go-noto-universal)

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
