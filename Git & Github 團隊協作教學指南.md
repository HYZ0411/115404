# Git & GitHub 團隊協作教學指南

這份指南分為組長（管理員）與組員（協作者）兩大部分，請根據你的角色執行對應的流程。

---

## 👑 第一份：組長專用指南 (Team Leader Guide)
**核心任務：** 建立專案、設定環境、邀請成員、審核並合併程式碼。

### 1. 初始化專案與環境設定
* **設定身分：** (只需設定一次)
    ```bash
    git config --global user.name "你的名字"
    git config --global user.email "你的Email"
    ```
* **建立儲存庫 (Repository)：** 在 VS Code 開啟專案資料夾後：
    ```bash
    git init
    ```
    > **注意：** 這會產生隱藏的 `.git` 資料夾，請勿刪除。
* **設定忽略檔案：** 手動建立 `.gitignore` 檔案，寫入不需要追蹤的檔案（如：`node_modules/`, `.env`）。

### 2. 建立第一版內容 (Main Branch)
* **檢查狀態：** `git status`
* **加入暫存區 (Staging)：**
    ```bash
    git add .
    ```
* **提交版本 (Commit)：**
    ```bash
    git commit -m "修改/新增/刪除：檔案 - 描述"
    ```

### 3. 上傳至 GitHub 與邀請組員
1.  **建立 GitHub 遠端儲存庫：** 到 GitHub 官網點擊 **New Repository**。
2.  **連結並上傳：**
    ```bash
    git remote add origin <GitHub專案網址>
    git branch -M main
    git push -u origin main
    ```
3.  **邀請組員：**
    * 進入專案頁面 `Settings` > `Collaborators`。
    * 點擊 `Add people`，輸入組員帳號發送邀請。

### 4. 審核與合併 (Merge)
1.  **查看 Pull Request：** 在 GitHub `Pull requests` 分頁檢查組員的申請。
2.  **審核與合併：** 檢查無誤後點擊 `Merge pull request`。
3.  **更新本地進度：** 合併後，將雲端最新內容拉回電腦：
    ```bash
    git pull
    ```

---

## 👨‍💻 第二份：組員專用指南 (Team Member Guide)
**核心任務：** 複製專案、在獨立分支開發、保持同步、發起合併請求。

### 1. 加入專案與下載程式碼
1.  **接受邀請：** 到信箱收取邀請信並點擊同意。
2.  **複製專案 (Clone)：**
    ```bash
    git clone <專案網址>
    cd <資料夾名稱>
    ```

### 2. 同步與建立分支 (Branch)
> **重要觀念：** 永遠不要直接在 `main` 上修改！
* **更新進度：** `git pull origin main`
* **建立並切換分支（-b 這個參數的作用是 「建立並切換」。當分支已經存在，直接去掉 -b 即可）：**
    ```bash
    git checkout -b <你的分支名稱>
    ```

### 3. 開發與提交 (Daily Workflow)
* **加入暫存：** `git add .`
* **提交快照：** `git commit -m "修改/新增/刪除：檔案-描述"`

### 4. 上傳與發起合併 (Pull Request)
* **推送到雲端：**
    ```bash
    git push origin <你的分支名稱>
    ```
* **發起 PR：** 回到 GitHub 點擊 `Compare & pull request`，填寫說明後建立請求。

### 5. 任務完成後的清理
* **回到主分支並更新：**
    ```bash
    git checkout main
    git pull
    ```

---

## 🛠 通用指令速查表 (Cheat Sheet)

### 查看紀錄
* **詳細紀錄：** `git log` (按 `q` 離開)
* **簡潔紀錄：** `git log --oneline`

### 還原與差異 (後悔藥)
* **比較差異：** `git diff <版本ID> <檔名>`
* **單一檔案還原：** `git checkout <版本ID> <檔名>`
* **強制還原至特定版本：** (小心！未提交的資料會消失)
    ```bash
    git reset --hard <版本ID>
    ```

### 刪除處理
* 若手動刪除了檔案，仍需執行 `git add .` 來告知 Git 該「刪除」動作，再進行 `commit`。