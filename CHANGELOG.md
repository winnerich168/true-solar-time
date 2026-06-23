# Changelog

本檔記錄真太陽時換算器的版本變更。

All notable changes to this project will be documented in this file.

## [1.0.0] - 2026-06-23

### 首次公開發布 Initial Public Release

#### Added
- 真太陽時換算核心功能(以 GMT 為錨點,東加西減)
- Jean Meeus《Astronomical Algorithms》§25 完整天文公式 (精度 ±7 秒)
- NASA Espenak-Meeus ΔT 多項式修正
- 國家→城市兩層級篩選 (約 80 個城市,10 個區域)
- 雙人對照比對 (A 案 / B 案)
- 推算過程透明顯示
- 計算法則與來源說明區
- 📍 地理定位自動偵測經度功能
- 中國傳統十二時辰對照
- RWD 響應式設計,支援手機/平板/桌面
- 完全前端計算,不上傳個人資料

#### Technical
- 純 HTML + CSS + JavaScript,零外部依賴
- 單一 HTML 檔可獨立執行
- 可部署於任何靜態網站服務
