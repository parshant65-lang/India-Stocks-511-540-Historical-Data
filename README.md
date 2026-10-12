# India-Stocks-511-540-Historical-Data

Institutional Historical 1-Minute Market Data Archive for **India Equities (Constituents 511 to 540)** with automated daily cloud capture via GitHub Actions.

---

## 🏛️ Directory Hierarchy

```text
India-Stocks-511-540-Historical-Data/
├── .github/workflows/daily_ingest.yml
├── fetch_batch.py
├── README.md
├── <SYMBOL>/
│   └── 1m/
│       ├── README.md
│       └── <YYYY>/
│           └── <MM>/
│               ├── <SYMBOL>_1m_<YYYY-MM-DD>.csv
```

---

## ⏰ 4-Tier Automated Schedule (Mon–Fri)

| Trigger | Time (IST) | Cron (UTC) | Role |
|:---|:---:|:---:|:---|
| **Primary Trigger** | **15:45 IST** | `15 10 * * 1-5` | 15 mins post-market close |
| **Backup Trigger 1** | **16:45 IST** | `15 11 * * 1-5` | 1 hour safety net |
| **Backup Trigger 2** | **17:45 IST** | `15 12 * * 1-5` | 2 hours safety net |
| **Backup Trigger 3** | **18:45 IST** | `15 13 * * 1-5` | 3 hours safety net |

---

## 📦 Constituents (511 to 540)

| # | Symbol | Company Name | Yahoo Ticker |
|---|---|---|---|
| 511 | `5PAISA` | 5Paisa Capital Limited | `5PAISA.NS` |
| 512 | `63MOONS` | 63 moons technologies limited | `63MOONS.NS` |
| 513 | `A2ZINFRA` | A2Z Infra Engineering Limited | `A2ZINFRA.NS` |
| 514 | `AAATECH` | AAA Technologies Limited | `AAATECH.NS` |
| 515 | `AAKASH` | Aakash Exploration Services Limited | `AAKASH.NS` |
| 516 | `AAREYDRUGS` | Aarey Drugs & Pharmaceuticals Limited | `AAREYDRUGS.NS` |
| 517 | `AARNAV` | Aarnav Fashions Limited | `AARNAV.NS` |
| 518 | `AARON` | Aaron Industries Limited | `AARON.NS` |
| 519 | `AARTECH` | Aartech Solonics Limited | `AARTECH.NS` |
| 520 | `AARTIDRUGS` | Aarti Drugs Limited | `AARTIDRUGS.NS` |
| 521 | `AARTIPHARM` | Aarti Pharmalabs Limited | `AARTIPHARM.NS` |
| 522 | `AARTISURF` | Aarti Surfactants Limited | `AARTISURF.NS` |
| 523 | `AARVI` | Aarvi Encon Limited | `AARVI.NS` |
| 524 | `AASTHA` | Aastha Spintex Limited | `AASTHA.NS` |
| 525 | `ABAN` | Aban Offshore Limited | `ABAN.NS` |
| 526 | `ABANSENT` | Abans Enterprises Limited | `ABANSENT.NS` |
| 527 | `ABCOTS` | A B Cotspin India Limited | `ABCOTS.NS` |
| 528 | `ABFRL` | Aditya Birla Fashion and Retail Limited | `ABFRL.NS` |
| 529 | `ABINFRA` | A B Infrabuild Limited | `ABINFRA.NS` |
| 530 | `ABLBL` | Aditya Birla Lifestyle Brands Limited | `ABLBL.NS` |
| 531 | `ABMINTLLTD` | ABM International Limited | `ABMINTLLTD.NS` |
| 532 | `ABMKNO` | ABM Knowledgeware Limited | `ABMKNO.NS` |
| 533 | `ACCELYA` | Accelya Solutions India Limited | `ACCELYA.NS` |
| 534 | `ACCURACY` | Accuracy Shipping Limited | `ACCURACY.NS` |
| 535 | `ACEINTEG` | Ace Integrated Solutions Limited | `ACEINTEG.NS` |
| 536 | `ACEVECTOR` | AceVector Limited | `ACEVECTOR.NS` |
| 537 | `ACGL` | Automobile Corporation of Goa Limited | `ACGL.NS` |
| 538 | `ACI` | Archean Chemical Industries Limited | `ACI.NS` |
| 539 | `ACL` | Andhra Cements Limited | `ACL.NS` |
| 540 | `ACSTECH` | ACS Technologies Limited | `ACSTECH.NS` |


---

## ⚡ 1-Line Pandas Stream Loader

```python
import pandas as pd

# Example: Stream 5PAISA 1m data
url = "https://raw.githubusercontent.com/parshant65-lang/India-Stocks-511-540-Historical-Data/main/5PAISA/1m/2026/10/5PAISA_1m_2026-10-12.csv"
df = pd.read_csv(url)
print(df.head())
```
