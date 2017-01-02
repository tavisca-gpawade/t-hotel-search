# t-hotel-search Specification

```html
<script>

	var searchOptions = {
		traveller:{
			minAdultCount : 1,
			maxAdultCount : 6,
			minChildCount : 0,
			maxChildCount : 6,
			totalRoomPaxCount : 9,
			minChildAge : 0,
			maxChildAge : 12,
			defaultAdultCount : 2,
			defaultChildCount :0,

			defaultSelectOption : [
				{ 
					room : 1,
					adult : 1
				},
				{ 
					room : 1,
					adult : 2
				},
				{ 
					room : 1,
					adult : 2,
					child : 1
				}
			]
		},
		multiRoomEnable : true,
		maxRoomCount : 4,
		date : {

			// check-in allowed from current date. Value 0 means same day seach allowed.
			checkInAllowFromNow : 0,

			// Duration between check-in and check-out date
			maxDuration : 30,

			//default checkout date if check-in date is selected
			defaultStayDuration : 1,

			format : "mm/dd/yyyy"
		}

	}

	var resources = {
		labels : {
			adult : 'Adult',
			children : 'Children',
			child : 'Child',
			age : 'Age',
			room : "Room"
		},
		watermark : {
			checkIn : "MM/DD/YYYY",
			checkOut : "MM/DD/YYYY",
			hotelLocation : "City, Airport, Address or Point of Interest"
		}
	}

	var searchModel = {
		"destination": {
			"id": 1235,
			"name": "Las Vegas, NV, US",
			"geoCode": "36.23305,-115.2423",
			"type": "City",
			"code": "LAS",
			"formattedAddress": "Las Vegas, NV, US"
		},
		"checkInDate": {
			"date": "01/10/2017",
		},
		"checkOutDate": {
			"date": "01/15/2017",
		},
		"rooms": [
			{
				"adults": {
					"quantity": 1,
					"type": "Adult",
					"ages": [
						25
					]
				},
				"children": {
					"quantity": 1,
					"ages": [
						2
					],
					"type": "Child"
				}
			}
		],
				
		"type": "Hotel"
	}


</script>



<t-search 
		options={{searchOption}} 
		resources={{resources}} 
		init-model={{searchModel}} 
		on-do-search="{{doSearch}}"
		lang="en">
</t-search>

```
