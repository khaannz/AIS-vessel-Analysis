# AIS Vessel Trajectory Analysis

This project analyzes Automatic Identification System (AIS) data to understand vessel movement patterns and identify distinct journeys.

## 📁 Project Structure

```
├── Notebook/
│   ├── ais_data_analysis.ipynb    # Main analysis notebook
│   └── vessel_map.html           # Interactive vessel map (generated)
├── requirements.txt              # Python dependencies
├── .gitignore                   # Git ignore rules
└── README.md                    # This file
```

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- Jupyter Notebook/Lab

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd AIS
   ```

2. **Create virtual environment**
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # Windows
   # source .venv/bin/activate  # Linux/Mac
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Get the data**
   - Place your AIS CSV file in `data/aisdk-2025-03-01.csv`
   - Or update the file path in the notebook

5. **Run the analysis**
   ```bash
   jupyter notebook Notebook/ais_data_analysis.ipynb
   ```

## 📊 What This Analysis Does

### Journey Segmentation
- **Stops**: When vessel speed < 1 knot (docking, anchored)
- **Moving**: When vessel is in motion
- **Journeys**: High-speed transits (≥3 knots, ≥10 minutes)

### Key Features
- ✅ Data quality checks and timestamp validation
- ✅ Invalid position filtering (removes 0,0 coordinates)
- ✅ Automatic journey ID assignment
- ✅ Geographic distance calculations using geopy
- ✅ Interactive folium maps with journey visualization
- ✅ Detailed journey analysis (duration, speed, distance)

### Outputs
- **Speed plots**: Vessel behavior over time
- **Interactive map**: Journey routes with start/end markers
- **Journey table**: Detailed metrics for each trip

## 🗺️ Map Features

The generated map shows:
- **Light blue line**: Complete vessel track
- **Colored lines**: Individual journeys (red, green, purple, etc.)
- **Green markers**: Journey start points with timestamps
- **Red markers**: Journey end points with timestamps  
- **Orange circles**: Stop locations sized by duration

## 📋 Requirements

See `requirements.txt` for complete list:
- pandas: Data manipulation
- numpy: Numerical operations
- matplotlib: Basic plotting
- folium: Interactive maps
- geopy: Geographic distance calculations

## 🤝 Contributing

This is a student project for maritime data analysis. Suggestions welcome!

## 📝 Notes

- Data files are not included in the repository (see `.gitignore`)
- Virtual environments are excluded from version control
- Generated maps are saved as HTML files for easy sharing

