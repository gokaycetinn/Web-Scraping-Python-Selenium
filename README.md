## Web Scraping Project

This project collects topics and related data from https://discuss.huggingface.co/c/research/7/l/top forum using Selenium and Python in Google Colab environment. Data is saved in CSV, JSON and TXT formats. Process steps are as follows:

- **Browser Setup with Selenium**:

Chrome WebDriver is used to launch the browser and before launching the browser, some options are added to customize the headers and window (headless, incognito, etc.).
- **Going to the Page**:

The URL (Hugging Face research forum) specified with the driver.get(url) command is visited.
Scrolling the Page:

To load the page content, the page is scrolled at certain intervals (window.scrollTo) and after each scroll, it waits for new content to be loaded. This process is repeated until a certain number of scrolls are made.
- **Data Collection**:

Topics in the forum (title, link, owner, number of replies, number of views, event date) are collected from the relevant HTML elements (By.CLASS_NAME, By.XPATH).

- **Data Saving**:

The collected data is saved in three different formats:

- *CSV*: A CSV file is created containing information such as title, link, owner, number of replies, number of views, event date.

- *JSON*: The same data is saved in JSON format.

- *TXT*: A TXT file is created for each topic, where the title, link, owner, etc. information is written in a text file.

- **Close the Browser**:

After the process is completed, the browser is closed with the driver.quit() command.

As a result, this code collects the topics in the forum, the number of replies and views, and more, and saves this data as CSV, JSON, and TXT files.
