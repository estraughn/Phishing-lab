# Phishing-lab

## Objective


The phishing lab focused on how to identify and analyze phishing attacks, emphasizing the detection of malicious emails, extracting indicators of compromise (IOCs), and applying countermeasures to prevent breaches.

### Skills Learned

-Identifying common phishing tactics, such as email spoofing and social engineering

-Analyzing phishing emails to extract key indicators of compromise (IOCs)

-Using email header analysis to detect suspicious activity

-Leveraging security tools to validate and mitigate phishing threats

-Recognizing red flags in URLs, attachments, and content within phishing messages

-Implementing best practices for phishing attack prevention and user awareness training

-Utilizing sandbox environments to safely analyze and examine phishing payloads



### Tools Used

- Sublime Text
- Thunderbird
- CyberChef


## Steps
1. Analyze the email header utilizng Sublime Text to determine the emails sender, domain, creation time and date, and other IOC

*Ref 1.1:![Screenshot 2025-01-25 114810](https://github.com/user-attachments/assets/daee7e2f-bfa2-4542-a5e0-727c4a70cf2b)

*Ref 1.2: ![Screenshot 2025-01-25 115042](https://github.com/user-attachments/assets/6457b9f6-e234-48a0-8af1-743ac92b2a71)

2. The next email that I analyzed I took a look at the contents of the body of the email for typical signs of phishing like grammer issues, mispelled words and attempts at social engineering. Then I did a more in depth analysis utilizing Sublime text. I then took the base64 text found in the body of the email and ran it through CyberChef to decode the text.

*Ref 2.1: ![Screenshot 2025-01-25 152756](https://github.com/user-attachments/assets/a40ff144-d9f6-4601-be4c-155f4df30f16)
*Ref 2.2: ![Screenshot 2025-01-25 153910](https://github.com/user-attachments/assets/07357d0d-420c-4642-8577-9eac267223e9)
*Ref 2.3:![Screenshot 2025-01-25 153959](https://github.com/user-attachments/assets/c247767e-fc32-490b-b788-b0a064028d0f)

