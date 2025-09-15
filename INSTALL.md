# 安裝和運行說明

## 快速開始

### 1. 安裝依賴

```bash
pip install -r requirements.txt
```

### 2. 運行應用程序

```bash
python watermark_app.py
```

### 3. 測試應用程序

```bash
python test_app.py
```

## 功能說明

### 主要功能
- 📁 **批量處理**: 選擇包含圖片的資料夾，自動處理所有符合條件的圖片
- 🎨 **水印設置**: 可調整水印大小（10%-100%）、位置（5個位置）、透明度（10%-100%）
- 🖼️ **多格式支持**: 支持 JPG、TIFF、PNG 格式
- 🌍 **多語言**: 支持英文、繁體中文、簡體中文
- 🌙 **主題切換**: 支持淺色/深色主題
- 📝 **實時日誌**: 顯示處理進度和結果

### 版本信息
- 版本號碼顯示在右下角
- 如果配置了 GitHub URL，版本號碼會變成可點擊的藍色連結
- 點擊版本號碼會在瀏覽器中打開 GitHub 頁面

## 配置說明

### 修改 GitHub URL

在 `config.yaml` 文件中修改：

```yaml
version: "1.0"
github_url: "https://github.com/yourusername/qt_watermark"
```

將 `yourusername` 替換為您的 GitHub 用戶名，將 `qt_watermark` 替換為您的倉庫名稱。

### 自定義公司信息

在 `config.yaml` 的翻譯部分修改：

```yaml
translations:
  zh_tw:
    company_name: "您的公司名稱"
    copyright: "版權所有 © 2024 您的公司。保留所有權利。"
```

## 打包為可執行文件

### 使用 PyInstaller

```bash
# 安裝 PyInstaller
pip install pyinstaller

# 打包應用程序
pyinstaller watermark_app.spec
```

打包後的可執行文件會在 `dist/` 目錄中。

## 故障排除

### 常見問題

1. **導入錯誤**: 確保已安裝所有依賴包
2. **圖片處理失敗**: 檢查圖片格式是否支持，水印文件是否為有效的 PNG 文件
3. **權限錯誤**: 確保對輸出資料夾有寫入權限

### 日誌信息

應用程序底部有日誌區域，會顯示：
- 處理進度
- 錯誤信息
- 成功處理的文件數量

## 技術要求

- Python 3.7+
- PyQt5
- Pillow (PIL)
- PyYAML

## 支持

如有問題，請查看 GitHub 頁面或提交 Issue。
