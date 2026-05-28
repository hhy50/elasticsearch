```shell
bin\elasticsearch-certutil ca `
  --out config\certs\ca.p12 `
  --pass P85vDOJlQMKOiwmXx4DgmA `
  --silent
```

```shell
bin\elasticsearch-certutil cert `
  --name http `
  --out config\certs\http.p12 `
  --pass P85vDOJlQMKOiwmXx4DgmA `
  --dns localhost,127.0.0.1 `
  --self-signed `
  --silent
```

```shell
bin\elasticsearch-certutil cert `
  --name transport `
  --out config\certs\transport.p12 `
  --pass 4AXrJuiASeirK3QtJQ1diQ `
  --ca config\certs\ca.p12 `
  --ca-pass P85vDOJlQMKOiwmXx4DgmA `
  --dns localhost,127.0.0.1 `
  --silent
```


