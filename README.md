# README

### PROBLEM STATEMENT

One of the most common reasons students cite in choosing to go to college is the expansion of employment opportunities. The College Scorecard project under the Department of Education is designed to increase transparency, putting the power in the hands of students and families to compare how well individual postsecondary institutions are preparing their students to be successful. 

Among over 7000 institutions in the United States, how one student could start? Application process is very time consuming and costly. Helping students create a balanced list of options that reflect both their ambitions and aspirations as well as the realities of the college admissions landscape today. There are many wonderful options across the spectrum of selectivity. College is a match to be made and not a prize to be won. Guiding Students to approach their search from a position of strength, optimism, and excitement. 

Starting from the common test score SAT, this college recommender first guide student to 3 categories of colleges to explore: The REACH, TARGET, and SAFETY schools. Secondly, college recommender can provide list of colleges with similar characristics and experience based on a student's choice of college. This will broaden student's search to more colleges under the same focus. Further, college recommender will not only provide a good starting point of understanding colleges but also guide student in their direction of college application.


### OVERVIEW

About a year ago, the united state government put much emphasis on higher education in the country. In March 2019, whitehouse published Executive Order on Improving Free Inquiry, Transparency, and Accountability at Colleges and Universities. The purpose of this order is to enhance the quality of postsecondary education by making it more affordable, more transparent, and more accountable. Institutions of higher education (institutions) should be accountable both for student outcomes and for student life on campus. Per the Executive Order, the Department of Education continues its efforts to update the College Scorecard so that it includes clear information on the cost of college, expected earnings after graduation, and student loan repayment rates.

The College Scorecard project under the Department of Education is designed to increase transparency, putting the power in the hands of students and families to compare how well individual postsecondary institutions are preparing their students to be successful. This project provides data to help students and families compare college costs and outcomes as they weigh the tradeoffs of different colleges, accounting for their own needs and educational goals.

These data are provided through federal reporting from institutions, data on federal financial aid, and tax information. These data provide insights into the performance of institutions that receive federal financial aid dollars, and the outcomes of the students of those institutions. 

Many elements are available only for students who receive federal grants and loans. These data are reported at the individual level to the National Student Loan Data System (NSLDS), which is used to distribute federal aid, and published at the aggregate institutional level. All Treasury elements are protected for privacy purposes; those data that do not meet reporting standards are shown as PrivacySuppressed. And while the data come with some noteworthy limitations, their availability is an important step forward.

### DATA

I used the College Scorecard data released by the Department of Education for my analysis. The full data set has information on more than 7,000 institutions in the United States, including community colleges, undergraduate schools, and post-graduate institutions like law and medical schools. It also contains about 2,000 variables. This project includes the following from Academic Year 2017-2018 Data:

'UNITID', unique identification number assigned to postsecondary institutions 

'INSTNM', institution’s name

'CITY', 

'STABBR', state name

'NUMBRANCH', the number of branch campuses at that institution

'MAIN', Main Campus/Branch 

'HIGHDEG', # identifies the highest award level conferred at the institution

'PREDDEG', type of award that the institution primarily confers9

'CONTROL', institution’s governance structure is public, private nonprofit, or private for-profit.

'DISTANCEONLY', 

'TUITIONFEE_IN',  # Average Cost of Attendance, Tuition and Fees 
 
'TUITIONFEE_OUT', 'TUITIONFEE_PROG', 'TUITFTE',
 
'AVGFACSAL', #The average faculty salary 
 
'RELAFFIL', #  identified by their religious affiliation

'ADM_RATE_ALL', 

'SATVR25', 'SATVR75', 'SATMT25', 'SATMT75','SATVRMID', 'SATMTMID',
'SAT_AVG_ALL', 
'ACTCM25', 'ACTCM75', 
'ACTCMMID', 'ACTENMID', 'ACTMTMID', 

the percentage of degrees awarded in each two-digit CIP code category of academic areas. 

'PCIP01', 'PCIP03','PCIP04','PCIP05','PCIP09','PCIP10','PCIP11',
'PCIP12', 'PCIP13','PCIP14','PCIP15','PCIP16','PCIP19',  'PCIP22','PCIP23','PCIP24','PCIP25','PCIP26','PCIP27','PCIP29',
'PCIP30','PCIP31','PCIP38','PCIP39','PCIP40','PCIP41','PCIP42', 'PCIP43','PCIP44','PCIP45','PCIP46','PCIP47','PCIP48','PCIP49',
'PCIP50','PCIP51','PCIP52','PCIP54',

'UGDS', # number of degree/certificate-seeking undergraduates enrolled 

'UGDS_WHITE','UGDS_BLACK','UGDS_HISP','UGDS_ASIAN', #Undergraduate Student Body by Race and Gender

'UGDS_AIAN','UGDS_NHPI','UGDS_2MOR','UGDS_NRA','UGDS_UNKN',  #Number of Undergraduate Students 

'UG25ABV', # Undergraduate Student Body by Age who are ages 25 and over

'PPTUG_EF', # Undergraduate Students by Part-Time/Full-Time Status 

'COSTT4_A','COSTT4_P', # Average Cost of Attendance, Tuition and Fees 

'INEXPFTE', #Instructional expenditures per FTE student      

'C150_4', #Completion Rates for 4 year college

'RET_FT4','RET_FTL4', #Retention Rate - return to the institution after the first year

'PCTFLOAN', # Percent of Undergraduates Receiving Federal Loans 

'OPENADMP', # OPENADMP

'DEBT_MDN', #  the sum of all undergraduate federal loans over students’ college education at the institution

'CDR3', #  repayment Cohort Default Rate, The three-year cohort default rate 

Median Earnings:  Median earnings for all federally aided students. Data is available for each year starting six years after a student enrolls in college and up to 10 years after the student enrolls. for this analysis, I used 10-year earnings data in Academic Year 2014-2015 Data because that is the latest data file contains earing data.

It is important to mention that many of these variables, including median earnings and graduate debt, only apply to student borrowers of federal loans and may not be representative of students who have private loans or no student debt.

### APPROACH

First, User input a SAT score, this Recommender will output colleges to user in 3 categories:

REACH: Test Score Meets 25th percentile of applicants admitted

TARGET: Test Score About median but less than 75 percentile of applicants admitted 

SAFETY COLLEGES: Test Score Higher than 75 percentile of applicants admitted

This process is done by regression algorithm.

Secondly, Recommender system can provide lots of statistic as well as visualization based on user query. Student is able to find state variation of costs and outcomes, schools cost less and providing higher earning potential, student completion rate, average student debt, and many more. 

Further, user can input a name of college, Recommender system will generate a list of similar colleges to broaden seach of colleges.

This process is done by using pairwised distance algorithm based on cosine similarity. Scaling of variables is important for this step.

### CONCLUTION

While no single data point can capture a school's "value," the College Scorecard Data is a very useful resource for prospective college students to understand and compare different schools across a variety of important metrics. Based on the College Scorecard Data, I am able to make a College Recommender system to help and guide student's college searching process. This is a phase one of the college recommender, the next step will be Choice of a state. State-Only Recommendation, Choice of ACT as Test Score, Choice of Specific field of interest/major, and Free Website for people to explore.



