# 🛒 E-commerce Price Monitoring & Product Data Scraper

## 📌 Project Overview
This project is a professional Python-based web scraping solution for collecting and monitoring product data from e-commerce websites. It extracts key details such as product names, prices, vendors, and availability, then delivers clean, structured datasets in CSV, Excel, and JSON formats.  

The project highlights a client-ready, ethical approach to web scraping with outputs designed for business analysis, automation, and reporting.  

> *Note: This project was developed and tested on live e-commerce data. For portfolio purposes, only sanitized sample outputs are included to ensure legal and ethical compliance.*

---

## ⚙️ Features  
- **Accurate Product Data** – Titles, prices, vendors, availability, SKUs, and links.  
- **Pagination Handling** – Automatically collects data across all product pages.  
- **Clean, Structured Outputs** – Deduplicated and normalized datasets.  
- **Multiple Export Formats**:  
  - `products.csv` – Clean product dataset  
  - `variants.csv` – Variant-level details  
  - `products.xlsx` – Excel with multiple sheets (Products & Variants)  
  - `products.json` – Raw structured data  
- **Ethical & Professional Practices** – Custom User-Agent, robots.txt compliance, and polite rate limiting.  

---

## 📂 Project Structure  

press_scraper/  
│  
├── scraper/  
│   ├── fetch_products_api.py     # Fetches product data with pagination (API-based)  
│   ├── parse_products.py         # Cleans and structures raw product data  
│   ├── export_products.py        # Exports datasets to CSV, JSON, Excel  
│   ├── rate_limiter.py           # Polite scraping with basic rate limiting  
│   ├── robots_checker.py         # Checks robots.txt compliance  
│  
├── outputs/                      # Sample sanitized outputs (no real URLs)  
│   ├── products.json  
│   ├── products.csv  
│   ├── products_clean.csv  
│   ├── products.xlsx  
│  
├── screenshots/                  # Portfolio screenshots  
│   ├── run_and_structure.png     # Combined terminal run + project structure  
│   ├── excel_output.png          # Sanitized Excel output sample  
│   ├── code_snippet.png          # Key code excerpt (sanitized)  
│  
├── README.md  
└── requirements.txt  

---


---


---

## 📊 Sample Output (Sanitized)  

> *Note: Dataset samples (CSV, JSON, Excel) are fully sanitized for legal and ethical reasons. The terminal screenshot shows a real scraper run on live data, but no raw client data is shared.*  

### Example CSV (`products.csv`)  

| id         | title            | handle             | vendor      | price_min | price_max | url                               |
|------------|-----------------|------------------|------------|-----------|-----------|----------------------------------|
| 1000000001 | Sample Product A | sample-product-a | Demo Store | 19.99     | 19.99     | https://www.example.com/product-a |
| 1000000002 | Sample Product B | sample-product-b | Demo Store | 24.99     | 29.99     | https://www.example.com/product-b |

### Example JSON (`products.json`)  

```json
[
  {
    "id": 1000000001,
    "title": "Sample Product A",
    "handle": "sample-product-a",
    "vendor": "Demo Store",
    "price_min": 19.99,
    "price_max": 19.99,
    "url": "https://www.example.com/product-a"
  },
  {
    "id": 1000000002,
    "title": "Sample Product B",
    "handle": "sample-product-b",
    "vendor": "Demo Store",
    "price_min": 24.99,
    "price_max": 29.99,
    "url": "https://www.example.com/product-b"
  }
]


🚀 How It Works

1. **Activate the virtual environment**
   Windows (PowerShell): & venv\Scripts\Activate.ps1
   Linux / MacOS: source venv/bin/activate
   ![Run and structure](screenshots/run_and_structure.png)  
   *📸 Screenshot: Running the scraper project and viewing folder structure*  

2. **Run the scraper to fetch products**  
   python -m scraper.fetch_products_api  
   ![Code snippet](screenshots/code_snippet.png)  
   *📸 Screenshot: Example code snippet from `fetch_products_api.py`*  

3. **Parse and clean the data**  
   python -m scraper.parse_products  

4. **Export the datasets**  
   python -m scraper.export_products  
   ![Excel output](screenshots/excel_output.png)  
   *📸 Screenshot: Cleaned product dataset exported to Excel*  

All processed files are saved inside the `outputs/` folder:  
- `products.csv` – Clean dataset  
- `products.xlsx` – Excel report (Products & Variants sheets)  
- `products.json` – Raw structured data  

---

## ⚙️ Installation & Usage  

1. Clone the Repository  
   git clone https://github.com/Ek-Coder-Tech/press_scraper.git  
   cd press_scraper  

2. Create a Virtual Environment  
   - Windows: python -m venv venv && venv\Scripts\activate  
   - Linux/Mac: python3 -m venv venv && source venv/bin/activate  

3. Install Dependencies  
   pip install -r requirements.txt  

4. Run the Workflow  
   # Step 1: Fetch product data  
   python -m scraper.fetch_products_api  

   # Step 2: Parse & clean product data  
   python -m scraper.parse_products  

   # Step 3: Export to CSV, Excel, JSON  
   python -m scraper.export_products  

The final structured outputs will be available in the `outputs/` directory.  

---

## ⚙️ Technologies Used  
- Python 3.11 – Core language  
- Requests – Fetch product data via API  
- JSON & CSV modules – Structured outputs  
- OpenPyXL – Excel reporting  

---

## 🎯 Use Cases  
This scraper can be adapted for:  
- 📊 Price Monitoring – Track competitor pricing trends  
- 🛒 E-Commerce Catalogs – Feed structured data into ERP/CRM systems  
- 📑 Market Research – Collect clean datasets for analysis  
- ⚙️ Workflow Automation – Integrate into pipelines or dashboards  

---

## 💼 How Clients Benefit  
- 📊 Price Tracking & Market Research – Monitor competitors’ pricing and availability  
- 🛒 Catalog Management – Automate updates to product listings  
- ⚙️ Business Automation – Connect clean data with ERP/CRM workflows  
- 📑 Reporting & Analytics – Generate dashboards and insights directly from structured data  

---

## 🔮 Next Steps / Future Improvements  

This project demonstrates a strong foundation for professional e-commerce scraping. Future enhancements can expand its business value and technical robustness:  

- 🌍 **Multi-Site Support** – Unify data collection across multiple e-commerce platforms.  
- 📦 **Variant & Inventory Tracking** – Monitor stock levels, sizes, and color variations.  
- 📈 **Historical Price Tracking** – Record and analyze pricing trends over time.  
- 🔔 **Automated Alerts** – Notify via email/Slack when products restock or prices change.  
- 🗄️ **Database Integration** – Store results in SQL/NoSQL databases for scalability.  
- ☁️ **Cloud Deployment** – Run scheduled scrapers using Docker, GitHub Actions, or cloud services.  
- 📊 **Analytics & Dashboards** – Feed clean data into BI tools (Power BI, Tableau, Metabase) for decision-making.  
- 🔐 **Advanced Rate Limiting & Proxies** – Strengthen compliance and resilience against request blocks.  

---

## ⚖️ Legal & Professional Standards  

This project follows ethical scraping practices:  
- ✅ Respects `robots.txt` directives  
- ✅ Uses polite rate limiting  
- ✅ No login, personal, or private data is collected  
- ✅ Portfolio/demo use only — not intended for unauthorized commercial deployment  

*Important: Always review a website’s terms of service before deploying scrapers in production.*  

---

## 📄 License / Disclaimer  

This repository is provided **for educational and portfolio purposes only**.  
- No live client or proprietary data is included.  
- Example outputs are fully sanitized.  
- The author assumes no liability for misuse of this project.  

Licensed under the MIT License — you are free to use and adapt with attribution.  

---

## 🙌 Acknowledgments / Author Info  

Developed by **Eric — Python Automation & Web Developer**  
- 🔗 GitHub: [https://github.com/Ek-Coder-Tech]  
- 💼 Upwork: [https://www.upwork.com/freelancers/~012558bab6232e8e65]  
- 🎯 Fiverr: [https://www.fiverr.com/sellers/eric_mutisya/edit]  

Special thanks to the Python open-source community for the libraries and tools that made this project possible.  