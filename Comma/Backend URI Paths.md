# Info
This part of the doc consists of all the Backend API endpoints of Comma. For Frontend URL paths, please refer to other document.

# URI List
## Not Authenticated User (logged out)
### Register
To register new users

```bash
[GET] /comma/v1/users/register
```

### All Items
To view all items

```bash
[GET] /comma/v1/items
```

### Item with id
```bash
[GET] /comma/v1/items/{id}
```

### Item with name (whole)
```bash
[GET] /comma/v1/items/{name}
```

### Item with name (partial)
```bash
[GET] /comma/v1/items/{partial name}
```

### All shops
```bash
[GET] /comma/v1/shops
```

### Shops with id
```bash
[GET] /comma/v1/shops/{id}
```

### Shops with name (whole)
```bash
[GET] /comma/v1/shops/{name}
```

### Shops with name (partial)
```bash
[GET] /comma.v1/shops/{partial name}
```
## Authenticated User (logged in)

### View personal profile
```bash
[GET] /comma/v1/items/user/profile/{id}
```

### Edit personal profile
```bash
[POST] /comma/v1/items/user/profile/{id}/edit
```

### Delete personal profile
```bash
[POST] /comma/v1/items/user/profile/{id}/delete
```

### Submit new item
```bash
[POST] /comma/v1/items/submit/
```

### Edit item
```bash
[POST] /comma/v1/items/{id}/edit/
```

### Delete item
```bash
[POST] /comma/v1/items/{id}/delete
```

### Submit new shop
```bash
[POST] /comma/v1/shops/submit/
```

### Edit shop
```bash
[POST] /comma/v1/shops/{id}/edit/
```

### Delete shop
```bash
[POST] /comma/v1/shops/{id}/delete
```


## Authenticated Admin (logged in)

### View user profile
```bash
[GET] /comma/v1/items/user/profile/{id}
```

### Edit user profile
```bash
[POST] /comma/v1/items/user/profile/{id}/edit
```


### Delete user profile
```bash
[POST] /comma/v1/items/user/profile/{id}/delete
```

### Suspend user profile
This allows `admins` to suspend a `user` for a certain periods of time or permanently (until further notice). `admins` are also required to submit a reason for the suspension. 

```bash
[POST] /comma/v1/items/user/profile/{id}/suspend
```

### Submit new item
```bash
[POST] /comma/v1/items/submit/
```

### Edit item
```bash
[POST] /comma/v1/items/{id}/edit/
```

### Delete item
```bash
[POST] /comma/v1/items/{id}/delete
```

### Suspend item
This allows `admins` to suspend an item from being listed. Can be for a period of time or permanently (until further notice). `admins` are required to submit a reason for suspension. A separate message can be inserted for `users` view. 
```bash
[POST] /comma/v1/items/{id}/suspend
```

### Submit new shop
```bash
[POST] /comma/v1/shops/submit/
```

### Edit shop
```bash
[POST] /comma/v1/shops/{id}/edit/
```

### Delete shop
```bash
[POST] /comma/v1/shops/{id}/delete
```

### Suspend shop
This allows `admins` to suspend a shop from being listed. Can be for a period of time or permanently (until further notice). `admins` are required to submit a reason for suspension. A separate message can be inserted for `users` view.

```bash
[POST] /comma/v1/shops/{id}/suspend
```

### View users audit trail
Note that **NO ALTERATIONS** should happen in audit trail.

```bash
[GET] /comma/v1/users/audit
```

### View items audit trail
Note that **NO ALTERATIONS** should happen in audit trail.

```bash
[GET] /comma/v1/items/audit
```

### View shops
Note that **NO ALTERATIONS** should happen in audit trail.

```bash
[GET] /comma/v1/shops/audit
```

