# UML類別圖
![類別圖](類別圖.png)
# 使用案例一：設置健康目標
## 循序圖
```mermaid
sequenceDiagram
    用戶 ->> 系統: 輸入健康目標
    系統 ->> 健康目標: 存儲用戶健康目標
    健康目標 -->> 系統: 目標已存儲
    系統 -->> 提醒服務: 生成定期提醒
    提醒服務 ->> 用戶:接受提醒通知
```
## 活動圖
```mermaid
graph TD
    A(開始) --> |用戶啟動設置目標流程|B[用戶輸入健康目標]
    B --> C[系統接收並存儲目標數據]
    C --> D[系統生成定期提醒]
    D --> E[用戶接受提醒通知]
    E -->F(結束)
```
# 使用案例二：生成健康報告
## 循序圖
```mermaid
sequenceDiagram
    用戶 ->> 報告: 用戶請求查看報告
    報告 ->> 健康數據: 提取用戶的健康數據
    健康數據 -->> 報告: 將用戶數據傳回報告
    報告 ->> 風險評估: 進行風險評估
    風險評估 -->> 報告:計算後的風險分數
    報告 ->> 用戶:生成報告並顯示給用戶
```
## 活動圖
```mermaid
graph TD
    A(開始) --> B[用戶請求健康報告]
    B --> C[系統提取健康數據]
    C --> D[系統進行風險評估]
    D --> E[生成健康報告]
    E --> F[報告展示給用戶]
    F --> G(結束)
```
# 使用案例三：健康風險評估
## 循序圖
```mermaid
sequenceDiagram
    用戶 ->> 系統: 提交健康問卷
    系統 ->> 健康數據庫: 查詢用戶健康數據
    健康數據庫 -->> 系統: 返回健康數據
    系統 ->> 風險評估模組: 計算健康風險
    風險評估模組 -->> 系統: 返回風險分數和建議
    系統 ->> 用戶: 顯示風險評估結果
```
## 活動圖
```mermaid
graph TD
    A(開始) --> |系統啟動健康風險評估流程|B[提取用戶健康數據]
    B --> C[系統進行風險計算]
    C --> D[生成健康建議]
    D --> E[結果反饋給用戶]
    E --> F(結束)
```
