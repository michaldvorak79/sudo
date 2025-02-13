# ![Sudo for Windows icon](./img/Windows/AppList.targetsize-24.png) Sudo for Windows (modified)

This is a fork of Microsoft's [Sudo for Windows](https://github.com/microsoft/sudo) with one simple change: it doesn't check whether the user has admin rights. This enables the app to (sometimes) work under various over-the-shoulder elevation schemes, i.e. when the users doesn't have admin rights themselves and they need to use another account's credentials or some horrible enterprise solution to obtain elevated rights.

No other changes were made to the app. I don't think this should introduce any issues, but use at your own risk.

## Installation
Put the `sudo.exe` file somewhere in your `PATH`.

Run `sudo config --enable enable` in admin command prompt.

If you find the default `inline` mode doesn't work for you, you may consider running `sudo config --enable forceNewWindow` in admin command prompt. This will make `sudo` always run the elevated commands in a new window which &ndash; on the one hand &ndash; is annoying, but on the other hand it seems to be generally more compatible. Your mileage may vary.