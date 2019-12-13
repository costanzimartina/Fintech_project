# Car insurance premium rate determination

### Summary of variables to include in premium rate calculation:

| Variable                 | Type    | Categories                                                   |
| ------------------------ | ------- | ------------------------------------------------------------ |
| Age (*)                  | Boolean | Teen driver (1), Adult driver (0)                            |
| Driving_record (*)       | Integer | Quantity of incidents                                        |
| Credit_score             | Integer | Poor (0), Medium (1), Good (2)                               |
| Driving_experience (*)   | Integer | Quantity of years of driving experience                      |
| Location (*)             | Boolean | City (1), Not City (0)                                       |
| Gender (*)               | Boolean | Male (1), Female (0)                                         |
| Insurance_record (*)     | Integer | Quantity of years of insurance coverage (rounded up, so None = 0) |
| Marital_status           | Boolean | Married (0), Not married (1)                                 |
| Claims_record (*)        | Integer | Quantity of claims filed                                     |
| Coverage_level           | Integer | Depends on categories and amount of types of coverage included (I think for simplicity in our model we'd be offering just one type and therefore this variable wouldn't be necessary). |
| Vehicle_type (*)         | Boolean | New (0), Old (1)                                             |
| Vehicle_ownership_status | Integer | Owned (0), leased (1), financed (2)                          |

For the initial model to be generated, just the most relevant should be included for simplicity's sake.  I marked them with an (*), although wee could even use less.



## Breakdown

A rating factor is an individual characteristic of a customer used to price car insurance premiums. 

Put simply, the less risky your rating factors, the cheaper your car insurance. Some auto insurance rating factors — such as driving record or vehicle type — have relatively large impacts on car insurance costs. Others — like gender or marital status — are less important. Below are the 15 rating factors most often used by car insurance companies, along with associated costs by insurer.

### 1. Age

Age is a very significant rating factor, especially for young drivers.

Data show that teen drivers drive more recklessly and get into more accidents than do drivers in any other age group.

###### INSURANCE PREMIUMS BY AGE

| **Insurance Provider** | **6-month premium — Teen Driver** | **6-month — 50-yo** |
| ---------------------- | --------------------------------- | ------------------- |
| Allstate               | $1,851                            | $874                |
| Farmers                | $1,272                            | $650                |
| GEICO                  | $1,170                            | $577                |
| Liberty Mutual         | $1,472                            | $677                |
| Nationwide             | $1,108                            | $575                |
| Progressive            | $1,360                            | $658                |
| State Farm             | $1,247                            | $607                |
| USAA                   | $752                              | $418                |
| Average                | $1,279                            | $630                |

### 2. Driving record

Car insurance companies see a driver's past as an accurate predictor of their future performance. 

A history of tickets or violations will inflate the cost of current and future insurance premiums. The below data show how a speeding ticket (speeding 16-20 miles per hour over the limit), a DUI, and a reckless driving charge may impact insurance premiums.

![average premium by violation type](https://doubxab0r1mke.cloudfront.net/media/zfront/production/images/Average_6-Month_Premium_by_Violation_2.width-800.png)

### 3. Credit score

Credit is a major — but often overlooked — rating factor. 

Data from the Federal Trade Commission show drivers with poor credit file more claims than do drivers with better credit. And when they do file claims, they are generally more expensive than claims from drivers with good credit.

###### INSURANCE PREMIUMS BY CREDIT HISTORY

| **Insurance Provider** | **6-month premium — Very Poor Credit** | **6-month premium — Great Credit** |
| ---------------------- | -------------------------------------- | ---------------------------------- |
| Allstate               | $1,597                                 | $850                               |
| Farmers                | $1,180                                 | $668                               |
| GEICO                  | $1,130                                 | $599                               |
| Liberty Mutual         | $1,823                                 | $698                               |
| Nationwide             | $934                                   | $586                               |
| Progressive            | $1,647                                 | $639                               |
| State Farm             | $1,512                                 | $536                               |
| USAA                   | $1,128                                 | $427                               |
| **Average**            | $1,369                                 | $625                               |

In the above table, "worst credit" is defined as a credit rating between 300 and 579. A "best credit" rating sits between 800 and 580. 

### 4. Years of driving experience

The more experience you have behind the wheel, the less likely you are to make the mistakes that lead violations and claims. For an insurance company, this means you’re less risky of a client. Drivers with many years of experience typically enjoy lower insurance prices than do newer drivers. 

### 5. Location

City dwellers pay more for insurance because there are more people in cities, raising the likelihood of theft, accidents or vandalism. In fact, which city you call home may also affect your premium rates. 

### 6. Gender

Men typically drive more miles than women and more often engage in risky driving practices including not using seat belts, driving while impaired by alcohol, and speeding. Crashes involving male drivers often are more severe than those involving female drivers.

###### INSURANCE PREMIUMS BY AGE & GENDER

| **Gender and Age Group** | **6-Month Premium** |
| ------------------------ | ------------------- |
| Female Teen Driver       | $1,245              |
| Male Teen Driver         | $1,399              |

### 7. Insurance record

Unless you are a brand new driver, insurance companies see a lack of continuous coverage as a major risk factor. In an insurance company's estimation, if you were licensed but didn't have insurance, you were most likely driving uninsured. Driving without insurance is considered irresponsible and so it results in higher premiums. 

The below data show the difference between drivers with no previous coverage and five years of consecutive coverage: $119 per year.

![average 6-month premium by insurance history](https://doubxab0r1mke.cloudfront.net/media/zfront/production/images/Average_6-Month_Premium_by_Insurance_History_1.width-800.png)

### 8. Marital status

Married drivers are considered more likely to drive with loved ones in the passenger seat; fewer accidents are reported in this group, perhaps because of a reluctance to take needless risks when children and family members are in their cars. A study in New Zealand proved that never-married drivers are twice as likely to file a claim for collision, making single drivers a high-risk group regardless of their safety measures.

### 9. Claims record

Every single insurance company sees a long claims history as a red flag. Included in your claims history is any insurance claim you file — and any claim filed against you. If your insurance company pays out a claim, you should expect your rate to increase. 

Below are estimated rates from popular insurance companies across the U.S. after an at-fault accident.

| **Insurance Provider** | **None** | **6-month premium** |
| ---------------------- | -------- | ------------------- |
| Allstate               | $993     | $1,425              |
| Farmers                | $781     | $1,010              |
| GEICO                  | $602     | $934                |
| Liberty Mutual         | $769     | $1,181              |
| Nationwide             | $667     | $859                |
| Progressive            | $777     | $1,343              |
| State Farm             | $665     | $802                |
| USAA                   | $458     | $607                |

### 10. Coverage level

The more coverage you have, the more expensive it will be. The reason for this is simple: if you carry more coverage, your insurance company is obligated to pay out to meet a higher coverage limit.

![average premium by coverage level](https://doubxab0r1mke.cloudfront.net/media/zfront/production/images/6-Month_Premium_by_Coverage_Level.width-800.png)

### 11. Vehicle

Insurance rates on a brand new sports car will be more expensive than premiums for a 1999 Civic. If a vehicle costs more to replace, the insurance company will charge you more each month to cover these potential costs (via collision and comprehensive coverage). 

### 12. Vehicle ownership status

Car insurance companies categorize car ownership in three ways: owned, leased, and financed. Premiums vary by ownership status.



## References

- https://www.thezebra.com/auto-insurance/factors-affecting-car-insurance-rates/

  (Full methodology is available in https://www.thezebra.com/state-of-insurance/auto/2019/ )

- https://www.insurancecompanies.com/insider-information-how-insurance-companies-measure-risk/

