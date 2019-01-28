# letsimple

## Requisites

In order to use `letsimple` you need to have:

- Bash
- Netcat (nc)
- Docker

## Available options

`letsimple` provide the following options. You could use either the short or the long version.

Short | Long        | Arguments        | Description
----- | ----------- | ---------------- | ----------------------------------------------
`-c`  | `--certify` | `DOMAIN` `EMAIL` | Issue a certificate for `DOMAIN` using `EMAIL`
`-d`  | `--delete`  | `DOMAIN`         | Delete `DOMAIN` certificate
`-h`  | `--help`    | -                | Show help
`-r`  | `--renew`   | -                | Attempts to renew all installed certificates
`-t`  | `--test`    | `DOMAIN`         | Issue a TEST certificate for `DOMAIN`
`-v`  | `--version` | -                | Print version

## Examples

### To issue a TEST certificate for domain `example.com`

```
letsimple --test example.com
```

### To delete a certificate issued for domain `example.com`

```
letsimple --delete example.com
```

### To issue a certificate for domain `example.com`

```
letsimple --certify example.com mail@example.com
```

## Exit codes

Code | Description
---- | --------------------
0    | OK
1    | Invalid option
2    | No `DOMAIN` informed
3    | No `EMAIL` informed
