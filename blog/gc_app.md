---
layout: default
title: How to get lucky? A Data Scientist Guide to US Immigration
---
<h1 class="page-title">How to get lucky? A Data Scientist Guide to US Immigration.</h1>
<span class="post-date">Written: 08 Jan 2018</span>
<img src="/public/pics/gc_app.jpg">
<!-- ### Prologue -->
<!-- Even though most of the students come to the US on non-immigrant visa F-1, some of them want to stay here for good. There are various ways to attain that goal, but if you are not a distinguished expert in your filed or don't want to marry an American, your best bet is employment-based visas or green cards. -->
<!--  -->
<!-- That is a case for me. I am from Poland. I recently got an MS in CS and looking for a full-time position as a data scientist. The most common way is to get a job with an employer that is open to sponsoring you an H1-B visa - aka the work visa. Trust me; this step is not that easy. Even when you find a company willing to do so, USCIS imposes a cap of 85,000 H1-B visas, and consequently, the applications are subject to a lottery. According to USCIS, there have been a total of 190,098 H1-B petitions received for FY 2019 quota. **If you are unlucky like me, there is a 55% chance that USCIS will deny your application.** Even if you find an employer and your application is approved, the visas are given out only for three years period, so you also have to make sure that your employer will be happy to sponsor an application for you, but this time for a green card EB-2. -->
<!--  -->
<!-- > The EB-2 visa allows those in certain specialised professions – such as doctors, business managers, and educators – who have a master's degree or higher to gain lawful permanent residence in the US. **- workpermit.com** -->
<!--  -->
<!--Add more about EB-2-->
<!--  -->
<!-- I am not an immigration lawyer, but it seems like getting a green card straight away is a much better deal than EB-2. Both for the employer and the employee. -->
<!--  -->
<!-- This leads to the goal for this blog: **How to find EB-2 Employers?** -->
<!--  -->
<!-- ![enter image description here](https://d13ezvd6yrslxm.cloudfront.net/wp/wp-content/images/Fantastic-Beasts-and-Where-To-Find-Them-logo.jpg) -->
<!--  -->
<!-- ### The Guide -->
<!--  -->

<!-- > The total number of international students, **1,095,299**, is a 0.05 percent increase over last year, according to the _2019 Open Doors Report on International Educational Exchange_. International students make up 5.5 percent of the total U.S. higher education population. According to data from the U.S. Department of Commerce, international students contributed $44.7 billion to the U.S. economy in 2018, an increase of 5.5 percent from the previous year. **- iie.com** -->
<!--  -->
When I first moved to New York in 2013 to get my bachelors degree, I knew that this is the place that I want to call home. Almost 7 years later, I am still fighting with the US Immigration laws to secure pernament residency for me and my familly. Given that I am married, and not even close to being a millioniare like many immigrants the only path to green card is through employement.

The common path for foreign students is get [OPT](https://www.uscis.gov/opt) (1-year work authorization), find employer that wants to sponsor you, get [H1-B visa](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-dod-cooperative-research-and-development-project-workers-and-fashion-models) (3 years work authorization), and finally persuade them to sponsor an [EB-2](https://www.uscis.gov/working-united-states/permanent-workers/employment-based-immigration-second-preference-eb-2) (pernament residency) for you.

Given that, It's actually quite hard to find an employer willing to support your plan for next 3-4 years, you also have only XX% chance of winning H1-B visa lottery, and that anything can change in that time (immigration laws, employer going bankrupt, your personal life changes - having a baby), you should know what are the chances of success and how to improve them.

### Key Findings:
1. Number of EB-2 Applications are increasing each year.
2. ~70% of submitted EB-2 applications were for H1-B visa holders.
3. Most of the EB-2 sponsors are located in New York, NY.
4. The lagest portion of applicatns are Software Engineers (XX%).
5. In 2018 only 3.6% of F-1 Students in OPT  were lucky enough to have an employer sponsor a green card for them, whithout getting a work visa first.
6. The largest green card sponors are
7. Average salary of EB-2 applicant was $XXX in 2019.
8. The most succesful law firm for EB-2 applications in 2019 was.
<!-- #### . What are trends in green card applications? -->

### How EB-2 applications count changes?

### What are visas leading to EB-2 application?
<img src="/public/pics/blog/get_lucky/visas_pie.png">
In past 5 years about 70% of submitted EB-2 applications (315700) were for H1-B visa holders. Making it the most common way to pernament residency in US. Every year exactly [85,000](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-and-fashion-models/h-1b-fiscal-year-fy-2020-cap-season) H1-B visas are granted for 6 years period, so the count of H1-B visa holders in any year is lower bounded by `6 * 85,000 = 510,000`.

Consequently, this means that in worst case (assuming maxium possible count of H1-B visas in any year **only XX.X% of work visa holders in 2019 were sponsored for EB-2.**

Intrestignly employers very rarely sponosor EB-2s for F-1 students (5.6%). One might think that desperate employers would skip the uncertain H1-B visa lottery and choose more propable solution like EB-2 (there is no lottery), but unfortunely that's not the case. **Furthermore, if we assume that only students on OPT are eligibale to get sponosored (a conservative case), only 3.6%  were sponsored an EB-2 in 2018.** For perspective, it was more probable to get into [Harvard University](https://college.harvard.edu/admissions/admissions-statistics) this year.

### What are the most sponosored positions?

The most popular postions amongs EB-2 applicants in last 5 years was software development with XX.X%. Clearly, it's the most desired position by domestic employers.

### Who are the largest EB-2 Sponsors?

Obviously the biggest sponosrs, as heard in the [news](), are IT and Tech comapnies. Coginzant takes the first place with XX.X%. Then it's Microsoft, Facebook and Google with X.X%, X.X%, X.X% repspectively.

### Where are the EB-2 sponosrs located?

Most of the green card sponsors are located in New York.

### . What are the most successful lawyers for EB-2s?

### How to improve your chances?
You have the highest chances for EB-2, if you are currently a Software Engineer on H1-B, working at one of the top companies. However there are a lot of other smaller companies or companies with smaller engineering teams, where you might have equal chances of getting a green card sponsored. Perhaps try finding comapnies like that in New York, NY, San Francisco, CA or Seattle,WA.

### Data & Code
To get green card application data is scraped one of the Green Card sponors database websites (like XXX) using XXX in python (notebook). Then analyzed the data

### Future work:
1. Analyze H1-B sponsors

