# react-turnstile

A very simple React library for [Cloudflare Turnstile](https://challenges.cloudflare.com).

## Installation

```sh
npm i react-turnstile
```

## Usage

```jsx
import Turnstile from "react-turnstile";

// ...

function TurnstileWidget() {
  return (
    <Turnstile
      sitekey="1x00000000000000000000AA"
      onVerify={(token) => alert(token)}
    />
  );
}
```

## Documentation

Turnstile takes the following arguments:

| name     | type   | description                        |
| -------- | ------ | ---------------------------------- |
| sitekey  | string | sitekey of your website (REQUIRED) |
| action   | string | -                                  |
| cData    | string | -                                  |
| theme    | string | one of "light", "dark", "auto"     |
| tabIndex | number |
| id       | string | id of the div                      |

And the following callbacks:

| name     | arguments | description                                |
| -------- | --------- | ------------------------------------------ |
| onVerify | token     | called when challenge is passed (REQUIRED) |
| onLoad   | -         | called when the widget is loaded           |
| onError  | error     | called when an error occurs                |
| onExpire | -         | called when the challenge expires          |

For more details on what each argument does, see the [Cloudflare Documentation](https://developers.cloudflare.com/turnstile/get-started/client-side-rendering/#configurations).
