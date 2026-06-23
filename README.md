# 真太陽時換算器 True Solar Time Calculator

> 校正出生時間的真太陽時,讓紫微、八字、河洛、易經命盤推算更精準。
> A free web tool for calculating true solar time, used in Chinese metaphysics and astronomy.

🌞 **線上試用 / Live Demo**:[winnerich.com](https://winnerich.com)

---

## 特色 Features

- 📐 **以 GMT 為錨點**,東加西減,自動消除夏令時間 (DST) 干擾
- ☀️ **Jean Meeus 天文公式**計算均時差 Et,精度 ±7 秒
- 🌏 涵蓋全球 **80+ 城市**,國家→城市層級篩選
- 📍 支援 **地理定位** 自動偵測經度
- 🔢 雙人對照比對功能
- 🇨🇳 對應 **中國傳統十二時辰**
- 💯 純前端 JavaScript,**零後端依賴、不上傳任何個人資料**

## 公式 Formula

```
真太陽時 = GMT + 經度時差(東+西−) + 均時差 Et

True Solar Time = GMT + Longitude Offset (E+/W−) + Equation of Time
```

### 計算法則

1. **退回 GMT**:`GMT = 當地手錶時間 − UTC Offset`
2. **經度時差**:`經度時差(分鐘) = 經度 × 4`,東經加、西經減
3. **均時差 Et**:依 Jean Meeus《Astronomical Algorithms》§25 公式計算
4. **大一統輸出**:三者相加得真太陽時

## 使用方式 Usage

直接打開 `index.html` 即可使用,無需任何伺服器或建構流程。

```bash
# Clone repo
git clone https://github.com/YOUR_USERNAME/true-solar-time.git
cd true-solar-time

# 直接用瀏覽器打開
open index.html
```

也可以直接部署到任何靜態網站服務(GitHub Pages、Vercel、Netlify、Cloudflare Pages 等)。

## 技術細節 Technical Details

| 項目 | 來源 / 標準 |
|------|------------|
| 時區資料 | IANA Time Zone Database (tzdata) |
| 城市經度資料 | GeoNames 地理資料庫 |
| 均時差公式 | Jean Meeus《Astronomical Algorithms》§25 |
| ΔT 修正 | NASA Espenak-Meeus 多項式 |
| 時辰對照 | 中國傳統十二時辰制 |

## 精度說明 Accuracy

- 均時差 Et 精度:**±7 秒**(Jean Meeus 完整公式)
- 城市經度為市中心參考值,若出生地遠離市中心建議手動微調
- 夏令時間 (DST) 已透過 GMT 校正機制自動消除
- 歷史時期(清朝、民國早期)的時區制度與現行不同,使用時需自行考量

## 授權 License

MIT License — 詳見 [LICENSE](LICENSE) 檔案。

歡迎自由使用、修改、商用,只需保留原作者署名。

## 作者 Author

**林勝烽 (Lin Sheng-Feng)**
奉熙易理研究所 · [winnerich.com](https://winnerich.com)

## 貢獻 Contributing

歡迎透過 Issue 回報問題或 Pull Request 提交改進。如要新增城市資料,請依照現有格式提供:

```javascript
{ name: '城市名', lon: 經度數字, hem: 'E' 或 'W', tz: 時區數字 }
```

## 相關工具 Related Tools

奉熙易理研究所其他命理工具(均為付費版):

- 河洛玄機 — 河洛九宮排盤
- 易經配卦 — 六爻配卦推算
- 紫微飛星 — 紫微斗數
- 六日七分擇日 — 擇日吉凶
- 九曜推命 — 九曜星推算

詳見 [winnerich.com](https://winnerich.com)。
