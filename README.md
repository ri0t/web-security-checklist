# Web Security Checklist (draft)

## Instructions

Please fork this gist and use as your own checklist as you develop/deploy your web application or api.

**WARNING:** This checklist makes an assumption of the level of expertise and experience of the reader and assumes significant in-depth knowledge and experience in web development.

## App

*Checklist for Backend<->Frontend Web Application(s)*

* [ ] TLS/SSL -- Protect the transport from sniffing.
* [ ] OTP/U2F -- Helps proect against stolen user credentials.
  * [ ] Expire OTP/U2F tokens periodically -- Helps prevent stolen OTP/U2F devices.
* [ ] Secure session cookies -- Helps prevent session fixation, hijacking and replay
  * [ ] Regenerate Session IDs -- Helps twart session hijacking/replay.
  * [ ] Store session state server-side -- Riskier storing state client-side.
  * [ ] Set `HttpOnly` -- Helps mitigates successful Cross-Site Scripting attacks.
  * [ ] Set `Secure` -- Helps mitigates against Man-In-The-Middle attacks.
* [ ] Secure Session IDs -- Helps twart brute-force gusses of valid session ids.
  * [ ] Cryptographic randomoly generate UUIDs
* [ ] Secure password database -- Makes offline brute-force attacks much harder or impossible.
  * [ ] Use either bcrypt or scrypt

## API

*Checklist for Backend<->Client Web API(s)*

* [ ] TLS/SSL -- Protect the transport from sniffing.

## Libraries

*Recommended / Vetted libraires solving particular parts of security well.*

### Python

### Java

### Go

## Resources

* [Google](https://developers.google.com)
  * [Progressive Web App Checklist](https://developers.google.com/web/progressive-web-apps/checklist)
* [OWASP](https://www.owasp.org)
  * [XSS (Cross Site Scripting) Prevention Cheat Sheet](https://www.owasp.org/index.php/XSS_(Cross_Site_Scripting)_Prevention_Cheat_Sheet)
  * [Cross-Site Request Forgery (CSRF) Prevention Cheat Sheet](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)