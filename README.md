# 🕸️ Web Scraping Project – Hugging Face Forum

A web scraping project that collects research topics from the [Hugging Face Research Forum](https://discuss.huggingface.co/c/research/7/l/top) using **Selenium** and **Python**, executed in the **Google Colab** environment.

---

## 🚀 Project Overview

This script scrapes discussion topics from the forum and extracts the following details:

- Title  
- Topic link  
- Topic owner  
- Number of replies  
- Number of views  
- Date of last activity

The data is saved in **CSV**, **JSON**, and **TXT** formats.

---

## 🔧 Process Steps

### 1. 🔍 Browser Setup with Selenium

- **Chrome WebDriver** is used to automate the browser.  
- Options such as **headless mode**, **incognito**, and **custom headers** are set.

### 2. 🌐 Navigating to the Page

- The script navigates to the Hugging Face Research Forum using:  
  ```python
  driver.get(url)
  ```

### 3. 📜 Scrolling the Page

- To load dynamic content, the page is scrolled multiple times using:
  ```javascript
  window.scrollTo(0, document.body.scrollHeight)
  ```
- A delay is added between scrolls to allow new content to load.
- The number of scrolls is limited to avoid over-fetching.

### 4. 📊 Data Collection

- Forum topics are extracted using HTML element selectors like:
  - `By.CLASS_NAME`
  - `By.XPATH`
- Collected fields:
  - Title  
  - Link  
  - Owner  
  - Replies  
  - Views  
  - Last activity date

### 5. 💾 Saving Data

- Data is stored in **three formats**:

  - **CSV** – Tabular format  
  - **JSON** – Structured, key-value format  
  - **TXT** – One `.txt` file per topic with detailed content  

### 6. ❎ Closing the Browser

- Once scraping is complete:
  ```python
  driver.quit()
  ```

---

## 📁 Output Files

- `topics.csv`  
- `topics.json`  
- `txt_topics/` – Directory with one `.txt` file per topic  

---

## ✅ Summary

This project efficiently collects structured forum data including views and replies and saves them in multiple formats for further analysis or reporting. It showcases dynamic content handling, Selenium automation, and multi-format export.
