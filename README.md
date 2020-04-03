-Assignment 5

Used map function, custom function, dateTime function, String function, variable

1) Endpoint -> Post: http://localhost:8081/api/transform
Reuest data -

<data>
    <Employee>
        <Name>Seagull</Name>
        <Id>3674</Id>
        <Age>34</Age>
        <Salary>12000</Salary>
        <Address>28-H</Address>
        <DOJ>2018/12/09</DOJ>
        <City>Noida</City>
        <State>Utter Pradesh</State>
        <Zip>201306</Zip>
    </Employee>
    <Employee>
        <Name>Robin</Name>
        <Id>3675</Id>
        <Age>25</Age>
        <Salary>13000</Salary>
        <Address>20-P</Address>
        <DOJ>2014/01/03</DOJ>
        <City>Delhi</City>
        <State>Delhi</State>
        <Zip>110087</Zip>
    </Employee>
    <Employee>
        <Name>Crow</Name>
        <Id>3676</Id>
        <Age>28</Age>
        <Salary>11000</Salary>
        <Address>Sector 21</Address>
        <DOJ>2015/10/31</DOJ>
        <City>Gurugram</City>
        <State>Haryana</State>
        <Zip>301303</Zip>
    </Employee>
</data>



Response Data -

{
  "data": {
    "Employee": {
      "Name": "Seagull",
      "Age": "34",
      "City": "Noida",
      "State": "Utter Pradesh",
      "Zip": "201306"
    },
    "Employee": {
      "Name": "Robin",
      "Age": "25",
      "City": "Delhi",
      "State": "Delhi",
      "Zip": "110087"
    },
    "Employee": {
      "Name": "Crow",
      "Age": "28",
      "City": "Gurugram",
      "State": "Haryana",
      "Zip": "301303"
    }
  }
}




- CSV input file Data
2) Endpoint -> POST: http://localhost:8081/api/csvdata 
Request -

Name,Id,Age,Salary,Address,BOJ,City,State,Zip
Seagull,3674,34,12000,28-H,12/9/2018,Noida,Utter Pradesh,201306
Robin,3675,25,13000,20-P,1/3/2014,Delhi,Delhi,110087
Crow,3676,28,11000,Sector 21,31/10/2015,Gurugram,Haryana,301303

Response in Json Format -

[
  {
    "Name": "Seagull",
    "Id": "3674",
    "Age": "34",
    "Salary": "12000",
    "Address": "28-H",
    "BOJ": "12/9/2018",
    "City": "Noida",
    "State": "Utter Pradesh",
    "Zip": "201306"
  },
  {
    "Name": "Robin",
    "Id": "3675",
    "Age": "25",
    "Salary": "13000",
    "Address": "20-P",
    "BOJ": "1/3/2014",
    "City": "Delhi",
    "State": "Delhi",
    "Zip": "110087"
  },
  {
    "Name": "Crow",
    "Id": "3676",
    "Age": "28",
    "Salary": "11000",
    "Address": "Sector 21",
    "BOJ": "31/10/2015",
    "City": "Gurugram",
    "State": "Haryana",
    "Zip": "301303"
  }
]