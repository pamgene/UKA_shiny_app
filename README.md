# UKA app

##### Description

The `UKA_app` allows the user to perform Upstream Kinase Analysis (UKA) for tyrosine or serine threonine kinases. The UKA algorithm predicts differential kinase activity in a Test Condition compared to Control. The UKA uses knowledge from publicly available databases of kinase-substrate relationships. 

##### Details

* Use the Log2 Signals of the 2 groups.

* Significant peptides should not be pre-selected for input. (Pre-selection should only be based on general QC considerations, e.g. removing peptides with low or absent signals.)

* The denominator in the comparison is the group with an initial letter that is ahead in the alphabet, or a lower number. (Numeric characters precede alphabets.)

Input projection|.
---|---
`y-axis`        | numeric, single signal value per cell
`row`           | peptides
`column`| group and samples (e.g. Test Condition and Sample name)
`color`| group (e.g. Test Condition)


Input parameters|.
---|---
`Kinase_family`      | Type of kinase family, either PTK or STK.
`Lock_kinase_family` | If Yes, kinase family cannot be selected when running.

This workflow has 1 operator:

* [Upstream Kinase Analysis Shiny Operator](https://github.com/pamgene/upstream_kinase_analysis_shiny_operator)

More on UKA:  
https://pamcloud.pamgene.com/wiki/Wiki.jsp;jsessionid=C05336E7DB607B2FAB61F9479C1DD2C8?page=Background%20to%20the%20Upstream%20Kinase%20Analysis%20PamApp&TARGET=https%3A%2F%2Fpamcloud.pamgene.com%2Fwiki%2FWiki.jsp%3Bjsessionid%3DC05336E7DB607B2FAB61F9479C1DD2C8%3Fpage%3DBackground%2520to%2520the%2520Upstream%2520Kinase%2520Analysis%2520PamApp&SAMLart=AAFSsPYAkNKN6Mb0Q6Li8D8gawrtLLyj2rv3yxkxmhvECwuISY44YcAl


