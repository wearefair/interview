# Data Engineering - ETL Code Challenge

This code challenge focuses on ETL and reporting tasks. You will extract data from a postgres database and generate reports with said data. Ideally, you will load this data into a reporting database / data warehouse.

## Source Data
Your dataset is from Federal Elections Committee campaign contributions data. This data has been extracted from OpenSecrets (https://www.opensecrets.org/) and provided as a Postgres Dump here: https://github.com/Solomon/opensecrets_to_postgres

This database includes:
#### Candidates
- cid (candidate unique ID)
- party (party affiliation)
- cycle (election cycle)

#### Committees
- includes PACs (political action committes, campaign committees, Republican National Committee, etc)
- committee_id (committee unique ID)
- party (party affiliation)

#### industry_codes
- category_code
  - `real_code` in `individual_contributions` associates to this code
- industry_code
  - a less granular grouping
- sector
  - an even less granular grouping

#### individual_contributions
- This table contains all the individual contributions
- cycle (election cycle)
- recipient_id
  - This is the recipient of the contribution.
  - That recipient can either be a candidate (begins with N) or a committee (begins with C).
- date
- amount
- real_code
  - associates to `category_code` on `industry_codes` table (though not with a foreign key)
- committee_id
  - The committee this was donated to. If this and recipient_id do not match, then it was donated to this committee for the intended recipient. For example, a donation to committee_id `C00431445` (Obama for America) would generally have the recipient_id of `N00009638` for candidate `Barack Obama (D)`.
- other_id
  - same as committee_id, except the committee_id was likely a pass through to providing the money to this committee. For example, ActBlue (https://en.wikipedia.org/wiki/ActBlue) is a fundaising PAC that simply passes on the money to the candidate you intended it to be donated to. Thus, the committee_id would be for ActBlue `C00401224` but the other_id would be or Obama for America (`C00431445`).
- gender
  - gender of contributor
- location information
  - city
  - state
  - zip

## Desired Reports:

### Columns Per Report:
- Total $ donated
- Total number of contributors
- Average $ donation amount
- By Gender
  - number of female contributors
  - Total $ contributed from female contributors
  - Average $ donation amount by female contributors
  - number of male contributors
  - Total $ contributed from male contributors
  - Average $ donation amount by male contributors
- First Time Contributors
  - contributors who this cycle is their first political contribution to any organization
  - number of contributors
  - Total $ contributed from those contributors
  - Average $ donation amount by first time contributors
- Small Contributors
  - Contributed less than $100 total for that cycle
  - number of contributors
  - Total $ contributed from those contributors
  - Average $ donation amount by small contributors
- Large Contributors
  - Contributed more than $2,000 total for that cycle
  - number of contributors
  - Total $ contributed from those contributors
  - Average $ donation amount by large contributors


### Set of Reports:
- By Cycle (e.g. 2000, 2002, 2004, 2006, ...)
- By Party by Cycle (e.g. Republicans in 2000, Democrats in 2000, Republicans in 2002, Democrats in 2002, ...)
- Top 20 candidates by amount raised by cycle (e.g. Obama 2008, McCain 2008, ...)
- Top 20 committees by amount raised by cycle (e.g. Republican National Committee 2008, Obama For America 2008, ...)
- By Industrial Sector by Cycle
  - `real_code` attribute on `individual_contributions` joined to `category_code` on `industry_codes` table. Then aggregated by `sector` attribute on `industry_codes`.
  - Additional Columns for this report:
    - breakdowns by political party


## Requirements

**Absolute:**
- Use Python
- Provide reproducible results and code (enabling us to reproduce)
- You can use an ETL framework like airflow or luigi or you can roll your own.

**Nice to Have:**
- Load results into a data warehouse (the L of the ETL)
  - Can simply be another postgres DB. At a minumum export the data as flat files if you don't load them into another data store.





