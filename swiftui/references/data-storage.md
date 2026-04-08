# Data and Storage — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Creating and sharing view state

- [Managing user interface state](/documentation/swiftui/managing-user-interface-state) *(article)*
- [State](/documentation/swiftui/state) — property wrapper for view-owned mutable state
- [Bindable](/documentation/swiftui/bindable) — creates bindings to @Observable properties
- [Binding](/documentation/swiftui/binding) — two-way reference to a value owned elsewhere

## Creating model data

- [Managing model data in your app](/documentation/swiftui/managing-model-data-in-your-app) *(article)*
- [Migrating from Observable Object protocol to Observable macro](/documentation/swiftui/migrating-from-the-observable-object-protocol-to-the-observable-macro) *(article)*
- [@Observable](/documentation/observation/observable()) — modern macro for model objects
- [StateObject](/documentation/swiftui/stateobject) — owns an ObservableObject instance `[legacy]`
- [ObservedObject](/documentation/swiftui/observedobject) — subscribes to an ObservableObject `[legacy]`
- [ObservableObject](/documentation/combine/observableobject) `[legacy — prefer @Observable]`

## Responding to data changes

- [func onChange(of:initial:_:)](/documentation/swiftui/view/onchange(of:initial:_:)) — react to value changes
- [func onReceive(_:perform:)](/documentation/swiftui/view/onreceive(_:perform:)) — subscribe to a Publisher

## Distributing model data throughout your app

- [func environmentObject(_:)](/documentation/swiftui/view/environmentobject(_:)) — inject into view hierarchy `[legacy]`
- [EnvironmentObject](/documentation/swiftui/environmentobject) `[legacy — prefer @Environment with @Observable]`

## Environment

- [Environment](/documentation/swiftui/environment) — reads values from the environment
- [EnvironmentValues](/documentation/swiftui/environmentvalues) — all built-in environment keys
- [macro Entry()](/documentation/swiftui/entry()) — declare custom environment keys
- [EnvironmentKey](/documentation/swiftui/environmentkey) — protocol for custom keys `[legacy — prefer @Entry]`

### Key EnvironmentValues *(fetch EnvironmentValues JSON for complete list)*

**Accessibility:** accessibilityEnabled, accessibilityReduceMotion, accessibilityReduceTransparency, accessibilityDifferentiateWithoutColor, accessibilityVoiceOverEnabled, accessibilityInvertColors, legibilityWeight

**Actions:** dismiss, dismissSearch, dismissWindow, openURL, openWindow, pushWindow, openImmersiveSpace, dismissImmersiveSpace, newDocument, openDocument, refresh, rename, resetFocus, openSettings

**Controls:** controlSize, buttonRepeatBehavior, keyboardShortcut, menuOrder, menuIndicatorVisibility, searchSuggestionsPlacement

**Display:** colorScheme, colorSchemeContrast, displayScale, horizontalSizeClass, verticalSizeClass, imageScale, pixelLength

**Global:** calendar, locale, timeZone, managedObjectContext, modelContext, undoManager, documentConfiguration

**Scrolling:** isScrollEnabled, horizontalScrollIndicatorVisibility, verticalScrollIndicatorVisibility, scrollDismissesKeyboardMode

**State:** editMode, isEnabled, isFocused, isPresented, isSearching, scenePhase, supportsMultipleWindows

**Text:** font, dynamicTypeSize, lineLimit, lineSpacing, multilineTextAlignment, textCase, truncationMode, layoutDirection, allowsTightening, minimumScaleFactor

**View attributes:** backgroundMaterial, backgroundStyle, redactionReasons, symbolRenderingMode, symbolVariants, contentTransition

**Widgets:** widgetFamily, widgetRenderingMode, showsWidgetContainerBackground, widgetContentMargins

### Modifying the environment

- [func environment(_:)](/documentation/swiftui/view/environment(_:)) — set an Observable type
- [func environment(_:_:)](/documentation/swiftui/view/environment(_:_:)) — set by key path
- [func transformEnvironment(_:transform:)](/documentation/swiftui/view/transformenvironment(_:transform:)) — modify in place

## Preferences

- [Preferences](/documentation/swiftui/preferences) *(article)*
- [func preference(key:value:)](/documentation/swiftui/view/preference(key:value:)) — set a preference
- [func transformPreference(_:_:)](/documentation/swiftui/view/transformpreference(_:_:)) — modify a preference
- [PreferenceKey](/documentation/swiftui/preferencekey) — protocol for custom preference keys
- [func anchorPreference(key:value:transform:)](/documentation/swiftui/view/anchorpreference(key:value:transform:)) — geometry-based preference
- [func onPreferenceChange(_:perform:)](/documentation/swiftui/view/onpreferencechange(_:perform:)) — respond to changes
- [func backgroundPreferenceValue(_:_:)](/documentation/swiftui/view/backgroundpreferencevalue(_:_:)) — generate background from preference
- [func overlayPreferenceValue(_:_:)](/documentation/swiftui/view/overlaypreferencevalue(_:_:)) — generate overlay from preference

## Persistent storage

- [Restoring your app's state with SwiftUI](/documentation/swiftui/restoring-your-app-s-state-with-swiftui) *(article)*
- [func defaultAppStorage(_:)](/documentation/swiftui/view/defaultappstorage(_:)) — set UserDefaults for view hierarchy
- [AppStorage](/documentation/swiftui/appstorage) — reads/writes UserDefaults
- [SceneStorage](/documentation/swiftui/scenestorage) — per-scene state restoration

## Core Data

- [Loading and displaying a large data feed](/documentation/swiftui/loading-and-displaying-a-large-data-feed) *(article)*
- [FetchRequest](/documentation/swiftui/fetchrequest) — fetches Core Data results
- [FetchedResults](/documentation/swiftui/fetchedresults) — the result collection
- [SectionedFetchRequest](/documentation/swiftui/sectionedfetchrequest) — sectioned Core Data fetch
- [SectionedFetchResults](/documentation/swiftui/sectionedfetchresults) — sectioned result collection
