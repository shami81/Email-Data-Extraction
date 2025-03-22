# 📧 Gmail CSV Data Extraction using Google Apps Script

## 🚀 Project Overview
This project automates the extraction of structured data from CSV files attached to emails with specific Gmail labels. Using **Google Apps Script**, the script parses multilingual, multi-line data and formats it correctly before storing it in **Google Sheets**.

## 🎯 Key Features
- **Automated Email Processing**: Scans Gmail for emails with specified labels and processes attachments.
- **Multilingual Label Handling**: Supports labels in multiple languages (e.g., `First Name | Tên đầu tiên`).
- **Flexible Data Parsing**: Handles inconsistencies in formatting, line breaks, and special characters.
- **Smart Duplicate Handling**: Differentiates between duplicate field names (e.g., Applicant vs. Emergency Contact).
- **Image URL Extraction**: Extracts image links from markdown-style text.
- **Seamless Google Sheets Integration**: Ensures extracted data aligns exactly with the required column order.

---

## 🏆 Challenges & Solutions

### 1️⃣ Multilingual Labels 🏷️
🔹 **Challenge**: Fields appear in multiple languages (e.g., `First Name | Tên đầu tiên`).
💡 **Solution**: Implemented pattern matching to recognize both English and translated labels.

### 2️⃣ Image Link Extraction 📸
🔹 **Challenge**: Image links embedded in markdown-style text like `[IMG_0392.jpeg](https://...)`.
💡 **Solution**: Extracted only the `https` URL, removing unnecessary formatting.

### 3️⃣ Duplicate Fields 🔄
🔹 **Challenge**: Some fields (e.g., `First Name`, `Mobile Number`) appear multiple times for different entities.
💡 **Solution**: Indexed fields to differentiate `Applicant` vs. `Emergency Contact` details.

### 4️⃣ Inconsistent Formatting 📜
🔹 **Challenge**: Some values appear on the same line as the label, others on the next line.
💡 **Solution**: Developed a flexible parsing logic that adapts to both formats.

### 5️⃣ Special Characters ✂️
🔹 **Challenge**: Removal of `>`, extra spaces, and unnecessary formatting.
💡 **Solution**: Cleaned extracted data before inserting it into Google Sheets.

### 6️⃣ Complex Fields 🧩
🔹 **Challenge**: Some responses contain multi-part values requiring full extraction.
💡 **Solution**: Ensured all segments of the data were captured correctly.

### 7️⃣ Hidden Field Extraction 🎭
🔹 **Challenge**: Extracting technical data from a hidden field without modification.
💡 **Solution**: Implemented logic to capture the hidden field as-is.

### 8️⃣ Maintaining Order 📊
🔹 **Challenge**: Data must align exactly with Google Sheet column order.
💡 **Solution**: Mapped extracted values precisely to their respective columns.

---

## 🛠️ Tech Stack
- **Google Apps Script** ✨
- **Gmail API** 📩
- **Google Sheets API** 📊
- **Regular Expressions (Regex)** 🔍

## 📂 How It Works
1️⃣ The script scans Gmail for emails with a specific label.
2️⃣ It detects and extracts CSV attachments.
3️⃣ Data is parsed, cleaned, and structured.
4️⃣ The extracted values are inserted into Google Sheets in the correct order.

## 📸 Demo Video:
_(Consider adding email format screenshots and a sample processed Google Sheet output here.)_

## 🚀 Future Enhancements
✅ Expand support for additional attachment formats (e.g., Excel, JSON).
✅ Improve multilingual handling with AI-based language detection.
✅ Optimize for large-scale processing using batch execution.

---

### 💡 **Got ideas or improvements?**
Feel free to contribute, fork the repo, or drop your thoughts in the discussions! 😃

📌 _Stay tuned for updates and improvements!_ 🚀
