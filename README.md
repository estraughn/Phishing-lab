# Phishing-lab

## Objective


The phishing lab focused on how to identify and analyze phishing attacks, emphasizing the detection of malicious emails, extracting indicators of compromise (IOCs), and applying countermeasures to prevent breaches.

### Skills Learned

- Identifying common phishing tactics, such as email spoofing and social engineering

- Analyzing phishing emails to extract key indicators of compromise (IOCs)

- Using email header analysis to detect suspicious activity

- Leveraging security tools to validate and mitigate phishing threats

- Recognizing red flags in URLs, attachments, and content within phishing messages

- Implementing best practices for phishing attack prevention and user awareness training

- Utilizing sandbox environments to safely analyze and examine phishing payloads



### Tools Used

- Sublime Text
- Thunderbird
- CyberChef
- PhishTank
- URL2PNG
- urlscan.io
- Virus Total
- Hybrid Analysis


## Steps
1. I Analyzed the email header utilizng Sublime Text to determine the emails sender, domain, creation time and date, and other IOC.

*Ref 1.1:![Screenshot 2025-01-25 114810](https://github.com/user-attachments/assets/daee7e2f-bfa2-4542-a5e0-727c4a70cf2b)

*Ref 1.2: ![Screenshot 2025-01-25 115042](https://github.com/user-attachments/assets/6457b9f6-e234-48a0-8af1-743ac92b2a71)

2. The next email that I analyzed, I took a look at the contents of the body of the email for typical signs of phishing like grammer issues, mispelled words and attempts at social engineering. Then I did a more in depth analysis utilizing Sublime text. I then took the base64 text found in the body of the email and ran it through CyberChef to decode the text.

*Ref 2.1: ![Screenshot 2025-01-25 152756](https://github.com/user-attachments/assets/a40ff144-d9f6-4601-be4c-155f4df30f16)

*Ref 2.2: ![Screenshot 2025-01-25 153910](https://github.com/user-attachments/assets/07357d0d-420c-4642-8577-9eac267223e9)

*Ref 2.3:![Screenshot 2025-01-25 153959](https://github.com/user-attachments/assets/c247767e-fc32-490b-b788-b0a064028d0f)

3. My next step is to analyze any URLs that are present within the emails for example the link in Ref 1.1. Again I will take a look at the body of the email in Sublime text and find the associated URL. I then took the associated email as a .eml file and place it into CyberChef to decode, defang, and extract URLs. I then took the decoded URL and checked it with PhishTank to see if it is already a known malicious domain. I also ran the URL through URL2PNG to see what the image of the malicious URL website looks like and compared it to the site being spoofed. Next I went to urlscan.io to run the URL through a sandboxed environment to see how the malicious link behaves when activated.

*Ref 3.1: ![Screenshot 2025-01-25 163016](https://github.com/user-attachments/assets/cb1e8b71-24ad-4dc3-8198-6522a8ddcb1c)

*Ref 3.2: ![Screenshot 2025-01-25 163438](https://github.com/user-attachments/assets/8f54e8fe-cabd-4a37-84b9-faa45a5b4a79)

*Ref 3.3:![Screenshot 2025-01-25 165414](https://github.com/user-attachments/assets/6b311902-ca44-454a-9137-555608bac21d)

*Ref 3.4: ![Screenshot 2025-01-25 165343](https://github.com/user-attachments/assets/7a3272cc-bcf2-4a24-b52a-3c7d2fbea659)

*Ref 3.5: ![Screenshot 2025-01-25 165700](https://github.com/user-attachments/assets/62c8d79c-421a-48ee-9dd6-5a4d0cfbeb85)

4. On a another sample email I was able to analyze a malicious attachment by first saving the attachment to a designated file on my ubuntu VM for analysis. I then opened the terminal and ran the command sha256sum, sha1sum, and md5sum followed by the  file name quotation[.]iso to obtain the hash values of the email attachment. I then ran the SHA256 hash through Virus Total to find out if these are known malicious hashes. I then took the malicious file and ran it through the Hybrid Analysis sandbox environement to see how the malware behaves when activated and obtain a malware analysis report. I then took the associated CVE from the malware analysis report and looked it up on cve.mitre.org to find out the malwares attack chain.

*Ref 4.1:![Screenshot 2025-01-25 171058](https://github.com/user-attachments/assets/29613146-d6d7-4857-9a0a-0869d7691de1)

*Ref 4.2:![Screenshot 2025-01-25 172248](https://github.com/user-attachments/assets/c8536172-1500-462d-96a6-e518920094b4)

*Ref 4.3:![Screenshot 2025-01-25 174022](https://github.com/user-attachments/assets/712edb6a-83d7-4c4a-b317-bd78465f4442)

5. The next steps after the analysis is complete is to begin conducting reactive phishing defense which consists of the following:

   -containment of the sender, web, and file artifacts related to the email as well as quarantining any affected systems

   -eradication of the maliciouious emails and files as well as changing any compromised credentials

   -recovery from clean backups of the compromised systems

   -communicate the situation to affected users and stakeholders

   -Lastly is end user education to help aid in the prevention of future incidents

6. Here are also some steps that can be taken to bolster proactive phishing defense:

   -implementing email filtering applications and mark external emails

   -admininster URL scanning and blocking

   -attachment filtering to block certain file extensions as well as using attachment sandboxing


