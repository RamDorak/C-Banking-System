# CPP-Banking-System
<h2>1. Gather User Inputs</h2>

1. User Details
Collect the following information from the user:

Name: Full name of the user.
Date of Birth (DOB): Input format: YYYY MM DD.
Address: Residential address of the user.
Unique ID: A government-issued ID or any unique identifier (e.g., PAN, Aadhaar).
2. Account Details
Gather details related to the new account:

Account Type: Specify either "Savings" or "Current".
Initial Deposit: Minimum required balance or custom deposit amount.
IFSC Code: Bank-specific identifier.
3. Authentication Details
Prompt the user to set a password:

Password: Ensure the password matches the hash value of the same stored.
Confirm Password: Re-enter to validate.

<h2>2. Validate User Inputs</h2>

1. Ensure Completeness
Verify all required fields are provided.

2. Password Validation
Check if the password meets complexity requirements (e.g., minimum length, special characters).
Confirm that the two password inputs match.

<h2>3. Generate Unique Account ID</h2>

1. Account ID Generation
Generate a unique identifier for the account.
Ensure the account ID does not conflict with existing accounts in the system.
Storage of Account ID

The ID will be used to link user details, account data, and password securely.
<h2>4. Store User Details</h2>

1. Create UserDetails Object
Use the UserDetails class to encapsulate user-specific information:
Name
DOB
Address
Unique ID
2. Store Object
The UserDetails object is included as part of the account data structure.

<h2>5. Store Account Details</h2>

Create Account Object
Instantiate an account object (SavingsAccount or CurrentAccount).
Provide necessary parameters, such as:
Account ID
UserDetails object
IFSC code
Account type
Initial balance
5. Add to System Storage
Store the account object in a vector or map within the BankSystem class.

<h2>6. Store Password Securely</h2>

1. Password Hashing
Use the hashPass method in the PassStore class to hash the plaintext password.
2. Link Password with Account
Store the hashed password in the passMan unordered map using the account ID as the key:
passStore.addPassword(accountID, hashedPassword);
