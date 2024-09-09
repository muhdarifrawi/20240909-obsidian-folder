# Info
This consists of all models that can be found in the backend that are then stored into the database. Database in use as of writing is MongoDB.

# Database and Collection
Database name is `comma`. 

Database are sorted into the following `collections`:
- blacklists
- users
- items
- shops
- admins
- ethnicity
- profile type

# Models
## Users model
```JSON
{
	"username":"",
	"email":"",
	"password":"",
	"ethnicity":"",
	"profileType":""
}
```

**profileType** (string) :

This shows the type of profile the user has. 

The list of profile type is as follows:
- Free - can view items and shops but not adding, updating or deleting.
- Paid - can view, add, update and delete.
- Admin - can view, add, update and delete. Plus admin roles. 
## Sample Users
```JSON
{
	"username": "tester_1",
	"email": "tester_1@asd.com",
	"password": hashedpasswordshouldbeseenhere,
	"ethnicity": "chinese",
	"profileType": "Free"
}
```
## Shops model
```JSON
{
	"shopName":"",
	"location":"",
	"address":"",
	"description":"",
	"operatingHours":"",
	"holidaysObserved":""
}
```

**location (string)** : denotes the lat, long of the shop location.

**operatingHours** (array) : denotes the operating hours known. Monday starts on index 0.

Days are as follows:
- Monday: index 0
- Tuesday: index 1
- Wednesday: index 2
- Thursday: index 3
- Friday: index 4
- Saturday: index 5
- Sunday: index 6
- Public Holiday: index 7

Strings should be inserted into the array and the time format should be in `hh:mmAM/PM` format. Example: `06:00PM` 

**holidaysObserved** (array):
Indicates the holidays that the shop may observe. Strings should be inserted into the array.
## Sample Shops

```JSON
{
	"shopName":"the best shop",
	"location":"1.35,103.81",
	"address":"1 tampines central 1, singapore 529539",
	"description":"best shop you have ever seen!",
	"operatingHours":[
		"10:00AM to 08:00PM",
		"10:00AM to 08:00PM",
		"10:00AM to 08:00PM",
		"10:00AM to 08:00PM",
		"10:00AM to 09:00PM",
		"10:00AM to 10:00PM",
		"10:00AM to 10:00PM",
		"10:00AM to 10:00PM"	
	],
	"holidaysObserved":[
		"new years",
		"chinese new year"
	]
}
```

## Items model
```JSON
{
	"itemName":"",
	"itemCost":"",
	"barcodeNumber":"",
	"category":"",
	"restrictionType":"",
	"sellingQty":"",
	"onSale":"",
	"knownSalesHour":"",
	"availability":""
}
```

**itemName** (string) :
Information on item name.

**itemCost** (string) :
Information on price of item.

**barcodeNumber** (string) :

**category** (string) :
This lets user know if the item is a food items or non-food items. Do take note that there are non-food items that also have a `restrictionType` .

**restrictionType** (string) :
This lets user know the `restrictionType` the item is. 

The known `restrictionType` are as follows:
- generic (default value, no dietary restriction)
- halal (must have the halal logo or certification)
- kosher
- vegan
- vegetarian

**sellingQty** (string) :
Indicates how the item is being sold as. Will require a sample picture of the types of packaging.

The known `sellingQty` is as such:
- bags
- cartons
- packets
- weight

**onSale** (boolean) : 
Indicates if item is currently on sale. Value is `true` or `false`. Default value is `false`.

**knownSalesHour** (object) :
Any known sales hour will be placed in here as an object. 
Example:
```JSON
{
	"known0": ["10:00AM", "12:00PM"],
	"known1": ["04:00PM", "06:00PM"]
	... 
}
```

**availability** (boolean) :
Information on currently availability of item. Default value is `true`. `true` indicates item is available in shop.