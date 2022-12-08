# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring climate data of Singapore

### Overview of Project 1

Our first module in DSI covers:
- Basic statistics and probability
- Many Python programming concepts
- Programmatically interacting with files and directories
- Visualizations
- EDA
- Working with Jupyter notebooks for development and reporting

You might wonder if you're ready to start doing data science. While you still have **tons** to learn, there are many aspects of the data science process that you're ready to tackle. Project 1 aims to allow you to practice and demonstrate these skills.

For our first project, we're going to analyze climate trends in Singapore. Climate refers to the general weather conditions prevailing over an area for a long period. There are several aspect to studying climate that includes rainfall, temperature, relative humidity, wet build temperature, sun shine duration etc.


### Problem Statement

1. Audience - who, what, how
2. Data?
3. Value to Audience - insights, decisions

#### Background
Water is one of the most essential resources to sustain lives. Due to its challenging environment and geographical limitations, water supply and sanitation are intricately linked to Singapore's planning and development efforts. One of the efforts is to build reservoirs to contain rainfall. As water demand is expected to double from 380 to 760 million gallons per day between 2010-2060, the government is planning on constructive more desalination plants.

In this project, I am part of PUB's data science team. 

This study and analysis aims to help my agency to understand the rainfall trends, and make some recommendations in the building of artificial reservoirs as water catchment areas.

---

### Datasets

#### Provided Data

There are 2 datasets included in the [`data`](./data/) folder for this project. These correponds to rainfall information. 

* [`rainfall-monthly-number-of-rain-days.csv`](./data/rainfall-monthly-number-of-rain-days.csv): Monthly number of rain days from 1982 to 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.
* [`rainfall-monthly-total.csv`](./data/rainfall-monthly-total.csv): Monthly total rain recorded in mm(millimeters) from 1982 to 2022

#### Other Data

##### Time series 
* [Monthly Maximum Daily Rainfall](https://data.gov.sg/dataset/rainfall-monthly-maximum-daily-total)
* Population growth trend in Singapore
* Immigration flow rate to Singapore

##### Categorical
* Size of existing artificial reservoirs, and the capacity for water catchment 

---

### Deliverables

All of your projects will comprise of a written technical report and a presentation. As we continue in the course, your technical report will grow in complexity, but for this initial project it will comprise:
- A Jupyter notebook that describes your data with visualizations & statistical analysis.
- A README markdown file the provides an introduction to and overview of your project.
- Your presentation slideshow rendered as a .pdf file.
**NOTE**: Your entire Github repository will be evaluated as your technical report. Make sure that your files and directories are named appropriately, that all necessary files are included, and that no unnecessary or incomplete files are included.

For your first presentation, you'll be presenting to a **non-technical** audience. You should prepare a slideshow with appropriately scaled visuals to complement a compelling narrative. **Presentation duration will be 10 minutes.**

---

### Technical Report Starter Code

Future projects will require you to decide on the entire structure of your technical report. Here, we provide you with [starter code](./code/starter-code.ipynb) in a Jupyter notebook that will help to guide your data exploration and analysis. **If you choose to edit the core structure of this notebook, make sure you don't exclude any of the requested operations**.

---

### Suggested Resources

Here's a link on [how to give a good lightning talk](https://www.semrush.com/blog/16-ways-to-prepare-for-a-lightning-talk/), which provides some good recommendations for short presentations.

[Here's a great summary](https://towardsdatascience.com/storytelling-with-data-a-data-visualization-guide-for-business-professionals-97d50512b407) of the main points of the book _Storytelling with Data_, which I can't recommend enough. [Here's a blog post](http://www.storytellingwithdata.com/blog/2017/8/9/my-guiding-principles) by the author about his guiding principles for visualizations.

---

### Submission

**Materials must be submitted through your GitHub account repo shared with the Teaching Team by scheduled due date.**

Your technical report will be hosted on Github Enterprise. Make sure it includes:

- A README.md (that isn't this file)
- Jupyter notebook(s) with your analysis (renamed to describe your project)
- Data files
- Presentation slides
- Any other necessary files (images, etc.)

---

### Presentation Structure

- **Presentation Time: 15 minutes**
- Use Google Slides or some other visual aid (Keynote, Powerpoint, etc).
- Consider the audience. Assume you are presenting to a non-technical audience (executives with the College Board, school administrators, admissions counselors, State officials, etc.).
- Start with the **data science problem**.
- Use visuals that are appropriately scaled and interpretable.
- Talk about your procedure/methodology (high level, **CODE IS ALWAYS INAPPROPRIATE FOR A NON-TECHNICAL AUDIENCE**).
- Talk about your primary findings.
- Make sure you provide **clear recommendations** that follow logically from your analyses and narrative and answer your data science problem.

Be sure to rehearse and time your presentation before class.

---

### Rubric
Teaching team will evaluate your project using the following criteria.  You should make sure that you consider and/or follow most if not all of the considerations/recommendations outlined below **while** working through your project.

**Note:** Presentation will be done as a group while codes will be prepared and submitted by each student.

**Scores will be out of 21 points based on the 7 items in the rubric.** <br>
*3 points per section*<br>

| Score | Interpretation |
| --- | --- |
| **0** | *Project fails to meet the minimum requirements for this item.* |
| **1** | *Project meets the minimum requirements for this item, but falls significantly short of portfolio-ready expectations.* |
| **2** | *Project exceeds the minimum requirements for this item, but falls short of portfolio-ready expectations.* |
| **3** | *Project meets or exceeds portfolio-ready expectations; demonstrates a thorough understanding of every outlined consideration.* |

**Project Organization**
- Are modules imported correctly (using appropriate aliases)?
- Are data imported/saved using relative paths?
- Does the README provide a good executive summary of the project?
- Is markdown formatting used appropriately to structure notebooks?
- Are there an appropriate amount of comments to support the code?
- Are files & directories organized correctly?
- Are there unnecessary files included?
- Do files and directories have well-structured, appropriate, consistent names?

**Clarity of Message**
- Is the problem statement clearly presented?
- Does a strong narrative run through the project?
- Does the student provide appropriate context to connect individual steps back to the overall project?
- Is it clear how the final recommendations were reached?
- Are the conclusions/recommendations clearly stated?

**Python Syntax and Control Flow**
- Is care taken to write human readable code?
- Is the code syntactically correct (no runtime errors)?
- Does the code generate desired results (logically correct)?
- Does the code follows general best practices and style guidelines?
- Are Pandas functions used appropriately?
- Does the student demonstrate mastery masking in Pandas?
- Does the student demonstrate mastery sorting in Pandas?

**Data Cleaning and EDA**
- Does the student fix data entry issues?
- Are data appropriately labeled?
- Are data appropriately typed?
- Are datasets combined correctly?
- Are appropriate summary statistics provided?
- Are steps taken during data cleaning and EDA framed appropriately?

**Visualizations**
- Are the requested visualizations provided?
- Do plots accurately demonstrate valid relationships?
- Are plots labeled properly?
- Plots interpreted appropriately?
- Are plots formatted and scaled appropriately for inclusion in a notebook-based technical report?

**Research and Conceptual Understanding**
- Were useful insights gathered from outside sources?
- Are sources clearly identified?
- Does the student provide appropriate interpretation with regards to descriptive and inferential statistics?

**Presentation**
- Is the problem statement clearly presented?
- Does a strong narrative run through the presentation building toward a final conclusion?
- Are the conclusions/recommendations clearly stated?
- Is the level of technicality appropriate for the intended audience?
- Is the student substantially over or under time?
- Does the student appropriately pace their presentation?
- Does the student deliver their message with clarity and volume?
- Are appropriate visualizations generated for the intended audience?
- Are visualizations necessary and useful for supporting conclusions/explaining findings?

In order to pass the project, students must earn a minimum score of 1 for each category.
- Earning below a 1 in one or more of the above categories would result in a failing project.
- While a minimum of 1 in each category is the required threshold for graduation, students should aim to earn at least an average of 1.5 across each category. An average score below 1.5, while it may be passing, means students may want to solicit specific feedback in order to significantly improve the project before showcasing it as part of a portfolio or the job search.

### REMEMBER:

This is a learning environment and you are encouraged to try new things, even if they don't work out as well as you planned! While this rubric outlines what we look for in a _good_ project, it is up to you to go above and beyond to create a _great_ project. **Learn from your failures and you'll be prepared to succeed in the workforce**.
# ga_project1_dsif9
