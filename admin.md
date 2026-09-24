

## 🛡️ Admin Panel

After registering, become admin by opening your browser console (F12) on the live site:

```javascript
// Run this in the browser console after logging in
let users = JSON.parse(localStorage.getItem('mc_users') || '[]');
let me = users.find(u => u.email === 'YOUR_EMAIL_HERE');
if (me) {
  me.role = 'admin';
  localStorage.setItem('mc_users', JSON.stringify(users));
  console.log('✅ You are now admin! Log out and back in.');
} else {
  console.log('❌ User not found. Make sure you registered first.');
}
```

Log out and back in → Profile tab → scroll down → **Admin Panel** appears.

**Admin capabilities:**
- 👥 View all registered users, ban/unban with reason
- 🚩 Review flagged content (posts reported by users)
- 📰 View and delete any post



---

## 📝 Updating the App

1. Make changes to `index.html` on GitHub (click ✏️ pencil icon)
2. Commit changes
3. Vercel auto-deploys in ~30 seconds — no manual action needed

---
