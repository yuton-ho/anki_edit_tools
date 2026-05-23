# anki_edit_tools
修改成克漏字的腳本
這是一份專為「個人備份與未來操作筆記」設計的雙語（中英）README。內容簡明扼要，方便你日後回顧時能一秒看懂如何操作。

你可以直接將以下的 Markdown 原始碼複製並貼上到你的 `README.md` 檔案中：

```markdown
# Anki Cloze Spelling Generator / Anki 克漏字拼寫卡片產生器

## 📝 簡介 / Description
**[中文]**
這是一個用於個人備份與自動化處理 Anki `.apkg` 檔案的 Python 腳本。它能讀取原始的單字牌組，將例句中的目標單字（由 `<b>` 標籤包覆）自動挖空，並重新打包成一個帶有「打字輸入框（拼字檢查）」功能的全新獨立牌組。

**[English]**
This is a Python script for personal automation and backup of Anki `.apkg` files. It reads an original vocabulary deck, automatically blanks out target words in example sentences (wrapped in `<b>` tags), and repackages the data into a brand new, independent deck featuring a "type-in-the-answer" spelling check.

## ✨ 主要功能 / Key Features
*   **統一牌組 (Unified Deck):** 忽略原有的子牌組階層，將所有單字集中合併到一個名為「克漏字拼寫練習」的全新大牌組中。
*   **避開重複機制 (Bypass Duplicate Check):** 自動在第一欄生成獨立的 `Card_ID`，確保匯入時能與舊卡片完美共存，不會被 Anki 顯示「已略過」。
*   **媒體無損 (Media Preservation):** 自動解開並重新打包原有的圖片與發音音檔。

---

## 🛠 環境需求 / Prerequisites

Please ensure you have Python installed, and then install the required package:
請確保電腦已安裝 Python，並使用以下指令安裝必要套件：

```bash
pip install genanki

```

---

## 🚀 使用方式 / Usage

**[中文]**

1. 將你想修改的原始 Anki 檔案重新命名為 `my_original_deck.apkg`。
2. 將該檔案與 Python 腳本放在**同一個資料夾**內。
3. 在終端機執行腳本：

```bash
   python script_name.py

```

4. 執行完成後，資料夾內會產出 `my_edited_cloze_deck.apkg`。
5. 雙擊該檔案匯入 Anki 即可開始練習！

**[English]**

1. Rename your original Anki file to `my_original_deck.apkg`.
2. Place it in the **same directory** as the Python script.
3. Run the script in your terminal:

```bash
   python script_name.py

```

4. The script will generate a new file named `my_edited_cloze_deck.apkg`.
5. Double-click the new file to import it into Anki and start practicing!

---

## 📌 個人備忘錄 / Personal Notes

* **修改牌組名稱 (Change Deck Name):** 如果日後想要更改匯入後的牌組名稱，請打開 Python 腳本，尋找並修改 `UNIFIED_DECK_NAME = "克漏字拼寫練習"` 這個變數。
* **修改輸入/輸出檔名 (Change I/O Filenames):** 可以直接在程式碼最下方的 `INPUT_FILE` 與 `OUTPUT_FILE` 變數中進行調整。

```

```
