# Washington State Certified Public Accountants

## Overview

This dataset lists individuals who hold, or have held credentials from the Washington State Board of Accountancy. The Board of Accountancy provides this data to aid in verifying credentials and disciplinary history. There is a growing demand for CPAs in Washington state, which aligns with the nationwide trend of a growing demand for skilled accounting professionals due to a talent shortage in the field. However the Board does not guarantee the use of this information for any purpose and as such, the information obtained from this database should not be considered an official endorsement of any individual or firm. 

In WA, CPA licenses are valid for 3 years and must be renewed between January 1 and April 30. 

CPA mobility allows a licensed CPA from one state to practice in another state or to transfer your license to another state hence the data shows WA licensed CPAs being in different states and Countries. 

## Importance of the Data

This data provides valuable insights for regulatory bodies, businesses, CPA firms, job recruiters, policymakers, and even CPAs themselves. It helps track industry trends, ensure compliance, and inform business decisions. Such as: 

### 1. State Boards of Accountancy: 
Can monitor license holders to ensure compliance with Washington’s CPA requirements, even if they live out of state.
### 2. Renewal & Compliance Tracking:
Helps track how many CPAs maintain their license, even after relocating.

### 3. Mobility & Relocation Patterns: 
Understanding how many CPAs move out of Washington but keep their licenses helps assess workforce mobility.
### 4. Multi-State Practice: 
Identifies how many CPAs may be serving clients across different states, which is useful for firms expanding operations.

### 5.Recruitment & Talent Acquisition:
Employers can use this data to identify areas with high concentrations of CPAs for hiring purposes.
### Remote Work Trends: 
With remote work becoming more common, companies may look at this data to analyze where CPAs are practicing from.

### 6. License Status Verification: 
Ensures that CPAs representing themselves as Washington-licensed are actually in compliance.

## Data Source

The data is collected and maintained by the Washington State Open Data Portal. Each record represents the tindividuals who hold, or have held credentials from the Washington State Board of Accountancy. To inquire about any disciplinary actions taken against an individual or firm, please contact enforcement at (360) 664-9266. For all other inquiries, please contact customer service at (360) 753-2586.

## Malloy Code Files

This repository contains one Malloy code files:

- [complaints.malloynb](https://github.com/nmonareng/TSA-Complaints/blob/main/complaints.malloynb)



## Summary of Findings

The results provide an overview of the analyzed complaints; however, they may not be fully comprehensive. Unfortunately, some complaints have not been allocated to an airport, category, or subcategory due to missing or incomplete data. As a result, certain insights may be limited, and the findings should be interpreted with this consideration in mind.

Using Malloy, a summary of complaints by country has been generated and this is the code:

This calculation helps analyze the proportion of total complaints attributed to different countries, providing insights into geographic trends in traveler concerns. The results of this code is shown below under visualizations. 

```
SubCategory_Complaints -> {
    group_by: Airport_code.country_name
    aggregate: total_complaints
    # percent
    all_complaints is total_complaints / all(total_complaints)
}
```


### Visualization

## Below are images showcasing some of the main findings from the analysis:

This summary is a result of the above Malloy code. It provides a high-level overview of total complaints in the 448 airports. It further shows the distribution of the complaints to the various airports in different countries with USA leading with the most complaints as it is known to for having the largest number of people flying through it's aiports. With this data we were able to further deduce that 2022 going to 2023 had the most complaints as a result of covid and this is shown in the bar_chart below. 

<img src="https://github.com/nmonareng/TSA-Complaints/blob/main/Summary_of_findings.png?raw=true" width="500">



### Finding 1

This visualization shows the categories with consistently increasing or decreasing complaint trends. The most increasing categories involve Additional Information Required/Insufficient Information,customer service, patdown, screening procedures, and property damage/loss. Some categories, such as Animals, maintain a consistent number of complaints, indicating ongoing concerns in those areas. During COVID-19 airports had to implement a lot of changes such as flight bans, new regulations, and restrictions which led to increased complaints.Understanding this breakdown helps prioritize areas for improvement.  

<img src="https://github.com/nmonareng/TSA-Complaints/blob/main/Findings1.png" width="500">



### Finding 2

This time-series chart tracks the total number of complaints submitted each month. The data reveals long-term trends in passenger dissatisfaction with TSA procedures. There is a clear pattern of increased complaints during peak travel seasons (summer and holidays), suggesting that TSA resources may need to be adjusted accordingly. TSA complaints increased significantly after mid-2021, likely due to the post-COVID travel surge. Complaints remain consistently high, suggesting persistent passenger frustrations with TSA operations and there is no clear downward trend, meaning issues have not been fully resolved.

<img src="https://github.com/nmonareng/TSA-Complaints/blob/main/Findings2.png" width="500">



### Finding 3

This chart highlights how complaints in different sub_categories fluctuate over time. The data helps identify which passenger groups are experiencing more issues over time like, concerns related to Active Duty Military and Age-related complaints.A major spike in a particular subcategory occurred around 2021, possibly due to a policy change. Age-related complaints show irregular patterns, implying potential issues affecting older travelers during specific periods. This may indicate that they were handled, escalated, or remained unresolved. A significant portion of complaints appear to be left unresolved, pointing to potential gaps in TSA’s response system. 

<img src="https://github.com/nmonareng/TSA-Complaints/blob/main/Findings3.png" width="500">


# How to Open a Shared GitHub File and Run Malloy Code
To explore the data and run the analyses:

## 1. Open the Shared GitHub File 

Click on the https://github.com/nmonareng/TSA-Complaints provided to access the shared repository or file. 

Once on Github, click Shift + period this will load the web editor. Then install the malloy extension. See images below for reference:
| **Step**   | **Image Preview** |
|--------|-----------|
| `Step 1 - Press allow` | <img src="step1.png" width="50%"> |
| `Step 2 - Click the Blocks, search for Malloy, install` | <img src="step2.png" width="50%"> |
| `Step 3 - Click Trust` | <img src="step3.png" width="50%"> |
| `Step 4 - Click a .malloynb file` | <img src="step4.png" width="50%"> |
| `Step 5 - Press Run` | <img src="step5.png" width="50%"> |


Navigate to file complaints.malloynb to run the code. 

### Install Dependencies: 

Ensure you have the necessary tools to run .malloynb notebooks. Malloy is a data modeling language; you'll need the appropriate environment to execute these notebooks.

Run the Notebooks: Open and run the .malloynb notebooks using your preferred environment to reproduce the analyses.

If using VS Code, install the Malloy plugin.

## License

This dataset is provided for educational and research purposes. Please cite the TSA as the original data source if used in publications or projects. The Github data files and codes have been generated by Nobuhle Lisa Monareng for Gonzaga University Graduate School of Business as part of the MSBA-622-01 Data Science for Business (Spring 2025) course. 
Additional information and access to the cleaned dataset can be found at the Data Liberation Project: [tsa-complaint-counts](https://www.data-liberation-project.org/datasets/tsa-complaint-counts/).

## Contact

For questions or more information, please contact the TSA at [tsa.gov](https://www.tsa.gov/).

