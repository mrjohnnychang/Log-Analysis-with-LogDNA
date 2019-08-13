---

copyright:
  years:  2018, 2019
lastupdated: "2019-03-06"

keywords: LogDNA, IBM, Log Analysis, logging, alerts

subcollection: LogDNA

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:important: .important}
{:note: .note}

 
# 使用警示
{: #alerts}

您可以將一個以上的警示連接至視圖。您可以為警示定義多個通知頻道。您可以停用警示通知。您可以分離視圖與警示。
{:shortdesc}

您可以針對警示配置下列任何條件：

* *時間頻率*：指定觸發警示的頻率。有效值為：30 秒、1 分鐘、5 分鐘、15 分鐘、30 分鐘、1 小時、6 小時、12 小時、24 小時
* *日誌行計數器*：指定符合視圖過濾及搜尋準則的日誌行數量。達到日誌行數量時，便會觸發警示。

您可以決定檢查這兩個條件，或只檢查一個條件。如果兩個條件都已設定，則會在達到任何臨界值時觸發警示。 

例如，您可以配置警示在 30 秒之後觸發，或在收集到符合視圖過濾和搜尋準則的 100 個日誌行時觸發。

您可以配置多個通知頻道。有效的頻道為：`email`、`Slack`、`PagerDuty`、`Webhook`、`OpsGenie`、`Datadog`、`AppOptics`、`VictorOps`

您也可以定義**預設**。預設是警示範本，您可以連接至任意數目的視圖。 

若要在不同的視圖重複使用警示配置，請配置**警示預設**。
{: tip}

視圖中會顯示一個鈴聲圖示，指出此視圖已連接一個警示。



## 配置預設（警示範本）
{: #config_preset}

請完成下列步驟來配置預設：

1. 選取**配置**圖示 ![配置圖示](images/admin.png "管理圖示")。
2. 選取**警示**。
3. 選取**新增預設警示**。
4. 選擇通知頻道。 
5. 定義臨界條件。

    1. 選取時間頻率。例如，12 小時。

    2. 輸入日誌行數量，您想要在達到該數量之後觸發警示。

    3. 選取您希望同時勾選這兩個條件，還是只勾選一個。

6. 新增所選通知頻道的詳細資料。

    例如，針對電子郵件通知頻道，新增一個以上的收件者，並選擇性地新增時區。

7. 按一下**儲存警示**。



## 使用預設配置警示
{: #config_alert_preset}

請完成下列步驟，以將預設連接至視圖：

1. 按一下**視圖**圖示 ![配置圖示](images/views.png)。
2. 建立視圖。 

    套用時間範圍、過濾器及搜尋準則，以過濾透過視圖顯示的日誌行。 

    如需相關資訊，請參閱[建立視圖](/docs/services/Log-Analysis-with-LogDNA?topic=LogDNA-view_logs#view_logs_step7)。

3. 按一下視圖名稱。然後，選取**連接警示**。

4. 選擇預設以重複使用警示定義。 

5. 按一下**儲存警示**。 




## 配置視圖特定的警示
{: #config_alert_view}

請完成下列步驟，以將警示連接至視圖：

1. 按一下**視圖**圖示 ![配置圖示](images/views.png)。
2. 建立視圖。 

    套用時間範圍、過濾器及搜尋準則，以過濾透過視圖顯示的日誌行。 

    如需相關資訊，請參閱[建立視圖](/docs/services/Log-Analysis-with-LogDNA?topic=LogDNA-view_logs#view_logs_step7)。

3. 按一下視圖名稱。然後，選取**連接警示**。

4. 選擇**檢視特定警示**。

5. 選擇通知頻道。 

6. 定義臨界條件。

    1. 選取時間頻率。例如，12 小時。

    2. 輸入日誌行數量，您想要在達到該數量之後觸發警示。

    3. 選取您希望同時勾選這兩個條件，還是只勾選一個。

7. 新增所選通知頻道的詳細資料。

    例如，針對電子郵件通知頻道，新增一個以上的收件者，並選擇性地新增時區。

8. 按一下**儲存警示**。



## 刪除預設（警示範本）
{: #delete_preset}

請完成下列步驟來刪除預設：

1. 選取**配置**圖示 ![配置圖示](images/admin.png "管理圖示")。
2. 選取**警示**。
3. 將滑鼠移至您要刪除的預設的*編輯* 按鈕上。即會顯示*刪除* 選項。
4. 選取**刪除**。
5. 確認您要刪除預設。按一下**刪除**。

## 分離視圖中的視圖特定警示
{: #delete_alert}

請完成下列步驟來分離預設：

1. 選取**配置**圖示 ![配置圖示](images/admin.png "管理圖示")。
2. 選取**警示**。
3. 將滑鼠移至您要刪除的警示的*編輯* 按鈕上。即會顯示*刪除* 選項。
4. 選取**分離**。
5. 確認您要刪除警示。按一下**分離**。



## 通知頻道
{: #channels}

下表列出當觸發警示時，您可以配置的通知頻道：

| 頻道           | 配置詳細資料 | 
|-------------------|-----------------------|
| `email`             | 您可以配置一個以上的電子郵件位址。| 
| `Slack`             | 您可以配置 Slack 頻道。|
| `Webhook`           | 您可以配置 Webhook URL。|
| `PagerDuty`         | 您可以配置 PagerDuty 系統的連線詳細資料，並選取一個服務。|
| `OpsGenie`          | 您可以配置要連接至 OpsGenie 系統的 API 金鑰。|
| `Datadog`           | 您可以配置要連接至 `Datadog` 系統的 API 金鑰。|
| `AppOptics/Librato` | 您可以配置要連接至 AppOptics/Librato 系統的 API 金鑰。|
| `VictorOps`         | 您可以配置當觸發警示時要通知的 URL、遞送金鑰以及警示類型。有效的警示類型為：`info`、`warning`、`critical` |
{: caption="通知頻道" caption-side="top"} 

