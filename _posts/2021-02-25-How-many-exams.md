---
layout: post
title:  How many exams should you pass before you graduate? Let's do a NPV anaylsis.
date:   2021-02-25
categories: [Actuarial, Exams]
excerpt: One of the most common questions I heard is whether passing more actuarial exams before graduation is good things. Since we are all want be an actuary, let's look at this question in an actuarial way. We will perform a NPV (Net Present Value) anaylsis.
---

![NPV of SOA exams](/images/article_images/2021-02-25-How-many-exams/NPV_Exam.png)

One of the most common questions I heard is whether passing more actuarial exams before graduation is a good thing.
Since we all want to be actuaries, let’s look at this question in an actuarial way.
We will perform an NPV (Net Present Value) analysis.



### Gains and loss of passing exams

To begin, let's identify what are the gains of passing exams before and after graduation.<br>
For passing exams before graduation, the gains are:

- Getting exam salary raise added to starting salary
- Progress faster in exams, reaching fellowship exams with much higher salary raise earlier

For passing exams after working in a company, the gains are:
- Full reimbursement of exam fee and study materials
- Study leaves

To find out which benefits are greater, we will proceed to the analysis.



### NPV of a single exam

Our first model will only consider "salary raise vs reimbursement" for each exam individually.
From the SOA website, we find out how much each exam cost and how often they are offered.
Also, SOA tends to release results 2 months after an exam.
I will assume no further expense but you can add additional study expense in the spreadsheet.
The effective pass rate for each exam can also be found on [Actuarial Lookup](http://www.actuarial-lookup.com/).

Then, I grab exam salary raise from 
[Reddit](https://www.reddit.com/r/actuary/wiki/study_program_survey#wiki_society_of_actuaries_respondents).
I used numbers for John Hancock as an example, but I encourage you to plug in your own numbers as they can vary from company to company.

To calculate the NPV, we need to first consider the cash flow of the two options.
If we take the exams now, we need to pay the exam fee ourselves, but we will have a higher start salary when we graduate if we passed.
If we defer taking the exams, our employer will reimburse our exam fees and study materials, but we will receive our salary raise later.
The following  timeline summarizes the cash flows.

![Cash flow timeline](/images/article_images/2021-02-25-How-many-exams/cash_flow_timeline.png)

C: Exam cost<br>
S: Basic salary<br>
R: Exam raise<br>
P: Probability of pass

To calculate the marginal NPV, we only need to discount the difference in cash flow between both options back to the present.
The following table summarizes the results for preliminary exams.
(I assume there is 2 year until graduation and interest rate is at 3%)


<!-- start of result table -->
<style type="text/css">
.tg  {border-collapse:collapse;border-spacing:0;}
.tg td{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  overflow:hidden;padding:10px 5px;word-break:normal;}
.tg th{border-color:black;border-style:solid;border-width:1px;font-family:Arial, sans-serif;font-size:14px;
  font-weight:normal;overflow:hidden;padding:10px 5px;word-break:normal;}
.tg .tg-wa1i{font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-ogll{background-color:#fce4d6;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-en9y{background-color:#e2efda;font-weight:bold;text-align:center;vertical-align:middle}
.tg .tg-nrix{text-align:center;vertical-align:middle}
</style>
<table class="tg">
<thead>
  <tr>
    <th class="tg-ogll" rowspan="2">Exam</th>
    <th class="tg-wa1i" colspan="2">USD Salary Increase</th>
    <th class="tg-wa1i" rowspan="2">Fee USD</th>
    <th class="tg-wa1i" rowspan="2">Offer frequency (Months)</th>
    <th class="tg-wa1i" rowspan="2">Months til result release</th>
    <th class="tg-wa1i" rowspan="2">Effective pass rate</th>
    <th class="tg-wa1i" rowspan="2">Payback Period (Months)</th>
    <th class="tg-wa1i" colspan="2">Value of taking 1 siting ahead</th>
  </tr>
  <tr>
    <td class="tg-wa1i">Annual</td>
    <td class="tg-wa1i">Monthly</td>
    <td class="tg-ogll">NPV</td>
    <td class="tg-en9y">Profitability Index</td>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-ogll">P</td>
    <td class="tg-nrix">3,000</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">4</td>
    <td class="tg-nrix">49%</td>
    <td class="tg-nrix">1.00</td>
    <td class="tg-ogll">209</td>
    <td class="tg-en9y">84%</td>
  </tr>
  <tr>
    <td class="tg-ogll">FM</td>
    <td class="tg-nrix">3,000</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">2</td>
    <td class="tg-nrix">4</td>
    <td class="tg-nrix">54%</td>
    <td class="tg-nrix">1.00</td>
    <td class="tg-ogll">255</td>
    <td class="tg-en9y">102%</td>
  </tr>
  <tr>
    <td class="tg-ogll">IFM</td>
    <td class="tg-nrix">3,000</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">300</td>
    <td class="tg-nrix">4</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">55%</td>
    <td class="tg-nrix">1.20</td>
    <td class="tg-ogll">475</td>
    <td class="tg-en9y">158%</td>
  </tr>
  <tr>
    <td class="tg-ogll">LTAM</td>
    <td class="tg-nrix">4,000</td>
    <td class="tg-nrix">333</td>
    <td class="tg-nrix">365</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">8</td>
    <td class="tg-nrix">55%</td>
    <td class="tg-nrix">1.10</td>
    <td class="tg-ogll">839</td>
    <td class="tg-en9y">230%</td>
  </tr>
  <tr>
    <td class="tg-ogll">STAM</td>
    <td class="tg-nrix">3,500</td>
    <td class="tg-nrix">292</td>
    <td class="tg-nrix">300</td>
    <td class="tg-nrix">4</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">55%</td>
    <td class="tg-nrix">1.03</td>
    <td class="tg-ogll">595</td>
    <td class="tg-en9y">198%</td>
  </tr>
  <tr>
    <td class="tg-ogll">SRM</td>
    <td class="tg-nrix">3,000</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">260</td>
    <td class="tg-nrix">4</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">71%</td>
    <td class="tg-nrix">1.04</td>
    <td class="tg-ogll">732</td>
    <td class="tg-en9y">282%</td>
  </tr>
  <tr>
    <td class="tg-ogll">PA</td>
    <td class="tg-nrix">3,000</td>
    <td class="tg-nrix">250</td>
    <td class="tg-nrix">1,250</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">8</td>
    <td class="tg-nrix">59%</td>
    <td class="tg-nrix">5.00</td>
    <td class="tg-ogll">-285</td>
    <td class="tg-en9y">-23%</td>
  </tr>
  <tr>
    <td class="tg-ogll">FAP</td>
    <td class="tg-nrix">5,000</td>
    <td class="tg-nrix">417</td>
    <td class="tg-nrix">2,100</td>
    <td class="tg-nrix">6</td>
    <td class="tg-nrix">8</td>
    <td class="tg-nrix">100%</td>
    <td class="tg-nrix">5.04</td>
    <td class="tg-ogll">622</td>
    <td class="tg-en9y">30%</td>
  </tr>
</tbody>
</table>
<!-- end of result table -->

From the result, we can see that almost all exams and FAP have a positive NPV, so it is profitable to take them now.
Exam PA may seem unprofitable at first, but if you are confident enough to pass it with a probability greater than 77%, it will become profitable.
The more confident you are in passing the exam, the higher the NPV.



### NPV of passing all preliminary exam before graduation

Since the first model only considers each exam individually, it does not take into account that the fact we pass exams one by one.
Therefore, let's build a timeline to model this effect.

In the model, we will compare 2 options:
- Option 1: Passed all 7 preliminary exams and FAP before graduation
- Option 2: Passed only exam P, FM, IFM before graduation

For simplicity, I will assume passing all exams on the first attempt (to avoid building a decrement table or stochastic model).
I build a timeline that attempts to take all exams as fast as reasonable.
Detail can be found in the excel model at the [bottom of the page](#taking-exams-is-profitable).

The first graph shows the yearly cash flow resulted from all exam raise.
If we pass more exams before graduation, we need to pay the exam fee ourselves, causing a negative cash flow during the first 2 years.
However, our starting salary is much higher and we can move on to FSA exams sooner.
If we defer exams until graduation, our salary is playing catch up, but we don't need to pay for the exams.

![Cash flow for 2 options](/images/article_images/2021-02-25-How-many-exams/CF_2_option.png)

Marginal cash flow can be calculated as the difference between the two cash flows.
The graph below shows marginal value gain or loss during each year if option 1 is chosen instead of option 2.

![Marginal ash flow](/images/article_images/2021-02-25-How-many-exams/CF_marginal.png)

From the model, if we can pass every exam on the first attempt, we gain an NPV of **USD 45,180** at the time we graduate, which is quite a lot.
Note that this is the best-case scenario, you can play around with the model to simulate different cases.
(Or maybe comment or message me, I would build a stochastic model if a lot of you are interested.)



### Taking exams is profitable 

To summarize, from an actuarial perspective, taking exams as soon as possible is profitable if you intend to stay in the actuarial field after graduation.
However, my model only considers the financial aspect of passing actuarial exams.
There are also other qualitative things to be considered when it comes to exams.

In general, I recommend getting them done as fast as you can.
You gonna have to pass them anyway, why not do it now.
If you what to know how to pass them quickly, check out [my other blog post](https://actuarialcat.github.io/How-to-pass-7-SOA/).

You can **download the spreadsheet model**
<a href="/files/2021-02-25-How-many-exams/NPV_model.xlsx" target="_blank" onclick="tag_share_event('view_external_file', 'How many exam NPV model');"><b>here</b></a>.
I encourage you to use it to simulate different scenarios and put in more accurate assumptions that you have.
The model works for all currencies, just input the exam fees in your local currency.

Just a small caveat, I am writing this based on what I observe in Hong Kong, so your experience may vary from country to country.



<p>&nbsp;</p>

Thanks for reading. I appreciate any feedback.
Connect with me on 
<a href="https://www.linkedin.com/in/jackson-leung-805828174/" target="_blank" onclick="tag_share_event('linkedin_portfolio', '{{ page.title }}');">LinkedIn</a> 
and tell me what I should write about next.




