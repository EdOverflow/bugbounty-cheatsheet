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

# [Apktool](https://ibotpeaches.github.io/Apktool/) to [LinkFinder](https://github.com/GerbenJavado/LinkFinder)

```
apktool d app.apk; cd app;mkdir collection; find . -name \*.smali -exec sh -c "cp {} collection/\$(head /dev/urandom | md5 | cut -d' ' -f1).smali" \;; linkfinder -i 'collection/*.smali' -o cli
```

# [Aquatone](https://github.com/michenriksen/aquatone/) One-liner

```
$ echo "aquatone-discover -d \$1 && aquatone-scan -d \$1 --ports huge && aquatone-takeover -d \$1 && aquatone-gather -d \$1" >> aqua.sh && chmod +x aqua.sh
$./aqua.sh domain.com
```
