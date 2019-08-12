[![Latest Stable Version](https://poser.pugx.org/codeq/passwordprotectedcontent/v/stable)](https://packagist.org/packages/codeq/passwordprotectedcontent)
[![License](https://poser.pugx.org/codeq/passwordprotectedcontent/license)](LICENSE)

# Password Protect Content for Neos CMS

This package allows editors to password protect any document and content NodeType, where the mixin is included.

**Attention:**
This is on purpose not super secure. We do store the unencrypted passwords in the content repository, so that multiple 
editors can see and editor the password.

The password can be set in the request as POST or GET argument.

## Installation

CodeQ.HtmlWidget is available via packagist. `"codeq/passwordprotectedcontent" : "~1.0"` to the require section of the 
composer.json or run:

```bash
composer require codeq/passwordprotectedcontent
```

We use semantic-versioning so every breaking change will increase the major-version number.

## Usage

1. Add the mixin `'CodeQ.PasswordProtectedContent:Mixin.Password'` to any NodeType to allow editors to configure a password.
2. Add the following process function to protect the content 
`@process.protect = CodeQ.PasswordProtectedContent:Helper.ProtectContent`

The process function is not added automatically, because you probably want to render headers and footers for you page. 
So you can specifically define which content should be rendered and which no when no password is define.

## License

Licensed under MIT, see [LICENSE](LICENSE)

## Contribution

We will gladly accept contributions. Please send us pull requests.

*The development and the public-releases of this package is generously sponsored [Code Q Web Factory](http://codeq.at).*

<img src="codeq.png" alt="Code Q" width="200"/>
