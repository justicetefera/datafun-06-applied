# 🕵️‍♂️ Crime Data Analysis – Project Documentation

## 🧱 Custom Project
Welcome to the documentation site for my applied analytics project. This site explains the purpose, workflow, methods, and results of my analysis of Seattle crime data, completed as part of my datafun‑06‑applied coursework.

### 📦 Basis
This project is built on a large real‑world dataset containing approximately 481,000 police‑reported crime incidents from the City of Seattle. The dataset spans roughly ten years and includes detailed information such as:
- Date and time of occurrence and reporting
- Crime category and subcategory
- Precinct, sector, and beat
- Neighborhood information

The original workflow I started with was the Applied Analytics EDA notebook provided as an example. That example demonstrated a structured, repeatable approach to exploratory data analysis using a clean CO₂ dataset. My goal was to adapt that workflow to a much larger, messier, and more complex dataset — the Seattle crime data — and show that the same principles still apply.
I used the example as a foundation for:
- Notebook structure
- Logging setup
- Data dictionary creation
- Descriptive statistics workflow
- Clean‑view creation
- Group‑by summaries
From there, I expanded the workflow to handle the unique challenges of real‑world crime data.

### 🔧 Phase 4 Modifications
For Phase 4, I implemented a targeted technical modification focused on feature engineering. The raw dataset stored time in HHMM format (e.g., 2114, 0030), which is not directly usable for analysis. To address this, I:
- Created a custom `parse_time()` function to convert HHMM integers into valid datetime.time objects
- Engineered new numeric features: `Occurred Hour`, `Reported Hour`, `Occurred Month`, `Occurred Year`, `Report Delay (Hours)`
- Added logic to compute reporting delays by subtracting the occurred date from the reported date
- Updated the clean‑view logic to drop rows missing any of these engineered fields

I verified the modification by:
- Printing the new columns
- Checking descriptive statistics
- Confirming the clean dataset size changed appropriately
- Ensuring downstream sections (group‑by, describe, plots) worked without errors

This modification was essential because it transformed raw timestamps into structured numeric features that enabled meaningful temporal analysis.

### 🚓 Phase 5 Custom Project
For Phase 5, I applied the full EDA workflow to the Seattle crime dataset and expanded the project significantly beyond the example. My custom project included:

#### ***What I changed from the example***
- Replaced the CO₂ dataset with a 481k‑row crime dataset
- Added extensive feature engineering for dates and times
- Built a new clean‑view pipeline tailored to crime data
- Updated grouping logic to use Crime Subcategory
- Generated descriptive statistics for five engineered numeric features
- Produced new visualizations

#### ***What results I produced***
- A complete data dictionary showing missing values and data types
- Cleaned and engineered dataset ready for analysis
- Summary statistics for all numeric features
- Group‑by statistics for every crime subcategory
- Visual insights into temporal crime patterns
- Identification of patterns such as: Crime peaks around 13–15 hours while Some crimes have extremely long reporting delays

#### ***What I learned***
- This project taught me how to:
- Adapt a structured EDA workflow to a messy, real‑world dataset
- Engineer meaningful features from raw timestamps
- Handle missing values, inconsistent formats, and outliers
- Use logging to track notebook execution
- Build clean subsets for reliable analysis
- Interpret temporal crime patterns
- Manage Git, pre‑commit hooks, and notebook formatting

#### ***How much I exercised the skills***
I used nearly every technique covered in the module:
- Logging
- Data dictionaries
- Feature engineering
- Descriptive statistics
- Group‑by analysis
- Clean‑view creation
- Git workflow
- Pre‑commit automation
- Documentation writing

#### ***Future applications***
These skills can be applied to:
- Public safety analytics
- Time‑series forecasting
- Geospatial crime mapping
- Operational dashboards
- Any dataset involving timestamps, categories, or large‑scale records
This project demonstrates my ability to take a professional EDA workflow and apply it to a complex, real‑world problem.

## How-To Guide

To run this project locally:
1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies using `uv`
4. Run the notebook or scripts inside the `notebooks/` directory

For reference, see the example workflow:
[⭐ **Workflow: Apply Example**](https://denisecase.github.io/pro-analytics-02/workflow-b-apply-example-project/)
to get these projects running on your machine.

## Project Documentation Pages (docs/)

- **Home** - this documentation landing page
- [**Project Instructions**](./project-instructions.md)  - the standard project workflow
- [**Your Files**](./your-files.md) - how to copy the example and create your version
- [**Glossary**](./glossary.md) - project terms and concepts
- [**API**](./api.md) - autogenerated code documentation for the public project interface

The API page is not always easy to read at first,
but it becomes useful as you get more comfortable with project structure,
modules, functions, and docstrings.
