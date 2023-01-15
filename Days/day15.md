# **Broken Object Level Authorization**

It's all about **bypassing** the **authorization** check and access data elements they should not be allowed to us. for example when an application offers "object level" access control. IOW, certain users are only granted access to certain objects (e.g., customer records). If an attacker is able to use the application's API in such a way that they can manipulate the objects being returned, then they would be able to bypass this authorization control and gain unauthorized access to the restricted data.

**Access control** and **Authorization** are two components of **web application security** that are often used to ensure that only users who are authorized to access a particular resource can do so. Access control is the process of enabling or disabling access to a given resource based on the user's identity. Authorization is then the process of deciding what level of access should be provided for a given user, based on their identity and/or role. In essence, the authorization process determines what a user can, and cannot do within the system.

For example, let's say MR X wants to login to a sales data system used by his company:

- Access Control would verify that X has access privileges to use this system. It will check his identity (e.g. username and password) before granting him access to the system itself.
- Authorization will then determine if X has permission to view or edit specific data within that system he's been given access too (such as his sales figures). This might be based on where he works in the company or what role he holds - i.e., Sales Manager or Regional Director, etc.

- Access control is the process of limiting and controlling access to a web app by providing authentication to users before allowing them access. It is primarily used to keep malicious or unauthorized users out of a secure environment.
- Authentication is the process of verifying an individual’s identity before granting permission to access a web app.

# Types of Broken Object Level Authorization

- **ID-Based Authorization**: This type of authorization is based on the unique ID that each user has within the system. For example, different levels of access to confidential information can be granted to personnel based on their ID numbers.
    - `https://example.com/search_history?userID=1234` If we replace the `userID` with someone else's userID, we should not be able to get the search history of other users
- **Permission-Based Authorization**: This type of authorization is based on privileges granted to the user, such as read and write permissions or access control lists aka ACLs. For example, a file server might grant different levels of access to an organization's employees based on their department IDs or job roles.
    - For example, you could implement an API that requires all requests to submit a valid API key with their request. The server then checks the provided key against its database, and if the key is valid, it grants the user access based on the permissions associated with that key.
- **Role-Based Access Control**: This type of authorization assigns specific roles to specific users, with each role having its own set of privileges and limitations. For example, an administrator would have more privileges than a regular employee, such as the ability to create new users or change permissions for existing ones.
    - For example, an Administrator might be granted full access to all APIs while a Standard User might only have read-only access.
