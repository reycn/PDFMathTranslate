<div align="center">

Anglais |[Chinois simplifié](docs/README_zh-CN.md)\|[japonais](docs/README_ja-JP.md)

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

Traduction d'articles scientifiques PDF et comparaison bilingue.

-   📊 Conservez les formules, les graphiques, la table des matières et les annotations_([aperçu](#preview))_.
-   🌐 Soutien[plusieurs langues](#language), et diversifié[services de traduction](#services).
-   🤖 Fournit[outil de ligne de commande](#usage),[interface utilisateur interactive](#gui), et[Docker](#docker)

N'hésitez pas à donner votre avis dans[Problèmes GitHub](https://github.com/Byaidu/PDFMathTranslate/issues),[Groupe de télégrammes](https://t.me/+Z9_SgnxmsmA5NzBl)ou[Groupe QQ](https://qm.qq.com/q/DixZCxQej0).

<h2 id="updates">Updates</h2>

-   [19 décembre 2024.]Les documents non PDF/A sont désormais pris en charge à l'aide de`-cp`_(par[@reycn](https://github.com/reycn))_
-   [13 décembre 2024.]Prise en charge supplémentaire du backend par_(par[@YaminJinta](https://github.com/YadominJinta))_
-   [10 décembre 2024.]Le traducteur prend désormais en charge les modèles OpenAI sur Azure_(par[@a atteint trois mille](https://github.com/yidasanqian))_

<h2 id="preview">Preview</h2>

<div align="center">
<img src="./docs/images/preview.gif" width="80%"/>
</div>

<h2 id="demo">Online Service 🌟</h2>

Vous pouvez essayer notre application en utilisant l'une des démos suivantes :

-   [Service public gratuit](https://pdf2zh.com/)en ligne sans installation_(recommandé)_.
-   [Démo hébergée sur HuggingFace](https://huggingface.co/spaces/reycn/PDFMathTranslate-Docker)
-   [Démo hébergée sur ModelScope](https://www.modelscope.cn/studios/AI-ModelScope/PDFMathTranslate)sans installation.

Notez que les ressources informatiques de la démo sont limitées, évitez donc d'en abuser.

<h2 id="install">Installation and Usage</h2>

### Méthodes

Pour différents cas d'utilisation, nous proposons quatre méthodes distinctes pour utiliser notre programme :

<details open>
  <summary>1. Commandline</summary>

1.  Python installé (3.8 &lt;= version &lt;= 3.12)

2.  Installez notre package :

    ```bash
    pip install pdf2zh
    ```

3.  Exécuter la traduction, les fichiers générés dans[répertoire de travail actuel](https://chatgpt.com/share/6745ed36-9acc-800e-8a90-59204bd13444):

    ```bash
    pdf2zh document.pdf
    ```

</details>

<details>
  <summary>2. Portable (w/o Python installed)</summary>

1.  Télécharger[configuration.bat](https://raw.githubusercontent.com/Byaidu/PDFMathTranslate/refs/heads/main/script/setup.bat)

2.  Double-cliquez pour exécuter.

</details>

<details>
  <summary>3. Graphic user interface</summary>
1. Python installed (3.8 <= version <= 3.12)
2. Install our package:

```bash
pip install pdf2zh
```

3.  Commencez à utiliser dans le navigateur :

    ```bash
    pdf2zh -i
    ```

4.  Si votre navigateur n'a pas démarré automatiquement, allez sur

    ```bash
    http://localhost:7860/
    ```

    <img src="./docs/images/gui.gif" width="500"/>

Voir[documentation pour l'interface graphique](./docs/README_GUI.md)pour plus de détails.

</details>

<details>
  <summary>4. Docker</summary>

1.  Tirez et courez :

    ```bash
    docker pull byaidu/pdf2zh
    docker run -d -p 7860:7860 byaidu/pdf2zh
    ```

2.  Ouvrir dans le navigateur :

        http://localhost:7860/

Pour le déploiement de Docker sur le service cloud :

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

### Impossible d'installer ?

Le programme actuel a besoin d'un modèle d'IA (`wybxc/DocLayout-YOLO-DocStructBench-onnx`) avant de travailler et certains utilisateurs ne peuvent pas télécharger en raison de problèmes de réseau. Si vous rencontrez un problème lors du téléchargement de ce modèle, nous proposons une solution de contournement en utilisant la variable d'environnement suivante :

```shell
set HF_ENDPOINT=https://hf-mirror.com
```

Si la solution ne fonctionne pas pour vous/si vous rencontrez d'autres problèmes, veuillez vous référer à[questions fréquemment posées](https://github.com/Byaidu/PDFMathTranslate/wiki#-faq--%E5%B8%B8%E8%A7%81%E9%97%AE%E9%A2%98).

<h2 id="usage">Advanced Options</h2>

Exécutez la commande de traduction dans la ligne de commande pour générer le document traduit`example-mono.pdf`et le document bilingue`example-dual.pdf`dans le répertoire de travail actuel. Utilisez Google comme service de traduction par défaut.

<img src="./docs/images/cmd.explained.png" width="580px"  alt="cmd"/>

Dans le tableau suivant, nous répertorions toutes les options avancées pour référence :

| Option         | Fonction                                                                                                           | Exemple                                        |
| -------------- | ------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------- |
| fichiers       | Fichiers locaux                                                                                                    | `pdf2zh ~/local.pdf`                           |
| links          | Fichiers en ligne                                                                                                  | `pdf2zh http://arxiv.org/paper.pdf`            |
| `-i`           | [Entrez dans l'interface graphique](#gui)                                                                          | `pdf2zh -i`                                    |
| `-p`           | [Traduction partielle de documents](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#partial) | `pdf2zh example.pdf -p 1`                      |
| `-li`          | [Langue source](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)                   | `pdf2zh example.pdf -li en`                    |
| `-lo`          | [Langue cible](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#languages)                    | `pdf2zh example.pdf -lo zh`                    |
| `-s`           | [Service de traduction](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#services)            | `pdf2zh example.pdf -s deepl`                  |
| `-t`           | [Multi-threads](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#threads)                     | `pdf2zh example.pdf -t 1`                      |
| `-o`           | Répertoire de sortie                                                                                               | `pdf2zh example.pdf -o output`                 |
| `-f`,`-c`      | [Exceptions](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#exceptions)                     | `pdf2zh example.pdf -f "(MS.*)"`               |
| `-cp`          | Mode de compatibilité                                                                                              | `pdf2zh example.pdf --compatible`              |
| `--share`      | Lien public                                                                                                        | `pdf2zh -i --share`                            |
| `--authorized` | Autorisation                                                                                                       | `pdf2zh -i --authorized users.txt [auth.html]` |
| `--prompt`     | [Invite personnalisée](https://github.com/Byaidu/PDFMathTranslate/blob/main/docs/ADVANCED.md#prompt)               | `pdf2zh --prompt [prompt.txt]`                 |

Pour des explications détaillées, veuillez vous référer à notre document sur[Utilisation avancée](./docs/ADVANCED.md)pour une liste complète de chaque option.

<h2 id="downstream">Secondary Development (APIs)</h2>

Pour les applications en aval, veuillez vous référer à notre document sur[Détails de l'API](./docs/APIS.md)pour plus d'informations sur :

-   [API Python](./docs/APIS.md#api-python), comment utiliser le programme dans d'autres programmes Python
-   [API HTTP](./docs/APIS.md#api-http), comment communiquer avec un serveur avec le programme installé

<h2 id="todo">TODOs</h2>

-   [ ] Analyser la mise en page avec des modèles basés sur DocLayNet,[PagaieX](https://github.com/PaddlePaddle/PaddleX/blob/17cc27ac3842e7880ca4aad92358d3ef8555429a/paddlex/repo_apis/PaddleDetection_api/object_det/official_categories.py#L81),[PapierMage](https://github.com/allenai/papermage/blob/9cd4bb48cbedab45d0f7a455711438f1632abebe/README.md?plain=1#L102),[Sama](https://github.com/facebookresearch/sam2)

-   [ ] Correction de la rotation des pages, de la table des matières, du format des listes

-   [ ] Correction de la formule de pixel dans les vieux papiers

-   [ ] Nouvelle tentative asynchrone sauf KeyboardInterrupt

-   [ ] Algorithme de Knuth – Plass pour les langues occidentales

-   [ ] Prise en charge des fichiers non PDF/A

-   [ ] Plugins de[Donc](https://github.com/zotero/zotero)et[Obsidienne](https://github.com/obsidianmd/obsidian-releases)

<h2 id="acknowledgement">Acknowledgements</h2>

-   Fusion de documents :[PyMuPDF](https://github.com/pymupdf/PyMuPDF)

-   Analyse de documents :[Pdfminer.six](https://github.com/pdfminer/pdfminer.six)

-   Extraction de documents :[Minel](https://github.com/opendatalab/MinerU)

-   Traduction multithread :[MathTraduire](https://github.com/SUSYUSTC/MathTranslate)

-   Analyse de la mise en page :[DocLayout-YOLO](https://github.com/opendatalab/DocLayout-YOLO)

-   Norme documentaire :[PDF expliqué](https://zxyle.github.io/PDF-Explained/),[Aide-mémoire PDF](https://pdfa.org/resource/pdf-cheat-sheets/)

-   Police multilingue :[Aller à Noto Universal](https://github.com/satbyy/go-noto-universal)

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
