# Let's Encrypt & ZeroSSL
Quite a lot of our infrastructure uses either [:octicons-link-external-16: Let's Encrypt]() or [:octicons-link-external-16: ZeroSSL]() for SSL certificates.

This page is for notes about funky implementations for getting those working.

## Notification email address
If you're setting up a new certificate, use the following email address for renewal and security notices:
```
ssl-certs-notify@ops.blkcat.space
```
This email is a group address that is set up to forward to teams who need notifications about problems with certificates. When generating the certificate, **do NOT** opt in to emails from EFF (choose ++n++ if Certbot prompts.)