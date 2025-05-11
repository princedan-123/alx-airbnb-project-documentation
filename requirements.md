# **Requirement Specification**
## **User Registration**
### **Functional Requirements**
- Users should be able to register and create a profile account.
- Users should be able to update and delete their account.
- The actions users can take should depend on their role (guest, host or admin).
### **Technical Requirements**
#### **API**
- **endpoint** POST /user
- **input**: {
    user_id: "uuid",
    first_name: "Daniel",
    last_name: "Mabia",
    email: "daniel.tech@gmail.com",
    password_hash: "password",
    phone_number: "047944484737"
    role: "guest"
}
- **output**: {
    user: <fistname>,
    user_id: <user_id>,
    message: "created"
}
- **Validation**
 - password must be hashed and should be at least 8 character long.
 - Email must be a valid email
- **Error**
  - `409 Conflict`: Email already exists
  - `422 Unprocessable`: Missing fields