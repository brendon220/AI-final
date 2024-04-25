def is_spam(email_content, spam_keywords):
    """
    Determine if an email is spam based on the presence of spam keywords.

    Args:
    email_content (str): The text of the email to analyze.
    spam_keywords (list): A list of words commonly found in spam emails.

    Returns:
    bool: True if the email is spam, False otherwise.
    """
    # Convert the email content to lower case for case insensitive matching
    email_content = email_content.lower()

    # Check if any spam keywords are in the email content
    for keyword in spam_keywords:
        if keyword in email_content:
            return True
    return False

# Example usage
spam_keywords = ['win', 'free', 'winner', 'prize', 'money', 'offer', 'credit', 'cheap', 'claim', 'redeem']
emails = [
    "Congratulations! You've won a prize! Click here to claim.",
    "Here is a reciept for your recent purchase.",
    "Redeem this limited time offer for a 50% discount at apple",
    "Thank you for subscribing to youtubetv, We hope you enjoy!",
    "You have a free Iphone 15! click here to redeem"
]

# Filter emails
filtered_emails = {'spam': [], 'regular': []}
for email in
 emails:
    if is_spam(email, spam_keywords):
        filtered_emails['spam'].append(email)
    else:
        filtered_emails['regular'].append(email)

# Print categorized emails
print("Spam Emails:")
for spam in filtered_emails['spam']:
    print(f"- {spam}")

print("\nRegular Emails:")
for regular in filtered_emails['regular']:
    print(f"- {regular}")


