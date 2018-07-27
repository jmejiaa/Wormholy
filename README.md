<p align="center">
  <img src="https://raw.githubusercontent.com/pmusolino/Wormholy/master/logo.png" alt="Icon"/>
</p>

  [![Language](https://img.shields.io/badge/Swift-4-orange.svg)]()
  [![Pod version](https://img.shields.io/cocoapods/v/Wormholy.svg?style=flat)](https://cocoapods.org/pods/Wormholy)
  
  Start debugging iOS network calls like a wizard, without extra code! Wormholy makes debugging quick and reliable.
  
  
  **What you can do:**
  
  - [x] No code, no import.
  - [x] Record all the app traffic that use NSURLSession.
  - [x] Reveal the content of all requests, responses, and headers shaking your phone!
  - [x] No headaches with SSL certificates on HTTPS calls.
  - [x] Search and delete bugs quickly.
  - [x] Swift & Objective-C compatibility
  - [x] Works also with external libraries like Alamofire & AFNetworking.
  
  <p align="center">
  <img src="https://raw.githubusercontent.com/pmusolino/Wormholy/master/screens.png" alt="Icon"/>
</p>
  
## Requirements
----------------

- iOS 9.0+
- Xcode 9+


## Usage
----------------
Add it to your project, and that's all! **Shake your device** or your simulator and Wormholy will appear! You don't need to import the library into your code, it works magically!

I suggest you install it only in debug mode. The easy way is via cocoapods:

```
pod 'Wormholy', :configurations => ['Debug']
``` 


If you want to disable the shake, and fire Wormholy from another point inside your app, you need to set the [environment variable](https://medium.com/@derrickho_28266/xcode-custom-environment-variables-681b5b8674ec) `WORMHOLY_SHAKE_ENABLED` = `NO`, and call this local notification:

```
NotificationCenter.default.post(name: NSNotification.Name(rawValue: "wormholy_fire"), object: nil)
```

You can also programmatically enable/disable the shake gesture at any time. You can do `Wormholy.shakeEnabled = false // or true` to enable or disable the shake gesture. 



## Carthage
----------------

Another way to install Wormholy is [Carthage](https://github.com/Carthage/Carthage).

To integrate Wormholy into your Xcode project using Carthage, specify it in your `Cartfile`:

```ogdl
github "pmusolino/Wormholy"
```
Run `carthage update` to build the framework and drag the built `Wormholy.framework` into your Xcode project.

## Contributing

- If you **need help** or you'd like to **ask a general question**, open an issue.
- If you **found a bug**, open an issue.
- If you **have a feature request**, open an issue.
- If you **want to contribute**, submit a pull request.


## Acknowledgements

Made with ❤️ by [Paolo Musolino](https://github.com/pmusolino).
Follow me on:
[Twitter](http://twitter.com/pmusolino)
[Linkedin](https://www.linkedin.com/in/paolomusolino/)
[Facebook](https://www.facebook.com/paolomusolino)

## MIT License
----------------
Wormholy is available under the MIT license. See the LICENSE file for more info.