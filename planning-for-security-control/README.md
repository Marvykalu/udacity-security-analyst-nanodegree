# Planning for Security Controls

Organizations 

In this project, I assume the role of an Information Security Analyst for  COMPANY_A. Working for the infrastructure team, I am the only staff member whose role is dedicated solely to information security. 

#### Primary Responsibilities

To Protect, Detect, and Respond to possible threats to the security of the organization’s mission. These duties include:


### About COMPANY_A

- COMPANY_A was founded in 2010, it develops and sells the famous “Beeplepop” along with a line of household innovations that forever revolutionized the way we live and work.

- COMPANY_A’s main office is located at an office park in St. Louis, MO, and accommodates approximately 100 full-time employees. The office park is home to 3-4 similarly sized companies with shared parking facilities.

- COMPANY_A maintains an on-premise data center with dedicated hardware running its entire infrastructure

- COMPANY_A’s primary web property (www) is an eCommerce website, built on WordPress with SSL certificate. 

- COMPANY_A’s ERP system contains highly sensitive data and is used to generate all of the business intelligence for the senior executives. 

-  Due to legal reasons, COMPANY_A is obligated to retain this legacy data

## TASK 1: Standards

Heather, my manager, asked me to review how well COMPANY_A’s current security controls hold-up against the NIST-800-53 framework. I used an abbreviated NIST-800-53 work book for this assignment. Please see [NISTWorkBook.xlsx](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/NIST-workbook.xlsx), for my feedback about how COMPANY_A addresses various control families.

## TASK 2: Controls

After my dazzling NIST report, the CIO is asked me to provide feedback on additional measures to integrate into his IT strategic plan that specifically addresses information security.
 
- Please see [security-plan.docx](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/security-plan.docx), for my recommended physical and logical controls to enhance the security posture of COMPANY_A.

- Please see [Remote_Access_Policy.docx](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/remote-access-policy.docx) and Password_Protection_Policy.docx](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/password-protection-policy.docx) for customized policies for use by COMPANY_A.

## TASK 3: Security Design

### SCENARIO 1: Workforce Mobilization

*** Recent company wide communication ***

From: Kathy (k^^^@^^^m)

To: ALL-Employees

Subject: URGENT Pandemic Response

Dear COMPANY_A staff-

Due to a recent public health emergency, effective March 20, COMPANY_A will be closing its physical office and limiting access to the facilities to essential personnel only. Senior leadership is working with the technology team to distribute the necessary computing resources to continue business operations remotely. We will publish an updated Remote Work Agreement with additional guidelines to provide the same level of exceptional service to our customers despite the challenges ahead.

Thank you for your cooperation.

Kathy, CEO | COMPANY_A

The technology team has been scrambling to inventory and distribute computing resources for all staff. Additionally, Ken (CIO) and Heather (Infrastructure Manager) have been putting together a Remote Work Policy which includes some basic home-office considerations. Under the current network topology, employees will not be able to access the Enterprise Resource Planning (ERP) system that is currently located in the on-premise datacenter.

#### TODO

After careful deliberation with the leadership team, I recommended implementing a VPN gateway as a quick, low-cost solution to provide access to resources behind COMPANY_A's firewall. 

I am now tasked with creating a deployment plan to incorporate this new VPN functionality into the network topology. 

Please see [OpenVPN_Network_digram.jpg](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/OpenVPN_Network_diagram.jpg) for the deployment plan. 

### SCENARIO 2: Authentication Factor

Great work in planning the VPN deployment! We are now operating with 95% of our staff working remotely.

...2 months later...


From: Jim (j***@****m)

To: Ken (k@**m)

cc: Heather (h@******m), me

Subject: HELP!

Dear Ken, Heather-

I think I have been hacked! I got an email saying that the paystubs were ready, but when I checked my bank account, I didn't see anything in there. I logged into ERP, and my direct > > > deposit information is not right. I have never heard of BANK OF FAKESLOVIA._

Please let me know what to do!

Jim, Lift Operator | Shipping & Receiving | COMPANY_A


After my forensic analysis, I discovered that COMPANY_A suffered a major data breach when a successful email phishing campaign exfiltrated the username and passwords for a number of employees. Although the incident was contained in a timely fashion, COMPANY_A suffered some significant financial implications including unexpected legal fees, remediation service fees, an increase in insurance premiums, and direct financial loss for the missing direct deposit transactions. Kathy (CEO) was advised by COMPANY_A's cyberinsurance provider to implement stronger authentication controls.

#### TO DO: 

After completing a request for proposal (RFP) with several vendors, Ken (CIO) has decided that Duo is the best candidate for offering 2FA services. He has asked you to provide a deployment plan for incorporating Duo's 2FA service into COMPANY_A's network topology.

Please see [DUO2F_Network_Diagram.jpg](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/planning-for-security-control/Duo2F_Network_Diagram.jpg), for the deployment plan.


