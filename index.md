---
layout: page
title: "Bigfoot Sightings Visualization"
---

# Bigfoot Sightings Analysis

This page presents visualizations of Bigfoot‑sightings data across the United States using the dataset from the Bigfoot Field Researchers Organization (BFRO).  
Explore trends by year, by state, and dive into an interactive view by state over time.

## Visualization 1: Sightings by Year 

**Description:**

The first visualization is a bar chart displaying the number of Bigfoot Sightings by year. Each bar represents the total numbers of sightings in a given year, allowing for easy understanding of sightings, as well as trends and patterns. 

**Design Choices:**

-The X axis was encoded as an ordinal variable and sorted into chronological order, to ensure that the chart would display the years in chronological order rather than sorting them based on the number of sightings in that year.

-The y-axis was encoded as quantitative to show the number of sightings. 

-The color was encoded as quantitative, and the color scheme was “oranges”, further visualizing the years that had more sightings. By making the years with a greater number of sightings darker, it can enhance the contrast and show patterns in the years. By using a color scheme with a single color it also allows individuals with color blindness or other visual impairments understand the pattern using the contrast of the colors, rather than the colors themselves, ensuring the chart is accessible. 

This visualization is static, so it cannot be interacted with. 
{% include_relative by_year.html %}

## Visualization 2: Sightings by State 
**Description:**

The second visualization is a bar chart showing the total number of Bigfoot sightings in each U.S state. Each horizontal bar represents a state, and the length is the total number of sightings in that state. This plot can help identify some geography information and show which states have more sightings. 

**Design Choices:**

-The X-axis of this chart is quantitative, and is encoded with the number of sightings.

-The Y-axis is encoded as nominal categorical variables, since the labels are state names and don't have an inherent numeric order assigned to them. I sorted the bars in descending order to show the states with the most sightings on the top of the graph. 

-The color is also quantitative, and has a sequential blue color scale for a similar reason as the first chart: to show the magnitude of the sightings and make the contrast easier to visually compare them. From this choice, it is easily understood that Washington has far more sightings than any other state even without looking at the actual number of reports. 

-The data was aggregated by state, and this chart is static, and not interactable. The horizontal orientation, compared to vertical, makes it easier to read the states and make the chart overall easier to read and understand. 
{% include_relative by_state.html %}

## Visualization 3: Yearly Sightings by State (Interactive)  
**Description:**

The third visualization is an interactive line chart showing how Bigfoot sightings have changed over time for a particular state. Users can select the state from a dropdown menu located at the bottom of the chart, and the chart updates to show that state’s sightings by year. Every point represents the number of sightings in a given year, clearly displaying trends and changes. 

**Design Choices:**

-The X_axis is encoded as ordinal, and shows the chronological order of the years where sightings have occurred. 

-The Y_axis is quantitative, and displays the number of sightings, which corresponds to the line as points in the line graph. 

-The Color is a set, fixed color of midnight blue, contrasting against the white background and making it easier to see the line, even if an individual is usually impaired. I aggregated the dataset by both year and state to allow for the chart to calculate yearly sightings by state. 

**Interactivity:**

The chart is interactive using the dropdown menu, interactive sizing option,and the tooltip. The dropdown menu allows for a user to choose which state they want to look into with more detail. The .interactive() feature makes it easy to adjust the size of the line chart for visibility and exploratory purposes. The tooltip allows for a user to hover over a particular point, which will display the state, year and count, making it even easier to see. 
{% include_relative inter.html %}

### Data & Analysis  
[The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/bfro_reports_fall2022.csv)  
[The Analysis](https://github.com/mtrzu/mtrzu.github.io/blob/main/python_notebooks/Workbook.ipynb)

---