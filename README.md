# Good domain disposable emails

This repository contains a list of temporary email addresses that originate from well-known, reputable domains like gmail.com or outlook.com.

## Example usage

### JavaScript

```js
const email = "bob@gmail.com";

const response = await fetch("https://raw.githubusercontent.com/filip-769/good-domain-disposable-emails/main/list.txt");
const text = await response.text();
const list = text.split("\n").map(line => line.trim()).filter(Boolean).filter(line => !line.startsWith("#"));

const is_disposable = list.includes(email.toLowerCase().replace("@googlemail.com", "@gmail.com").replace(/(\.(?=.*@gmail\.com))|(\+.*(?=@))/g, ""));
```

## Contributing

### A new provider

Create a new issue containing a url where you can generate temp emails.

### New emails

Most providers rotate these emails relatively often. If you see that, please create an issue.

## License

This project is licensed under CC0.
Attribution is not required but appreciated.
