---
title: "Introducing MapItemPicker"
date: 2023-04-18T18:42:00+02:00
draft: false
taxonomies:
    category: ["SwiftUI", "iOS", "Library"]
    tag: ["Map", "MapView", "Swift", "SwiftUI", "Library"]
---

# Introducing [MapItemPicker](https://github.com/FiveSheepCo/MapItemPicker): A Powerful Location Picker for SwiftUI

As an app developer, there are times when you need to create a view that allows users to find and select locations. However, Apple doesn't provide a built-in view for this in their frameworks, and much of the information displayed in the Maps app that makes it easy to search for and discover map items is not exposed on `MKMapItem`. That's why we created **MapItemPicker**, a simple, yet highly customizable and powerful location picker for SwiftUI that uses data from MapKit, OpenStreetMaps, and Wikidata to deliver a comprehensive map item picker experience.

<table>
    <tbody>
        <tr>
            <td style="border:none;"><img style="border-radius:.25rem;" src="https://user-images.githubusercontent.com/31473326/230954413-98d3428c-69d2-4273-9d49-d0e032fb7173.png" /></td>
            <td style="border:none;"><img style="border-radius:.25rem;" src="https://user-images.githubusercontent.com/31473326/230954579-8c47e8ce-1d57-4623-a6de-c615a0dd5c82.png" /></td>
        </tr>
    </tbody>
</table>

## What is MapItemPicker?

MapItemPicker is a SwiftUI library that provides an easy-to-use and customizable location picker for your app. It combines data from MapKit, OpenStreetMaps, and Wikidata to offer a beautiful and feature-rich map item picker.

The library has built-in support for annotations and overlays, making it simple to add custom markers and lines on the map. Additionally, it provides a powerful search and filtering functionality, allowing users to quickly find the location they need.

## Getting Started

To start using MapItemPicker, simply add it to your project via Swift Package Manager. Once installed, you can use the convenience method to add a simple picker to your app:

```Swift
.mapItemPickerSheet(isPresented: $showsSheet) { mapItem in
    print("Map Item:", mapItem)
}
```

For more advanced use cases, you can customize the picker using the parameters of `MapItemPicker` view:

```Swift
MapItemPicker(
    annotations: [MKPointAnnotation.chicago],
    overlays: [MKPolyline.newYorkToLosAngeles],
    showsLocationButton: false,
    additionalTopRightButtons: [
        .init(
            imageName: "magnifyingglass",
            handler: { searchControllerShown = true }
        )
    ],
    initialRegion: MKCoordinateRegion.unitedStates,
    standardView: { Text("Standard View") },
    searchControllerShown: $searchControllerShown,
    standardSearchView: { Text("Search View") }
)
```

Check out the full [README](https://github.com/FiveSheepCo/MapItemPicker/blob/main/README.md) for more examples and detailed usage instructions.

## Localization

MapItemPicker includes localizations for categories, titles of sections in the views, and other strings. Currently, only English and German are supported. If you can provide localization for any other language, please submit a PR. You can copy the strings from the English `Localizable.strings` file at `Sources/MapItemPicker/Resources/en.lproj`. It's not a lot of localization keys, and you'll probably be done in 5 minutes.

## Future Plans and Contributions

MapItemPicker is under active development, and there are many exciting features planned for future releases, including:

- Improved location type handling
- More data sources
- Editing opening hours and reporting back to OpenStreetMaps
- Additional filters in search
- Unit tests and UI tests
- Compiled documentation

If you're interested in contributing to MapItemPicker or have any suggestions, feel free to [open an issue](https://github.com/FiveSheepCo/MapItemPicker/issues) or submit a pull request.

## Conclusion

MapItemPicker is an essential tool for developers looking to add a powerful and customizable location picker to their SwiftUI apps. With its combination of MapKit, OpenStreetMaps, and Wikidata, MapItemPicker offers a comprehensive solution that is both user-friendly and feature-rich. By integrating this library into your projects, you'll save valuable development time and provide your users with an intuitive and enjoyable experience when searching for and selecting locations.

Don't hesitate to give MapItemPicker a try and take advantage of its capabilities to enhance your app's functionality. Remember that contributions are always welcome, so feel free to join the project and help improve this fantastic tool even further.

Happy coding!
