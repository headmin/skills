# App Structure — SwiftUI Reference

## Contents
- [App structure](#app-structure)
  - [Creating an app](#creating-an-app)
  - [Targeting iOS and iPadOS](#targeting-ios-and-ipados)
  - [Targeting macOS](#targeting-macos)
  - [Targeting watchOS](#targeting-watchos)
  - [Targeting tvOS](#targeting-tvos)
  - [Handling system recenter events](#handling-system-recenter-events)
  - [Creating scenes](#creating-scenes)
  - [Monitoring scene life cycle](#monitoring-scene-life-cycle)
  - [Managing a settings window](#managing-a-settings-window)
  - [Building a menu bar](#building-a-menu-bar)
  - [Creating a menu bar extra](#creating-a-menu-bar-extra)
  - [Creating watch notifications](#creating-watch-notifications)
  - [Essentials](#essentials)
  - [Creating windows](#creating-windows)
  - [Styling the associated toolbar](#styling-the-associated-toolbar)
  - [Opening windows](#opening-windows)
  - [Closing windows](#closing-windows)
  - [Sizing a window](#sizing-a-window)
  - [Positioning a window](#positioning-a-window)
  - [Configuring window visibility](#configuring-window-visibility)
  - [Managing window behavior](#managing-window-behavior)
  - [Interacting with volumes](#interacting-with-volumes)
  - [Deprecated Types](#deprecated-types)
  - [Creating an immersive space](#creating-an-immersive-space)
  - [Opening an immersive space](#opening-an-immersive-space)
  - [Closing the immersive space](#closing-the-immersive-space)
  - [Hiding upper limbs during immersion](#hiding-upper-limbs-during-immersion)
  - [Adjusting content brightness](#adjusting-content-brightness)
  - [Responding to immersion changes](#responding-to-immersion-changes)
  - [Adding menu items to an immersive space](#adding-menu-items-to-an-immersive-space)
  - [Handling remote immersive spaces](#handling-remote-immersive-spaces)
  - [Creating a document](#creating-a-document)
  - [Storing document data in a structure instance](#storing-document-data-in-a-structure-instance)
  - [Storing document data in a class instance](#storing-document-data-in-a-class-instance)
  - [Accessing document configuration](#accessing-document-configuration)
  - [Reading and writing documents](#reading-and-writing-documents)
  - [Opening a document programmatically](#opening-a-document-programmatically)
  - [Configuring the document launch experience](#configuring-the-document-launch-experience)
  - [Renaming a document](#renaming-a-document)
  - [Essentials](#essentials)
  - [Presenting views in columns](#presenting-views-in-columns)
  - [Stacking views in one column](#stacking-views-in-one-column)
  - [Managing column collapse](#managing-column-collapse)
  - [Setting titles for navigation content](#setting-titles-for-navigation-content)
  - [Configuring the navigation bar](#configuring-the-navigation-bar)
  - [Configuring the sidebar](#configuring-the-sidebar)
  - [Presenting views in tabs](#presenting-views-in-tabs)
  - [Configuring a tab bar](#configuring-a-tab-bar)
  - [Configuring a tab](#configuring-a-tab)
  - [Enabling tab customization](#enabling-tab-customization)
  - [Displaying views in multiple panes](#displaying-views-in-multiple-panes)
  - [Deprecated Types](#deprecated-types)
  - [Configuring a dialog](#configuring-a-dialog)
  - [Showing a sheet, cover, or popover](#showing-a-sheet-cover-or-popover)
  - [Adapting a presentation size](#adapting-a-presentation-size)
  - [Configuring a sheet’s height](#configuring-a-sheets-height)
  - [Styling a sheet and its background](#styling-a-sheet-and-its-background)
  - [Presenting an alert](#presenting-an-alert)
  - [Getting confirmation for an action](#getting-confirmation-for-an-action)
  - [Showing a confirmation dialog with a message](#showing-a-confirmation-dialog-with-a-message)
  - [Configuring a dialog](#configuring-a-dialog)
  - [Exporting to file](#exporting-to-file)
  - [Importing from file](#importing-from-file)
  - [Moving a file](#moving-a-file)
  - [Configuring a file dialog](#configuring-a-file-dialog)
  - [Presenting an inspector](#presenting-an-inspector)
  - [Dismissing a presentation](#dismissing-a-presentation)
  - [Deprecated modal presentations](#deprecated-modal-presentations)
  - [Populating a toolbar](#populating-a-toolbar)
  - [Populating a customizable toolbar](#populating-a-customizable-toolbar)
  - [Removing default items](#removing-default-items)
  - [Setting toolbar visibility](#setting-toolbar-visibility)
  - [Specifying the role of toolbar content](#specifying-the-role-of-toolbar-content)
  - [Styling a toolbar](#styling-a-toolbar)
  - [Configuring the toolbar title display mode](#configuring-the-toolbar-title-display-mode)
  - [Setting the toolbar title menu](#setting-the-toolbar-title-menu)
  - [Creating an ornament](#creating-an-ornament)
  - [Searching your app’s data model](#searching-your-apps-data-model)
  - [Making search suggestions](#making-search-suggestions)
  - [Limiting search scope](#limiting-search-scope)
  - [Detecting, activating, and dismissing search](#detecting-activating-and-dismissing-search)
  - [Displaying toolbar content during search](#displaying-toolbar-content-during-search)
  - [Searching for text in a view](#searching-for-text-in-a-view)
  - [Creating widgets](#creating-widgets)
  - [Composing control widgets](#composing-control-widgets)
  - [Labeling a widget](#labeling-a-widget)
  - [Styling a widget group](#styling-a-widget-group)
  - [Controlling the accented group](#controlling-the-accented-group)
  - [Managing placement in the Dynamic Island](#managing-placement-in-the-dynamic-island)

---
## App structure

- [App organization](/documentation/swiftui/app-organization)

### Creating an app

- [Destination Video](/documentation/visionos/destination-video)
- [Hello World](/documentation/visionos/world)
- [Backyard Birds: Building an app with SwiftData and widgets](/documentation/swiftui/backyard-birds-sample)
- [Food Truck: Building a SwiftUI multiplatform app](/documentation/swiftui/food-truck-building-a-swiftui-multiplatform-app)
- [Fruta: Building a feature-rich app with SwiftUI](/documentation/appclip/fruta-building-a-feature-rich-app-with-swiftui)
- [Migrating to the SwiftUI life cycle](/documentation/swiftui/migrating-to-the-swiftui-life-cycle)
- [App](/documentation/swiftui/app)

#### Implementing an app

- [var body: Self.Body](/documentation/swiftui/app/body-swift.property)
- [Body](/documentation/swiftui/app/body-swift.associatedtype)

#### Running an app

- [init()](/documentation/swiftui/app/init())
- [static func main()](/documentation/swiftui/app/main())

### Targeting iOS and iPadOS

- [UILaunchScreen](/documentation/bundleresources/information-property-list/uilaunchscreen)
- [UILaunchScreens](/documentation/bundleresources/information-property-list/uilaunchscreens)
- [UIApplicationDelegateAdaptor](/documentation/swiftui/uiapplicationdelegateadaptor)

#### Creating a delegate adaptor

- [init(_:)](/documentation/swiftui/uiapplicationdelegateadaptor/init(_:))

#### Getting the delegate adaptor

- [var projectedValue: ObservedObject<DelegateType>.Wrapper](/documentation/swiftui/uiapplicationdelegateadaptor/projectedvalue)
- [var wrappedValue: DelegateType](/documentation/swiftui/uiapplicationdelegateadaptor/wrappedvalue)

### Targeting macOS

- [NSApplicationDelegateAdaptor](/documentation/swiftui/nsapplicationdelegateadaptor)

#### Creating a delegate adaptor

- [init(_:)](/documentation/swiftui/nsapplicationdelegateadaptor/init(_:))

#### Getting the delegate adaptor

- [var projectedValue: ObservedObject<DelegateType>.Wrapper](/documentation/swiftui/nsapplicationdelegateadaptor/projectedvalue)
- [var wrappedValue: DelegateType](/documentation/swiftui/nsapplicationdelegateadaptor/wrappedvalue)

### Targeting watchOS

- [WKApplicationDelegateAdaptor](/documentation/swiftui/wkapplicationdelegateadaptor)

#### Creating a delegate adaptor

- [init(_:)](/documentation/swiftui/wkapplicationdelegateadaptor/init(_:))

#### Getting the delegate adaptor

- [var projectedValue: ObservedObject<DelegateType>.Wrapper](/documentation/swiftui/wkapplicationdelegateadaptor/projectedvalue)
- [var wrappedValue: DelegateType](/documentation/swiftui/wkapplicationdelegateadaptor/wrappedvalue)
- [WKExtensionDelegateAdaptor](/documentation/swiftui/wkextensiondelegateadaptor)

#### Creating a delegate adaptor

- [init(_:)](/documentation/swiftui/wkextensiondelegateadaptor/init(_:))

#### Getting the delegate adaptor

- [var projectedValue: ObservedObject<DelegateType>.Wrapper](/documentation/swiftui/wkextensiondelegateadaptor/projectedvalue)
- [var wrappedValue: DelegateType](/documentation/swiftui/wkextensiondelegateadaptor/wrappedvalue)

### Targeting tvOS

- [Creating a tvOS media catalog app in SwiftUI](/documentation/swiftui/creating-a-tvos-media-catalog-app-in-swiftui)

### Handling system recenter events

- [WorldRecenterPhase](/documentation/swiftui/worldrecenterphase)

#### Enumeration Cases

- [case began](/documentation/swiftui/worldrecenterphase/began)
- [case ended](/documentation/swiftui/worldrecenterphase/ended)
- [Scenes](/documentation/swiftui/scenes)

### Creating scenes

- [Scene](/documentation/swiftui/scene)

#### Creating a scene

- [var body: Self.Body](/documentation/swiftui/scene/body-swift.property)
- [Body](/documentation/swiftui/scene/body-swift.associatedtype)

#### Watching for changes

- [func onChange(of:initial:_:)](/documentation/swiftui/scene/onchange(of:initial:_:))
- [func handlesExternalEvents(matching: Set<String>) -> some Scene](/documentation/swiftui/scene/handlesexternalevents(matching:))

#### Creating background tasks

- [func backgroundTask<D, R>(BackgroundTask<D, R>, action: (D) async -> R) -> some Scene](/documentation/swiftui/scene/backgroundtask(_:action:))

#### Managing app storage

- [func defaultAppStorage(UserDefaults) -> some Scene](/documentation/swiftui/scene/defaultappstorage(_:))

#### Setting commands

- [func commands<Content>(content: () -> Content) -> some Scene](/documentation/swiftui/scene/commands(content:))
- [func commandsRemoved() -> some Scene](/documentation/swiftui/scene/commandsremoved())
- [func commandsReplaced<Content>(content: () -> Content) -> some Scene](/documentation/swiftui/scene/commandsreplaced(content:))
- [func keyboardShortcut(KeyboardShortcut?) -> some Scene](/documentation/swiftui/scene/keyboardshortcut(_:))
- [func keyboardShortcut(KeyEquivalent, modifiers: EventModifiers, localization: KeyboardShortcut.Localization) -> some Scene](/documentation/swiftui/scene/keyboardshortcut(_:modifiers:localization:))

#### Sizing and positioning the scene

- [func defaultPosition(UnitPoint) -> some Scene](/documentation/swiftui/scene/defaultposition(_:))
- [func defaultSize(_:)](/documentation/swiftui/scene/defaultsize(_:))
- [func defaultSize(width: CGFloat, height: CGFloat) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:))
- [func defaultSize(width: CGFloat, height: CGFloat, depth: CGFloat) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:depth:))
- [func defaultSize(Size3D, in: UnitLength) -> some Scene](/documentation/swiftui/scene/defaultsize(_:in:))
- [func defaultSize(width: CGFloat, height: CGFloat, depth: CGFloat, in: UnitLength) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:depth:in:))
- [func defaultWindowPlacement((WindowLayoutRoot, WindowPlacementContext) -> WindowPlacement) -> some Scene](/documentation/swiftui/scene/defaultwindowplacement(_:))
- [func windowResizability(WindowResizability) -> some Scene](/documentation/swiftui/scene/windowresizability(_:))
- [func windowIdealSize(WindowIdealSize) -> some Scene](/documentation/swiftui/scene/windowidealsize(_:))
- [func windowIdealPlacement((WindowLayoutRoot, WindowPlacementContext) -> WindowPlacement) -> some Scene](/documentation/swiftui/scene/windowidealplacement(_:))
- [func windowManagerRole(WindowManagerRole) -> some Scene](/documentation/swiftui/scene/windowmanagerrole(_:))

#### Interacting with volumes

- [func volumeWorldAlignment(WorldAlignmentBehavior) -> some Scene](/documentation/swiftui/scene/volumeworldalignment(_:))
- [func defaultWorldScaling(WorldScalingBehavior) -> some Scene](/documentation/swiftui/scene/defaultworldscaling(_:))

#### Configuring scene visibility

- [func defaultLaunchBehavior(SceneLaunchBehavior) -> some Scene](/documentation/swiftui/scene/defaultlaunchbehavior(_:))
- [func restorationBehavior(SceneRestorationBehavior) -> some Scene](/documentation/swiftui/scene/restorationbehavior(_:))
- [func persistentSystemOverlays(Visibility) -> some Scene](/documentation/swiftui/scene/persistentsystemoverlays(_:))

#### Styling the scene

- [func immersionStyle(selection: Binding<any ImmersionStyle>, in: any ImmersionStyle...) -> some Scene](/documentation/swiftui/scene/immersionstyle(selection:in:))
- [func upperLimbVisibility(Visibility) -> some Scene](/documentation/swiftui/scene/upperlimbvisibility(_:))
- [func windowStyle<S>(S) -> some Scene](/documentation/swiftui/scene/windowstyle(_:))
- [func windowLevel(WindowLevel) -> some Scene](/documentation/swiftui/scene/windowlevel(_:))
- [func windowToolbarStyle<S>(S) -> some Scene](/documentation/swiftui/scene/windowtoolbarstyle(_:))
- [func windowToolbarLabelStyle(Binding<ToolbarLabelStyle>) -> some Scene](/documentation/swiftui/scene/windowtoolbarlabelstyle(_:))
- [func windowToolbarLabelStyle(fixed: ToolbarLabelStyle) -> some Scene](/documentation/swiftui/scene/windowtoolbarlabelstyle(fixed:))

#### Configuring a data model

- [func modelContext(ModelContext) -> some Scene](/documentation/swiftui/scene/modelcontext(_:))
- [func modelContainer(ModelContainer) -> some Scene](/documentation/swiftui/scene/modelcontainer(_:))
- [func modelContainer(for:inMemory:isAutosaveEnabled:isUndoEnabled:onSetup:)](/documentation/swiftui/scene/modelcontainer(for:inmemory:isautosaveenabled:isundoenabled:onsetup:))

#### Managing the environment

- [func environment<T>(T?) -> some Scene](/documentation/swiftui/scene/environment(_:))
- [func environment<V>(WritableKeyPath<EnvironmentValues, V>, V) -> some Scene](/documentation/swiftui/scene/environment(_:_:))
- [func environmentObject<T>(T) -> some Scene](/documentation/swiftui/scene/environmentobject(_:))
- [func transformEnvironment<V>(WritableKeyPath<EnvironmentValues, V>, transform: (inout V) -> Void) -> some Scene](/documentation/swiftui/scene/transformenvironment(_:transform:))

#### Interacting with dialogs

- [func dialogIcon(Image?) -> some Scene](/documentation/swiftui/scene/dialogicon(_:))
- [func dialogSeverity(DialogSeverity) -> some Scene](/documentation/swiftui/scene/dialogseverity(_:))
- [func dialogSuppressionToggle(isSuppressed: Binding<Bool>) -> some Scene](/documentation/swiftui/scene/dialogsuppressiontoggle(issuppressed:))
- [func dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/scene/dialogsuppressiontoggle(_:issuppressed:))

#### Supporting drag behavior

- [func windowBackgroundDragBehavior(WindowInteractionBehavior) -> some Scene](/documentation/swiftui/scene/windowbackgrounddragbehavior(_:))

#### Deprecated symbols

- [func onChange<V>(of: V, perform: (V) -> Void) -> some Scene](/documentation/swiftui/scene/onchange(of:perform:))

#### Instance Methods

- [func documentBrowserContextMenu(([URL]?) -> some View) -> some Scene](/documentation/swiftui/scene/documentbrowsercontextmenu(_:))
- [func immersiveContentBrightness(ImmersiveContentBrightness) -> some Scene](/documentation/swiftui/scene/immersivecontentbrightness(_:))
- [func immersiveEnvironmentBehavior(ImmersiveEnvironmentBehavior) -> some Scene](/documentation/swiftui/scene/immersiveenvironmentbehavior(_:))
- [func menuBarExtraStyle<S>(S) -> some Scene](/documentation/swiftui/scene/menubarextrastyle(_:))
- [SceneBuilder](/documentation/swiftui/scenebuilder)

#### Building content

- [static buildBlock(_:)](/documentation/swiftui/scenebuilder/buildblock(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/scenebuilder/buildexpression(_:))
- [static buildLimitedAvailability(_:)](/documentation/swiftui/scenebuilder/buildlimitedavailability(_:))
- [static func buildOptional((any Scene & _LimitedAvailabilitySceneMarker)?) -> some Scene](/documentation/swiftui/scenebuilder/buildoptional(_:))

### Monitoring scene life cycle

- [var scenePhase: ScenePhase](/documentation/swiftui/environmentvalues/scenephase)
- [ScenePhase](/documentation/swiftui/scenephase)

#### Getting scene phases

- [case active](/documentation/swiftui/scenephase/active)
- [case inactive](/documentation/swiftui/scenephase/inactive)
- [case background](/documentation/swiftui/scenephase/background)

### Managing a settings window

- [Settings](/documentation/swiftui/settings)

#### Creating a settings scene

- [init(content: () -> Content)](/documentation/swiftui/settings/init(content:))
- [SettingsLink](/documentation/swiftui/settingslink)

#### Creating a settings link

- [init()](/documentation/swiftui/settingslink/init())
- [init(label: () -> Label)](/documentation/swiftui/settingslink/init(label:))

#### Supporting types

- [DefaultSettingsLinkLabel](/documentation/swiftui/defaultsettingslinklabel)
- [OpenSettingsAction](/documentation/swiftui/opensettingsaction)

#### Instance Methods

- [func callAsFunction()](/documentation/swiftui/opensettingsaction/callasfunction())
- [var openSettings: OpenSettingsAction](/documentation/swiftui/environmentvalues/opensettings)

### Building a menu bar

- [Building and customizing the menu bar with SwiftUI](/documentation/swiftui/building-and-customizing-the-menu-bar-with-swiftui)

### Creating a menu bar extra

- [MenuBarExtra](/documentation/swiftui/menubarextra)

#### Creating a menu bar extra

- [init(_:content:)](/documentation/swiftui/menubarextra/init(_:content:))
- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/menubarextra/init(content:label:))
- [init(_:isInserted:content:)](/documentation/swiftui/menubarextra/init(_:isinserted:content:))
- [init(isInserted: Binding<Bool>, content: () -> Content, label: () -> Label)](/documentation/swiftui/menubarextra/init(isinserted:content:label:))

#### Creating a menu bar extra with an image

- [init(_:image:content:)](/documentation/swiftui/menubarextra/init(_:image:content:))
- [init(_:image:isInserted:content:)](/documentation/swiftui/menubarextra/init(_:image:isinserted:content:))
- [init(_:systemImage:content:)](/documentation/swiftui/menubarextra/init(_:systemimage:content:))
- [init(_:systemImage:isInserted:content:)](/documentation/swiftui/menubarextra/init(_:systemimage:isinserted:content:))
- [func menuBarExtraStyle<S>(S) -> some Scene](/documentation/swiftui/scene/menubarextrastyle(_:))
- [MenuBarExtraStyle](/documentation/swiftui/menubarextrastyle)

#### Getting menu bar extra styles

- [static var automatic: AutomaticMenuBarExtraStyle](/documentation/swiftui/menubarextrastyle/automatic)
- [static var menu: PullDownMenuBarExtraStyle](/documentation/swiftui/menubarextrastyle/menu)
- [static var window: WindowMenuBarExtraStyle](/documentation/swiftui/menubarextrastyle/window)

#### Supporting types

- [AutomaticMenuBarExtraStyle](/documentation/swiftui/automaticmenubarextrastyle)

##### Creating the menu bar extra style

- [init()](/documentation/swiftui/automaticmenubarextrastyle/init())
- [PullDownMenuBarExtraStyle](/documentation/swiftui/pulldownmenubarextrastyle)

##### Creating the menu bar extra style

- [init()](/documentation/swiftui/pulldownmenubarextrastyle/init())
- [WindowMenuBarExtraStyle](/documentation/swiftui/windowmenubarextrastyle)

##### Creating the menu bar extra style

- [init()](/documentation/swiftui/windowmenubarextrastyle/init())

### Creating watch notifications

- [WKNotificationScene](/documentation/swiftui/wknotificationscene)

#### Creating a notification scene

- [init(controller: Controller.Type, category: String)](/documentation/swiftui/wknotificationscene/init(controller:category:))
- [Windows](/documentation/swiftui/windows)

### Essentials

- [Customizing window styles and state-restoration behavior in macOS](/documentation/swiftui/customizing-window-styles-and-state-restoration-behavior-in-macos)
- [Bringing multiple windows to your SwiftUI app](/documentation/swiftui/bringing-multiple-windows-to-your-swiftui-app)

### Creating windows

- [WindowGroup](/documentation/swiftui/windowgroup)

#### Creating a window group

- [init(content: () -> Content)](/documentation/swiftui/windowgroup/init(content:))
- [init(_:content:)](/documentation/swiftui/windowgroup/init(_:content:))

#### Identifying a window group

- [init(id: String, content: () -> Content)](/documentation/swiftui/windowgroup/init(id:content:))
- [init(_:id:content:)](/documentation/swiftui/windowgroup/init(_:id:content:))

#### Creating a data-driven window group

- [init<D, C>(for: D.Type, content: (Binding<D?>) -> C)](/documentation/swiftui/windowgroup/init(for:content:))
- [init(_:for:content:)](/documentation/swiftui/windowgroup/init(_:for:content:))

#### Providing default data to a window group

- [init<D, C>(for: D.Type, content: (Binding<D>) -> C, defaultValue: () -> D)](/documentation/swiftui/windowgroup/init(for:content:defaultvalue:))
- [init(_:for:content:defaultValue:)](/documentation/swiftui/windowgroup/init(_:for:content:defaultvalue:))

#### Identifying a data-driven window group

- [init<D, C>(id: String, for: D.Type, content: (Binding<D?>) -> C)](/documentation/swiftui/windowgroup/init(id:for:content:))
- [init(_:id:for:content:)](/documentation/swiftui/windowgroup/init(_:id:for:content:))

#### Identifying a window group that has default data

- [init<D, C>(id: String, for: D.Type, content: (Binding<D>) -> C, defaultValue: () -> D)](/documentation/swiftui/windowgroup/init(id:for:content:defaultvalue:))
- [init(_:id:for:content:defaultValue:)](/documentation/swiftui/windowgroup/init(_:id:for:content:defaultvalue:))

#### Supporting types

- [PresentedWindowContent](/documentation/swiftui/presentedwindowcontent)

#### Initializers

- [init(_:id:makeContent:)](/documentation/swiftui/windowgroup/init(_:id:makecontent:))
- [init(_:makeContent:)](/documentation/swiftui/windowgroup/init(_:makecontent:))
- [init(id: String, makeContent: () -> Content)](/documentation/swiftui/windowgroup/init(id:makecontent:))
- [init(makeContent: () -> Content)](/documentation/swiftui/windowgroup/init(makecontent:))
- [Window](/documentation/swiftui/window)

#### Creating a window

- [init(_:id:content:)](/documentation/swiftui/window/init(_:id:content:))
- [UtilityWindow](/documentation/swiftui/utilitywindow)

#### Initializers

- [init(_:id:content:)](/documentation/swiftui/utilitywindow/init(_:id:content:))
- [WindowStyle](/documentation/swiftui/windowstyle)

#### Getting built-in window styles

- [static var automatic: DefaultWindowStyle](/documentation/swiftui/windowstyle/automatic)
- [static var hiddenTitleBar: HiddenTitleBarWindowStyle](/documentation/swiftui/windowstyle/hiddentitlebar)
- [static var plain: PlainWindowStyle](/documentation/swiftui/windowstyle/plain)
- [static var titleBar: TitleBarWindowStyle](/documentation/swiftui/windowstyle/titlebar)
- [static var volumetric: VolumetricWindowStyle](/documentation/swiftui/windowstyle/volumetric)

#### Supporting types

- [DefaultWindowStyle](/documentation/swiftui/defaultwindowstyle)

##### Creating the window style

- [init()](/documentation/swiftui/defaultwindowstyle/init())
- [HiddenTitleBarWindowStyle](/documentation/swiftui/hiddentitlebarwindowstyle)

##### Creating the window style

- [init()](/documentation/swiftui/hiddentitlebarwindowstyle/init())
- [PlainWindowStyle](/documentation/swiftui/plainwindowstyle)

##### Creating the window style

- [init()](/documentation/swiftui/plainwindowstyle/init())
- [TitleBarWindowStyle](/documentation/swiftui/titlebarwindowstyle)

##### Creating the window style

- [init()](/documentation/swiftui/titlebarwindowstyle/init())
- [VolumetricWindowStyle](/documentation/swiftui/volumetricwindowstyle)

##### Creating the window style

- [init()](/documentation/swiftui/volumetricwindowstyle/init())
- [func windowStyle<S>(S) -> some Scene](/documentation/swiftui/scene/windowstyle(_:))

### Styling the associated toolbar

- [func windowToolbarStyle<S>(S) -> some Scene](/documentation/swiftui/scene/windowtoolbarstyle(_:))
- [func windowToolbarLabelStyle(Binding<ToolbarLabelStyle>) -> some Scene](/documentation/swiftui/scene/windowtoolbarlabelstyle(_:))
- [func windowToolbarLabelStyle(fixed: ToolbarLabelStyle) -> some Scene](/documentation/swiftui/scene/windowtoolbarlabelstyle(fixed:))
- [WindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle)

#### Getting built-in window toolbar styles

- [static var automatic: DefaultWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/automatic)
- [static var expanded: ExpandedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/expanded)
- [static var unified: UnifiedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unified)
- [static func unified(showsTitle: Bool) -> UnifiedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unified(showstitle:))
- [static var unifiedCompact: UnifiedCompactWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unifiedcompact)
- [static func unifiedCompact(showsTitle: Bool) -> UnifiedCompactWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unifiedcompact(showstitle:))

#### Supporting types

- [DefaultWindowToolbarStyle](/documentation/swiftui/defaultwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/defaultwindowtoolbarstyle/init())
- [ExpandedWindowToolbarStyle](/documentation/swiftui/expandedwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/expandedwindowtoolbarstyle/init())
- [UnifiedWindowToolbarStyle](/documentation/swiftui/unifiedwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/unifiedwindowtoolbarstyle/init())
- [init(showsTitle: Bool)](/documentation/swiftui/unifiedwindowtoolbarstyle/init(showstitle:))
- [UnifiedCompactWindowToolbarStyle](/documentation/swiftui/unifiedcompactwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/unifiedcompactwindowtoolbarstyle/init())
- [init(showsTitle: Bool)](/documentation/swiftui/unifiedcompactwindowtoolbarstyle/init(showstitle:))

### Opening windows

- [Presenting windows and spaces](/documentation/visionos/presenting-windows-and-spaces)
- [var supportsMultipleWindows: Bool](/documentation/swiftui/environmentvalues/supportsmultiplewindows)
- [var openWindow: OpenWindowAction](/documentation/swiftui/environmentvalues/openwindow)
- [OpenWindowAction](/documentation/swiftui/openwindowaction)

#### Calling the action

- [func callAsFunction(id: String)](/documentation/swiftui/openwindowaction/callasfunction(id:))
- [func callAsFunction<D>(id: String, value: D)](/documentation/swiftui/openwindowaction/callasfunction(id:value:))
- [func callAsFunction<D>(value: D)](/documentation/swiftui/openwindowaction/callasfunction(value:))

#### Structures

- [OpenWindowAction.SharingBehavior](/documentation/swiftui/openwindowaction/sharingbehavior)

##### Type Properties

- [static let requested: OpenWindowAction.SharingBehavior](/documentation/swiftui/openwindowaction/sharingbehavior/requested)
- [static let required: OpenWindowAction.SharingBehavior](/documentation/swiftui/openwindowaction/sharingbehavior/required)

#### Instance Methods

- [func callAsFunction(id: String, sharingBehavior: OpenWindowAction.SharingBehavior) async throws](/documentation/swiftui/openwindowaction/callasfunction(id:sharingbehavior:))
- [func callAsFunction<D>(id: String, value: D, sharingBehavior: OpenWindowAction.SharingBehavior) async throws](/documentation/swiftui/openwindowaction/callasfunction(id:value:sharingbehavior:))
- [func callAsFunction<D>(value: D, sharingBehavior: OpenWindowAction.SharingBehavior) async throws](/documentation/swiftui/openwindowaction/callasfunction(value:sharingbehavior:))
- [PushWindowAction](/documentation/swiftui/pushwindowaction)

#### Instance Methods

- [func callAsFunction(id: String)](/documentation/swiftui/pushwindowaction/callasfunction(id:))
- [func callAsFunction<D>(id: String, value: D)](/documentation/swiftui/pushwindowaction/callasfunction(id:value:))
- [func callAsFunction<D>(value: D)](/documentation/swiftui/pushwindowaction/callasfunction(value:))

### Closing windows

- [var dismissWindow: DismissWindowAction](/documentation/swiftui/environmentvalues/dismisswindow)
- [DismissWindowAction](/documentation/swiftui/dismisswindowaction)

#### Calling the action

- [func callAsFunction()](/documentation/swiftui/dismisswindowaction/callasfunction())
- [func callAsFunction(id: String)](/documentation/swiftui/dismisswindowaction/callasfunction(id:))
- [func callAsFunction<D>(id: String, value: D)](/documentation/swiftui/dismisswindowaction/callasfunction(id:value:))
- [func callAsFunction<D>(value: D)](/documentation/swiftui/dismisswindowaction/callasfunction(value:))
- [var dismiss: DismissAction](/documentation/swiftui/environmentvalues/dismiss)
- [DismissAction](/documentation/swiftui/dismissaction)

#### Calling the action

- [func callAsFunction()](/documentation/swiftui/dismissaction/callasfunction())
- [DismissBehavior](/documentation/swiftui/dismissbehavior)

#### Getting behaviors

- [static let destructive: DismissBehavior](/documentation/swiftui/dismissbehavior/destructive)
- [static let interactive: DismissBehavior](/documentation/swiftui/dismissbehavior/interactive)

### Sizing a window

- [Positioning and sizing windows](/documentation/visionos/positioning-and-sizing-windows)
- [func defaultSize(_:)](/documentation/swiftui/scene/defaultsize(_:))
- [func defaultSize(width: CGFloat, height: CGFloat) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:))
- [func defaultSize(width: CGFloat, height: CGFloat, depth: CGFloat) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:depth:))
- [func defaultSize(Size3D, in: UnitLength) -> some Scene](/documentation/swiftui/scene/defaultsize(_:in:))
- [func defaultSize(width: CGFloat, height: CGFloat, depth: CGFloat, in: UnitLength) -> some Scene](/documentation/swiftui/scene/defaultsize(width:height:depth:in:))
- [func windowResizability(WindowResizability) -> some Scene](/documentation/swiftui/scene/windowresizability(_:))
- [WindowResizability](/documentation/swiftui/windowresizability)

#### Getting the resizability

- [static var automatic: WindowResizability](/documentation/swiftui/windowresizability/automatic)
- [static var contentMinSize: WindowResizability](/documentation/swiftui/windowresizability/contentminsize)
- [static var contentSize: WindowResizability](/documentation/swiftui/windowresizability/contentsize)
- [func windowIdealSize(WindowIdealSize) -> some Scene](/documentation/swiftui/scene/windowidealsize(_:))
- [WindowIdealSize](/documentation/swiftui/windowidealsize)

#### Type Properties

- [static let automatic: WindowIdealSize](/documentation/swiftui/windowidealsize/automatic)
- [static let fitToContent: WindowIdealSize](/documentation/swiftui/windowidealsize/fittocontent)
- [static let maximum: WindowIdealSize](/documentation/swiftui/windowidealsize/maximum)

### Positioning a window

- [func defaultPosition(UnitPoint) -> some Scene](/documentation/swiftui/scene/defaultposition(_:))
- [WindowLevel](/documentation/swiftui/windowlevel)

#### Type Properties

- [static var automatic: WindowLevel](/documentation/swiftui/windowlevel/automatic)
- [static var desktop: WindowLevel](/documentation/swiftui/windowlevel/desktop)
- [static var floating: WindowLevel](/documentation/swiftui/windowlevel/floating)
- [static var normal: WindowLevel](/documentation/swiftui/windowlevel/normal)
- [func windowLevel(WindowLevel) -> some Scene](/documentation/swiftui/scene/windowlevel(_:))
- [WindowLayoutRoot](/documentation/swiftui/windowlayoutroot)

#### Instance Methods

- [func sizeThatFits(ProposedViewSize) -> CGSize](/documentation/swiftui/windowlayoutroot/sizethatfits(_:))
- [WindowPlacement](/documentation/swiftui/windowplacement)

#### Structures

- [WindowPlacement.Position](/documentation/swiftui/windowplacement/position)

##### Type Properties

- [static var utilityPanel: WindowPlacement.Position](/documentation/swiftui/windowplacement/position/utilitypanel)

##### Type Methods

- [static func above(WindowProxy) -> WindowPlacement.Position](/documentation/swiftui/windowplacement/position/above(_:))
- [static func below(WindowProxy) -> WindowPlacement.Position](/documentation/swiftui/windowplacement/position/below(_:))
- [static func leading(WindowProxy) -> WindowPlacement.Position](/documentation/swiftui/windowplacement/position/leading(_:))
- [static func replacing(WindowProxy) -> WindowPlacement.Position](/documentation/swiftui/windowplacement/position/replacing(_:))
- [static func trailing(WindowProxy) -> WindowPlacement.Position](/documentation/swiftui/windowplacement/position/trailing(_:))

#### Initializers

- [init(WindowPlacement.Position?)](/documentation/swiftui/windowplacement/init(_:))
- [init(WindowPlacement.Position?, size3D: Size3D?)](/documentation/swiftui/windowplacement/init(_:size3d:))
- [init(_:size:)](/documentation/swiftui/windowplacement/init(_:size:))
- [init(UnitPoint, width: CGFloat?, height: CGFloat?)](/documentation/swiftui/windowplacement/init(_:width:height:))
- [init(WindowPlacement.Position?, width: CGFloat?, height: CGFloat?, depth: CGFloat?)](/documentation/swiftui/windowplacement/init(_:width:height:depth:))
- [init(x: CGFloat?, y: CGFloat?, width: CGFloat?, height: CGFloat?)](/documentation/swiftui/windowplacement/init(x:y:width:height:))
- [func defaultWindowPlacement((WindowLayoutRoot, WindowPlacementContext) -> WindowPlacement) -> some Scene](/documentation/swiftui/scene/defaultwindowplacement(_:))
- [func windowIdealPlacement((WindowLayoutRoot, WindowPlacementContext) -> WindowPlacement) -> some Scene](/documentation/swiftui/scene/windowidealplacement(_:))
- [WindowPlacementContext](/documentation/swiftui/windowplacementcontext)

#### Instance Properties

- [var defaultDisplay: DisplayProxy](/documentation/swiftui/windowplacementcontext/defaultdisplay)
- [var windows: [WindowProxy]](/documentation/swiftui/windowplacementcontext/windows)
- [WindowProxy](/documentation/swiftui/windowproxy)

#### Instance Properties

- [var id: String?](/documentation/swiftui/windowproxy/id)
- [var phase: ScenePhase](/documentation/swiftui/windowproxy/phase)
- [DisplayProxy](/documentation/swiftui/displayproxy)

#### Instance Properties

- [let bounds: CGRect](/documentation/swiftui/displayproxy/bounds)
- [let safeAreaInsets: EdgeInsets](/documentation/swiftui/displayproxy/safeareainsets)
- [let visibleRect: CGRect](/documentation/swiftui/displayproxy/visiblerect)

### Configuring window visibility

- [WindowVisibilityToggle](/documentation/swiftui/windowvisibilitytoggle)

#### Creating a window visibility toggle

- [init(windowID: String)](/documentation/swiftui/windowvisibilitytoggle/init(windowid:))

#### Supporting types

- [DefaultWindowVisibilityToggleLabel](/documentation/swiftui/defaultwindowvisibilitytogglelabel)
- [func defaultLaunchBehavior(SceneLaunchBehavior) -> some Scene](/documentation/swiftui/scene/defaultlaunchbehavior(_:))
- [func restorationBehavior(SceneRestorationBehavior) -> some Scene](/documentation/swiftui/scene/restorationbehavior(_:))
- [SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior)

#### Type Properties

- [static let automatic: SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior/automatic)
- [static let presented: SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior/presented)
- [static let suppressed: SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior/suppressed)
- [SceneRestorationBehavior](/documentation/swiftui/scenerestorationbehavior)

#### Type Properties

- [static let automatic: SceneRestorationBehavior](/documentation/swiftui/scenerestorationbehavior/automatic)
- [static let disabled: SceneRestorationBehavior](/documentation/swiftui/scenerestorationbehavior/disabled)
- [func persistentSystemOverlays(Visibility) -> some Scene](/documentation/swiftui/scene/persistentsystemoverlays(_:))
- [func windowToolbarFullScreenVisibility(WindowToolbarFullScreenVisibility) -> some View](/documentation/swiftui/view/windowtoolbarfullscreenvisibility(_:))
- [WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility)

#### Type Properties

- [static let automatic: WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility/automatic)
- [static let onHover: WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility/onhover)
- [static let visible: WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility/visible)

### Managing window behavior

- [WindowManagerRole](/documentation/swiftui/windowmanagerrole)

#### Type Properties

- [static let associated: WindowManagerRole](/documentation/swiftui/windowmanagerrole/associated)
- [static let automatic: WindowManagerRole](/documentation/swiftui/windowmanagerrole/automatic)
- [static let principal: WindowManagerRole](/documentation/swiftui/windowmanagerrole/principal)
- [func windowManagerRole(WindowManagerRole) -> some Scene](/documentation/swiftui/scene/windowmanagerrole(_:))
- [WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior)

#### Type Properties

- [static let automatic: WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior/automatic)
- [static let disabled: WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior/disabled)
- [static let enabled: WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior/enabled)
- [func windowDismissBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowdismissbehavior(_:))
- [func windowFullScreenBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowfullscreenbehavior(_:))
- [func windowMinimizeBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowminimizebehavior(_:))
- [func windowResizeBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowresizebehavior(_:))
- [func windowBackgroundDragBehavior(WindowInteractionBehavior) -> some Scene](/documentation/swiftui/scene/windowbackgrounddragbehavior(_:))

### Interacting with volumes

- [func onVolumeViewpointChange(updateStrategy: VolumeViewpointUpdateStrategy, initial: Bool, (Viewpoint3D, Viewpoint3D) -> Void) -> some View](/documentation/swiftui/view/onvolumeviewpointchange(updatestrategy:initial:_:))
- [func supportedVolumeViewpoints(SquareAzimuth.Set) -> some View](/documentation/swiftui/view/supportedvolumeviewpoints(_:))
- [VolumeViewpointUpdateStrategy](/documentation/swiftui/volumeviewpointupdatestrategy)

#### Type Properties

- [static let all: VolumeViewpointUpdateStrategy](/documentation/swiftui/volumeviewpointupdatestrategy/all)
- [static let supported: VolumeViewpointUpdateStrategy](/documentation/swiftui/volumeviewpointupdatestrategy/supported)
- [Viewpoint3D](/documentation/swiftui/viewpoint3d)

#### Instance Properties

- [var squareAzimuth: SquareAzimuth](/documentation/swiftui/viewpoint3d/squareazimuth)

#### Type Properties

- [static let standard: Viewpoint3D](/documentation/swiftui/viewpoint3d/standard)
- [SquareAzimuth](/documentation/swiftui/squareazimuth)

#### Structures

- [SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set)

##### Initializers

- [init(SquareAzimuth)](/documentation/swiftui/squareazimuth/set/init(_:))

##### Instance Methods

- [func contains(SquareAzimuth) -> Bool](/documentation/swiftui/squareazimuth/set/contains(_:))

##### Type Properties

- [static let all: SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set/all)
- [static let back: SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set/back)
- [static let front: SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set/front)
- [static let left: SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set/left)
- [static let right: SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set/right)

#### Enumeration Cases

- [case back](/documentation/swiftui/squareazimuth/back)
- [case front](/documentation/swiftui/squareazimuth/front)
- [case left](/documentation/swiftui/squareazimuth/left)
- [case right](/documentation/swiftui/squareazimuth/right)

#### Initializers

- [init(closestToAzimuth: Angle)](/documentation/swiftui/squareazimuth/init(closesttoazimuth:))

#### Instance Properties

- [var orientation: Rotation3D](/documentation/swiftui/squareazimuth/orientation)
- [WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior)

#### Type Properties

- [static var adaptive: WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior/adaptive)
- [static var automatic: WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior/automatic)
- [static var gravityAligned: WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior/gravityaligned)
- [func volumeWorldAlignment(WorldAlignmentBehavior) -> some Scene](/documentation/swiftui/scene/volumeworldalignment(_:))
- [WorldScalingBehavior](/documentation/swiftui/worldscalingbehavior)

#### Type Properties

- [static var automatic: WorldScalingBehavior](/documentation/swiftui/worldscalingbehavior/automatic)
- [static var dynamic: WorldScalingBehavior](/documentation/swiftui/worldscalingbehavior/dynamic)
- [func defaultWorldScaling(WorldScalingBehavior) -> some Scene](/documentation/swiftui/scene/defaultworldscaling(_:))
- [WorldScalingCompensation](/documentation/swiftui/worldscalingcompensation)

#### Type Properties

- [static let scaled: WorldScalingCompensation](/documentation/swiftui/worldscalingcompensation/scaled)
- [static let unscaled: WorldScalingCompensation](/documentation/swiftui/worldscalingcompensation/unscaled)
- [var worldTrackingLimitations: Set<WorldTrackingLimitation>](/documentation/swiftui/environmentvalues/worldtrackinglimitations)
- [WorldTrackingLimitation](/documentation/swiftui/worldtrackinglimitation)

#### Type Properties

- [static let orientation: WorldTrackingLimitation](/documentation/swiftui/worldtrackinglimitation/orientation)
- [static let translation: WorldTrackingLimitation](/documentation/swiftui/worldtrackinglimitation/translation)
- [SurfaceSnappingInfo](/documentation/swiftui/surfacesnappinginfo)

#### Instance Properties

- [var classification: SurfaceClassification?](/documentation/swiftui/surfacesnappinginfo/classification)
- [var isSnapped: Bool](/documentation/swiftui/surfacesnappinginfo/issnapped)

#### Type Properties

- [static var authorizationStatus: SurfaceSnappingInfo.AuthorizationStatus](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.type.property)

#### Enumerations

- [SurfaceSnappingInfo.AuthorizationStatus](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.enum)

##### Enumeration Cases

- [case authorized](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.enum/authorized)
- [case denied](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.enum/denied)
- [case notDetermined](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.enum/notdetermined)
- [case restricted](/documentation/swiftui/surfacesnappinginfo/authorizationstatus-swift.enum/restricted)

### Deprecated Types

- [ControlActiveState](/documentation/swiftui/controlactivestate)

#### Getting control active states

- [case key](/documentation/swiftui/controlactivestate/key)
- [case active](/documentation/swiftui/controlactivestate/active)
- [case inactive](/documentation/swiftui/controlactivestate/inactive)
- [Immersive spaces](/documentation/swiftui/immersive-spaces)

### Creating an immersive space

- [ImmersiveSpace](/documentation/swiftui/immersivespace)

#### Creating an immersive space

- [init(content:)](/documentation/swiftui/immersivespace/init(content:))

#### Identifying an immersive space

- [init(id:content:)](/documentation/swiftui/immersivespace/init(id:content:))

#### Creating a data-driven immersive space

- [init(for:content:)](/documentation/swiftui/immersivespace/init(for:content:))
- [init(id:for:content:)](/documentation/swiftui/immersivespace/init(id:for:content:))

#### Providing default data to an immersive space

- [init(for:content:defaultValue:)](/documentation/swiftui/immersivespace/init(for:content:defaultvalue:))
- [init(id:for:content:defaultValue:)](/documentation/swiftui/immersivespace/init(id:for:content:defaultvalue:))

#### Supporting types

- [ImmersiveSpaceViewContent](/documentation/swiftui/immersivespaceviewcontent)
- [ImmersiveSpaceContent](/documentation/swiftui/immersivespacecontent)

##### Creating immersive space content

- [var body: Self.Body](/documentation/swiftui/immersivespacecontent/body-swift.property)
- [Body](/documentation/swiftui/immersivespacecontent/body-swift.associatedtype)

#### Initializers

- [init<C>(for: Data.Type, makeContent: (Binding<Data?>) -> C)](/documentation/swiftui/immersivespace/init(for:makecontent:))
- [init<C>(for: Data.Type, makeContent: (Binding<Data>) -> C, defaultValue: () -> Data)](/documentation/swiftui/immersivespace/init(for:makecontent:defaultvalue:))
- [init(foveatedStreaming: FoveatedStreamingSession)](/documentation/swiftui/immersivespace/init(foveatedstreaming:))
- [init<V>(foveatedStreaming: FoveatedStreamingSession, content: () -> V)](/documentation/swiftui/immersivespace/init(foveatedstreaming:content:))
- [init<C>(id: String, for: Data.Type, makeContent: (Binding<Data?>) -> C)](/documentation/swiftui/immersivespace/init(id:for:makecontent:))
- [init<C>(id: String, for: Data.Type, makeContent: (Binding<Data>) -> C, defaultValue: () -> Data)](/documentation/swiftui/immersivespace/init(id:for:makecontent:defaultvalue:))
- [init(id:makeContent:)](/documentation/swiftui/immersivespace/init(id:makecontent:))
- [init<C>(makeContent: () -> C)](/documentation/swiftui/immersivespace/init(makecontent:))
- [ImmersiveSpaceContentBuilder](/documentation/swiftui/immersivespacecontentbuilder)

#### Building content

- [static func buildBlock<Content>(Content) -> Content](/documentation/swiftui/immersivespacecontentbuilder/buildblock(_:))
- [func immersionStyle(selection: Binding<any ImmersionStyle>, in: any ImmersionStyle...) -> some Scene](/documentation/swiftui/scene/immersionstyle(selection:in:))
- [ImmersionStyle](/documentation/swiftui/immersionstyle)

#### Getting built-in styles

- [static var automatic: AutomaticImmersionStyle](/documentation/swiftui/immersionstyle/automatic)
- [static var full: FullImmersionStyle](/documentation/swiftui/immersionstyle/full)
- [static var mixed: MixedImmersionStyle](/documentation/swiftui/immersionstyle/mixed)
- [static var progressive: ProgressiveImmersionStyle](/documentation/swiftui/immersionstyle/progressive)

#### Supporting types

- [AutomaticImmersionStyle](/documentation/swiftui/automaticimmersionstyle)

##### Creating the immersion style

- [init()](/documentation/swiftui/automaticimmersionstyle/init())
- [FullImmersionStyle](/documentation/swiftui/fullimmersionstyle)

##### Creating the immersion style

- [init()](/documentation/swiftui/fullimmersionstyle/init())
- [MixedImmersionStyle](/documentation/swiftui/mixedimmersionstyle)

##### Creating the immersion style

- [init()](/documentation/swiftui/mixedimmersionstyle/init())
- [ProgressiveImmersionStyle](/documentation/swiftui/progressiveimmersionstyle)

##### Creating the immersion style

- [init()](/documentation/swiftui/progressiveimmersionstyle/init())

##### Initializers

- [init(immersion:initialAmount:)](/documentation/swiftui/progressiveimmersionstyle/init(immersion:initialamount:))

##### Instance Properties

- [let aspectRatio: ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionstyle/aspectratio)
- [let initialImmersionAmount: Double?](/documentation/swiftui/progressiveimmersionstyle/initialimmersionamount)
- [let maximumImmersionAmount: Double?](/documentation/swiftui/progressiveimmersionstyle/maximumimmersionamount)
- [let minimumImmersionAmount: Double?](/documentation/swiftui/progressiveimmersionstyle/minimumimmersionamount)

#### Type Methods

- [static progressive(_:initialAmount:)](/documentation/swiftui/immersionstyle/progressive(_:initialamount:))
- [static progressive(_:initialAmount:aspectRatio:)](/documentation/swiftui/immersionstyle/progressive(_:initialamount:aspectratio:))
- [static func progressive(aspectRatio: ProgressiveImmersionAspectRatio) -> ProgressiveImmersionStyle](/documentation/swiftui/immersionstyle/progressive(aspectratio:))
- [var immersiveSpaceDisplacement: Pose3D](/documentation/swiftui/environmentvalues/immersivespacedisplacement)
- [ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior)

#### Type Properties

- [static var automatic: ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior/automatic)
- [static var coexist: ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior/coexist)
- [static var replace: ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior/replace)
- [ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio)

#### Type Properties

- [static var automatic: ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio/automatic)
- [static var landscape: ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio/landscape)
- [static var portrait: ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio/portrait)

### Opening an immersive space

- [var openImmersiveSpace: OpenImmersiveSpaceAction](/documentation/swiftui/environmentvalues/openimmersivespace)
- [OpenImmersiveSpaceAction](/documentation/swiftui/openimmersivespaceaction)

#### Calling the action

- [func callAsFunction(id: String) async -> OpenImmersiveSpaceAction.Result](/documentation/swiftui/openimmersivespaceaction/callasfunction(id:))
- [func callAsFunction<D>(id: String, value: D) async -> OpenImmersiveSpaceAction.Result](/documentation/swiftui/openimmersivespaceaction/callasfunction(id:value:))
- [func callAsFunction<D>(value: D) async -> OpenImmersiveSpaceAction.Result](/documentation/swiftui/openimmersivespaceaction/callasfunction(value:))

#### Getting the result

- [OpenImmersiveSpaceAction.Result](/documentation/swiftui/openimmersivespaceaction/result)

##### Getting the result

- [case opened](/documentation/swiftui/openimmersivespaceaction/result/opened)
- [case userCancelled](/documentation/swiftui/openimmersivespaceaction/result/usercancelled)
- [case error](/documentation/swiftui/openimmersivespaceaction/result/error)

#### Instance Methods

- [func callAsFunction(foveatedStreaming: FoveatedStreamingSession) async -> OpenImmersiveSpaceAction.Result](/documentation/swiftui/openimmersivespaceaction/callasfunction(foveatedstreaming:))

### Closing the immersive space

- [var dismissImmersiveSpace: DismissImmersiveSpaceAction](/documentation/swiftui/environmentvalues/dismissimmersivespace)
- [DismissImmersiveSpaceAction](/documentation/swiftui/dismissimmersivespaceaction)

#### Calling the action

- [func callAsFunction() async](/documentation/swiftui/dismissimmersivespaceaction/callasfunction())

### Hiding upper limbs during immersion

- [func upperLimbVisibility(Visibility) -> some Scene](/documentation/swiftui/scene/upperlimbvisibility(_:))
- [func upperLimbVisibility(Visibility) -> some View](/documentation/swiftui/view/upperlimbvisibility(_:))

### Adjusting content brightness

- [func immersiveContentBrightness(ImmersiveContentBrightness) -> some Scene](/documentation/swiftui/scene/immersivecontentbrightness(_:))
- [ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness)

#### Getting brightness levels

- [static let automatic: ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness/automatic)
- [static let dark: ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness/dark)
- [static let dim: ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness/dim)
- [static let bright: ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness/bright)
- [static func custom(Double) -> ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness/custom(_:))

### Responding to immersion changes

- [func onImmersionChange(initial: Bool, (ImmersionChangeContext, ImmersionChangeContext) -> Void) -> some View](/documentation/swiftui/view/onimmersionchange(initial:_:))
- [ImmersionChangeContext](/documentation/swiftui/immersionchangecontext)

#### Instance Properties

- [let amount: Double?](/documentation/swiftui/immersionchangecontext/amount)

### Adding menu items to an immersive space

- [func immersiveEnvironmentPicker<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/immersiveenvironmentpicker(content:))

### Handling remote immersive spaces

- [RemoteImmersiveSpace](/documentation/swiftui/remoteimmersivespace)

#### Initializers

- [init<C>(content: () -> C)](/documentation/swiftui/remoteimmersivespace/init(content:))
- [init<C>(for: Data.Type, content: (Binding<Data?>) -> C)](/documentation/swiftui/remoteimmersivespace/init(for:content:))
- [init<C>(for: Data.Type, content: (Binding<Data>) -> C, defaultValue: () -> Data)](/documentation/swiftui/remoteimmersivespace/init(for:content:defaultvalue:))
- [init<C>(id: String, content: () -> C)](/documentation/swiftui/remoteimmersivespace/init(id:content:))
- [init<C>(id: String, for: Data.Type, content: (Binding<Data?>) -> C)](/documentation/swiftui/remoteimmersivespace/init(id:for:content:))
- [init<C>(id: String, for: Data.Type, content: (Binding<Data>) -> C, defaultValue: () -> Data)](/documentation/swiftui/remoteimmersivespace/init(id:for:content:defaultvalue:))
- [RemoteDeviceIdentifier](/documentation/swiftui/remotedeviceidentifier)

#### Instance Properties

- [var cDevice: ar_device_t](/documentation/swiftui/remotedeviceidentifier/cdevice)
- [Documents](/documentation/swiftui/documents)

### Creating a document

- [Building a document-based app with SwiftUI](/documentation/swiftui/building-a-document-based-app-with-swiftui)
- [Building a document-based app using SwiftData](/documentation/swiftui/building-a-document-based-app-using-swiftdata)
- [DocumentGroup](/documentation/swiftui/documentgroup)

#### Creating a document group

- [init(newDocument:editor:)](/documentation/swiftui/documentgroup/init(newdocument:editor:))
- [init(viewing:viewer:)](/documentation/swiftui/documentgroup/init(viewing:viewer:))

#### Editing a document backed by a persistent store

- [init(editing:contentType:editor:prepareDocument:)](/documentation/swiftui/documentgroup/init(editing:contenttype:editor:preparedocument:))
- [init(editing: UTType, migrationPlan: any SchemaMigrationPlan.Type, editor: () -> Content, prepareDocument: (ModelContext) -> Void)](/documentation/swiftui/documentgroup/init(editing:migrationplan:editor:preparedocument:))

#### Viewing a document backed by a persistent store

- [init(viewing:contentType:viewer:)](/documentation/swiftui/documentgroup/init(viewing:contenttype:viewer:))
- [init(viewing: UTType, migrationPlan: any SchemaMigrationPlan.Type, viewer: () -> Content)](/documentation/swiftui/documentgroup/init(viewing:migrationplan:viewer:))

### Storing document data in a structure instance

- [FileDocument](/documentation/swiftui/filedocument)

#### Reading a document

- [init(configuration: Self.ReadConfiguration) throws](/documentation/swiftui/filedocument/init(configuration:))
- [static var readableContentTypes: [UTType]](/documentation/swiftui/filedocument/readablecontenttypes)
- [FileDocument.ReadConfiguration](/documentation/swiftui/filedocument/readconfiguration)

#### Writing a document

- [func fileWrapper(configuration: Self.WriteConfiguration) throws -> FileWrapper](/documentation/swiftui/filedocument/filewrapper(configuration:))
- [static var writableContentTypes: [UTType]](/documentation/swiftui/filedocument/writablecontenttypes)
- [FileDocument.WriteConfiguration](/documentation/swiftui/filedocument/writeconfiguration)
- [FileDocumentConfiguration](/documentation/swiftui/filedocumentconfiguration)

#### Getting and setting the document

- [var document: Document](/documentation/swiftui/filedocumentconfiguration/document)
- [var $document: Binding<Document>](/documentation/swiftui/filedocumentconfiguration/$document)

#### Getting document properties

- [var fileURL: URL?](/documentation/swiftui/filedocumentconfiguration/fileurl)
- [var isEditable: Bool](/documentation/swiftui/filedocumentconfiguration/iseditable)

### Storing document data in a class instance

- [ReferenceFileDocument](/documentation/swiftui/referencefiledocument)

#### Reading a document

- [init(configuration: Self.ReadConfiguration) throws](/documentation/swiftui/referencefiledocument/init(configuration:))
- [static var readableContentTypes: [UTType]](/documentation/swiftui/referencefiledocument/readablecontenttypes)
- [ReferenceFileDocument.ReadConfiguration](/documentation/swiftui/referencefiledocument/readconfiguration)

#### Getting a snapshot

- [func snapshot(contentType: UTType) throws -> Self.Snapshot](/documentation/swiftui/referencefiledocument/snapshot(contenttype:))
- [Snapshot](/documentation/swiftui/referencefiledocument/snapshot)

#### Writing a document

- [func fileWrapper(snapshot: Self.Snapshot, configuration: Self.WriteConfiguration) throws -> FileWrapper](/documentation/swiftui/referencefiledocument/filewrapper(snapshot:configuration:))
- [static var writableContentTypes: [UTType]](/documentation/swiftui/referencefiledocument/writablecontenttypes)
- [ReferenceFileDocument.WriteConfiguration](/documentation/swiftui/referencefiledocument/writeconfiguration)
- [ReferenceFileDocumentConfiguration](/documentation/swiftui/referencefiledocumentconfiguration)

#### Getting and setting the document

- [var document: Document](/documentation/swiftui/referencefiledocumentconfiguration/document)
- [var $document: ObservedObject<Document>.Wrapper](/documentation/swiftui/referencefiledocumentconfiguration/$document)

#### Getting document properties

- [var fileURL: URL?](/documentation/swiftui/referencefiledocumentconfiguration/fileurl)
- [var isEditable: Bool](/documentation/swiftui/referencefiledocumentconfiguration/iseditable)
- [var undoManager: UndoManager?](/documentation/swiftui/environmentvalues/undomanager)

### Accessing document configuration

- [var documentConfiguration: DocumentConfiguration?](/documentation/swiftui/environmentvalues/documentconfiguration)
- [DocumentConfiguration](/documentation/swiftui/documentconfiguration)

#### Getting configuration values

- [var fileURL: URL?](/documentation/swiftui/documentconfiguration/fileurl)
- [var isEditable: Bool](/documentation/swiftui/documentconfiguration/iseditable)

### Reading and writing documents

- [FileDocumentReadConfiguration](/documentation/swiftui/filedocumentreadconfiguration)

#### Reading the content

- [let contentType: UTType](/documentation/swiftui/filedocumentreadconfiguration/contenttype)
- [let file: FileWrapper](/documentation/swiftui/filedocumentreadconfiguration/file)
- [FileDocumentWriteConfiguration](/documentation/swiftui/filedocumentwriteconfiguration)

#### Writing the content

- [let contentType: UTType](/documentation/swiftui/filedocumentwriteconfiguration/contenttype)
- [let existingFile: FileWrapper?](/documentation/swiftui/filedocumentwriteconfiguration/existingfile)

### Opening a document programmatically

- [var newDocument: NewDocumentAction](/documentation/swiftui/environmentvalues/newdocument)
- [NewDocumentAction](/documentation/swiftui/newdocumentaction)

#### Calling the action

- [func callAsFunction(_:)](/documentation/swiftui/newdocumentaction/callasfunction(_:))
- [func callAsFunction(contentType: UTType)](/documentation/swiftui/newdocumentaction/callasfunction(contenttype:))
- [func callAsFunction(contentType: UTType, prepareDocument: (ModelContext) -> Void)](/documentation/swiftui/newdocumentaction/callasfunction(contenttype:preparedocument:))
- [var openDocument: OpenDocumentAction](/documentation/swiftui/environmentvalues/opendocument)
- [OpenDocumentAction](/documentation/swiftui/opendocumentaction)

#### Calling the action

- [func callAsFunction(at: URL) async throws](/documentation/swiftui/opendocumentaction/callasfunction(at:))

### Configuring the document launch experience

- [DocumentGroupLaunchScene](/documentation/swiftui/documentgrouplaunchscene)

#### Initializers

- [init(_:_:background:)](/documentation/swiftui/documentgrouplaunchscene/init(_:_:background:))
- [init(_:_:background:backgroundAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:_:background:backgroundaccessoryview:))
- [init(_:_:background:backgroundAccessoryView:overlayAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:_:background:backgroundaccessoryview:overlayaccessoryview:))
- [init(_:_:background:overlayAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:_:background:overlayaccessoryview:))
- [init(_:backgroundStyle:_:)](/documentation/swiftui/documentgrouplaunchscene/init(_:backgroundstyle:_:))
- [init(_:backgroundStyle:_:backgroundAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:backgroundstyle:_:backgroundaccessoryview:))
- [init(_:backgroundStyle:_:backgroundAccessoryView:overlayAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:backgroundstyle:_:backgroundaccessoryview:overlayaccessoryview:))
- [init(_:backgroundStyle:_:overlayAccessoryView:)](/documentation/swiftui/documentgrouplaunchscene/init(_:backgroundstyle:_:overlayaccessoryview:))
- [DocumentLaunchView](/documentation/swiftui/documentlaunchview)

#### Initializers

- [init(_:for:_:onDocumentOpen:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:))
- [init(_:for:_:onDocumentOpen:background:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:background:))
- [init(_:for:_:onDocumentOpen:background:backgroundAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:background:backgroundaccessoryview:))
- [init(_:for:_:onDocumentOpen:background:backgroundAccessoryView:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:background:backgroundaccessoryview:overlayaccessoryview:))
- [init(_:for:_:onDocumentOpen:background:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:background:overlayaccessoryview:))
- [init(_:for:_:onDocumentOpen:backgroundAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:backgroundaccessoryview:))
- [init(_:for:_:onDocumentOpen:backgroundAccessoryView:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:backgroundaccessoryview:overlayaccessoryview:))
- [init(_:for:_:onDocumentOpen:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:_:ondocumentopen:overlayaccessoryview:))
- [init(_:for:backgroundStyle:_:onDocumentOpen:)](/documentation/swiftui/documentlaunchview/init(_:for:backgroundstyle:_:ondocumentopen:))
- [init(_:for:backgroundStyle:_:onDocumentOpen:backgroundAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:backgroundstyle:_:ondocumentopen:backgroundaccessoryview:))
- [init(_:for:backgroundStyle:_:onDocumentOpen:backgroundAccessoryView:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:backgroundstyle:_:ondocumentopen:backgroundaccessoryview:overlayaccessoryview:))
- [init(_:for:backgroundStyle:_:onDocumentOpen:overlayAccessoryView:)](/documentation/swiftui/documentlaunchview/init(_:for:backgroundstyle:_:ondocumentopen:overlayaccessoryview:))

#### Instance Properties

- [var body: some View](/documentation/swiftui/documentlaunchview/body)
- [DocumentLaunchGeometryProxy](/documentation/swiftui/documentlaunchgeometryproxy)

#### Instance Properties

- [var frame: CGRect](/documentation/swiftui/documentlaunchgeometryproxy/frame)
- [var titleViewFrame: CGRect](/documentation/swiftui/documentlaunchgeometryproxy/titleviewframe)
- [DefaultDocumentGroupLaunchActions](/documentation/swiftui/defaultdocumentgrouplaunchactions)

#### Initializers

- [init()](/documentation/swiftui/defaultdocumentgrouplaunchactions/init())
- [NewDocumentButton](/documentation/swiftui/newdocumentbutton)

#### Initializers

- [init(_:contentType:)](/documentation/swiftui/newdocumentbutton/init(_:contenttype:))
- [init(_:contentType:prepareDocumentURL:)](/documentation/swiftui/newdocumentbutton/init(_:contenttype:preparedocumenturl:))
- [init(_:for:contentType:prepareDocument:)](/documentation/swiftui/newdocumentbutton/init(_:for:contenttype:preparedocument:))
- [DocumentBaseBox](/documentation/swiftui/documentbasebox)

#### Associated Types

- [Document](/documentation/swiftui/documentbasebox/document)

#### Instance Properties

- [var base: Self.Document?](/documentation/swiftui/documentbasebox/base)

### Renaming a document

- [RenameButton](/documentation/swiftui/renamebutton)

#### Creating an rename button

- [init()](/documentation/swiftui/renamebutton/init())
- [func renameAction(_:)](/documentation/swiftui/view/renameaction(_:))
- [var rename: RenameAction?](/documentation/swiftui/environmentvalues/rename)
- [RenameAction](/documentation/swiftui/renameaction)

#### Calling the action

- [func callAsFunction()](/documentation/swiftui/renameaction/callasfunction())
- [Navigation](/documentation/swiftui/navigation)

### Essentials

- [Understanding the navigation stack](/documentation/swiftui/understanding-the-navigation-stack)

### Presenting views in columns

- [Bringing robust navigation structure to your SwiftUI app](/documentation/swiftui/bringing-robust-navigation-structure-to-your-swiftui-app)
- [Migrating to new navigation types](/documentation/swiftui/migrating-to-new-navigation-types)
- [NavigationSplitView](/documentation/swiftui/navigationsplitview)

#### Creating a navigation split view

- [init(sidebar: () -> Sidebar, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(sidebar:detail:))
- [init(sidebar: () -> Sidebar, content: () -> Content, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(sidebar:content:detail:))

#### Hiding columns in a navigation split view

- [init(columnVisibility: Binding<NavigationSplitViewVisibility>, sidebar: () -> Sidebar, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(columnvisibility:sidebar:detail:))
- [init(columnVisibility: Binding<NavigationSplitViewVisibility>, sidebar: () -> Sidebar, content: () -> Content, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(columnvisibility:sidebar:content:detail:))

#### Specifying a preferred compact column

- [init(preferredCompactColumn: Binding<NavigationSplitViewColumn>, sidebar: () -> Sidebar, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(preferredcompactcolumn:sidebar:detail:))
- [init(preferredCompactColumn: Binding<NavigationSplitViewColumn>, sidebar: () -> Sidebar, content: () -> Content, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(preferredcompactcolumn:sidebar:content:detail:))

#### Specifying a preferred compact column and column visibility

- [init(columnVisibility: Binding<NavigationSplitViewVisibility>, preferredCompactColumn: Binding<NavigationSplitViewColumn>, sidebar: () -> Sidebar, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(columnvisibility:preferredcompactcolumn:sidebar:detail:))
- [init(columnVisibility: Binding<NavigationSplitViewVisibility>, preferredCompactColumn: Binding<NavigationSplitViewColumn>, sidebar: () -> Sidebar, content: () -> Content, detail: () -> Detail)](/documentation/swiftui/navigationsplitview/init(columnvisibility:preferredcompactcolumn:sidebar:content:detail:))
- [func navigationSplitViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationsplitviewstyle(_:))
- [func navigationSplitViewColumnWidth(CGFloat) -> some View](/documentation/swiftui/view/navigationsplitviewcolumnwidth(_:))
- [func navigationSplitViewColumnWidth(min: CGFloat?, ideal: CGFloat, max: CGFloat?) -> some View](/documentation/swiftui/view/navigationsplitviewcolumnwidth(min:ideal:max:))
- [NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility)

#### Getting visibilities

- [static var automatic: NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility/automatic)
- [static var all: NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility/all)
- [static var doubleColumn: NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility/doublecolumn)
- [static var detailOnly: NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility/detailonly)
- [NavigationLink](/documentation/swiftui/navigationlink)

#### Presenting a destination view

- [init(_:destination:)](/documentation/swiftui/navigationlink/init(_:destination:))
- [init(destination:label:)](/documentation/swiftui/navigationlink/init(destination:label:))

#### Presenting a value

- [init(_:value:)](/documentation/swiftui/navigationlink/init(_:value:))
- [init(value:label:)](/documentation/swiftui/navigationlink/init(value:label:))

#### Configuring the link

- [func isDetailLink(Bool) -> some View](/documentation/swiftui/navigationlink/isdetaillink(_:))

#### Deprecated symbols

- [Deprecated symbols](/documentation/swiftui/navigationlink-deprecated)

##### Creating links with view builders

- [init(_:isActive:destination:)](/documentation/swiftui/navigationlink/init(_:isactive:destination:))
- [init(isActive: Binding<Bool>, destination: () -> Destination, label: () -> Label)](/documentation/swiftui/navigationlink/init(isactive:destination:label:))
- [init(_:tag:selection:destination:)](/documentation/swiftui/navigationlink/init(_:tag:selection:destination:))
- [init<V>(tag: V, selection: Binding<V?>, destination: () -> Destination, label: () -> Label)](/documentation/swiftui/navigationlink/init(tag:selection:destination:label:))

##### Creating links for WatchKit

- [init(destinationName: String, isActive: Binding<Bool>, label: () -> Label)](/documentation/swiftui/navigationlink/init(destinationname:isactive:label:))
- [init<V>(destinationName: String, tag: V, selection: Binding<V?>, label: () -> Label)](/documentation/swiftui/navigationlink/init(destinationname:tag:selection:label:))
- [init(destinationName: String, label: () -> Label)](/documentation/swiftui/navigationlink/init(destinationname:label:))

##### Creating links with view arguments

- [init(_:destination:isActive:)](/documentation/swiftui/navigationlink/init(_:destination:isactive:))
- [init(destination: Destination, isActive: Binding<Bool>, label: () -> Label)](/documentation/swiftui/navigationlink/init(destination:isactive:label:))
- [init(_:destination:tag:selection:)](/documentation/swiftui/navigationlink/init(_:destination:tag:selection:))
- [init<V>(destination: Destination, tag: V, selection: Binding<V?>, label: () -> Label)](/documentation/swiftui/navigationlink/init(destination:tag:selection:label:))

### Stacking views in one column

- [NavigationStack](/documentation/swiftui/navigationstack)

#### Creating a navigation stack

- [init(root: () -> Root)](/documentation/swiftui/navigationstack/init(root:))

#### Creating a navigation stack with a path

- [init(path:root:)](/documentation/swiftui/navigationstack/init(path:root:))
- [NavigationPath](/documentation/swiftui/navigationpath)

#### Creating a navigation path

- [init()](/documentation/swiftui/navigationpath/init())
- [init(_:)](/documentation/swiftui/navigationpath/init(_:))

#### Managing path contents

- [var isEmpty: Bool](/documentation/swiftui/navigationpath/isempty)
- [var count: Int](/documentation/swiftui/navigationpath/count)
- [func append(_:)](/documentation/swiftui/navigationpath/append(_:))
- [func removeLast(Int)](/documentation/swiftui/navigationpath/removelast(_:))

#### Encoding a path

- [var codable: NavigationPath.CodableRepresentation?](/documentation/swiftui/navigationpath/codable)
- [NavigationPath.CodableRepresentation](/documentation/swiftui/navigationpath/codablerepresentation)
- [func navigationDestination<D, C>(for: D.Type, destination: (D) -> C) -> some View](/documentation/swiftui/view/navigationdestination(for:destination:))
- [func navigationDestination<V>(isPresented: Binding<Bool>, destination: () -> V) -> some View](/documentation/swiftui/view/navigationdestination(ispresented:destination:))
- [func navigationDestination<D, C>(item: Binding<Optional<D>>, destination: (D) -> C) -> some View](/documentation/swiftui/view/navigationdestination(item:destination:))

### Managing column collapse

- [NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn)

#### Getting a column

- [static var sidebar: NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn/sidebar)
- [static var content: NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn/content)
- [static var detail: NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn/detail)

### Setting titles for navigation content

- [func navigationTitle(_:)](/documentation/swiftui/view/navigationtitle(_:))
- [func navigationSubtitle(_:)](/documentation/swiftui/view/navigationsubtitle(_:))
- [func navigationDocument(_:)](/documentation/swiftui/view/navigationdocument(_:))
- [func navigationDocument(_:preview:)](/documentation/swiftui/view/navigationdocument(_:preview:))

### Configuring the navigation bar

- [func navigationBarBackButtonHidden(Bool) -> some View](/documentation/swiftui/view/navigationbarbackbuttonhidden(_:))
- [func navigationBarTitleDisplayMode(NavigationBarItem.TitleDisplayMode) -> some View](/documentation/swiftui/view/navigationbartitledisplaymode(_:))
- [NavigationBarItem](/documentation/swiftui/navigationbaritem)

#### Setting a title display mode

- [NavigationBarItem.TitleDisplayMode](/documentation/swiftui/navigationbaritem/titledisplaymode)

##### Getting title display modes

- [case automatic](/documentation/swiftui/navigationbaritem/titledisplaymode/automatic)
- [case inline](/documentation/swiftui/navigationbaritem/titledisplaymode/inline)
- [case large](/documentation/swiftui/navigationbaritem/titledisplaymode/large)

### Configuring the sidebar

- [var sidebarRowSize: SidebarRowSize](/documentation/swiftui/environmentvalues/sidebarrowsize)
- [SidebarRowSize](/documentation/swiftui/sidebarrowsize)

#### Getting row sizes

- [case small](/documentation/swiftui/sidebarrowsize/small)
- [case medium](/documentation/swiftui/sidebarrowsize/medium)
- [case large](/documentation/swiftui/sidebarrowsize/large)

### Presenting views in tabs

- [Enhancing your app’s content with tab navigation](/documentation/swiftui/enhancing-your-app-content-with-tab-navigation)
- [TabView](/documentation/swiftui/tabview)

#### Creating a tab view

- [init(content:)](/documentation/swiftui/tabview/init(content:))
- [init(selection:content:)](/documentation/swiftui/tabview/init(selection:content:))

#### Configuring search activation

- [TabSearchActivation](/documentation/swiftui/tabsearchactivation)

##### Type Properties

- [static var automatic: TabSearchActivation](/documentation/swiftui/tabsearchactivation/automatic)
- [static var searchTabSelection: TabSearchActivation](/documentation/swiftui/tabsearchactivation/searchtabselection)
- [Tab](/documentation/swiftui/tab)

#### Creating a tab

- [init(content: () -> Content)](/documentation/swiftui/tab/init(content:))
- [init(value:content:)](/documentation/swiftui/tab/init(value:content:))
- [init(role: TabRole?, content: () -> Content)](/documentation/swiftui/tab/init(role:content:))
- [init(value:role:content:)](/documentation/swiftui/tab/init(value:role:content:))

#### Creating a tab with label

- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/tab/init(content:label:))
- [init(value:content:label:)](/documentation/swiftui/tab/init(value:content:label:))
- [init(role: TabRole?, content: () -> Content, label: () -> Label)](/documentation/swiftui/tab/init(role:content:label:))
- [init(value:role:content:label:)](/documentation/swiftui/tab/init(value:role:content:label:))

#### Creating a tab with system symbol

- [init(_:systemImage:content:)](/documentation/swiftui/tab/init(_:systemimage:content:))
- [init(_:systemImage:value:content:)](/documentation/swiftui/tab/init(_:systemimage:value:content:))
- [init(_:systemImage:role:content:)](/documentation/swiftui/tab/init(_:systemimage:role:content:))
- [init(_:systemImage:value:role:content:)](/documentation/swiftui/tab/init(_:systemimage:value:role:content:))

#### Creating a tab with image

- [init(_:image:content:)](/documentation/swiftui/tab/init(_:image:content:))
- [init(_:image:value:content:)](/documentation/swiftui/tab/init(_:image:value:content:))
- [init(_:image:role:content:)](/documentation/swiftui/tab/init(_:image:role:content:))
- [init(_:image:value:role:content:)](/documentation/swiftui/tab/init(_:image:value:role:content:))

#### Supporting types

- [DefaultTabLabel](/documentation/swiftui/defaulttablabel)
- [TabRole](/documentation/swiftui/tabrole)

#### Type Properties

- [static var search: TabRole](/documentation/swiftui/tabrole/search)
- [TabSection](/documentation/swiftui/tabsection)

#### Creating a tab section

- [init(content:)](/documentation/swiftui/tabsection/init(content:))
- [init(_:content:)](/documentation/swiftui/tabsection/init(_:content:))
- [init(content:header:)](/documentation/swiftui/tabsection/init(content:header:))

#### Supporting types

- [DefaultTabLabel](/documentation/swiftui/defaulttablabel)
- [func tabViewStyle<S>(S) -> some View](/documentation/swiftui/view/tabviewstyle(_:))

### Configuring a tab bar

- [func defaultAdaptableTabBarPlacement(AdaptableTabBarPlacement) -> some View](/documentation/swiftui/view/defaultadaptabletabbarplacement(_:))
- [func tabViewSidebarHeader<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarheader(content:))
- [func tabViewSidebarFooter<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarfooter(content:))
- [func tabViewSidebarBottomBar<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarbottombar(content:))
- [AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement)

#### Type Properties

- [static let automatic: AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement/automatic)
- [static let sidebar: AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement/sidebar)
- [static let tabBar: AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement/tabbar)
- [var tabBarPlacement: TabBarPlacement?](/documentation/swiftui/environmentvalues/tabbarplacement)
- [TabBarPlacement](/documentation/swiftui/tabbarplacement)

#### Type Properties

- [static let bottomBar: TabBarPlacement](/documentation/swiftui/tabbarplacement/bottombar)
- [static let ornament: TabBarPlacement](/documentation/swiftui/tabbarplacement/ornament)
- [static let pageIndicator: TabBarPlacement](/documentation/swiftui/tabbarplacement/pageindicator)
- [static let sidebar: TabBarPlacement](/documentation/swiftui/tabbarplacement/sidebar)
- [static let topBar: TabBarPlacement](/documentation/swiftui/tabbarplacement/topbar)
- [var isTabBarShowingSections: Bool](/documentation/swiftui/environmentvalues/istabbarshowingsections)
- [TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior)

#### Type Properties

- [static let automatic: TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior/automatic)
- [static let never: TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior/never)
- [static let onScrollDown: TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior/onscrolldown)
- [static let onScrollUp: TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior/onscrollup)
- [TabViewBottomAccessoryPlacement](/documentation/swiftui/tabviewbottomaccessoryplacement)

#### Enumeration Cases

- [case expanded](/documentation/swiftui/tabviewbottomaccessoryplacement/expanded)
- [case inline](/documentation/swiftui/tabviewbottomaccessoryplacement/inline)

### Configuring a tab

- [func sectionActions<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/sectionactions(content:))
- [TabPlacement](/documentation/swiftui/tabplacement)

#### Type Properties

- [static let automatic: TabPlacement](/documentation/swiftui/tabplacement/automatic)
- [static let pinned: TabPlacement](/documentation/swiftui/tabplacement/pinned)
- [static let sidebarOnly: TabPlacement](/documentation/swiftui/tabplacement/sidebaronly)
- [TabContentBuilder](/documentation/swiftui/tabcontentbuilder)

#### Structures

- [TabContentBuilder.Content](/documentation/swiftui/tabcontentbuilder/content)

#### Type Methods

- [static func buildBlock(some TabContent<TabValue>) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:))
- [static func buildBlock<C0, C1>(C0, C1) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:))
- [static func buildBlock<C0, C1, C2>(C0, C1, C2) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:))
- [static func buildBlock<C0, C1, C2, C3>(C0, C1, C2, C3) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4>(C0, C1, C2, C3, C4) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5>(C0, C1, C2, C3, C4, C5) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6>(C0, C1, C2, C3, C4, C5, C6) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7>(C0, C1, C2, C3, C4, C5, C6, C7) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8>(C0, C1, C2, C3, C4, C5, C6, C7, C8) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8, C9>(C0, C1, C2, C3, C4, C5, C6, C7, C8, C9) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))
- [static func buildEither<T, F>(first: T) -> _ConditionalContent<T, F>](/documentation/swiftui/tabcontentbuilder/buildeither(first:))
- [static func buildEither<T, F>(second: F) -> _ConditionalContent<T, F>](/documentation/swiftui/tabcontentbuilder/buildeither(second:))
- [static func buildExpression(some TabContent<TabValue>) -> some TabContent<TabValue>
](/documentation/swiftui/tabcontentbuilder/buildexpression(_:))
- [static func buildIf((some TabContent<TabValue>)?) -> (some TabContent<TabValue>)?
](/documentation/swiftui/tabcontentbuilder/buildif(_:))
- [static func buildLimitedAvailability<T>(T) -> AnyTabContent<T.TabValue>](/documentation/swiftui/tabcontentbuilder/buildlimitedavailability(_:))
- [TabContent](/documentation/swiftui/tabcontent)

#### Associated Types

- [Body](/documentation/swiftui/tabcontent/body-swift.associatedtype)
- [TabValue](/documentation/swiftui/tabcontent/tabvalue)

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/tabcontent/body-swift.property)

#### Instance Methods

- [func accessibilityHint(_:isEnabled:)](/documentation/swiftui/tabcontent/accessibilityhint(_:isenabled:))
- [func accessibilityIdentifier(String, isEnabled: Bool) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/accessibilityidentifier(_:isenabled:))
- [func accessibilityInputLabels(_:isEnabled:)](/documentation/swiftui/tabcontent/accessibilityinputlabels(_:isenabled:))
- [func accessibilityLabel(_:isEnabled:)](/documentation/swiftui/tabcontent/accessibilitylabel(_:isenabled:))
- [func accessibilityValue(_:isEnabled:)](/documentation/swiftui/tabcontent/accessibilityvalue(_:isenabled:))
- [func badge(_:)](/documentation/swiftui/tabcontent/badge(_:))
- [func contextMenu<M>(menuItems: () -> M) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/contextmenu(menuitems:))
- [func customizationBehavior(TabCustomizationBehavior, for: AdaptableTabBarPlacement...) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/customizationbehavior(_:for:))
- [func customizationID(String) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/customizationid(_:))
- [func defaultVisibility(Visibility, for: AdaptableTabBarPlacement...) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/defaultvisibility(_:for:))
- [func disabled(Bool) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/disabled(_:))
- [func draggable<T>(@autoclosure () -> T) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/draggable(_:))
- [func dropDestination<T>(for: T.Type, action: ([T]) -> Void) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/dropdestination(for:action:))
- [func hidden(Bool) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/hidden(_:))
- [func popover<Content>(isPresented: Binding<Bool>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: () -> Content) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/popover(ispresented:attachmentanchor:arrowedge:content:))
- [func popover<Item, Content>(item: Binding<Item?>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: (Item) -> Content) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/popover(item:attachmentanchor:arrowedge:content:))
- [func sectionActions<Content>(content: () -> Content) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/sectionactions(content:))
- [func springLoadingBehavior(SpringLoadingBehavior) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/springloadingbehavior(_:))
- [func swipeActions<T>(edge: HorizontalEdge, allowsFullSwipe: Bool, content: () -> T) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/swipeactions(edge:allowsfullswipe:content:))
- [func tabPlacement(TabPlacement) -> some TabContent<Self.TabValue>
](/documentation/swiftui/tabcontent/tabplacement(_:))
- [AnyTabContent](/documentation/swiftui/anytabcontent)

#### Initializers

- [init<T>(T)](/documentation/swiftui/anytabcontent/init(_:))

### Enabling tab customization

- [func tabViewCustomization(Binding<TabViewCustomization>?) -> some View](/documentation/swiftui/view/tabviewcustomization(_:))
- [TabViewCustomization](/documentation/swiftui/tabviewcustomization)

#### Structures

- [TabViewCustomization.SectionCustomization](/documentation/swiftui/tabviewcustomization/sectioncustomization)

##### Instance Properties

- [var tabOrder: [String]?](/documentation/swiftui/tabviewcustomization/sectioncustomization/taborder)

##### Instance Methods

- [func resetTabOrder()](/documentation/swiftui/tabviewcustomization/sectioncustomization/resettaborder())
- [TabViewCustomization.TabCustomization](/documentation/swiftui/tabviewcustomization/tabcustomization)

##### Instance Properties

- [var sidebarVisibility: Visibility](/documentation/swiftui/tabviewcustomization/tabcustomization/sidebarvisibility)
- [var tabBarVisibility: Visibility](/documentation/swiftui/tabviewcustomization/tabcustomization/tabbarvisibility)

#### Initializers

- [init()](/documentation/swiftui/tabviewcustomization/init())

#### Instance Methods

- [func resetSectionOrder()](/documentation/swiftui/tabviewcustomization/resetsectionorder())
- [func resetSectionOrder(for: String)](/documentation/swiftui/tabviewcustomization/resetsectionorder(for:))
- [func resetVisibility()](/documentation/swiftui/tabviewcustomization/resetvisibility())

#### Subscripts

- [subscript(section _: String) -> TabViewCustomization.SectionCustomization](/documentation/swiftui/tabviewcustomization/subscript(section:))
- [subscript(sectionID _: String) -> [String]?](/documentation/swiftui/tabviewcustomization/subscript(sectionid:))
- [subscript(sidebarVisibility _: String) -> Visibility](/documentation/swiftui/tabviewcustomization/subscript(sidebarvisibility:))
- [subscript(tab _: String) -> TabViewCustomization.TabCustomization](/documentation/swiftui/tabviewcustomization/subscript(tab:))
- [TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior)

#### Type Properties

- [static var automatic: TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior/automatic)
- [static var disabled: TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior/disabled)
- [static var reorderable: TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior/reorderable)

### Displaying views in multiple panes

- [HSplitView](/documentation/swiftui/hsplitview)

#### Creating a horizontal split view

- [init(content: () -> Content)](/documentation/swiftui/hsplitview/init(content:))
- [VSplitView](/documentation/swiftui/vsplitview)

#### Creating a vertical split view

- [init(content: () -> Content)](/documentation/swiftui/vsplitview/init(content:))

### Deprecated Types

- [NavigationView](/documentation/swiftui/navigationview)

#### Creating a navigation view

- [init(content: () -> Content)](/documentation/swiftui/navigationview/init(content:))

#### Styling navigation views

- [func navigationViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationviewstyle(_:))
- [NavigationViewStyle](/documentation/swiftui/navigationviewstyle)

##### Getting built-in navigation view styles

- [static var automatic: DefaultNavigationViewStyle](/documentation/swiftui/navigationviewstyle/automatic)
- [static var columns: ColumnNavigationViewStyle](/documentation/swiftui/navigationviewstyle/columns)
- [static var stack: StackNavigationViewStyle](/documentation/swiftui/navigationviewstyle/stack)

##### Supporting types

- [DefaultNavigationViewStyle](/documentation/swiftui/defaultnavigationviewstyle)

###### Creating a default navigation view style

- [init()](/documentation/swiftui/defaultnavigationviewstyle/init())
- [ColumnNavigationViewStyle](/documentation/swiftui/columnnavigationviewstyle)
- [StackNavigationViewStyle](/documentation/swiftui/stacknavigationviewstyle)

###### Creating a stack navigation view style

- [init()](/documentation/swiftui/stacknavigationviewstyle/init())
- [DoubleColumnNavigationViewStyle](/documentation/swiftui/doublecolumnnavigationviewstyle)

###### Create a double column view style

- [init()](/documentation/swiftui/doublecolumnnavigationviewstyle/init())
- [func tabItem<V>(() -> V) -> some View](/documentation/swiftui/view/tabitem(_:))
- [Modal presentations](/documentation/swiftui/modal-presentations)

### Configuring a dialog

- [DialogSeverity](/documentation/swiftui/dialogseverity)

#### Getting severities

- [static let automatic: DialogSeverity](/documentation/swiftui/dialogseverity/automatic)
- [static let standard: DialogSeverity](/documentation/swiftui/dialogseverity/standard)
- [static let critical: DialogSeverity](/documentation/swiftui/dialogseverity/critical)

### Showing a sheet, cover, or popover

- [func sheet<Content>(isPresented: Binding<Bool>, onDismiss: (() -> Void)?, content: () -> Content) -> some View](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:))
- [func sheet<Item, Content>(item: Binding<Item?>, onDismiss: (() -> Void)?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/sheet(item:ondismiss:content:))
- [func fullScreenCover<Content>(isPresented: Binding<Bool>, onDismiss: (() -> Void)?, content: () -> Content) -> some View](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:))
- [func fullScreenCover<Item, Content>(item: Binding<Item?>, onDismiss: (() -> Void)?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/fullscreencover(item:ondismiss:content:))
- [func popover<Item, Content>(item: Binding<Item?>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/popover(item:attachmentanchor:arrowedge:content:))
- [func popover<Content>(isPresented: Binding<Bool>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: () -> Content) -> some View](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:))
- [PopoverAttachmentAnchor](/documentation/swiftui/popoverattachmentanchor)

#### Getting attachment anchors

- [case point(UnitPoint)](/documentation/swiftui/popoverattachmentanchor/point(_:))
- [case rect(Anchor<CGRect>.Source)](/documentation/swiftui/popoverattachmentanchor/rect(_:))

### Adapting a presentation size

- [func presentationCompactAdaptation(horizontal: PresentationAdaptation, vertical: PresentationAdaptation) -> some View](/documentation/swiftui/view/presentationcompactadaptation(horizontal:vertical:))
- [func presentationCompactAdaptation(PresentationAdaptation) -> some View](/documentation/swiftui/view/presentationcompactadaptation(_:))
- [PresentationAdaptation](/documentation/swiftui/presentationadaptation)

#### Getting adaptation strategies

- [static var automatic: PresentationAdaptation](/documentation/swiftui/presentationadaptation/automatic)
- [static var none: PresentationAdaptation](/documentation/swiftui/presentationadaptation/none)
- [static var fullScreenCover: PresentationAdaptation](/documentation/swiftui/presentationadaptation/fullscreencover)
- [static var popover: PresentationAdaptation](/documentation/swiftui/presentationadaptation/popover)
- [static var sheet: PresentationAdaptation](/documentation/swiftui/presentationadaptation/sheet)
- [func presentationSizing(some PresentationSizing) -> some View](/documentation/swiftui/view/presentationsizing(_:))
- [PresentationSizing](/documentation/swiftui/presentationsizing)

#### Getting built-in presentation size

- [static var automatic: AutomaticPresentationSizing](/documentation/swiftui/presentationsizing/automatic)
- [static var fitted: FittedPresentationSizing](/documentation/swiftui/presentationsizing/fitted)
- [static var form: FormPresentationSizing](/documentation/swiftui/presentationsizing/form)
- [static var page: PagePresentationSizing](/documentation/swiftui/presentationsizing/page)

#### Creating custom presentation size

- [func fitted(horizontal: Bool, vertical: Bool) -> some PresentationSizing](/documentation/swiftui/presentationsizing/fitted(horizontal:vertical:))
- [func proposedSize(for: PresentationSizingRoot, context: PresentationSizingContext) -> ProposedViewSize](/documentation/swiftui/presentationsizing/proposedsize(for:context:))
- [func sticky(horizontal: Bool, vertical: Bool) -> some PresentationSizing](/documentation/swiftui/presentationsizing/sticky(horizontal:vertical:))

#### Supporting types

- [AutomaticPresentationSizing](/documentation/swiftui/automaticpresentationsizing)
- [FittedPresentationSizing](/documentation/swiftui/fittedpresentationsizing)
- [FormPresentationSizing](/documentation/swiftui/formpresentationsizing)
- [PagePresentationSizing](/documentation/swiftui/pagepresentationsizing)
- [PresentationSizingRoot](/documentation/swiftui/presentationsizingroot)

#### Instance Methods

- [func sizeThatFits(ProposedViewSize) -> CGSize](/documentation/swiftui/presentationsizingroot/sizethatfits(_:))
- [PresentationSizingContext](/documentation/swiftui/presentationsizingcontext)

### Configuring a sheet’s height

- [func presentationDetents(Set<PresentationDetent>) -> some View](/documentation/swiftui/view/presentationdetents(_:))
- [func presentationDetents(Set<PresentationDetent>, selection: Binding<PresentationDetent>) -> some View](/documentation/swiftui/view/presentationdetents(_:selection:))
- [func presentationContentInteraction(PresentationContentInteraction) -> some View](/documentation/swiftui/view/presentationcontentinteraction(_:))
- [func presentationDragIndicator(Visibility) -> some View](/documentation/swiftui/view/presentationdragindicator(_:))
- [PresentationDetent](/documentation/swiftui/presentationdetent)

#### Getting built-in detents

- [static let large: PresentationDetent](/documentation/swiftui/presentationdetent/large)
- [static let medium: PresentationDetent](/documentation/swiftui/presentationdetent/medium)

#### Creating custom detents

- [static func custom<D>(D.Type) -> PresentationDetent](/documentation/swiftui/presentationdetent/custom(_:))
- [static func fraction(CGFloat) -> PresentationDetent](/documentation/swiftui/presentationdetent/fraction(_:))
- [static func height(CGFloat) -> PresentationDetent](/documentation/swiftui/presentationdetent/height(_:))
- [PresentationDetent.Context](/documentation/swiftui/presentationdetent/context)

##### Getting the height

- [var maxDetentValue: CGFloat](/documentation/swiftui/presentationdetent/context/maxdetentvalue)

##### Supporting types

- [subscript<T>(dynamicMember _: KeyPath<EnvironmentValues, T>) -> T](/documentation/swiftui/presentationdetent/context/subscript(dynamicmember:))
- [CustomPresentationDetent](/documentation/swiftui/custompresentationdetent)

#### Getting the height

- [static func height(in: Self.Context) -> CGFloat?](/documentation/swiftui/custompresentationdetent/height(in:))
- [CustomPresentationDetent.Context](/documentation/swiftui/custompresentationdetent/context)
- [PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction)

#### Getting interaction behaviors

- [static var automatic: PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction/automatic)
- [static var resizes: PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction/resizes)
- [static var scrolls: PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction/scrolls)

### Styling a sheet and its background

- [func presentationCornerRadius(CGFloat?) -> some View](/documentation/swiftui/view/presentationcornerradius(_:))
- [func presentationBackground<S>(S) -> some View](/documentation/swiftui/view/presentationbackground(_:))
- [func presentationBackground<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/presentationbackground(alignment:content:))
- [func presentationBackgroundInteraction(PresentationBackgroundInteraction) -> some View](/documentation/swiftui/view/presentationbackgroundinteraction(_:))
- [PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction)

#### Getting interaction types

- [static var automatic: PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction/automatic)
- [static var disabled: PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction/disabled)
- [static var enabled: PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction/enabled)
- [static func enabled(upThrough: PresentationDetent) -> PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction/enabled(upthrough:))

### Presenting an alert

- [AlertScene](/documentation/swiftui/alertscene)

#### Initializers

- [init(_:isPresented:actions:)](/documentation/swiftui/alertscene/init(_:ispresented:actions:))
- [init(_:isPresented:actions:message:)](/documentation/swiftui/alertscene/init(_:ispresented:actions:message:))
- [init(_:isPresented:presenting:actions:)](/documentation/swiftui/alertscene/init(_:ispresented:presenting:actions:))
- [init(_:isPresented:presenting:actions:message:)](/documentation/swiftui/alertscene/init(_:ispresented:presenting:actions:message:))
- [func alert(_:isPresented:actions:)](/documentation/swiftui/view/alert(_:ispresented:actions:))
- [func alert(_:isPresented:presenting:actions:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:))
- [func alert<E, A>(isPresented: Binding<Bool>, error: E?, actions: () -> A) -> some View](/documentation/swiftui/view/alert(ispresented:error:actions:))
- [func alert(_:isPresented:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:actions:message:))
- [func alert(_:isPresented:presenting:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:message:))
- [func alert<E, A, M>(isPresented: Binding<Bool>, error: E?, actions: (E) -> A, message: (E) -> M) -> some View](/documentation/swiftui/view/alert(ispresented:error:actions:message:))

### Getting confirmation for an action

- [func confirmationDialog(_:isPresented:titleVisibility:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:))

### Showing a confirmation dialog with a message

- [func confirmationDialog(_:isPresented:titleVisibility:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:message:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:message:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:message:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:message:))

### Configuring a dialog

- [func dialogIcon(Image?) -> some View](/documentation/swiftui/view/dialogicon(_:))
- [func dialogIcon(Image?) -> some Scene](/documentation/swiftui/scene/dialogicon(_:))
- [func dialogSeverity(DialogSeverity) -> some View](/documentation/swiftui/view/dialogseverity(_:))
- [func dialogSeverity(DialogSeverity) -> some Scene](/documentation/swiftui/scene/dialogseverity(_:))
- [func dialogSuppressionToggle(isSuppressed: Binding<Bool>) -> some View](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:))
- [func dialogSuppressionToggle(isSuppressed: Binding<Bool>) -> some Scene](/documentation/swiftui/scene/dialogsuppressiontoggle(issuppressed:))
- [func dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/view/dialogsuppressiontoggle(_:issuppressed:))
- [func dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/scene/dialogsuppressiontoggle(_:issuppressed:))

### Exporting to file

- [func fileExporter(isPresented:document:contentType:defaultFilename:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:))
- [func fileExporter(isPresented:documents:contentType:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttype:oncompletion:))
- [func fileExporter(isPresented:document:contentTypes:defaultFilename:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter(isPresented:documents:contentTypes:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttypes:oncompletion:oncancellation:))
- [func fileExporter<T>(isPresented: Binding<Bool>, item: T?, contentTypes: [UTType], defaultFilename: String?, onCompletion: (Result<URL, any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileexporter(ispresented:item:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter<C, T>(isPresented: Binding<Bool>, items: C, contentTypes: [UTType], onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileexporter(ispresented:items:contenttypes:oncompletion:oncancellation:))
- [func fileExporterFilenameLabel(_:)](/documentation/swiftui/view/fileexporterfilenamelabel(_:))

### Importing from file

- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], allowsMultipleSelection: Bool, onCompletion: (Result<[URL], any Error>) -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:))
- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], onCompletion: (Result<URL, any Error>) -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:))
- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], allowsMultipleSelection: Bool, onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:oncancellation:))

### Moving a file

- [func fileMover(isPresented: Binding<Bool>, file: URL?, onCompletion: (Result<URL, any Error>) -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:))
- [func fileMover<C>(isPresented: Binding<Bool>, files: C, onCompletion: (Result<[URL], any Error>) -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:))
- [func fileMover(isPresented: Binding<Bool>, file: URL?, onCompletion: (Result<URL, any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:oncancellation:))
- [func fileMover<C>(isPresented: Binding<Bool>, files: C, onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:oncancellation:))

### Configuring a file dialog

- [func fileDialogBrowserOptions(FileDialogBrowserOptions) -> some View](/documentation/swiftui/view/filedialogbrowseroptions(_:))
- [func fileDialogConfirmationLabel(_:)](/documentation/swiftui/view/filedialogconfirmationlabel(_:))
- [func fileDialogCustomizationID(String) -> some View](/documentation/swiftui/view/filedialogcustomizationid(_:))
- [func fileDialogDefaultDirectory(URL?) -> some View](/documentation/swiftui/view/filedialogdefaultdirectory(_:))
- [func fileDialogImportsUnresolvedAliases(Bool) -> some View](/documentation/swiftui/view/filedialogimportsunresolvedaliases(_:))
- [func fileDialogMessage(_:)](/documentation/swiftui/view/filedialogmessage(_:))
- [func fileDialogURLEnabled(Predicate<URL>) -> some View](/documentation/swiftui/view/filedialogurlenabled(_:))
- [FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions)

#### Getting browser options

- [static let displayFileExtensions: FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions/displayfileextensions)
- [static let enumeratePackages: FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions/enumeratepackages)
- [static let includeHiddenFiles: FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions/includehiddenfiles)

### Presenting an inspector

- [func inspector<V>(isPresented: Binding<Bool>, content: () -> V) -> some View](/documentation/swiftui/view/inspector(ispresented:content:))
- [func inspectorColumnWidth(CGFloat) -> some View](/documentation/swiftui/view/inspectorcolumnwidth(_:))
- [func inspectorColumnWidth(min: CGFloat?, ideal: CGFloat, max: CGFloat?) -> some View](/documentation/swiftui/view/inspectorcolumnwidth(min:ideal:max:))

### Dismissing a presentation

- [var isPresented: Bool](/documentation/swiftui/environmentvalues/ispresented)
- [var dismiss: DismissAction](/documentation/swiftui/environmentvalues/dismiss)
- [DismissAction](/documentation/swiftui/dismissaction)

#### Calling the action

- [func callAsFunction()](/documentation/swiftui/dismissaction/callasfunction())
- [func interactiveDismissDisabled(Bool) -> some View](/documentation/swiftui/view/interactivedismissdisabled(_:))

### Deprecated modal presentations

- [Alert](/documentation/swiftui/alert)

#### Creating an alert

- [init(title: Text, message: Text?, dismissButton: Alert.Button?)](/documentation/swiftui/alert/init(title:message:dismissbutton:))
- [init(title: Text, message: Text?, primaryButton: Alert.Button, secondaryButton: Alert.Button)](/documentation/swiftui/alert/init(title:message:primarybutton:secondarybutton:))
- [static func sideBySideButtons(title: Text, message: Text?, primaryButton: Alert.Button, secondaryButton: Alert.Button) -> Alert](/documentation/swiftui/alert/sidebysidebuttons(title:message:primarybutton:secondarybutton:))

#### Specifying the button type

- [Alert.Button](/documentation/swiftui/alert/button)

##### Getting a button

- [static func `default`(Text, action: (() -> Void)?) -> Alert.Button](/documentation/swiftui/alert/button/default(_:action:))
- [static func cancel((() -> Void)?) -> Alert.Button](/documentation/swiftui/alert/button/cancel(_:))
- [static func cancel(Text, action: (() -> Void)?) -> Alert.Button](/documentation/swiftui/alert/button/cancel(_:action:))
- [static func destructive(Text, action: (() -> Void)?) -> Alert.Button](/documentation/swiftui/alert/button/destructive(_:action:))
- [ActionSheet](/documentation/swiftui/actionsheet)

#### Creating an action sheet

- [init(title: Text, message: Text?, buttons: [ActionSheet.Button])](/documentation/swiftui/actionsheet/init(title:message:buttons:))

#### Specifying the button type

- [ActionSheet.Button](/documentation/swiftui/actionsheet/button)
- [Toolbars](/documentation/swiftui/toolbars)

### Populating a toolbar

- [func toolbar(content:)](/documentation/swiftui/view/toolbar(content:))
- [ToolbarItem](/documentation/swiftui/toolbaritem)

#### Creating a toolbar item

- [init(placement: ToolbarItemPlacement, content: () -> Content)](/documentation/swiftui/toolbaritem/init(placement:content:))
- [init(id: String, placement: ToolbarItemPlacement, content: () -> Content)](/documentation/swiftui/toolbaritem/init(id:placement:content:))
- [init(id: String, placement: ToolbarItemPlacement, showsByDefault: Bool, content: () -> Content)](/documentation/swiftui/toolbaritem/init(id:placement:showsbydefault:content:))
- [ToolbarItemGroup](/documentation/swiftui/toolbaritemgroup)

#### Creating a toolbar item group

- [init(placement: ToolbarItemPlacement, content: () -> Content)](/documentation/swiftui/toolbaritemgroup/init(placement:content:))
- [init<C, L>(placement: ToolbarItemPlacement, content: () -> C, label: () -> L)](/documentation/swiftui/toolbaritemgroup/init(placement:content:label:))

#### Supporting types

- [LabeledToolbarItemGroupContent](/documentation/swiftui/labeledtoolbaritemgroupcontent)
- [ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement)

#### Getting semantic placement

- [static let automatic: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/automatic)
- [static let principal: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/principal)
- [static let status: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/status)

#### Getting placement for specific actions

- [static let primaryAction: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/primaryaction)
- [static let secondaryAction: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/secondaryaction)
- [static let confirmationAction: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/confirmationaction)
- [static let cancellationAction: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/cancellationaction)
- [static let destructiveAction: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/destructiveaction)
- [static let navigation: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/navigation)

#### Getting explicit placement

- [static var topBarLeading: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/topbarleading)
- [static var topBarTrailing: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/topbartrailing)
- [static let bottomBar: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/bottombar)
- [static let bottomOrnament: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/bottomornament)
- [static let keyboard: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/keyboard)
- [static func accessoryBar<ID>(id: ID) -> ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/accessorybar(id:))

#### Deprecated symbols

- [init<ID>(id: ID)](/documentation/swiftui/toolbaritemplacement/init(id:))
- [static let navigationBarLeading: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/navigationbarleading)
- [static let navigationBarTrailing: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/navigationbartrailing)

#### Type Properties

- [static let largeSubtitle: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/largesubtitle)
- [static let largeTitle: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/largetitle)
- [static let subtitle: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/subtitle)
- [static var title: ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement/title)
- [ToolbarContent](/documentation/swiftui/toolbarcontent)

#### Implementing toolbar content

- [var body: Self.Body](/documentation/swiftui/toolbarcontent/body-swift.property)
- [Body](/documentation/swiftui/toolbarcontent/body-swift.associatedtype)

#### Instance Methods

- [func hidden(Bool) -> some ToolbarContent](/documentation/swiftui/toolbarcontent/hidden(_:))
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID) -> some ToolbarContent](/documentation/swiftui/toolbarcontent/matchedtransitionsource(id:in:))
- [func sharedBackgroundVisibility(Visibility) -> some ToolbarContent](/documentation/swiftui/toolbarcontent/sharedbackgroundvisibility(_:))
- [ToolbarContentBuilder](/documentation/swiftui/toolbarcontentbuilder)

#### Building toolbar content

- [static buildBlock(_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:))
- [static buildBlock(_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:))
- [static buildBlock(_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:))
- [static buildBlock(_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:))
- [static buildBlock(_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:_:_:)](/documentation/swiftui/toolbarcontentbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))

#### Building conditional toolbar content

- [static buildIf(_:)](/documentation/swiftui/toolbarcontentbuilder/buildif(_:))
- [static buildEither(first:)](/documentation/swiftui/toolbarcontentbuilder/buildeither(first:))
- [static buildEither(second:)](/documentation/swiftui/toolbarcontentbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/swiftui/toolbarcontentbuilder/buildexpression(_:))
- [static buildLimitedAvailability(_:)](/documentation/swiftui/toolbarcontentbuilder/buildlimitedavailability(_:))
- [ToolbarSpacer](/documentation/swiftui/toolbarspacer)

#### Initializers

- [init(SpacerSizing, placement: ToolbarItemPlacement)](/documentation/swiftui/toolbarspacer/init(_:placement:))
- [DefaultToolbarItem](/documentation/swiftui/defaulttoolbaritem)

#### Initializers

- [init(kind: ToolbarDefaultItemKind, placement: ToolbarItemPlacement)](/documentation/swiftui/defaulttoolbaritem/init(kind:placement:))

### Populating a customizable toolbar

- [func toolbar<Content>(id: String, content: () -> Content) -> some View](/documentation/swiftui/view/toolbar(id:content:))
- [CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent)

#### Using default options

- [func defaultCustomization() -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/defaultcustomization())
- [func defaultCustomization(Visibility, options: ToolbarCustomizationOptions) -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/defaultcustomization(_:options:))

#### Customizing the behavior

- [func customizationBehavior(ToolbarCustomizationBehavior) -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/customizationbehavior(_:))

#### Instance Methods

- [func hidden(Bool) -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/hidden(_:))
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID) -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/matchedtransitionsource(id:in:))
- [func sharedBackgroundVisibility(Visibility) -> some CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent/sharedbackgroundvisibility(_:))
- [ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior)

#### Getting customization behaviors

- [static var `default`: ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior/default)
- [static var disabled: ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior/disabled)
- [static var reorderable: ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior/reorderable)
- [ToolbarCustomizationOptions](/documentation/swiftui/toolbarcustomizationoptions)

#### Getting customization options

- [static var alwaysAvailable: ToolbarCustomizationOptions](/documentation/swiftui/toolbarcustomizationoptions/alwaysavailable)
- [SearchToolbarBehavior](/documentation/swiftui/searchtoolbarbehavior)

#### Type Properties

- [static var automatic: SearchToolbarBehavior](/documentation/swiftui/searchtoolbarbehavior/automatic)
- [static var minimize: SearchToolbarBehavior](/documentation/swiftui/searchtoolbarbehavior/minimize)

### Removing default items

- [func toolbar(removing: ToolbarDefaultItemKind?) -> some View](/documentation/swiftui/view/toolbar(removing:))
- [ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind)

#### Getting the default item types

- [static let sidebarToggle: ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind/sidebartoggle)

#### Type Properties

- [static let search: ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind/search)
- [static let title: ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind/title)

### Setting toolbar visibility

- [func toolbar(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbar(_:for:))
- [func toolbarVisibility(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarvisibility(_:for:))
- [func toolbarBackgroundVisibility(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarbackgroundvisibility(_:for:))
- [ToolbarPlacement](/documentation/swiftui/toolbarplacement)

#### Getting placements

- [static var automatic: ToolbarPlacement](/documentation/swiftui/toolbarplacement/automatic)
- [static func accessoryBar<ID>(id: ID) -> ToolbarPlacement](/documentation/swiftui/toolbarplacement/accessorybar(id:))
- [static var bottomBar: ToolbarPlacement](/documentation/swiftui/toolbarplacement/bottombar)
- [static var bottomOrnament: ToolbarPlacement](/documentation/swiftui/toolbarplacement/bottomornament)
- [static var navigationBar: ToolbarPlacement](/documentation/swiftui/toolbarplacement/navigationbar)
- [static var tabBar: ToolbarPlacement](/documentation/swiftui/toolbarplacement/tabbar)
- [static var windowToolbar: ToolbarPlacement](/documentation/swiftui/toolbarplacement/windowtoolbar)

#### Deprecated symbols

- [init<ID>(id: ID)](/documentation/swiftui/toolbarplacement/init(id:))
- [ContentToolbarPlacement](/documentation/swiftui/contenttoolbarplacement)

#### Type Properties

- [static let tabViewSidebar: ContentToolbarPlacement](/documentation/swiftui/contenttoolbarplacement/tabviewsidebar)

### Specifying the role of toolbar content

- [func toolbarRole(ToolbarRole) -> some View](/documentation/swiftui/view/toolbarrole(_:))
- [ToolbarRole](/documentation/swiftui/toolbarrole)

#### Behavior-specific roles

- [static var browser: ToolbarRole](/documentation/swiftui/toolbarrole/browser)
- [static var editor: ToolbarRole](/documentation/swiftui/toolbarrole/editor)
- [static var navigationStack: ToolbarRole](/documentation/swiftui/toolbarrole/navigationstack)

#### Automatic roles

- [static var automatic: ToolbarRole](/documentation/swiftui/toolbarrole/automatic)

### Styling a toolbar

- [func toolbarBackground(_:for:)](/documentation/swiftui/view/toolbarbackground(_:for:))
- [func toolbarColorScheme(ColorScheme?, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarcolorscheme(_:for:))
- [func toolbarForegroundStyle<S>(S, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarforegroundstyle(_:for:))
- [func windowToolbarStyle<S>(S) -> some Scene](/documentation/swiftui/scene/windowtoolbarstyle(_:))
- [WindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle)

#### Getting built-in window toolbar styles

- [static var automatic: DefaultWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/automatic)
- [static var expanded: ExpandedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/expanded)
- [static var unified: UnifiedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unified)
- [static func unified(showsTitle: Bool) -> UnifiedWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unified(showstitle:))
- [static var unifiedCompact: UnifiedCompactWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unifiedcompact)
- [static func unifiedCompact(showsTitle: Bool) -> UnifiedCompactWindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle/unifiedcompact(showstitle:))

#### Supporting types

- [DefaultWindowToolbarStyle](/documentation/swiftui/defaultwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/defaultwindowtoolbarstyle/init())
- [ExpandedWindowToolbarStyle](/documentation/swiftui/expandedwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/expandedwindowtoolbarstyle/init())
- [UnifiedWindowToolbarStyle](/documentation/swiftui/unifiedwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/unifiedwindowtoolbarstyle/init())
- [init(showsTitle: Bool)](/documentation/swiftui/unifiedwindowtoolbarstyle/init(showstitle:))
- [UnifiedCompactWindowToolbarStyle](/documentation/swiftui/unifiedcompactwindowtoolbarstyle)

##### Creating the window toolbar style

- [init()](/documentation/swiftui/unifiedcompactwindowtoolbarstyle/init())
- [init(showsTitle: Bool)](/documentation/swiftui/unifiedcompactwindowtoolbarstyle/init(showstitle:))
- [var toolbarLabelStyle: ToolbarLabelStyle?](/documentation/swiftui/environmentvalues/toolbarlabelstyle)
- [ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle)

#### Type Properties

- [static var automatic: ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle/automatic)
- [static var iconOnly: ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle/icononly)
- [static var titleAndIcon: ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle/titleandicon)
- [static var titleOnly: ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle/titleonly)
- [SpacerSizing](/documentation/swiftui/spacersizing)

#### Type Properties

- [static let fixed: SpacerSizing](/documentation/swiftui/spacersizing/fixed)
- [static let flexible: SpacerSizing](/documentation/swiftui/spacersizing/flexible)

### Configuring the toolbar title display mode

- [func toolbarTitleDisplayMode(ToolbarTitleDisplayMode) -> some View](/documentation/swiftui/view/toolbartitledisplaymode(_:))
- [ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode)

#### Getting display modes

- [static var automatic: ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode/automatic)
- [static var inline: ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode/inline)
- [static var inlineLarge: ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode/inlinelarge)
- [static var large: ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode/large)

### Setting the toolbar title menu

- [func toolbarTitleMenu<C>(content: () -> C) -> some View](/documentation/swiftui/view/toolbartitlemenu(content:))
- [ToolbarTitleMenu](/documentation/swiftui/toolbartitlemenu)

#### Creating a toolbar title menu

- [init()](/documentation/swiftui/toolbartitlemenu/init())
- [init(content: () -> Content)](/documentation/swiftui/toolbartitlemenu/init(content:))

### Creating an ornament

- [func ornament(visibility:attachmentAnchor:contentAlignment:ornament:)](/documentation/swiftui/view/ornament(visibility:attachmentanchor:contentalignment:ornament:))
- [OrnamentAttachmentAnchor](/documentation/swiftui/ornamentattachmentanchor)

#### Getting an anchor

- [static scene(_:)](/documentation/swiftui/ornamentattachmentanchor/scene(_:))

#### Type Methods

- [static func parent(UnitPoint3D) -> OrnamentAttachmentAnchor](/documentation/swiftui/ornamentattachmentanchor/parent(_:))
- [Search](/documentation/swiftui/search)

### Searching your app’s data model

- [Adding a search interface to your app](/documentation/swiftui/adding-a-search-interface-to-your-app)
- [Performing a search operation](/documentation/swiftui/performing-a-search-operation)
- [func searchable(text:placement:prompt:)](/documentation/swiftui/view/searchable(text:placement:prompt:))
- [func searchable(text:tokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:placement:prompt:token:))
- [func searchable(text:editableTokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:editabletokens:placement:prompt:token:))
- [SearchFieldPlacement](/documentation/swiftui/searchfieldplacement)

#### Getting a search field placement

- [static let automatic: SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/automatic)
- [static let navigationBarDrawer: SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/navigationbardrawer)
- [static func navigationBarDrawer(displayMode: SearchFieldPlacement.NavigationBarDrawerDisplayMode) -> SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/navigationbardrawer(displaymode:))
- [static var sidebar: SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/sidebar)
- [static let toolbar: SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/toolbar)

#### Supporting types

- [SearchFieldPlacement.NavigationBarDrawerDisplayMode](/documentation/swiftui/searchfieldplacement/navigationbardrawerdisplaymode)

##### Getting display modes

- [static let always: SearchFieldPlacement.NavigationBarDrawerDisplayMode](/documentation/swiftui/searchfieldplacement/navigationbardrawerdisplaymode/always)
- [static let automatic: SearchFieldPlacement.NavigationBarDrawerDisplayMode](/documentation/swiftui/searchfieldplacement/navigationbardrawerdisplaymode/automatic)

#### Type Properties

- [static var toolbarPrincipal: SearchFieldPlacement](/documentation/swiftui/searchfieldplacement/toolbarprincipal)

### Making search suggestions

- [Suggesting search terms](/documentation/swiftui/suggesting-search-terms)
- [func searchSuggestions<S>(() -> S) -> some View](/documentation/swiftui/view/searchsuggestions(_:))
- [func searchSuggestions(Visibility, for: SearchSuggestionsPlacement.Set) -> some View](/documentation/swiftui/view/searchsuggestions(_:for:))
- [func searchCompletion(_:)](/documentation/swiftui/view/searchcompletion(_:))
- [func searchable(text:tokens:suggestedTokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:placement:prompt:token:))
- [SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement)

#### Getting placements

- [static var automatic: SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement/automatic)
- [static var content: SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement/content)
- [static var menu: SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement/menu)

#### Supporting types

- [SearchSuggestionsPlacement.Set](/documentation/swiftui/searchsuggestionsplacement/set)

##### Getting placement sets

- [static var content: SearchSuggestionsPlacement.Set](/documentation/swiftui/searchsuggestionsplacement/set/content)
- [static var menu: SearchSuggestionsPlacement.Set](/documentation/swiftui/searchsuggestionsplacement/set/menu)

##### Creating a set

- [init(rawValue: Int)](/documentation/swiftui/searchsuggestionsplacement/set/init(rawvalue:))
- [var rawValue: Int](/documentation/swiftui/searchsuggestionsplacement/set/rawvalue)

##### Supporting types

- [SearchSuggestionsPlacement.Set.Element](/documentation/swiftui/searchsuggestionsplacement/set/element)

### Limiting search scope

- [Scoping a search operation](/documentation/swiftui/scoping-a-search-operation)
- [func searchScopes<V, S>(Binding<V>, scopes: () -> S) -> some View](/documentation/swiftui/view/searchscopes(_:scopes:))
- [func searchScopes<V, S>(Binding<V>, activation: SearchScopeActivation, () -> S) -> some View](/documentation/swiftui/view/searchscopes(_:activation:_:))
- [SearchScopeActivation](/documentation/swiftui/searchscopeactivation)

#### Getting search scope activiation types

- [static var automatic: SearchScopeActivation](/documentation/swiftui/searchscopeactivation/automatic)
- [static var onSearchPresentation: SearchScopeActivation](/documentation/swiftui/searchscopeactivation/onsearchpresentation)
- [static var onTextEntry: SearchScopeActivation](/documentation/swiftui/searchscopeactivation/ontextentry)

### Detecting, activating, and dismissing search

- [Managing search interface activation](/documentation/swiftui/managing-search-interface-activation)
- [var isSearching: Bool](/documentation/swiftui/environmentvalues/issearching)
- [var dismissSearch: DismissSearchAction](/documentation/swiftui/environmentvalues/dismisssearch)
- [DismissSearchAction](/documentation/swiftui/dismisssearchaction)

#### Calling the action

- [func callAsFunction()](/documentation/swiftui/dismisssearchaction/callasfunction())
- [func searchable(text:isPresented:placement:prompt:)](/documentation/swiftui/view/searchable(text:ispresented:placement:prompt:))
- [func searchable(text:tokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:ispresented:placement:prompt:token:))
- [func searchable(text:editableTokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:editabletokens:ispresented:placement:prompt:token:))
- [func searchable(text:tokens:suggestedTokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:ispresented:placement:prompt:token:))

### Displaying toolbar content during search

- [func searchPresentationToolbarBehavior(SearchPresentationToolbarBehavior) -> some View](/documentation/swiftui/view/searchpresentationtoolbarbehavior(_:))
- [SearchPresentationToolbarBehavior](/documentation/swiftui/searchpresentationtoolbarbehavior)

#### Getting toolbar behaviors

- [static var automatic: SearchPresentationToolbarBehavior](/documentation/swiftui/searchpresentationtoolbarbehavior/automatic)
- [static var avoidHidingContent: SearchPresentationToolbarBehavior](/documentation/swiftui/searchpresentationtoolbarbehavior/avoidhidingcontent)

### Searching for text in a view

- [func findNavigator(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/findnavigator(ispresented:))
- [func findDisabled(Bool) -> some View](/documentation/swiftui/view/finddisabled(_:))
- [func replaceDisabled(Bool) -> some View](/documentation/swiftui/view/replacedisabled(_:))
- [FindContext](/documentation/swiftui/findcontext)

#### Instance Properties

- [var isPresented: Binding<Bool>?](/documentation/swiftui/findcontext/ispresented)
- [var supportsReplace: Bool](/documentation/swiftui/findcontext/supportsreplace)
- [App extensions](/documentation/swiftui/app-extensions)

### Creating widgets

- [Building Widgets Using WidgetKit and SwiftUI](/documentation/widgetkit/building_widgets_using_widgetkit_and_swiftui)
- [Creating a widget extension](/documentation/widgetkit/creating-a-widget-extension)
- [Keeping a widget up to date](/documentation/widgetkit/keeping-a-widget-up-to-date)
- [Making a configurable widget](/documentation/widgetkit/making-a-configurable-widget)
- [Widget](/documentation/swiftui/widget)

#### Implementing a widget

- [var body: Self.Body](/documentation/swiftui/widget/body-swift.property)
- [Body](/documentation/swiftui/widget/body-swift.associatedtype)

#### Running a widget

- [init()](/documentation/swiftui/widget/init())
- [static func main()](/documentation/swiftui/widget/main())
- [WidgetBundle](/documentation/swiftui/widgetbundle)

#### Implementing a widget bundle

- [var body: Self.Body](/documentation/swiftui/widgetbundle/body-swift.property)
- [Body](/documentation/swiftui/widgetbundle/body-swift.associatedtype)
- [WidgetBundleBuilder](/documentation/swiftui/widgetbundlebuilder)

##### Bundling widgets

- [static func buildBlock() -> some Widget](/documentation/swiftui/widgetbundlebuilder/buildblock())
- [static buildBlock(_:)](/documentation/swiftui/widgetbundlebuilder/buildblock(_:))
- [static buildExpression(_:)](/documentation/swiftui/widgetbundlebuilder/buildexpression(_:))
- [static buildLimitedAvailability(_:)](/documentation/swiftui/widgetbundlebuilder/buildlimitedavailability(_:))
- [static func buildOptional((any Widget & _LimitedAvailabilityWidgetMarker)?) -> some Widget](/documentation/swiftui/widgetbundlebuilder/buildoptional(_:))

#### Running a widget bundle

- [init()](/documentation/swiftui/widgetbundle/init())
- [static func main()](/documentation/swiftui/widgetbundle/main())
- [LimitedAvailabilityConfiguration](/documentation/swiftui/limitedavailabilityconfiguration)
- [WidgetConfiguration](/documentation/swiftui/widgetconfiguration)

#### Implementing a widget

- [var body: Self.Body](/documentation/swiftui/widgetconfiguration/body-swift.property)
- [Body](/documentation/swiftui/widgetconfiguration/body-swift.associatedtype)

#### Setting a name

- [func configurationDisplayName(_:)](/documentation/swiftui/widgetconfiguration/configurationdisplayname(_:))

#### Setting a description

- [func description(_:)](/documentation/swiftui/widgetconfiguration/description(_:))

#### Setting the appearance

- [func supportedFamilies([WidgetFamily]) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/supportedfamilies(_:))
- [func contentMarginsDisabled() -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/contentmarginsdisabled())
- [func disfavoredLocations([WidgetLocation], for: [WidgetFamily]) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/disfavoredlocations(_:for:))
- [func containerBackgroundRemovable(Bool) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/containerbackgroundremovable(_:))

#### Managing background tasks

- [func backgroundTask<D, R>(BackgroundTask<D, R>, action: (D) async -> R) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/backgroundtask(_:action:))
- [func onBackgroundURLSessionEvents(matching:_:)](/documentation/swiftui/widgetconfiguration/onbackgroundurlsessionevents(matching:_:))

#### Instance Methods

- [func associatedKind(String?) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/associatedkind(_:))
- [func promptsForUserConfiguration() -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/promptsforuserconfiguration())
- [func pushHandler(any WidgetPushHandler.Type) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/pushhandler(_:))
- [func supplementalActivityFamilies([ActivityFamily]) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/supplementalactivityfamilies(_:))
- [func supportedMountingStyles([WidgetMountingStyle]) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/supportedmountingstyles(_:))
- [func widgetTexture(WidgetTexture) -> some WidgetConfiguration](/documentation/swiftui/widgetconfiguration/widgettexture(_:))
- [EmptyWidgetConfiguration](/documentation/swiftui/emptywidgetconfiguration)

#### Creating a configuration

- [init()](/documentation/swiftui/emptywidgetconfiguration/init())

### Composing control widgets

- [ControlWidget](/documentation/swiftui/controlwidget)

#### Associated Types

- [Body](/documentation/swiftui/controlwidget/body-swift.associatedtype)

#### Initializers

- [init()](/documentation/swiftui/controlwidget/init())

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/controlwidget/body-swift.property)

#### Type Methods

- [static func main()](/documentation/swiftui/controlwidget/main())
- [ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration)

#### Associated Types

- [Body](/documentation/swiftui/controlwidgetconfiguration/body-swift.associatedtype)

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/controlwidgetconfiguration/body-swift.property)

#### Instance Methods

- [func description(LocalizedStringResource) -> some ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration/description(_:))
- [func displayName(LocalizedStringResource) -> some ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration/displayname(_:))
- [func promptsForUserConfiguration() -> some ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration/promptsforuserconfiguration())
- [func pushHandler(any ControlPushHandler.Type) -> some ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration/pushhandler(_:))
- [EmptyControlWidgetConfiguration](/documentation/swiftui/emptycontrolwidgetconfiguration)

#### Initializers

- [init()](/documentation/swiftui/emptycontrolwidgetconfiguration/init())
- [ControlWidgetConfigurationBuilder](/documentation/swiftui/controlwidgetconfigurationbuilder)

#### Type Methods

- [static func buildBlock<Content>(Content) -> some ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfigurationbuilder/buildblock(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/controlwidgetconfigurationbuilder/buildexpression(_:))
- [ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate)

#### Associated Types

- [Body](/documentation/swiftui/controlwidgettemplate/body-swift.associatedtype)

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/controlwidgettemplate/body-swift.property)

#### Instance Methods

- [func disabled(Bool) -> some ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate/disabled(_:))
- [func privacySensitive(Bool) -> some ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate/privacysensitive(_:))
- [func tint(Color?) -> some ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate/tint(_:))
- [EmptyControlWidgetTemplate](/documentation/swiftui/emptycontrolwidgettemplate)

#### Initializers

- [init()](/documentation/swiftui/emptycontrolwidgettemplate/init())
- [ControlWidgetTemplateBuilder](/documentation/swiftui/controlwidgettemplatebuilder)

#### Type Methods

- [static func buildBlock<Content>(Content) -> some ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplatebuilder/buildblock(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/controlwidgettemplatebuilder/buildexpression(_:))
- [func controlWidgetActionHint(_:)](/documentation/swiftui/view/controlwidgetactionhint(_:))
- [func controlWidgetStatus(_:)](/documentation/swiftui/view/controlwidgetstatus(_:))

### Labeling a widget

- [func widgetLabel(_:)](/documentation/swiftui/view/widgetlabel(_:))
- [func widgetLabel<Label>(label: () -> Label) -> some View](/documentation/swiftui/view/widgetlabel(label:))

### Styling a widget group

- [func accessoryWidgetGroupStyle(AccessoryWidgetGroupStyle) -> some View](/documentation/swiftui/view/accessorywidgetgroupstyle(_:))

### Controlling the accented group

- [func widgetAccentable(Bool) -> some View](/documentation/swiftui/view/widgetaccentable(_:))

### Managing placement in the Dynamic Island

- [func dynamicIsland(verticalPlacement: DynamicIslandExpandedRegionVerticalPlacement) -> some View](/documentation/swiftui/view/dynamicisland(verticalplacement:))

