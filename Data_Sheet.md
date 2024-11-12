# Datasheet Template
The dataset was provided on the Kaggle website [Life Expectancy (WHO) Fixed](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated). It provides life expectatancy and a number of health and economic related indicators for the period 2000-2015. This was based on primary data sources from _WHO_, _World Bank_, and _Our World in Data_:

- The [World Health Organization (WHO)](https://www.who.int/about) is a specialized agency of the United Nations responsible for global public health.
- The [World Bank](https://www.worldbank.org/ext/en/who-we-are) is an international financial institution that provides loans and grants to the governments of low- and middle-income countries for the purposes of economic development.
- [Our World in Data](https://ourworldindata.org/about) is a collaborative effort between researchers at the University of Oxford, who are the scientific editors of the website content; and the non-profit organization Global Change Data Lab (GCDL), who publishes and maintains the website and the data tools that make our work possible.

## Motivation
**For what purpose was the dataset created?** _Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description._ <br>
The primary motivation given [here](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated) is to correct an existing WHO [dataset](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) on life expectancy. 

**Who created the dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)?** <br>
The dataset was created by a data scientist Lasha Gochiashvili. No affiliation was provided on the appropriate [Kaggle](https://www.kaggle.com/lashagoch) page. 

**Who funded the creation of the dataset?** _If there is an associated grant, please provide the name of the grantor and the grant name and number._ <br>
No funding is mentioned.

**Any other comments?** <br>
None

## Composition
**What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?** _Are there multiple types of in
stances (e.g., movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description._ <br>
This is tabular numerical data.

**How many instances are there in total (of each type, if appropriate)?** <br>
There are 2,864 instances in total.

**Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** _If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g., geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g., to cover a more diverse range of instances, because instances were withheld or unavailable)._ <br>
It contains all possible instances.

**What data does each instance consist of?**  _“Raw” data (e.g., unprocessed text or images) or features? In either case, please provide a description._ <br>
The data schema is given here: https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated

For convenience I have summarised this below:

| Attribute                  | Comment     | Source  |
| :----                       | :----         | :-----
| Country                     | List of 179 countries  | 
| Region                      | 179 countries are distributed in 9 regions. E.g. Africa, Asia, Oceania, European Union, Rest of Europe and etc. | 
| Year                        | Years observed from 2000 to 2015    | 
|	Infant_deaths               | Infant deaths per 1000 population | WHO
|	Under_five_deaths           | Deaths of children under five years old per 1000 population | WHO
|	Adult_mortality             | Number of deaths between the ages of 15 years of age to 60 years per 1,000 population | WHO
|	Alcohol_consumption         | Alcohol consumption that is recorded in liters of pure alcohol per capita with 15+ years old | WHO
|	Hepatitis_B                 | Percentage of coverage of Hepatitis B (HepB3) immunization among 1-year-olds | WHO
|	Measles                     | Percentage of coverage of Measles containing vaccine first dose (MCV1) immunization among 1-year-olds | WHO
|	BMI                         | BMI is a measure of nutritional status in adults. It is defined as a person's weight in kilograms divided by the square of that person's height in meters (kg/m2) | WHO
|	Polio                       | Percentage of coverage of Polio (Pol3) immunization among 1-year-olds | WHO
|	Diphtheria                  | Percentage of coverage of Diphtheria tetanus toxoid and pertussis (DTP3) immunization among 1-year-olds | WHO
|	Incidents_HIV               | Incidents of HIV per 1000 population aged 15-49 | World Bank
|	GDP_per_capita              | GDP per capita in current USD | World Bank
|	Population_mln              | Total population in millions | World Bank
|	Thinness_ten_nineteen_years | Prevalence of thinness among adolescents aged 10-19 years. BMI < -2 standard deviations below the median | WHO
|	Thinness_five_nine_years    | Prevalence of thinness among children aged 5-9 years. BMI < -2 standard deviations below the median | WHO
|	Schooling                   | Average years that people aged 25+ spent in formal education | Our world in data
|	Economy_status_Developed    | Developed country | World Bank
|	Economy_status_Developing   | Developing country | World Bank
|	Life_expectancy             | Average life expectancy for both genders | WHO

Developed status has been derived from World Bank Gross National Income

**Is there a label or target associated with each instance?** _If so, please provide a description._ <br>
No. All numerical data, including life expectancy, is provided for each Country from the period 2000-2015.

**Is there any missing information from individual instances?** _If so, please provide a description, explaining why this information is missing (e.g., because it was unavailable). This does not include intentionally removed information, but might include, e.g., redacted text._ <br>
No.

**Are relationships between individual instances made explicit (e.g. users’ movie ratings, social network links)?** _If so, please describe how these relationships are made explicit._ <br>
There are no relationships.

**Are there recommended data splits (e.g., training, development/validation, testing)?** _If so, please provide a description of these splits, explaining the rationale behind them._ <br>
No.

**Are there any errors, sources of noise, or redundancies in the dataset?** _If so, please provide a description._ <br>
There is a minor redundancy in that the fields _Economy_status_Developed_ and _Economy_status_Developing_ provide precisely complementary information.
 
**Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g., websites, tweets, other datasets)?** _If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g. licenses, fees) associated with any of the external resources that might apply to a dataset consumer? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate._ <br>
The dataset is self-contained.

**Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor–patient confidentiality, data that includes the content of individuals’ non-public communications)?** _If so, please provide a description._ <br>
No.

**Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** _If so, please describe why._ <br>
No.

**Does the dataset identify any subpopulations (e.g., by age, gender)?** _If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset._ <br>
The dataset is indexed by Country and Year.

**Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** _If so, please describe how._ <br>
No.

**Does the dataset contain data that might be considered sensitive in any way (e.g., data that reveals race or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** _If so, please provide a description._ <br>
No.

**Any other comments?** <br>
No.

## Collection process
**How was the data associated with each instance acquired?** _How was the data associated with each instance acquired? Was the data directly observable (e.g., raw text, movie ratings), reported by subjects (e.g., survey responses), or indirectly inferred/derived from other data (e.g., part-of-speech tags, model-based guesses for age or language)? If the data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how._ <br>
The data was retrieved from [Kaggle](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated). This in turn used data from WHO, WorldBank, and Our World in Data.

**What mechanisms or procedures were used to collect the data (e.g., hardware apparatuses or sensors, manual human curation, software programs, software APIs)?** _How were these mechanisms or procedures validated?_ <br>
Not known.

**If the dataset is a sample from a larger set, what was the sampling strategy (e.g., deterministic, probabilistic with specific sampling probabilities)?** <br>
It is the complete dataset.

**Who was involved in the data collection process (e.g., students, crowdworkers, contractors) and how were they compensated (e.g., how much were crowd workers paid)?** <br>
Not known.

**Over what time frame was the data collected?** _Does this timeframe match the creation timeframe of the data associated with the instances
 (e.g., recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created._ <br>
The data was collected over the period 2000-2015 which corresponds to the timeframe of the data.

**Were there any ethical review processes conducted (e.g. by an institutional reviewing board?)** _If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation._ <br>
Not known.

**Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g., websites)?** <br>
The data was obtained from the Kaggle website.

**Were the individuals in question notified about the data collection?** _If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or other wise reproduce, the exact language of the notification itself._ <br>
Not known.

**Did the individuals in question consent to the collection and use of their data?** _If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented._ <br>
Not known.

**If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** _If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate)._ <br>
Not known.

**Has an analysis of the potential impact of the dataset and its use on data subjects (e.g., a data protection impact analysis) been conducted?** _If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation._ <br>
Not known.

**Any other comments?** <br>
No.

## Preprocessing/cleaning/labelling

**Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** _If so, please provide a description. If not, you may skip the remaining questions in this section._ <br>
No.

**Was the “raw” data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?** _If so, please provide a link or other access point to the
 “raw” data._ <br>
No.

**Is the software that was used to preprocess/clean/label the data available?** _If so, please provide a link or other access point._ <br>
No.

**Any other comments?** <br>
No.

## Uses
**Has the dataset been used for any tasks already?** _If so, please provide a description._ <br>
Yes. Many other users on Kaggle have used this dataset.

**Is there a repository that links to any or all papers or systems that use the dataset?** _If so, please provide a link or other access point._ <br>
This information is available in [Kaggle](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated/code).

**What (other) tasks could the dataset be used for?** <br>
This could be used for studying trends in vaccinations, schooling, or infant deaths.

**Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** _For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other risks or harms (e.g., legal risks, financial harms)? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms?_ <br>
Not known.

**Are there tasks for which the dataset should not be used?** _If so, please provide a description._ <br>
Not known.

**Any other comments?** <br>
No.

## Distribution
**Will the dataset be distributed to third parties outside of the entity (e.g., company, institution, organization) on behalf of which the dataset was created?** _If so, please provide a description._ <br>
This dataset is publically available on Kaggle.

**How will the dataset will be distributed (e.g., tarball on website, API, GitHub)?** _Does the dataset have a digital object identifier (DOI)?_ <br>
The CSV dataset is publically available on [Kaggle](https://www.kaggle.com/datasets/lashagoch/life-expectancy-who-updated/data).

**When will the dataset be distributed?** <br>
It was distributed on Kaggle in 2023.

**Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?** _If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions._ <br> 
There is no copyright. It is distributed under the [Creative Commons license 1.0](https://creativecommons.org/publicdomain/zero/1.0/)

**Have any third parties imposed IP-based or other restrictions on the data associated with the instances?** _If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms, as well as any fees associated with these restrictions._ <br>
No.

**Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?** _If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any supporting documentation._ <br>
No.
 
**Any other comments?** <br>
No.

## Maintenance
**Who will be supporting/hosting/maintaining the dataset?** <br>
The creator has declared that no updates will be produced.

**How can the owner/curator/manager of the dataset be contacted (e.g., email address)?** <br>
The creator is available via [Kaggle](https://www.kaggle.com/lashagoch), [GitHub](https://github.com/lashagoch), or [LinkedIn](https://www.linkedin.com/in/lashagochiashvili/).

**Is there an erratum?** _If so, please provide a link or other access point._ <br>
No.

**Will the dataset be updated (e.g., to correct labeling errors, add new instances, delete instances)?** _If so, please describe how often, by whom, and how updates will be communicated to data set consumers(e.g., mailing list, GitHub)?_ <br>
No.

**If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g., were the individuals in question told that their data would be retained for a fixed period of time and then deleted)?** _If so, please describe these limits and explain how they will be enforced._ <br>
N/A.

**Will older versions of the dataset continue to be supported/hosted/maintained?** _If so, please describe how. If not, please describe how its obsolescence will be communicated to dataset consumers._ <br>
N/A.

**If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?** _If so, please provide a description. Will these contributions be validated/verified? If so, please describe how. If not, why not? Is there a process for communicating/distributing these contributions to dataset consumers? If so, please provide a description._ <br>
No.

**Any other comments?** <br>
None.
