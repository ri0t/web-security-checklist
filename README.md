# Web Security Checklist (draft)

## Instructions

Please [fork](https://github.com/prologic/web-security-checklist#fork-destination-box) this repo and use as your own checklist as you develop/deploy your web application or api.

If you have [hub](https://hub.github.com/) installed:

```#!bash
$ git clone prologic/web-security-checklist
$ git fork
```

Or:

```#!bash
$ git clone https://github.com/prologic/web-security-checklist
```

**WARNING:** This checklist makes an assumption of the level of expertise and experience of the reader and assumes significant in-depth knowledge and experience in web development.

## App

*Checklist for Backend<->Frontend Web Application(s)*

* [ ] Transport Security -- Protect the transport from sniffing.
  * [ ] TLS/SSL
  * [ ] Redirect al HTTP requests to HTTPS
  * [ ] Use a trusted CA such as [LetsEncrypt](https://letsencrypt.org/)
* [ ] Two Factor Auth -- Helps proect against stolen user credentials.
  * [ ] Expire tokens periodically -- Helps prevent stolen OTP/U2F devices.
* [ ] Session Cookies -- Helps prevent session fixation, hijacking and replay
  * [ ] Regenerate Session IDs -- Helps twart session hijacking/replay.
  * [ ] Store session state server-side -- Riskier storing state client-side.
  * [ ] Set `HttpOnly` -- Helps mitigates successful Cross-Site Scripting attacks.
  * [ ] Set `Secure` -- Helps mitigates against Man-In-The-Middle attacks.
* [ ] Secure IDs -- Helps twart brute-force gusses of valid session ids.
  * [ ] Cryptographic randomoly generate UUIDs
* [ ] Password Store -- Makes offline brute-force attacks much harder or impossible.
  * [ ] Use a strong KDFS such as bcrypt or scrypt.
  * [ ] Unique cryptographically secure 32bit (*ideally 64bit*) salt per password.
  * [ ] Do not restrict length and charset set or encoding.
  * [ ] Impose minimum length and compexity.
* [ ] XSS (*Cross Site Scriptiong*)
  * [ ] Validate all untrusted inputs.
  * [ ] Escape all untrusted inputs.
* [ ] CSRF (*Cross Site Request Forgery*)
  * [ ] Same Origin verification
  * [ ] CSRF Token verification

## API

*Checklist for Backend<->Client Web API(s)*

* [ ] TLS/SSL -- Protect the transport from sniffing.

## Libraries

*Recommended / Vetted libraires solving particular parts of security well.*
(*Pleasr contribute only librarires to this section; Its much harder to vet frameworks.*)

### Python

### Java

### Go

## Resources

* [Google](https://developers.google.com)
  * [Progressive Web App Checklist](https://developers.google.com/web/progressive-web-apps/checklist)
* [OWASP](https://www.owasp.org)
  * [XSS (Cross Site Scripting) Prevention Cheat Sheet](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
  * [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)
  * [Password Storage Cheat Sheet](https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet#Use_a_cryptographically_strong_credential-specific_salt)

## License

This project is licensed under the MIT License. See: [LICENSE](https://github.com/prologic/web-security-checklist/blob/master/LICENSE)

## Contributing

Please fork and submit pull-request(s) to contribute to this checklist, recommended libraries for your favourite language or external resources. See also [CONTRIBUTING.md](https://github.com/prologic/web-security-checklist/blob/master/CONTRIBUTING.md)
