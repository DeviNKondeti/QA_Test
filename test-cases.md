# Manual Test Cases

## TestCase-01: View Profile as Visitor
- **Description**: To verify visitors can view profile information without logging in
- **Steps**:
  1. Navigate to https://linqapp.com/welcome
  2. Click on any visible profile picture/name
- **Expected**: Profile details display without requiring login
- **Actual**: when clicked on any public customer such as McDonalds, it will not redirect to anywhere but stay on the home page.


## TestCase-02: Successful Signup with Valid Credentials
- **Description**: Verify Signup works with correct email and password (Signup)
- **Steps**:
  1. Navigate to login page
  2. Enter valid email: `dnkondeti@gmail.com`
  3. Click "Login"
- **Expected**: Successful login, redirect to dashboard
- **Actual**: Logged into the app, within seconds, automatically parsed the Name and Profile picture from the Gmail.
When a working email used, it redirects to the dashboard and the views first page giving the linq url as "https://linqapp.com/devi_kondeti?r=link"

While clicking on the URL, it directly takes to that users page and shows their details such as their role, company and where they are based.

- **Screenshot** : ![alt text](<Screenshot (30).png>)

## TC-2.2: Login with Malformed Email (Missing @,.,',')
- **Description**: Test email validation - missing @ symbol
            - **Steps**:
            1. Navigate to login page
            2. Enter invalid email: `devikgmail.com` (or) `devik@gmailcom` (or) `devik@gmail,com`
            3. Enter any password: `D1234`
            4. Click "Login"
            - **Expected**: Error message "Please enter a valid email address"
            - **Actual**: It didn't accept the malformed email
            - **Screenshot** : ![alt text](<Screenshot (33).png>)



## TC-2.3: Login with Unregistered Email
- **Description**: Test system response for unregistered accounts
            - **Steps**:
            1. Navigate to login page
            2. Enter dummy email: `nonexistent@prod.com`
            3. Enter dummy password: `Pass123`
            4. Click "Login"
            - **Expected**: Generic error message "Invalid credentials" 
            - **Actual**: Invalid Credentials, enter valid email and password


## TestCase-03: Save Valid Contact
- **Description**: Test saving contact with valid information
- **Steps**:
  1. Open a profile
  2. Click "Save Contact"
  3. Enter valid name and email
  4. Submit form
- **Expected**: Contact saves successfully with confirmation
- **Actual**: contact saved successfully and displays the contact name along with the details like Recent Activity, Tags and Notes
- **Screenshot**: ![alt text](<Screenshot (38).png>)