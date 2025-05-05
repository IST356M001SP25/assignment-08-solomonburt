# Reflection

Student Name: Solomon Burt
Sudent Email:  sdburt@syr.edu

## Instructions

Reflection is a key activity of learning. It helps you build a strong metacognition, or "understanding of your own learning." A good learner not only "knows what they know", but they "know what they don't know", too. Learning to reflect takes practice, but if your goal is to become a self-directed learner where you can teach yourself things, reflection is imperative.

- Now that you've completed the assignment, share your throughts. What did you learn? What confuses you? Where did you struggle? Where might you need more practice?
- A good reflection is: **specific as possible**,  **uses the terminology of the problem domain** (what was learned in class / through readings), and **is actionable** (you can pursue next steps, or be aided in the pursuit). That last part is what will make you a self-directed learner.
- Flex your recall muscles. You might have to review class notes / assigned readings to write your reflection and get the terminology correct.
- Your reflection is for **you**. Yes I make you write them and I read them, but you are merely practicing to become a better self-directed learner. If you read your reflection 1 week later, does what you wrote advance your learning?

Examples:

**Poor Reflection:**  "I don't understand loops."   
**Better Reflection:** "I don't undersand how the while loop exits."   
**Best Reflection:** "I struggle writing the proper exit conditions on a while loop." It's actionable: You can practice this, google it, ask Chat GPT to explain it, etc. 

**Poor Reflection** "I learned loops."   
**Better Reflection** "I learned how to write while loops and their difference from for loops."   
**Best Reflection** "I learned when to use while vs for loops. While loops are for sentiel-controlled values (waiting for a condition to occur), vs for loops are for iterating over collections of fixed values."

`--- Reflection Below This Line ---`

This assignment focused on the ETL process for data visualization, specifically addressing the common scenario where data requires further transformation even after initial cleaning. The task involved creating two Streamlit dashboards to visualize parking ticket data from Syracuse, NY. The source data, final_cuse_parking_violations.csv, contained information about individual parking tickets, including location, time of issuance, and fine amount.

The assignment was divided into two main parts. The first part required completing the etl.py script to perform specific data transformations. This involved creating three functions: top_locations, which identified locations with $1,000 or more in total fines; top_locations_mappable, which augmented the top locations data with latitude and longitude for mapping; and tickets_in_top_locations, which filtered the original dataset to include only tickets issued at these top locations. The script then read the input CSV, applied these functions, and wrote the resulting DataFrames to new CSV files. This ETL process was crucial for preparing the data for effective visualization, as the raw data contained too many locations to be directly useful.

The second part of the assignment involved building the two Streamlit dashboards. The first, map_dashboard.py, visualized the top locations on a map using streamlit_folium. Each location was represented by a circle, with the size indicating the total fines issued at that location. This dashboard provided a spatial overview of where the most parking ticket activity occurs in Syracuse. The second dashboard, location_dashboard.py, allowed users to select a specific location from a dropdown menu and then displayed detailed information about that location. This included total tickets issued, total fine amounts, and distributions of tickets by day of the week and hour of the day, using bar and line charts. This dashboard enabled a more in-depth analysis of parking ticket patterns at specific locations.

A key challenge in this assignment was determining how to effectively reduce the dimensionality of the location data. The solution was to focus on "top locations," defined by a threshold of $1,000 in total fines. This transformation, implemented in the etl.py script, made it possible to create meaningful visualizations. Another challenge was integrating folium maps into a Streamlit application. The streamlit_folium component facilitated this integration, allowing for interactive maps within the dashboards.

Through this assignment, I gained a deeper understanding of the importance of data transformation in the visualization process. I learned how to use Pandas to perform complex data manipulations, such as pivoting, merging, and filtering, to prepare data for specific visualization needs. I also gained experience with Streamlit, building interactive dashboards that allow users to explore data and gain insights. The assignment reinforced the idea that effective visualizations are not simply about plotting raw data but require careful consideration of how to transform and present the data to highlight relevant patterns and trends.