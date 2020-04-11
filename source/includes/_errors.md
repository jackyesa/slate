# Errors

<aside class="notice">
 Below are the error codes used throughout the Paystore API.
</aside>


Error Code | Meaning
---------- | -------
00	| Missing parameter - Signature key key required.
101	| Missing parameter - Retailer ID required.
102	| Missing parameter - Retailer user ID required.
103	| Missing parameter - Password required.
104	| Missing parameter - Location required.
105	| Malicious access - Exceeded maximum attempts allowed. Kindly contact paystore admin for assistance.
106	| Malicious access - Signature key not found.
107	| Malicious access - Invalid login.
108	| Invalid parameter - The A/C or User Id that enter is invalid. Please enter again.
109	| Malicious access - The A/C has been BLOCKED or SUSPENDED. Please consult PAYSTORE Administrator.
110	| Malicious access - You are not allowed to access using this IP address.
111	| Malicious access - Error Occur. Please consult PAYSTORE Administrators.
112	| Action required - First time login.
113	| Action required - Activate key code.
114	| Malicious access - Authentication failed.
115	| Malicious access - Token Invalid/Expired.
116	| Invalid parameter - Invalid token.
117	| Missing parameter - Token required.
118	| Retailer ID must be a string.
119	| Malicious access - Invalid Retailer ID.
120	| Invalid parameter - No product type found.
121	| Invalid parameter - No product category Found.
122	| Missing parameter - Item category ID required.
123	| Missing parameter - Item ID required.
124	| Missing parameter - Quantity required.
125	| Missing parameter - Please select minimum 1 item to purchase.
126	| Invalid parameter - Invalid item.
127	| Error - Insufficient stock.
128	| Malicious access - Order not found.
129	| Error - Current Balance Credit NOT enough for this purchase. Please consult your administrator to increase your credit limit.
130	| Unkown error. Unable to process order.
131	| Malicious access - You account is not autorized to access the api. Kindly contact Paystore admin for assistance.
132	| No Purchase history found.
133	| Invalid parameter - Kindly input correct date format. i.e: 1970-01-01.
134	| Invalid parameter - You may only request order history for 30 days.
135	| Invalid parameter - Kindly input correct location format: {latitude, longitude}
136	| Error - Zero credit.
137	| Error - No product found.
138	| Invalid parameter - Please provide a number for pagination.