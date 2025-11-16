# AKIPS

AKIPS API endpoints

## Installation

AKIPS package
```bash
go get github.com/xtokio/akips
```

ENV Variables
```bash
export AKIPS_URL="akips_server.com"
export AKIPS_PASSWORD="akips_api_password"
```

Add the dependency to your `main.go` file:

  ```go
 import (
    "fmt"
    "github.com/xtokio/akips"
  )
  ```

## Usage

```go
func main() {
  // Get list of switches
  switch_list := akips.Switch_list()
  for _, current_switch := range switch_list{
    fmt.Printf("Switch: %s :: IP: %s",current_switch.Switch, current_switch.IP)
  }

  // Get list of Interfaces usage
  interface_usage := akips.Interface_usage("lgomezreswitch.acme")
  fmt.Print(interface_usage)
}
```

## Contributing

1. Fork it (<https://github.com/xtokio/akips/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## Contributors

- [Luis Gomez](https://github.com/xtokio) - creator and maintainer
