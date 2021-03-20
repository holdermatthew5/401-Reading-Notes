# DRF Permissions

## Authentication

`IsAuthenticated` class in Django REST Framework defines a view as only viewbale by those with permission.
`IsAuthenticatedOrReadOnly` class defines a view as fully usable to users with permission and only readable for users without permission.
REST views checks permission when `.get_object()` is run.
When creating your own views or over writing `get_object` check permissions explicitly with `self.check_object_permissions(request, obj)`.
`.AllowAny` can be used to allow unrestricted access.

## API Reference

"AllowAny
- The AllowAny permission class will allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

This permission is not strictly required, since you can achieve the same result by using an empty list or tuple for the permissions setting, but you may find it useful to specify this class because it makes the intention explicit.

IsAuthenticated
- The IsAuthenticated permission class will deny permission to any unauthenticated user, and allow permission otherwise.

This permission is suitable if you want your API to only be accessible to registered users.

IsAdminUser
- The IsAdminUser permission class will deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

This permission is suitable if you want your API to only be accessible to a subset of trusted administrators.

IsAuthenticatedOrReadOnly
- The IsAuthenticatedOrReadOnly will allow authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.

This permission is suitable if you want to your API to allow read permissions to anonymous users, and only allow write permissions to authenticated users." - (Copied directly from [Django-Documentation](https://www.django-rest-framework.org/api-guide/permissions/))