---
title: "Introducing ChatView"
date: 2023-04-19T00:00:00+02:00
draft: false
taxonomies:
    category: ["SwiftUI", "iOS", "macOS", "Library"]
    tag: ["ChatView", "Swift", "SwiftUI", "Messaging", "Library"]
---

# QSChatView: A beautiful data-driven chat view for iOS and macOS
> In today's fast-paced world, chat applications have become an essential means of communication. With the increasing popularity of SwiftUI and its easy-to-use, declarative syntax, developers are always on the lookout for reliable libraries to build messaging interfaces for their apps. Look no further! Quintschaf has created a SwiftUI library called QSChatView that provides a customizable chat view for rendering static and interactive chat conversations, similar to popular messaging apps like WhatsApp and Signal.

QSChatView is a fully interactive, data-driven chat view that works on iOS, macOS, and Catalyst. It supports light and dark mode, and offers various customization options.

## Key Features

QSChatView offers a range of features that make it an ideal choice for creating chat interfaces in your SwiftUI apps. Some of the key features include:

1. **Data-driven chat view**: The chat view is fully data-driven, allowing you to easily connect it to your app's data source, whether it's a server, database, or local cache.

2. **Interactive elements**: The library supports various interactive elements, such as typing indicators, which help create a more engaging user experience.

3. **Customizable appearance**: You can easily customize the appearance of your chat interface using the `ChatConfigBuilder` to match your app's design and requirements.

4. **Rich media support**: `QSChatView` allows you to incorporate rich media, such as images and videos[^1], into your chat conversations, providing a more immersive experience for your users.

5. **Cross-platform compatibility**: The library works seamlessly on iOS, macOS, and Catalyst, making it a perfect choice for developers looking to create chat interfaces across multiple platforms.

6. **Light and dark mode support**: `QSChatView` supports both light and dark modes, ensuring that your chat interface will look great regardless of the user's system preferences.

7. **Swift Package Manager integration**: Installing and managing `QSChatView` is easy thanks to its Swift Package Manager integration. Just add the library's URL to your project's dependencies and you're good to go.

With these features and more, `QSChatView` makes it simple to build beautiful, data-driven chat applications for iOS and macOS.

[^1]: Images are implemented, but Video and Audio is not yet supported.

### Customization Options

One of the key features of QSChatView is the ability to customize the chat view according to your app's design and requirements. Using the `ChatConfigBuilder`, you can easily adjust many settings and behaviors.

Here's an example of how to create a basic, custom chat configuration:

```swift
let config = ChatConfigBuilder()
    .showTextField()
    .showTimestamps(false)
    .withScrollingBehavior(.adaptive)
    .build()
```

## Installing QSChatView

To install QSChatView, simply add the following URL to your Swift Package Manager dependencies:

```
https://github.com/quintschaf/qschatview.git
```

## Getting Started with QSChatView

### Basic Example

Here is a basic example with a single chat participant and message:

```swift
import SwiftUI
import QSChatView

struct MyChatView: View {
    // Instantiate a `ChatController` with some initial messages
    @StateObject var controller = ChatController(messages: [
        ChatMessage(from: .me, content: .text("Hello world")),
    ])

    var body: some View {
        // Render the chat view with our controller
        QSChatView(controller).padding()
    }
}
```

### Advanced Example

A more advanced example with a modified config, multiple participants and a custom chat backend:

```swift
import SwiftUI
import QSChatView

class MyChatData: ObservableObject {
    @Published var controller: ChatController
    @Published var chatPartner: ChatParticipant

    init() {
        // Build chat config.
        // You can also use `ChatConfig.default` here.
        let config = ChatConfigBuilder()
            .showTextField()
            .showTimestamps(false)
            .withScrollingBehavior(.adaptive)
            .build()

        // In this example we specify a fixed set of initial messages.
        //
        // In a real-world application, you would probably load messages
        // from a server or database, or restore them from a local cache.
        let messages: [ChatMessage] = [
            ChatMessage(from: .me, content: .text("Hey John, are you there?"))
        ]

        // Create a chat controller with our messages and config
        self.controller = ChatController(messages: messages, config: config)

        // Create a chat partner
        self.chatPartner = ChatParticipantBuilder().withName("John Doe").build()
    }

    // This is meant as an example on how to interact with the chat controller.
    // It also serves as an introduction to the `ChatMessagePromise` API.
    func startMessageTimer() {

        // Run this block every 5 seconds
        Timer.scheduledTimer(withTimeInterval: 5, repeats: true) { _ in

            // Add a temporary message with a typing indicator.
            // In this case, John Doe is shown as typing.
            let messagePromise = self.controller.sendPromise(from: self.chatPartner)

            // Wait 2 seconds before resolving the promise
            DispatchQueue.main.asyncAfter(deadline: .now() + 2) {

                // Resolve the promise with the actual message
                messagePromise.fulfill(withContent: .text("Hello from John!"))

                // In the case that John stops typing without sending
                // a message, we can use `messagePromise.reject()` instead.
            }
        }
    }
}

struct MyChatView: View {
    @StateObject var chat = MyChatData()

    // Called when the user sends a message through the chat view
    func handleMessageSent(_ message: String) {
        // Messages are added to the controller before this callback is called.
        // 
        // We can do additional processing here, such as sending the message
        // to a server, logging it, updating statistics, and so on.
        // 
        // In this example, we just print the message to the console.
        print("User sent message: \(message)")
    }

    var body: some View {
        // Render the chat view with our controller and callback
        QSChatView(chat.controller, onMessageSent: handleMessageSent)
            .padding()
            .onAppear { chat.startMessageTimer() }
    }
}
```

## Conclusion

QSChatView is an excellent SwiftUI library for creating customizable and interactive chat views for your iOS and macOS applications. The examples provided in the README demonstrate how easy it is to implement and customize the chat view according to your application's requirements. By leveraging the power of SwiftUI and QSChatView, you can create beautiful, data-driven chat applications for iOS and macOS.

Give QSChatView a try by visiting the [GitHub repository](https://github.com/Quintschaf/QSChatView) and start building amazing chat experiences for your users today!