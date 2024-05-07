# IAM

### IAM Users & Groups

IAM is a global service

Root account is the default account, security best practices is to create an IAM group + user for priv management

Users can be grouped and can be part of multiple groups

Groups only contain users not other groups

Users dont have to be apart of groups

<img width="414" alt="image" src="https://github.com/UpheldSmile/Virtual-Network/assets/49825639/6ad31eb7-8d51-4745-b79e-8a7fe898bb5f">

### IAM Hands-on

Is configured in Identity and Access Management (IAM)

You can specify users in Identity Center which is recommended - however there is another option which allows

<img width="325" alt="image" src="https://github.com/UpheldSmile/Virtual-Network/assets/49825639/da5c1b5a-f0e7-42a8-bdc5-7d99ec4e08e8">

You then can add them to a group and add a policy to that particular user.

Then you can add tags > e.g adding a user to a department

You can add policies to groups, a lot more easier to manage as they inherit permissions from that group rather than individual perms.

## Permissions

Users or groups can be assigned an IAM policy via a JSON document, it defines permissions for users > make sure to follow least privilege principle.

<img width="446" alt="image" src="https://github.com/UpheldSmile/Virtual-Network/assets/49825639/936d2a8f-7c40-45dd-970d-183b2ff94ca3">

## IAM Policies indepth

<img width="440" alt="image" src="https://github.com/UpheldSmile/Virtual-Network/assets/49825639/8d086bd6-ed1c-4e2f-a84b-33a7adba1c30">

In the screenshot - we can see Alice, Bob, and Charles are apart of the 'Developers' group and therefore will have the assigned policy however Charles is also part of the 'Audit team' so therefore will inherit both group policies. We see Fred is not part of any group but can have their own inline policy

### Policy structure

Consists of:
- the version always will be 2012-10-17
- Id: an identifier for the policy (optional)
- Statement: one or more individual statements (required)

Statements consist of:
- Sid: Identifier of statement (Optional)
- Effect: Allow or Deny - self explanatory
- Principal: Accout/user/role to which this policy applies to
- Action: list of actions the policy allows or denies
- Resource: Which AWS resource it applies to
- Condition: Is optional - conditions for when this policy is in effect
- <img width="182" alt="image" src="https://github.com/UpheldSmile/Virtual-Network/assets/49825639/920bbed3-655f-4f63-a139-49b824eaa0c8">

