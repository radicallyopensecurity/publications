# ROS Access Control Policy

## 1. Purpose

To ensure that access controls are implemented and in compliance with IT security policies, standards, and procedures. 

## 2. Policy

This policy is applicable to all users of Radically Open Security’s (ROS) resources and assets.

## 2.1 Account management

### 2.1.1. Introduction

Describe identity provider 

### 2.1.2. Overview 

Definitions of user types, groups and permissions based on role (RBAC).


a. The Infrastructure Team shall identify and select the following types of information system accounts to support organizational and business functions:

**EyeDP Administrators**: A user with administrative permissions. A user becomes an administrator when they're added to a group that has the admin flag enabled, which can be done in the admin UI by an administrator. An administrator has no restrictions on the actions that they can perform, so should be a small group of users. An administrator account is needed to change membvership in administrator and operator groups, as well as creating and managing these group types.

**EyeDP Managers**: A user with manager permissions. A manager is a type of user that can manage users and groups, but cannot manage EyeDP. A user becomes a manager when they're added to a group that has the manager flag enabled, which can be done in the admin UI by an administrator. A manager cannot add or remove a user from an operator or administrator group, nor change those flags on other groups. A manager user can add and remove additional managers.

**EyeDP Operators**: A user with operator permissions. An operator is a type of user that can manage EyeDP itself, but cannot manage users or groups. A user becomes an operator when they're added to a group that has the operator flag enabled, which can be done in the admin UI by an administrator. In this context, managing EyeDP means that an operator can manage SSO applications such as OpenID Connect and SAML applications. In additional, they can change EyeDP's settings, such as key data for the IdP, hostnames, and templates.

**The infrastructure team shall:**

b. Assign account managers for information system accounts:

The infrastructure team assigns ROS project managers with permissions for a manager role. As such, project managers can create accounts for staff and clients. The project managers can not create an administrative account for infrastructure team members. This can only be done by someone with an administrator role.

c. Establish conditions for group and role membership:

EyeDP has the following groups: Staff, access-tokens, test-email-group, services, pge (post-growth entrepreneurship), npv (non-profit ventures), npv-mail, postmaster, admin, reviewfacility, reviewfacility-service, rosbot, staging, staging-mail, staging-services, pm and users. Staff that needs access to e.g. the PGE and NPV environments will get a separate user account with access to the these groups. To ensure adequate separation there are also groups for staging and other groups.

d. Specify authorized users of the information system, group and role membership, and access authorizations (ie,privileges) and other attributes (as required) for each account:

- Infrastructure team members have a regular account that belongs to the staff and users group. For infrastructure work there is a separate account with their username + adm in EyeDP and belong to the following groups: staff, admin and administrators
- Project managers belong to the following groups: staff, pm and users.
- Pentesters belong to the following groups: staff, users.
- Clients belong to the following group: users

e. Require approvals by system owners for requests to create information system accounts.

f. Create, enable, modify, disable, and remove information system accounts in accordance with approved procedures.

g. Monitor the use of information system accounts.

h. Notify account managers when accounts are no longer required, when users are terminated or transferred, and when individual information system usage or need-to-know changes.

i. Authorize access to the information system based on a valid access authorization or intended system usage.

j. Review accounts for compliance with account management requirements [entity defined frequency].

k. Establish a process for reissuing shared/group account credentials (if deployed) when individuals are removed from the group.

l. Employ automated mechanisms to support the management of information system accounts.

m. Ensure that the information system automatically disables temporary and emergency accounts after usage.

n. Ensure that the information system automatically disables inactive accounts after [entity defined frequency]

o. Ensure that the information system automatically audits account creation, modification, enabling, disabling, and removal actions, and notifies appropriate IT personnel.

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

From our information security policy: We have ‘Chinese walling’ in place. E.g. not every pentester has access to every assignment. Client information and details are shared on need to know basis with staff members. 

### 2.5 Least privilege

The Infrastructure Team shall:

a. Employ the principle of least privilege, allowing only authorized accesses for users (or processes acting on behalf of users) which are necessary to accomplish assigned tasks in accordance with organizational missions and business functions.

b. Authorize explicitly access to hardware and software controlling access to systems and filtering rules for routers/firewalls, cryptographic key management information, configuration parameters for security services, and access control lists.

c. Require that users of information system accounts, or roles, with access to GitLab, RocketChat or GitHub, use non-privileged accounts or roles, when accessing non-security functions.

d. Restrict privileged accounts on the information system to infrastructure team members and the CISO (Melanie Rieback).

e. Ensure that the information system audits the execution of privileged functions.

f. Ensure that the information system prevents non-privileged users from executing privileged functions to include disabling, circumventing, or altering implemented security safeguards/countermeasures.

From our information security policy: When we onboard new infrastructure team members, pentesters and project managers they all start with reduced access to our systems and channels and gradually get more access over time. We use role-based access control (e.g. Ansible base roles) managed via SSO / SAML across multiple systems.

### 2.6 Unsuccessful logon attempts

The Infrastructure Team shall ensure that the information system:

a. Enforces a limit of 10 attempts of consecutive invalid logon attempts by a user. See: https://github.com/CentauriSolutions/EyeDP/blob/main/config/initializers/devise.rb#L207

b. Locks the account automatically after 24 hours or an email from the user when the maximum number of unsuccessful attempts is exceeded. See: https://github.com/CentauriSolutions/EyeDP/blob/main/config/initializers/devise.rb#L203 

### 2.7 Session lock

a. At Radically Open Security our team adhere to best practice security standards. Whilst this is a given for the pentesters and infrastructure team, our project managers and other on-technical staff are instructed to adhere to basic digital security practices as well. Project managers will lock their screen when working from home (with others present) and when they are working from an office or cafe.

b. There is no unlock strategy. Users can set timeout in EyeDP via a configurable amount. The user should handle unlocking by themselves. There's no default on it so it's set per-installation. See: https://github.com/CentauriSolutions/EyeDP/blob/main/config/initializers/devise.rb#L203 . 

### 2.8 Session termination

The Infrastructure Team shall:

a. Ensure that the information system automatically terminates a user session after 168 hours.

### 2.9 Remote access (SSH)

a. Connections are routed through one managed access control point, i.e. the VPN APU running Wireguard. Once you have root access as an infra member, you can perform all privileged commands on all the infrastructure and access all the data without restriction.

b. Establish and document usage restrictions, configuration/connection requirements, and implementation guidance for each type of remote access allowed.

c. Authorize remote access to the information system prior to allowing such connections.

d. Ensure that the information system monitors and controls remote access methods.

e. Authorize the execution of privileged commands and access to security-relevant information via remote access only for infra administrators

f. Document the rationale for such access in the security plan for the information system.

### 2.10 Wireless access

ROS doesn't have a physical office thus is not operating wireless networks.

### 2.11 Access control for mobile devices

ROS doesn't have mobile devices for staff. If work-related actions are performed on a staff members personal mobile device such as accessing chat, we enforce 2FA as well as best practice recommendations on locking their devices with an adequate passcode as well as security recommendations on password management for ROS services.

### 2.12 Use of external information systems

The Infrastructure Team shall:

a. Establish terms and conditions, consistent with any trust relationships established with other organizations owning, operating, and/or maintaining external information systems, allowing authorized individuals to:

i. Access the information system from external information systems.

ii. Process, store, or transmit organization-controlled information using external information systems.

b. Permit authorized individuals to use an external information system to access the information system or to process, store, or transmit organization-controlled information only when the organization:

i. Verifies the implementation of required security controls on the external system as specified in the organization’s information security policy and security plan.

ii. Retains approved information system connection or processing agreements with the organizational entity hosting the external information system.

### 2.13 Information sharing

The Infrastructure Team shall:

a. Facilitate information sharing by enabling authorized users to determine whether access authorizations assigned to the sharing partner match the access restrictions on the information for sharing circumstances where user discretion is required. In general, we adhere to Chinese walling principles.

b. If an incident response request comes in we keep the information we share in e.g. the ros-assignment channel to an absolute minimum to ensure we protect client confidentially. A mutual NDA is sent by the client and us whilst the project managers keep the details we share to a minimum. Only when the project is staffed these details can be shared.

### 2.14 Publicly accessible content

a. We only publish certain pentest reports depending on the assignment and only with prior approval of client as well as our public GitHub repositories.

b. Designate individuals authorized to post information onto a publicly accessible information system.

## 3. Policy exceptions

Requests for exceptions to this policy shall be reviewed by ROS' Chief Information Security Officer (CISO) (Melanie Rieback) and the infrastructure team project manager (Deborah Meibergen). Departments requesting exceptions shall provide such requests to the CISO and project manager. The request should specifically state the scope of the exception along with justification for granting the exception, the potential impact or risk attendant upon granting the exception, risk mitigation measures to be undertaken by the Infrastructure Team, initiatives, actions and a time-frame for achieving the minimum compliance level with the policies set forth herein. The CISO and infrastructure project manager shall review such requests.

## 4. Responsible entities

The CISO, infrastructure team including the infrastructure project manager.

## 5. Version

| Version | Date | Author | Rationale | Details |
| ------ | ------ | ------ | ------ | ------ |
