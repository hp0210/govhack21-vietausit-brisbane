
## Govhack 2021 - Team 1468 - VietAusIt -Brisbane
## Outliers Project

## Demo
* [High Fidelity Prototye](https://www.figma.com/file/QXa9VS0JQmNDGXRDEcsvhX/GovhackBrisbane?node-id=0%3A1)
* [Quick POC implementation for the user interface](https://govhack.vercel.app)

## Evident of Works / Quicklinks
* Brainstorming session
  - [Ideas for challenges](https://miro.com/app/board/o9J_l3KV1eE=/)
  - [Ideas for the POC](https://miro.com/app/board/o9J_l1NG-mw=/)
* Code Repository
  - [POC implementation UI](https://github.com/dohaicuong/govhack)
  - [General Data Processing](https://github.com/rodonguyen/vait-govhack-data)
  - [Statistical Areas Data aggregation](https://github.com/punkupoz/data-wrangle-govhack)
* Presentation Slide
* [Team work photo](https://drive.google.com/drive/folders/1arkY6Qp8fznHLuC_mPsPX0mTOmr2r4Se?usp=sharing)

### Project Description
We implement a reverse search that allows general public to build skill profiles and match their skill set to the potential industry and career paths.

At the moment, Australian Skills Classification’s search requires you to have the domain knowledge to drill down to the skill requirements for that industry or occupations.

Our solution focuses mainly on the user’s existing skill set to provide them wth jobs or career paths insight that might fit into their interest area, helping them to discover new opportunities within the region of their choice.

### Data Story
One of the major challenges is how to utilise the datasets from various sources including Australian National Skill Classification, Contract Disclosure and Forward Procurement from Queensland open data portal, then putting the data provided by the user to generate the recommended career paths.

Having the Australian National Skill Classification “skill clusters” and “occupation” datasets allows us to directly get the analytic data for skill clusters for each occupation. By reversing the mechanism and build the correlation between the skills, which is clustering into 10 main clusters (Numeracy, Digital engagement, Teamwork, Writing, Reading, Learning, Problem solving, Oral communication, Planning and organising, Initiative and innovation) and 3 tiers for each skill, we are able to generate the connected graph which allows user to explore the job titles associate with the user’s skills level.

Another objective is to predict the demanding workforce for each region in Queensland particularly and Australia potentially. Having deep insight and utilising the data from “Forward Procurement” and “Contract Disclosure” datasets, we calculated the market capital and ranking on which industry is providing high opportunities/employee shortage for each region. The result would be able to tell the user on which industries in a region have high opportunities for the user.

Further implementations include clustering the number of jobs currently available for each industry in real time, which requires data from job searching platforms such as SEEK or Indeed

### User Story
#### Story 1
As a user I want to create my profile by providing the system these following information (self assess)

1. Numeracy
2. Digital engagement
3. Teamwork
4. Writing
5. Reading
6. Learning
7. Problem solving
8. Oral communication
9. Planning and organising
10. Initiative and innovation

*Assessment Scale*
1-10 for each skills depends on what the user feel ez too accomplish.
The user should choose one of the tier first (basic, intermediate, high - we use the task description with the highest score in the dataset for hint)
Then depends on what the user selects we can ask questions to classify the user into three level within that tier

*Example scenario*

Rate your numeracy competency (baseline "Identify the numerical position of items on a shelf from left to right" as basic, select basic if you found it a bit too hard but still doable in case training is provided); otherwise choose "Not Applicable"

Basic, Intermediate, High, NA

#### Story 2
As a user, I can found a list of jobs title recommended for me that are best match my skill sets.
I should be able to see related tasks and technology tools associated with that job title
A breakdown of time spent for different types of tasks associated with the given job title

#### Story 3
As a user, I want to know which region potentially demand this skill.
I should be able to filter by location, age and gender competency
An option to know if I can get better in this skill, which industry is best for me and is demanding by which region.

### User flow
#### 1. User Profile
* When user first goes to the website, the system will prompt the user with Skill Competency self-assessed form.
* When user rates a skill on a scale from 1-10 based on their confidence with that skill , the system will show a drop down of 3 tasks associate with the level of confidence in that skill. User will need to choose a task that they are most confident in for that skill.
* When the user completes the form and clicks “Submit”, the system will generate a competency profile for the user. Using the competency profile, the system will generate the “Connected graph” and “Recommend job titles” for them. The "Connected graph"

#### 2. Connected graph
* When the user completes the self-assessed form, the system will generate a competency profile for the user. Using the competency profile, the system will generate the “Connected graph” and “Recommend job titles” for them.
* The “Connected graph” will have several hubs accordingly to the skills. When the user clicks on a skill node in the “Connected graph”, the system will highlight the job titles that require the skill.
* When the user clicks on a job title in the “Connected graph”, the system will show that job description/responsibilities and a pie chart of the usage of skills/tasks by time and a button “See which region is demanding these skills”.

#### 3. Recommend job titles
* When the user completes the self-assessed form, the system will generate a competency profile for the user. Using the competency profile, the system will generate the “Connected graph” and “Recommend job titles” for them.
* When the user clicks on a “Job title” in “Recommend job titles”, the system will show them job description/responsibilities and a pie chart of the usage of skills/tasks by time and a button “See which region is demanding these skills”.
* When the user clicks on the button, the system will show them a map that shows which region requires workers in the industry that the job title associate with

#### 4. Visualisation
* When the user navigates to “Visualisation” page, the system should show a map with a pinpoint on each region. The pinpoint will show the top 3-5 industries that are demanding more workers (potentially) for that region
* When the user select a location from the “Location” tab, the map will focus on the region and shows details of top 3-5 industries that are demanding more workers (potentially) along with competencies.
* When the user clicks on “Skill” tab and modify the skill competencies profile, the system will re-generate the recommended job titles and shows the region that demanding workers in industries that those job titles associate with.


