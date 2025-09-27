# Simple Authentication Examples

Two simple ways to authenticate users in Node.js:

## What's Inside
- `basic_auth.js` - Simple username/password authentication
- `cookie_auth.js` - Login with cookies (remembers you for 5 minutes)

## Setup
1. Install packages: `npm install`
2. Make sure MongoDB is running

## How to Use

### Basic Authentication
```bash
node basic_auth.js
```
- Visit: http://localhost:3000 (no login needed)
  <img width="983" height="998" alt="image" src="https://github.com/user-attachments/assets/b191be85-0128-40e7-804e-8b318d336427" />

- Visit: http://localhost:3000/secure (asks for username/password)
  <img width="970" height="997" alt="image" src="https://github.com/user-attachments/assets/cf308363-fd00-4a60-8428-5de888a14a8b" />

- **Login:** admin / 12345
<img width="960" height="989" alt="image" src="https://github.com/user-attachments/assets/ddbd2b81-c32d-43df-b90c-ddd6c8144e02" />

### Cookie Authentication  
```bash
node cookie_auth.js
```
**Login:** Send POST to http://localhost:3001/login
```json
{
  "username": "admin",
  "password": "12345"
}
```
<img width="987" height="1006" alt="image" src="https://github.com/user-attachments/assets/5a400be9-78a5-4882-8a66-36950b2bd0a0" />

**Check Profile:** GET http://localhost:3001/profile (works if logged in)
<img width="974" height="977" alt="image" src="https://github.com/user-attachments/assets/f112d207-3288-4fca-8a2a-0937c0199d13" />

**Logout:** POST http://localhost:3001/logout
<img width="978" height="1003" alt="image" src="https://github.com/user-attachments/assets/2ff287a0-d240-4e64-8bbd-997546fc302c" />

## Test Credentials
- Username: `admin`
- Password: `12345`
<img width="1768" height="867" alt="image" src="https://github.com/user-attachments/assets/522a7bc1-4b45-4080-aefb-a92661582030" />

## Note
These are learning examples - don't use in real projects without proper security!
