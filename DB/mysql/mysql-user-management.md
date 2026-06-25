# MySQL User Management Cheat Sheet

## Login to MySQL

```bash
mysql -u root -p
```

For AWS RDS:

```bash
mysql -h <db-endpoint> -u admin -p
```

---

## List Existing Users

```sql
SELECT user, host FROM mysql.user;
```

---

## Create New User

### Access from Any Host

```sql
CREATE USER 'dev_user'@'%' IDENTIFIED BY 'StrongPassword@123';
```

### Access from Specific IP

```sql
CREATE USER 'dev_user'@'10.0.1.25' IDENTIFIED BY 'StrongPassword@123';
```

### Access from Localhost Only

```sql
CREATE USER 'dev_user'@'localhost' IDENTIFIED BY 'StrongPassword@123';
```

---

## Verify User

```sql
SELECT user, host
FROM mysql.user
WHERE user='dev_user';
```

---

## Read Only Access

```sql
GRANT SELECT
ON staging_db.*
TO 'dev_user'@'%';
```

---

## Read + Write Access

```sql
GRANT SELECT, INSERT, UPDATE, DELETE
ON staging_db.*
TO 'dev_user'@'%';
```

---

## Migration Access

```sql
GRANT SELECT, INSERT, UPDATE, DELETE,
CREATE, ALTER, INDEX
ON staging_db.*
TO 'dev_user'@'%';
```

---

## Full Database Access

```sql
GRANT ALL PRIVILEGES
ON staging_db.*
TO 'dev_user'@'%';
```

---

## Check User Permissions

```sql
SHOW GRANTS FOR 'dev_user'@'%';
```

---

## Apply Privileges

```sql
FLUSH PRIVILEGES;
```

---

## Revoke Specific Permission

```sql
REVOKE DELETE
ON staging_db.*
FROM 'dev_user'@'%';
```

---

## Revoke All Permissions

```sql
REVOKE ALL PRIVILEGES
ON staging_db.*
FROM 'dev_user'@'%';
```

---

## Change Password

```sql
ALTER USER 'dev_user'@'%'
IDENTIFIED BY 'NewPassword@123';
```

---

## Lock User

```sql
ALTER USER 'dev_user'@'%'
ACCOUNT LOCK;
```

Unlock:

```sql
ALTER USER 'dev_user'@'%'
ACCOUNT UNLOCK;
```

---

## Delete User

```sql
DROP USER 'dev_user'@'%';
```

---

## Active Connections

```sql
SHOW PROCESSLIST;
```

---

## Kill Session

```sql
KILL <process_id>;
```

Example:

```sql
KILL 12345;
```

---

# Recommended Workflow

### Step 1 - Create User

```sql
CREATE USER 'dev_user'@'%' IDENTIFIED BY 'Password@123';
```

### Step 2 - Assign Permissions

```sql
GRANT SELECT, INSERT, UPDATE, DELETE
ON staging_db.*
TO 'dev_user'@'%';
```

### Step 3 - Verify

```sql
SHOW GRANTS FOR 'dev_user'@'%';
```

### Step 4 - Share Credentials Securely

* AWS Secrets Manager
* HashiCorp Vault
* Bitwarden
* 1Password

Never share credentials through email or public chat.

### Step 5 - Revoke Access When Work Is Done

```sql
DROP USER 'dev_user'@'%';
```

Or

```sql
ALTER USER 'dev_user'@'%'
ACCOUNT LOCK;
```
