# DemoAR

unity version：2019.4.1f

## Getting Started

新增專案時，選擇 3D，開啟專案後，點選 File -> Build Settings -> 選擇 Android -> Switch Platform -> 點選 Assets -> Import Package -> Custom Package -> Import

如想從頭開始，流程如下：

1. 安裝 Vuforia AR 套件
   Window/Package Manager -> 選擇 Unity Registry -> 搜尋 Vuforia Engine AR -> 按下 Install

2. 註冊 Vuforia
   [Vuforia](https://developer.vuforia.com/)
   登入後 -> 點選 Develop -> License Manager -> Get Basic -> 輸入 License Name、Checkbox 打勾，確認

3. 獲取 License
   點選 DemoAR -> 複製 License Key

4. 建立目標圖片庫
   點選 Add Database -> 取名字，Type：Device -> 完成後，點選 DemoAR -> Add Target

   - Type：Single Image
   - File：圖片名稱
   - Width：10
   - Name：英文數字
   - 完成後，Rating：至少 3 顆星

   -> 選取欲轉出的圖片 -> 點選 Download Database -> 轉出圖片資料庫 -> 選取 Unity Editor，Download

5. 匯入圖片資料庫
   回到 unity -> Assets/Import Package/Custom Package -> 按下右下角的 Import

   - 加入元件
     - GameObject/Vuforia Engine/
     - AR Camera
     - ImageTarget
   - 加入 License -> 點選 AR Camera -> 點選 Open... -> 貼入 License Key

6. 設定 ImageTarget
   - Type：Predefined
   - Database：DemoAR
   - Image Target：1 or 2
     加入 Cube 元件 -> 在 ImageTarget 下加入 Cube

## 加入影片

    - 先將欲播放的影片拖曳到Resource的資料夾裡
    - 在Cube下加入Video Player
    - 設定Video Player元件
        - Source：Video Clip
        - Video Clip：將Resource裡的影片拖曳到Videp Clip元件
        - Render Mode：Material Override
        - Renderer：Cube

### 測試

    - 將圖片資料庫的圖片放在手機裡
    - 選取ImageTarget所設定的圖片
    - unity案執行
