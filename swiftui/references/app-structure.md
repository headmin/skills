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

- [App](/documentation/swiftui/app) — protocol for app entry point; provides body and main()
- Articles: [Destination Video](/documentation/visionos/destination-video), [Hello World](/documentation/visionos/world), [Backyard Birds](/documentation/swiftui/backyard-birds-sample), [Food Truck](/documentation/swiftui/food-truck-building-a-swiftui-multiplatform-app), [Fruta](/documentation/appclip/fruta-building-a-feature-rich-app-with-swiftui), [Migrating to SwiftUI life cycle](/documentation/swiftui/migrating-to-the-swiftui-life-cycle)

### Platform delegate adaptors

- [UIApplicationDelegateAdaptor](/documentation/swiftui/uiapplicationdelegateadaptor) — bridges UIApplicationDelegate (iOS/iPadOS)
- [UILaunchScreen](/documentation/bundleresources/information-property-list/uilaunchscreen), [UILaunchScreens](/documentation/bundleresources/information-property-list/uilaunchscreens) — Info.plist launch screen config
- [NSApplicationDelegateAdaptor](/documentation/swiftui/nsapplicationdelegateadaptor) — bridges NSApplicationDelegate (macOS)
- [WKApplicationDelegateAdaptor](/documentation/swiftui/wkapplicationdelegateadaptor), [WKExtensionDelegateAdaptor](/documentation/swiftui/wkextensiondelegateadaptor) — bridges WK delegates (watchOS)
- [Creating a tvOS media catalog app in SwiftUI](/documentation/swiftui/creating-a-tvos-media-catalog-app-in-swiftui) (article)

### Handling system recenter events

- [WorldRecenterPhase](/documentation/swiftui/worldrecenterphase) — enum: began, ended (visionOS)

---

## Scenes

- [Scenes](/documentation/swiftui/scenes) (article)
- [Scene](/documentation/swiftui/scene) — protocol; body, onChange, backgroundTask, commands, sizing, positioning, styling, environment, dialogs
- [SceneBuilder](/documentation/swiftui/scenebuilder) — result builder for composing scenes
- [ScenePhase](/documentation/swiftui/scenephase) — enum: active, inactive, background | env: `scenePhase`

### Managing a settings window

- [Settings](/documentation/swiftui/settings) — macOS settings scene
- [SettingsLink](/documentation/swiftui/settingslink), [DefaultSettingsLinkLabel](/documentation/swiftui/defaultsettingslinklabel) — button that opens settings
- [OpenSettingsAction](/documentation/swiftui/opensettingsaction) — callable action | env: `openSettings`

### Menu bar

- [Building and customizing the menu bar with SwiftUI](/documentation/swiftui/building-and-customizing-the-menu-bar-with-swiftui) (article)
- [MenuBarExtra](/documentation/swiftui/menubarextra) — macOS menu bar item scene
- [MenuBarExtraStyle](/documentation/swiftui/menubarextrastyle) — styles: automatic, menu, window | types: AutomaticMenuBarExtraStyle, PullDownMenuBarExtraStyle, WindowMenuBarExtraStyle

### Watch notifications

- [WKNotificationScene](/documentation/swiftui/wknotificationscene) — watchOS notification scene

---

## Windows

- Articles: [Windows](/documentation/swiftui/windows), [Customizing window styles (macOS)](/documentation/swiftui/customizing-window-styles-and-state-restoration-behavior-in-macos), [Multiple windows](/documentation/swiftui/bringing-multiple-windows-to-your-swiftui-app)

### Creating windows

- [WindowGroup](/documentation/swiftui/windowgroup) — primary multi-window scene; data-driven and identified variants
- [PresentedWindowContent](/documentation/swiftui/presentedwindowcontent) — content wrapper for presented windows
- [Window](/documentation/swiftui/window) — single-instance named window (macOS)
- [UtilityWindow](/documentation/swiftui/utilitywindow) — utility-panel-style window (macOS)
- [WindowStyle](/documentation/swiftui/windowstyle) — styles: automatic, hiddenTitleBar, plain, titleBar, volumetric | types: DefaultWindowStyle, HiddenTitleBarWindowStyle, PlainWindowStyle, TitleBarWindowStyle, VolumetricWindowStyle
- `func windowStyle<S>(S) -> some Scene` — [Scene.windowStyle](/documentation/swiftui/scene/windowstyle(_:))

### Styling the associated toolbar

- `func windowToolbarStyle<S>(S) -> some Scene` — [Scene.windowToolbarStyle](/documentation/swiftui/scene/windowtoolbarstyle(_:))
- `func windowToolbarLabelStyle` — [binding](/documentation/swiftui/scene/windowtoolbarlabelstyle(_:)) | [fixed](/documentation/swiftui/scene/windowtoolbarlabelstyle(fixed:))
- [WindowToolbarStyle](/documentation/swiftui/windowtoolbarstyle) — styles: automatic, expanded, unified, unified(showsTitle:), unifiedCompact, unifiedCompact(showsTitle:) | types: DefaultWindowToolbarStyle, ExpandedWindowToolbarStyle, UnifiedWindowToolbarStyle, UnifiedCompactWindowToolbarStyle

### Opening and closing windows

- [Presenting windows and spaces](/documentation/visionos/presenting-windows-and-spaces) (article)
- [OpenWindowAction](/documentation/swiftui/openwindowaction) — open by id/value; SharingBehavior | env: `openWindow`
- [PushWindowAction](/documentation/swiftui/pushwindowaction) — push a window (visionOS)
- env: `supportsMultipleWindows` — [EnvironmentValues](/documentation/swiftui/environmentvalues/supportsmultiplewindows)
- [DismissWindowAction](/documentation/swiftui/dismisswindowaction) — dismiss by id/value | env: `dismissWindow`
- [DismissAction](/documentation/swiftui/dismissaction) — dismiss current presentation | env: `dismiss`
- [DismissBehavior](/documentation/swiftui/dismissbehavior) — values: destructive, interactive

### Sizing and positioning a window

- [Positioning and sizing windows](/documentation/visionos/positioning-and-sizing-windows) (article)
- `func defaultSize(...)` — [Scene](/documentation/swiftui/scene/defaultsize(_:)) — 2D, 3D, UnitLength variants
- [WindowResizability](/documentation/swiftui/windowresizability) — values: automatic, contentMinSize, contentSize | `func windowResizability(...)` [Scene](/documentation/swiftui/scene/windowresizability(_:))
- [WindowIdealSize](/documentation/swiftui/windowidealsize) — values: automatic, fitToContent, maximum | `func windowIdealSize(...)` [Scene](/documentation/swiftui/scene/windowidealsize(_:))
- `func defaultPosition(UnitPoint)` — [Scene](/documentation/swiftui/scene/defaultposition(_:))
- [WindowLevel](/documentation/swiftui/windowlevel) — values: automatic, desktop, floating, normal | `func windowLevel(...)` [Scene](/documentation/swiftui/scene/windowlevel(_:))
- [WindowPlacement](/documentation/swiftui/windowplacement) — Position (above, below, leading, trailing, replacing, utilitypanel), size
- [WindowLayoutRoot](/documentation/swiftui/windowlayoutroot) — layout root | `func defaultWindowPlacement(...)` [Scene](/documentation/swiftui/scene/defaultwindowplacement(_:)) | `func windowIdealPlacement(...)` [Scene](/documentation/swiftui/scene/windowidealplacement(_:))
- [WindowPlacementContext](/documentation/swiftui/windowplacementcontext) — defaultDisplay, windows | [WindowProxy](/documentation/swiftui/windowproxy) — id, phase | [DisplayProxy](/documentation/swiftui/displayproxy) — bounds, safeAreaInsets, visibleRect

### Configuring window visibility

- [WindowVisibilityToggle](/documentation/swiftui/windowvisibilitytoggle), [DefaultWindowVisibilityToggleLabel](/documentation/swiftui/defaultwindowvisibilitytogglelabel) — toggle showing/hiding a window
- [SceneLaunchBehavior](/documentation/swiftui/scenelaunchbehavior) — values: automatic, presented, suppressed | `func defaultLaunchBehavior(...)` [Scene](/documentation/swiftui/scene/defaultlaunchbehavior(_:))
- [SceneRestorationBehavior](/documentation/swiftui/scenerestorationbehavior) — values: automatic, disabled | `func restorationBehavior(...)` [Scene](/documentation/swiftui/scene/restorationbehavior(_:))
- `func persistentSystemOverlays(Visibility) -> some Scene` — [Scene](/documentation/swiftui/scene/persistentsystemoverlays(_:))
- [WindowToolbarFullScreenVisibility](/documentation/swiftui/windowtoolbarfullscreenvisibility) — values: automatic, onHover, visible | `func windowToolbarFullScreenVisibility(...)` [View](/documentation/swiftui/view/windowtoolbarfullscreenvisibility(_:))

### Managing window behavior

- [WindowManagerRole](/documentation/swiftui/windowmanagerrole) — values: associated, automatic, principal | `func windowManagerRole(...)` [Scene](/documentation/swiftui/scene/windowmanagerrole(_:))
- [WindowInteractionBehavior](/documentation/swiftui/windowinteractionbehavior) — values: automatic, disabled, enabled
- View modifiers using WindowInteractionBehavior: [windowDismissBehavior](/documentation/swiftui/view/windowdismissbehavior(_:)), [windowFullScreenBehavior](/documentation/swiftui/view/windowfullscreenbehavior(_:)), [windowMinimizeBehavior](/documentation/swiftui/view/windowminimizebehavior(_:)), [windowResizeBehavior](/documentation/swiftui/view/windowresizebehavior(_:))
- `func windowBackgroundDragBehavior(WindowInteractionBehavior) -> some Scene` — [Scene](/documentation/swiftui/scene/windowbackgrounddragbehavior(_:))

### Interacting with volumes

- `func onVolumeViewpointChange(updateStrategy:initial:_:)` — [View](/documentation/swiftui/view/onvolumeviewpointchange(updatestrategy:initial:_:)) | `func supportedVolumeViewpoints(...)` — [View](/documentation/swiftui/view/supportedvolumeviewpoints(_:))
- [VolumeViewpointUpdateStrategy](/documentation/swiftui/volumeviewpointupdatestrategy) — values: all, supported
- [Viewpoint3D](/documentation/swiftui/viewpoint3d) — 3D viewpoint; standard, squareAzimuth
- [SquareAzimuth](/documentation/swiftui/squareazimuth) — enum: front, back, left, right; [SquareAzimuth.Set](/documentation/swiftui/squareazimuth/set)
- [WorldAlignmentBehavior](/documentation/swiftui/worldalignmentbehavior) — values: adaptive, automatic, gravityAligned | `func volumeWorldAlignment(...)` [Scene](/documentation/swiftui/scene/volumeworldalignment(_:))
- [WorldScalingBehavior](/documentation/swiftui/worldscalingbehavior) — values: automatic, dynamic | `func defaultWorldScaling(...)` [Scene](/documentation/swiftui/scene/defaultworldscaling(_:))
- [WorldScalingCompensation](/documentation/swiftui/worldscalingcompensation) — values: scaled, unscaled
- [WorldTrackingLimitation](/documentation/swiftui/worldtrackinglimitation) — values: orientation, translation | env: `worldTrackingLimitations`
- [SurfaceSnappingInfo](/documentation/swiftui/surfacesnappinginfo) — classification, isSnapped, AuthorizationStatus

### Deprecated types

- [ControlActiveState](/documentation/swiftui/controlactivestate) [deprecated] — enum: key, active, inactive

---

## Immersive spaces

- [Immersive spaces](/documentation/swiftui/immersive-spaces) (article)

### Creating an immersive space

- [ImmersiveSpace](/documentation/swiftui/immersivespace) — visionOS immersive space; data-driven, identified, foveated streaming variants
- [ImmersiveSpaceViewContent](/documentation/swiftui/immersivespaceviewcontent), [ImmersiveSpaceContent](/documentation/swiftui/immersivespacecontent), [ImmersiveSpaceContentBuilder](/documentation/swiftui/immersivespacecontentbuilder) — content types and builder
- [ImmersionStyle](/documentation/swiftui/immersionstyle) — styles: automatic, full, mixed, progressive | types: AutomaticImmersionStyle, FullImmersionStyle, MixedImmersionStyle, ProgressiveImmersionStyle | progressive(_:initialAmount:), progressive(aspectRatio:)
- `func immersionStyle(selection:in:) -> some Scene` — [Scene](/documentation/swiftui/scene/immersionstyle(selection:in:))
- [ImmersiveEnvironmentBehavior](/documentation/swiftui/immersiveenvironmentbehavior) — values: automatic, coexist, replace
- [ProgressiveImmersionAspectRatio](/documentation/swiftui/progressiveimmersionaspectratio) — values: automatic, landscape, portrait
- env: `immersiveSpaceDisplacement: Pose3D` — [EnvironmentValues](/documentation/swiftui/environmentvalues/immersivespacedisplacement)

### Opening an immersive space

- [OpenImmersiveSpaceAction](/documentation/swiftui/openimmersivespaceaction) — async callable; Result: opened, userCancelled, error | env: `openImmersiveSpace`

### Closing the immersive space

- [DismissImmersiveSpaceAction](/documentation/swiftui/dismissimmersivespaceaction) — async callable | env: `dismissImmersiveSpace`

### Hiding upper limbs during immersion

- `func upperLimbVisibility(Visibility)` — [Scene](/documentation/swiftui/scene/upperlimbvisibility(_:)) | [View](/documentation/swiftui/view/upperlimbvisibility(_:))

### Adjusting content brightness

- [ImmersiveContentBrightness](/documentation/swiftui/immersivecontentbrightness) — values: automatic, dark, dim, bright, custom(Double) | `func immersiveContentBrightness(...)` [Scene](/documentation/swiftui/scene/immersivecontentbrightness(_:))

### Responding to immersion changes

- `func onImmersionChange(initial:_:)` — [View](/documentation/swiftui/view/onimmersionchange(initial:_:))
- [ImmersionChangeContext](/documentation/swiftui/immersionchangecontext) — amount property

### Adding menu items to an immersive space

- `func immersiveEnvironmentPicker(content:)` — [View](/documentation/swiftui/view/immersiveenvironmentpicker(content:))

### Handling remote immersive spaces

- [RemoteImmersiveSpace](/documentation/swiftui/remoteimmersivespace) — remote immersive space (visionOS)
- [RemoteDeviceIdentifier](/documentation/swiftui/remotedeviceidentifier) — remote device id

---

## Documents

- Articles: [Documents](/documentation/swiftui/documents), [Building a document-based app with SwiftUI](/documentation/swiftui/building-a-document-based-app-with-swiftui), [Building a document-based app using SwiftData](/documentation/swiftui/building-a-document-based-app-using-swiftdata)
- [DocumentGroup](/documentation/swiftui/documentgroup) — scene for document-based apps; FileDocument, ReferenceFileDocument, SwiftData

### Storing document data

- [FileDocument](/documentation/swiftui/filedocument) — value-type documents (struct) | [FileDocumentConfiguration](/documentation/swiftui/filedocumentconfiguration) — binding, fileURL, isEditable
- [ReferenceFileDocument](/documentation/swiftui/referencefiledocument) — reference-type documents (class) | [ReferenceFileDocumentConfiguration](/documentation/swiftui/referencefiledocumentconfiguration) — document, fileURL, isEditable, undoManager
- [DocumentConfiguration](/documentation/swiftui/documentconfiguration) — fileURL, isEditable | env: `documentConfiguration`
- [FileDocumentReadConfiguration](/documentation/swiftui/filedocumentreadconfiguration) — contentType, file | [FileDocumentWriteConfiguration](/documentation/swiftui/filedocumentwriteconfiguration) — contentType, existingFile

### Opening a document programmatically

- [NewDocumentAction](/documentation/swiftui/newdocumentaction) — create new documents | env: `newDocument`
- [OpenDocumentAction](/documentation/swiftui/opendocumentaction) — async open at URL | env: `openDocument`

### Document launch experience

- [DocumentGroupLaunchScene](/documentation/swiftui/documentgrouplaunchscene) — customizable launch scene
- [DocumentLaunchView](/documentation/swiftui/documentlaunchview) — launch view | [DocumentLaunchGeometryProxy](/documentation/swiftui/documentlaunchgeometryproxy) — frame, titleViewFrame
- [DefaultDocumentGroupLaunchActions](/documentation/swiftui/defaultdocumentgrouplaunchactions), [NewDocumentButton](/documentation/swiftui/newdocumentbutton), [DocumentBaseBox](/documentation/swiftui/documentbasebox)

### Renaming a document

- [RenameButton](/documentation/swiftui/renamebutton) — triggers rename | [RenameAction](/documentation/swiftui/renameaction) — callable | env: `rename`
- `func renameAction(_:)` — [View](/documentation/swiftui/view/renameaction(_:))

---

## Navigation

- Articles: [Navigation](/documentation/swiftui/navigation), [Understanding the navigation stack](/documentation/swiftui/understanding-the-navigation-stack), [Robust navigation structure](/documentation/swiftui/bringing-robust-navigation-structure-to-your-swiftui-app), [Migrating to new navigation types](/documentation/swiftui/migrating-to-new-navigation-types)

### Presenting views in columns
- [NavigationSplitView](/documentation/swiftui/navigationsplitview) — two/three-column navigation; column visibility, preferred compact column
- `func navigationSplitViewStyle<S>(S)` — [View](/documentation/swiftui/view/navigationsplitviewstyle(_:))
- `func navigationSplitViewColumnWidth` — [fixed](/documentation/swiftui/view/navigationsplitviewcolumnwidth(_:)) | [min:ideal:max:](/documentation/swiftui/view/navigationsplitviewcolumnwidth(min:ideal:max:))
- [NavigationSplitViewVisibility](/documentation/swiftui/navigationsplitviewvisibility) — values: automatic, all, doubleColumn, detailOnly
- [NavigationSplitViewColumn](/documentation/swiftui/navigationsplitviewcolumn) — values: sidebar, content, detail
- [NavigationLink](/documentation/swiftui/navigationlink) — push destination or present value | [deprecated variants](/documentation/swiftui/navigationlink-deprecated) [deprecated]

### Stacking views in one column

- [NavigationStack](/documentation/swiftui/navigationstack) — stack-based navigation with optional path binding
- [NavigationPath](/documentation/swiftui/navigationpath) — type-erased path; append, removeLast, CodableRepresentation
- `func navigationDestination` — [for:destination:](/documentation/swiftui/view/navigationdestination(for:destination:)) | [isPresented:](/documentation/swiftui/view/navigationdestination(ispresented:destination:)) | [item:](/documentation/swiftui/view/navigationdestination(item:destination:))

### Setting titles for navigation content

- `func navigationTitle(_:)` — [View](/documentation/swiftui/view/navigationtitle(_:)) | `func navigationSubtitle(_:)` — [View](/documentation/swiftui/view/navigationsubtitle(_:))
- `func navigationDocument` — [basic](/documentation/swiftui/view/navigationdocument(_:)) | [preview](/documentation/swiftui/view/navigationdocument(_:preview:))

### Configuring the navigation bar

- `func navigationBarBackButtonHidden(Bool)` — [View](/documentation/swiftui/view/navigationbarbackbuttonhidden(_:))
- `func navigationBarTitleDisplayMode(...)` — [View](/documentation/swiftui/view/navigationbartitledisplaymode(_:))
- [NavigationBarItem](/documentation/swiftui/navigationbaritem) — TitleDisplayMode: automatic, inline, large

### Configuring the sidebar

- [SidebarRowSize](/documentation/swiftui/sidebarrowsize) — enum: small, medium, large | env: `sidebarRowSize`

### Presenting views in tabs

- [Enhancing your app's content with tab navigation](/documentation/swiftui/enhancing-your-app-content-with-tab-navigation) (article)
- [TabView](/documentation/swiftui/tabview) — tabbed container; selection binding | `func tabViewStyle<S>(S)` [View](/documentation/swiftui/view/tabviewstyle(_:))
- [Tab](/documentation/swiftui/tab) — individual tab; label, systemImage, image, role variants | [TabSection](/documentation/swiftui/tabsection) — groups tabs
- [TabRole](/documentation/swiftui/tabrole) — search | [DefaultTabLabel](/documentation/swiftui/defaulttablabel) | [TabSearchActivation](/documentation/swiftui/tabsearchactivation) — automatic, searchTabSelection
- `func defaultAdaptableTabBarPlacement(...)` — [View](/documentation/swiftui/view/defaultadaptabletabbarplacement(_:)) | sidebar: [header](/documentation/swiftui/view/tabviewsidebarheader(content:)), [footer](/documentation/swiftui/view/tabviewsidebarfooter(content:)), [bottomBar](/documentation/swiftui/view/tabviewsidebarbottombar(content:))
- [AdaptableTabBarPlacement](/documentation/swiftui/adaptabletabbarplacement) — automatic, sidebar, tabBar | [TabBarPlacement](/documentation/swiftui/tabbarplacement) — bottomBar, ornament, pageIndicator, sidebar, topBar | env: `tabBarPlacement`
- [TabBarMinimizeBehavior](/documentation/swiftui/tabbarminimizebehavior) — automatic, never, onScrollDown, onScrollUp | [TabViewBottomAccessoryPlacement](/documentation/swiftui/tabviewbottomaccessoryplacement) — expanded, inline
- `func sectionActions(content:)` — [View](/documentation/swiftui/view/sectionactions(content:)) | [TabPlacement](/documentation/swiftui/tabplacement) — automatic, pinned, sidebarOnly
- [TabContentBuilder](/documentation/swiftui/tabcontentbuilder) — result builder | [TabContent](/documentation/swiftui/tabcontent) — protocol; badge, customization, contextMenu, drag/drop, swipeActions | [AnyTabContent](/documentation/swiftui/anytabcontent)
- `func tabViewCustomization(...)` — [View](/documentation/swiftui/view/tabviewcustomization(_:)) | [TabViewCustomization](/documentation/swiftui/tabviewcustomization) — order/visibility; SectionCustomization, TabCustomization
- [TabCustomizationBehavior](/documentation/swiftui/tabcustomizationbehavior) — automatic, disabled, reorderable | env: `isTabBarShowingSections`

### Displaying views in multiple panes

- [HSplitView](/documentation/swiftui/hsplitview) — horizontal split (macOS) | [VSplitView](/documentation/swiftui/vsplitview) — vertical split (macOS)

### Deprecated types

- [NavigationView](/documentation/swiftui/navigationview) [deprecated -- prefer NavigationStack/NavigationSplitView]
- [NavigationViewStyle](/documentation/swiftui/navigationviewstyle) [deprecated] — automatic, columns, stack | types: DefaultNavigationViewStyle, ColumnNavigationViewStyle, StackNavigationViewStyle, DoubleColumnNavigationViewStyle
- `func tabItem(...)` — [View](/documentation/swiftui/view/tabitem(_:)) [legacy -- prefer Tab]

---

## Modal presentations

- [Modal presentations](/documentation/swiftui/modal-presentations) (article)
- [DialogSeverity](/documentation/swiftui/dialogseverity) — values: automatic, standard, critical

### Showing a sheet, cover, or popover

- `func sheet` — [isPresented:](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:)) | [item:](/documentation/swiftui/view/sheet(item:ondismiss:content:))
- `func fullScreenCover` — [isPresented:](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:)) | [item:](/documentation/swiftui/view/fullscreencover(item:ondismiss:content:))
- `func popover` — [isPresented:](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:)) | [item:](/documentation/swiftui/view/popover(item:attachmentanchor:arrowedge:content:))
- [PopoverAttachmentAnchor](/documentation/swiftui/popoverattachmentanchor) — point(UnitPoint), rect(Anchor)

### Adapting a presentation size

- `func presentationCompactAdaptation` — [single](/documentation/swiftui/view/presentationcompactadaptation(_:)) | [horizontal:vertical:](/documentation/swiftui/view/presentationcompactadaptation(horizontal:vertical:))
- [PresentationAdaptation](/documentation/swiftui/presentationadaptation) — values: automatic, none, fullScreenCover, popover, sheet
- `func presentationSizing(...)` — [View](/documentation/swiftui/view/presentationsizing(_:))
- [PresentationSizing](/documentation/swiftui/presentationsizing) — values: automatic, fitted, form, page; fitted(h:v:), sticky(h:v:) | types: AutomaticPresentationSizing, FittedPresentationSizing, FormPresentationSizing, PagePresentationSizing
- [PresentationSizingRoot](/documentation/swiftui/presentationsizingroot), [PresentationSizingContext](/documentation/swiftui/presentationsizingcontext) — layout helpers

### Configuring a sheet's height

- `func presentationDetents` — [set](/documentation/swiftui/view/presentationdetents(_:)) | [selection:](/documentation/swiftui/view/presentationdetents(_:selection:))
- `func presentationContentInteraction(...)` — [View](/documentation/swiftui/view/presentationcontentinteraction(_:)) | `func presentationDragIndicator(...)` — [View](/documentation/swiftui/view/presentationdragindicator(_:))
- [PresentationDetent](/documentation/swiftui/presentationdetent) — large, medium; custom: fraction(_:), height(_:), custom(_:)
- [CustomPresentationDetent](/documentation/swiftui/custompresentationdetent) — protocol for custom height
- [PresentationContentInteraction](/documentation/swiftui/presentationcontentinteraction) — values: automatic, resizes, scrolls

### Styling a sheet and its background

- `func presentationCornerRadius(...)` — [View](/documentation/swiftui/view/presentationcornerradius(_:))
- `func presentationBackground` — [style](/documentation/swiftui/view/presentationbackground(_:)) | [alignment:content:](/documentation/swiftui/view/presentationbackground(alignment:content:))
- `func presentationBackgroundInteraction(...)` — [View](/documentation/swiftui/view/presentationbackgroundinteraction(_:))
- [PresentationBackgroundInteraction](/documentation/swiftui/presentationbackgroundinteraction) — values: automatic, disabled, enabled, enabled(upThrough:)

### Presenting an alert

- [AlertScene](/documentation/swiftui/alertscene) — macOS alert scene
- `func alert` — [basic](/documentation/swiftui/view/alert(_:ispresented:actions:)) | [error](/documentation/swiftui/view/alert(ispresented:error:actions:)) | [message](/documentation/swiftui/view/alert(_:ispresented:actions:message:)) — also presenting: variants

### Getting confirmation for an action

- `func confirmationDialog` — [basic](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:)) | [presenting:](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:)) | [message:](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:message:)) | [presenting:message:](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:message:))
- `func dismissalConfirmationDialog` — [basic](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:)) | [message:](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:message:))

### Configuring a dialog (view/scene)

- `func dialogIcon(Image?)` — [View](/documentation/swiftui/view/dialogicon(_:)) | [Scene](/documentation/swiftui/scene/dialogicon(_:))
- `func dialogSeverity(DialogSeverity)` — [View](/documentation/swiftui/view/dialogseverity(_:)) | [Scene](/documentation/swiftui/scene/dialogseverity(_:))
- `func dialogSuppressionToggle` — [isSuppressed:](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:)) | [_:isSuppressed:](/documentation/swiftui/view/dialogsuppressiontoggle(_:issuppressed:))

### File export, import, and move

- `func fileExporter` — [document](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:)) | [documents](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttype:oncompletion:)) | [contentTypes](/documentation/swiftui/view/fileexporter(ispresented:document:contenttypes:defaultfilename:oncompletion:oncancellation:)) | [documents+contentTypes](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttypes:oncompletion:oncancellation:)) | [item](/documentation/swiftui/view/fileexporter(ispresented:item:contenttypes:defaultfilename:oncompletion:oncancellation:)) | [items](/documentation/swiftui/view/fileexporter(ispresented:items:contenttypes:oncompletion:oncancellation:)) | [filenameLabel](/documentation/swiftui/view/fileexporterfilenamelabel(_:))
- `func fileImporter` — [multi](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:)) | [single](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:)) | [onCancellation](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:oncancellation:))
- `func fileMover` — [file](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:)) | [files](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:)) | [file+cancel](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:oncancellation:)) | [files+cancel](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:oncancellation:))
- File dialog modifiers: [browserOptions](/documentation/swiftui/view/filedialogbrowseroptions(_:)), [confirmationLabel](/documentation/swiftui/view/filedialogconfirmationlabel(_:)), [customizationID](/documentation/swiftui/view/filedialogcustomizationid(_:)), [defaultDirectory](/documentation/swiftui/view/filedialogdefaultdirectory(_:)), [importsUnresolvedAliases](/documentation/swiftui/view/filedialogimportsunresolvedaliases(_:)), [message](/documentation/swiftui/view/filedialogmessage(_:)), [urlEnabled](/documentation/swiftui/view/filedialogurlenabled(_:))
- [FileDialogBrowserOptions](/documentation/swiftui/filedialogbrowseroptions) — displayFileExtensions, enumeratePackages, includeHiddenFiles

### Presenting an inspector

- `func inspector(isPresented:content:)` — [View](/documentation/swiftui/view/inspector(ispresented:content:))
- `func inspectorColumnWidth` — [fixed](/documentation/swiftui/view/inspectorcolumnwidth(_:)) | [min:ideal:max:](/documentation/swiftui/view/inspectorcolumnwidth(min:ideal:max:))

### Dismissing a presentation

- env: `isPresented: Bool` — [EnvironmentValues](/documentation/swiftui/environmentvalues/ispresented)
- [DismissAction](/documentation/swiftui/dismissaction) — callable | env: `dismiss`
- `func interactiveDismissDisabled(Bool)` — [View](/documentation/swiftui/view/interactivedismissdisabled(_:))

### Deprecated modal presentations

- [Alert](/documentation/swiftui/alert) [deprecated -- prefer alert(_:isPresented:actions:)]
- [ActionSheet](/documentation/swiftui/actionsheet) [deprecated -- prefer confirmationDialog]

---

## Toolbars

- [Toolbars](/documentation/swiftui/toolbars) (article)

### Populating a toolbar

- `func toolbar(content:)` — [View](/documentation/swiftui/view/toolbar(content:)) | `func toolbar(id:content:)` — [customizable](/documentation/swiftui/view/toolbar(id:content:)) | `func toolbar(removing:)` — [remove defaults](/documentation/swiftui/view/toolbar(removing:))
- [ToolbarItem](/documentation/swiftui/toolbaritem) — single item | [ToolbarItemGroup](/documentation/swiftui/toolbaritemgroup) — group | [LabeledToolbarItemGroupContent](/documentation/swiftui/labeledtoolbaritemgroupcontent)
- [ToolbarItemPlacement](/documentation/swiftui/toolbaritemplacement) — semantic: automatic, principal, status | actions: primaryAction, secondaryAction, confirmationAction, cancellationAction, destructiveAction, navigation | explicit: topBarLeading, topBarTrailing, bottomBar, bottomOrnament, keyboard, accessoryBar(id:) | titles: largeSubtitle, largeTitle, subtitle, title | deprecated: init(id:), navigationBarLeading, navigationBarTrailing
- [ToolbarContent](/documentation/swiftui/toolbarcontent) — protocol; hidden(_:), matchedTransitionSource, sharedBackgroundVisibility | [ToolbarContentBuilder](/documentation/swiftui/toolbarcontentbuilder) — result builder
- [ToolbarSpacer](/documentation/swiftui/toolbarspacer), [DefaultToolbarItem](/documentation/swiftui/defaulttoolbaritem) — spacer and default items
- [CustomizableToolbarContent](/documentation/swiftui/customizabletoolbarcontent) — defaultCustomization, customizationBehavior
- [ToolbarCustomizationBehavior](/documentation/swiftui/toolbarcustomizationbehavior) — default, disabled, reorderable | [ToolbarCustomizationOptions](/documentation/swiftui/toolbarcustomizationoptions) — alwaysAvailable
- [ToolbarDefaultItemKind](/documentation/swiftui/toolbardefaultitemkind) — sidebarToggle, search, title | [SearchToolbarBehavior](/documentation/swiftui/searchtoolbarbehavior) — automatic, minimize

### Toolbar visibility, role, and styling

- `func toolbar(Visibility, for:)` [View](/documentation/swiftui/view/toolbar(_:for:)) | `func toolbarVisibility(...)` [View](/documentation/swiftui/view/toolbarvisibility(_:for:)) | `func toolbarBackgroundVisibility(...)` [View](/documentation/swiftui/view/toolbarbackgroundvisibility(_:for:))
- [ToolbarPlacement](/documentation/swiftui/toolbarplacement) — automatic, accessoryBar(id:), bottomBar, bottomOrnament, navigationBar, tabBar, windowToolbar | deprecated: init(id:)
- [ContentToolbarPlacement](/documentation/swiftui/contenttoolbarplacement) — tabViewSidebar
- `func toolbarRole(ToolbarRole)` [View](/documentation/swiftui/view/toolbarrole(_:)) | [ToolbarRole](/documentation/swiftui/toolbarrole) — automatic, browser, editor, navigationStack
- `func toolbarBackground(_:for:)` [View](/documentation/swiftui/view/toolbarbackground(_:for:)) | `func toolbarColorScheme(...)` [View](/documentation/swiftui/view/toolbarcolorscheme(_:for:)) | `func toolbarForegroundStyle(...)` [View](/documentation/swiftui/view/toolbarforegroundstyle(_:for:))
- [ToolbarLabelStyle](/documentation/swiftui/toolbarlabelstyle) — automatic, iconOnly, titleAndIcon, titleOnly | env: `toolbarLabelStyle`
- [SpacerSizing](/documentation/swiftui/spacersizing) — fixed, flexible

### Toolbar title

- `func toolbarTitleDisplayMode(...)` [View](/documentation/swiftui/view/toolbartitledisplaymode(_:)) | [ToolbarTitleDisplayMode](/documentation/swiftui/toolbartitledisplaymode) — automatic, inline, inlineLarge, large
- `func toolbarTitleMenu(content:)` [View](/documentation/swiftui/view/toolbartitlemenu(content:)) | [ToolbarTitleMenu](/documentation/swiftui/toolbartitlemenu) — title menu with optional custom content

### Creating an ornament

- `func ornament(visibility:attachmentAnchor:contentAlignment:ornament:)` — [View](/documentation/swiftui/view/ornament(visibility:attachmentanchor:contentalignment:ornament:))
- [OrnamentAttachmentAnchor](/documentation/swiftui/ornamentattachmentanchor) — scene(_:), parent(_:)

---

## Search

- Articles: [Search](/documentation/swiftui/search), [Adding a search interface](/documentation/swiftui/adding-a-search-interface-to-your-app), [Performing a search](/documentation/swiftui/performing-a-search-operation), [Suggesting search terms](/documentation/swiftui/suggesting-search-terms), [Scoping a search](/documentation/swiftui/scoping-a-search-operation), [Managing search activation](/documentation/swiftui/managing-search-interface-activation)

### Searching your app's data model

- `func searchable` — [text:](/documentation/swiftui/view/searchable(text:placement:prompt:)) | [tokens:](/documentation/swiftui/view/searchable(text:tokens:placement:prompt:token:)) | [editableTokens:](/documentation/swiftui/view/searchable(text:editabletokens:placement:prompt:token:))
- [SearchFieldPlacement](/documentation/swiftui/searchfieldplacement) — automatic, navigationBarDrawer, navigationBarDrawer(displayMode:), sidebar, toolbar, toolbarPrincipal

### Making search suggestions

- `func searchSuggestions` — [content](/documentation/swiftui/view/searchsuggestions(_:)) | [visibility](/documentation/swiftui/view/searchsuggestions(_:for:)) | `func searchCompletion(_:)` [View](/documentation/swiftui/view/searchcompletion(_:))
- `func searchable(text:tokens:suggestedTokens:...)` — [View](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:placement:prompt:token:))
- [SearchSuggestionsPlacement](/documentation/swiftui/searchsuggestionsplacement) — automatic, content, menu; Set with rawValue

### Limiting search scope

- `func searchScopes` — [basic](/documentation/swiftui/view/searchscopes(_:scopes:)) | [activation:](/documentation/swiftui/view/searchscopes(_:activation:_:))
- [SearchScopeActivation](/documentation/swiftui/searchscopeactivation) — automatic, onSearchPresentation, onTextEntry

### Detecting, activating, and dismissing search

- env: `isSearching: Bool` | `dismissSearch:` [DismissSearchAction](/documentation/swiftui/dismisssearchaction)
- `func searchable` isPresented variants — [text:](/documentation/swiftui/view/searchable(text:ispresented:placement:prompt:)) | [tokens:](/documentation/swiftui/view/searchable(text:tokens:ispresented:placement:prompt:token:)) | [editableTokens:](/documentation/swiftui/view/searchable(text:editabletokens:ispresented:placement:prompt:token:)) | [suggestedTokens:](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:ispresented:placement:prompt:token:))

### Displaying toolbar content during search

- [SearchPresentationToolbarBehavior](/documentation/swiftui/searchpresentationtoolbarbehavior) — automatic, avoidHidingContent | `func searchPresentationToolbarBehavior(...)` [View](/documentation/swiftui/view/searchpresentationtoolbarbehavior(_:))

### Searching for text in a view

- `func findNavigator(isPresented:)` [View](/documentation/swiftui/view/findnavigator(ispresented:)) | `func findDisabled(Bool)` [View](/documentation/swiftui/view/finddisabled(_:)) | `func replaceDisabled(Bool)` [View](/documentation/swiftui/view/replacedisabled(_:))
- [FindContext](/documentation/swiftui/findcontext) — isPresented, supportsReplace

---

## App extensions

- Articles: [App extensions](/documentation/swiftui/app-extensions), [Building Widgets](/documentation/widgetkit/building_widgets_using_widgetkit_and_swiftui), [Creating a widget extension](/documentation/widgetkit/creating-a-widget-extension), [Keeping a widget up to date](/documentation/widgetkit/keeping-a-widget-up-to-date), [Making a configurable widget](/documentation/widgetkit/making-a-configurable-widget)

### Creating widgets

- [Widget](/documentation/swiftui/widget) — protocol for widget entry point | [WidgetBundle](/documentation/swiftui/widgetbundle) — groups widgets | [WidgetBundleBuilder](/documentation/swiftui/widgetbundlebuilder) — result builder
- [WidgetConfiguration](/documentation/swiftui/widgetconfiguration) — protocol; configurationDisplayName, description, supportedFamilies, contentMarginsDisabled, disfavoredLocations, containerBackgroundRemovable, backgroundTask, pushHandler, supplementalActivityFamilies, supportedMountingStyles, widgetTexture
- [EmptyWidgetConfiguration](/documentation/swiftui/emptywidgetconfiguration) | [LimitedAvailabilityConfiguration](/documentation/swiftui/limitedavailabilityconfiguration)

### Composing control widgets

- [ControlWidget](/documentation/swiftui/controlwidget) — Control Center widget | [ControlWidgetConfiguration](/documentation/swiftui/controlwidgetconfiguration) — description, displayName, pushHandler
- [EmptyControlWidgetConfiguration](/documentation/swiftui/emptycontrolwidgetconfiguration) | [ControlWidgetConfigurationBuilder](/documentation/swiftui/controlwidgetconfigurationbuilder)
- [ControlWidgetTemplate](/documentation/swiftui/controlwidgettemplate) — disabled, privacySensitive, tint | [EmptyControlWidgetTemplate](/documentation/swiftui/emptycontrolwidgettemplate) | [ControlWidgetTemplateBuilder](/documentation/swiftui/controlwidgettemplatebuilder)
- `func controlWidgetActionHint(_:)` [View](/documentation/swiftui/view/controlwidgetactionhint(_:)) | `func controlWidgetStatus(_:)` [View](/documentation/swiftui/view/controlwidgetstatus(_:))

### Widget view modifiers

- `func widgetLabel` — [text](/documentation/swiftui/view/widgetlabel(_:)) | [label:](/documentation/swiftui/view/widgetlabel(label:))
- `func accessoryWidgetGroupStyle(...)` [View](/documentation/swiftui/view/accessorywidgetgroupstyle(_:)) | `func widgetAccentable(Bool)` [View](/documentation/swiftui/view/widgetaccentable(_:)) | `func dynamicIsland(verticalPlacement:)` [View](/documentation/swiftui/view/dynamicisland(verticalplacement:))
