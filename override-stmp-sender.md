* /etc/postfix/main.cf

```
sender_canonical_classes = envelope_sender, header_sender
sender_canonical_maps = regexp:/etc/postfix/sender_canonical_maps
header_checks = regexp:/etc/postfix/header_checks
```

* /etc/postfix/header_checks
```
/From: .*/ REPLACE From: "Piggy E-Mail" <noreply@piggy.io>
```

* /etc/postfix/sender_canonical_maps

```
/.+/    noreply@piggy.io
```
