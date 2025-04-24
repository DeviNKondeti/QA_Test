# Postman API Inspection Notes

## Endpoint: `POST /api/v2/contacts`
### Request Details
- **Method**: POST
- **URL**: `https://api.linqapp.com/api/v2/contacts`
- **Request Body**:
  {
    "full_name": "ky j",
    "phone_number": "+19999999999",
    "email": "kyj@mail.com",
    "title": "",
    "company": "",
    "location": "CA", #added the CA part in the postman
    "first_name": "ky",
    "last_name": "j"
  }

  ***Screenshot**: ![alt text](<Screenshot (47).png>)
                   


- ### Response Details

    Status: 200 OK

    Response Time: 192 ms

    Response Size: 1.89 KB

- ***Response Body***:
    {
    "contact": {
        "id": 2569379,
        "first_name": "ky",
        "last_name": "j",
        "phone_number": "+19999999999",
        "location": "CA",
        "email": "kyj@mail.com",
        "company": "",
        "title": "",
        "image_url": null
    }
    }
    ***Screenshot***: ![alt text](<Screenshot (49).png>)
    ***Screenshot***: ![alt text](<Screenshot (52).png>)

- ***Test Findings***:
    ## 1. Functional Observations
            1.1. Successful Creation
                Correctly generates unique ID (2569379)
                Returns all submitted fields in response

            1.2. Data Handling
                Accepts empty strings for optional fields (title, company)
                Preserves exact case for names ("ky" vs "Ky")

    ## 2. Validation Issues
            Test Case -> Result -> Severity
            Invalid email (kyj@mail) ->	Accepted ->	Medium
            Empty phone_number	-> Not tested	-> High
            300-char location	-> Not tested	-> Low


- ***Recommended Tests***: 

    1. [ ] Submit with SQL injection in `first_name`
    2. [ ] Test 50 concurrent requests
    3. [ ] Verify response with missing required fields