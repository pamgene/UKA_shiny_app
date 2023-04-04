# UKA_app

##### Description

`UKA_app` is an application that allows user to perform Upstream Kinase Analysis (UKA) for tyrosine or serine threonine kinases. The UKA algorithm is used to predict differential kinase activity in a Test Condition compared to Control. The UKA uses knowledge from publicly available databases of kinase-substrate relationships. 

##### Details

* This application performs a two group comparison between kinase activity (Here use Log2 Signals of the 2 groups) or kinase inhibition profiles (Here use the Log2 Fold Change/ LFC/ LogRatio/ Delta values) of each sample. Make sure the "control" LFC value is removed, and the LFC of the 2 Groups/ Classes are included. 

* In order to visualise the correct effect DIRECTION, "Control" (=denominator in the comparison) should be of a lower alphabet or number. (Numeric characters precede alphabets.)

* Significant peptides should not be pre-selected for input. (Pre-selection should only be based on general QC considerations, e.g. removing peptides with low or absent signals.)

Input projection|.
---|---
`y-axis`        | numeric, single y value per cell
`row`           | peptides
`column`| samples

Input parameters|.
---|---
`Kinase_family`      | Type of kinase family, either PTK or STK. Default is PTK.
`Lock_kinase_family` | If Yes, kinase family cannot be selected when running. Default is Yes.

The input data is the [UKA dataset](https://tercen.com/r/ebd643c3119c715cacdef627bb88a5a7)

This workflow has 1 operators:

* [Upstream Kinase Analysis Shiny Operator](https://github.com/tercen/upstream_kinase_analysis_shiny_operator)

This workflow has 1 view:
* Upstream Kinases Analysis

