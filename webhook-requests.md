### Webhooks examples
##### Headers
Headers are common for all webhooks:

- ***X-Notification-Secret*** - notification key
- ***X-Notification-Delivery-Attempt*** - number of delivery attempts
- ***X-Notification-Type*** - type of notification (as described below)
- ***X-Notification-Id*** - internal notification ID
##### New transaction
X-Notification-Type - ***NewTransaction***
```
{  
   "buyer":{  
      "id":142694,
      "email":"test@example.com",
      "quantity":1,
      "sent_count":0,
      "created_at":"2018-12-29T20:29:23+01:00"
   },
   "listing":{  
      "id":36,
      "name":"GTA V STEAM KEY"
   },
   "database":{  
      "id":16141,
      "available_codes_count":7
   },
   "payment":{  
      "id":null,
      "code":null,
      "amount":null,
      "currency":null,
      "done":false
   },
   "created_at":"2018-12-29T20:29:23+01:00"
}
```
##### New payment for transaction
X-Notification-Type - ***NewPayment***
```
{  
   "buyer":{  
      "id":142697,
      "email":"test@example.com",
      "quantity":1,
      "sent_count":0,
      "created_at":"2018-12-29T20:32:31+01:00"
   },
   "listing":{  
      "id":36,
      "name":"GTA V STEAM KEY"
   },
   "database":{  
      "id":16141,
      "available_codes_count":0
   },
   "payment":{  
      "id":129288,
      "code":"PAYPAL_TEST",
      "amount":1,
      "currency":"PLN",
      "done":true
   },
   "created_at":"2018-12-29T20:32:31+01:00"
}
```
