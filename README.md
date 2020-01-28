# Vehicle-Rental-System

## We start off with some stored users & passwords (in .txt file) ...
```
tcss305,305,true
henry,1234,true
athirai,1234,true
gary,3245,false
```

## We Can Register New Users:

Can register new users (checks that username is not already registered and that password meets criteria)...

```
Enter 1 or 2 (1. New Registration 2. Login):1
You entered option 1

******************************
 Enter Details
******************************
User Name:athirai
User already exists, enter different user name:myUser
Password:pass
Password Does not Comply:
  1) > 5 characters
  2) Must contain the character ('Z')
  3) Must contain an apostrophe (')
  4) Must contain the number 0
  5) Must be less than 10 characters
Enter Password:Z'0PASS
isVIP(true/false):true
Registration Successfull
```
Now this newly registered user is appended to the list of users in the text file....

```
myUser,Z'0PASS,true
```

## We can login
```
Enter 1 or 2 (1. New Registration 2. Login):2
You entered option 2

******************************
 Enter Details
******************************
User Name:myUser
Password:pass

Wrong Credentials
Enter User Name:UETH
Enter Passworduoeunth

Wrong Credentials
Enter User Name:myUser
Enter PasswordZ'0PASS
Login Successfull
Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
```

### We can browse available vehicles to rent (and their associated costs & features)

Shown in ascending cost per category (car, motor bike, bike).
```
Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
4
You entered option 4

********************************************
List of all vehicles by ascending cost:
Cost per Day: $30.00: Car (ID:1, Name:Fiat, VIN:V100, CanRent?:true, IsLuxury?:false, HasNavigation?:false, HasAssistance?:false)
Cost per Day: $41.00: Car (ID:2, Name:Outback, VIN:V101, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:false)
Cost per Day: $43.00: Car (ID:3, Name:BMW, VIN:V102, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:true)
Cost per Day: $20.00: MotorBike (ID:4, Name:Bike1, VIN:B100, CanRent?:true, IsTouring?:false)
Cost per Day: $25.00: MotorBike (ID:5, Name:Bike2, VIN:B101, CanRent?:true, IsTouring?:true)
Cost per Day: $10.00: Bicycle (ID:6, Name:Roadies, VIN:C100, CanRent?:true, CycleType:Road)
Cost per Day: $10.20: Bicycle (ID:7, Name:Cruiser, VIN:C101, CanRent?:true, CycleType:Cruiser)
Cost per Day: $10.10: Bicycle (ID:8, Name:Mountain, VIN:C102, CanRent?:true, CycleType:Mountain)
**********************
 Do you want to continue?Y
 ```
 
 ### We can rent one of the vehicles (changing canRent to false for the given vehicle).
 
 Furthermore, a bill is generate for the rental, which is output to the console, and to an external bill text file.
 ```
 Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
1
You entered option 1

********************************************
List of available vehicles:
Car (ID:1, Name:Fiat, VIN:V100, CanRent?:true, IsLuxury?:false, HasNavigation?:false, HasAssistance?:false)
Car (ID:2, Name:Outback, VIN:V101, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:false)
Car (ID:3, Name:BMW, VIN:V102, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:true)
MotorBike (ID:4, Name:Bike1, VIN:B100, CanRent?:true, IsTouring?:false)
MotorBike (ID:5, Name:Bike2, VIN:B101, CanRent?:true, IsTouring?:true)
Bicycle (ID:6, Name:Roadies, VIN:C100, CanRent?:true, CycleType:Road)
Bicycle (ID:7, Name:Cruiser, VIN:C101, CanRent?:true, CycleType:Cruiser)
Bicycle (ID:8, Name:Mountain, VIN:C102, CanRent?:true, CycleType:Mountain)
**********************
 Enter Rental Details
**********************
Enter Vehicle ID:3
Enter User Name:myUser
Enter NumDays to Rent:2

**********************
 Rental Bill Summary
**********************
User Name: myUser
----Vehicle Information----
VehicleName BMW
VehicleID 1
VehicleType V102
VIN V102
----Cost Information----
RentalPerDay: 
Cost per Day: $43.00
No.of Rental days: 2
Total Amount: $86.00
Insurance: $0.86
VIPDiscount: -$0.86
Tax: $8.60
Total Rent: $94.60
Rent Successfull
**********************
 Do you want to continue?Y
 ```
 
 ### Now that we have rented the BMW, we can see that we can no longer rent it (again) through the rent menu.
 
 Only vehicles that can be rented are shown (canRent = true).
 
 ```
 Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
1
You entered option 1

********************************************
List of available vehicles:
Car (ID:1, Name:Fiat, VIN:V100, CanRent?:true, IsLuxury?:false, HasNavigation?:false, HasAssistance?:false)
Car (ID:2, Name:Outback, VIN:V101, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:false)
MotorBike (ID:4, Name:Bike1, VIN:B100, CanRent?:true, IsTouring?:false)
MotorBike (ID:5, Name:Bike2, VIN:B101, CanRent?:true, IsTouring?:true)
Bicycle (ID:6, Name:Roadies, VIN:C100, CanRent?:true, CycleType:Road)
Bicycle (ID:7, Name:Cruiser, VIN:C101, CanRent?:true, CycleType:Cruiser)
Bicycle (ID:8, Name:Mountain, VIN:C102, CanRent?:true, CycleType:Mountain)
**********************
 Enter Rental Details
**********************
Enter Vehicle ID:
```
 
 ### Finally, we can drop off the vehicle, and quit the program
 ```
 Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
4
You entered option 4

********************************************
List of all vehicles by ascending cost:
Cost per Day: $30.00: Car (ID:1, Name:Fiat, VIN:V100, CanRent?:true, IsLuxury?:false, HasNavigation?:false, HasAssistance?:false)
Cost per Day: $41.00: Car (ID:2, Name:Outback, VIN:V101, CanRent?:true, IsLuxury?:true, HasNavigation?:true, HasAssistance?:false)
Cost per Day: $43.00: Car (ID:3, Name:BMW, VIN:V102, CanRent?:false, IsLuxury?:true, HasNavigation?:true, HasAssistance?:true)
Cost per Day: $20.00: MotorBike (ID:4, Name:Bike1, VIN:B100, CanRent?:true, IsTouring?:false)
Cost per Day: $25.00: MotorBike (ID:5, Name:Bike2, VIN:B101, CanRent?:true, IsTouring?:true)
Cost per Day: $10.00: Bicycle (ID:6, Name:Roadies, VIN:C100, CanRent?:true, CycleType:Road)
Cost per Day: $10.20: Bicycle (ID:7, Name:Cruiser, VIN:C101, CanRent?:true, CycleType:Cruiser)
Cost per Day: $10.10: Bicycle (ID:8, Name:Mountain, VIN:C102, CanRent?:true, CycleType:Mountain)
**********************
 Do you want to continue?2
Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
2
You entered option 2

********************************************
**********************
 Enter Drop-off Details
**********************
Enter Drop-off Vehicle ID:2
Vehicle is not rented already
Enter Drop-off Vehicle ID:3
Drop-off Successfull
**********************
 Do you want to continue?Y
Enter 1 or 2 or 3 or 4 (1. Rent 2. Drop-off 3.Exit 4.List Vehicles By Rental Cost):
3
You entered option 3

********************************************
```
