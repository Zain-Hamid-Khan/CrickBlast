# CrickBlast_GUI

CrickBlast_GUI is a C# application that includes functionalities for managing user accounts, playing matches, and other related operations. This repository contains various classes that handle different parts of the application.

## Table of Contents

- [Account](#account)
- [Admin](#admin)
- [ConnectionString](#connectionstring)
- [ConvertImage](#convertimage)
- [Login](#login)
- [Match](#match)
- [Getting Started](#getting-started)
- [License](#license)

## Account

The `Account` class provides methods for user account management such as checking if an email is unique, creating new accounts, modifying details, and deleting accounts. 

### Methods

- `IsUnique(string email)`: Checks if the given email is unique.
- `Create(string username, string email, string password, string phoneNumber, int gender, Image image)`: Creates a new user account.
- `ModifyDetails(string username, string email, string password, string phoneNumber, string id)`: Modifies user account details.
- `Delete(string id)`: Deletes a user account.

## Admin

The `Admin` class is designed for managing administrative functions within the application.

### Methods

- `Authenticate(string username, string password)`: Authenticates an admin user.
- `CreateAdmin(string username, string password)`: Creates a new admin user.
- `DeleteAdmin(string username)`: Deletes an admin user.

## ConnectionString

The `ConnectionString` class holds the database connection strings.

### Fields

- `CricBlastDB`: Connection string for the CricBlast database.

## ConvertImage

The `ConvertImage` class provides utility methods for converting images to byte arrays and vice versa.

### Methods

- `ToBytes(Image image)`: Converts an image to a byte array.
- `ToImage(byte[] imageData)`: Converts a byte array back to an image.

## Login

The `Login` class handles user login operations.

### Methods

- `Authenticate(string email, string password)`: Authenticates a user based on email and password.
- `GetUserDetails(string email)`: Retrieves user details based on email.

## Match

The `Match` class manages match-related operations such as recording match results and updating user statistics.

### Methods

- `Play(bool won, string result)`: Records a match and updates the result.
- `Played(bool won)`: Updates the played match count and win count for a user.
- `Result(string result)`: Records the match result in the database.

## Getting Started

To get started with CricBlast_GUI, follow these steps:

1. Clone the repository:
    ```sh
    git clone https://github.com/your-username/CricBlast_GUI.git
    ```
2. Open the solution in Visual Studio.
3. Restore the NuGet packages.
4. Build the solution and run the application.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
