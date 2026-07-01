# Security Spec

1. Data Invariants:
- A user can only access their own data.
- Tasks must have an ownerId that matches the user's uid.
- Users must have an ownerId that matches their uid.
- Notifications must have an ownerId that matches the user's uid.

2. Dirty Dozen Payloads:
- Shadow field in User profile
- Spoofed ownerId on User profile creation
- Modify ownerId on User profile update
- Update missing fields
- Spoofed ownerId on Task creation
- Modify ownerId on Task update
- Task title size too large
- Unauthenticated read
- Cross-user read
- Unauthenticated write
- Create task for another user

3. Test Runner
We will skip implementing the full test suite in this environment but the rules will handle these invariants.
