***CURRENTLY IN DEVELOP MODE***


# autosuggest
Application which auto suggest/ auto correct when user types 

Train input data 
T1. {"text": " Iphone 5s in mumbai","filter":{"user":45432,"category":453,"location":34,"model":1}}
T2. {"text": "Samsung 10L automatic washing machine","filter":{"category":321,"location":34,"model":14}}
T3. {"text": " Iphone 6s in good condition","filter":{"user":342,"category":453,"location":12,"model":2}}

<b>Text</b> tag Basically used to create tree and <b>filter</b> tag is to filter query when searching.
1. Search Query with no user tag.

{"query":"Iphone","filter":{"location": 34 }}

Return  T1 only

2. Search Query with no location, no user

{"query":"Iphone","filter":{}}

Return T1 and T3

3. Search Query with user tag.

{"query":"Iphone","filter":{"user":45432}} [Here user tag is used to prioritize search done by user[45432] first and rest later.

Returns in with T1 coming first and T2 next.

3. Auto Correct text feature is also available

{"query":"Ephone","filter":{}}

Returns T1 and T2
