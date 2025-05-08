# Utils

### (m)TLS generate util

Source: [tls-gen](/tls-gen.exe)
Flags:
- `-mutual` (*optional) - create server (+ CA & client) certificates & keys.
- `--out-path` (*optional) - outputs certificates & keys to the specified directory.

Example:
> #### Architecture:
> ```
> mtls-demo/
> ├── mycrts/
> |
> ├── service1/
> │   ├── main.go
> │   └── go.mod
> |
> └── service2/
>    ├── main.go
>    └── go.mod
> ```
>
> #### Terminal:
> `./tls-gen.exe -mutual --out-path=mycrts`
> 
> #### Architecture:
> ```
> mtls-demo/
> ├── mycrts/
> |   ├── ca.crt
> |   ├── ca.key
> |   ├── client.crt
> |   ├── client.key
> |   ├── server.crt
> |   └── server.key
> |   
> ├── service1/
> │   ├── main.go
> │   └── go.mod
> |
> └── service2/
>    ├── main.go
>    └── go.mod
> ```
