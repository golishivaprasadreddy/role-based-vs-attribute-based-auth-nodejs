

# Role-Based and Attribute-Based Authentication in Node.js

## 1. Introduction

### Overview of Authentication & Authorization
Authentication is the process of verifying the identity of a user, while authorization determines what an authenticated user is allowed to do. Both are critical for securing applications.

### Difference between RBAC and ABAC
- **Role-Based Access Control (RBAC):** Access is granted based on user roles.
- **Attribute-Based Access Control (ABAC):** Access is granted based on user attributes, resource attributes, and environmental conditions.

## 2. Role-Based Access Control (RBAC)

### How RBAC Works
RBAC assigns permissions to users based on their roles (e.g., admin, user). Each role has a set of permissions associated with it.

### Advantages & Disadvantages
**Advantages:**
- Simple to implement and manage
- Clear separation of permissions based on roles

**Disadvantages:**
- Scalability issues with a large number of roles
- Lack of fine-grained control

### Examples of RBAC in Real-World Applications
- **Admin Panels:** Only admins can access certain features.
- **Content Management Systems:** Different roles like editor, viewer, and contributor.

### Example Implementation

1. **Setup a Node.js Project**
   ```sh
   mkdir rbac-example
   cd rbac-example
   npm init -y
   npm install express jsonwebtoken bcryptjs mongoose