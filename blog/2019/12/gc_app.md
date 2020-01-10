---
layout: default
title: How to get lucky? A Data Scientist Guide to US Immigration
---
<h1 class="page-title">How to get lucky? A Data Scientist Guide to US Immigration.</h1>
<span class="post-date">28 Dec 2019 · 5 min read</span>
<img src="/public/pics/gc_app.jpg">
Since I moved from Poland to the US in 2013 to get my bachelor's degree, I knew that this is the place that I want to call home. Almost seven years later, I am still fighting with the US Immigration laws to secure a permanent residency for my family and me. Given that I am married and not even close to being a millionaire like many immigrants, the only path to a green card is through employment.

The standard path for international students is getting [OPT](https://www.uscis.gov/opt) (1-year work authorization), finding employer that wants to sponsor you, get [H1-B visa](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-dod-cooperative-research-and-development-project-workers-and-fashion-models) (3 years work authorization), and finally persuading them to sponsor an [EB-2](https://www.uscis.gov/working-united-states/permanent-workers/employment-based-immigration-second-preference-eb-2) (permanent residency) for you.

Given that, It's actually quite hard to find an employer willing to support your plan for next 3-4 years, you also have only ~55% chance of winning H1-B visa lottery, and that anything can change in that time (immigration laws, employer going bankrupt, your personal life changes - having a baby), you should know what are the chances of success and how to improve them.

### Key Findings:
1. In 2019 the number of applications went down by 20%.
2. ~70% of submission was for H1-B visa holders.
3. In the last five years, 71% of EB-2 applications were approved.
4. Most of the EB-2 sponsors are located in New York, NY.
5. The greatest portion of applications is for Software Engineers (15%).
6. In 2018 only 3.6% of F-1 Students in OPT  were lucky enough to have an employer sponsor a green card for them without getting a work visa first.
7. The largest green card sponsors are Cognizant, Microsoft, and Intel.

### What are trends in green card applications?
<img src="/public/pics/blog/get_lucky/trend_plot.png">
When looking only at the data in the last five years, it seems like there is seasonality in the applications submitted, as every other year count of applications goes down. If the seasonality continues, 2020 should be a good year, as 2019 was a negative year (-23%). The count of applications seems to oscillate around about 33k.

### What are visas leading to EB-2 application?
<img src="/public/pics/blog/get_lucky/visas_pie.png">
In the past five years, about 70% of submitted EB-2 applications (315700) were for H1-B visa holders. Making it the most common way to permanent residency in the US. Every year exactly [85,000](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-and-fashion-models/h-1b-fiscal-year-fy-2020-cap-season) H1-B visas are granted for six years period, so the count of H1-B visa holders in any year is lower bounded by `6 * 85,000 = 510,000`.

Consequently, this means that in the worst case (assuming maximum possible count of H1-B visas in any year) **only 12.3% of work visa holders in 2019 were sponsored for EB-2.**

Interestingly employers very rarely sponsor EB-2s for F-1 students (5.6%). One might think that desperate employers would skip the uncertain H1-B visa lottery and choose a more probable solution like EB-2 (there is no lottery), but unfortunately, that's not the case. **Furthermore, if we assume that only students on OPT are eligible to get sponsored (a conservative case), only 3.6%  were sponsored an EB-2 in 2018.** For perspective, it was more probable to get into [Harvard University](https://college.harvard.edu/admissions/admissions-statistics) this year.

### What are the most sponsored positions?
<img src="/public/pics/blog/get_lucky/pos_bar.png">
The most popular position among EB-2 applicants in the last five years was software engineering, with 6%. However, clearly, the first six positions in the list describe the same job, so practically **software dev/engineering positions account for ~15% of all applications**. Interestingly, there have been 3.77x more poultry processing worker applications and data scientist'. (I should have become a poultry processing worker)

### Who are the largest EB-2 Sponsors?

<figure>
  <table>
    <tr>
      <th>Employer</th>
      <th>Count</th>
      <th>Percent</th>
    </tr>
    <tr>
      <td>Cognizant Technology</td>
      <td>18345</td>
      <td>3.5%</td>
    </tr>
    <tr>
      <td>Microsoft</td>
      <td>9951</td>
      <td>1.88%</td>
    </tr>
    <tr>
      <td>Intel</td>
      <td>8637</td>
      <td>1.63%</td>
    </tr>
    <tr>
      <td>Google</td>
      <td>5830</td>
      <td>1.10%</td>
    </tr>
    <tr>
      <td>Amazon</td>
      <td>5060</td>
      <td>0.95%</td>
    </tr>
  </table>
  <figcaption class="image-caption">EB-2 Applications Since 2015 by Company</figcaption>
</figure>
Obviously the biggest sponosrs, as we hear in the [news](https://news.bloomberglaw.com/daily-labor-report/it-consulting-industry-hardest-hit-by-jump-in-h-1b-denials-1), are IT and Tech comapnies. **Cognizant takes the first place with 3.5% of applications in last 5 years**. Then it's Microsoft, Intel, Google and Amazon with 1.88%, 1.63%, 1.10%, 0.95% repspectively.

Consequently, when looking just at the year 2019, Cognizant also took first place, then it was Google, Amazon, Tata Consultancy, and Microsoft.

Facebook, Apple, Google, Virtusa Corp, and Adobe were among the companies that increased the count of EB-2 applications in 2019 the most.

When applying for a job, keep all of these companies in mind. However, there were about 24k EB-2 sponsors in 2019, so make sure to check out the [full list](/blog/2019/12/emp_list_2019.csv).

### Where are the EB-2 sponsors located?
<img src="/public/pics/blog/get_lucky/city_bar.png">
In the last five years, New York City, Los Angeles, and Houston have been the epicenters of EB-2 sponsors. Even though these cities are not the ones creating the most applications, these are the markets with the largest variety of employers. The cities with most applications would be locations of major EB-2 sponsors like Cognizant Technologies - College Station, TX, and Amazon - Seattle, WA. Although it's important to keep these companies in mind, these job markets are really overpowered by a few large players.

<figure>
  <table>
    <tr>
      <th>City</th>
      <th>Count</th>
    </tr>
    <tr>
      <td>New York</td>
      <td>1643</td>
    </tr>
    <tr>
      <td>San Francisco</td>
      <td>716</td>
    </tr>
    <tr>
      <td>Houston</td>
      <td>708</td>
    </tr>
    <tr>
      <td>Los Angeles</td>
      <td>598</td>
    </tr>
    <tr>
      <td>Miami</td>
      <td>525</td>
    </tr>
  </table>
  <figcaption class="image-caption">2019 EB-2 Applications by City</figcaption>
</figure>

New York continues to be the leading source of EB-2 employers in 2019. San Francisco catches up, but it's still at least 50% smaller job market than New York.

### How to improve your chances?
To have the highest chances for EB-2, if you should be a Software Engineer on H1-B, working at one of the top companies. However, there are a lot of other smaller companies or companies with smaller engineering teams, where you might have equal chances of getting a green card sponsored. Perhaps try finding companies like that in New York, NY, San Francisco, CA or Houston, TX.

### Data & Code
To get green card application data, I scraped one of the Green Card sponsors database websites (like [immihelp](https://immihelp.com)) using lxml in python. Then analyzed the data with Pandas, numpy, and matplotlib.

I will soon release the code and data.

### Future work:
1. Analyze H1-B sponsors
2. Try to dig deeper in the data
3. Improve visualizations
4. Implement fuzzy name matching for names of companies, cities, and positions
5. Analyze salary data
6. Analyze lawyer data to find the most successful lawyers
7. Normalize city names and states

#### If you have any questions or comments, feel free to send me a DM [@michallys](https://twitter.com/michallys).
