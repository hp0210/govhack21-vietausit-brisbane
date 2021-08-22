
## Govhack 2021 - Team 1468 - VietAusIt -Brisbane
## Outliers Project
### Evident of Works / Quicklinks
* [High Fidelity Prototye](https://www.figma.com/file/QXa9VS0JQmNDGXRDEcsvhX/GovhackBrisbane?node-id=0%3A1)
* [Quick POC implementation for the user interface](https://govhack.vercel.app)
* Brainstorming session
  - [Ideals for challenges](https://miro.com/app/board/o9J_l3KV1eE=/)
  - [Ideals for the POC](https://miro.com/app/board/o9J_l1NG-mw=/)
* Code Repository [To be updated]
  - [POC implementation UI](https://github.com/dohaicuong/govhack)
  - [Data processing](https://github.com/rodonguyen/vait-govhack-data)
* Presentation Slide
* Team work photo

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
