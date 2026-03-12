# Lab 3.1 — India Agriculture Crop Production: Statistical Analysis

## Objective

Is notebook mein **India ke agricultural crop production data** par **descriptive statistics** calculate ki gayi hain — specifically **Wheat** aur **Rice** ki production ke liye **Mean, Median, aur Mode** nikala gaya hai.

---

## Dataset

**File:** `India Agriculture Crop Production.csv`

### Columns

| Column Name | Type | Description |
|---|---|---|
| `State` | object | Indian state ka naam |
| `District` | object | District ka naam |
| `Crop` | object | Fasal ka naam (e.g., Wheat, Rice, Arecanut) |
| `Year` | object | Year (e.g., 2001-02) |
| `Season` | object | Season (e.g., Kharif, Whole Year, Rabi) |
| `Area` | float64 | Fasal ka area |
| `Area Units` | object | Area ki unit (Hectare) |
| `Production` | float64 | Production amount |
| `Production Units` | object | Production ki unit (Tonnes) |
| `Yield` | float64 | Yield per hectare |

---

## Analysis Performed

### 1. Libraries Import ✅
- `numpy` — mean, median calculation
- `pandas` — data loading aur filtering
- `scipy.stats` — mode calculation

### 2. Data Loading ✅
- CSV file load kiya
- `df.head()` se pehle 5 rows inspect kiye

### 3. Data Filtering ✅
- Dataset mein se sirf **Wheat** aur **Rice** ke records alag kiye
- `Production` column ke missing values drop kiye (`dropna`)

### 4. Descriptive Statistics ✅

#### Wheat Production
| Statistic | Value |
|-----------|-------|
| Mean | 1,78,925.07 Tonnes |
| Median | 59,000.0 Tonnes |
| Mode | 1.0 Tonnes |

#### Rice Production
| Statistic | Value |
|-----------|-------|
| Mean | 1,03,667.93 Tonnes |
| Median | 29,100.0 Tonnes |
| Mode | 1,000.0 Tonnes |

> **Note:** Mean >> Median — iska matlab data mein **right skew** hai, yani kuch states mein bahut zyada production hai jo average ko upar khich rahi hai.

---

## Key Findings

- **Wheat ka mean production (1.78 lakh tonnes)** Rice se zyada hai, jo wheat ki India mein dominant role ko darshata hai
- **Median kaafi kam hai Mean se** — data highly skewed hai, kuch bade states (Punjab, Haryana, UP) production mein bahut aage hain
- **Mode bahut kam value hai** — matlab majority districts mein production bahut kam hai

---

## How to Run

```bash
# 1. Dataset file notebook ke saath same folder mein rakh
# India Agriculture Crop Production.csv

# 2. Dependencies install karo
pip install numpy pandas scipy

# 3. Jupyter Notebook chalao
jupyter notebook Lab3_1.ipynb
```

---

## Tech Stack

| Library | Usage |
|---------|-------|
| `pandas` | Data loading, filtering, missing value handling |
| `numpy` | Mean aur Median calculation |
| `scipy.stats` | Mode calculation (`stats.mode`) |

---

## File Structure

```
Lab3_1/
├── Lab3_1.ipynb                          # Main notebook
├── India Agriculture Crop Production.csv # Dataset
└── README.md                             # Yeh file
```
