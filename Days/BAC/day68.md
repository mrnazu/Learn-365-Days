# ****Lab 2: Unprotected admin functionality with unpredictable URL****

This lab has an unprotected admin panel. It's located at an unpredictable location, but the location is disclosed somewhere in the application.

- When it say "**unprotected admin panel**" it means it is not secured with any form of protection, like a username and password.

Solve the lab by accessing the admin panel, and using it to delete the user `carlos`.

---

## **Solution💡**

1. Review the lab home page's source using Burp Suite or your web browser's developer tools.
2. that it contains some JavaScript that discloses the URL of the admin panel.
3. Load the admin panel and delete `carlos`.

**Line 41-43**

```jsx
<script>
var isAdmin = false;
if (isAdmin) {
   var topLinksTag = document.getElementsByClassName("top-links")[0];
   var adminPanelTag = document.createElement('a');
   adminPanelTag.setAttribute('href', '/admin-vxyj8f');
   adminPanelTag.innerText = 'Admin panel';
   topLinksTag.append(adminPanelTag);
   var pTag = document.createElement('p');
   pTag.innerText = '|';
   topLinksTag.appendChild(pTag);
}
</script>
```
