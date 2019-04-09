# AppropriateFacility
It is an api to locate the appropriate facilities: 
Firstly, I use a customer’s ID to query data in mysql. If the customer has a preference, it is returned.
Then check the postal code in mysql. If I can find a facility locate in the specified zipcode, then return it. If I can’t find it, then try to find the closest one. 
For this part, I use API in http://www.zipcodeapi.com/ . The API helps me to find all zip codes within a given radius of a zip code. So there’s a loop to increase radius until I can find a zipcode which facilities locate in. This loop has MAX_TRY_TIMES setting to avoid overtime proceeding.
