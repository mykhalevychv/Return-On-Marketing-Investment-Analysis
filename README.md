## Return on Marketing Investment Analysis for Weekly Cohort

### Overview of the Dataset

![Dataset Overview](https://github.com/user-attachments/assets/cb394090-e2b1-4ca2-80c9-6ced18ae7115)

Firstly, we clean the dataset by removing rows where information about `spend_usd` is missing but where we have data on users or revenue.

Next, we examine statistics for each row to see how the data is populated.

![Data Statistics](https://github.com/user-attachments/assets/de76f792-ffa4-46bf-96f7-fee7f917a908)

Then, we analyze the distribution of `spent_usd` and `revenue`.

![Spent vs Revenue Distribution 1](https://github.com/user-attachments/assets/c41b9743-8b03-4a30-81e8-4246ac785dd5)
![Spent vs Revenue Distribution 2](https://github.com/user-attachments/assets/92e743f2-bc72-4612-be39-ef0b99c23231)

For the first media source, spending and revenue are nearly equal, but overall spending is higher. The second media source shows more profitability, with the largest profit occurring on 2021-01-01. The third media source's spending and revenue are both counted from 2021-01-01, but total spending exceeds total revenue.

Next, we calculate ROMI using the formula ((revenue - spend)/spend x 100)

We then calculate the total ROMI for each media source.

![Total ROMI](https://github.com/user-attachments/assets/188d241e-d50c-4615-a371-d9d716e2b54c)

- The highest total ROMI is for media source 2, while the lowest is for media source 3.

Then we output the total ROMI based on total revenue and spending for each media source and country.

![Total ROMI by Country](https://github.com/user-attachments/assets/b67132f4-a278-4254-a62c-12bd5f839473)

We also display the bottom 10 countries with the lowest total ROMI for each media source.

![Bottom 10 Countries by ROMI](https://github.com/user-attachments/assets/4eef85cf-40e8-4d61-ad5b-5df9edb07b1e)

- Since the total ROMI for media source 3 is negative and only the US shows positive total ROMI, the first conclusion is that we can stop acquiring traffic from this source.

## Further Analysis for Media Source 1 and Media Source 2
We can leave countries for media source 1 and media source 2 where the total ROMI for all days exceeds 30%.

### Countries with Total ROMI > 30%
- **Media Source 1**: 'AG', 'AL', 'AR', 'AT', 'AU', 'AZ', 'BG', 'BH', 'BJ', 'BM', 'BR', 'BS', 'CI', 'CL', 'DE', 'GG', 'GH', 'HN', 'HU', 'IM', 'IT', 'JP', 'LA', 'LI', 'LT', 'MV', 'NG', 'PK', 'PY', 'QA', 'SG', 'SK', 'TC', 'TZ', 'UA', 'UY', 'VC'
- **Media Source 2**: 'AE', 'AR', 'CA', 'DE', 'DO', 'GB', 'MA', 'MX', 'NL', 'NO', 'SA', 'US'

For countries where total ROMI is lower than 30%, we will check if it improves on certain days.

![ROMI by Country and Date 1](https://github.com/user-attachments/assets/df80ffd0-348c-45ff-8b76-27a42e945167)
![ROMI by Country and Date 2](https://github.com/user-attachments/assets/79438746-4c7f-4a3a-957c-b04d250ecb94)

- From these plots, we can draw conclusions about specific countries and days, allowing us to decide whether to acquire more traffic for these particular countries and days.


