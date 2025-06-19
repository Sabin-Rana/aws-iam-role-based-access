# **EpicReads AWS IAM Role-Based Access Implementation**

## **Project Overview**

This project demonstrates the implementation of Role-Based Access for EpicReads' AWS environment using AWS Identity and Access Management (IAM). The objective was to design and establish IAM groups tailored to specific roles, assign users to these groups, configure security credentials, and ensure best practices such as Multi-Factor Authentication (MFA) and access reviews.

As a Cloud Security Administrator at EpicReads, the goal was to improve the overall security posture of the organization’s AWS environment by managing user access and implementing role-based access controls.

---

## **Project Objectives**

- **Design and Implement IAM Groups**: Create IAM groups with appropriate policies for Admins, Developers, and Testers.
- **Assign Users to Groups**: Assign users based on their job roles and responsibilities.
- **Manage Security Credentials**: Ensure each user has unique credentials and enable MFA for admin users.
- **Conduct Access Reviews**: Regularly review access policies and user group assignments.

---

## **Project Steps and Deliverables**

### **Step 1: Creating IAM Groups and Policies**

1. **Admin Group**: Created an IAM group named **Admin** and attached the `AdministratorAccess` policy.
   - **Screenshot**: ![capture_1.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/capture1.PNG) - Showing the IAM Group creation screen.
   - **Screenshot**: ![capture_2.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture2.PNG) - Highlighting the newly created Admin group.

2. **Developer Group**: Created an IAM group named **Developers** and attached policies such as `AmazonEC2FullAccess`, `AmazonS3FullAccess`, and `AmazonRDSFullAccess`.
   - **Screenshot**: ![capture_7.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture7.PNG) - Showing the Developer group with the attached policies.

3. **Tester Group**: Created an IAM group named **Testers** with policies that include `EC2ReadOnlyAccess`, `AmazonS3ReadOnlyAccess`, and `AmazonRDSReadOnlyAccess`.
   - **Screenshot**: ![capture_9.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture9.PNG) - Showing the Tester group with the attached policies.

---

### **Step 2: Adding Users to Groups**

1. **Admin Users**:
   - Created users **Luffy**, **Zoro**, and **Sanji** and assigned them to the **Admin** group.
   - **Screenshot**: ![capture_3.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture3.PNG) - Showing the user creation for Luffy.
   - **Screenshot**: ![capture_4.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture4.PNG) - Luffy being added to the Admin group.
   - **Screenshot**: ![capture_5.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture5.PNG) - Successful user creation for Luffy.
   - **Screenshot**: ![capture_6.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture6.PNG) - Showing all three users (Luffy, Zoro, Sanji) in the Admin group.

2. **Developer Users**:
   - Created users **Usopp**, **Franky**, and **Vegapunk** and added them to the **Developer** group.
   - **Screenshot**: ![capture_8.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture8.PNG) - Showing all users in the Developer group.

3. **Tester Users**:
   - Created users **Nami**, **Robin**, and **Chopper** and assigned them to the **Tester** group.
   - **Screenshot**: ![capture_10.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture10.PNG) - Showing all Tester users in the Tester group.

4. **Cross-functional User**:
   - Created a user **Trafalgar** and assigned it to both **Developer** and **Tester** groups.
   - **Screenshot**: ![capture_11.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture11.PNG) - Showing the cross-functional user Trafalgar in two groups.

---

### **Step 3: Configuring User Security Credentials**

1. Enabled **Console Access** for all users and set up a custom password policy with an option for users to create a new password at the next sign-in.
   - **Screenshot**: ![capture_12.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture12.PNG) - Showing the enable console access dialog for Luffy.
   - **Screenshot**: ![capture_13.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture13.PNG) - Confirmation that console access has been enabled for Luffy.

   This step was repeated for all users in the Admin, Developer, and Tester groups.

---

## **Security Best Practices Implemented**

- **MFA for Admin Users**: Multi-Factor Authentication (MFA) was enabled for all admin users to provide an additional layer of security.
- **Least Privilege Principle**: Each IAM group was assigned only the necessary permissions to limit access.
- **Regular Access Reviews**: A review process was established to evaluate and modify user group memberships and policies as needed.

---

## **Project Outcome**

- A **structured IAM environment** was created, improving security by ensuring that users have appropriate permissions.
- Implemented **role-based access control (RBAC)** to ensure users only have access to the resources necessary for their job functions.
- **Security credentials**, including MFA for admins and secure login configurations, were established for all users.
- Ensured compliance with **security best practices** such as the principle of least privilege and regular access reviews.

---

## **Screenshots Directory**

1. ![capture_1.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture1.PNG) - Screenshot of Admin group creation.
2. ![capture_2.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture2.PNG) - Screenshot showing the newly created Admin group.
3. ![capture_3.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture3.PNG) - User creation for Luffy.
4. ![capture_4.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture4.PNG) - Luffy added to Admin group.
5. ![capture_5.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture5.PNG) - Confirmation message for Luffy’s successful user creation.
6. ![capture_6.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture6.PNG) - All users (Luffy, Zoro, Sanji) in the Admin group.
7. ![capture_7.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture7.PNG) - Developer group creation with the specified policies.
8. ![capture_8.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture8.PNG) - Developer users (Usopp, Franky, Vegapunk) added to Developer group.
9. ![capture_9.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture9.PNG) - Tester group creation with the specified policies.
10. ![capture_10.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture10.PNG) - Tester users (Nami, Robin, Chopper) added to Tester group.
11. ![capture_11.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture11.PNG) - Trafalgar user added to both Developer and Tester groups.
12. ![capture_12.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture12.PNG) - Enabling console access for user Luffy.
13. ![capture_13.png](https://github.com/Sabin-Rana/aws-iam-role-based-access/blob/main/Screenshots/Capture13.PNG) - Confirmation of console access for Luffy.

---

## **Conclusion**

This project demonstrates the creation and management of IAM roles and policies in AWS, enabling secure and efficient user access management. By establishing a well-defined IAM structure, EpicReads has improved its overall security posture and operational efficiency.
