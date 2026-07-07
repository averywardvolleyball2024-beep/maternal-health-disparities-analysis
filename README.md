# maternal-health-disparities-analysis
This project analyzes maternal health outcomes using CDC WONDER natality data. The main goal of the code is to examine how prenatal care access and preterm birth rates differ across racial and ethnic groups.

The code begins by importing the pandas library, which is used to load and organize the dataset. After the CSV file is read into Python, the dataset is displayed, and the column names are printed so the correct variables can be identified. This helps confirm that the dataset includes the needed columns, such as mother’s race, gestational age, prenatal care timing, number of prenatal visits, and number of births.

Next, the code classifies births based on gestational age. It uses the “Average OE Gestational Age (weeks)” column and applies a function that places each row into a birth category. Births under 28 weeks are classified as “Extremely Preterm,” births under 32 weeks are classified as “Very Preterm,” births under 37 weeks are classified as “Preterm,” and births at 37 weeks or higher are classified as “Full Term.” This step is important because preterm birth is one of the main outcomes being studied.

The code then prepares the prenatal care data. Since the number of prenatal visits is stored as text, the code extracts the numeric value from that column and converts it into a number. It defines “adequate prenatal care” as care that began during the first trimester and included 12 to 14 prenatal visits. The code also creates a “valid” category to make sure only rows with complete prenatal care information are included in the percentage calculation.

After that, the code groups the data by mother’s race. For each racial group, it calculates the percentage of valid records that meet the definition of adequate prenatal care. This allows the project to compare prenatal care access across racial and ethnic groups.

The code also calculates preterm birth rates by race. First, it converts the “Births” column into a numeric format so the values can be added correctly. Then it identifies which gestational age categories count as preterm. The code groups the dataset by mother’s race, calculates the total number of births for each group, calculates the number of preterm births for each group, and divides preterm births by total births to find the preterm birth percentage.

The prenatal care results and preterm birth results are then combined into one summary table. This table shows each racial group’s percentage of adequate prenatal care and percentage of preterm births. The data is sorted by preterm birth rate, so the groups with the highest rates appear first.

Finally, the code creates several visualizations using matplotlib. One bar graph shows the preterm birth rate by race and ethnicity. Another graph shows the percentage of adequate prenatal care by race and ethnicity. A grouped bar graph compares prenatal care adequacy and preterm birth rates side by side. The final stacked bar graph shows the distribution of birth categories, such as extremely preterm, very preterm, preterm, and full term, across racial and ethnic groups.

Overall, this code uses data cleaning, grouping, percentage calculations, and visualizations to explore racial and ethnic differences in prenatal care access and preterm birth outcomes. The project connects data science to maternal-fetal medicine by examining patterns that may help identify disparities in maternal and infant health outcomes.
