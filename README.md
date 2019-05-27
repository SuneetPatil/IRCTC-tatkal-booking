# IRCTC Tatkal Ticket Booking:
This repository demonstrates how to book IRCTC Tatkal tickets with ease using powerful RPA tool - UiPath

## Brief background:
Currently booking a Tatkal ticket through IRCTC is a very tedious and time-consuming job. 
There are many challenges faced by a user, from server downtime or timeouts to poor network connectivity. 
Even after having logged in, it takes time to fill data, navigate through all the forms and make payment to complete the booking. 

As Lakhs of people try to book tickets every day, for a user to get confirmed tickets is no easy task as tickets are sold out in minutes. Many are forced to pay an exponential fare for premium tatkal.

Our solution template using RPA's UiPath is aimed at addressing this issue. We as a team of certified RPA's UiPath developers, aim to improve user’s experience by automating mundane but important tasks. Booking Tatkal tickets is as simple as filling a simple XLS file and our solution will take care of the rest!. 

**With this, life will just get easier for lakhs of people every single day who try to book their Tatkal tickets.**

## How it works:

Below is the work flow of our solution template using UiPath tool. 
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/architecture.png" width="70%" alt="alt architecture">
</p>

* User needs to update the passenger's travel details in XLS in advance. Below is the sample XLS for reference.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/DataExcel.png" height="40%" alt="alt sample_xls">
</p>

* At given time(ie 10am AC tickets and 11am for NON-AC tickets) our solution kick starts the process of IRCTC tatkal booking. It takes the Login details of IRCTC from Windows Credential manager of the local running system(Highly secure) and tries logging in. 
Login with OTP is an alternate way of logging into IRCTC other than regular login with Captcha. We read OTP from Gmail(Gmail login details are extracted from Windows Credential manager of the local running system). Below are the sample imgaes for reference. 
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/Login.png" height="30%" alt="alt login">

  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/otp.png" height="40%" width="50%" alt="alt otp" vertical-align="middle" >
</p>

* After successful login, our Solution takes travel details like source, destination, date of travel from XLS and autofills the IRCTC screen and searches from available trains.

* Once all the trains details are fetched, updates tatkal quota and then selects the train mentioned in the XLS and checks for seat availibility.

* Once seat available, fetchs passanger details from XLS and autofills the form as show below.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/passenger%20details.png" height="70%" width="90%" alt="alt passenger_details">
</p>

* Once all the details are filled and submits for review page.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/passenger_confirmation.png" width="60%" alt="alt passenger_confirmation">
</p>

* Once ticket is confirmed, it fetchs UPI details from XLS and takes to make payment using UPI. User will get the notification about the payment in his/her mobile and requests to make payment.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/UPI.png" height="70%" width="70%" alt="alt UPI">
</p>

* Actual request received in mobile device of the user and user needs to make payment.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/Payment.png" width="20%" alt="alt payment">
</p>

* Once payment is received, IRCTC will comfirm the booking and allocates the berth as shown in the image below. This ends the booking process.
<p align="center">
  <img src="https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/Images/ticket_confirmation.png" height="70%" width="70%" alt="alt ticket_confirmation">
</p>

### Prerequisites 
* should have [UiPath Community edition.](https://www.uipath.com/developers/community-edition-download) account
* Should have IRCTC and Gmail account
* IRCTC account should be linked to Gmail
* User should have UPI Id for payment

### How To Use This Code 
* Please [Clone](https://github.com/SuneetPatil/IRCTC-tatkal-booking/archive/master.zip) this repository to your local system.
* Update the Config.xlsx file (inside Data folder) with required travel and passenger details.
* Open and Run the Main.xaml file(in the root of the folder) in UiPath Studio.

### Built With 
* [UiPath Community edition.](https://www.uipath.com/developers/community-edition-download) - IDE used.

### Demo Video 
[IRCTC Tatkal Ticket Booking.](https://youtu.be/XWgZB64LXLs)

## RoadMap 
* Updating the user about booking confirmation using WhatsApp.

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/SuneetPatil/IRCTC-tatkal-booking/blob/master/LICENSE) file for details.

