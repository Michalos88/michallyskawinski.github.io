---
layout: default
title: How to get lucky? A Data Scientist Guide to US Immigration
---
<h1 class="page-title">How to get lucky? A Data Scientist Guide to US Immigration.</h1>
<span class="post-date">Written: 08 Jan 2018</span>
<img src="/public/pics/gc_app.jpg">
Since I moved from Poland to US in 2013 to get my bachelors degree, I knew that this is the place that I want to call home. Almost 7 years later, I am still fighting with the US Immigration laws to secure pernament residency for me and my familly. Given that I am married, and not even close to being a millioniare like many immigrants the only path to green card is through employement.

The common path for foreign students is get [OPT](https://www.uscis.gov/opt) (1-year work authorization), find employer that wants to sponsor you, get [H1-B visa](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-dod-cooperative-research-and-development-project-workers-and-fashion-models) (3 years work authorization), and finally persuade them to sponsor an [EB-2](https://www.uscis.gov/working-united-states/permanent-workers/employment-based-immigration-second-preference-eb-2) (pernament residency) for you.

Given that, It's actually quite hard to find an employer willing to support your plan for next 3-4 years, you also have only ~55% chance of winning H1-B visa lottery, and that anything can change in that time (immigration laws, employer going bankrupt, your personal life changes - having a baby), you should know what are the chances of success and how to improve them.

### Key Findings:
1. In 2019 number of applications went down by 20%.
2. ~70% of submission  were for H1-B visa holders.
2. In last 5 years 71% of EB-2 applications were approved.
3. Most of the EB-2 sponsors are located in New York, NY.
4. The lagest portion of applicatns are Software Engineers (15%).
5. In 2018 only 3.6% of F-1 Students in OPT  were lucky enough to have an employer sponsor a green card for them, whithout getting a work visa first.
6. The largest green card sponors are
7. The most succesful law firm for EB-2 applications in 2019 was.

### What are trends in green card applications?
<img src="/public/pics/blog/get_lucky/trend_plot.png">
Looking only at at the data in last 5 years, it seems like there is seasonality in the applications submitted, as every other year count of applications goes down. If the seasonality continues 2020 should be good year, as 2019 was a negative year (-23%). The count of applications seems to oscilate arround about 33k.

### What are visas leading to EB-2 application?
<img src="/public/pics/blog/get_lucky/visas_pie.png">
In past 5 years about 70% of submitted EB-2 applications (315700) were for H1-B visa holders. Making it the most common way to pernament residency in US. Every year exactly [85,000](https://www.uscis.gov/working-united-states/temporary-workers/h-1b-specialty-occupations-and-fashion-models/h-1b-fiscal-year-fy-2020-cap-season) H1-B visas are granted for 6 years period, so the count of H1-B visa holders in any year is lower bounded by `6 * 85,000 = 510,000`.

Consequently, this means that in worst case (assuming maxium possible count of H1-B visas in any year **only 12.3% of work visa holders in 2019 were sponsored for EB-2.**

Intrestignly employers very rarely sponosor EB-2s for F-1 students (5.6%). One might think that desperate employers would skip the uncertain H1-B visa lottery and choose more propable solution like EB-2 (there is no lottery), but unfortunely that's not the case. **Furthermore, if we assume that only students on OPT are eligibale to get sponosored (a conservative case), only 3.6%  were sponsored an EB-2 in 2018.** For perspective, it was more probable to get into [Harvard University](https://college.harvard.edu/admissions/admissions-statistics) this year.

### What are the most sponosored positions?
<img src="/public/pics/blog/get_lucky/pos_bar.png">
The most popular postions amongs EB-2 applicants in last 5 years was software engineer with 6%. However, clearly the first 6 postions in the list describe the same job, so practically **software dev/engineering postions account for ~15% of all applications**. Interestingly, there have been 3.77x more poulty processing worker applications and data scientist'. (I should have become a poultry processing worker)

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
      <td>716</td>
      <td>3.5%</td>
    </tr>
    <tr>
      <td>Google</td>
      <td>708</td>
      <td>3.5%</td>
    </tr>
    <tr>
      <td>Los Angeles</td>
      <td>598</td>
      <td>3.5%</td>
    </tr>
    <tr>
      <td>Miami</td>
      <td>525</td>
      <td>3.5%</td>
    </tr>
  </table>
  <figcaption class="image-caption">2019 EB-2 Applications by City</figcaption>
</figure>
Obviously the biggest sponosrs, as we hear in the [news](https://news.bloomberglaw.com/daily-labor-report/it-consulting-industry-hardest-hit-by-jump-in-h-1b-denials-1), are IT and Tech comapnies. Cognizant takes the first place with 3.5% of applications in last 5 years. Then it's Microsoft, Facebook and Google with X.X%, X.X%, X.X% repspectivel
### Where are the EB-2 sponosrs located?
<img src="/public/pics/blog/get_lucky/city_bar.png">
In last 5 years New York City, Los Angeles and Houston has been the epicenters of EB-2 sponsors. Even though thease cities are not the ones creating the most applications, these are the markets with the largest variety of employeers. The cities with most applications would be locations of major EB-2 sponsors like Coginzant Technologies - College Station, TX and Amazon - Seatlle, WA. Although it's important to keep these companies in mind, these job markets are really overpowered by few large players.

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
To have the highest chances for EB-2, if you should be a Software Engineer on H1-B, working at one of the top companies. However there are a lot of other smaller companies or companies with smaller engineering teams, where you might have equal chances of getting a green card sponsored. Perhaps try finding comapnies like that in New York, NY, San Francisco, CA or Houston, TX.

### Data & Code
To get green card application data is scraped one of the Green Card sponors database websites (like immihelp.com) using lxml in python (notebook). Then analyzed the data with Pandas, numpy and matplotlib.

I will soon release the code and data.

### Future work:
1. Analyze H1-B sponsors
2. Try to dig deeper in the data
3. Improve visualizations
4. Implement fuzzy name matching for names of companies, cities, and postions
5. Analyze salary data
6. Analyze lawyer data

#### If you have any questions or comments, feel free to send me a DM [@michallys](https://twitter.com/michallys).
