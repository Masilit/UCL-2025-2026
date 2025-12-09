# UCL 2025-2026 Prediction Competition

A simple web page that displays live standings for a UEFA Champions League prediction competition among friends.

## Features

- 🏆 **Live Updates**: Fetches current UCL standings from the official UEFA API
- 📊 **Automatic Scoring**: Calculates scores based on prediction accuracy
- 🎨 **Simple Design**: Clean, responsive interface
- 🔄 **Auto-Refresh**: Updates results on page refresh

## How It Works

The page:
1. Fetches the latest UEFA Champions League standings from the API
2. Compares them against friends' predictions stored in the CSV file
3. Calculates scores with bonuses for correctly predicting teams in top-8 or positions 9-24
4. Displays the results in a ranked table

## Scoring System

- **Base Score**: Absolute difference between predicted and actual position
- **Bonus**: -3 points for correctly predicting a team in top 8
- **Bonus**: -1 point for correctly predicting a team in positions 9-24
- **Winner**: Person with the lowest total score

## Live URL

Once GitHub Pages is enabled, the page will be available at:
`https://masilit.github.io/UCL-2025-2026/`

## Setup Instructions

### Enable GitHub Pages

1. Go to repository **Settings**
2. Navigate to **Pages** (in the left sidebar)
3. Under **Source**, select **GitHub Actions**
4. The workflow will automatically deploy the site

### Files

- `index.html` - Main web page with embedded JavaScript and predictions data
- `Final_Predictions_standardized.CSV` - Friends' predictions data (also embedded in index.html for simplicity)
- `Results.ipynb` - Original calculation notebook
- `.github/workflows/pages.yml` - GitHub Pages deployment workflow

**Note**: The predictions are embedded directly in the HTML file for simplicity and to avoid CORS issues when loading CSV files. The CSV file is kept for reference and potential future use.

## Local Testing

To test locally:
```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/index.html` in your browser.

**Note**: The API may not work locally due to CORS restrictions, but it will work fine when deployed to GitHub Pages.

## Credits

Data provided by [Football-Data.org API](https://www.football-data.org/)
