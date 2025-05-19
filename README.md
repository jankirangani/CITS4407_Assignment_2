# CITS4407 Assignment 2 – Board Games Dataset Analysis
research with shell script of Board Games or Bored Games: which type and mechanics of board-game rules

**Name:** Janki Rangani  
**Student ID:** 24095031

## Overview

This assignment explores and analyzes the Board Game Geek dataset to answer key research questions using Bash scripting and UNIX tools. The project involves three main components:

- **Data quality checking**
- **Data cleaning**
- **Data analysis**

All scripts were written in Bash and tested using the Docker environment provided by the professor Mr.Michel Wise.

---

## Files Included

| File Name         | Purpose                                             |
|-------------------|-----------------------------------------------------|
| `empty_cells`     | Reports the number of empty cells in each column    |
| `preprocess`      | Cleans the raw dataset and outputs a tab-separated file |
| `analysis`        | Performs statistical and categorical analysis       |
| `README.md`       | Describes the project, usage, and file details      |
| `bgg_dataset.txt` | Full BoardGameGeek dataset                          |
| `bgg_cleaned.tsv` | Cleaned version of `bgg_dataset.txt`                |
| `Sample Files`    | All the other files provided in the Assignment      |

---

## How to Run

### 1. Check for empty cells

This script checks for missing (empty) values in each column of a raw `.txt` dataset using the specified delimiter (semicolon).


```bash
./empty_cells bgg_dataset.txt ";"
```

### 2. Clean the raw dataset

The preprocess script converts the raw semicolon-separated file to a clean tab-separated file, replaces decimal commas, strips non-ASCII characters, ensures each row has 14 fields, and fills in missing IDs.

```bash
./preprocess bgg_dataset.txt > bgg_cleaned.tsv
```

### 3. Analyze the cleaned dataset

The analysis script answers the 4 research questions based on the cleaned data file.

```bash
./analysis bgg_cleaned.tsv
```

Each run of the analysis script prints:

The most popular game mechanics
The most popular game domain
The correlation between year published and average rating
The correlation between complexity and average rating

All numeric correlations are shown with 3 decimal places.




