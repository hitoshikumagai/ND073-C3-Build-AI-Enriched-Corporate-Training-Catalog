### Procedure

#### Built-in Skill
1. Modify your skillset definitions to add a built-in skill to enrich the data with descriptive information related to the entities listed in the MoodleInstructorProfiles.json file
2. Modify the index and indexer files to allow this enriched data to be used in queries

#### Custom Skill
1. First we need the credentials for the Springer API. This service is free and allows you to query the Springer API for information about articles in their database.
    * Visit the Springer API page (opens in a new tab)https://dev.springernature.com/(opens in a new tab) and sign up for credentials (For organization, you can just use "personal")
    * Once you are signed up and signed in, you can visit the "Applications" page and copy your credential for use in the next step
2. Next, you need to deploy the Azure Function:
    * From the GitHub starter code, open the "Function" folder in Visual Studio Code
    * Modify the SpringerLookup.cs file to include the API key you created in Step #1
    * Run the Function App by going to Run & Debug and running. This will restore packages and spin up the function locally. (See note below if you want to test this locally)
    * Function inputs and outputs
        * This Function App takes in a single data element named: "ArticleName"
        * The Function App will return the following data elements for each ArticleName:
            * PublicationName
            * Publisher
            * DOI
            * PublicationDate
3. Finally, modify your Azure Cognitive Search to use the Azure Function
    * Modify your skillset definition to add the custom skill to enrich the data by passing the document title to the function
    * Modify the index and indexer files to allow this enriched data to be used in queries

Once you are done with both of the above, make sure you use the Search Explorer interface to write query strings demonstrating the data elements from each of these skills.
