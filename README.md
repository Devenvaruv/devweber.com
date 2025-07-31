## Unity Package Development Workflow

This is the workflow used to build and maintain scoped Unity packages (like `com.devweber.room`).

### How to make changes and publish a new version

1. **Make your changes**

   Add or update anything inside:

   ```
   Packages/com.devweber.room/
   ```

2. **Commit the changes**

   ```bash
   git add Packages/com.devweber.room
   git commit -m "added ..."
   ```

3. **Tag the version**

   Use a tag in the format `room-1.0.0` or whatever version you're releasing.

   ```bash
   git tag room-1.0.0
   ```

4. **Push everything**

   Push both the commit and the tag:

   ```bash
   git push origin main --follow-tags
   ```

---

### How to use this package in another Unity project

In your other project’s `manifest.json`, add this line:

```json
"com.devweber.room": "https://github.com/Devenvaruv/devweber.com.git?path=Packages/com.devweber.room#room-1.0.0"
```
or add this github url in package manager
```
https://github.com/Devenvaruv/devweber.com.git?path=Packages/com.devweber.room#room-1.0.0
```

Replace `room-1.0.0` with the version you want.

---

### 🛠️ Notes

- Only tagged versions should be used in `manifest.json`.
- Always commit and push before tagging.
- Make sure you’re on the correct branch (`main`) before tagging.
