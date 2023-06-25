

# LangChainの開発環境構築手順
CTCのセキュアPCにLangChainの開発環境を構築する手順を下記に示します。

## Windows subsystem for linux2のインストール

1. PowerShellを管理者権限で開きます。
    ![Alt text](image.png)

1. WSLを有効化するために、以下のコマンドを実行します。
    ```
    wsl --install
    ```
    ![Alt text](image-1.png)

1. Ubuntuを初期化します。スタートメニューからUbuntuを起動します。
    ![Alt text](image-5.png)

1. 初期バスワードを登録します。
    ![Alt text](image-6.png)

1. Windowsの左下の検索から「機能の有効化」を検索します。
    ![Alt text](image-3.png)

1. 「Hyper-V」と「Linux用Windowsサブシステム」を有効化されていることを確認します。有効化されていない場合は、チェックを入れて有効化してください。

    ![Alt text](image-4.png)

1. インストールされているLinuxディストリビューションを確認します。
    ```
    wsl -l -v
    ```
    ![Alt text](image-2.png)

参考：
https://learn.microsoft.com/ja-jp/windows/wsl/install


## Visual Studio Code最新版のインストール
1. Visual Studio Codeを下記からダウンロードします。
    https://azure.microsoft.com/ja-jp/products/visual-studio-code
    ![Alt text](image-8.png)

1. WSLに接続します。
    ![Alt text](image-9.png)

1. Ctrl+Shift+@でターミナルを起動します。
    ![Alt text](image-10.png)


## Python 3.10のインストール
1. aptパッケージを更新します。
    ```
    sudo apt update
    ```

1. pipをインストールします。
    ```
    sudo apt install -y python3-pip
    pip3 -V
    ```

1. リポジトリを追加します。
    ```
    sudo apt install -y software-properties-common
    sudo add-apt-repository ppa:deadsnakes/ppa
    ```

1. Python3.10をインストールします。venvで仮想環境を分けるため、python.3.10もインストールしています。
    ```
    sudo apt install -y python3.10 python3.10-venv
    ```

1. pythonのバージョンを確認します。
    ```
    python3 --version
    ```

## git for windows最新版のインストール
1. git for windowsを下記からダウンロードします。
    https://gitforwindows.org/

1. git for windowsのインストーラを起動します。

    ![Alt text](image-7.png)

1. Gitリポジトリをクローンします。
    ```
    git clone https://github.com/ctc-shuichi-ikeda/HelloLangChain.git
    ```
    ![Alt text](image-21.png)

1. クローンしたGitリポジトリのフォルダをVSCodeで開きます。
    ```
    cd HelloLangChain
    code -r .
    ```
    ![Alt text](image-12.png)

## 必要なライブラリの最新版のインストール
1. Pythonの仮想環境を作成します。
    ```
    python3 -m venv venv
    ```
    ![Alt text](image-24.png)

1. Pythonの仮想環境を有効化します。
    ```
    . venv/bin/activate
    ```
    ![Alt text](image-13.png)
    
1. 必要なライブラリであるlangChain、openai、chromadb、titokenの最新版をインストールします。
    ```
    pip3 install -r requirements.txt
    ```
    ![Alt text](image-22.png)

## 動作確認
1. ChatGPTの有償版のAPI keysのページにアクセスし、「
Create new secret key」を押下します。
    https://platform.openai.com/account/api-keys
    ![Alt text](image-16.png)

1. Create new secret keyに名前を付与します。
    ![Alt text](image-17.png)

1. new secret keyをコピーします。

    ![Alt text](image-18.png)

1. HelloQA.py等のソースコードのos.environ['OPENAI_API_KEY']に値をセットします。
    ![Alt text](image-19.png)

1. 「F5」を押下し、「Pythonファイル 現在アクティブなPythonファイルをデバッグする」を選択します。
    ![Alt text](image-23.png)

1. 下記の画面が出力されます。
    ![Alt text](image-25.png)

以上
