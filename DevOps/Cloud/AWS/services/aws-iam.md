# AWS Identity and Access Management (IAM)

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ac593bfc-69cb-4fb6-a7d1-efe3d3e0ab63">
</p>

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. Use IAM; to control who is authenticated (logged in) and authorized (has permissions) to use resources.

When you create an AWS Account, you start with a login identity that has full access to all AWS resources and Services in the account. This identity is given the AWS Account root user name and is accessed by logging in with the email and password you used to create the account. We recommend that you do not use the root user for everyday tasks. Protect the root user credentials and use them only for tasks that the root user can perform. For a complete list of tasks that require you to log in as the root user, see Tasks that require root user credentials in the AWS Account Management Reference Guide.

It is basically recommended to generate the configurations on the users by means of the groups, we configure them, and associate the users to the mentioned groups, this facilitates the management when a user is removed or is moved from one position to another. 

In addition to this, it is recommended to configure the multifactor authentication for the root account, and even when starting it is recommended not to use the root account but to configure an administrator type user to carry out the pertinent managements, this is fundamental since it can be parameterized, with the exception of the root user. 

## Characteristics of IAM

To help control access and manage identities for your AWS account, IAM offers many features to ensure security.

- IAM is global and is not region-specific. You can view and use IAM settings from any region in the AWS Management Console.
- IAM is integrated into many AWS services by default.
You can set password policies in IAM to specify complexity requirements and mandatory rotation periods for users.
- IAM supports MFA.
- IAM supports federated identity, which allows users who already have passwords elsewhere (e.g., on your corporate network or with an Internet Identity Provider) to gain temporary access to your AWS account.
Any AWS customer can use IAM; the service is offered at no additional charge.

## Users of IAM

An IAM user represents the person or service that interacts with AWS. You can define the user for your AWS account. Your account is billed for any activity performed by that user. Once a user is created, that user can log in to access AWS resources in your account.

You can also add more users to the account as needed. For example, for your cat photo application, you could create individual users in your AWS account that correspond to the people who are working on your application. Each person should have their own login credentials. Providing users with their own login credentials prevents credentials from being shared.

## Roles of IAM

Maintaining roles is more efficient than maintaining users. When you assume a role, IAM dynamically provides temporary credentials that expire after a defined period, between 15 minutes and 36 hours. Users, on the other hand, have long-term credentials in the form of username and password combinations, or a set of access keys.

User access keys expire only when you or the account administrator rotates the keys. User login credentials expire if you apply a password policy to your account that forces users to rotate passwords.

## Identity providers (IdP)

If you decide to turn your cat photo application into a business and start having more than a few people working on it, consider managing employee identity information through an identity provider (IdP). Using an IdP, whether it's an AWS service such as AWS Single Sign-On or a third-party identity provider, provides a single source of information for all identities in your organization.

You no longer have to create separate IAM users in AWS. Instead, you can use IAM roles to provide permissions to your IdP's federated identities. For example, there is an employee, Martha, who has access to multiple AWS accounts. Instead of creating and managing multiple IAM users named "Martha" in each of those AWS accounts, you could manage Martha in your company IdP. If Martha moves to another position in the company or leaves the company, she can be updated in the IdP, rather than in all of the company's AWS accounts.

If you have an organization that spans many employees and multiple AWS accounts, you may want your employees to sign in with a single credential.

AWS SSO is an IdP that allows users to sign in to a user portal with a single set of credentials. It then provides users with access to their assigned accounts and applications in a central location.

It is similar to IAM. AWS SSO provides a directory where you can create users, organize them into groups, set permissions on all groups, and grant access to AWS resources. However, AWS SSO has some advantages compared to IAM. For example, if you use a third-party IdP, you can synchronize your users and groups with AWS SSO. This eliminates the burden of recreating users that already exist elsewhere and allows you to manage users from your IdP. Most importantly, AWS SSO separates tasks between your IdP and AWS, ensuring that cloud access management is not in or dependent on the IdP.

## User credentials of IAM

An IAM user consists of a name and a set of credentials. When you create a user, you can provide it with the following types of access:

- Access to the AWS Management Console.
- Programmatic access to the AWS Command Line Interface (AWS CLI) and the AWS Application Programming Interface (AWS API).

To access the AWS Management Console, provide the user with a user name and password. For programmatic access, AWS generates a set of access keys that can be used with the AWS CLI and the AWS API. IAM user credentials are considered permanent, meaning they stay with the user until administrators do a forced rotation.

When you create an IAM user, you can grant permissions directly at the user level. This may seem like a good idea if you only have one or a few users. However, as the number of users increases, keeping up with permissions can become more complicated. For example, if you have 3000 users in your AWS account, it can be a challenge to manage access and get an overview of who can perform what actions on which resources.

If only there was a way to group IAM users and instead attach permissions at the group level. Guess what? There is.

## Groups of IAM

An IAM group is a collection of users. All users in the group inherit the permissions assigned to the group. This allows you to grant permissions to multiple users at once. It is a more convenient and scalable way to manage permissions for users in your AWS account. This is why it is a best practice to use IAM groups.

If you are trying to build an application and there are multiple users in an account working on the application, you can organize them by job role. For example, you can organize IAM groups by developers, security, and administrators. You can then place all IAM users into their respective groups.

This provides a way to see who has what permissions in your organization. It also helps you to escalate when new people join or leave, and when they change roles in your organization.

Consider the following examples:

- A new developer joins your AWS account to help you with your application. You create a new user and add them to the developer group, without thinking about what permissions they need.
- A developer changes jobs and becomes a security engineer. Instead of editing the user's permissions directly, you remove them from the old group and add them to the new group that already has the correct level of access.

Please note the following characteristics of groups:

- Groups can have many users.
- Users can belong to many groups.
- Groups cannot belong to groups.

The root user can perform all actions on all resources in an AWS account by default. This is in contrast to creating new IAM users, new groups, or roles. New IAM identities cannot perform actions on your AWS account by default until you explicitly grant them permission.

The way you grant permissions in IAM is through IAM policies.

## Policies of IAM

To manage access and provide permissions to AWS services and resources, you create IAM policies and attach them to IAM users, groups, and roles. Each time a user or role makes a request, AWS evaluates the policies associated with them. For example, if there is a developer in the developer group requesting an AWS service, AWS evaluates the policies attached to the developer group and the policies attached to the developer user to define whether the request should be allowed or denied.

## References
- https://docs.aws.amazon.com/en_en/IAM/latest/UserGuide/introduction.html
