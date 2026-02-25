# Website HTML Fetcher

This project provides a simple, browser-based tool to fetch and view the raw HTML source code of any website. It's designed to be user-friendly, allowing you to quickly get the underlying HTML of a webpage.

## Features

*   **Fetch HTML from any URL:** Simply enter a website URL, and the tool will retrieve its HTML content.
*   **CORS Bypass:** Uses a proxy (`allorigins.win`) to circumvent Cross-Origin Resource Sharing (CORS) restrictions, allowing you to fetch HTML from almost any domain directly from your browser.
*   **Automatic HTTPS:** If you enter a URL without `http://` or `https://`, the tool automatically prepends `https://` for convenience.
*   **Copy to Clipboard:** Easily copy the fetched HTML content to your clipboard with a single click.
*   **Download HTML File:** Download the retrieved HTML as an `.html` file to your local machine.
*   **Responsive User Interface:** The application's layout adjusts to fit various screen sizes, from desktops to mobile devices.
*   **Simple & Intuitive Design:** A clean and easy-to-understand interface makes it straightforward to use for beginners.
*   **Request Cooldown:** Prevents rapid-fire requests to the fetching service.

## Limitations

*   **Reliance on Third-Party Proxy:** The tool depends on the `allorigins.win` proxy service. If this service becomes unavailable or changes, the fetching functionality will cease to work.
*   **Website Blocking:** Some websites may employ measures to block requests originating from known proxies or automated tools, which can prevent the HTML from being fetched successfully.
*   **Client-Side Only (No JavaScript Execution):** This tool fetches the *initial* HTML document. It does not execute client-side JavaScript on the target website. Therefore, it will not retrieve content that is dynamically loaded or rendered by JavaScript after the initial page load (e.g., content on Single-Page Applications - SPAs).
*   **Request Cooldown Period:** There's a 5-second waiting period between fetch requests to avoid overwhelming the proxy service.
*   **No Advanced Fetching Options:** The tool does not offer options for custom headers, user-agent spoofing, or specific element scraping.
*   **Potential for Misuse:** While intended for educational and utility purposes, an accessible HTML fetcher could potentially be misused for less ethical activities if hosted publicly without proper rate limiting or abuse prevention.

## How to Use (Beginner-Friendly Guide)

This tool is very simple to use! Follow these steps:

1.  **Open the Application:** Open the `index.html` file in your web browser. You'll see a simple page with an input box and a button.

2.  **Enter a Website URL:**
    *   Look for the text box labeled "Website URL".
    *   Type or paste the full address of the website you want to get the HTML from.
    *   **Example:** If you want to get the HTML for Google, you would type `https://www.google.com`.
    *   Don't worry if you forget `http://` or `https://`; the tool will try to add `https://` automatically.

3.  **Fetch the HTML:**
    *   Click the big "Fetch HTML" button.
    *   The tool will then contact the website and try to get its HTML code.
    *   You'll see a message like "Fetching HTML... Please wait." in the "Fetched HTML" area.
    *   If you try to click the button too quickly, it will tell you to "Wait Xs" for a few seconds. This is normal!

4.  **View the HTML:**
    *   Once fetched, the raw HTML code of the website will appear in the large box labeled "Fetched HTML".
    *   You can scroll through this box to see all the code that makes up the webpage.

5.  **Copy the HTML (Optional):**
    *   If you want to save the code or use it somewhere else, click the "Copy HTML" button.
    *   A small message "Copied!" will briefly appear on the button to confirm.
    *   Now you can paste the HTML into a text editor, a document, or anywhere else!

6.  **Download the HTML (Optional):**
    *   If you prefer to save the HTML as a file, click the "Download HTML" button.
    *   Your browser will then download a file named `downloaded_site.html` (or similar) to your computer's downloads folder. You can then open this file with a text editor or web browser.

**Important Tip for SPAs (Single-Page Applications):**
If you fetch a website that looks mostly empty or doesn't show all the content you expect (like a Facebook feed or a complex dashboard), it's probably a "Single-Page Application." These websites load most of their content using JavaScript *after* the initial HTML is fetched. This tool only gets the *initial* HTML, so it won't see that dynamically loaded content.
