# 圖片水印工具 (Image Watermark Tool)

一個基於 PyQt5 的圖片水印添加工具，支持批量處理 JPG、TIFF、PNG 格式的圖片。

## 功能特點

- 🖼️ 支持多種圖片格式：JPG、TIFF、PNG
- 🎨 可調整水印大小、位置和透明度
- 🌍 多語言支持：英文、繁體中文、簡體中文
- 🌙 支持淺色/深色主題切換
- 📁 批量處理整個資料夾
- 📝 實時日誌顯示
- 🔄 異步處理，不會阻塞界面

## 安裝要求

```bash
pip install -r requirements.txt
```

## 使用方法

1. 運行應用程序：
```bash
python watermark_app.py
```

2. 按照界面提示：
   - 選擇包含圖片的來源資料夾
   - 選擇帶透明背景的水印 PNG 檔案
   - 選擇輸出資料夾
   - 調整水印設置（大小、位置、透明度）
   - 選擇要處理的圖片類型
   - 點擊「開始處理」

## 水印設置

- **大小**：10% - 100%（相對於圖片最小邊的百分比）
- **位置**：左上、右上、左下、右下、居中
- **透明度**：10% - 100%
- **支援格式**：JPG、TIFF、PNG

## 打包為可執行文件

使用 PyInstaller 打包：

```bash
pyinstaller watermark_app.spec
```

## 文件結構

```
qt_watermark/
├── watermark_app.py          # 主應用程序
├── watermark_processor.py    # 水印處理模組
├── config.yaml              # 配置文件
├── requirements.txt         # 依賴包列表
├── watermark_app.spec       # PyInstaller 配置
└── README.md               # 說明文件
```

## 技術特點

- 使用 PyQt5 構建現代化界面
- 多線程處理，避免界面卡頓
- 支持透明 PNG 水印
- 保持原始圖片質量
- 自動創建輸出目錄
- 錯誤處理和日誌記錄

## 版本信息

版本：1.0
版權：© 2024 HuHu Tech. All rights reserved.

