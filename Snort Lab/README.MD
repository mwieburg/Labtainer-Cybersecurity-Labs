# SEE snort.pdf lab manual for specific objective details for the solutions below


## 4.3 Write a simple bad rule

The alert for tcp traffic will issue an alert every time tcp traffic is detected on the network by Snort. This rule is not useful and is used to show how the Snort IDS works and the importance of writing affective rules

![snort_bad_rule](https://github.com/user-attachments/assets/b08f4b47-4c37-4cd3-a97e-f724f7f1f5ff)

![snort_bad_rule_traffic](https://github.com/user-attachments/assets/8611a39b-feb6-46eb-bfc7-21b8b5c6220a)


## 4.4 Custom rule for CONFIDENTIAL traffic
The snort rule for detecting the presence the word "CONFIDENTIAL" in the network traffic will raise an alert when sensitive information is shared:

## 4.7 Distingushing traffic by address

