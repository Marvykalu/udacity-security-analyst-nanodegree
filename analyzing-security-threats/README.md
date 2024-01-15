# Analyzing Security Threats

## SCENARIO

Udajuicer is the largest juice shop in the world. Without a reliance, the owner of Udajuicer have amassed millions with shops all around the world. The business was booming until Covid-19 hit. Stubborn and not wanting to adapt to the current climate, Manu tried all sorts of gimmicks and deals to drive foot traffic to his business but wasn’t successful. Begrudgingly he accepted his predicament, and it was time to embrace technology.

Manu left it to his internal business team to come up with an online application where customers can place orders for delivery/pickup. Udajuicer’s business team, left with very vague instructions on how to build an application, eventually settled on a newbie Chad, who fleeced their money and created an insecure application.

Excitement was in the air as Udajuicer finally had its flagship product! Udajuicer proceeded to test the application out in beta for a week before production. Unfortunately, the site would constantly go down, and they weren’t sure what the issue was. They reached out to Chad once again to troubleshoot but weren’t able to identify what was going on, as Chad assured them it was nothing on his end. Paranoid Manu thought it was his rival Super Smoothies hacking and taking down his application.

Wanting to get to the bottom of the issue, he reached out to SecureCorp, a cybersecurity consulting firm. SecureCorp has deployed me, a security analyst, to get to the bottom of the issue and find out why the Juice Shop site keeps going down. 

## TO DO:

My job will consist of building a threat model for Manu’s website. I will help Manu mitigate his current issue and build a secure application.

## Section 1 - ASSESSMENT

Section 1: Assessment
It’s time to get to work! You’ve arrived at one of Udajuicer’s headquarters located in Miami and are shocked at the lack of technology. You ponder how in the world this is the largest juice shop without ever using computers or relying on technology. After the initial shock, you’re ready to get back on track and get to work. Manu, the eccentric owner, takes it upon himself to work with you directly to make sure you have everything you need. You first request an architecture diagram of the application and logs from right before the application went down. At a quick glance, you notice the woefully designed architecture and buckle up for a long day, all the whilst Manu is in your ear talking about Super Smoothies evil plot to take down his franchise.


### Part 1: Asset Inventory

What does Udajuicer have of value?  The first part of our threat model is being able to identify all the assets involved in the target of the assessment. Looking at the [network architecture diagram](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/network_architecture.png)

I have identified all the components that make up Udajuicer and documented them in the assessment scope of my [assessment report](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/Threat-Report-Assessment.pdf).

### Part 2: Architecture Audit

Now that I’ve identified all the components that make up Udajuicer, I will conduct an architecture review with the given diagram. Following secure architecture best practices, I have listed three flaws in the design. See [Architecture Audit section](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/Threat-Report-Assessment.pdf) in the threat report file.

### Part 3: Threat Model

I built a threat model diagram showing the flow of data using OWASP Threat Dragon. Following OWASP Top 10, I identified at 3 possible threats that would pose a threat to the web application. See [threat model section](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/Threat-Report-Assessment.pdf) of the for data flow diagram.

### Part 4: Threat Analysis

Let us now use our knowledge of the few insecurities in Udajuicer’s architecture to identify the cause of the website down time. Again see Threat Analysis section of [Threat-report-Assessment.pdf](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/Threat-Report-Assessment.pdf) for my findings.


### Part 5: Threat Actor Analysis

The final part of my assessment consists of me trying to identify the threat actor -                                                                                                                           who would possibly want to take down the Juice Shop? You can view my finings in [Threat-Report](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/Threat-Report-Assessment.pdf).

## Section 2: Vulnerability Testing

I’ve identified the initial attack and shortcomings of the application setup. Now I have to continue with a deeper analysis of the application to see if I can find more vulnerabilities. 

### Task 1: SQL Injection

The first vulnerability I want to exploit is on the login page of the website. To see if it is success-title to SQL Injection.  If it is, I will gain root access into the website. See [vulnerability testing]() for my findings. 

### Task 2: XSS - Cross-Site Scripting

The second vulnerability I want to exploit is after I’ve logged into the site. I want to exploit an XSS vulnerability in the search bar, attempting an arbitrary command that will render an alert with the value “Hacked”.

See [vulnerability assessment](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/vulnerability-assessment.pdf) for my findings.

## Section 3: Risk Analysis


I identified the risks in the web application, and applied score to each risks, as well as the rationale. See [risk-analysis-report](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/risk-analysis.pdf) for output.

Ranking show where Udajuicer’s resources should be allocated first as opposed to trying to tackle everything at once.

## Section 4: Mitigation Plan

I’ve broken down all the risks and in what order Udajuicer should mitigate them. I will build out the mitigation plan and get Udajuicer back up and running! See [mitigation plan](https://github.com/Marvykalu/udacity-security-analyst-nanodegree/blob/main/analyzing-security-threats/mitigation-plan.pdf) for output.

### Task 1: Secure Architecture

Utilizing draw.io I designed a far more secure architecture for Manu to implement in getting the Juice Shop back up and running. 

## Task 2: Mystery Attack Mitigation

I will tackle Manu's most pressing issue and implement a solution to mitigate the attack on website and prevent further attacks of this type.

Task 3: SQL Injection Mitigation

Here I described how to implement mitigation plan for injection attacks. 

Task 4: XSS Mitigation

The last issue I fixed is XSS attack. I described mitigations ad how to implement it to avoid future attacks of this type.



