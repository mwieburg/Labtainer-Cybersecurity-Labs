# SEE snort.pdf lab manual for specific objective details for the solutions below


## 4.3 Write a simple bad rule

The alert for tcp traffic will issue an alert every time tcp traffic is detected on the network by Snort. This rule is not useful and is used to show how the Snort IDS works and the importance of writing affective rules

![snort_bad_rule](https://github.com/user-attachments/assets/b08f4b47-4c37-4cd3-a97e-f724f7f1f5ff)

![snort_bad_rule_traffic](https://github.com/user-attachments/assets/8611a39b-feb6-46eb-bfc7-21b8b5c6220a)


## 4.4 Custom rule for CONFIDENTIAL traffic
The snort rule for detecting the presence the word "CONFIDENTIAL" in the network traffic will raise an alert when sensitive information is shared:

Snort rule for alerting when the confidential plan.html page is accessed 

![snort_confidential_rule](https://github.com/user-attachments/assets/ff5efc4a-7582-490e-a005-c7bdf2f36007)

Accessing the www.example.com/plan.html page triggers the alert and sends to console

![snort_confidential_alert](https://github.com/user-attachments/assets/ef68ab35-a012-4ae8-adb8-cf08f4761679)

## 4.7 Distingushing traffic by address

Internal workstations should be able to view the www.example.com/plan.html page without triggering an alert, however NMAP scans from any workstation should cause an ICMP alert

Nmap command from internal workstation triggers ICMP alert

![nmap_command](https://github.com/user-attachments/assets/c2b13aa5-e7ee-43f5-a4f3-17e37c189be5)

![snort_nmap_alert_ICMP](https://github.com/user-attachments/assets/b616758c-8966-41cb-81a8-1c8c88b878fa)

Internal workstation ws2 accesses the confidential plan page and no alert is triggered from the IDS as expected

![snort_internal_no_confidential_alert](https://github.com/user-attachments/assets/8a41e8a1-142f-48f7-ae36-0f0a5d0d3e20)
