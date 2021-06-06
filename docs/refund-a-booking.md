# Cancel and refund booking  

_This guide contains a step-by-step instruction on how to make  
a refund of a booking in Comers with PayEx/SwedbankPay._  

!!! Warning  
> If original payment was made with Swish, stop here and consult Erik or Malin  

## Prerequisites  

Before you proceed make sure to have the necessary credentials  

- [**Comers**](https://adminang.comers.se)  
- [**PayEx** (older transactions)](https://secure.payex.com/Admin/Logon.aspx)  
- [**SwedbankPay** (newer transactions)](https://admin.payex.com/psp/login)  
- [**REFUND spreadsheet**](https://docs.google.com/spreadsheets/d/11JW8NCPnV5h49dYcMxpH6dfmC2V1dVvGJWCkPWrYnb4/edit#gid=0)  

## Overview  

- [Cancel booking in Comers](#cancel-the-booking)  
- [Refund via PayEx/SwedbankPay](#payexswedbankpay)  
- [Register the refund in Comers](#register-refund-manually)  
- [Contact customer](#contact-customer)  
- [Log the transaction in REFUND spreadsheet](#log-the-transaction)  

---  

## Detailed instruction  

### Comers  

_Make sure you're aware of any administration/cancellation fees according to the booking policies:_  
 - [Course/Retreat](https://www.angsbacka.com/about-angsbacka/course-retreat-booking-policy/)  
 - [Festivals](https://www.angsbacka.com/about-angsbacka/festival-ticket-policy/)  


#### Cancel the booking  

- Go to booking  
- Click button `Cancel` in the bottom of the page  
- Set `--- State reason for cancellation ---` to `According agreement` or `Free`. If cancellation fee apply use `According agreement`  
- Click button `Confirm Cancel`  
- Go to the **Payments** tab  
- In the section **Registrered payments**:  
    - Make note of the **Payment date** & the **Reference** number  

!!! Note  

> _We'll use the **Payment date** and **Reference** number to find the payment in PayEx/SwedbankPay_.  

**[⬆ Back to Top](#overview)**  

---  

### PayEx/SwedbankPay  

If **Payment date** is _earlier_ than 18.06.20 open [**PayEx**](https://secure.payex.com/Admin/Logon.aspx) otherwise use [**SwedbankPay**](https://admin.payex.com/psp/login). Please note that both PayEx and SwedbankPay currently shows the same PayEx logo.  

You'll need a _reason for refund._ When in doubt use _"Event cancellation"_ or something else that makes sense.  

#### Refund via PayEx  

- Click menu `Transaction search`  
- Set `Filter` to `Transaction number`  
- Set `Transaction number` to **Reference** number from previous step  
- Click button `Search`  
- Click link in column **Transaction number**  
- Copy the current url in your browser and store it for later  
- Click button `Credit` in the button of the page  
- Set `Partial credit?` to checked  
- Set `Amount` to equal **Outstanding amount to pay** without the minus(-) symbol  
- Set `Comment` to _reason for refund_  
- Click button `OK`  

!!! Note  

> "Transaction is credited" should show at the bottom of the page.  

**[⬆ Back to Top](#overview)**  

#### Refund via SwedbankPay  

- Click `Menu` > `Payments`  
- Input **Reference** in search field  
- Open the payment details  
- Copy the current url in your browser and store it for later  
- Click button `Reversal`  
- Set `AMOUNT TO REVERSE` to equal **Outstanding amount to pay** without the minus(-) symbol (_default_)  
- Set `Description` to _reason for refund_  
- Click `Reverse Payment`  

!!! Note  

> "Reversal completed successfully" should show on top of the page.  

**[⬆ Back to Top](#overview)**  

---  

### Comers  

_Refunds in PayEx/SwedbankPay is not automatically registered in Comers. We'll need to register the refund manually._  

#### Register refund manually  

- Go to the **Payments** tab  
  - In the section **Register payment manually**:  
      - Set `Amount` to **Remains to be paid** (_default_)  
      - Set `Way of payment` to same as original payment in **Registered payments**  
      - Set `Reference` to _reason for refund_  
      - Click button `Register payment`  
- Go to the **Booking cart** tab  
    - Click button `Create reciept` (if possible)  
    - Click button `Create itinerary` (if possible)  

**[⬆ Back to Top](#overview)**  

---  

#### Contact customer  

- Go to the **Contact** tab  
    - In the section **E-post**:  
        - Verify `Sender` makes sense.  
        - Set `--- Select a message on the customers language ---` to `Customer Cancellation & Refund`  
    - In the section **Attach files**:  
        - Make sure neccessary attachments are included, if any.  
    - Click button `Send` in section **E-post**  

!!! Note  

> The email templates might look different if booking contact language is Swedish.  

**[⬆ Back to Top](#overview)**  

---  

### Log the transaction  

_Final step is to log the transaction in a Spreadsheet._  

- Open [**REFUND**](https://docs.google.com/spreadsheets/d/11JW8NCPnV5h49dYcMxpH6dfmC2V1dVvGJWCkPWrYnb4/edit#gid=0) spreadsheet  
- Fill **all** columns on a new row.  

---  

### Celebrate  

**Congratulations!** You're truly a beautiful flower that brings joy to this world.  

_Now, let's do another one._  

**[⬆ Back to Top](#overview)**  

---  
