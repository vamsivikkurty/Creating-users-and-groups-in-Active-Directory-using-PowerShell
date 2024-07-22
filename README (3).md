# Active Directory User and Group Management using PowerShell

## Description

This repository contains a set of PowerShell scripts designed to simplify the creation and management of users and groups in Active Directory (AD). These scripts are intended to help administrators efficiently perform common AD tasks without relying on CSV files for input.

### Features

- **Create Users**: Easily create individual user accounts with specified attributes.
- **Create Groups**: Quickly create security and distribution groups with specified properties.
- **Assign Users to Groups**: Add users to groups as part of the user creation process or separately.
- **Error Handling**: Includes robust error handling to manage issues such as existing users/groups and invalid OUs.
- **Logging**: Detailed logging of operations for auditing and troubleshooting purposes.

### Prerequisites

To use the scripts in this repository, ensure you have the following:

- **Active Directory Module for PowerShell**: Necessary for running AD-specific cmdlets.
- **Administrative Privileges**: Required to create and manage users and groups in AD.
- **PowerShell 5.1 or later**: Ensure you have a compatible version of PowerShell.

### Getting Started

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/yourusername/AD-User-Group-Management.git
   ```

2. **Navigate to the Directory**:
   ```sh
   cd AD-User-Group-Management
   ```

### Usage

#### Creating a User

To create a user, use the `Create-ADUser.ps1` script. You need to provide the necessary parameters such as `FirstName`, `LastName`, `Username`, `Password`, and `OU` (Organizational Unit).

Example command:
```powershell
.\Create-ADUser.ps1 -FirstName John -LastName Doe -Username jdoe -Password P@ssw0rd -OU "OU=Users,DC=example,DC=com"
```

#### Creating a Group

To create a group, use the `Create-ADGroup.ps1` script. Provide the required parameters such as `GroupName`, `Description`, and `OU`.

Example command:
```powershell
.\Create-ADGroup.ps1 -GroupName "IT Department" -Description "Group for IT department" -OU "OU=Groups,DC=example,DC=com"
```

#### Adding a User to a Group

To add a user to a group, use the `Add-UserToGroup.ps1` script. Specify the `Username` and `GroupName`.

Example command:
```powershell
.\Add-UserToGroup.ps1 -Username jdoe -GroupName "IT Department"
```

### Error Handling

The scripts include basic error handling to manage common issues such as:
- User or group already exists.
- Insufficient permissions.
- Invalid OU path.

If an error occurs, a detailed message will be logged in the `logs` directory.

### Logging

All operations performed by the scripts are logged for auditing and troubleshooting purposes. Logs are stored in the `logs` directory and include timestamps and detailed information about each operation.

### Contribution

Contributions are welcome! If you have any suggestions for improvements or find any issues, please open an issue or submit a pull request.

### Contact

For questions or further information, please contact lukesundar@gmail.com
---

By using this repository, you can efficiently manage user and group creation in your Active Directory environment, leveraging the power and flexibility of PowerShell.
