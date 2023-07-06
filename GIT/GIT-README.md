## Gitの利用方法

### GitHubへのアカウント作成
1. GitHubのWebサイトにアクセスします。
    https://github.co.jp/
    ![Alt text](image.png)

1. GitHubのアカウント、電子メールアドレス、パスワードを設定します。
    ![Alt text](image-1.png)

1. GitHubから下図のようなメールが届きます。GitHubを開きます。
    ![Alt text](image-2.png)

1. GitHubのプロファイルを適宜編集します。
    ![Alt text](image-3.png)

1. Gitコマンドユーザー名と電子メールを設定します。
    ```
    git config --global user.name 'CTC/Shuichi Ikeda'
    git config --global user.emai 'shuichi.ikeda@ctc-g.co.jp'
    ```
    ![Alt text](image-23.png)

## 新しいリポジトリの作成

1. GitHubで新しいリポジトリを作成します。
    ![Alt text](image-4.png)

1. リポジトリ名、詳細、Privateを選択します。
※ Publicを選択するとインターネットに公開されますのでご注意ください。
    ![Alt text](image-5.png)

1. こちらの画面が表示されればリポジトリの追加は成功です。
    ![Alt text](image-6.png)

1. GitリポジトリのURLをコピーします。
    ![Alt text](image-15.png)
    もし上記の画面が表示されなくなった場合は、下記の画面からもURLがコピーできます。
    ![Alt text](image-24.png)

1. VSCodeでリポジトリにPUSHしたいフォルダを開きます。
    ![Alt text](image-7.png)

1. Gitコマンドで、現在のリモートのURLを確認します。
    ```
    git config remote.origin.url
    ```
    ![Alt text](image-16.png)

1. Gitコマンドで、コピーしたURLに変更します。
    ```
    git remote set-url origin "コピーしたURL"
    ```
    ![Alt text](image-19.png)

1. Gitコマンドで、変更後のリモートのURLを確認します。
    ```
    git config remote.origin.url
    ```
    ![Alt text](image-20.png)

1. Gitコマンドで、ソースコードをPushします。
    ```
    git push
    ```
    ![Alt text](image-21.png)

1. GitHubのリポジトリにソースコードがPushされていることを確認します。
    ![Alt text](image-22.png)

1. その後ファイルを編集した際は、VSCodeのソース管理からもコミットできます。

    ![Alt text](image-12.png)

1. VSCodeで変更を同期します。

    ![Alt text](image-13.png)

1. GitHubのリポジトリにソースコードが変更されていることを確認します。
    ![Alt text](image-22.png)


