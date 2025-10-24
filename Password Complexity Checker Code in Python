#PasswordComplexityChecker
import re

def check_password_strength(password):
    score = 0
    feedback = []

    if len(password) < 8:
        feedback.append("Weak: Password must be at least 8 characters long.")
    else:
        score += 1

    if re.search(r"[A-Z]", password):
        score += 1
    else:
        feedback.append("Weak: Password must have at least one uppercase letter.")

    if re.search(r"[a-z]", password):
        score += 1
    else:
        feedback.append("Weak: Password must have at least one lowercase letter.")

    if re.search(r"[0-9]", password):
        score += 1
    else:
        feedback.append("Weak: Password must have at least one number.")

    if re.search(r"[!@#$%^&*(),.?\":{}|<>]", password):
        score += 1
    else:
        feedback.append("Weak: Password must have at least one special character.")

    if score == 5:
        return "Strong: Password is strong!"
    else:
        return "\n".join(feedback) + f"\nScore: {score}/5. Improve your password!"

def main():
    print("Welcome to the Password Strength Checker!")
    print("Enter a password to check its strength. Type 'exit' to quit.")
    
    while True:
        user_password = input("Enter a password to check: ")
        if user_password.lower() == 'exit':
            print("Goodbye!")
            break
        print(check_password_strength(user_password))

if __name__ == "__main__":
    main()
