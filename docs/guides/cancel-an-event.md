# Cancel an event  

These steps are needed to properly cancel an event in Comers.  

### Deactivate the Arrangement  

This step prevents new bookings to be made in Comers.  

 - Go to `Product > Arrangements` and find your Arrangement.  
 - Set checkbox `Active` to unchecked in Channels.  

### Remove capacity for hotels  

The capacity for products in cancelled events needs to be removed to prevent conflicts when creating future events.  

_This step is tedious but there's no shortcuts._  

 - Remove capacity between `$DATE_FROM` and `$DATE_TO`, for each product in `$HOTELS`  


### Remove price for hotels  

The price for products in cancelled events needs to be removed to prevent conflicts with future events.  

 - Go to `Product > Products`  
 - Set `Name` to **TEMPLATE\_**  
 - Set checkbox `Show only active` to unchecked  
 - Click `Search`  
Remove price between `$DATE_FROM` and `$DATE_TO -1 day` with price type `$PRICE_TYPE`  

### Update COMERS OVERVIEW  

Set `STATUS` in COMERS OVERVIEW to `CANCELLED`  
