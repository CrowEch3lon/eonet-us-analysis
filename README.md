# eonet-us-analysis
Exploratory analysis of US natural disaster events using the NASA EONET v3 API. Includes density mapping, temporal frequency analysis, and wildfire hotspot identification by state.

## View:
https://nbviewer.org/github/CrowEch3lon/eonet-us-analysis/blob/main/eonet-us-analysis.ipynb

## Setup

1. Clone the repo
2. Create a `.env` file in the root directory:

    NASA_API_KEY=your_nasa_key_here
    MAPBOX_TOKEN=your_mapbox_token_here

3. Create and activate a virtual environment:
```bash
   python -m venv .venv
   source eonet-us-analysis/bin/activate
```
4. Register the kernel:
```bash
   pip install ipykernel
   python -m ipykernel install --user --name=eonet-us-analysis
```
5. Open `eonet-us-analysis.ipynb` in VSCode, select the `eonet-us-analysis` kernel, and run the notebook -- dependencies install automatically in the first cell

## Run Modes

- **Full run:** No cached data found. Fetches from EONET API, saves CSVs to `data/`.
- **Staging mode:** CSVs already exist. API is not called. Geocoding also skipped if cached.

## Questions Explored

1. Where do natural disasters cluster most densely in the US?
2. Is the frequency of a specific event type increasing over time?
3. Which months or seasons see the highest event activity?
4. Which US states are most prone to wildfires?

## Data Source

[NASA EONET v3 API](https://eonet.gsfc.nasa.gov/docs/v3)

## Dependencies

| Package | Version |
|---|---|
| certifi | 2026.4.22 |
| geographiclib | 2.1 |
| geopy | 2.4.1 |
| numpy | 2.4.2 |
| pandas | 3.0.1 |
| plotly | 6.7.0 |
| python-dotenv | 1.2.2 |
| requests | 2.33.1 |