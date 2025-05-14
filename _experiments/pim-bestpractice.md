---

layout: page
collection: experiments
title: Public Identity Management Best Practice Guide Identity Proofing
permalink: /experiments/pim/bestpractices/
sidenav: experiments
sticky_sidenav: true

subnav:
  # - text: Introduction
  #   href: '#introduction'


---

{% include alert-warning.html heading="Draft" content="The following document is a Draft and should not be interpreted as a finalized rule." %}

## 1. Executive Summary

As the number of identity thefts committed in the U.S. for fraud purposes increases every year, the federal government must establish common business practices for identity proofing. Identity theft occurs when rights (e.g., benefits and access) are wrongfully claimed, causing the victim financial loss, reputational (credit) damage, and legal issues. Some of the most common reasons people or criminal groups commit identity fraud are to:

- Access services they’re not entitled to,  
- Get benefits they’re not entitled to, and  
- Steal personal, medical, or financial information from other identities.

The federal government has identity proofing guidelines established by the National Institute of Standards and Technology, but these guidelines are not uniformly followed—particularly when ensuring linkage between a claimed identity and the person presenting the evidence. The practice of adhering to these guidelines must become standard across the federal landscape when citizens access federal services online. This will help protect both individuals and organizations by ensuring that people are who they claim to be, mitigating the risk of financial loss, reputational damage, and legal issues associated with identity theft. 

This document provides an overview of identity proofing along with use cases and best practices. It is based on federal policies (such as Office of Management and Budget Memorandum M-19-18) and guidance, and existing Federal Identity, Credential, and Access Management (FICAM) playbooks. 

## 2. Disclaimer

GSA’s Office of Government-wide Policy, Identity Assurance and Trusted Access Division,  
developed this best practice guide. U.S. Executive Branch agencies can use it to plan identity proofing processes and services. This guide is not an official policy or mandated action. However, it does provide information backed by authoritative federal sources.

## 3. Key Terms

**Assertion**: A digital statement from a verifier (usually an Identity Provider) to a Relying Party (usually an application) that contains subscriber (usually a username) information. It can include additional attributes such as government employee or law enforcement agent status, or authenticator type used in an access control decision.

**Identity**: The set of physical and behavioral characteristics by which an individual is uniquely recognizable. The digital representation of this is called Digital Identity.

**Public Identity**: A digital identity owned and managed by an agency, which may include US Citizens, service providers, and employees/contractors from Federal, State, and Local government levels.

**Identity Proofing**: The process by which information is collected, validated, and verified about a person in order to issue credentials to that person.

 ## 4. Identity Proofing Overview

Identity proofing, also known as identity verification, is the process of verifying a person's identity to confirm that they are who they claim to be. It plays a critical role in protecting against fraud and security threats. It is particularly vital to federal services offered to U.S. citizens and for service providers working with federal agencies, especially in contexts involving financial benefits. By verifying identities, federal agencies can ensure that individuals (especially new or unknown users) are legitimate before granting them access to services or sensitive data.

Identity verification is therefore crucial for safeguarding both individuals and organizations. It helps prevent identity theft, financial loss, reputational damage, and legal issues by ensuring only authorized individuals can access protected resources, in addition to enabling agencies and businesses to comply with important regulations. 

Identity proofing is typically the first step in the authentication process. It can be performed either remotely or in person. In some cases, it may not be required to access lower-risk services. 

![Figure 1]()

**Per established federal guidelines, identity proofing should lead to the following outcomes (as depicted in the graphic above):**

- Resolution of a claimed identity to a single, unique identity, i.e., determining “of the 10,000 possible John Smiths that are in the U.S., which one is this?”

- Validation that all supplied evidence is correct and genuine (e.g., not counterfeit or misappropriated), i.e., determining “that the documentation and information presented by ‘John Smith’ is genuine.”

- Proof that the claimed identity exists in the real world, i.e., determining that someone claiming to be a “particular John Smith” is in fact a real person and not a made-up (synthetic) identity.

- Verification that the claimed identity is associated with the real person supplying the identity evidence, i.e., that someone claiming to be a “particular John Smith” is in fact that person—and not someone who is trying to steal his identity.

![Figure 2]()

## 5. Identity Proofing in the Federal Landscape

The Public Identity and Access Management (PIAM) framework has four components (depicted in the image below), of which one, Identity Management, encompasses identity proofing. The four components provide a common model through which agencies can understand and implement identity, credential, and access management (ICAM) processes.

![Figure 3]()

1. **Identity management** focuses on managing the lifecycle, governance, and compliance aspects of a person’s identity. This includes capabilities such as role-based access control (RBAC), access certification, and policy enforcement. It is also concerned with managing user access according to organizational policies and in alignment with regulatory requirements.

2. **Access management** is the process of identifying, tracking, controlling, and managing authorized users' access to a system or application. It encompasses the policies, processes, methodologies, and tools used to validate users before granting access to applications or data. Access management plays a central role in information security, IT, and data governance by ensuring that only authorized users can access protected resources, while blocking unauthorized access.

Credential management is a subset of access management, focusing on how credentials are used in an organization’s access control strategy. Credential management refers to managing the lifecycle of credentials used for authentication. This lifecycle includes activities such as issuance, reissuance, reset, suspend, restore, updating, and revoking/terminating. These credentialing activities are grouped into three stages: initial provisioning, maintenance, and revocation. 

3. **Privileged access** refers to the processes and technologies used to manage privileged access to data. In the context of public identity, this typically focuses on access that allows an identity to view or interact with sensitive data. Additionally, a delegated public identity can be defined as privileged if it is granted access to modify other identity profiles or submit financial transactions on behalf of others.

4. **Governance** involves monitoring and responding to user behavior and system events by leveraging data as a strategic asset to make adaptive and risk-based decisions. It ensures the right individual accesses the right resource, at the right time, for the right reason, which supports federal business objectives and facilitates secure and effective agency mission delivery.

The image below shows the various subsections of Access Management. This practical guide offers guidance around identity proofing as a subsection of the Access Management component of the PIAM framework. 

![Figure 4]()

 ## 5. Identity Proofing Challenges

Identity proofing solutions for public identity must balance several challenges, including:

- **Accuracy**: Ensuring that an individual’s identity is valid.

- **Security**: Preventing fraud-related incidents, such as social engineering or account takeover.

- **Usability**: Enabling secure access without creating unnecessary friction or burden for users that might cause them to abandon the verification process. 

- **Data Protection**: Safeguarding personally identifiable information (PII) collected during the identity verification process against unauthorized access.

- **Privacy**: Ensuring that only necessary data is collected, used, and handled to prevent unauthorized access or disclosure.

- **Accessibility**: Making sure that everyone, regardless of their abilities or circumstances, can easily and reliably use the identity proofing methods.

When evaluating identity proofing systems and processes, it is important to select ones that are user-friendly and can be integrated seamlessly into an organization’s operational structures. Additionally, it is also imperative to ensure these solutions serve all members of the public equally, taking into account the following considerations:

- 1 in 10 adults do not have a valid driver’s license or state-issued ID according to the Center for Democracy and Civic Engagement (Appendix \- Reference \#4)

- 14% of US adults are considered underbanked according to the Federal Deposit Insurance Corporation (FDIC) (Appendix \- Reference \#5)

- 12% of American households do not have internet access at home according to the National Telecommunications and Information Administration (NTIA) (Appendix \- Reference \#6)

 ## 6. Key Reasons Why Identity Proofing is Important

- **Fraud prevention**: Verifying identities significantly reduces the risk of identity theft, account takeover, and other fraudulent activities.

- **Data security**: Identity proofing ensures that only authorized individuals can access sensitive information and services, minimizing the risk of system or data breaches. 

- **Compliance with regulations**: Many industries, and particularly financial services, are required by law to verify customer identities. 

- **Trust building**: Identity proofing helps build trust by ensuring that users are who they claim to be, leading to greater confidence in the security of transactions and interactions between the government and citizens.

- **Customer experience**: While identity proofing adds an additional layer of security, it should be seamless and non-intrusive for users. Effective identity-proofing processes can enhance the overall customer experience by balancing security with convenience.

- **Accountability**: Federal agencies may need to prove who uses their services for accountability purposes. For example, an agency might need to identify an individual who registers for a federal service under an alias and then uses it to harass others. 


By preventing identity theft, fraud, and unauthorized access to sensitive information, the identity proofing process protects both individuals and federal agencies. The image below depicts one example of how identity proofing helps, specifically by enabling compliance with regulations like KYC (Know Your Customer) and AML (Anti-Money Laundering). 

![Figure 5]()

# Identity Proofing Assurance Levels & Methods

The first step in identity proofing is to determine what level of identity assurance is required. NIST guidelines have established a simple framework that provides direction for federal agencies in making this determination. The framework identifies three levels of identity assurance. 

- **NIST Identity Assurance Level One**  
  Identity proofing is not required. For instance, it is unnecessary when signing up for a loyalty account or a newsletter.

- **NIST Identity Assurance Level Two**  
  Limited identity proofing is required; for instance, when it is necessary to provide identifying information in person or remotely as well as evidence of address validity (e.g., uploading a photo of a driver’s license). While not a requirement, Level Two identity assurance may include biometric checks (e.g., fingerprints or a retinal scan).

- **NIST Identity Assurance Level Three**  
  In-person or supervised remote identity verification, address verification, and biometric checks are all required for the highest level of identity proofing.

The appropriate identity-proofing systems can be selected and implemented based on the level required by the situation. Potential scenarios requiring some level of identity proofing include:

- Individuals registering for an account for the first time to access federal services.

- Individuals accessing federal sites for services and logging in from restricted countries or locations.

- Individuals accessing federal sites for services on behalf of other citizens.

- Individuals accessing federal sites to request financial transactions of significant monetary value.

There are various ways to verify identity. The methods an organization uses depend on the required level of identity assurance and what works with their internal processes. Typically, multiple methods are used together. Common methods include:

- **Document verification** typically involves a government-issued ID such as a driver’s license or passport. Where permitted, this could be a photo or scan of a physical ID or a digital ID such as a mobile driver’s license. 

- **Biometric verification** most commonly involves taking a “selfie” with a mobile phone, with the selfie then compared against an official ID to ensure a match.

- **Database verification** involves comparing user-supplied information against official databases, such as those managed by the DMV and IRS. 

The following is an exploration of a variety of identity proofing methods that may be implemented based on the required level of identity assurance in a particular situation. Both definitions and examples of the step-by-step process of applying each method are provided.

