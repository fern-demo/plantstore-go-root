# plantstore-go-root

FSE-84 verification: Fern generates the SDK at the repo **root**; the frozen
openapi-generator SDK lives in `legacy/`, protected by `.fernignore`.

| Import path | SDK |
| --- | --- |
| `github.com/fern-demo/plantstore-go-root/v2` | Fern (current) |
| `github.com/fern-demo/plantstore-go-root/v2/legacy` | openapi-generator (frozen) |
