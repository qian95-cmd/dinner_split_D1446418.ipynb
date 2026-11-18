# 🍽️ 聚餐費用分攤與預算判斷系統

- **姓名**：黃佳芊
- **學號**：D1446418
- **作業名稱**：Python 資料型別實作作業：聚餐費用試算器

本專案使用 Python 計算聚餐的服務費、折價後應付總額，以及每人平均分攤金額，並判斷是否超過設定的個人預算。程式收錄於 Jupyter Notebook（`.ipynb`）中，共有三組不同人數與折扣的測試情境。

---

## 📌 功能說明

- **字串清理**：使用 `strip()` 和 `lower()` 清理聚餐名稱。
- **資料轉型**：移除餐費字串中的 `NT$`、千分位逗號與空白，再轉換成數值；將人數字串轉換為整數。
- **費用計算**：依原始餐費計算服務費，扣除折價券後取得應付總額。
- **預算判斷**：計算每人平均費用，並以布林值判斷是否超出預算。
- **格式化輸出**：將金額統一以小數點後兩位格式輸出。

---

## 🛠️ 使用環境

- Python 3
- Google Colab / Jupyter Notebook（執行 `.ipynb` 檔案）
- 不需安裝額外的第三方 Python 套件

---

## 📐 計算公式

```python
service_fee = meal_value * service_rate
total_amount = meal_value + service_fee - discount
amount_per_person = total_amount / people_count
is_over_budget = amount_per_person > budget_per_person
