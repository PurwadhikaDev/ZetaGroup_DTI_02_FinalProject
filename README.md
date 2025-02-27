# **<big> HOTEL BOOKING CANCELLATION PREDICTION </big>**

Group Contibutors :
1. Ergia Lativolia Putri Subiyantari
2. Diah Purnamaningsih Mulyawan
3. Kezia Patricia Fadli

## [Business Problem Analytics:](https://example.com)
A company operating in the hospitality industry, specifically in the hotel sector, is based in Portugal. The dataset has been extracted from the hotel's Property Management System (PMS), which records various aspects of reservations, including cancellation status, room rates (ADR), length of stay, and more. The hospitality industry falls under the lodging sector, which plays a crucial role in providing accommodation for both domestic and international travelers. 

According to the Crishty & CO Industry Report (2023) [3], more than 28.4 million tourists visited Portugal, contributing nearly 16% to the country's GDP. Regions such as Lisbon, Algarve, and Madeira are the main tourist hubs, with more than 70% of total stays coming from international tourists.

There is also a noticeable shift in travel trends, where Portugal has surpassed Spain as the primary source of tourists in Lisbon. The industry report "Staying Power" predicted that occupancy rates would increase in 2016 and 2017 in Lisbon. However, our analysis revealed a decline in occupancy rates, especially in City Hotels.

Some possible reasons include:
- Over-Supply of Hotels: Lisbon experienced a surge in new hotels, increasing competition and impacting occupancy in certain hotels.
- Changing Travel Trends: Global events, security concerns, and economic factors have shifted travel preferences, with a higher preference for Resort Hotels over City Hotels.

The Staying Power Industry Report (2015-2017) [2] states that Portugal experienced economic growth of 1.6%-1.7%, with increased tourism due to a weaker Euro and improved airline connectivity. However, global factors have influenced tourist behavior, such as:
- Economic Uncertainty: Events like Brexit or terrorist attacks led to a decline in business travel, increasing the cancellation ratio in City Hotels to 0.44 and decreasing occupancy growth (-11% in 2016, -6% in 2017). City Hotels are more impacted by global factors since their guests often include business travelers or international event participants (groups). Resort Hotels are more stable, with a lower cancellation ratio (0.31) and occupancy rates ranging between 67%-79%, even with a slight decline in occupancy growth (-5% & -10%).
- Currency Fluctuations: A weaker Euro was expected to attract more non-Eurozone tourists, but City Hotels still faced declining occupancy. This suggests that tourists preferred resorts for long vacations rather than business trips to city centers.

The cancellation rate in our dataset is 30% for City Hotels and 23.7% for Resort Hotels. Lower than the global average (33%-40%) (HospitalityTech, 2019) [3]. Resort Hotels have a lower cancellation ratio (0.31), likely due to contract and group bookings, which are less affected by economic and political factors. City Hotels have a higher cancellation rate due to their customer base, which includes business travelers with flexible schedules.
The most influential customer type in our dataset is "transient" (flexible customers).

Seasonality Impact on Occupancy Rates:
- Peak Season (Sept–Nov) = High occupancy, especially in Resort Hotels. For example, a direct booking website for Algarve resorts in Portugal offers a 15% off-season promo in early autumn with an average stay lead time of 5-6 days [4]. September–October is an ideal time to visit Algarve as the season transitions from winter [5].
- Low Season (Apr–Jun) = Stable but lower than peak season.
- Off-Season (Dec & Aug) = Significant occupancy decline, especially in City Hotels.
- ADR (Average Daily Rate) Trends in City Hotels within 32.5 EUR in 2015, 36.2 EUR in 2016 and 38.9 EUR in 2017. This increase in ADR suggests a pricing strategy that may have been too aggressive, contributing to an occupancy decline of -11% & -5%.
According to the Staying Power Report (2015-2017) [2], Lisbon’s ADR increased to 95-99 EUR due to major events in 2016, such as The Web Summit (moved from Dublin) and Diabetes Conference as well as new airline routes.
These events drove higher demand, pushing ADR up and increasing occupancy.

Target Feature (is_canceled):

1 : Cancel (positive)
0 : No Cancel (negative)

## [Project Stakeholders:](https://example.com)
Project Stakeholders:
- Marketing & Sales Departement : Responsible for maximizing revenue through marketing strategies (e.g., promotions/discounts). This model will help identify the right customers for promotions, ensuring a more targeted approach.
- Revenue Management : One of The Finance Department jobdesc are manages the company's income and expenses, including those from marketing campaigns.

Since marketing and sales impact revenue, both departments need to work together to maximize profits.

## [Analytic Approach:](https://example.com)
We will analyze the dataset to identify patterns that differentiate customers who will cancel their booking vs. those who won’t.

Then, we will build a supervised machine learning classification model to help the company predict cancellations and take proactive action.

## [Metric Evaluation:](https://example.com)
- Type I Error: False Positive Cindition where the model predicts a customer will cancel, but in reality, they do not.
Consequence: Misguided marketing efforts, leading to suboptimal revenue. Financial Impact: Without marketing intervention, the hotel could still earn 101 EUR.

- Type II Error: False Negative Condition is where the model predicts a customer will not cancel, but in reality, they do.
Consequence: Lost potential revenue due to missed marketing opportunities.
Financial Impact: The marketing cost average per customer is 10.07 - 10.14 EUR and the worst-case scenario the hotel could earn 113.2 EUR ADR without marketing costs.


## [Tableau:](https://example.com)
Tableau link: https://public.tableau.com/shared/9KZYM93CF?:display_count=n&:origin=viz_share_link

![image](https://github.com/user-attachments/assets/28769744-9855-48d4-9cf2-28dd6ccbc6e6)



## [Sources:](https://example.com)

[1] [Nama Tampil]([https://example.com](https://assets-eu-01.kc-usercontent.com/6bb3df3c-b648-01ae-2357-22fa5c7d5f19/93b732c7-e612-4890-88f4-31d2996a52eb/Portugal%20Hotel%20Market%20Performance%202023))
[2] [Nama Tampil](https://www.pwc.ch/en/publications/2016/european-cities-hotel-forecast-2016-2017.pdf)
[3] [Nama Tampil](https://hospitalitytech.com/global-cancellation-rate-hotel-reservations-reaches-40-average) 
[4] [Nama Tampil](https://algarveresorts.net/en/promocoes/ver/6)
[5] [Nama Tampil](https://myportugalholiday.com/portugal-guides/portugal-september.html#google_vignette)
[6] [Nama Tampil](https://www.sciencedirect.com/science/article/pii/S2352340918315191) 
[7] [Nama Tampil](https://www.bdc.ca/en/articles-tools/marketing-sales-export/marketing/what-average-marketing-budget-for-small-business#:~:text=1.-,Start%20by%20researching%20your%20industry,%E2%80%94between%205%20and%2010%25.)
