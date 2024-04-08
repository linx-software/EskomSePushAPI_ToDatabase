# EskomSePush API to Database

## Description
This solution shows how to interact with the EskomSePush API with Linx. The solution contains functions to interact with the API (a function for each endpoint) and then also how to write the schedule information into a database table (SQL Server).

## Usage
The solution has a collection of functions to interact with the API, and a single function to load the schedule (of a specific area) to a table. There is a table creation script for the table included in this solution. 

#### API interactivity
- GetStatus: Retrieve the current and next loadshedding statuses for South Africa and (Optional) municipal overrides
- AreaSearch: Search area based on text - Pass in an area search text as a parameter
- GetAreaInformation: Retreive details needed to monitor upcoming loadshedding events for the chosen suburb - pass in the Area ID retrieved from AreaSearch
- CheckAllowance: Check allowance allocated for token

#### Load schedule data to database
- WriteToDatabase: Get the area information for a specific area ID and write it to a database table. The solution was made for a MS SQL Database but can be modified to work with any other database - Pass in the Area ID

### Try it out
The table create script is included as Create Schedule Table Script.sql, create this table to load the schedule for an area with the WriteToDatabase function. 
Add your Database Connection string, and ESP Licence to the settings

### Use API Interactions it in your own Linx solution
Copy the relevant function along with its types folder to your solution and call it from anywhere.
Note that you will need to create a setting for the ESPLisence and ESPURI. 

### Notes
You need an EskomSePush API Subscription, obtain one from [this site](https://eskomsepush.gumroad.com/l/api)

## Contributing

For questions, please ask the [Linx community](https://linx/software/community)

## License

[MIT](https://github.com/linx-software/template-repo/blob/main/LICENSE.txt)
