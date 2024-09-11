#Securityplus 
# 1- 10
1. B
2. ~~B~~
3. A
4. D
5. C
6. B
7. ~~A~~
8. ~~C~~
9. C
10. ~~C~~
6/10

2 B is correct 
Valerie wants to use a certificate to handle multiple subdomains for her website, including
the sales.example.com and support.example.com subdomains. What type of certificate should she use?
A. A self-signed certificate
B. A root of trust certificate
C. A CRL certificate
D. A wildcard certificate

Wildcard certificates are used to handle multiple subdomains with a single certificate. A self-signed certificate will not be recognized by browsers and other services, creating confusion for customers. Root of trust certificates and CRL certificates are not types of certificates.

7 C is correct
Log monitoring is an example of what control category?
A. Technical
B. Managerial
C. Operational
D. Physical

Operational controls like log monitoring, change management processes, and vulnerability management are all put in place to support managing and using technology in a secure manner. 

8 D is correct
Rick wants to make offline brute-force attacks against his password file very difficult for
attackers. Which of the following is not a common technique to make passwords harder
to crack?
A. Use of a salt
B. Use of a pepper
C. Use of a purpose-built password hashing algorithm
D. Encrypting password plain text using symmetric encryption

Retaining the actual password is not a best practice, and thus encrypting password plain text is not a common technique to make passwords harder to crack.  Since the application would need the cryptographic key to read the passwords, anybody who had access to that key would decrypt the passwords. Using a salt, a pepper, and a cryptographic hashing
algorithm designed for passwords are all common best practices.

10 B is correct
Sally wants to ensure that her change management process includes a procedure for
what to do if the change fails. What should she create to handle this possibility?
A. An impact analysis
B. A backout plan
C. A regression test
D. A maintenance window

Backout plans document what to do to return to a state prior to the change being made and are designed to be implemented if the change fails. They may involve undoing changes, restoring from backups, or taking other steps and they must contain an appropriate level of detail to ensure that the change can be undone. An impact analysis looks at the potential impact of a change, regression testing ensures that old issues are not introduced in new updates, and maintenance windows are scheduled to allow for downtime or other maintenance activities with appropriate communications, staffing, and other needed elements.

# 11-20
11. D
12. C
13. ~~B~~
14. ~~D~~
15. D
16. ~~D~~
17. A
18. A
19. C
20. A
7/10

13 D is correct
Ben has deployed a data loss prevention (DLP) tool that inspects data and flags specific data
types for review before emails containing it are sent outside the organization. What control
type best describes this type of solution?
A. Managerial
B. Detective
C. Corrective
D. Preventive

This is a preventive control that is intended to prevent sensitive data from being sent outside the organization. Managerial controls are procedural mechanisms, corrective controls remediate security issues that have already occurred, and detective controls identify security events that have already occurred. 

14 A is correct 
What type of control is a policy or procedure?
A. Directive
B. Corrective
C. Detective
D. Preventive

Policies and procedures are examples of directive control that inform employees and others of what they should do to achieve security objectives. Corrective controls remediate already existing security issues, detective controls identify security events that have already happened, and preventive controls attempt to stop a security issue before it occurs.

16 C is correct 
Charles wants to reduce the threat scope of compromised credentials. What type of the following security controls is best suited to meeting this need?
A. Single sign-on
B. Federation
C. Zero trust
D. Multifactor authentication (MFA)

Zero trust designs implement continuous verification, which is an effective control used to limit the threat scope of compromised credentials While MFA can be a useful control in this circumstance, a fully implemented zero-trust design will provide a greater control than just MFA alone. 

# 21-30
21. A
22. ~~A~~
23. B
24. B
25. C
26. B
27. ~~B~~
28. ~~A~~
29. ~~A~~
30. B
6/10

22 C is correct 
Greg wants to implement a version control system to ensure that changes are made in ways
that will not cause problems for his organization’s critical software. Which of the following is
not a common feature of version control systems designed for software source code?
A. Atomic operations
B. File locking
C. Regression testing
D. Tagging and labeling

Version control systems track versions but don't do testing themselves. Atomic operations ensure that actions like commits don't overwrite other commits in progress. File locking allows a developer to check out a file while it is being worked on, and tagging and labeling helps developers track files and versions. 

27 C is correct 
What hardware component is used to generate, store, and manage cryptographic keys?
A. A CPU
B. A NSA
C. A TPM
D. A CCA
A TPM stands for a trusted platform module, and it is a cryptographic processor that is used to generate, store, and manage cryptographic keys. CPU is a CPU, NSA is national security agency, and a CCA is a chosen ciphertext attack.

28 D is correct
Chris wants to check to see if a certificate has been revoked. What protocol can he use to
validate the current status of a certificate?
A. TLS
B. OCRS
C. SSL
D. OCSP
The online certificate status protocol (OCSP) is used to validate certificate status, including checking to see if the certificate is on a certificate revocation list (CRL). TLS is Transport layer security, SSL is outdated and is often used to refer TLS of which both are incorrect. 

29 B is correct
Brian’s organization uses a process where a secure module boots systems, then monitors them
as each boot stage proceeds. It validates each signed boot stage and reports on whether the
boot process was correct or not when complete. What is the secure module used to verify
these stages called?
A. A secure initiation manager
B. A root of trust
C. A boot hash
D. A cryptographic boot manager

A root of trust-based secure boot process validates each signed component as it starts and ensures that the entrusted components are all loaded as part of the boot process. Secure initiation manager, boot hash, cryptographic boot manager were made up for this question.

# 31 - 40
31. ~~A~~
32. ~~B~~
33. A
34. C
35. C
36. B
37. ~~C~~
38. ~~B~~
39. C
40. ~~B~~
5/10

31 C is correct
Jason knows that his Apple system uses a separate portion of its SoC (system on chip) to
store keys and biometric information. What is this specialized component called?
A. A TPM
B. A HSM
C. A secure enclave
D. A screened subnet
The device it uses is called a security enclave. This is distinct from a TPM or HSM, and a screened subnet is a networking concept.

32 A is correct
What change management term is used to describe the processes that an organization uses
for each change that is made to ensure that a consistent process is used?
A. Standard operating procedures
B. A change plan
C. Fixed operating procedures
D. A backout plan
Standard Operating Procedures (SOP) is an organizations normal processes that it uses.

37 B is correct
Renee wants to ensure that her logs support nonrepudiation. What should she do to
ensure this?
A. Encrypt, then hash the logs.
B. Hash the logs and then digitally sign them.
C. Digitally sign the log file, then encrypt it.
D. Hash, then encrypt the logs.
Calculating a cryptographic hash allows the log's hash to be compared against copies to validate that they match. Digitally signing the hash ensures that it can be verified to be the original. Encrypting does not allow verification. Without verification nonrepudiation is not satisfied. 

38 A is correct
Isaac wants to deploy sensors to detect intruders in a facility, but he is concerned about the
sensors being overly sensitive. What type of sensor is best suited to detecting intruders in an
open office environment without significant expense or issues with sensitivity?
A. Infrared
B. Pressure
C. Microwave
D. Ultrasonic
Infrared sensors are commonly used in open spaces. They are well suited to detecting individuals and are less likely to be overly sensitive.

40 D is correct
What are considerations like database and network connectivity, authentication system
access, and network time availability considered in the context of change management
processes?
A. Allowed services
B. Standard operating procedures
C. Denied services
D. Dependencies
Database and network connectivity, authentication system access, and network time availability are all common dependencies that must be considered when making changes. Applications and services may fail to start properly if these dependencies are not available when they attempt to start.

# 41 - 50
41. ~~C~~
42. D
43. ~~C~~
44. D
45. ~~B~~
46. B
47. ~~D~~
48. ~~B~~
49. C
50. D
5/10

41 B is correct
What role does the policy engine play in a zero-trust environment?
A. It creates new administrative policies based on user behavior.
B. It grants access based on policies created by administrators and based on security systems data.
C. It enforces policies by monitoring connections between clients and servers.
D. It suggests new administrative policies based on usage patterns for adoption by the
organization.
Policy engines decide whether to grant access to resources based on policies created by administrators and based on the data provided by tools like endpoint detection and response tools, threat intelligence feeds, and security information and event management tools. It does not create or suggest administrative policies, and it does not directly enforce policies - that occurs at a policy enforcement point, typically through a zero-trust agent on the client and at the resource or service side.

43 B is correct
Which of the following activities should Alaina not restrict as part of her preparation for a
change window?
A. Patching
B. Scaling clustered systems up or down
C. Changing hostnames
D. Modifying database configurations
Change windows rely on the documented change being able to be made. Patching and other technical changes may lead to unexpected interactions or dependency changes that are not accounted for in the original change window.

45 A is correct
Damian issues the following command on his Linux server:
openssl req -new -newkey rsa:2048 -nodes -keyout exampleserver.
key -out exampleserver.csr
What has he done?
A. Created a certificate signing request
B. Created a certificate revocation request
C. Signed a certificate signing request
D. Updated the OCSP record for a certificate
Damian has created the certificate signing request, which he can submit to a certificate authority.

47 B is correct
Megan wants to assess the impact of a change as part of her change management process.
Which of the following is most likely to help her assess impact?
A. A backout plan
B. An estimate of the downtime expected
C. A list of stakeholders
D. A list of dependencies for impacted systems
An estimate of the downtime expected as part of the change will help Megan to assess the impact of the change on her organization's business operations. A backout plan is useful if something goes wrong and can help estimate impact if that happens, but it does not identify impact under normal circumstances. A list of stakeholders can help when communicating with stakeholders to notify them of what will occur, but without the estimate of downtime, Megan will not be able to ask them what the impact would be. Finally, a list of dependencies is helpful to ensure that the change does not have unexpected issues and can help with the impact assessment to determine if other systems may impacted, but the downtime expected remains the most important item.

48 C is correct
Jared wants to estimate the downtime that will result as part of a planned change. Which of the following methods will most effectively help him estimate downtime?
A. Average the downtime from other recent changes.
B. Contact the vendor for time estimates for the change.
C. Perform the change in a test environment.
D. Use a fixed maintenance window.
Organizations often perform changes in a test environment to allow accurate time estimates and to determine if there are issues with the change like an undocumented dependencies or problems with patches. Average downtime is a poor indicator of what a specific change may require, a fixed maintenance window does not ensure the change will take that amount of time, and vendors rarely have a full understanding of the environment an organization is operating in.

# 51 - 60
51. A
52. A
53. C
54. ~~C~~
55. C
56. ~~A~~
57. C
58. B
59. C
60. C
8/10

54 B is correct
What technology is record-level encryption most commonly associated with?
A. Stored audio files
B. Databases
C. Physical disks
D. Removable storage
Record level encryption is commonly associated with databases, where it is used to encrypt each record with a unique encryption key, allowing it to be more secure than database-level encryption.

56 B is correct
Valerie wants to authenticate her systems using her AAA system. Which of the following
options is best suited to system authentication?
A. Asymmetric authentication
B. Certificate-based authentication
C. Symmetric authentication
D. PIN-based authentication
Certificates are commonly used for system authentication in AAA systems. While asymmetric and symmetric are forms of encryption, they are not authentication schemes, and PIN based authentication is not commonly used for system authentication. 

# 61-70
61. ~~A~~
62. C
63. C
64. A
65. B
66. A
67. A
68. C
69. ~~A~~
70. B
8/10

61 B is correct
Joanna’s organization has a policy that requires a user’s password to be immediately reset to lock accounts if the account is determined to have been successfully phished. What type of control is this?
A. A detective control
B. A directive control
C. A compensating control
D. A preventive control

Policies are examples of directive controls. This could be considered a corrective control, but that is not one of the options listed. Detective controls identify security events that have already occurred, and this does not detect the compromised account -it directs what must happen afterward. A compensating control mitigates risks due to exceptions in the security policy like a violation of policy due to an instability to implement a specific technical control like patching. 

69 C is correct
Theresa wants to use a cloud-hosted security solution that will allow her to safely store and manage secrets. What type of solution should she select?
A. A TPM
B. A CA
C. A KMS
D. A CSR

A KMS, or key management system, is a solution that allows you to safely store and manage secrets like keys and certificates. Centralizing a KMS allow organizations to effectively manage their secrets, including tracking their life cycle and rotation. A TPM is used for hardware security on physical systems, a CA is a certificate authority used to create and sign certificates, and a CSR is a certificate signing request.

# 71-80
71. A
72. ~~D~~
73. B
74. ~~A~~
75. ~~A~~
76. C
77. B
78. A
79. C
80. ~~D~~
6/10\


72 B is correct
What role does a subordinate CA have in a CA hierarchy?
A. Subordinate CAs issue certificates based on subdomains.
B. Subordinate CAs provide control over certificate issuance while avoiding the cost of
being a root CA.
C. Subordinate CAs validate root CA activities to ensure auditability.
D. Subordinate CAs review certificate signing requests before forwarding them to the
root CA.

Subordinate CAs avoid the cost of maintaining a root CA while providing control over certificates that are issued and allowing specialized support for different types of certificates like SSL and S/MIME

74 D is correct
Which of the following is not a managerial control?
A. Risk assessments
B. Including security in change management processes
C. Security planning exercises
D. Implementing firewalls

Firewalls are technical control, not a managerial control that focuses on the mechanics of the risk management process

75 C is correct
What purpose do third-party certificates serve for customers of cloud services?
A. They reduce costs by using bring-your-own certificates.
B. They allow certificates for domains other than the service provider’s domain.
C. They provide control over cryptographic security for the customer.
D. They allow more flexibility in TLS version selection.

Third party certificates allow customers to have full control over the certificate, including the private key and certificate signing request. By bringing your own certificate, encrypted traffic cannot be decrypted by the cloud provider. Using provider-provided, or -created certificates leads to a potential risk if the provider is malicious or compromised and private keys managed by the provider are compromised. Bringing your own certificate does not necessarily reduce costs. Providers typically allow certificate signing requests for customer domains and subdomains as needed and supported by the service.

80 B is correct
Jill needs to explain the concept of open public ledgers to her organization as management wants to adopt a blockchain-based system. What should she tell them about access to the ledger?
A. Members must be added by a vote of all current members.
B. Anyone can join at any time.
C. Members must be added by a vote of more than 51 percent of current members.
D. Ledgers are public but membership is private and controlled by the creator of the ledger

Open public ledgers are open and public - anyone can join at any time. No vote is required, and creators do not control the ledger once it is made public.

# 81-90 
81. ~~D~~
82. C
83. B
84. A
85. D
86. B
87. ~~C~~
88. D
89. C
90. B
8/10

81 A is correct
Olivia wants to use a self-signed certificate in her test environment for her organization’s services to save money on commercial certificates. What warning should her team give her about the use of self-signed certificates in a test environment?
A. Certificate root of trust validation attempts will fail if implemented.
B. Self-signed certificates cannot be used for external users to support SSL.
C. Self-signed certificates cannot be used for internal users to support SSL.
D. Browsers will not allow self-signed certificates to be used when browsing sites

Some software may attempt to validate the certificates in use and could fail. This may also lead to unexpected differences between production certificates and test certificates, which is undesirable in a test environment intended to mirror production. 

87 D is correct
Certificates expire, but expiration does not place them on a CRL. 

# 91-100
91. A
92. ~~C~~
93. A
94. B
95. ~~C~~
96. C
97. B
98. B
99. ~~D~~
100. ~~D~~
6/10

92 D is correct
Mikayla’s zero-trust system has received a request for access with an identity, and the basic
criteria for access have been met. What should the system do next before providing access to
the resource requested?
A. Check the remote system’s security status.
B. Require reauthentication using MFA.
C. Check the user’s rights to ensure they can access the resource.
D. Determine its level of confidence in the request.

A zero trust system should validate its level of confidence in a request that it receives once the basic criteria have been met. This may involve checking the access against known patterns of access by the user, validating current threat feed information, or checking other details that will help ensure the security and authenticity of the request.

95 B is correct
What operating system is commonly associated with secure enclaves?
A. Windows
B. iOS
C. Linux
D. Android

Secure enclaves are used by apple and require iOS machines.

99 B is correct
Which of the following is not a common factor in adaptive authentication for zero trust?
A. Where the user is logging in from
B. Whether the user has logged in recently from another device
C. What device the user is logging in from
D. If the device is configured correctly

Adaptive authentication looks at the context of a login, including where they're logging in from - both geographically, and from a network trust perspective, what device they're logging in from, and if the device is configured correctly. In modern usage whether the user has logged in recently from a another device isn't as likely to be considered, but if the devices were in different countries it would likely raise a flag.

100 A is correct
Juan’s organization is designing their zero-trust model. Which of the following statements is true for network security zones?
A. All communication is secured, regardless of the network security zone it occurs in.
B. Communication receives additional security in low-trust zones.
C. Communication receives less security in high-trust zones.
D. All zero-trust networks are considered secured zones.

One of the basic tenets of zero-trust architecture is that all communication is secured, regardless of the security zone or trust zone that it occurs in. All zero trust networks are considered potential risk areas - thus the zero in zero trust.

# 101-110
101. C
102. C
103. ~~A~~
104. B
105. D
106. B
107. ~~C~~
108. B
109. ~~D~~
110. C
7/10

103 B is correct
Rachel wants to select an obfuscation method that will allow her customer service representatives to validate customer identities without providing full access to customer data. What
should she select?
A. Tokenization
B. Data masking
C. Steganography
D. Hashing

Data masking reveals only part of a field and is often used with details like credit card numbers or social security numbers where only the last four digits will be revealed for validation purposes.

107 D is correct
Michelle wants to store secrets for her organization in a cloud service. She wants to ensure
the greatest level of security for her organization, and she is willing to spend more money
to provide that security. What solution should she look for?
A. A shared cloud TPM
B. A shared cloud HSM
C. A dedicated hardware cloud TPM
D. A dedicated hardware cloud HSM

A dedicated hardware cloud hardware security module HSM would be the correct choice as it is better than cloud while a TPM is used for secure booting and related services, not for security.

109 C is correct
What information is necessary for a certificate to be identified properly in an OCSP
request?
A. The domain name
B. The original requestor’s name
C. The certificate’s serial number
D. The identifier for the open public ledger entry

OCSP requests must include the certificate's serial number to allow the ocsp responder to check the CA database for the certificate and its status. It does not require the domain name or requestor's name. 

# 111-120
111. A
112. A
113. C
114. C
115. A
116. 