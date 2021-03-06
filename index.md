---
title: Users
order: xx
---

## Manging Users

Admin Users can manage the access of other users in their mParticle Account from the **User Management** tab of their User Settings page:

![medium](Platform-Update-Manage-Users-042019.png)

To add a new user, provide first and last name, an email address, and select the user's permissions. See [Roles](#roles) for more on permisisons.

![medium](Platform-Update-Manage-Users-New-User-042019.png)


## Roles

mParticle offers several User Roles with different levels of access to the mParticle Dashboard. You can check your Role from your User Settings page:

![medium](Platform-Update-Mange-Users-User-Settings-042019.png)

mParticle's User Roles are:

* **User** - Can view and make updates to all parts of the mParticle platform except for the User Activity view and managing other users
* **Read Only** - Has the same view access as 'User' level but cannot make any changes additions
* **Admin** - Same access as 'User' level, plus the ability to add, remove and manage users and access the User Activity view
* **Audiences Only** - Can view and manage Audiences. Cannot view other areas of the mParticle platform. Note that this means Audiences Only users can connect audiences to existing Outputs, but cannot add and configure new Audience Outputs
* **Compliance** - Can view and manage the [Requests Page](/guides/data-subject-requests/#managing-data-subject-requests-in-the-mparticle-dashboard). Has Read Only access in other parts of the dashboard
* **Admin & Compliance** - All Admin permissions, plus can view and manage the [Requests Page](/guides/data-subject-requests/#managing-data-subject-requests-in-the-mparticle-dashboard)
* **Support Access** - All Admin permissions except for user management capabilities.  This role should be used to delegate access to an mParticle support representative while troubleshooting a ticket.  This role has access to end-user PII within the account.

## Advanced Feature: Using the Platform API

If you have the proper credentials, you can issue API calls to get a list of users:

```
curl \
  -X GET \
  -H "Authorization: Bearer YWIxMjdi883GHBBDnjsdKAJQxNjdjYUUJABbg6hdI.8V6HhxW-" \
  "https://api.mparticle.com/v1/users?accountId=1"
  ```
  
  example response
  
  ```
  {
  "data": [
    {
      "first_name": "Test",
      "last_name": "User",
      "email": "testuser@mparticle.com",
      "data_type": "usr"
    }
  ],
  "dataType": "user",
  "errors": null
}
```

You can also get information about a single user:

```
curl \
  -X GET \
  -H "Authorization: Bearer YWIxMjdi883GHBBDnjsdKAJQxNjdjYUUJABbg6hdI.8V6HhxW-" \
  "https://api.mparticle.om/v1/users/test40mparticle2Ecom?accountId=1"
```

Example Response

```
{
  "data": [
    {
      "first_name": "Test",
      "last_name": "User",
      "email": "test@mparticle.com",
      "data_type": "user"
    }
  ],
  "dataType": "user",
  "errors: null
}
```
