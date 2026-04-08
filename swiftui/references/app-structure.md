# App Structure — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [App structure](#app-structure)
- [Scenes](#scenes)
- [Windows](#windows)
- [Immersive spaces](#immersive-spaces)
- [Documents](#documents)
- [Navigation](#navigation)
- [Modal presentations](#modal-presentations)
- [Toolbars](#toolbars)
- [Search](#search)
- [App extensions](#app-extensions)

---

## App structure

- [App organization](/documentation/swiftui/app-organization) (article)

### Creating an app

- [Destination Video](/documentation/visionos/destination-video) (article)
- [Hello World](/documentation/visionos/world) (article)
- [Backyard Birds: Building an app with SwiftData and widgets](/documentation/swiftui/backyard-birds-sample) (article)
- [Food Truck: Building a SwiftUI multiplatform app](/documentation/swiftui/food-truck-building-a-swiftui-multiplatform-app) (article)
- [Fruta: Building a feature-rich app with SwiftUI](/documentation/appclip/fruta-building-a-feature-rich-app-with-swiftui) (article)
- [Migrating to the SwiftUI life cycle](/documentation/swiftui/migrating-to-the-swiftui-life-cycle) (article)
- [App](/documentation/swiftui/app) — protocol for the app entry point; provides body and main()

### Targeting iOS and iPadOS

- [UILaunchScreen](/documentation/bundleresources/information-property-list/uilaunchscreen) — Info.plist key for launch screen config
- [UILaunchScreens](/documentation/bundleresources/information-property-list/uilaunchscreens) — per-scene launch screen config
- [UIApplicationDelegateAdaptor](/documentation/swiftui/uiapplicationdelegateadaptor) — bridges UIApplicationDelegate into SwiftUI

### Targeting macOS

- [NSApplicationDelegateAdaptor](/documentation/swiftui/nsapplicationdelegateadaptor) — bridges NSApplicationDelegate into SwiftUI

### Targeting watchOS

- [WKApplicationDelegateAdaptor](/documentation/swiftui/wkapplicationdelegateadaptor) — bridges WKApplicationDelegate into SwiftUI
- [WKExtensionDelegateAdaptor](/documentation/swiftui/wkextensiondelegateadaptor) — bridges WKExtensionDelegate into SwiftUI

### Targeting tvOS

- [Creating a tvOS media catalog app in SwiftUI](/documentation/swiftui/creating-a-tvos-media-catalog-app-in-swiftui) (article)

### Handling system recenter events

- [WorldRecenterPhase](/documentation/swiftui/worldrecenterphase) — enum: began, ended (visionOS recenter)

---

## Scenes

- [Scenes](/documentation/swiftui/scenes) (article)
- [Scene](/documentation/swiftui/scene) — protocol for scene definition; body, onChange, backgroundTask, commands, sizing, positioning, styling, environment, dialogs
- [SceneBuilder](/documentation/swiftui/scenebuilder) — result builder for composing scenes

### Monitoring scene life cycle

- `var scenePhase: ScenePhase` — [EnvironmentValues.scenePhase](/documentation/swiftui/environmentvalues/scenephase)
- [ScenePhase](/documentation/swiftui/scenephase) — enum: active, inactive, background

### Managing a settings window

- [Settings](/documentation/swiftui/settings) — macOS settings scene
- [SettingsLink](/documentation/swiftui/settingslink) — button that opens settings
- [DefaultSettingsLinkLabel](/documentation/swiftui/defaultsettingslinklabel) — default label for SettingsLink
- [OpenSettingsAction](/documentation/swiftui/opensettingsaction) — callable action to open settings
- `var openSettings: OpenSettingsAction` — [EnvironmentValues.openSettings](/documentation/swiftui/environmentvalues/opensettings)

### Building a menu bar

- [Building and customizing the menu bar with SwiftUI](/documentation/swiftui/building-and-customizing-the-menu-bar-with-swiftui) (article)

### Creating a menu bar extra

- [MenuBarExtra](/documentation/swiftui/menubarextra) — macOS menu bar item scene
- [MenuBarExtraStyle](/documentation/swiftui/menubarextrastyle) — styles: automatic, menu, window
  - Supporting types: AutomaticMenuBarExtraStyle, PullDownMenuBarExtraStyle, WindowMenuBarExtraStyle

### Creating watch notifications

- [WKNotificationScene](/documentation/swiftui/wknotificationscene) — watchOS notification scene

---

## Windows

- [Windows](/documentation/swiftui/windows) (article)
- [Customizing window styles and state-restoration behavior in macOS](/documentation/swiftui/customizing-window-styles-and-state-restoration-behavior-in-macos) (article)
- [Bringing multiple windows to your SwiftUI app](/documentation/swiftui/bringing-multiple-windows-to-your-swiftui-app) (article)

### Creating windows

- [WindowGroup](/documentation/swiftui/windowgroup) — primary multi-window scene; supports data-driven and identified variants
- [PresentedWindowContent](/documentation/swiftui/presentedwindowcontent) — content wrapper for presented windows
- [Window](/documentation/swiftui/window) — single-instance named window (macOS)
- [UtilityWindow](/documentation/swiftui/utilitywindow) — utility-panel-style window (macOS)
- [WindowStyle](/documentation/swiftui/windowstyle) — protocol; styles: automatic, hiddenTitleBar, plain, titleBar, volumetric
  - Supporting types: DefaultWindowStyle, HiddenTitleBarWindowStyle, PlainWindowStyle, TitleBarWindowStyle, VolumetricWindowStyle
- `func windowStyle<S>(S) -> some Scene` — [Scene.windowStyle](/documentation/swiftui/scene/windowstyle(_:))

### Styling the associated toolbar

- `func windowToolbarStyle<S>(S) -> some Scene` — [Scene.windowToolbarStyle](/documentation/swiftui/scene/windowtoolbarstyle(_:))
- `func windowToolbarLabelStyle(Binding<ToolbarLabelStyle>) -> some Scene` — [Scene.windowToolbarLabelStyle](/documentation/swiftui/scene/windowtoolbarlabelstyle(_:))
- `func windowToolbarLabelStyle(fixed:) -> some Scene` — [Scene.windowToolbarLabelStyle(fixed:)](/documentation/swiftui/scene/windowtoolbarlabelstyle(fixed:))
- [WindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle) — protocol; styles: automatic, expanded, unified, unified(showsTitle:), unifiedCompact, unifiedCompact(showsTitle:)
  - Supporting types: DefaultWindowToolbarStyle, ExpandedWindowToolbarStyle, UnifiedWindowToolbarStyle, UnifiedCompactWindowToolbarStyle

### Opening windows

- [Presenting windows and spaces](/documentation/visionos/presenting-windows-and-spaces) (article)
- `var supportsMultipleWindows: Bool` — [EnvironmentValues.supportsMultipleWindows](/documentation/swiftui/environmentvalues/supportsmultiplewindows)
- `var openWindow: OpenWindowAction` — [EnvironmentValues.openWindow](/documentation/swiftui/environmentvalues/openwindow)
- [OpenWindowAction](/documentation/swiftui/openwindowaction) — callable action to open windows by id/value; includes SharingBehavior
- [PushWindowAction](/documentation/swiftui/pushwindowaction) — callable action to push a window (visionOS)

### Closing windows

- `var dismissWindow: DismissWindowAction` — [EnvironmentValues.dismissWindow](/documentation/swiftui/environmentvalues/dismisswindow)
- [DismissWindowAction](/documentation/swiftui/dismisswindowaction) — callable action to dismiss windows by id/value
- `var dismiss: DismissAction` — [EnvironmentValues.dismiss](/documentation/swiftui/environmentvalues/dismiss)
- [DismissAction](/documentation/swiftui/dismissaction) — callable action to dismiss current presentation
- [DismissBehavior](/documentation/swiftui/dismissbehavior) — values: destructive, interactive

### Sizing a window

- [Positioning and sizing windows](/documentation/visionos/positioning-and-sizing-windows) (article)
- `func defaultSize(...)` — [Scene.defaultSize](/documentation/swiftui/scene/defaultsize(_:)) — multiple variants: 2D, 3D, UnitLength
- `func windowResizability(WindowResizability) -> some Scene` — [Scene.windowResizability](/documentation/swiftui/scene/windowresizability(_:))
- [WindowResizability](/documentation/swiftui/windowresizability) — values: automatic, contentMinSize, contentSize
- `func windowIdealSize(WindowIdealSize) -> some Scene` — [Scene.windowIdealSize](/documentation/swiftui/scene/windowidealsize(_:))
- [WindowIdealSize](/documentation/swiftui/windowidealsize) — values: automatic, fitToContent, maximum

### Positioning a window

- `func defaultPosition(UnitPoint) -> some Scene` — [Scene.defaultPosition](/documentation/swiftui/scene/defaultposition(_:))
- [WindowLevel](/documentation/swiftui/windowlevel) — values: automatic, desktop, floating, normal
- `func windowLevel(WindowLevel) -> some Scene` — [Scene.windowLevel](/documentation/swiftui/scene/windowlevel(_:))
- [WindowLayoutRoot](/documentation/swiftui/windowlayoutroot) — layout root for placement calculations
- [WindowPlacement](/documentation/swiftui/windowplacement) — placement value with Position, size variants
  - [WindowPlacement.Position](/documentation/swiftui/windowplacement/position) — static methods: above, below, leading, trailing, replacing, utilitypanel
- `func defaultWindowPlacement(...)` — [Scene.defaultWindowPlacement](/documentation/swiftui/scene/defaultwindowplacement(_:))
- `func windowIdealPlacement(...)` — [Scene.windowIdealPlacement](/documentation/swiftui/scene/windowidealplacement(_:))
- [WindowPlacementContext](/documentation/swiftui/windowplacementcontext) — provides defaultDisplay, windows
- [WindowProxy](/documentation/swiftui/windowproxy) — id, phase of a window
- [DisplayProxy](/documentation/swiftui/displayproxy) — bounds, safeAreaInsets, visibleRect

### Configuring window visibility

- [WindowVisibilityToggle](/documentation/swiftui/windowvisibilitytoggle) — toggle for showing/hiding a window
- [DefaultWindowVisibilityToggleLabel](/documentation/swiftui/defaultwindowvisibilitytogglelabel) — default label
- `func defaultLaunchBehavior(SceneLaunchBehavior) -> some Scene` — [Scene.defaultLaunchBehavior](/documentation/swiftui/scene/defaultlaunchbehavior(_:))
- `func restorationBehavior(SceneRestorationBehavior) -> some Scene` — [Scene.restorationBehavior](/documentation/swiftui/scene/restorationbehavior(_:))
- [SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior) — values: automatic, presented, suppressed
- [SceneRestorationBehavior](/documentation/swiftui/scenerestorationbehavior) — values: automatic, disabled
- `func persistentSystemOverlays(Visibility) -> some Scene` — [Scene.persistentSystemOverlays](/documentation/swiftui/scene/persistentsystemoverlays(_:))
- `func windowToolbarFullScreenVisibility(WindowToolbarFullScreenVisibility) -> some View` — [View.windowToolbarFullScreenVisibility](/documentation/swiftui/view/windowtoolbarfullscreenvisibility(_:))
- [WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility) — values: automatic, onHover, visible

### Managing window behavior

- [WindowManagerRole](/documentation/swiftui/windowmanagerrole) — values: associated, automatic, principal
- `func windowManagerRole(WindowManagerRole) -> some Scene` — [Scene.windowManagerRole](/documentation/swiftui/scene/windowmanagerrole(_:))
- [WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior) — values: automatic, disabled, enabled
- `func windowDismissBehavior(WindowInteractionBehavior) -> some View` — [View.windowDismissBehavior](/documentation/swiftui/view/windowdismissbehavior(_:))
- `func windowFullScreenBehavior(WindowInteractionBehavior) -> some View` — [View.windowFullScreenBehavior](/documentation/swiftui/view/windowfullscreenbehavior(_:))
- `func windowMinimizeBehavior(WindowInteractionBehavior) -> some View` — [View.windowMinimizeBehavior](/documentation/swiftui/view/windowminimizebehavior(_:))
- `func windowResizeBehavior(WindowInteractionBehavior) -> some View` — [View.windowResizeBehavior](/documentation/swiftui/view/windowresizebehavior(_:))
- `func windowBackgroundDragBehavior(WindowInteractionBehavior) -> some Scene` — [Scene.windowBackgroundDragBehavior](/documentation/swiftui/scene/windowbackgrounddragbehavior(_:))

### Interacting with volumes

- `func onVolumeViewpointChange(updateStrategy:initial:_:) -> some View` — [View.onVolumeViewpointChange](/documentation/swiftui/view/onvolumeviewpointchange(updatestrategy:initial:_:))
- `func supportedVolumeViewpoints(SquareAzimuth.Set) -> some View` — [View.supportedVolumeViewpoints](/documentation/swiftui/view/supportedvolumeviewpoints(_:))
- [VolumeViewpointUpdateStrategy](/documentation/swiftui/volumeviewpointupdatestrategy) — values: all, supported
- [Viewpoint3D](/documentation/swiftui/viewpoint3d) — 3D viewpoint; standard value, squareAzimuth property
- [SquareAzimuth](/documentation/swiftui/squareazimuth) — enum: front, back, left, right; SquareAzimuth.Set for combinations
- [WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior) — values: adaptive, automatic, gravityAligned
- `func volumeWorldAlignment(WorldAlignmentBehavior) -> some Scene` — [Scene.volumeWorldAlignment](/documentation/swiftui/scene/volumeworldalignment(_:))
- [WorldScalingBehavior](/documentation/swiftui/worldscalingbehavior) — values: automatic, dynamic
- `func defaultWorldScaling(WorldScalingBehavior) -> some Scene` — [Scene.defaultWorldScaling](/documentation/swiftui/scene/defaultworldscaling(_:))
- [WorldScalingCompensation](/documentation/swiftui/worldscalingcompensation) — values: scaled, unscaled
- `var worldTrackingLimitations: Set<WorldTrackingLimitation>` — [EnvironmentValues.worldTrackingLimitations](/documentation/swiftui/environmentvalues/worldtrackinglimitations)
- [WorldTrackingLimitation](/documentation/swiftui/worldtrackinglimitation) — values: orientation, translation
- [SurfaceSnappingInfo](/documentation/swiftui/surfacesnappinginfo) — surface classification, snap state, authorization status

### Deprecated types

- [ControlActiveState](/documentation/swiftui/controlactivestate) [deprecated] — enum: key, active, inactive

---

## Immersive spaces

- [Immersive spaces](/documentation/swiftui/immersive-spaces) (article)

### Creating an immersive space

- [ImmersiveSpace](/documentation/swiftui/immersivespace) — visionOS immersive space scene; supports data-driven, identified, foveated streaming variants
- [ImmersiveSpaceViewContent](/documentation/swiftui/immersivespaceviewcontent) — view content for immersive space
- [ImmersiveSpaceContent](/documentation/swiftui/immersivespacecontent) — protocol for immersive space content
- [ImmersiveSpaceContentBuilder](/documentation/swiftui/immersivespacecontentbuilder) — result builder for immersive content
- `func immersionStyle(selection:in:) -> some Scene` — [Scene.immersionStyle](/documentation/swiftui/scene/immersionstyle(selection:in:))
- [ImmersionStyle](/documentation/swiftui/immersionstyle) — protocol; styles: automatic, full, mixed, progressive
  - Supporting types: AutomaticImmersionStyle, FullImmersionStyle, MixedImmersionStyle, ProgressiveImmersionStyle
  - Progressive variants: progressive(_:initialAmount:), progressive(aspectRatio:)
- `var immersiveSpaceDisplacement: Pose3D` — [EnvironmentValues.immersiveSpaceDisplacement](/documentation/swiftui/environmentvalues/immersivespacedisplacement)
- [ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior) — values: automatic, coexist, replace
- [ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio) — values: automatic, landscape, portrait

### Opening an immersive space

- `var openImmersiveSpace: OpenImmersiveSpaceAction` — [EnvironmentValues.openImmersiveSpace](/documentation/swiftui/environmentvalues/openimmersivespace)
- [OpenImmersiveSpaceAction](/documentation/swiftui/openimmersivespaceaction) — callable async action; returns Result (opened, userCancelled, error)

### Closing the immersive space

- `var dismissImmersiveSpace: DismissImmersiveSpaceAction` — [EnvironmentValues.dismissImmersiveSpace](/documentation/swiftui/environmentvalues/dismissimmersivespace)
- [DismissImmersiveSpaceAction](/documentation/swiftui/dismissimmersivespaceaction) — callable async action

### Hiding upper limbs during immersion

- `func upperLimbVisibility(Visibility) -> some Scene` — [Scene.upperLimbVisibility](/documentation/swiftui/scene/upperlimbvisibility(_:))
- `func upperLimbVisibility(Visibility) -> some View` — [View.upperLimbVisibility](/documentation/swiftui/view/upperlimbvisibility(_:))

### Adjusting content brightness

- `func immersiveContentBrightness(ImmersiveContentBrightness) -> some Scene` — [Scene.immersiveContentBrightness](/documentation/swiftui/scene/immersivecontentbrightness(_:))
- [ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness) — values: automatic, dark, dim, bright, custom(Double)

### Responding to immersion changes

- `func onImmersionChange(initial:_:) -> some View` — [View.onImmersionChange](/documentation/swiftui/view/onimmersionchange(initial:_:))
- [ImmersionChangeContext](/documentation/swiftui/immersionchangecontext) — provides amount property

### Adding menu items to an immersive space

- `func immersiveEnvironmentPicker(content:) -> some View` — [View.immersiveEnvironmentPicker](/documentation/swiftui/view/immersiveenvironmentpicker(content:))

### Handling remote immersive spaces

- [RemoteImmersiveSpace](/documentation/swiftui/remoteimmersivespace) — remote immersive space scene (visionOS)
- [RemoteDeviceIdentifier](/documentation/swiftui/remotedeviceidentifier) — identifier for a remote device

---

## Documents

- [Documents](/documentation/swiftui/documents) (article)
- [Building a document-based app with SwiftUI](/documentation/swiftui/building-a-document-based-app-with-swiftui) (article)
- [Building a document-based app using SwiftData](/documentation/swiftui/building-a-document-based-app-using-swiftdata) (article)

### Creating a document

- [DocumentGroup](/documentation/swiftui/documentgroup) — scene for document-based apps; supports FileDocument, ReferenceFileDocument, SwiftData

### Storing document data in a structure instance

- [FileDocument](/documentation/swiftui/filedocument) — protocol for value-type documents (struct)
- [FileDocumentConfiguration](/documentation/swiftui/filedocumentconfiguration) — wraps document binding, fileURL, isEditable

### Storing document data in a class instance

- [ReferenceFileDocument](/documentation/swiftui/referencefiledocument) — protocol for reference-type documents (class)
- [ReferenceFileDocumentConfiguration](/documentation/swiftui/referencefiledocumentconfiguration) — wraps document, fileURL, isEditable, undoManager

### Accessing document configuration

- `var documentConfiguration: DocumentConfiguration?` — [EnvironmentValues.documentConfiguration](/documentation/swiftui/environmentvalues/documentconfiguration)
- [DocumentConfiguration](/documentation/swiftui/documentconfiguration) — provides fileURL, isEditable

### Reading and writing documents

- [FileDocumentReadConfiguration](/documentation/swiftui/filedocumentreadconfiguration) — contentType, file
- [FileDocumentWriteConfiguration](/documentation/swiftui/filedocumentwriteconfiguration) — contentType, existingFile

### Opening a document programmatically

- `var newDocument: NewDocumentAction` — [EnvironmentValues.newDocument](/documentation/swiftui/environmentvalues/newdocument)
- [NewDocumentAction](/documentation/swiftui/newdocumentaction) — callable action to create new documents
- `var openDocument: OpenDocumentAction` — [EnvironmentValues.openDocument](/documentation/swiftui/environmentvalues/opendocument)
- [OpenDocumentAction](/documentation/swiftui/opendocumentaction) — callable async action to open a document at URL

### Configuring the document launch experience

- [DocumentGroupLaunchScene](/documentation/swiftui/documentgrouplaunchscene) — customizable document browser launch scene
- [DocumentLaunchView](/documentation/swiftui/documentlaunchview) — launch view for document apps
- [DocumentLaunchGeometryProxy](/documentation/swiftui/documentlaunchgeometryproxy) — frame, titleViewFrame
- [DefaultDocumentGroupLaunchActions](/documentation/swiftui/defaultdocumentgrouplaunchactions) — default launch actions
- [NewDocumentButton](/documentation/swiftui/newdocumentbutton) — button to create a new document
- [DocumentBaseBox](/documentation/swiftui/documentbasebox) — protocol for document base boxing

### Renaming a document

- [RenameButton](/documentation/swiftui/renamebutton) — button that triggers rename action
- `func renameAction(_:)` — [View.renameAction](/documentation/swiftui/view/renameaction(_:))
- `var rename: RenameAction?` — [EnvironmentValues.rename](/documentation/swiftui/environmentvalues/rename)
- [RenameAction](/documentation/swiftui/renameaction) — callable action

---

## Navigation

- [Navigation](/documentation/swiftui/navigation) (article)
- [Understanding the navigation stack](/documentation/swiftui/understanding-the-navigation-stack) (article)

### Presenting views in columns

- [Bringing robust navigation structure to your SwiftUI app](/documentation/swiftui/bringing-robust-navigation-structure-to-your-swiftui-app) (article)
- [Migrating to new navigation types](/documentation/swiftui/migrating-to-new-navigation-types) (article)
- [NavigationSplitView](/documentation/swiftui/navigationsplitview) — two/three-column navigation; supports column visibility and preferred compact column
- `func navigationSplitViewStyle<S>(S) -> some View` — [View.navigationSplitViewStyle](/documentation/swiftui/view/navigationsplitviewstyle(_:))
- `func navigationSplitViewColumnWidth(CGFloat) -> some View` — [View.navigationSplitViewColumnWidth](/documentation/swiftui/view/navigationsplitviewcolumnwidth(_:))
- `func navigationSplitViewColumnWidth(min:ideal:max:) -> some View` — [View.navigationSplitViewColumnWidth(min:ideal:max:)](/documentation/swiftui/view/navigationsplitviewcolumnwidth(min:ideal:max:))
- [NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility) — values: automatic, all, doubleColumn, detailOnly
- [NavigationLink](/documentation/swiftui/navigationlink) — link that pushes destination or presents value
  - Deprecated variants: [NavigationLink deprecated symbols](/documentation/swiftui/navigationlink-deprecated) [deprecated]

### Stacking views in one column

- [NavigationStack](/documentation/swiftui/navigationstack) — stack-based navigation with optional path binding
- [NavigationPath](/documentation/swiftui/navigationpath) — type-erased navigation path; supports append, removeLast, CodableRepresentation
- `func navigationDestination(for:destination:) -> some View` — [View.navigationDestination(for:destination:)](/documentation/swiftui/view/navigationdestination(for:destination:))
- `func navigationDestination(isPresented:destination:) -> some View` — [View.navigationDestination(isPresented:destination:)](/documentation/swiftui/view/navigationdestination(ispresented:destination:))
- `func navigationDestination(item:destination:) -> some View` — [View.navigationDestination(item:destination:)](/documentation/swiftui/view/navigationdestination(item:destination:))

### Managing column collapse

- [NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn) — values: sidebar, content, detail

### Setting titles for navigation content

- `func navigationTitle(_:)` — [View.navigationTitle](/documentation/swiftui/view/navigationtitle(_:))
- `func navigationSubtitle(_:)` — [View.navigationSubtitle](/documentation/swiftui/view/navigationsubtitle(_:))
- `func navigationDocument(_:)` — [View.navigationDocument](/documentation/swiftui/view/navigationdocument(_:))
- `func navigationDocument(_:preview:)` — [View.navigationDocument(_:preview:)](/documentation/swiftui/view/navigationdocument(_:preview:))

### Configuring the navigation bar

- `func navigationBarBackButtonHidden(Bool) -> some View` — [View.navigationBarBackButtonHidden](/documentation/swiftui/view/navigationbarbackbuttonhidden(_:))
- `func navigationBarTitleDisplayMode(NavigationBarItem.TitleDisplayMode) -> some View` — [View.navigationBarTitleDisplayMode](/documentation/swiftui/view/navigationbartitledisplaymode(_:))
- [NavigationBarItem](/documentation/swiftui/navigationbaritem) — contains TitleDisplayMode enum: automatic, inline, large

### Configuring the sidebar

- `var sidebarRowSize: SidebarRowSize` — [EnvironmentValues.sidebarRowSize](/documentation/swiftui/environmentvalues/sidebarrowsize)
- [SidebarRowSize](/documentation/swiftui/sidebarrowsize) — enum: small, medium, large

### Presenting views in tabs

- [Enhancing your app's content with tab navigation](/documentation/swiftui/enhancing-your-app-content-with-tab-navigation) (article)
- [TabView](/documentation/swiftui/tabview) — tabbed container view; supports selection binding
- [TabSearchActivation](/documentation/swiftui/tabsearchactivation) — values: automatic, searchTabSelection
- [Tab](/documentation/swiftui/tab) — individual tab with label, systemImage, image, role variants
- [DefaultTabLabel](/documentation/swiftui/defaulttablabel) — default tab label type
- [TabRole](/documentation/swiftui/tabrole) — values: search
- [TabSection](/documentation/swiftui/tabsection) — groups tabs into sections with optional header
- `func tabViewStyle<S>(S) -> some View` — [View.tabViewStyle](/documentation/swiftui/view/tabviewstyle(_:))

### Configuring a tab bar

- `func defaultAdaptableTabBarPlacement(AdaptableTabBarPlacement) -> some View` — [View.defaultAdaptableTabBarPlacement](/documentation/swiftui/view/defaultadaptabletabbarplacement(_:))
- `func tabViewSidebarHeader(content:) -> some View` — [View.tabViewSidebarHeader](/documentation/swiftui/view/tabviewsidebarheader(content:))
- `func tabViewSidebarFooter(content:) -> some View` — [View.tabViewSidebarFooter](/documentation/swiftui/view/tabviewsidebarfooter(content:))
- `func tabViewSidebarBottomBar(content:) -> some View` — [View.tabViewSidebarBottomBar](/documentation/swiftui/view/tabviewsidebarbottombar(content:))
- [AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement) — values: automatic, sidebar, tabBar
- `var tabBarPlacement: TabBarPlacement?` — [EnvironmentValues.tabBarPlacement](/documentation/swiftui/environmentvalues/tabbarplacement)
- [TabBarPlacement](/documentation/swiftui/tabbarplacement) — values: bottomBar, ornament, pageIndicator, sidebar, topBar
- `var isTabBarShowingSections: Bool` — [EnvironmentValues.isTabBarShowingSections](/documentation/swiftui/environmentvalues/istabbarshowingsections)
- [TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior) — values: automatic, never, onScrollDown, onScrollUp
- [TabViewBottomAccessoryPlacement](/documentation/swiftui/tabviewbottomaccessoryplacement) — enum: expanded, inline

### Configuring a tab

- `func sectionActions(content:) -> some View` — [View.sectionActions](/documentation/swiftui/view/sectionactions(content:))
- [TabPlacement](/documentation/swiftui/tabplacement) — values: automatic, pinned, sidebarOnly
- [TabContentBuilder](/documentation/swiftui/tabcontentbuilder) — result builder for tab content
- [TabContent](/documentation/swiftui/tabcontent) — protocol for tab content; supports badge, customizationBehavior, contextMenu, drag/drop, swipeActions, tabPlacement
- [AnyTabContent](/documentation/swiftui/anytabcontent) — type-erased tab content

### Enabling tab customization

- `func tabViewCustomization(Binding<TabViewCustomization>?) -> some View` — [View.tabViewCustomization](/documentation/swiftui/view/tabviewcustomization(_:))
- [TabViewCustomization](/documentation/swiftui/tabviewcustomization) — stores tab/section order and visibility; includes SectionCustomization, TabCustomization
- [TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior) — values: automatic, disabled, reorderable

### Displaying views in multiple panes

- [HSplitView](/documentation/swiftui/hsplitview) — horizontal split view (macOS)
- [VSplitView](/documentation/swiftui/vsplitview) — vertical split view (macOS)

### Deprecated types

- [NavigationView](/documentation/swiftui/navigationview) [deprecated — prefer NavigationStack or NavigationSplitView]
- [NavigationViewStyle](/documentation/swiftui/navigationviewstyle) [deprecated] — styles: automatic, columns, stack
  - Supporting types: DefaultNavigationViewStyle, ColumnNavigationViewStyle, StackNavigationViewStyle, DoubleColumnNavigationViewStyle
- `func tabItem<V>(() -> V) -> some View` — [View.tabItem](/documentation/swiftui/view/tabitem(_:)) [legacy — prefer Tab]

---

## Modal presentations

- [Modal presentations](/documentation/swiftui/modal-presentations) (article)

### Configuring a dialog

- [DialogSeverity](/documentation/swiftui/dialogseverity) — values: automatic, standard, critical

### Showing a sheet, cover, or popover

- `func sheet(isPresented:onDismiss:content:) -> some View` — [View.sheet(isPresented:...)](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:))
- `func sheet(item:onDismiss:content:) -> some View` — [View.sheet(item:...)](/documentation/swiftui/view/sheet(item:ondismiss:content:))
- `func fullScreenCover(isPresented:onDismiss:content:) -> some View` — [View.fullScreenCover(isPresented:...)](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:))
- `func fullScreenCover(item:onDismiss:content:) -> some View` — [View.fullScreenCover(item:...)](/documentation/swiftui/view/fullscreencover(item:ondismiss:content:))
- `func popover(item:attachmentAnchor:arrowEdge:content:) -> some View` — [View.popover(item:...)](/documentation/swiftui/view/popover(item:attachmentanchor:arrowedge:content:))
- `func popover(isPresented:attachmentAnchor:arrowEdge:content:) -> some View` — [View.popover(isPresented:...)](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:))
- [PopoverAttachmentAnchor](/documentation/swiftui/popoverattachmentanchor) — cases: point(UnitPoint), rect(Anchor<CGRect>.Source)

### Adapting a presentation size

- `func presentationCompactAdaptation(horizontal:vertical:) -> some View` — [View.presentationCompactAdaptation(horizontal:vertical:)](/documentation/swiftui/view/presentationcompactadaptation(horizontal:vertical:))
- `func presentationCompactAdaptation(_:) -> some View` — [View.presentationCompactAdaptation](/documentation/swiftui/view/presentationcompactadaptation(_:))
- [PresentationAdaptation](/documentation/swiftui/presentationadaptation) — values: automatic, none, fullScreenCover, popover, sheet
- `func presentationSizing(some PresentationSizing) -> some View` — [View.presentationSizing](/documentation/swiftui/view/presentationsizing(_:))
- [PresentationSizing](/documentation/swiftui/presentationsizing) — protocol; values: automatic, fitted, form, page; methods: fitted(horizontal:vertical:), sticky(horizontal:vertical:)
  - Supporting types: AutomaticPresentationSizing, FittedPresentationSizing, FormPresentationSizing, PagePresentationSizing
- [PresentationSizingRoot](/documentation/swiftui/presentationsizingroot) — layout root for presentation sizing
- [PresentationSizingContext](/documentation/swiftui/presentationsizingcontext) — context for sizing calculations

### Configuring a sheet's height

- `func presentationDetents(Set<PresentationDetent>) -> some View` — [View.presentationDetents](/documentation/swiftui/view/presentationdetents(_:))
- `func presentationDetents(_:selection:) -> some View` — [View.presentationDetents(_:selection:)](/documentation/swiftui/view/presentationdetents(_:selection:))
- `func presentationContentInteraction(_:) -> some View` — [View.presentationContentInteraction](/documentation/swiftui/view/presentationcontentinteraction(_:))
- `func presentationDragIndicator(Visibility) -> some View` — [View.presentationDragIndicator](/documentation/swiftui/view/presentationdragindicator(_:))
- [PresentationDetent](/documentation/swiftui/presentationdetent) — values: large, medium; custom via fraction(_:), height(_:), custom(_:)
- [CustomPresentationDetent](/documentation/swiftui/custompresentationdetent) — protocol for custom detent height
- [PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction) — values: automatic, resizes, scrolls

### Styling a sheet and its background

- `func presentationCornerRadius(CGFloat?) -> some View` — [View.presentationCornerRadius](/documentation/swiftui/view/presentationcornerradius(_:))
- `func presentationBackground(_:) -> some View` — [View.presentationBackground](/documentation/swiftui/view/presentationbackground(_:))
- `func presentationBackground(alignment:content:) -> some View` — [View.presentationBackground(alignment:content:)](/documentation/swiftui/view/presentationbackground(alignment:content:))
- `func presentationBackgroundInteraction(_:) -> some View` — [View.presentationBackgroundInteraction](/documentation/swiftui/view/presentationbackgroundinteraction(_:))
- [PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction) — values: automatic, disabled, enabled, enabled(upThrough:)

### Presenting an alert

- [AlertScene](/documentation/swiftui/alertscene) — macOS alert as a scene
- `func alert(_:isPresented:actions:) -> some View` — [View.alert](/documentation/swiftui/view/alert(_:ispresented:actions:)) — multiple variants with presenting, error, message
- `func alert(isPresented:error:actions:) -> some View` — [View.alert(isPresented:error:...)](/documentation/swiftui/view/alert(ispresented:error:actions:))
- `func alert(_:isPresented:actions:message:)` — [View.alert(_:isPresented:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:actions:message:))

### Getting confirmation for an action

- `func confirmationDialog(_:isPresented:titleVisibility:actions:)` — [View.confirmationDialog](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:))
- `func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:)` — [View.confirmationDialog(presenting:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:))
- `func dismissalConfirmationDialog(_:shouldPresent:actions:)` — [View.dismissalConfirmationDialog](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:))

### Showing a confirmation dialog with a message

- `func confirmationDialog(_:isPresented:titleVisibility:actions:message:)` — [View.confirmationDialog(message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:message:))
- `func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:message:)` — [View.confirmationDialog(presenting:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:message:))
- `func dismissalConfirmationDialog(_:shouldPresent:actions:message:)` — [View.dismissalConfirmationDialog(message:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:message:))

### Configuring a dialog (view/scene modifiers)

- `func dialogIcon(Image?) -> some View` — [View.dialogIcon](/documentation/swiftui/view/dialogicon(_:))
- `func dialogIcon(Image?) -> some Scene` — [Scene.dialogIcon](/documentation/swiftui/scene/dialogicon(_:))
- `func dialogSeverity(DialogSeverity) -> some View` — [View.dialogSeverity](/documentation/swiftui/view/dialogseverity(_:))
- `func dialogSeverity(DialogSeverity) -> some Scene` — [Scene.dialogSeverity](/documentation/swiftui/scene/dialogseverity(_:))
- `func dialogSuppressionToggle(isSuppressed:) -> some View` — [View.dialogSuppressionToggle](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:))
- `func dialogSuppressionToggle(_:isSuppressed:)` — [View.dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/view/dialogsuppressiontoggle(_:issuppressed:))

### Exporting to file

- `func fileExporter(isPresented:document:contentType:defaultFilename:onCompletion:)` — [View.fileExporter](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:))
- `func fileExporter(isPresented:documents:contentType:onCompletion:)` — [View.fileExporter(documents:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttype:oncompletion:))
- `func fileExporter(isPresented:document:contentTypes:defaultFilename:onCompletion:onCancellation:)` — [View.fileExporter(contentTypes:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttypes:defaultfilename:oncompletion:oncancellation:))
- `func fileExporter(isPresented:documents:contentTypes:onCompletion:onCancellation:)` — [View.fileExporter(documents:contentTypes:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttypes:oncompletion:oncancellation:))
- `func fileExporter(isPresented:item:contentTypes:defaultFilename:onCompletion:onCancellation:)` — [View.fileExporter(item:)](/documentation/swiftui/view/fileexporter(ispresented:item:contenttypes:defaultfilename:oncompletion:oncancellation:))
- `func fileExporter(isPresented:items:contentTypes:onCompletion:onCancellation:)` — [View.fileExporter(items:)](/documentation/swiftui/view/fileexporter(ispresented:items:contenttypes:oncompletion:oncancellation:))
- `func fileExporterFilenameLabel(_:)` — [View.fileExporterFilenameLabel](/documentation/swiftui/view/fileexporterfilenamelabel(_:))

### Importing from file

- `func fileImporter(isPresented:allowedContentTypes:allowsMultipleSelection:onCompletion:)` — [View.fileImporter](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:))
- `func fileImporter(isPresented:allowedContentTypes:onCompletion:)` — [View.fileImporter(single)](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:))
- `func fileImporter(isPresented:allowedContentTypes:allowsMultipleSelection:onCompletion:onCancellation:)` — [View.fileImporter(onCancellation:)](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:oncancellation:))

### Moving a file

- `func fileMover(isPresented:file:onCompletion:)` — [View.fileMover](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:))
- `func fileMover(isPresented:files:onCompletion:)` — [View.fileMover(files:)](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:))
- `func fileMover(isPresented:file:onCompletion:onCancellation:)` — [View.fileMover(onCancellation:)](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:oncancellation:))
- `func fileMover(isPresented:files:onCompletion:onCancellation:)` — [View.fileMover(files:onCancellation:)](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:oncancellation:))

### Configuring a file dialog

- `func fileDialogBrowserOptions(FileDialogBrowserOptions) -> some View` — [View.fileDialogBrowserOptions](/documentation/swiftui/view/filedialogbrowseroptions(_:))
- `func fileDialogConfirmationLabel(_:)` — [View.fileDialogConfirmationLabel](/documentation/swiftui/view/filedialogconfirmationlabel(_:))
- `func fileDialogCustomizationID(String) -> some View` — [View.fileDialogCustomizationID](/documentation/swiftui/view/filedialogcustomizationid(_:))
- `func fileDialogDefaultDirectory(URL?) -> some View` — [View.fileDialogDefaultDirectory](/documentation/swiftui/view/filedialogdefaultdirectory(_:))
- `func fileDialogImportsUnresolvedAliases(Bool) -> some View` — [View.fileDialogImportsUnresolvedAliases](/documentation/swiftui/view/filedialogimportsunresolvedaliases(_:))
- `func fileDialogMessage(_:)` — [View.fileDialogMessage](/documentation/swiftui/view/filedialogmessage(_:))
- `func fileDialogURLEnabled(Predicate<URL>) -> some View` — [View.fileDialogURLEnabled](/documentation/swiftui/view/filedialogurlenabled(_:))
- [FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions) — values: displayFileExtensions, enumeratePackages, includeHiddenFiles

### Presenting an inspector

- `func inspector(isPresented:content:) -> some View` — [View.inspector](/documentation/swiftui/view/inspector(ispresented:content:))
- `func inspectorColumnWidth(CGFloat) -> some View` — [View.inspectorColumnWidth](/documentation/swiftui/view/inspectorcolumnwidth(_:))
- `func inspectorColumnWidth(min:ideal:max:) -> some View` — [View.inspectorColumnWidth(min:ideal:max:)](/documentation/swiftui/view/inspectorcolumnwidth(min:ideal:max:))

### Dismissing a presentation

- `var isPresented: Bool` — [EnvironmentValues.isPresented](/documentation/swiftui/environmentvalues/ispresented)
- `var dismiss: DismissAction` — [EnvironmentValues.dismiss](/documentation/swiftui/environmentvalues/dismiss)
- [DismissAction](/documentation/swiftui/dismissaction) — callable action
- `func interactiveDismissDisabled(Bool) -> some View` — [View.interactiveDismissDisabled](/documentation/swiftui/view/interactivedismissdisabled(_:))

### Deprecated modal presentations

- [Alert](/documentation/swiftui/alert) [deprecated — prefer alert(_:isPresented:actions:)]
- [ActionSheet](/documentation/swiftui/actionsheet) [deprecated — prefer confirmationDialog]

---

## Toolbars

- [Toolbars](/documentation/swiftui/toolbars) (article)

### Populating a toolbar

- `func toolbar(content:)` — [View.toolbar(content:)](/documentation/swiftui/view/toolbar(content:))
- [ToolbarItem](/documentation/swiftui/toolbaritem) — single toolbar item with placement
- [ToolbarItemGroup](/documentation/swiftui/toolbaritemgroup) — group of toolbar items with placement and optional label
- [LabeledToolbarItemGroupContent](/documentation/swiftui/labeledtoolbaritemgroupcontent) — labeled content for toolbar groups
- [ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement) — semantic: automatic, principal, status; actions: primaryAction, secondaryAction, confirmationAction, cancellationAction, destructiveAction, navigation; explicit: topBarLeading, topBarTrailing, bottomBar, bottomOrnament, keyboard, accessoryBar(id:); titles: largeSubtitle, largeTitle, subtitle, title
  - Deprecated: init(id:), navigationBarLeading, navigationBarTrailing [deprecated]
- [ToolbarContent](/documentation/swiftui/toolbarcontent) — protocol for toolbar content; methods: hidden(_:), matchedTransitionSource, sharedBackgroundVisibility
- [ToolbarContentBuilder](/documentation/swiftui/toolbarcontentbuilder) — result builder for toolbar content
- [ToolbarSpacer](/documentation/swiftui/toolbarspacer) — spacer in toolbar with sizing and placement
- [DefaultToolbarItem](/documentation/swiftui/defaulttoolbaritem) — default toolbar item by kind and placement

### Populating a customizable toolbar

- `func toolbar(id:content:) -> some View` — [View.toolbar(id:content:)](/documentation/swiftui/view/toolbar(id:content:))
- [CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent) — protocol for customizable toolbar; defaultCustomization, customizationBehavior
- [ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior) — values: default, disabled, reorderable
- [ToolbarCustomizationOptions](/documentation/swiftui/toolbarcustomizationoptions) — values: alwaysAvailable
- [SearchToolbarBehavior](/documentation/swiftui/searchtoolbarbehavior) — values: automatic, minimize

### Removing default items

- `func toolbar(removing:) -> some View` — [View.toolbar(removing:)](/documentation/swiftui/view/toolbar(removing:))
- [ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind) — values: sidebarToggle, search, title

### Setting toolbar visibility

- `func toolbar(Visibility, for: ToolbarPlacement...) -> some View` — [View.toolbar(_:for:)](/documentation/swiftui/view/toolbar(_:for:))
- `func toolbarVisibility(Visibility, for: ToolbarPlacement...) -> some View` — [View.toolbarVisibility](/documentation/swiftui/view/toolbarvisibility(_:for:))
- `func toolbarBackgroundVisibility(Visibility, for: ToolbarPlacement...) -> some View` — [View.toolbarBackgroundVisibility](/documentation/swiftui/view/toolbarbackgroundvisibility(_:for:))
- [ToolbarPlacement](/documentation/swiftui/toolbarplacement) — values: automatic, accessoryBar(id:), bottomBar, bottomOrnament, navigationBar, tabBar, windowToolbar
  - Deprecated: init(id:) [deprecated]
- [ContentToolbarPlacement](/documentation/swiftui/contenttoolbarplacement) — values: tabViewSidebar

### Specifying the role of toolbar content

- `func toolbarRole(ToolbarRole) -> some View` — [View.toolbarRole](/documentation/swiftui/view/toolbarrole(_:))
- [ToolbarRole](/documentation/swiftui/toolbarrole) — values: automatic, browser, editor, navigationStack

### Styling a toolbar

- `func toolbarBackground(_:for:)` — [View.toolbarBackground](/documentation/swiftui/view/toolbarbackground(_:for:))
- `func toolbarColorScheme(ColorScheme?, for: ToolbarPlacement...) -> some View` — [View.toolbarColorScheme](/documentation/swiftui/view/toolbarcolorscheme(_:for:))
- `func toolbarForegroundStyle<S>(S, for: ToolbarPlacement...) -> some View` — [View.toolbarForegroundStyle](/documentation/swiftui/view/toolbarforegroundstyle(_:for:))
- `var toolbarLabelStyle: ToolbarLabelStyle?` — [EnvironmentValues.toolbarLabelStyle](/documentation/swiftui/environmentvalues/toolbarlabelstyle)
- [ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle) — values: automatic, iconOnly, titleAndIcon, titleOnly
- [SpacerSizing](/documentation/swiftui/spacersizing) — values: fixed, flexible

### Configuring the toolbar title display mode

- `func toolbarTitleDisplayMode(ToolbarTitleDisplayMode) -> some View` — [View.toolbarTitleDisplayMode](/documentation/swiftui/view/toolbartitledisplaymode(_:))
- [ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode) — values: automatic, inline, inlineLarge, large

### Setting the toolbar title menu

- `func toolbarTitleMenu(content:) -> some View` — [View.toolbarTitleMenu](/documentation/swiftui/view/toolbartitlemenu(content:))
- [ToolbarTitleMenu](/documentation/swiftui/toolbartitlemenu) — toolbar title menu with optional custom content

### Creating an ornament

- `func ornament(visibility:attachmentAnchor:contentAlignment:ornament:)` — [View.ornament](/documentation/swiftui/view/ornament(visibility:attachmentanchor:contentalignment:ornament:))
- [OrnamentAttachmentAnchor](/documentation/swiftui/ornamentattachmentanchor) — anchors: scene(_:), parent(_:)

---

## Search

- [Search](/documentation/swiftui/search) (article)

### Searching your app's data model

- [Adding a search interface to your app](/documentation/swiftui/adding-a-search-interface-to-your-app) (article)
- [Performing a search operation](/documentation/swiftui/performing-a-search-operation) (article)
- `func searchable(text:placement:prompt:)` — [View.searchable](/documentation/swiftui/view/searchable(text:placement:prompt:))
- `func searchable(text:tokens:placement:prompt:token:)` — [View.searchable(tokens:)](/documentation/swiftui/view/searchable(text:tokens:placement:prompt:token:))
- `func searchable(text:editableTokens:placement:prompt:token:)` — [View.searchable(editableTokens:)](/documentation/swiftui/view/searchable(text:editabletokens:placement:prompt:token:))
- [SearchFieldPlacement](/documentation/swiftui/searchfieldplacement) — values: automatic, navigationBarDrawer, navigationBarDrawer(displayMode:), sidebar, toolbar, toolbarPrincipal

### Making search suggestions

- [Suggesting search terms](/documentation/swiftui/suggesting-search-terms) (article)
- `func searchSuggestions(() -> S) -> some View` — [View.searchSuggestions](/documentation/swiftui/view/searchsuggestions(_:))
- `func searchSuggestions(Visibility, for: SearchSuggestionsPlacement.Set) -> some View` — [View.searchSuggestions(_:for:)](/documentation/swiftui/view/searchsuggestions(_:for:))
- `func searchCompletion(_:)` — [View.searchCompletion](/documentation/swiftui/view/searchcompletion(_:))
- `func searchable(text:tokens:suggestedTokens:placement:prompt:token:)` — [View.searchable(suggestedTokens:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:placement:prompt:token:))
- [SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement) — values: automatic, content, menu; Set with rawValue

### Limiting search scope

- [Scoping a search operation](/documentation/swiftui/scoping-a-search-operation) (article)
- `func searchScopes(_:scopes:) -> some View` — [View.searchScopes](/documentation/swiftui/view/searchscopes(_:scopes:))
- `func searchScopes(_:activation:_:) -> some View` — [View.searchScopes(activation:)](/documentation/swiftui/view/searchscopes(_:activation:_:))
- [SearchScopeActivation](/documentation/swiftui/searchscopeactivation) — values: automatic, onSearchPresentation, onTextEntry

### Detecting, activating, and dismissing search

- [Managing search interface activation](/documentation/swiftui/managing-search-interface-activation) (article)
- `var isSearching: Bool` — [EnvironmentValues.isSearching](/documentation/swiftui/environmentvalues/issearching)
- `var dismissSearch: DismissSearchAction` — [EnvironmentValues.dismissSearch](/documentation/swiftui/environmentvalues/dismisssearch)
- [DismissSearchAction](/documentation/swiftui/dismisssearchaction) — callable action
- `func searchable(text:isPresented:placement:prompt:)` — [View.searchable(isPresented:)](/documentation/swiftui/view/searchable(text:ispresented:placement:prompt:))
- `func searchable(text:tokens:isPresented:placement:prompt:token:)` — [View.searchable(tokens:isPresented:)](/documentation/swiftui/view/searchable(text:tokens:ispresented:placement:prompt:token:))
- `func searchable(text:editableTokens:isPresented:placement:prompt:token:)` — [View.searchable(editableTokens:isPresented:)](/documentation/swiftui/view/searchable(text:editabletokens:ispresented:placement:prompt:token:))
- `func searchable(text:tokens:suggestedTokens:isPresented:placement:prompt:token:)` — [View.searchable(suggestedTokens:isPresented:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:ispresented:placement:prompt:token:))

### Displaying toolbar content during search

- `func searchPresentationToolbarBehavior(SearchPresentationToolbarBehavior) -> some View` — [View.searchPresentationToolbarBehavior](/documentation/swiftui/view/searchpresentationtoolbarbehavior(_:))
- [SearchPresentationToolbarBehavior](/documentation/swiftui/searchpresentationtoolbarbehavior) — values: automatic, avoidHidingContent

### Searching for text in a view

- `func findNavigator(isPresented:) -> some View` — [View.findNavigator](/documentation/swiftui/view/findnavigator(ispresented:))
- `func findDisabled(Bool) -> some View` — [View.findDisabled](/documentation/swiftui/view/finddisabled(_:))
- `func replaceDisabled(Bool) -> some View` — [View.replaceDisabled](/documentation/swiftui/view/replacedisabled(_:))
- [FindContext](/documentation/swiftui/findcontext) — isPresented, supportsReplace

---

## App extensions

- [App extensions](/documentation/swiftui/app-extensions) (article)

### Creating widgets

- [Building Widgets Using WidgetKit and SwiftUI](/documentation/widgetkit/building_widgets_using_widgetkit_and_swiftui) (article)
- [Creating a widget extension](/documentation/widgetkit/creating-a-widget-extension) (article)
- [Keeping a widget up to date](/documentation/widgetkit/keeping-a-widget-up-to-date) (article)
- [Making a configurable widget](/documentation/widgetkit/making-a-configurable-widget) (article)
- [Widget](/documentation/swiftui/widget) — protocol for widget entry point
- [WidgetBundle](/documentation/swiftui/widgetbundle) — groups multiple widgets
- [WidgetBundleBuilder](/documentation/swiftui/widgetbundlebuilder) — result builder for widget bundles
- [LimitedAvailabilityConfiguration](/documentation/swiftui/limitedavailabilityconfiguration) — availability-limited widget config
- [WidgetConfiguration](/documentation/swiftui/widgetconfiguration) — protocol; configurationDisplayName, description, supportedFamilies, contentMarginsDisabled, disfavoredLocations, containerBackgroundRemovable, backgroundTask, pushHandler, supplementalActivityFamilies, supportedMountingStyles, widgetTexture
- [EmptyWidgetConfiguration](/documentation/swiftui/emptywidgetconfiguration) — empty widget configuration

### Composing control widgets

- [ControlWidget](/documentation/swiftui/controlwidget) — protocol for Control Center widgets
- [ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration) — protocol; description, displayName, promptsForUserConfiguration, pushHandler
- [EmptyControlWidgetConfiguration](/documentation/swiftui/emptycontrolwidgetconfiguration) — empty control widget config
- [ControlWidgetConfigurationBuilder](/documentation/swiftui/controlwidgetconfigurationbuilder) — result builder
- [ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate) — protocol for control widget templates; disabled, privacySensitive, tint
- [EmptyControlWidgetTemplate](/documentation/swiftui/emptycontrolwidgettemplate) — empty template
- [ControlWidgetTemplateBuilder](/documentation/swiftui/controlwidgettemplatebuilder) — result builder
- `func controlWidgetActionHint(_:)` — [View.controlWidgetActionHint](/documentation/swiftui/view/controlwidgetactionhint(_:))
- `func controlWidgetStatus(_:)` — [View.controlWidgetStatus](/documentation/swiftui/view/controlwidgetstatus(_:))

### Labeling a widget

- `func widgetLabel(_:)` — [View.widgetLabel](/documentation/swiftui/view/widgetlabel(_:))
- `func widgetLabel(label:) -> some View` — [View.widgetLabel(label:)](/documentation/swiftui/view/widgetlabel(label:))

### Styling a widget group

- `func accessoryWidgetGroupStyle(AccessoryWidgetGroupStyle) -> some View` — [View.accessoryWidgetGroupStyle](/documentation/swiftui/view/accessorywidgetgroupstyle(_:))

### Controlling the accented group

- `func widgetAccentable(Bool) -> some View` — [View.widgetAccentable](/documentation/swiftui/view/widgetaccentable(_:))

### Managing placement in the Dynamic Island

- `func dynamicIsland(verticalPlacement:) -> some View` — [View.dynamicIsland](/documentation/swiftui/view/dynamicisland(verticalplacement:))
