# Multi-label-text-classification-using-supervised-learning
This is a template code for the research paper "Multi label text classification for un-trained data through supervised learning"; implements an efficient way to classify multi label texts - https://ieeexplore.ieee.org/document/8321804

<h2>Pre-Requisites</h2>
Please ensure the following before the setup - 

1. Insall PredictionIO framework and remember to choose HBase & ElasticSearch
2. Check pio status
3. Install this template


<h2>Overview</h2>

This classifier uses "lexions" to classify text of un-trained data.

System Architecture is as follows - 
1. Provide the engine with un-trained datasets
2. Sequencing using sets & lexion 
3. Boosting the weak learners into strong learners
4. Finally, decision trees are used to get final results. 

<h3> Import Sample Data </h3>

A. Create a new app with name, appName in engine.json

B. Run PredictionIO app new [app-name]

C. Import all events by running command -> pio import ==appid *app-ID* --input **eventfile.json** where it will show you the pio app list

D. Peform pio build, pio train and pio deploy

E. Execute sample queries run curl -H "Content-Type: application/json" -d '{"text": "My boy is growing up", "locale" : "EN" http://localhost:8000/queries.json

<h3> Usage </h3>

**Event data requirements**

**Event Training Data**
 1. eventTime : String
    2. entityId: GUID
    3. event : String
    4  properties
        * Query: String,
        * Category: String,
        * Locale: String
    5. entityType: String

<h2> Conclusion </h2>



