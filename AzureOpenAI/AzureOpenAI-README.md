## Azure Open AIの利用方法

### Azure PortalでのAzure Open AIの作成
1. Azure Portalにアクセスします。
    https://portal.azure.com/
    ![Alt text](image.png)

1. リソースの作成からAzure Open AIを選択します。
    ![Alt text](image-1.png)

1. Azure OpenAIを作成します。
    ![Alt text](image-2.png)

1. Azure OpenAIサービスへのアクセス要求を出します。
    ![Alt text](image-4.png)

1. Request Access to Azure OpenAI Serviceにアクセスします。
    ![Alt text](image-5.png)

1. Your First Name、Your Last Name、How many Azure Subscription ID's would you like to have access to this service?を入力します。
    ![Alt text](image-7.png)

1. Azure Subscription IDを入力します。
    ![Alt text](image-9.png)

1. 電子メール、会社名、会社住所等を入力します。

1. 下記の質問に回答します。
    ![Alt text](image-11.png)
    ![Alt text](image-12.png)
    ![Alt text](image-13.png)
    ![Alt text](image-14.png)

1. 以下の画面が表示されたら申請完了です。
    ![Alt text](image-15.png)

1. 翌日、下記のメールが届きます。
    ![Alt text](image-16.png)

1. 価格レベルで、Standard SOが選択できます。
    ![Alt text](image-19.png)

1. ネットワークは、「インターネットを含むすべてのネットワークのリソースにアクセスできます。」を選択します。
    ![Alt text](image-18.png)

1. 下図の画面で「作成」ボタンを押下します。
    ![Alt text](image-20.png)

1. 下図の画面で「デプロイが完了しました」と表示されます。
    ![Alt text](image-21.png)

1. Azure Open AIが利用可能になります。
    ![Alt text](image-22.png)

### Lang Chainへの組み込み
1. 下の画面によりキーを確認できます。
    ![Alt text](image-23.png)

1. 下記によりLangChainに設定ができます。

    ```
    # Set this to `azure`
    export OPENAI_API_TYPE=azure
    # The API version you want to use: set this to `2023-05-15` for the released version.
    export OPENAI_API_VERSION=2023-05-15
    # The base URL for your Azure OpenAI resource.  You can find this in the Azure portal under your Azure OpenAI resource.
    export OPENAI_API_BASE=https://ctcopenaidemo1.openai.azure.com/
    # The API key for your Azure OpenAI resource.  You can find this in the Azure portal under your Azure OpenAI resource.
    export OPENAI_API_KEY=XXXXXXXXXXXXXX
    ```

    【参考】
    https://python.langchain.com/docs/integrations/llms/azure_openai_example

1. Azure OpenAI Studioに移動します。
    ![Alt text](image-25.png)

1. 管理の「デプロイ」で「新しいデプロイの作成」をクリックします。
    ![Alt text](image-27.png)

1. モデルを選択し、デプロイ名を入力し、「作成」ボタンを押下します。
    ![Alt text](image-28.png)

1. モデルが作成されます。
    ![Alt text](image-29.png)

1. Azure Portalから課金情報も見えるようになります。
    ![Alt text](image-24.png)

以上