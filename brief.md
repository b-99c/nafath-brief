Version: NAFATH-V4
Track: Software

## Overview

Interoperability of software, mobile apps, data, artificial intelligence systems, and internet connections is essential to a national service. If any of these areas are weak, they can put the service or users at risk. Secure software practices help to secure settings and secrets, and mobile security checks help to find weaknesses in the application. Artificial intelligence systems also need to be protected from attacks that could interfere with their inputs or training data. Good networking ensures that Internet traffic is routed safely to the actual service. Cybersecurity teams need to identify and fix serious vulnerabilities, and a software bill of materials helps them understand what components the service relies on. Together, these fields help reduce risk and keep the service trustworthy; software configuration and secrets should be stored outside the code.

## Software

Software applications require settings, such as access keys and passwords. The application may be running on the developer’s computer and server and settings may differ. They should be kept outside the code so that the application can read them at start up time. This makes settings easier to change and reduces the chances of accidentally exposing secrets if code files are shared or published.

Resource: Config - The Twelve-Factor App - https://12factor.net/config

## AI

Machine learning systems are susceptible to various types of attacks. Poisoning attack is type of attack where the attacker manipulates or injects the malicious data in the training data of the model. This can lead to the model learning spurious patterns. In an evasion attack the attacker manipulates the input data after the model is trained with the aim of getting it to return an incorrect result. The key difference is the time of the attack: Poisoning is performed at the training phase, while evasion is performed at the model deployment phase.

Resource: Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - NIST - https://csrc.nist.gov/pubs/ai/100/2/e2025/final

## Mobile

OWASP Mobile Application Security Verification Standard (MASVS) A mobile app security requirements standard. This includes things like storing data, encrypting it, logging in, and communicating over a network. Its controls are used as a checklist by developers and testers to review an app and find security weaknesses. They can look at the application's files and test it as it is running. This is to help determine whether the app is protecting users and their information.

Resource: The Mobile Application Security Verification Standard - OWASP - https://mas.owasp.org/MASVS/03-Using_the_MASVS/

## Networking

A BGP route hijack happens when a network advertizes that it can deliver traffic to the IP address range. Other networks could send traffic over the wrong network which could be monitored or disrupted. RPKI helps by letting networks verify whether the network announcing the route is allowed to originate it. But RPKI does verify the origination of the route, it won't verify every network that traffic passes through or stop every kind of routing attack.

Resource: RFC 6811 - BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811

## Cybersecurity

Log4Shell (CVE-2021-44228) was a zero-day vulnerability in the Apache Log4j logging library. Specially crafted data could allow a vulnerable system to execute arbitrary code remotely on vulnerable versions. It was a serious vulnerability because Log4j was used everyplace and the attack was so easy. Affected systems were identified and Log4j was upgraded to a patched version in response. “Temporary workarounds were no substitute for the update.

Resource: Mitigating Log4Shell and Other Log4j-Related Vulnerabilities - CISA - https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a

## Data

What is a software bill of materials (SBOM)? A software bill of materials (SBOM) is a list of the components that make up a software product. It lets the organization see what its software depends on and to identify components that might need some TLC. The minimum information to be provided shall include the supplier name, the component name, the component version, other identifiers, dependency relationships, the SBOM author and the date and time it was created.

Resource: The Minimum Elements for a Software Bill of Materials (SBOM) - NTIA - https://www.ntia.gov/files/ntia/publications/sbom_minimum_elements_report.pdf

## Misconception in My Track

Another misconception in software development is if the code is private it is okay to store passwords and API keys directly in the code . But code can be shared, leaked, or copied accidentally and this exposes these secrets. In the Twelve-Factor App “Config” section it says, “Config that changes between deploys should be stored in the environment, not in the code. Configuration changes are possible, and the risk of leakage of sensitive information is reduced.”

## Open Question

How can a development team make sure that passwords and API keys are never accidentally included in code or shared through version control?
