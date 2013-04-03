gmail
=====

A simple Go library for sending emails from a Gmail account.

NB: The attachment code was inspired by [scorredoira's email][1]  and full credit goes
to him.

```go
email := gmail.Compose("Email subject", "Email body")
email.From = "username@gmail.com"
email.Password = "password"

// Normally you'll only need one of these, but I thought I'd show both.
email.AddRecipient("recipient@example.com")
email.AddRecipients("another@example.com", "more@example.com")

err := email.Send()
if err != nil {
	log.Fatal(err)
}
```

  [1]: https://github.com/scorredoira/email        "scorredoira's email"
