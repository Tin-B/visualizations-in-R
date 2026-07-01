# visualizations-in-R
one note: since `streamgraph` is no longer actively maintained and had compatibility issues with R 4.5.1,for this reason multiple implementations are included.

# 📊 Baby Names Data Visualization in R

## Overview

This project explores different approaches to visualizing the popularity of selected female baby names over time using R. The same dataset is visualized using multiple libraries to compare their capabilities, strengths, and limitations.

The visualizations were created using:

* **ggplot2** (static stacked area chart)
* **plotly** (interactive stacked area chart)
* **streamgraph** (interactive streamgraph)
* **gganimate** (animated bubble chart using the Gapminder dataset)

---

## Dataset

### Baby Names Dataset

The project uses the **babynames** dataset together with a sample CSV containing historical baby name records.

The analysis focuses on the following names:

* Ashley
* Amanda
* Jessica
* Patricia
* Linda
* Deborah
* Dorothy
* Betty
* Helen

Only female (`sex == "F"`) observations were included.

---

## Visualizations

### 1. ggplot2

A stacked area chart was created using **ggplot2** to display how the popularity of selected names changes over time.

**Features**

* Clean static visualization
* Publication-ready graphics
* Custom colour palettes
* Easy customization

---

### 2. Plotly

The same visualization was recreated using **plotly** to provide an interactive experience.

**Features**

* Hover tooltips
* Zoom and pan functionality
* Interactive legend
* Responsive visualization

---

### 3. Streamgraph

An interactive streamgraph was developed using the **streamgraph** package.

**Features**

* Smooth flowing layout
* Interactive legend
* Hover information

**Note**

The `streamgraph` package is no longer actively maintained and produces compatibility warnings with recent versions of R (R 4.5+) and modern `htmlwidgets`. The implementation is included for comparison and educational purposes.

---

### 4. Animated Bubble Chart

Using the **Gapminder** dataset together with **gganimate**, an animated bubble chart was created showing:

* GDP per capita
* Life expectancy
* Population size
* Continents
* Changes over time

The animation was exported as a GIF.

---

## Packages Used

```r
library(tidyverse)
library(ggplot2)
library(plotly)
library(streamgraph)
library(gganimate)
library(gapminder)
library(babynames)
```

---

## Repository Structure

```
├── data/
│   └── babynames_sample.csv
│
├── scripts/
│   ├── ggplot_visualization.R
│   ├── plotly_visualization.R
│   ├── streamgraph_visualization.R
│   └── gganimate_visualization.R
│
├── output/
│   ├── ggplot.png
│   ├── plotly.html
│   ├── streamgraph.html
│   └── FourthGraph.gif
│
└── README.md
```

---

## How to Run

1. Clone the repository.

2. Install the required packages.

```r
install.packages(c(
  "tidyverse",
  "ggplot2",
  "plotly",
  "gganimate",
  "gapminder",
  "babynames"
))
```

3. Open the desired R script.

4. Run the script to reproduce the visualization.

---

## Key Learning Outcomes

This project demonstrates:

* Data wrangling using **dplyr**
* Time-series visualization
* Static and interactive graphics
* Animation with **gganimate**
* Comparison of multiple R visualization libraries
* Exporting visualizations for presentations and reports

---

## Author

**Tinotenda**

Bachelor of Science Honours in Data Science and Systems

University of Zimbabwe
