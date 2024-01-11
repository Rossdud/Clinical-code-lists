# Clinical-code-lists
Validated clinical code lists for CPRD Aurum 

Bespoke clinical code lists generated to identify all relavent medcodeid codes within CPRD Aurum.  All other codes used within study are referenced in published papers.

All code lists clinically validated

**Bespoke clinical code list development approach** 

There is no standardised approach to developing clinical code lists.  However, after extensive discussions with other researchers who work in this area and searching for relevant literature, the following approach was adapted.  Using the CPRD medical term dictionary which maps all terms entered into the EMIS systems to unique CPRD specific medical code, a systematic search of relevant clinical terms was conducted.  This included selection of suitable terms of relevance to the condition/factor the code list was being generated for (e.g. Alzheimer’s; dementia etc) and selection of any exclusion terms which would otherwise return a large number of unwanted terms (e.g. family history).   Specifics of each code list developed varied slightly and was an iterative process of addition of exclusion terms to ensure the search of the CPRD medial term dictionary was as specific as possible, while also ensure that all potentially relevant terms were included.  The systematic approach employed in this study to generate bespoke clinical code lists followed three stages as described below.

Step 1 – automated search of relavent terms

First, the selection of inclusion and exclusion terms are defined which are then used when searching the CPRD Aurum dictionary in Stata.  Inclusion terms should be any word/series of words which are of relevance to the condition/factor of interest.  For example, inclusion terms for factor living arrangement may include “living alone, cohabitation, homeless, accommodation” etc.  Exclusion terms should be selected to help limit search results that are not of relavence to the condition/factor.  For example. Again for living arrangement, exclusion terms may be “stand tibia fibula aortic revision rvsn reaction test” etc.  Choosing exclusion terms is an iterative process and guided by the results of the search of inclusion terms.  This may involve scanning the search results of terms returned to identify terms witch may not be relevant, then going back to add any additional exclusion terms identified.  This can reduce the number of potentially relevant terms identified significantly.  To check for that the resultant number of terms is roughly in the right region, clinical code lists from other databases were inspected for total number of included terms.  Comparing the number of total included terms provided a level of confidence that the automatic process of code development was adequate before full validation by clinician. 

Step 2 – manual inspection

The next step is to manually inspect the returned clinical terms and make a judgment on their inclusion or exclusion.  This is required in addition to the automatic exclusion process as some included terms may still not be of relevance to the specific condition/factor of interest.  For example, the returned search terms for the condition depression included a large number of other clinical terms which included the word “depression” in it, like “depression in the skull” which is not of relevance to the mental disorder.  In addition, where a condition/factor was to be categorised, manual inspection and indicating which category each included term was to be assigned was also undertaken.  For example, eFI score is recorded directly into primary care records, and therefore, these can be obtained directly from CPRD data.  However, this needed to be categorised into mildly frail, moderately frail, and severely frail categories.  It is within tis manual step that this categorisation is carried out.  The manual inspection (and categorisation) was carried out by two individuals (RT and DO) independently.

Step 3 – clinical validation

Upon completion of manual inspection of the initial code lists (indicating what codes will be included, and where appropriate categorised, and which will be further excluded), these were then shared with a clinician for clinical validation.  The clinician reviewed the lists and indicated weather or not each term should be included or excluded.  Where differences occurred between the clinical expert and the initial assessment in step 2, the clinician provided rational for exclusion and the clinical judgment was accepted.  The final validated clinical code list was then generated and saved as .txt file format.

**Prescribed medication code list generation**

Generating code lists for prescribed medications require a slightly different approach to that of medical conditions or other personal information as described above.  Rather than using the Aurum Medical Term Dictionary, the EMIS Product Dictionary was used.  Within this, every prescribed drug, dosage and formulation is coded to a unique CPRD product code (prodcodid) which is the equivalent of the medcodeid for conditions.  In addition, because the drug substances to be included in this study were broad drug categories based on British National Formula (BNF) chapter, a slightly altered approach was required.

Step 1 – initial search

A search of the EMIS Product dictionary was conducted using BNF chapter numbers only of the relevant drug class (e.g. 2050501, 2050502 and 2050503 for ACE-inhibitors).  This returned only drugs which matched the relevant BNF chapters.  However, not all drugs within the dictionary have a corresponding BNF chapter recorded.  

Step 2 – refinement of search criteria

Therefore, to increase the sensitivity of the search, a second search was carried out using the BNF chapter again, but also including a range of chemical substances associated with the relevant BNF chapter.  For example, for ACE-inhibitors this included aliskiren azilsartan medoxomil amongst other chemical terms.  This search would return a number of other potentially relevant terms.  

Step 3 – manual inspection

As with the condition/factor clinical code lists the next step involved manual inspection of the potential drug product terms/BNF chapters returned by the automated aspect of the search described in steps 1 and 2.  Here  the returned detail was vissually inspected and a judgment on inclusion or exclusion was made. 

Step 4 – clinical validation

The final list of potential drug product code lists was shared with a clinician who specialises in clinical therapeutics to validate.  Where differences occurred between the clinical expert and the initial assessment in step 2, the clinician provided rational for exclusion and the clinical judgment was accepted.  The final validated clinical code list was then generated and saved as .txt file format.

