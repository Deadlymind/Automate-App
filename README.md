
#### Purpose:
This application automates various tasks including searching for company contact emails on Google and Facebook, updating Google Sheets with specific formulas, and automating annuCapt based on keywords and department numbers.

#### Key Features:

1. **User Interface:**
   - Built with PyQt5, it allows users to start and stop automation tasks and import data files.

2. **Automation Tasks:**
   - **Google Sheets Automation:** Updates cells in a Google Sheet with a formula to search for company information.
   - **Email Search Automation:** Searches Google and Facebook for company emails and extracts them.
   - **Keyword and Department Automation:** Automates web interactions using keywords and department numbers.

3. **Thread Management:**
   - Uses separate threads to handle tasks, keeping the UI responsive.
   - Threads perform tasks and update the UI with progress and log messages.

4. **Logging and Error Handling:**
   - Implements detailed logging for tracking progress and errors.
   - Displays log messages in the UI and saves them to a file.

5. **Google Sheets Integration:**
   - Uses `gspread` and Google OAuth2 credentials for interacting with Google Sheets.

6. **Web Scraping and Automation:**
   - Utilizes `selenium` for web interactions, including Facebook login and search.
   - Extracts email addresses using regular expressions.

7. **Email Notifications:**
   - Takes screenshots and sends them via email using `smtplib`.

#### Main Components:

1. **Main Application Window:**
   - Handles UI elements and user interactions.
   - Connects buttons to functions for starting/stopping automation tasks.
   - Uses a timer to process log messages and update the UI.

2. **Worker Threads:**
   - **WorkerThread1:** Updates Google Sheets with search formulas.
   - **WorkerGoogleFBSearch:** Searches Google and Facebook for emails and saves results.
   - **WorkerKeywordsAndDepartments & WorkerNumbersOnly:** Automate web interactions based on provided data.

3. **Utility Functions:**
   - **`hide_console()` & `is_admin()`:** Manage console visibility and admin privileges.
   - **`take_screenshot()` & `send_email()`:** Handle screenshots and email notifications.

4. **Web Automation Functions:**
   - **`init_driver()`:** Initializes Selenium WebDriver.
   - **`search_google()` & `search_facebook()`:** Perform web searches.
   - **`login_facebook()`:** Logs into Facebook.
   - **`extract_emails()`:** Extracts emails from web pages.

#### Usage:

- Run the script to launch the application.
- Enter required information in the UI and start automation tasks with the corresponding buttons.
- Progress and log messages are displayed in the UI, and results are saved to files. 

