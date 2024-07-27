# Email-Validation-in-python
Here's the code you provided in a more formatted way for readability. This code takes an email address as input and checks if it is valid based on several criteria.

```python
email = input("Enter your Email: ")
k, j, d = 0, 0, 0

if len(email) >= 6:
    if email[0].isalpha():
        if "@" in email and email.count("@") == 1:
            if email[-4] == "." or email[-3] == ".":
                for i in email:
                    if i.isspace():
                        k = 1
                    elif i.isalpha():
                        if i.isupper():
                            j = 1
                    elif i.isdigit():
                        continue
                    elif i in ["@", "_", "."]:
                        continue
                    else:
                        d = 1
                if j == 1 or k == 1 or d == 1:
                    print("Invalid Email")
                else:
                    print("Valid Email")
            else:
                print("Invalid Email")
        else:
            print("Invalid Email")
    else:
        print("Wrong email")
else:
    print("Email should be at least 6 characters long")
```

Here's a README file describing this script:

---

# Email Validation Script

## Description

This Python script validates an email address based on the following criteria:

1. The email address must be at least 6 characters long.
2. The first character must be a letter.
3. The email must contain exactly one "@" character.
4. The email must end with a dot followed by 2-4 characters (e.g., ".com" or ".co").
5. The email must not contain any spaces.
6. The email must not contain any uppercase letters.
7. The email must only contain letters, digits, "@" (one occurrence), "_" or ".".

## Usage

To run the script, you need to have Python installed on your machine. You can run the script by executing the following command in your terminal or command prompt:

```sh
python email_validation.py
```

When prompted, enter the email address you want to validate.

## Example

```
Enter your Email: example@domain.com
Valid Email
```

## Error Messages

- **Invalid Email**: The email does not meet one or more of the criteria listed above.
- **Wrong email**: The email's first character is not a letter.
- **Email should be at least 6 characters long**: The email is too short.

## Author

This script was created to demonstrate basic email validation logic in Python.

---

Save the above text into a file named `README.md` in the same directory as your script.