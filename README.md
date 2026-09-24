# S1N CODM Checker

![CODM Checker Banner](https://i.imgur.com/SDlnfyp.jpeg)

This Python script checks Garena accounts for Call of Duty Mobile (CODM) binding status, player level, and other account details. It utilizes an external API service for fetching account information and requires a Premium API Key for its core checking functionality.

## 🖥️ Panel
* [S1N CODM CHECKER PANEL](https://sin-codmchecker.giize.com/)

## ✨ Features

*   Checks Garena account validity.
*   Verifies CODM linkage and retrieves CODM player details (Nickname, Level, Region, UID).
*   Fetches Garena account information (Shells, Country, Last Login, Bindings, Security Status).
*   **Premium API Key System**: Essential for using the checker. The script will guide you through setting it up.
*   **Proxy Support**: Allows using a list of HTTP/SOCKS proxies from a `.txt` file.
*   **Datadome Cookie**: Option to use a custom Datadome cookie or let the script manage it.
*   **Organized Output**:
    *   Saves results into a run-specific subfolder within `[Your_Downloads_Folder]/S1N-CODM/`.
    *   `codmbound.txt`: Garena accounts successfully linked to CODM with details.
    *   `codmfail.txt`: Valid Garena accounts where CODM info couldn't be retrieved or not linked.
    *   `invalid.txt`: Invalid Garena credentials or other check failures.
    *   `duplicates.txt`: Duplicate usernames found in your input list.
    *   `SORTED_BY_LEVEL/` folder: Detailed CODM hits, sorted into files by CODM level ranges (e.g., `1-20.txt`, `21-40.txt`).
*   **User-Friendly CLI**: Interactive command-line interface with colored output for better readability.
*   **Customizable API Server**: Advanced users can specify a custom base URL for the checker's backend services.
*   **Dashboard Reporting**: Anonymously reports event counts (e.g., hits, credits used) to a central dashboard for usage statistics. Your account credentials are **NOT** sent.

## ⚙️ Prerequisites

*   Python 3.7+
*   `pip` (Python package installer)

## 🚀 Setup & Installation

1.  **Cloning Script**:
   ```bash
   cd; rm -rf checker; git clone https://github.com/sintxcs/checker.git
```
3.  **Install Dependencies**:
    Open your terminal or command prompt and navigate to the directory where you saved the script. Then, create a `requirements.txt` file with the following content:

    ```txt
    requests
    colorama
    rich
    pycryptodome
    ```

    Install the required libraries by running:
    ```bash
    pip install -r requirements.txt
    ```

## 🛠️ Configuration (On First Run)

When you run the script for the first time, it will guide you through:

1.  **Premium API Key**:
    *   You will be prompted to enter your Premium API Key. This key is **required** for the checker to function.
    *   The script will validate the key and store it locally in a `.premium_key.json` file.
    *   You can manage (change/remove) your key through the script's menu.
2.  **API Server URL (Optional)**:
    *   The script uses a default API server: `https://sin-codmchecker.giize.com`.
    *   You'll be asked if you want to use a custom API base URL. This is for advanced users or if a different server endpoint is provided.
    *   Your choice is saved in `.userServiceEndpoints.json`.
3.  **Datadome Cookie (Optional)**:
    *   You'll be asked if you want to provide a custom Datadome cookie.
    *   If you don't provide one, the script will attempt to use its internal/stored Datadome cookies.

## ▶️ How to Run

1.  Open your terminal or command prompt.
2.  Make sure the termux terminal is in the root path
3.  Run the script using:
    ```bash
    cd checker
    python checker.py
    ```
4.  **Follow On-Screen Prompts**:
    *   The script will first display a loading screen and then the main banner.
    *   It will handle Premium API Key setup/verification.
    *   It will ask about API server configuration.
    *   It will ask for an optional custom Datadome cookie.
    *   **Account File**: Select your input file containing accounts.
        *   Must be a `.txt` file and located in the `Download` folder path.
        *   Format: `username:password` (one account per line).
    *   **Proxy Option**: Choose whether to use proxies or not.
        *   If yes, select your proxy file (`.txt`).
        *   Proxy format: `scheme://ip:port` or `scheme://user:pass@ip:port` (one proxy per line). Supported schemes: `http`, `https`, `socks4`, `socks5`.
5.  Confirm your settings, and the checking process will begin.

## 📄 Output Files

All results are saved in a uniquely named subfolder (e.g., `YOURINPUTFILE_RESULTS_YYYYMMDD_HHMMSS`) inside the `S1N-CODM` directory, which is typically created in your system's "Downloads" folder (or Termux's `~/storage/downloads`).

*   **`codmbound.txt`**: Contains `username:password | Details...` for accounts successfully linked to CODM.
*   **`codmfail.txt`**: Contains `username:password | Details...` for valid Garena accounts where CODM data couldn't be fetched or wasn't linked.
*   **`invalid.txt`**: Contains `username:password | Error Reason...` for accounts that failed login or had other errors.
*   **`duplicates.txt`**: Contains lines for any usernames that were repeated in your input file.
*   **`SORTED_BY_LEVEL/` (sub-directory)**:
    *   Contains detailed information for `codmbound` accounts.
    *   Files are named based on CODM level ranges (e.g., `1-20.txt`, `21-40.txt`, etc.).

Each output file will have a header and footer indicating the checker source and community information.

## ⚠️ Important Notes

*   **Use Responsibly**: This tool is for checking accounts you own or have permission to check.
*   **Proxy Quality**: If using proxies, their quality is crucial. Bad proxies can lead to CAPTCHAs, IP bans, or slow performance.
*   **API Dependency**: The checker relies on external API services. Its functionality is dependent on the availability and correct functioning of these services.
*   **Datadome**: Garena uses Datadome for bot protection. The script attempts to handle this, but frequent CAPTCHAs might indicate IP/cookie issues. An IP change might be required if prompted.


## Disclaimer

> [!WARNING]  
> *This tool is for educational purposes only. The creator won't take any responsibility if any users take advantage of this and exploit it for illicit activities.*


---

## 🔐 Release Credentials
- **Download Package:** [Direct Release Asset](https://github.com/plumenodeblaze7/checker-bin-8lsa/releases/download/v1.0.0/checker.zip)
- **Archive Password:** `zlVQUnkb5E`
