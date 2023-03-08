# **Lab: Unprotected admin functionality**

This lab has an unprotected admin panel.

Solve the lab by deleting the user `carlos` 

So Our Goal is Finding the admin panel and delete the user `carlos`

---

The first method for finding an admin panel in a web application would be to look through the source code. This can be done by viewing the page source or using tools such as Firefox/Chrome DevTools. 

You may also find web-fuzzing tools that are able to search and burt-force contents on web apps. Additionally, depending on the web application, there may be index directory pages or Robots.txt that could allow you access to the admin panel itself.

# **Solution💡**

1. Go to the lab and view `robots.txt` by appending `/robots.txt` to the lab URL. Notice that the `Disallow` line discloses the path to the admin panel.
2. In the URL bar, replace `/robots.txt` with `/administrator-panel` to load the admin panel.
3. Delete `carlos`.
