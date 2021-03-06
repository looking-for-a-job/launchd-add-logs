<!--
https://readme42.com
-->



[![](https://img.shields.io/badge/OS-Unix-blue.svg?longCache=True)]()
[![](https://img.shields.io/pypi/v/launchd-add-logs.svg?maxAge=3600)](https://pypi.org/project/launchd-add-logs/)
[![](https://img.shields.io/npm/v/launchd-add-logs.svg?maxAge=3600)](https://www.npmjs.com/package/launchd-add-logs)[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/launchd-add-logs/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/launchd-add-logs/actions)

### Installation
```bash
$ [sudo] pip install launchd-add-logs
```

```bash
$ [sudo] npm i -g launchd-add-logs
```

#### How it works
```
~/Library/Logs/LaunchAgents/<Label>/out.log
~/Library/Logs/LaunchAgents/<Label>/err.log
```

`<name>.plist`
```xml
<key>StandardErrorPath</key>
<string>/Users/<username>/Library/Logs/LaunchAgents/<Label>/err.log</string>
<key>StandardOutPath</key>
<string>/Users/<username>/Library/Logs/LaunchAgents/<Label>/out.log</string>
```

#### Examples
```bash
$ find ~/Library/LaunchAgents -name "*.plist" -print0 | xargs -0 launchd-add-logs
```

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
