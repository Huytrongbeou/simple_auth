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
- Visit: http://localhost:3000/secure (asks for username/password)
- **Login:** admin / 12345

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

**Check Profile:** GET http://localhost:3001/profile (works if logged in)

**Logout:** POST http://localhost:3001/logout

## Test Credentials
- Username: `admin`
- Password: `12345`

## Note
These are learning examples - don't use in real projects without proper security!