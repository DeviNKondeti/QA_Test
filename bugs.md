# Bug Reports

## Bug 1: Missing Email 
- **Description**: Contact form accepts with no email
- **Steps to Reproduce**:
  1. Go to any profile page
  2. Click "Save Contact"
  3. Enter Name: `d kondeti`
  4. Enter Number: `9963641577` 
  4. Submit form
- **Expected**: Form should reject with "Add Email" error
- **Actual**: Form accepts submission
- **Severity**: Medium (could lead to bad data collection)
- **Screenshot**: ![alt text](<Screenshot (40)-1.png>)


## Bug 2: Phone Number Accepts Too Many Digits
- **Description**: Contact form accepts more than 15 digits in phone number field
- **Steps to Reproduce**:
  1. Go to any profile page
  2. Click "Save Contact"
  3. Enter Name: `John doe`
  4. Enter Phone: `889900000090000` 
  5. Submit form
- **Expected**: Form should reject with "Phone number too long" error
- **Actual**: Form accepts submission
- **Severity**: Medium (could cause failed communications)
- **Screenshot**: ![alt text](<Screenshot (46).png>)



## Observation: No Critical Bugs Detected  
- **Tested Flows**:  
  - Profile loading (10+ profiles, various network conditions)  
  - Contact form validation (invalid emails, empty submits)    
- **Suggestions**:  
  - Add form submission progress indicators  
  - Trim whitespace from contact fields automatically  