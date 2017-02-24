# MyGovBC-Captcha-Widget Angular2
This is just the user interface part of an overall solution, for service component see:

* https://github.com/bcgov/MyGovBC-CAPTCHA-Service

## Installing

First get the component via NPM:

```
npm install git+https://github.com/bcgov/MyGovBC-CAPTCHA-Widget.git
```

Add to your AngularJS module declaration:
```
let CaptchaComponent = require("mygovbc-captcha-widget/component").CaptchaComponent;
...
  declarations: [..., CaptchaComponent, ...]

```

Then use on a template:

```
<div class="row">
    <captcha [apiBaseUrl]="captchaApiBaseUrl" [nonce]="<optional string to get signed by the server>"
             (onValidToken)="authorizationToken = $event"></captcha>
</div>
```

