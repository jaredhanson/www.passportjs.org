# Log Out

Now that users can sign in, they'll need a way to sign out.

Open `'routes/auth.js'` and add this route at line 84, below the
`'/login/mailchain/verify'` route:

```js
router.post('/logout', function(req, res, next) {
  req.logout(function(err) {
    if (err) { return next(err); }
    res.redirect('/');
  });
});
```

Return to the app, where you should already be signed in, and click "Sign out."

We've now got a working app where users can sign in and sign out!
