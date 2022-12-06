## LOGIN FUNCTION

Test Suite
|Test Case| Desc | Steps |
|---------|------|-------|

|TC-1| Login with correct credentials | type username as "username" and password  as "password". Press login. Verify on homepage for username that is successfully logged in | 

|TC-2| Login with incorrect credentials | type username as "wrongname" and password  as "wrongpassword". Press login. Verify message says "LOGIN FAILED" |
|TC-3| Login with incorrect credentials | type username as "username" and password  as "wrongpassword". Press login. Verify message says "LOGIN FAILED" |
|TC-4| Login with incorrect credentials | type username as "name" and password  as "password". Press login. Verify message says "LOGIN FAILED" |



Defect Report
|Defect | Desc | Severity | Priority | Steps to reproduce |
|-------|------|----------|----------|--------------------|

|DEF1   | For TC-2, error message says "wrong password" | low | low | login with wrong username and password
|DEF2   | For TC-3, error message says "wrong username", when the password was incorrect | low| low | login with correct username and wrong password|
|DEF3   | For TC-4, error message says "wrong password", when the username was incorrect | low | low | login with wrong username and correct password|

Requirements Traceability Matrix
|Requirement| Test Cases | Status | Defects |
|-----------|------------|--------|---------|
|Users should see a generic message saying login has failed if they provide the wrong credentials | TC-2, TC-3, TC-4 | TC-1 PASS, TC-2 FAIL, TC3-FAIL, TC4-FAIL | DEF1, DEF2, DEF3 |



## SIGNUP-NEGATIVE
Test Suite
|Test Case| Desc | Steps |
|---------|------|-------|

|TC-1| SIGNUP w/ correct parameters (6-10 characters long, has lower case, has upper case, has #) | type username as "Username1" and password  as "Password1". Press Sign-up and get a "Success Message"  |

|TC-2| SIGNUP a user twice and see if it is prevented or not | type username as "Username1" and password  as "Password1", repeat to see if it is allowed. Press Sign-up and see if you are prevented from registering a user twice. 

|TC-3| SIGNUP w/ incorrect parameters (less than 6 characters) | type username as "User5" and password  as "Password1". Press Sign-up and see if an error message is produced  |
|TC-4| SIGNUP w/ incorrect parameters (less than 6 characters) | type username as "Username1" and password  as "Pass". Press Sign-up and see if an error message is produced  |

|TC-5| SIGNUP w/ incorrect parameters (more than 10 characters) | type username as "UsernameOVER10" and password  as "Password1". Press Sign-up and see if an error message is produced  |
|TC-6| SIGNUP w/ incorrect parameters (more than 10 characters) | type username as "Username1" and password  as "PasswordOVER10". Press Sign-up and see if an error message is produced  |

|TC-7| SIGNUP w/ incorrect parameters (no lower case) | type username as "USERNAME1" and password  as "Password1". Press Sign-up and see if an error message is produced  |
|TC-8| SIGNUP w/ incorrect parameters (no lower case) | type username as "Username1" and password  as "PASSWORD1". Press Sign-up and see if an error message is produced  |

|TC-9| SIGNUP w/ incorrect parameters (no uppercase) | type username as "username1" and password  as "Password1". Press Sign-up and see if an error message is produced  |
|TC-10| SIGNUP w/ incorrect parameters (no uppercase) | type username as "Username1" and password  as "password1". Press Sign-up and see if an error message is produced  |

|TC-11| SIGNUP w/ incorrect parameters (no #'s) | type username as "Username" and password  as "Password1". Press Sign-up and see if an error message is produced  |


Defect Report
|Defect | Desc | Severity | Priority | Steps to reproduce |
|-------|------|----------|----------|--------------------|

|DEF1   | For TC-2, you can re-register the same user more than once | Medium | Medium | login with the same correct username and password twice


Requirements Traceability Matrix
|Requirement| Test Cases | Status | Defects |
|-----------|------------|--------|---------|
|Users should see a generic message saying login has failed if they provide the wrong credentials | TC-1, TC-2, TC-3, TC-4, TC-5, TC-6, TC-7, TC-8, TC-9, TC-10, TC-11 | TC-1 PASS, TC-2 FAIL, TC-3 PASS, TC-4 PASS, TC-5 PASS, TC-6 PASS, TC-7 PASS, TC-8 PASS, TC-9 PASS, TC-10 PASS, TC-11 PASS | DEF1 |

