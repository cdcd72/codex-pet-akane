# Codex Pets: Akane

這裡提供一款以 Akane 為主題的 Codex 寵物：[Codex Pets](https://developers.openai.com/codex/app/settings#codex-pets)。

安裝之後，你寫 Code 時就不再是孤軍奮戰。

每當你想跳過文件、少寫測試、或是打算先硬做再說的時候，Akane 就會在旁邊一臉不耐煩地盯著你，像是在說：

「我、我才不是在幫你收尾，只是不想看你把專案搞砸而已。」

![Akane spritesheet](spritesheet.webp)

## 安裝

最簡單的安裝方式是在 Codex app 直接輸入以下提示詞：

```text
安裝 cdcd72/codex-pet-akane repo 的 Codex Pet 給我的 Codex app 使用
```

如果你想手動安裝，這個 repo 的 CI 會產出 GitHub Pages 套件：

```text
https://cdcd72.github.io/codex-pet-akane/akane.codex-pet.zip
```

macOS 或 Linux 可在終端機執行：

```sh
curl -sL "https://cdcd72.github.io/codex-pet-akane/akane.codex-pet.zip" -o "/tmp/akane.codex-pet.zip" && mkdir -p "$HOME/.codex/pets/akane" && unzip -o "/tmp/akane.codex-pet.zip" -d "$HOME/.codex/pets/akane"
```

Windows PowerShell 可執行：

```powershell
New-Item -ItemType Directory -Force "$HOME/.codex/pets/akane" | Out-Null
Invoke-WebRequest "https://cdcd72.github.io/codex-pet-akane/akane.codex-pet.zip" -OutFile "$env:TEMP/akane.codex-pet.zip"
Expand-Archive -Path "$env:TEMP/akane.codex-pet.zip" -DestinationPath "$HOME/.codex/pets/akane" -Force
```

執行後，Codex 會在 `~/.codex/pets/akane` 讀取這個寵物。

## 使用

1. 下載並解壓縮寵物檔案。
2. 確認 `~/.codex/pets/akane` 內有 `pet.json` 與 `spritesheet.webp`。
3. 重新啟動 Codex 並到設定中的寵物選單選取 `Akane`。
4. 到聊天視窗輸入 `/pet` 或從指令選單啟用寵物功能。
5. 啟用後，Akane 就會在介面中依狀態播放對應動畫。

## 檔案說明

- `pet.json`: 寵物的中繼資料。
- `spritesheet.webp`: 寵物的圖像素材。
