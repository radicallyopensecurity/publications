
# Access Control Policy

# Introduction

This generalized version of an access control policy, and serves as an example to ensure all measures and processes are captured adequately.

## 1. Purpose

To ensure that access controls are implemented and in compliance with IT security policies, standards, and procedures. 

## 2. Policy

This policy is applicable to all users of [company] resources and assets.

## 2.1 Account management

### 2.1.1. Introduction

Describe identity provider 

### 2.1.2. Overview 

Describe definitions of user types, groups and permissions based on role (RBAC). The Infrastructure Team shall:

a. Assign account managers for information system accounts:

b. Establish conditions for group and role membership:

c. Specify authorized users of the information system, group and role membership, and access authorizations (ie,privileges) and other attributes (as required) for each account:

d. Require approvals by system owners for requests to create information system accounts.

e. Create, enable, modify, disable, and remove information system accounts in accordance with approved procedures.

f. Monitor the use of information system accounts.

g. Notify account managers when accounts are no longer required, when users are terminated or transferred, and when individual information system usage or need-to-know changes.

h. Authorize access to the information system based on a valid access authorization or intended system usage.

i. Review accounts for compliance with account management requirements [entity defined frequency].

j. Establish a process for reissuing shared/group account credentials (if deployed) when individuals are removed from the group.

k. Employ automated mechanisms to support the management of information system accounts.

l. Ensure that the information system automatically disables temporary and emergency accounts after usage.

m. Ensure that the information system automatically disables inactive accounts after [entity defined frequency]

n. Ensure that the information system automatically audits account creation, modification, enabling, disabling, and removal actions, and notifies appropriate IT personnel.

### 2.2 Access enforcement

The Infrastructure Team shall:

a. Ensure that the information system enforces approved authorizations for logical access to information and system resources in accordance with applicable access control policies.

### 2.3 Information flow enforcement

The Infrastructure Team shall:

a. Ensure that the information system enforces approved authorizations for controlling the flow of information within the system and between interconnected systems based on applicable policy.

### 2.4 Separation of duties

The Infrastructure Team shall:

a. Separate duties of individuals as necessary, to prevent malevolent activity without collusion.

b. Document the separation of duties of individuals.

c. Define information system access authorizations to support separation of duties.

### 2.5 Least privilege

The Infrastructure Team shall:

a. Employ the principle of least privilege, allowing only authorized accesses for users (or processes acting on behalf of users) which are necessary to accomplish assigned tasks in accordance with organizational missions and business functions.

b. Authorize explicitly access to hardware and software controlling access to systems and filtering rules for routers/firewalls, cryptographic key management information, configuration parameters for security services, and access control lists.

c. Require that users of information system accounts, or roles, with access to key infrastructure, use non-privileged accounts or roles, when accessing non-security functions.

d. Restrict privileged accounts on the information system to infrastructure team members and the CISO 

e. Ensure that the information system audits the execution of privileged functions

f. Ensure that the information system prevents non-privileged users from executing privileged functions to include disabling, circumventing, or altering implemented security safeguards/countermeasures


### 2.6 Unsuccessful logon attempts

Describe what measures are in place around unsuccessful login attempts

### 2.7 Session lock

Describe screen locking when working from home (with others present) and when they are working from an office or cafe.

### 2.8 Session termination

Describe when the information system automatically terminates a user session, including x hours.

### 2.9 Remote access (SSH)

Describe remote access and connections requirements

### 2.10 Wireless access

Describe wireless access

### 2.11 Access control for mobile devices

Describe access controls mobile devices

### 2.12 Use of external information systems

Describe terms and conditions and details on how to use external information systems

### 2.13 Information sharing

Describe information sharing measures and process

### 2.14 Publicly accessible content

Describe where content is stored, who can assess it 

## 3. Policy exceptions

Requests for exceptions to this policy shall be reviewed by ROS' Chief Information Security Officer (CISO) and the infrastructure team project manager. 
The request should specifically state the scope of the exception along with justification for granting the exception, the potential impact or risk upon 
granting the exception, risk mitigation measures to be undertaken ensring compliance with the policies set forth herein. 

## 4. Responsible entities

Describe responsible entities

## 5. Version

| Version | Date | Author | Rationale | Details |
| ------ | ------ | ------ | ------ | ------ |
| 0.1 - 0.8 | Feb - May 2022 | Deborah | Draft policy from scratch | Resources used: [NIST](https://csrc.nist.gov/Projects/Access-Control-Policy-and-Implementation-Guides)
| 1.0 | May 2022 | Deborah | Updated with input infra team | [issue]
