# Survey-Analysis

Objective
To understand how respondents' demographics influences their behavior towards companies' involvement in social issues.

Questions to answer
1. How do gender and age affect purchase likelihood from socially aligned companies?
2. How does ethnicity influence seeking supportive companies?
3. How are social issues distributed across age groups?
4. How does education level relate to social issue resonance?
5. How does household income impact opinions on companies' responsibility to speak out?

Steps followed for the analysis:




Data Exploration

Columns:
The dataset has 40 columns. Each column represents a specific aspect of the respondents' demographics or their opinions on companies' involvement in social issues. There are 216 entries for each column.

| Column Name                           | Description                                                                                           | Entries |
|---------------------------------------|-------------------------------------------------------------------------------------------------------|---------|
| Respondent identifier                 | Unique identifier for each respondent                                                                 | 216     |
| Start time                            | Time when the survey started                                                                          | 216     |
| End time                              | Time when the survey ended                                                                            | 216     |
| State                                 | State of the respondent                                                                               | 216     |
| Region                                | Region of the respondent                                                                              | 216     |
| City                                  | City of the respondent                                                                                | 216     |
| GPS coordinates                       | GPS coordinates of the respondent                                                                     | 216     |
| Login parameters                      | Parameters used for login                                                                             | 216     |
| S1 - Total                            | Total respondents                                                                                     | 216     |
| S2 - Between 35 and 50 (Age)          | Respondents aged between 35 and 50                                                                    | 216     |
| S3 - Female (Gender)                  | Female respondents                                                                                   | 216     |
| S4 - Male (Gender)                    | Male respondents                                                                                     | 216     |
| S5 - Over 50 (Age)                    | Respondents aged over 50                                                                              | 216     |
| S6 - Under 35 (Age)                   | Respondents aged under 35                                                                             | 216     |
| CHQ1 - Feelings strength towards SI   | Strength of feelings towards social issues                                                            | 216     |
| CHQ2 - Day of Week Trap               | Day of the week trap question                                                                         | 216     |
| CHQ3 - Types of SI                    | Types of social issues respondents are passionate about                                               | 216     |
| OEQ1 - Other SI                       | Other social issues respondents are passionate about                                                  | 216     |
| CHQ4 - Company ability                | Respondents' belief in companies' ability to make positive social changes                             | 216     |
| OEQ2 - How to make positive change    | Ways companies can make positive social changes                                                       | 216     |
| OEQ3 - Why no positive change         | Reasons for believing companies cannot make positive social changes                                   | 216     |
| CHQ5 - Activism concerns              | Concerns about companies' activism                                                                    | 216     |
| OEQ4 - Concern type                   | Types of concerns about companies' activism                                                           | 216     |
| CHQ6 - Company responsibility         | Belief in companies' responsibility to speak out on social issues                                     | 216     |
| OEQ5 - Why responsible                | Reasons for believing companies are responsible for speaking out on social issues                     | 216     |
| OEQ6 - Specific responsibility        | Specific social issues companies are responsible for                                                  | 216     |
| OEQ7 - Why not responsible            | Reasons for believing companies are not responsible for speaking out on social issues                 | 216     |
| CHQ7 - Specific non-responsibility 1  | Specific social issues companies should not speak out on (part 1)                                     | 216     |
| OEQ8 - Specific non-responsibility 2  | Specific social issues companies should not speak out on (part 2)                                     | 216     |
| CHQ8 - Purchase likelihood agree      | Likelihood of purchasing from companies that align with respondents' social issues                    | 216     |
| CHQ9 - Purchase likelihood disagree   | Likelihood of purchasing from companies that oppose respondents' social issues                        | 216     |
| CHQ10 - Purchase likelihood undisclosed | Likelihood of purchasing from companies that do not disclose their stance on social issues            | 216     |
| CHQ11 - Company search                | Tendency to seek out companies that support social issues                                             | 216     |
| CHQ12 - Age                           | Age of the respondent                                                                                 | 216     |
| CHQ13 - Gender                        | Gender of the respondent                                                                              | 216     |
| CHQ14 - Ethnicity                     | Ethnicity of the respondent                                                                           | 216     |
| CHQ15 - Education level               | Highest education level attained by the respondent                                                    | 216     |
| CHQ16 - Income                        | Total annual household income of the respondent                                                       | 216     |
| CHQ17 - Political views               | Respondents' rating of their political views                                                          | 216     |
| ES1 - Complete                        | Completion status of the survey                                                                       | 216     |

Checking for missing values:

Filters were applied to the entire dataset to check for missing values in specific columns. Missing values were found in the title header, with some columns having 3 missing values while others had 2.

Typing errors:

The city column contains typos, with two values stored as '?'.

Duplicates:
The dataset has no duplicates.

Data cleaning
We noticed that the title header had merged cells, which would prevent us from creating a pivot table for data analysis. 
To solve this, the cells were unmerged, and the column names were edited to a single row and later simplified for better readability. 
After unmerging the cells and simplifying the column names for better readability, here are the updated column names in a clear table format:

After unmerging the cells and simplifying the column names for better readability, here are the updated column names in a clear table format:

| Column Name                                           | 
|-------------------------------------------------------|
| Respondent identifier                                 | 
| Start time                                            | 
| End time                                              | 
| State                                                 | 
| Region                                                | 
| City                                                  | 
| GPS coordinates                                       | 
| Login parameters                                      | 
| S1 - Total                                            | 
| Between 35 and 50 years                               | 
| Female                                                | 
| Male                                                  | 
| Over 50 years                                         | 
| Under 35 years                                        | 
| Which of the following statements resonates with you most? | 
| Climate change & other environmental issues          | 
| Civil rights & racial discrimination                  | 
| Gender inequality                                     | 
| Healthcare inaccessibility                            | 
| Gun violence                                          | 
| Poverty & food insecurity                             | 
| Unemployment                                          | 
| Other social issues                                   | 
| What other social issue(s) are you passionate about?  | 
| Companies ability to make positive change            | 
| How companies can make positive change               | 
| Reasons for no positive social change                | 
| Activism concerns towards a company                  | 
| Concern type                                          | 
| Companies responsibility to speak out on social issues | 
| Why companies should speak out on social changes     | 
| Specific issues to be addressed by companies         | 
| Why companies should not speak on social issues      | 
| Specific social issues companies should not speak out on, Y/N | 
| Specific issues companies should not speak out on   | 
| Purchase likelihood agree                             | 
| Purchase likelihood disagree                          | 
| Purchase likelihood undisclosed                       | 
| Actively Seek Supportive Companies When Purchasing   | 
| Age                                                   | 
| Gender                                                | 
| Black or African American                             | 
| White                                                 | 
| Asian                                                 | 
| Hispanic                                              | 
| Middle Eastern                                        | 
| Native American or Alaska Native                      | 
| Native Hawaiian or Pacific Islander                   | 
| Other Ethnicity                                       | 
| Undisclosed Ethnicity                                 | 
| Education level                                       | 
| Annual Household Income                               | 
| Political views                                       | 












