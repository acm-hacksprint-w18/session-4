# Hack Sprint Session 4 README

## Getting Started

1. Begin by creating a new project in Xcode.
2. Select "Create a new Xcode project" near the bottom left of the window.

![img](https://lh5.googleusercontent.com/Uv_0UW2wVlVMjLCC0YniMQTgR-SZEVgo27yXnlcWThcU2tvB9wDIeW4swW8Ky9C0LvOwxks0nwM3cjUWRoa_YxKu-Q1EsuSmeIRfAQqAhrJ5lln5IY9lE-8wdxwkNJAKNfHW5Y-v)

------

3. Ensure that the "iOS" tab at the top of the page is selected.
4. Double-click on "Single View App".

![img](https://lh5.googleusercontent.com/8K6MDiviiQGT4Zh34welL_CBntAvjlPDZAcGhEXWoswlfNNYY_Mxx1SPEqdgLpZF6wGVWqlUKfimvS_jXOlvPhSAmeHiZ4k76at4I3uYb_KM-TUFqRUNOE2hJvqPmcZXISCsqWaM)

------

5. Name your project "Twitterando".
6. Pick whatever Team, Organization Name and Organization Identifier that you want.
7. Ensure that the Language field is set to "Swift".
8. Ensure that "Use Core Data" is unchecked.
9. Click "Next".
10. On the following window, select where you'd like your project's folder to be create (default location is ~/Desktop) and click "Create".

![img](https://lh4.googleusercontent.com/rWru9AIk_E0k7MLGyr01Iaw6l4LwYVwPI0g5x6kv3YGBdkLonoGOJo28xfIpYrj168YqPTahgnqGtIo9V1h6cUaH80KQqGkCPmZFDy2pUdU2RV1ghWkTXTrwq5609svrm_4r3lYo)

---

## Installing CocoaPods

CocoaPods is the dependency manager for iOS projects. You can use it to access and integrate thousands of external Swift libraries into your projects which can scale them elegantly.

1. Open your Terminal, and run the command:

   `$ sudo gem install cocoapods`

   Note: The '$' is not a part of the command; it's merely there just to say that this line of code is a shell command explicitly.

2. After the installation has completed, run the command:

   `$ gem which cocoapods`

   to check if the installation was successful. Your terminal should output a path that ends with the file **cocoapods.rb**.

## Adding TwitterKit to our Project

1. Using the [cd](https://www.computerhope.com/unix/ucd.htm) command, navigate to your project folder. If it's stored on your Desktop (and named Twitterando), the command:

   `$ cd ~/Desktop/Twitterando`

   should work.

2. Once inside your project's folder, run the command:

   `$ pod init`

   This will create a file named **Podfile** inside the same folder.

3. Edit the Podfile by opening it using any text editor. Here are some convenince commands:

   **TextEdit**

   `$ open -a TextEdit Podfile`

   **Sublime Text**

   `$ open -a "Sublime Text" Podfile`

   **emacs**

   `$ emacs Podfile`

   **vim**

   `ew who uses vim`

4. Locate the line "# Pods for Twitterando".

5. Directly underneath, insert the line:

   `pod 'TwitterKit'`

<img src="https://lh4.googleusercontent.com/BxrCjNxfrUp5z78g8KI3yi3g2vJJMEQWW2FqHZRvnH6xRgv7jzRR4OjXBPT1lZQB81V0OR_k94bVLADR8E917Dj4ghsnoQLBwk38x0xE6ZwGsaPSzMlgdoSVIncjVlXJOUJYcTqG" width="500px">

---

6. Save your changes to the Podfile.

7. Return to the Terminal, and ensure you are still inside your project's folder/directory.

8. Run the command:

   `$ pod install`

9. If you run the [ls](https://www.computerhope.com/unix/uls.htm) command, you'll notice that the `pod install` command will have generated a file named **Twitterando.xcworkspace**. From now on, to work on your project, you **must** use this xcworkspace fill.

10. Return to Xcode and close the Twitterando project.

11. Through Finder or the Terminal, open the file **Twitterando.xcworkspace**.

    `$ open -a Xcode Twitterando.xcworkspace`

And just like that, we've successfully added the TwitterKit library to our project!

## Setting Up the UI

Back in Xcode, you should now notice a new object named **Pods** inside the Project Navigator on the left side of the screen. This is another insurance that your `pod install` command worked.

1. Using the **Project Navigator** on the left side of Xcode, select the **Main.storyboard** file to open the Interface Builder. If you cannot see the Main.storyboard file, use the arrows next to the folders to expand them.

<img src="https://lh6.googleusercontent.com/7vNszmgq-y-b_yWDduv0kgoqF9dpKZr7S_7HwqsvKHulUkayelNi1Q1IZXD7Zvc_eFMtM6OiWMnNnQEbz-Qw_Mz4dSBtlQwe-lr_UEUEq0Db2wyGVsBtiLR8RoYHrcqcVe-45p96" width="200px">

---

2. Click inside of the single View Controller inside the Interface Builder.
3. Open the **Atributes Inspector** by clicking on the icon to the left of the ruler icon in the top-right corner of Xcode.
4. Ensure that the header in the Attributes Inspector says **View**
5. Locate the "Background" field about six fields down from the top. Click on the white bar (not the blue arrows) to open the color picker.
6. Select the second tab in the color pickers and use the sliders to change the background color to the color (192, 222, 237):

<img src="https://lh5.googleusercontent.com/bi2PVPZy7ChqRPhq29MXbket7zkDGvWdO_BrlzlEpnQoyZyiuvmbeQ7M0M32EsfmL8tIojlUq9fjVohNR0Olp7fYQn9YH8mAXjDR8FR181JmsZIqUglo44AQ2RuI-RPaWnXZ6z__" width="400px">

---

7. Close the color picker.
8. In the pane on the bottom right of Xcode, ensuring the third tab is selected scroll to the very bottom so that you see the **Button** element.

<img src="https://lh3.googleusercontent.com/6WLxmh4unKgLEsDXT-fk0N5WS6kpOHXfbm2CW_MZ3EoBbfgIUH59SMDNNDTrHLHntt6kTKRZyTAbCzpg7V-Eha73KN-5TKG_-O3zPfGKIEyUPIUJ5fbLoQshKk3vhDnl-_zdoQsC" width="300px">

---

9. Drag a Button into the View Controller and position it similar to the following photo:

<img src="https://lh6.googleusercontent.com/ayI6PpEG80afYXmVAg1Kp4C1XTmfM1Jxn5mKW1ZL7AyR4XJzWeKWHD6R9cfNrFbQR_sXStgHAn68pBoU6e4_QlJ_uAEEdk5ATFeXUtZlpglMtVCzILVa4sOvnlCB5GBc_0nhqjpa" width="300px">

---

10. With the Button still selected, click on the "Resolve Auto Layout Constraints" button near the bottom right of Xcode.
11. Click the **topmost** button that says "Reset to Suggested Constraints".

<img src="https://lh3.googleusercontent.com/MHrKwKlcvkwyig3jnipmzSfkr-Qf3La4nv5S_7ckpUcmwG9RNxIOhfPaPQHS3JhdLr9Cd0PCXwwehbP0LbpxmC2mgnLsZz4Xef-rrYk9B6n9_VGJ2LCDDGx4RJEo7wWhPvHBZEoe" width="400px">

---

12. With the Button still selected, open the **Attributes Inspector** by clicking on the button to the left of the ruler icon near the top-right of Xcode.
13. Locate the "Title" field about four fields down from the top of the pane.
14. Change the button title from "Button" to "**Generate**". Press Enter.

<img src="https://lh5.googleusercontent.com/FcQK791Gt2Qa6I6hRTr6ebTZVSAUbLsZ2V2gEgR3ZEYzcjviq1KVAWxUiJb-uCKiql293A_ghgYm9_TbF5JzCutChePDnGDqeV55yoyK15HroBptBvRFofDaWFTrGAeX8F0xflP5" width="400px">

---

## Linking the Button Tap to our Code

1. Click on the two overlapping circles near the top right of Xcode to open the **Assistant Editor**.
2. If it is difficult to see our View Controller, close the left pane if necessary by clicking on the button (square with black rectangle on the left side) to the left of "View as iPhone..." in the bottom left of the window.

<img src="https://lh6.googleusercontent.com/UiUoxLRj4084y9zVeaRQrcOVg3UqbQpAYv3Ml14wrEGTCq2idzloTf-XmhKxJKEBzydSQFRDm21Q3dTO5SvVF3nlveIwEdcXwvW4m7W1mJjJhmANO6nUm0LRI5Zi2BpmOTuxCu2x" width="200px">

---

3. **While holding down control** (not to be confused with cmd), click on the Button and drag to the space just above `viewDidLoad()`, but still within the `class ViewController` block.
4. In the window that appears, **ensure that the "Type" field says UIButton, else press "Cancel" and try again.**
5. Change the "Connection" from Outlet to **Action** via the drop-down menu.
6. In the "Name" field, type "**tappedGenerate**".
7. Change the "Type" from Any to **UIButton**.
8. Ensure the "Event" says "**Touch Up Inside**".
9. Click "Connect"

<img src="https://lh5.googleusercontent.com/9F7EpYTzuhCXyIMm3YbTpNGXCmRWaFs0foO0cLcJWZoK09ckkvs7ldTcE0bdeIC5Kl7885JoFR8Bl92rkLkfTZg35BxUtRF37-OipmPQ7D3qfL97pmyID-3VkEIKV2_HWsM1t0J0" width="400px">

---

## Coding in Swift

### Configuring the Twitter API

1. Close the Assistant Editor by clicking on the "X" on the top right of the pane with our code in it.

<img src="https://lh4.googleusercontent.com/A-RVsXCWjLw7CCSyVnILjcA6unhMfWogMvawakNxymxEXA4XAsPmde8Efr-ql0YH5ypolsSQnb5uTRwzmfKu5a6CUjLadufzZVf8lOHZjQW_dnrlEThuQOdSILP7Ng-Fk0aeGQ19" width="300px">

---

2. Using the Project Navigator, select the **AppDelegate.swift** file.

3. Change the first function, `application(_:didFinishLaunchingWithOptions:)`, to the following:

   ```
   func application(_ application: UIApplication, didFinishLaunchingWithOptions launchOptions: [UIApplicationLaunchOptionsKey: Any]?) -> Bool {
   	// Override point for customization after application launch.
       Twitter.sharedInstance().start(withConsumerKey: "qsSBF4peypKJlnkEP8fvRvBUr", consumerSecret: "J3uFqQghjrnn406cuVLXpRYkyh1qsNBmBkaL4F5NPbBaFkapBi")
       return true
   }
   ```

pls don't use our app secret for malicious intents thx :')

### Adding a TweetView

1. Using the Project Navigator, select the **ViewController.swift** file.

2. Underneath the `import UIKit` line, **outside** of the class declaration of ViewController add the following line:

   `import TwitterKit`

3. **Inside** the class declaration of ViewController, just above the `tappedGenerate(_:)` function we created, declare the following property:

   `var tweetView: TWTRTweetView!`

4. Change `viewDidLoad()` to the following:

   ```
   override func viewDidLoad() {
   	super.viewDidLoad()
       // Do any additional setup after loading the view, typically from a nib.
           
       tweetView = TWTRTweetView()
       tweetView.center = self.view.center
           
       self.view.addSubview(tweetView)
   }
   ```

5. Change `tappedGenerate(_:)` to the following:

   ```
   @IBAction func tappedGenerate(_ sender: UIButton) {
           
       // Generate random number from 0 ... 1b
       let randomID = arc4random_uniform(1000000000)
           
   	TWTRAPIClient().loadTweet(withID: String(randomID)) { tweet, error in
               
       	if let t = tweet {
       		self.tweetView.removeFromSuperview()
               self.tweetView = TWTRTweetView(tweet: t)
               self.tweetView.center = self.view.center
               self.view.addSubview(self.tweetView)
       	}
               
       	else {
       		print("Failed to load Tweet: \(error?.localizedDescription)")
       	}
               
       }
           
   }
   ```

   ​