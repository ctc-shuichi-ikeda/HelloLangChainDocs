# LangChainのデモ環境

## デモの概要
テキスト、PDF、PPT等の社内ファイルを学習させて、質問に答えるシナリオとなります。
Visual Studio Code上でデモを実行します。
![Alt text](image-2.png)

## デモのアーキテクチャ
デモのアーキクチャを下図に示します。社内ファイルは各種Loaderにより読み込まれOpenAI Embeddingsで文書をベクトルに変換し、ベクトルDBであるChromadbに格納されます。
利用者からの質問に対して、RetriveQAがベクトルDBにある情報の検索結果をOpen AIが文書を生成し、利用者に回答していると想定しています。
![Alt text](image-3.png)

## 開発環境構成図
CTCのセキュアPCにLangChainの開発環境を構築します。
![Alt text](image.png)

## 開発環境構築手順
構築手順は[こちら](INSTALL/INSTALL.md)です。

## 参考
Open AI Quickstart:
https://platform.openai.com/docs/quickstart

LangChain Github:
https://github.com/hwchase17/langchain

LangChain Getting Started:
https://python.langchain.com/en/latest/getting_started/getting_started.html
