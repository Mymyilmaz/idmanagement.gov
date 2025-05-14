---

layout: page
collection: experiments
title: Public Identity Best Practices Guide
permalink: /experiments/pid/bestpractices/
sidenav: experiments
sticky_sidenav: true

release: 1.0 

subnav:
  - text: Executive Summary
    href: '#executive-summary'
  - text: Disclaimer
    href: '#disclaimer'
  - text: Key Terms
    href: '#key-terms'
  - text: Identity Proofing Overview
    href: '#identity-proofing-overview'
  - text: Identity Proofing in the Federal Landscape
    href: '#identity-proofing-in-the-federal-landscape'
  - text: Identity Proofing Challenges
    href: '#identity-proofing-challenges'
  - text: Key Reasons Why Identity Proofing is Important
    href: '#key-reasons-why-identity-proofing-is-important'
  - text: Identity Proofing Assurance Levels & Methods
    href: '#identity-proofing-assurance-levels--methods'
  - text: Identity Proofing Scenarios
    href: '#identity-proofing-scenarios'
  - text: Future Considerations
    href: '#future-considerations'
  - text: Conclusion
    href: '#conclusion'
  - text: Appendix
    href: '#appendix'
  - text: References
    href: '#references'

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

![Figure 1]({{site.baseurl}}/assets/experiments/pid/figure1.jpg)

**Per established federal guidelines, identity proofing should lead to the following outcomes (as depicted in the graphic above):**

- Resolution of a claimed identity to a single, unique identity, i.e., determining “of the 10,000 possible John Smiths that are in the U.S., which one is this?”

- Validation that all supplied evidence is correct and genuine (e.g., not counterfeit or misappropriated), i.e., determining “that the documentation and information presented by ‘John Smith’ is genuine.”

- Proof that the claimed identity exists in the real world, i.e., determining that someone claiming to be a “particular John Smith” is in fact a real person and not a made-up (synthetic) identity.

- Verification that the claimed identity is associated with the real person supplying the identity evidence, i.e., that someone claiming to be a “particular John Smith” is in fact that person—and not someone who is trying to steal his identity.

{% include alert-info.html content="Identity proofing and authentication are two related but distinct concepts in the field of online security. Identity proofing is the process of verifying an individual’s identity by collecting and verifying personal information, while authentication is the process of verifying that an individual is who they claim to be." %}

## 5. Identity Proofing in the Federal Landscape

The Public Identity and Access Management (PIAM) framework has four components (depicted in the image below), of which one, Identity Management, encompasses identity proofing. The four components provide a common model through which agencies can understand and implement identity, credential, and access management (ICAM) processes.

  ![Figure 3]({{site.baseurl}}/assets/experiments/pid/figure3.jpg)

  1. **Identity management** focuses on managing the lifecycle, governance, and compliance aspects of a person’s identity. This includes capabilities such as role-based access control (RBAC), access certification, and policy enforcement. It is also concerned with managing user access according to organizational policies and in alignment with regulatory requirements.

  2. **Access management** is the process of identifying, tracking, controlling, and managing authorized users' access to a system or application. It encompasses the policies, processes, methodologies, and tools used to validate users before granting access to applications or data. Access management plays a central role in information security, IT, and data governance by ensuring that only authorized users can access protected resources, while blocking unauthorized access.

  Credential management is a subset of access management, focusing on how credentials are used in an organization’s access control strategy. Credential management refers to managing the lifecycle of credentials used for authentication. This lifecycle includes activities such as issuance, reissuance, reset, suspend, restore, updating, and revoking/terminating. These credentialing activities are grouped into three stages: initial provisioning, maintenance, and revocation. 

  3. **Privileged access** refers to the processes and technologies used to manage privileged access to data. In the context of public identity, this typically focuses on access that allows an identity to view or interact with sensitive data. Additionally, a delegated public identity can be defined as privileged if it is granted access to modify other identity profiles or submit financial transactions on behalf of others.

  4. **Governance** involves monitoring and responding to user behavior and system events by leveraging data as a strategic asset to make adaptive and risk-based decisions. It ensures the right individual accesses the right resource, at the right time, for the right reason, which supports federal business objectives and facilitates secure and effective agency mission delivery.

The image below shows the various subsections of Access Management. This practical guide offers guidance around identity proofing as a subsection of the Access Management component of the PIAM framework. 

![Figure 4]({{site.baseurl}}/assets/experiments/pid/figure4.jpg)

## 5. Identity Proofing Challenges

Identity proofing solutions for public identity must balance several challenges, including:

- **Accuracy**: Ensuring that an individual’s identity is valid.

- **Security**: Preventing fraud-related incidents, such as social engineering or account takeover.

- **Usability**: Enabling secure access without creating unnecessary friction or burden for users that might cause them to abandon the verification process. 

- **Data Protection**: Safeguarding personally identifiable information (PII) collected during the identity verification process against unauthorized access.

- **Privacy**: Ensuring that only necessary data is collected, used, and handled to prevent unauthorized access or disclosure.

- **Accessibility**: Making sure that everyone, regardless of their abilities or circumstances, can easily and reliably use the identity proofing methods.

When evaluating identity proofing systems and processes, it is important to select ones that are user-friendly and can be integrated seamlessly into an organization’s operational structures. Additionally, it is also imperative to ensure these solutions serve all members of the public equally, taking into account the following considerations:

- 1 in 10 adults do not have a valid driver’s license or state-issued ID according to the Center for Democracy and Civic Engagement (Appendix - Reference #4)

- 14% of US adults are considered underbanked according to the Federal Deposit Insurance Corporation (FDIC) (Appendix - Reference #5)

- 12% of American households do not have internet access at home according to the National Telecommunications and Information Administration (NTIA) (Appendix - Reference #6)

## 6. Key Reasons Why Identity Proofing is Important

- **Fraud prevention**: Verifying identities significantly reduces the risk of identity theft, account takeover, and other fraudulent activities.

- **Data security**: Identity proofing ensures that only authorized individuals can access sensitive information and services, minimizing the risk of system or data breaches. 

- **Compliance with regulations**: Many industries, and particularly financial services, are required by law to verify customer identities. 

- **Trust building**: Identity proofing helps build trust by ensuring that users are who they claim to be, leading to greater confidence in the security of transactions and interactions between the government and citizens.

- **Customer experience**: While identity proofing adds an additional layer of security, it should be seamless and non-intrusive for users. Effective identity-proofing processes can enhance the overall customer experience by balancing security with convenience.

- **Accountability**: Federal agencies may need to prove who uses their services for accountability purposes. For example, an agency might need to identify an individual who registers for a federal service under an alias and then uses it to harass others. 


By preventing identity theft, fraud, and unauthorized access to sensitive information, the identity proofing process protects both individuals and federal agencies. The image below depicts one example of how identity proofing helps, specifically by enabling compliance with regulations like KYC (Know Your Customer) and AML (Anti-Money Laundering). 

![Figure 5]({{site.baseurl}}/assets/experiments/pid/figure5.jpg)

## 9. Identity Proofing Assurance Levels & Methods

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

### A. Knowledge Based

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon1.jpg" alt="Knowledge Base icon">Knowledge based identity proofing refers to a method of confirming someone's identity by asking them to answer questions about personal information that theoretically only they should readily know (such as their mother's maiden name or previous address). The most common type of knowledge-based proofing uses personal credit report data for validation.</p> 

![Figure 6]({{site.baseurl}}/assets/experiments/pid/figure6.jpg)

1. Public citizen accesses online registration link.  
2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
3. Public citizen performs the identity proofing step using credit report data.  
4. Credit report data is retrieved, and random questions are generated from the data and presented to the user. The public citizen then selects the answers to the random questions and submits them for validation.  
5. The answers given to the random questions are validated by comparing them with the credit report data.  
6. Public citizen identity is created with profile data after answers to the random questions are successfully validated.

### B. Third Party Provider

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon2.jpg" alt="Third Party Provider icon">Third party identity proofing refers to a method of confirming someone's identity by asking them to leverage third party credentials such as banking credentials. The majority of Americans have bank accounts, and since a bank account cannot be created without first validating government-furnished documentation in accordance with strict guidelines, this method provides a mechanism to validate identity for a government service.</p>

![Figure 7]({{site.baseurl}}/assets/experiments/pid/figure7.jpg)

1. Public citizen accesses online registration link.  
2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
3. Public citizen performs the identity proofing step using bank credentials.  
4. The bank website redirects to the bank login page.  
5. Public citizen enters bank credentials and performs any Multi-Factor Authentication (MFA) verification steps.  
6. Public citizen identity is created with the profile data after bank credentials are successfully validated.

### C. Biometrics

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon3.jpg" alt="Biometrics icon">Biometric identity verification is a process that uses unique physical or behavioral characteristics to confirm a person's identity. In a digital environment, biometrics give a higher assurance that a person is who they say they are than other forms of verification. Using biometrics is a secure and convenient way to prove customer identities during onboarding, verification, or authentication.</p>

Public citizens can anchor their physical identity to a digital account at sign-up using a photo ID and a selfie or video. First, a user takes a picture of their identity document and then submits either a selfie or a video, which is then compared to the photo on the identity document. 

- **Selfie Check**: Public citizens are guided to take a selfie picture. The face in the identity document is then compared to the selfie, returning a similarity score. This checks that the person submitting the ID is the same person who owns that ID, protecting against stolen or fake IDs. The selfie is also analyzed for abnormal texture which protects from fraud. It also detects photos of photos, or photos of screens, which a fraudster may try to pass off as a selfie.  
    
- **Motion check (Video):** A video check requires the public citizen take a short video of themselves on their phone to prove liveness. The individual is directed to record a specific movement, such as a simple head turn to the left and right. This liveness check determines if the person is present and not using a mask or prerecorded video, and that they are the same person as the one submitting the ID. Video adds an extra layer of protection from additional and more sophisticated fraud attacks, such as spoof selfies, deep fake videos, and 2D and 3D masks.

![Figure 8]({{site.baseurl}}/assets/experiments/pid/figure8.jpg)

1. Public citizen accesses online registration link.  
2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
3. Public citizen performs the identity proofing step using biometrics.  
4. Public citizen uploads image of a US government-issued photo ID such as state driver license or passport.  
5. Public citizen uploads live image capture using a mobile phone or other camera-enabled device.  
6. Public citizen identity is created with the profile data after successful comparison between the picture in the US government-issued photo ID and the live captured image.
	  
The U.S. General Services Administration’s Login.gov is an example of a federal service that uses biometric identity verification. Login.gov offers the public secure and private online access to participating government programs. With one Login.gov account, users can sign into multiple government agencies’ services. Login.gov uses facial matching technology that compares the selfie exclusively with the user’s photo ID and does not use the image for any other purpose. 

There are other forms of biometric identity proofing that can be used, including:

- **Fingerprint** identity proofing verifies a person's identity using their fingerprints. It is a type of biometric verification that uses algorithms to analyze the unique ridges and patterns of a person's fingertips.

- **Iris** identity proofing uses unique patterns in a person's iris to verify their identity. Iris recognition is considered more accurate than some other forms of biometrics, such as facial recognition.

- **Voice** identity proofing, also known as voice authentication, uses a person's voice to verify their identity.

- **Palm Vein** authentication is classified as a physiological biometric authentication. It uses palm vein patterns seen in a vascular image of a person's palm as personal information.

- **Finger Vein**: Finger vein identity proofing verifies someone's identity by using infrared light to capture the internal vascular structure of the veins in their fingers. This method is considered highly secure as it's nearly impossible to forge due to the vascular structure’s internal nature and unique pattern for each individual.

- **Behavioral Biometrics**: Behavioral biometrics refers to a method of identity proofing that uses a person's unique behavioral patterns, like how they type, swipe, or move their mouse, to verify their identity rather than relying on physical characteristics like fingerprints or facial recognition. It analyzes how someone interacts with a device to authenticate them as a legitimate user, helping to detect potential fraud by identifying unusual behavior patterns. Examples of behavioral biometrics include:

- **Mouse behavior** tracks how a user moves their mouse, including the speed and patterns of movement.

- **Touchscreen behavior** tracks how a user interacts with a touchscreen, including how they hold the device, how much pressure they apply, and what gestures they make.

- **Voice recognition** analyzes the behavioral signals in a user's voice to authenticate them.

- **Typing biometrics** analyzes a user's keystroke patterns to authenticate them.

- **Behavioral PIN authentication** analyzes how a user holds their phone and enters their PIN, including their wrist strength and finger placement.

- **Gesture recognition** analyzes how a user moves their hands, such as when typing on a keyboard or tapping on a screen.

### D. Remote Verification

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon4.jpg" alt="Remote Verification icon">Some members of the public want the opportunity to engage with a human during the identity verification process but are unable to visit a physical location. This method enables a user to digitally verify their identity with a human agent, such as through a live video chat with a trained identity verification professional.</p>

  ![Figure 9]({{site.baseurl}}/assets/experiments/pid/figure9.jpg)

  1. Public citizen accesses online registration link.  
  2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
  3. Public citizen performs the identity proofing step using live video chat.  
  4. Public citizen initiates live video chat and identity verification expert requests data for identity proofing.  
  5. Public citizen uploads live image capture using a mobile phone or camera enabled device and submits for validation.  
  6. Public citizen identity is created with the profile data after comparison with the picture in the government-issued photo ID and the live captured image is successfully validated by the identity verification expert.

### E. In-Person 

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon5.jpg" alt="In-Person icon">In-person identity proofing is the process of verifying that the individual requesting access to federal services both matches the identity on their submitted documents and is physically present at a federal facility. The process involves presenting original identification and proof of address documents during the verification process. This is a secure identity verification option for individuals that prefer face-to-face interactions and is available as part of both basic (non-Identity Assurance Level 2) and enhanced (IAL2) identity verification.</p>

According to the United States Postal Service (USPS), 99% of US public citizens live within 10 miles of a USPS location, thus providing a convenient way for identity proofing a public identity if remote/virtual methods cannot be leveraged by an individual.

  ![Figure 10]({{site.baseurl}}/assets/experiments/pid/figure10.jpg)

  1. Public citizen accesses online registration link and searches for a nearby federal facility such as a US Post Office.  
  2. Public citizen visits the federal facility in person.  
  3. Public citizen performs the identity proofing step with a federal employee.  
  4. Public citizen provides documentation such as a US government-issued photo ID or US passport.  
  5. Federal employee uploads real-time image captured using camera-enabled device and submits for validation.  
  6. Identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes is received, and a public citizen identity is created after a federal employee successfully validates the public citizen identity.

### F. Physical Mail - One Time Code

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon6.jpg" alt="Physical Mail - One Time Code icon">This identity proofing method validates an identity using a physical address that belongs to the public citizen. The key validation component is that the physical address matches the name of the public citizen under which it is registered. After this is validated, a random one-time code will be generated with an expiration date and a letter with the code will be mailed to the physical address that was validated. Using this code, the public citizen can then proceed to register for an online account to access federal services and benefits.</p>

  ![Figure 11]({{site.baseurl}}/assets/experiments/pid/figure11.jpg)

  1. Public citizen accesses online registration link.  
  2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
  3. Public citizen performs the identity proofing step using physical address data.  
  4. Physical Address data is received and checked against the address verification solution. If the verification process is successful, a random one-time code is generated and physically mailed to the public citizen’s physical address.  
  5. After the public citizen receives the mail, the one-time code is entered to continue with the registration process.  
  6. Public citizen identity is created with the profile data after one-time code validation is successful.

### G. Mobile Phone Device

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon7.jpg" alt="Mobile Phone Device icon">This identity proofing method validates an identity using a mobile device number that is registered to the public citizen. The key validation component is that the mobile device number is registered under a name which matches the public citizen’s name. After this is validated, a random one-time code with an expiration period is generated and sent to the validated mobile phone number. Using this code, the public citizen can proceed to register the device metadata (such as type of device, operating system geolocation, and other identity-related attributes). Once the device is successfully registered, the public citizen identity is created with the profile data.</p>

  ![Figure 12]({{site.baseurl}}/assets/experiments/pid/figure12.jpg)

  1. Public citizen accesses online registration link.  
  2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
  3. Public citizen performs the identity proofing step using mobile phone data.  
  4. Mobile phone data is received and checked against phone verification solutions. If the verification process is successful, a random one-time code is generated and sent to the public citizen’s mobile device.  
  5. After the public citizen receives the one-time code, it is entered to continue the registration process.  
  6. Public citizen identity is created with the profile data after one-time code validation is successful and mobile phone metadata is registered.

### H. Federal Employees or Contractors - PIV Card

<p><img class="float-left margin-right-2" width="105px" src="{{site.baseurl}}/assets/experiments/pid/icons/icon8.jpg" alt="Federal Employees or Contractors - PIV Card icon">This identity proofing method is the process of validating an identity using a Personal Identity Verification (PIV) card registered to the public citizen. The key validation component is that a PIV card is only issued after identity proofing steps are completed by a federal agency, which typically occurs in person at a federal facility and is only done for federal employees and contractors.</p>

  ![Figure 13]({{site.baseurl}}/assets/experiments/pid/figure13.jpg)

  1. Public citizen accesses online registration link.  
  2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.  
  3. Public citizen performs the identity proofing step using a PIV card.  
  4. Public citizen inserts the PIV card into a machine-readable device  
  5. Public citizen enters the PIN code for the PIV card.  
  6. Public citizen identity is created with the profile data after the PIN code for the PIV card is successfully validated.

## 10. Identity Proofing Scenarios

The following sections detail various scenarios which require identity proofing and give examples of how an agency can handle them.

### 1. Initial Identity Verification for New Users 

When a new customer applies to open an online account to access federal services (such as Medicaid benefits), identity proofing is required to verify their identity in compliance with KYC regulations. This process ensures that the customer is who they claim to be, mitigating the risk of identity theft and fraudulent activity. Listed below are some scenarios involving onboarding a new public identity. 

{:start="1"}
1. **First Time Public Citizen Registration**

    This use case is for a public citizen that requires an identity to create an account to access federal services. The public citizen will provide key mandatory profile attributes, some of which will be used to proceed to the identity proofing steps. Based on the federal service the public citizen is requesting, a list of identity proofing methods will be available for the public citizen to select from. 

    After identity proofing is successfully completed, an identity profile and associated account is created. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the public citizen should be instructed to visit a local facility for in-person identity proofing.

{:start="2"}
2. **Delegate Registration - Registering for Another Public Citizen**

    In this use case, the registration process for a public citizen is being performed by another individual serving as a delegated registration authority. For example, this could be a vendor performing registration on behalf of a public citizen with a vision impairment or who does not have access to online assets. The delegated authority will provide key mandatory profile attributes for both them and the public citizen, some of which will be used to proceed to the identity proofing steps. Based on the federal service the public citizen is requesting, a list of identity proofing methods will be available for the delegate to select from. 

    Both the delegate and public citizen need to be identity proofed. This ensures that an unauthorized individual is not attempting to fraudulently create an identity for a public citizen. After identity proofing is successfully completed for both the delegate and the public citizen, an identity profile and associated account is created only for the public citizen. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the delegated authority should be instructed to visit a local facility for in-person identity proofing.

{:start="3"}
3. **First Time Public Citizen Registration for Minors or the Elderly**
  
    This use case is similar to Delegate Registration with the distinction that the delegate is an immediate family member or other close relation of the public citizen. The assumption is that the public citizen is a minor or elderly person and either does not have access to online assets or has an impairment preventing them from performing the registration themselves. The family member acting as a delegate will provide key mandatory profile attributes for both them and the public citizen, and some of them will be used to proceed to the identity proofing steps. Based on the federal service the public citizen is requesting; a list of identity proofing methods will be available to be selected by the delegated registration authority. 

    Both the family member acting as the delegate and the public citizen need to be identity proofed. This ensures that an unauthorized individual is not attempting to fraudulently create an identity for a public citizen. After identity proofing is successfully completed for both the delegate and the public citizen, an identity profile and associated account is created only for the public citizen. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the family member acting as the delegate should be instructed to visit a local facility for in-person identity proofing.

### 2. Identity Profile Maintenance and Updates

The following relates to updating data in a public citizen’s profile that is critical to identifying their unique public identity (such as sensitive profile attributes like Address or Phone). In this scenario, the assumption is that the public identity is already onboarded, and the public citizen was identity proofed during the registration process. However, when updating sensitive profile data, verifying identity through the authentication process using MFA alone is insufficient. To add another layer of security in these circumstances, it is better to identity proof the public citizen again. Listed below are some scenarios involving updating public identity profile data. 

{:start="1"}
1. **Updating Key Profile Identity Attributes**

    This use case is related to a public citizen seeking updates to the critical profile data that is key to identifying their unique public identity. Key profile attributes can be First Name, Middle Name, Last Name, Date of Birth, Social Security Number, Primary Address, Driver License Data, State ID Data, Passport Data, Primary Phone or Primary Email.

    The first step is for the public citizen to authenticate successfully and then proceed to the profile page to update their identity attributes. Based on the attributes the public citizen is requesting to update, a list of identity proofing methods will be available for the public citizen to select from.

    After identity proofing is successfully completed, the identity profile and associated account are updated. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the public citizen should be instructed to visit a local facility for in-person identity proofing.

{:start="2"}
2. **Updating Key Profile Identity Attributes by Delegate**

    In this use case, the update process for a public citizen is being performed by another individual serving as a delegated authority. For example, this could be a vendor making updates on behalf of a public citizen with a vision impairment or who does not have access to online assets. The delegated authority will first be authenticated, and if authorized will proceed to the profile update page. The delegate then submits updates to the public citizen’s key profile attributes, some of which will be used to proceed with the identity proofing steps. Based on the attributes the delegate is seeking to update, a list of identity proofing methods will be available for the delegate to select from.

    Both the delegate and public citizen need to perform the identity proofing steps. This ensures that an unauthorized individual is not attempting to fraudulently update an identity for a public citizen. After identity proofing is successfully completed for both the delegate and the public citizen, the identity profile and associated account are updated only for the public citizen. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the delegated registration authority should be instructed to visit a local facility for in-person identity proofing. 

{:start="3"}
3. **Updating Non-Key Profile Identity Attributes**

    In this use case, identity proofing is generally not required. The assumption is that the profile identity attributes being updated are not sensitive and do not have any correlation to risk and fraud detection. Some non-key profile identity attributes include Secondary Address, Birth City, Secondary Phone, Gender, Age, and Contact Information.

### 3.  Financial Transaction Identity Confirmation

“Transaction” refers to an action related to financial benefits that a public citizen obtains from federal agencies. Not all transactions require additional identity proofing steps; requirements are dependent on risk factors such as transaction type, dollar amount, patterns of transactions, the public citizen’s risk score, and any type of violations. A risk management model should be developed and integrated into the authentication or authorization process to determine if identity proofing is needed for a specific transaction. Listed below are some identity proofing scenarios for transactions.  

{:start="1"}
1. **Public Citizen Requesting Benefits**

    In this use case, a public citizen is requesting financial benefits from a federal agency after having successfully been authenticated. The assumption is that the public citizen’s identity is already identity proofed and an identity profile has been created. In this scenario, the identity proofing steps are triggered only when certain conditions are true—for example, the amount requested is above a certain limit, previous transactions were flagged, or certain key identity attributes do not match. 

    The first step is for the public citizen to access a federal agency website and authenticate to access a federal service. Next, the citizen accesses an online form to request benefits, provides the necessary information, and submits their request for processing. Based on the type of transactions the public citizen is requesting and if certain risk-based business rules are true, a list of identity proofing methods will be available for the public citizen to select from. 

    After identity proofing is successfully completed, the request is processed and continues to the next business process activity. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the public citizen should be instructed to visit a local facility for in-person identity proofing and to resubmit the request. 

{:start="2"}
2. **Delegate Requesting Benefits for Another Public Citizen**

    In this use case, the benefit request process is being performed by an individual serving as a delegated authority on behalf of a public citizen with an impairment or who does not have access to online assets. In this scenario, the identity proofing steps are triggered only when certain conditions are true—for example, the amount requested is above a certain limit, previous transactions were flagged, or certain key identity attributes do not match. 

    After the delegate is authenticated and authorized, they will access an online form to provide the necessary information required to request benefits. Based on the type of transactions being requested and if certain risk-based business rules are true, a list of identity proofing methods will be available for the delegate to select from. 

    Both the delegate and public citizen need to perform the identity proofing steps. This ensures that an unauthorized individual is not fraudulently attempting to request funds for a public citizen.

    After identity proofing is successfully completed, the request is processed and continues to the next business process activity. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the delegate should be instructed to visit a local facility for in-person identity proofing and to resubmit the request. 

{:start="3"}
3. **Vendor Requesting Payment for Invoice**

    Federal agencies have experienced significant financial losses due to fraudulent vendor activities and ineffective controls. These incidents can involve vendors submitting large funding requests that are subsequently identified as potential fraud. In some cases, bad actors exploit vulnerabilities by misusing public citizens' personal identifying information to initiate fraudulent claims. Identity proofing helps federal agencies prevent fraud by ensuring only an authorized person is requesting funds. The identity proofing steps are only triggered in this scenario when certain conditions are true—such as if the amount requested is above a certain limit or previous transactions by the vendor were flagged.

    After the vendor is authenticated and authorized, they will access an online form to provide necessary information required to request funds. Based on the type of transactions being requested and if certain risk-based business rules are true, a list of identity proofing methods will be available for the vendor to select from.

    After identity proofing is successfully completed, the request is processed and continues to the next business process activity. If initial identity proofing attempts were unsuccessful, other options should be available. If all identity proofing options failed, then the vendor should be instructed to visit a local facility for in-person identity proofing and to resubmit the request.

### 4. Abnormal Behavior Identity Validation

Abnormal behavior is any behavior that deviates from what is considered normal or typical. It is identified by analyzing a user's behavior to recognize non-standard patterns. Identifying suspicious behavior can help block unauthorized access to an account. Examples of abnormal behavior which could prompt identity proofing to further confirm an individual’s identity include: 

- Multiple failed log in attempts in a short time.   
- Using a new device in a new country.  
- Attempting to log in from a blacklisted country.  
- Devices being used for high-risk transactions--such as requesting benefits for large dollar amounts—from a location that is not the user’s typical one. 

### 5. Access Outside the United States

Country-based access controls or location conditions can help control access from outside of the United States by blocking access from certain countries or regions. However, there are scenarios in which identity proofing can be enabled as an additional authentication for access outside of the US—such as when US citizens live in a foreign country, live on an overseas military facility, or work overseas at a US federal facility and require access to online federal services.

### 6. Risk-Driven Remote Identity Proofing 

Implementing a risk-based approach to remote identity proofing can enable greater adoption of remote-based verification by properly balancing the challenges of accuracy, security, and usability. Federal agencies should look at their remote identity proofing processes to make sure the proper security controls are in place and evaluate whether the organization is striking the right balance between competing challenges of ensuring public citizen identities are sufficiently identity proofed.

Risk-based remote identity proofing approaches commonly look at risk scores created by specialized identity verification services. These scores are generally derived from various attributes about an individual—for example, IP address, geolocation, device, and browser information—which a risk engine analyzes to flag anything suspicious. If nothing appears out of the ordinary, an account can be created with little or no identity proofing required. If the risk score is higher, the individual can be routed to another workflow with additional identity proofing; this may include knowledge-based authentication, document verification with liveness and biometrics, or live chat-based verification.

Taking a risk-based approach to remote identity proofing can save an organization money. Most of these verification systems charge on a per transaction basis, with document verification often the costliest. By taking a risk-based approach and only having individuals over a certain risk score threshold verify their identity documents or liveness, an organization can realize cost savings while also making it generally easier for individuals to create accounts.

## 11. Future Considerations

The following are theoretical ideas for approaches government agencies could take in the future to identity proof citizens (given sufficient technological and process advancements). 

A. **Replace current Social Security card with public PIV card**

  A future identity proofing strategy could involve transitioning from the traditional Social Security card to a more secure, multi-purpose public PIV card. Such a shift would leverage existing federal identity management infrastructure to provide citizens with a more secure, technologically advanced form of personal identification that could streamline access to government services and reduce identity fraud risks.

  ![Figure 14]({{site.baseurl}}/assets/experiments/pid/figure14.jpg)

  1. Public citizen accesses online registration link and searches for a local Social Security office.  
  2. Public citizen visits the federal facility in person.  
  3. Public citizen performs the identity proofing step with a federal employee.  
  4. Public citizen provides documentation such as a US government-issued photo ID or US passport.  
  5. Federal employee uploads live image captured using a camera-enabled device and submits for validation.  
  6. Federal employee issues public PIV card to the registered citizen in lieu of traditional Social Security card after successful verification.  
  7. Public citizen logs in to a federal agency website with their public PIV card.  
  8. Public citizen identity is created with the profile data after successful login.  

B. **Centralized repository of consolidated public identity metadata**

  The following notional approach for more efficient public identity proofing would require consolidating public identity metadata possessed by individual agencies into a single, centralized repository. This would enable individual agencies to identity proof public citizens using more attributes than they could using their agency-owned data alone.

  ![Figure 15]({{site.baseurl}}/assets/experiments/pid/figure15.jpg)

  1. Public citizen accesses online registration link.  
  2. Public citizen enters identity profile data such as First Name, Last Name, Address, Phone, and other relevant attributes.   
  3. Public citizen performs the identity proofing step using federal agency-known public identity data.  
  4. Federal agency-known public identity data is retrieved, and using the key identifier such as Social Security number, name, or home address, a query is sent to the consolidated public identity data repository.   
  5. Random questions are generated from the data and presented to the user.   
  6. Public citizen selects the answers to the random questions and submits them for validation.  
  7. The answers are validated by comparing to the federal agency-known public identity data.  
  8. Public citizen identity is created with profile data after answers to the random questions are successfully validated.

## 12. Conclusion
Identify proofing is essential for safeguarding organizations and citizens against cyber threats in an increasingly digital world. Implementing strong identity-proofing practices not only enhances security but also fosters an environment of trust and authenticity in online interactions. 

As this document has explained, identity proofing is a multifaceted process that combines various methods—including document verification, biometric authentication, and behavioral analysis—to confirm an individual’s identity accurately and securely. By leveraging advanced technologies and adopting multiple verification steps based on the scenarios laid out in this paper, federal agencies can enhance security, prevent fraud, and build trust with US citizens.

## 13. Appendix

### References

1. [https://login.gov/docs/login-gov-roadmap-dec-2024.pdf](https://login.gov/docs/login-gov-roadmap-dec-2024.pdf){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}
2. [https://pages.nist.gov/800-63-3-Implementation-Resources/63A/](https://pages.nist.gov/800-63-3-Implementation-Resources/63A/){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}
3. [https://www.cbpp.org/research/health/remote-identity-proofing-better-solutions-needed-to-ensure-equitable-access](https://www.cbpp.org/research/health/remote-identity-proofing-better-solutions-needed-to-ensure-equitable-access){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}
4. [https://www.voteriders.org/wp-content/uploads/2023/04/CDCE\_VoteRiders\_ANES2020Report\_Spring2023.pdf](https://www.voteriders.org/wp-content/uploads/2023/04/CDCE_VoteRiders_ANES2020Report_Spring2023.pdf){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}
5. [https://www.fdic.gov/household-survey\#:\~:text=An%20estimated%204.5%20percent%20of,the%20survey%20began%20in%202009](https://www.fdic.gov/household-survey#:~:text=An%20estimated%204.5%20percent%20of,the%20survey%20began%20in%202009){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}
6. [https://www.ntia.gov/blog/2024/new-ntia-data-show-13-million-more-internet-users-us-2023-2021](https://www.ntia.gov/blog/2024/new-ntia-data-show-13-million-more-internet-users-us-2023-2021){:target="_blank"}{:rel="noopener noreferrer"}{:class="usa-link usa-link--external"}  