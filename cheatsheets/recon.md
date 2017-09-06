# Certspotter

```zsh
curl https://certspotter.com/api/v0/certs\?domain\=example.com | jq '.[].dns_names[]' | sed 's/\"//g' | sed 's/\*\.//g' | uniq
```

```zsh
curl https://certspotter.com/api/v0/certs\?domain\=example.com | jq '.[].dns_names[]' | sed 's/\"//g' | sed 's/\*\.//g' | uniq | dig +short -f - | uniq | nmap -T5 -Pn -sS -i - -p 80,443,21,22,8080,8081,8443 --open -n -oG -
```

# Sublist3r One-liner

This runs [Sublist3r](https://github.com/aboul3la/Sublist3r) on a list of domains and outputs the results in separate files.

```
. <(cat domains | xargs -n1 -i{} python sublist3r.py -d {} -o {}.txt)
```
