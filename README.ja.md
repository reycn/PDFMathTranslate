<div align="center">

英語 |[簡体字中国語](docs/README_zh-CN.md)\|[日本語](docs/README_ja-JP.md)

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

PDF 科学論文の翻訳と対訳比較。

-   📊 数式、チャート、目次、注釈を保存_([プレビュー](#preview))_.
-   🌐 サポート[多言語](#language)、そして多様です[翻訳サービス](#services).
-   🤖 提供するもの[コマンドラインツール](#usage),[インタラクティブなユーザーインターフェイス](#gui)、 そして[ドッカー](#docker)

お気軽にフィードバックをお寄せください[GitHubの問題](https://github.com/Byaidu/PDFMathTranslate/issues),[電報グループ](https://t.me/+Z9_SgnxmsmA5NzBl)または[QQグループ](https://qm.qq.com/q/DixZCxQej0).

<h2 id="updates">Updates</h2>

-   [2024 年 12 月 19 日.]非 PDF/A ドキュメントがサポートされるようになりました。`-cp`_（による[@reycn](https://github.com/reycn))_
-   [2024 年 12 月 13 日.]バックエンドの追加サポート_（による[@やどみんじんた](https://github.com/YadominJinta))_
-   [2024 年 12 月 10 日.]トランスレータは Azure 上の OpenAI モデルをサポートするようになりました_（による[@は3000人に達しました](https://github.com/yidasanqian))_

<h2 id="preview">Preview</h2>

<div align="center">
<img src="./docs/images/preview.gif" width="80%"/>
</div>

<h2 id="demo">Online Service 🌟</h2>

次のいずれかのデモを使用して、アプリケーションを試すことができます。

-   [公開無料サービス](https://pdf2zh.com/)インストールせずにオンラインで_（推奨）_.
-   [デモはHuggingFaceでホストされています](https://huggingface.co/spaces/reycn/PDFMathTranslate-Docker)
-   [ModelScope でホストされるデモ](https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate)インストールなしで。

デモのコンピューティング リソースには限りがあるため、乱用は避けてください。

<h2 id="install">Installation and Usage</h2>

### メソッド

さまざまなユースケースに合わせて、プログラムを使用するための 4 つの異なる方法が提供されています。

<details open>
  <summary>1. Commandline</summary>

1.  Python がインストールされている (3.8 &lt;= バージョン &lt;= 3.12)

2.  パッケージをインストールします。

    ```bash
    pip install pdf2zh
    ```

3.  翻訳を実行し、ファイルが生成される[現在の作業ディレクトリ](https://chatgpt.com/share/6745ed36-9acc-800e-8a90-59204bd13444):

    ```bash
    pdf2zh document.pdf
    ```

</details>

<details>
  <summary>2. Portable (w/o Python installed)</summary>

1.  ダウンロード[setup.bat](https://raw.githubusercontent.com/Byaidu/PDFMathTranslate/refs/heads/main/script/setup.bat)

2.  ダブルクリックして実行します。

</details>

<details>
  <summary>3. Graphic user interface</summary>
1. Python installed (3.8 <= version <= 3.12)
2. Install our package:

```bash
pip install pdf2zh
```

3.  ブラウザで使用を開始します。

    ```bash
    pdf2zh -i
    ```

4.  ブラウザが自動的に起動しない場合は、次へ進んでください。

    ```bash
    http://localhost:7860/
    ```

    <img src="./docs/images/gui.gif" width="500"/>

見る[GUIのドキュメント](./docs/README_GUI.md)詳細については。

</details>

<details>
  <summary>4. Docker</summary>

1.  プルして実行します。

    ```bash
    docker pull byaidu/pdf2zh
    docker run -d -p 7860:7860 byaidu/pdf2zh
    ```

2.  ブラウザで開きます:

        http://localhost:7860/

クラウド サービスでの Docker デプロイメントの場合:

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

### インストールできないのですか？

現在のプログラムには AI モデルが必要です(`wybxc/DocLayout-YOLO-DocStructBench-onnx`) 作業する前に、一部のユーザーはネットワークの問題によりダウンロードできません。このモデルのダウンロードで問題が発生した場合は、次の環境変数を使用した回避策が提供されます。

```shell
set HF_ENDPOINT=https://hf-mirror.com
```

解決策がうまくいかない場合、または他の問題が発生した場合は、を参照してください。[よくある質問](https://github.com/Byaidu/PDFMathTranslate/wiki#-faq--%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98).

<h2 id="usage">Advanced Options</h2>

コマンドラインで翻訳コマンドを実行して、翻訳されたドキュメントを生成します。`example-mono.pdf`そしてそのバイリンガル文書`example-dual.pdf`現在の作業ディレクトリ内。 Google をデフォルトの翻訳サービスとして使用します。

<img src="./docs/images/cmd.explained.png" width="580px"  alt="cmd"/>

次の表に、参照用にすべての詳細オプションを示します。

| オプション          | 関数                                                                                        | 例                                              |
| -------------- | ----------------------------------------------------------------------------------------- | ---------------------------------------------- |
| ファイル           | ローカルファイル                                                                                  | `pdf2zh ~/local.pdf`                           |
| リンク            | オンラインファイル                                                                                 | `pdf2zh http://arxiv.org/paper.pdf`            |
| `-i`           | [GUIの入力](#gui)                                                                            | `pdf2zh -i`                                    |
| `-p`           | [部分的な文書翻訳](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#partial) | `pdf2zh example.pdf -p 1`                      |
| `-li`          | [ソース言語](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)  | `pdf2zh example.pdf -li en`                    |
| `-lo`          | [対象言語](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)   | `pdf2zh example.pdf -lo zh`                    |
| `-s`           | [翻訳サービス](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#services)  | `pdf2zh example.pdf -s deepl`                  |
| `-t`           | [マルチスレッド](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#threads)  | `pdf2zh example.pdf -t 1`                      |
| `-o`           | 出力ディレクトリ                                                                                  | `pdf2zh example.pdf -o output`                 |
| `-f`,`-c`      | [例外](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#exceptions)    | `pdf2zh example.pdf -f "(MS.*)"`               |
| `-cp`          | 互換モード                                                                                     | `pdf2zh example.pdf --compatible`              |
| `--share`      | パブリックリンク                                                                                  | `pdf2zh -i --share`                            |
| `--authorized` | 認可                                                                                        | `pdf2zh -i --authorized users.txt [auth.html]` |
| `--prompt`     | [カスタムプロンプト](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#prompt) | `pdf2zh --prompt [prompt.txt]`                 |

詳細な説明については、当社のドキュメントを参照してください。[高度な使用法](./docs/ADVANCED.md)各オプションの完全なリストについては、

<h2 id="downstream">Secondary Development (APIs)</h2>

ダウンストリームアプリケーションについては、当社のドキュメントを参照してください。[APIの詳細](./docs/APIS.md)詳細については、以下を参照してください。

-   [Python API](./docs/APIS.md#api-python)、他の Python プログラムでプログラムを使用する方法
-   [HTTP API](./docs/APIS.md#api-http)、プログラムがインストールされたサーバーと通信する方法

<h2 id="todo">TODOs</h2>

-   [ ] DocLayNet ベースのモデルでレイアウトを解析し、[パドルX](https://github.com/PaddlePaddle/PaddleX/blob/17cc27ac3842e7880ca4aad92358d3ef8555429a/paddlex/repo_apis/PaddleDetection_api/object_det/official_categories.py#L81),[ペーパーメイジ](https://github.com/allenai/papermage/blob/9cd4bb48cbedab45d0f7a455711438f1632abebe/README.md?plain=1#L102),[サマ](https://github.com/facebookresearch/sam2)

-   [ ] ページの回転、目次、リストの形式を修正

-   [ ] 古い論文のピクセル数式を修正

-   [ ] KeyboardInterrupt を除く非同期再試行

-   [ ] 西欧言語用の Knuth-Plas アルゴリズム

-   [ ] 非 PDF/A ファイルのサポート

-   [ ] のプラグイン[それで](https://github.com/zotero/zotero)そして[黒曜石](https://github.com/obsidianmd/obsidian-releases)

<h2 id="acknowledgement">Acknowledgements</h2>

-   文書の結合:[PyMuPDF](https://github.com/pymupdf/PyMuPDF)

-   文書の解析:[PDFminer.6](https://github.com/pdfminer/pdfminer.six)

-   ドキュメントの抽出:[MinerU](https://github.com/opendatalab/MinerU)

-   マルチスレッド翻訳:[数学翻訳](https://github.com/SUSYUSTC/MathTranslate)

-   レイアウト解析:[DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)

-   文書規格:[PDF の説明](https://zxyle.github.io/PDF-Explained/),[PDF チートシート](https://pdfa.org/resource/pdf-cheat-sheets/)

-   多言語フォント:[Go能登ユニバーサル](https://github.com/satbyy/go-noto-universal)

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
