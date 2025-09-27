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
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/dcff2896-8e00-403d-b94d-7ce1f002b892" />

- Visit: http://localhost:3000/secure (asks for username/password)
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/40d562cd-8b41-4cbf-9146-087433a4458b" />


- **Login:** admin / 12345
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e9c938bb-fb21-444a-bced-d8350fdd87ee" />

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
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/89868328-b51a-49f5-9164-76c356e11628" />

**Check Profile:** GET http://localhost:3001/profile (works if logged in)
<img width="1920" height="1078" alt="image" src="https://github.com/user-attachments/assets/e8461b95-54f8-4092-80bb-65f4dd8b09f5" />

**Logout:** POST http://localhost:3001/logout
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/b0f484f9-f89d-4ce0-93a3-1a5e97866b7c" />

## Test Credentials
- Username: `admin`
- Password: `12345`
## Check session database
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7d674ab0-cc7a-45db-b52a-2939fb4ed7bf" />

## Note
These are learning examples - don't use in real projects without proper security!
