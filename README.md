# Local Growth Funding in the UK
Automated combination of data sources on local growth funding in the UK

## Data Sources
This a notepad for all possible data sources that we might use in this project. It can be changed, and tidied up, and turned into a table etc... as we make progress.
* [Public Sector Statistical Analyses](https://www.gov.uk/government/statistics/public-expenditure-statistical-analyses-2018) are published by HM Treasury and have National Statistics status. They detail how much is spent, by NUTS1 region, on what, for every year since about 1998 (older tables go back further, there are older table if you look hard). Spending is split into capital and current and into sectors such as "transport". Data is only available in spreadsheets.
* The Eurostat database has many excellent [datasets on science and technology](https://ec.europa.eu/eurostat/web/science-technology-innovation/data/database). Of particular interest is Intramural R&D expenditure (GERD) by sectors of performance and NUTS 2 regions (rd_e_gerdreg). We have written scripts to parse CSV downloads of this data in C#, but the [data is also available via an API](https://ec.europa.eu/eurostat/web/json-and-unicode-web-services) which we need to learn to use.
* [Country and regional analysis](https://www.gov.uk/government/statistics/country-and-regional-analysis-2018) is published by HM Treasury and have National Statistics status. They are available as Excel spreadsheets.
* The [ESPRESSO tool](http://www.neweconomymanchester.com/publications/espresso-tax-and-expenditure-analysis-tool) by Greater Manchester Combined Authority which has already done much of the work on this project and is openly licensed, allowing us to re-use it. This will require significant work to repeat existing data processing algorithms in the Excel spreadsheet in another langauge (C#, Javascript, Python, R, etc...)
* The Heseltine ["No Stone Unturned"](https://www.gov.uk/government/publications/no-stone-unturned-in-pursuit-of-growth) report which is just a PDF but refers to other work that may give us some ideas.
* and lots lots lots more, that it would be great if you could add here! (even if you're not sure that they're relevant, but please be a bit sure that they're relevant).

## Project goal
There are three key parts of this project,
1. To build data parsing scripts that assemble multiple datasets on local growth funding (money spent by government on economic growth which has an identifiable location of impact) into a single dataset that can give a complete view of local growth funding in the UK. We would like to make this comparable with other countries in Europe or the OECD where possible (and if not possible, share the data that is missing).
2. To build a web frontend for visualising this data, and specifically to allow different definitions of "local growth funding" to change the calculations and thus the results.
3. To document this process openly, so that others can learn from our work, suggest improvements, and join in with understanding this complicated issue better.

## Inspirations
* [The OpenFisca project](https://openfisca.org/en/) began in France and has since expanded to many other countries. It aims to represent the whole of the tax and benefits system in open algorithms that anyone can contribute to, re-use, and improve. This means that when data or laws change the impact on society can be calculated in real time. This is in stark contrast to the system we have in the UK where budgets and autumn statements are typically analysed by institutes such as The IFS overnight and then shared with the public.
