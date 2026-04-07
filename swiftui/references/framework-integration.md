# Framework Integration — SwiftUI Reference

## Contents
- [Framework integration](#framework-integration)
  - [Displaying SwiftUI views in AppKit](#displaying-swiftui-views-in-appkit)
  - [Adding AppKit views to SwiftUI view hierarchies](#adding-appkit-views-to-swiftui-view-hierarchies)
  - [Adding AppKit gesture recognizers into SwiftUI view hierarchies](#adding-appkit-gesture-recognizers-into-swiftui-view-hierarchies)
  - [Displaying SwiftUI views in UIKit](#displaying-swiftui-views-in-uikit)
  - [Adding UIKit views to SwiftUI view hierarchies](#adding-uikit-views-to-swiftui-view-hierarchies)
  - [Adding UIKit gesture recognizers into SwiftUI view hierarchies](#adding-uikit-gesture-recognizers-into-swiftui-view-hierarchies)
  - [Sharing configuration information](#sharing-configuration-information)
  - [Hosting an ornament in UIKit](#hosting-an-ornament-in-uikit)
  - [Displaying SwiftUI views in WatchKit](#displaying-swiftui-views-in-watchkit)
  - [Adding WatchKit views to SwiftUI view hierarchies](#adding-watchkit-views-to-swiftui-view-hierarchies)
  - [Displaying web content](#displaying-web-content)
  - [Accessing Apple Pay and Wallet](#accessing-apple-pay-and-wallet)
  - [Authorizing and authenticating](#authorizing-and-authenticating)
  - [Configuring Family Sharing](#configuring-family-sharing)
  - [Reporting on device activity](#reporting-on-device-activity)
  - [Working with managed devices](#working-with-managed-devices)
  - [Creating graphics](#creating-graphics)
  - [Getting location information](#getting-location-information)
  - [Displaying media](#displaying-media)
  - [Selecting photos](#selecting-photos)
  - [Previewing content](#previewing-content)
  - [Interacting with networked devices](#interacting-with-networked-devices)
  - [Configuring a Live Activity](#configuring-a-live-activity)
  - [Interacting with the App Store and Apple Music](#interacting-with-the-app-store-and-apple-music)
  - [Accessing health data](#accessing-health-data)
  - [Providing tips](#providing-tips)
  - [Showing a translation](#showing-a-translation)
  - [Presenting journaling suggestions](#presenting-journaling-suggestions)
  - [Managing contact access](#managing-contact-access)
  - [Handling game controller events](#handling-game-controller-events)
  - [Creating a tabletop game](#creating-a-tabletop-game)
  - [Configuring camera controls](#configuring-camera-controls)
  - [Interacting with transactions](#interacting-with-transactions)
- [Tool support](#tool-support)
  - [Essentials](#essentials)
  - [Creating a preview](#creating-a-preview)
  - [Creating a preview in the context of a scene](#creating-a-preview-in-the-context-of-a-scene)
  - [Defining a preview](#defining-a-preview)
  - [Customizing a preview](#customizing-a-preview)
  - [Setting a context](#setting-a-context)
  - [Building in debug mode](#building-in-debug-mode)
  - [Creating library items](#creating-library-items)
  - [Essentials](#essentials)
  - [Analyzing SwiftUI performance](#analyzing-swiftui-performance)

---
## Framework integration

- [AppKit integration](/documentation/swiftui/appkit-integration)

### Displaying SwiftUI views in AppKit

- [Unifying your app’s animations](/documentation/swiftui/unifying-your-app-s-animations)
- [NSHostingController](/documentation/swiftui/nshostingcontroller)

#### Creating a hosting controller object

- [init(rootView: Content)](/documentation/swiftui/nshostingcontroller/init(rootview:))
- [init?(coder: NSCoder, rootView: Content)](/documentation/swiftui/nshostingcontroller/init(coder:rootview:))
- [init?(coder: NSCoder)](/documentation/swiftui/nshostingcontroller/init(coder:))

#### Getting the root view

- [var rootView: Content](/documentation/swiftui/nshostingcontroller/rootview)
- [var identifier: NSUserInterfaceItemIdentifier?](/documentation/swiftui/nshostingcontroller/identifier)

#### Configuring the controller

- [func sizeThatFits(in: CGSize) -> CGSize](/documentation/swiftui/nshostingcontroller/sizethatfits(in:))
- [var preferredContentSize: NSSize](/documentation/swiftui/nshostingcontroller/preferredcontentsize)
- [var sizingOptions: NSHostingSizingOptions](/documentation/swiftui/nshostingcontroller/sizingoptions)
- [var safeAreaRegions: SafeAreaRegions](/documentation/swiftui/nshostingcontroller/safearearegions)
- [var sceneBridgingOptions: NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingcontroller/scenebridgingoptions)
- [NSHostingView](/documentation/swiftui/nshostingview)

#### Creating a hosting view

- [init(rootView: Content)](/documentation/swiftui/nshostingview/init(rootview:))
- [init?(coder: NSCoder)](/documentation/swiftui/nshostingview/init(coder:))
- [func prepareForReuse()](/documentation/swiftui/nshostingview/prepareforreuse())

#### Getting the root view

- [var rootView: Content](/documentation/swiftui/nshostingview/rootview)

#### Configuring the view layout behavior

- [class var requiresConstraintBasedLayout: Bool](/documentation/swiftui/nshostingview/requiresconstraintbasedlayout)
- [var userInterfaceLayoutDirection: NSUserInterfaceLayoutDirection](/documentation/swiftui/nshostingview/userinterfacelayoutdirection)
- [var isFlipped: Bool](/documentation/swiftui/nshostingview/isflipped)
- [var layerContentsRedrawPolicy: NSView.LayerContentsRedrawPolicy](/documentation/swiftui/nshostingview/layercontentsredrawpolicy)
- [func updateConstraints()](/documentation/swiftui/nshostingview/updateconstraints())
- [func layout()](/documentation/swiftui/nshostingview/layout())
- [var safeAreaRegions: SafeAreaRegions](/documentation/swiftui/nshostingview/safearearegions)

#### Managing keyboard interaction

- [func keyDown(with: NSEvent)](/documentation/swiftui/nshostingview/keydown(with:))
- [func keyUp(with: NSEvent)](/documentation/swiftui/nshostingview/keyup(with:))
- [func performKeyEquivalent(with: NSEvent) -> Bool](/documentation/swiftui/nshostingview/performkeyequivalent(with:))
- [func insertText(Any)](/documentation/swiftui/nshostingview/inserttext(_:))
- [func didChangeValue(forKey: String)](/documentation/swiftui/nshostingview/didchangevalue(forkey:))
- [func makeTouchBar() -> NSTouchBar?](/documentation/swiftui/nshostingview/maketouchbar())

#### Responding to mouse events

- [func mouseDown(with: NSEvent)](/documentation/swiftui/nshostingview/mousedown(with:))
- [func mouseUp(with: NSEvent)](/documentation/swiftui/nshostingview/mouseup(with:))
- [func otherMouseDown(with: NSEvent)](/documentation/swiftui/nshostingview/othermousedown(with:))
- [func otherMouseUp(with: NSEvent)](/documentation/swiftui/nshostingview/othermouseup(with:))
- [func rightMouseDown(with: NSEvent)](/documentation/swiftui/nshostingview/rightmousedown(with:))
- [func rightMouseUp(with: NSEvent)](/documentation/swiftui/nshostingview/rightmouseup(with:))
- [func mouseEntered(with: NSEvent)](/documentation/swiftui/nshostingview/mouseentered(with:))
- [func mouseExited(with: NSEvent)](/documentation/swiftui/nshostingview/mouseexited(with:))
- [func mouseDragged(with: NSEvent)](/documentation/swiftui/nshostingview/mousedragged(with:))
- [func mouseMoved(with: NSEvent)](/documentation/swiftui/nshostingview/mousemoved(with:))
- [func otherMouseDragged(with: NSEvent)](/documentation/swiftui/nshostingview/othermousedragged(with:))
- [func rightMouseDragged(with: NSEvent)](/documentation/swiftui/nshostingview/rightmousedragged(with:))
- [func cursorUpdate(with: NSEvent)](/documentation/swiftui/nshostingview/cursorupdate(with:))

#### Responding to touch events

- [func touchesBegan(with: NSEvent)](/documentation/swiftui/nshostingview/touchesbegan(with:))
- [func touchesCancelled(with: NSEvent)](/documentation/swiftui/nshostingview/touchescancelled(with:))
- [func touchesEnded(with: NSEvent)](/documentation/swiftui/nshostingview/touchesended(with:))
- [func touchesMoved(with: NSEvent)](/documentation/swiftui/nshostingview/touchesmoved(with:))

#### Responding to gestures

- [func magnify(with: NSEvent)](/documentation/swiftui/nshostingview/magnify(with:))
- [func rotate(with: NSEvent)](/documentation/swiftui/nshostingview/rotate(with:))
- [func scrollWheel(with: NSEvent)](/documentation/swiftui/nshostingview/scrollwheel(with:))

#### Handling drag and drop

- [func validRequestor(forSendType: NSPasteboard.PasteboardType?, returnType: NSPasteboard.PasteboardType?) -> Any?](/documentation/swiftui/nshostingview/validrequestor(forsendtype:returntype:))

#### Providing a context menu

- [func menu(for: NSEvent) -> NSMenu?](/documentation/swiftui/nshostingview/menu(for:))

#### Responding to actions

- [func responds(to: Selector!) -> Bool](/documentation/swiftui/nshostingview/responds(to:))
- [func forwardingTarget(for: Selector!) -> Any?](/documentation/swiftui/nshostingview/forwardingtarget(for:))
- [func doCommand(by: Selector)](/documentation/swiftui/nshostingview/docommand(by:))

#### Configuring the responder behavior

- [var acceptsFirstResponder: Bool](/documentation/swiftui/nshostingview/acceptsfirstresponder)
- [var needsPanelToBecomeKey: Bool](/documentation/swiftui/nshostingview/needspaneltobecomekey)

#### Managing the view hierarchy

- [func viewWillMove(toWindow: NSWindow?)](/documentation/swiftui/nshostingview/viewwillmove(towindow:))
- [func viewDidMoveToWindow()](/documentation/swiftui/nshostingview/viewdidmovetowindow())
- [func viewDidChangeBackingProperties()](/documentation/swiftui/nshostingview/viewdidchangebackingproperties())
- [func viewDidChangeEffectiveAppearance()](/documentation/swiftui/nshostingview/viewdidchangeeffectiveappearance())

#### Modifying the frame rectangle

- [var intrinsicContentSize: NSSize](/documentation/swiftui/nshostingview/intrinsiccontentsize)
- [func setFrameSize(NSSize)](/documentation/swiftui/nshostingview/setframesize(_:))
- [var firstBaselineOffsetFromTop: CGFloat](/documentation/swiftui/nshostingview/firstbaselineoffsetfromtop)
- [var lastBaselineOffsetFromBottom: CGFloat](/documentation/swiftui/nshostingview/lastbaselineoffsetfrombottom)
- [var sizingOptions: NSHostingSizingOptions](/documentation/swiftui/nshostingview/sizingoptions)
- [var firstTextLineCenter: CGFloat?](/documentation/swiftui/nshostingview/firsttextlinecenter)

#### Testing for hits

- [func hitTest(NSPoint) -> NSView?](/documentation/swiftui/nshostingview/hittest(_:))

#### Managing accessibility behaviors

- [var accessibilityFocusedUIElement: Any?](/documentation/swiftui/nshostingview/accessibilityfocuseduielement)
- [func accessibilityChildren() -> [Any]?](/documentation/swiftui/nshostingview/accessibilitychildren())
- [func accessibilityChildrenInNavigationOrder() -> [any NSAccessibilityElementProtocol]?](/documentation/swiftui/nshostingview/accessibilitychildreninnavigationorder())
- [func accessibilityHitTest(NSPoint) -> Any?](/documentation/swiftui/nshostingview/accessibilityhittest(_:))
- [func accessibilityRole() -> NSAccessibility.Role?](/documentation/swiftui/nshostingview/accessibilityrole())
- [func accessibilitySubrole() -> NSAccessibility.Subrole?](/documentation/swiftui/nshostingview/accessibilitysubrole())
- [func isAccessibilityElement() -> Bool](/documentation/swiftui/nshostingview/isaccessibilityelement())

#### Bridging with SwiftUI

- [var sceneBridgingOptions: NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingview/scenebridgingoptions)

#### Initializers

- [init?(coder: NSCoder, rootView: Content)](/documentation/swiftui/nshostingview/init(coder:rootview:))

#### Instance Properties

- [var clipsToBounds: Bool](/documentation/swiftui/nshostingview/clipstobounds)

#### Instance Methods

- [func acceptsFirstMouse(for: NSEvent?) -> Bool](/documentation/swiftui/nshostingview/acceptsfirstmouse(for:))
- [func beginDocument()](/documentation/swiftui/nshostingview/begindocument())
- [func didAddSubview(NSView)](/documentation/swiftui/nshostingview/didaddsubview(_:))
- [func endDocument()](/documentation/swiftui/nshostingview/enddocument())
- [func observeValue(forKeyPath: String?, of: Any?, change: [NSKeyValueChangeKey : Any]?, context: UnsafeMutableRawPointer?)](/documentation/swiftui/nshostingview/observevalue(forkeypath:of:change:context:))
- [func shouldDelayWindowOrdering(for: NSEvent) -> Bool](/documentation/swiftui/nshostingview/shoulddelaywindowordering(for:))
- [func showContextMenuForSelection(Any?)](/documentation/swiftui/nshostingview/showcontextmenuforselection(_:))
- [func viewDidEndLiveResize()](/documentation/swiftui/nshostingview/viewdidendliveresize())
- [func viewWillStartLiveResize()](/documentation/swiftui/nshostingview/viewwillstartliveresize())
- [func willRemoveSubview(NSView)](/documentation/swiftui/nshostingview/willremovesubview(_:))
- [NSHostingMenu](/documentation/swiftui/nshostingmenu)

#### Initializers

- [init(rootView: Content)](/documentation/swiftui/nshostingmenu/init(rootview:))

#### Instance Properties

- [var rootView: Content](/documentation/swiftui/nshostingmenu/rootview)
- [NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions)

#### Geting sizing options

- [static let intrinsicContentSize: NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions/intrinsiccontentsize)
- [static let maxSize: NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions/maxsize)
- [static let minSize: NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions/minsize)
- [static let preferredContentSize: NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions/preferredcontentsize)
- [static let standardBounds: NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions/standardbounds)

#### Creating a sizing option

- [init(rawValue: Int)](/documentation/swiftui/nshostingsizingoptions/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/nshostingsizingoptions/rawvalue)
- [NSHostingSceneRepresentation](/documentation/swiftui/nshostingscenerepresentation)

#### Initializers

- [init(rootScene: () -> Content)](/documentation/swiftui/nshostingscenerepresentation/init(rootscene:))

#### Instance Properties

- [var environment: EnvironmentValues](/documentation/swiftui/nshostingscenerepresentation/environment)
- [NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions)

#### Geting bridging options

- [static let all: NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions/all)
- [static let title: NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions/title)
- [static let toolbars: NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions/toolbars)

#### Creating a bridging options

- [init(rawValue: Int)](/documentation/swiftui/nshostingscenebridgingoptions/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/nshostingscenebridgingoptions/rawvalue)

### Adding AppKit views to SwiftUI view hierarchies

- [NSViewRepresentable](/documentation/swiftui/nsviewrepresentable)

#### Creating and updating the view

- [func makeNSView(context: Self.Context) -> Self.NSViewType](/documentation/swiftui/nsviewrepresentable/makensview(context:))
- [func updateNSView(Self.NSViewType, context: Self.Context)](/documentation/swiftui/nsviewrepresentable/updatensview(_:context:))
- [NSViewRepresentable.Context](/documentation/swiftui/nsviewrepresentable/context)
- [NSViewType](/documentation/swiftui/nsviewrepresentable/nsviewtype)

#### Specifying a size

- [func sizeThatFits(ProposedViewSize, nsView: Self.NSViewType, context: Self.Context) -> CGSize?](/documentation/swiftui/nsviewrepresentable/sizethatfits(_:nsview:context:))

#### Cleaning up the view

- [static func dismantleNSView(Self.NSViewType, coordinator: Self.Coordinator)](/documentation/swiftui/nsviewrepresentable/dismantlensview(_:coordinator:))

#### Providing a custom coordinator object

- [func makeCoordinator() -> Self.Coordinator](/documentation/swiftui/nsviewrepresentable/makecoordinator())
- [Coordinator](/documentation/swiftui/nsviewrepresentable/coordinator)

#### Performing layout

- [NSViewRepresentable.LayoutOptions](/documentation/swiftui/nsviewrepresentable/layoutoptions)
- [NSViewRepresentableContext](/documentation/swiftui/nsviewrepresentablecontext)

#### Coordinating view-related interactions

- [let coordinator: View.Coordinator](/documentation/swiftui/nsviewrepresentablecontext/coordinator)
- [var transaction: Transaction](/documentation/swiftui/nsviewrepresentablecontext/transaction)

#### Getting the current environment data

- [var environment: EnvironmentValues](/documentation/swiftui/nsviewrepresentablecontext/environment)

#### Instance Methods

- [func animate(changes: () -> Void, completion: (() -> Void)?)](/documentation/swiftui/nsviewrepresentablecontext/animate(changes:completion:))
- [NSViewControllerRepresentable](/documentation/swiftui/nsviewcontrollerrepresentable)

#### Creating and updating the view controller

- [func makeNSViewController(context: Self.Context) -> Self.NSViewControllerType](/documentation/swiftui/nsviewcontrollerrepresentable/makensviewcontroller(context:))
- [func updateNSViewController(Self.NSViewControllerType, context: Self.Context)](/documentation/swiftui/nsviewcontrollerrepresentable/updatensviewcontroller(_:context:))
- [NSViewControllerRepresentable.Context](/documentation/swiftui/nsviewcontrollerrepresentable/context)
- [NSViewControllerType](/documentation/swiftui/nsviewcontrollerrepresentable/nsviewcontrollertype)

#### Specifying a size

- [func sizeThatFits(ProposedViewSize, nsViewController: Self.NSViewControllerType, context: Self.Context) -> CGSize?](/documentation/swiftui/nsviewcontrollerrepresentable/sizethatfits(_:nsviewcontroller:context:))

#### Cleaning up the view controller

- [static func dismantleNSViewController(Self.NSViewControllerType, coordinator: Self.Coordinator)](/documentation/swiftui/nsviewcontrollerrepresentable/dismantlensviewcontroller(_:coordinator:))

#### Providing a custom coordinator object

- [func makeCoordinator() -> Self.Coordinator](/documentation/swiftui/nsviewcontrollerrepresentable/makecoordinator())
- [Coordinator](/documentation/swiftui/nsviewcontrollerrepresentable/coordinator)

#### Performing layout

- [NSViewControllerRepresentable.LayoutOptions](/documentation/swiftui/nsviewcontrollerrepresentable/layoutoptions)
- [NSViewControllerRepresentableContext](/documentation/swiftui/nsviewcontrollerrepresentablecontext)

#### Coordinating view-related interactions

- [let coordinator: ViewController.Coordinator](/documentation/swiftui/nsviewcontrollerrepresentablecontext/coordinator)
- [var transaction: Transaction](/documentation/swiftui/nsviewcontrollerrepresentablecontext/transaction)

#### Getting the current environment data

- [var environment: EnvironmentValues](/documentation/swiftui/nsviewcontrollerrepresentablecontext/environment)

#### Instance Methods

- [func animate(changes: () -> Void, completion: (() -> Void)?)](/documentation/swiftui/nsviewcontrollerrepresentablecontext/animate(changes:completion:))

### Adding AppKit gesture recognizers into SwiftUI view hierarchies

- [NSGestureRecognizerRepresentable](/documentation/swiftui/nsgesturerecognizerrepresentable)

#### Associated Types

- [Coordinator](/documentation/swiftui/nsgesturerecognizerrepresentable/coordinator)
- [NSGestureRecognizerType](/documentation/swiftui/nsgesturerecognizerrepresentable/nsgesturerecognizertype)

#### Instance Methods

- [func handleNSGestureRecognizerAction(Self.NSGestureRecognizerType, context: Self.Context)](/documentation/swiftui/nsgesturerecognizerrepresentable/handlensgesturerecognizeraction(_:context:))
- [func makeCoordinator(converter: Self.CoordinateSpaceConverter) -> Self.Coordinator](/documentation/swiftui/nsgesturerecognizerrepresentable/makecoordinator(converter:))
- [func makeNSGestureRecognizer(context: Self.Context) -> Self.NSGestureRecognizerType](/documentation/swiftui/nsgesturerecognizerrepresentable/makensgesturerecognizer(context:))
- [func updateNSGestureRecognizer(Self.NSGestureRecognizerType, context: Self.Context)](/documentation/swiftui/nsgesturerecognizerrepresentable/updatensgesturerecognizer(_:context:))

#### Type Aliases

- [NSGestureRecognizerRepresentable.Context](/documentation/swiftui/nsgesturerecognizerrepresentable/context)
- [NSGestureRecognizerRepresentable.CoordinateSpaceConverter](/documentation/swiftui/nsgesturerecognizerrepresentable/coordinatespaceconverter)
- [NSGestureRecognizerRepresentableContext](/documentation/swiftui/nsgesturerecognizerrepresentablecontext)

#### Instance Properties

- [let converter: NSGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/nsgesturerecognizerrepresentablecontext/converter)
- [let coordinator: Representable.Coordinator](/documentation/swiftui/nsgesturerecognizerrepresentablecontext/coordinator)
- [NSGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter)

#### Instance Properties

- [var localLocation: CGPoint](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/locallocation)
- [var localTranslation: CGPoint?](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/localtranslation)
- [var localVelocity: CGPoint?](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/localvelocity)

#### Instance Methods

- [func convert(globalPoint: CGPoint, to: some CoordinateSpaceProtocol) -> CGPoint](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/convert(globalpoint:to:))
- [func location(in: some CoordinateSpaceProtocol) -> CGPoint](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/location(in:))
- [func translation(in: some CoordinateSpaceProtocol) -> CGPoint?](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/translation(in:))
- [func velocity(in: some CoordinateSpaceProtocol) -> CGPoint?](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter/velocity(in:))
- [UIKit integration](/documentation/swiftui/uikit-integration)

### Displaying SwiftUI views in UIKit

- [Using SwiftUI with UIKit](/documentation/uikit/using-swiftui-with-uikit)
- [Unifying your app’s animations](/documentation/swiftui/unifying-your-app-s-animations)
- [UIHostingController](/documentation/swiftui/uihostingcontroller)

#### Creating a hosting controller object

- [init(rootView: Content)](/documentation/swiftui/uihostingcontroller/init(rootview:))
- [init?(coder: NSCoder, rootView: Content)](/documentation/swiftui/uihostingcontroller/init(coder:rootview:))
- [init?(coder: NSCoder)](/documentation/swiftui/uihostingcontroller/init(coder:))

#### Responding to view-related events

- [func loadView()](/documentation/swiftui/uihostingcontroller/loadview())
- [func viewWillAppear(Bool)](/documentation/swiftui/uihostingcontroller/viewwillappear(_:))
- [func viewDidAppear(Bool)](/documentation/swiftui/uihostingcontroller/viewdidappear(_:))
- [func viewWillDisappear(Bool)](/documentation/swiftui/uihostingcontroller/viewwilldisappear(_:))
- [func viewDidDisappear(Bool)](/documentation/swiftui/uihostingcontroller/viewdiddisappear(_:))
- [func willMove(toParent: UIViewController?)](/documentation/swiftui/uihostingcontroller/willmove(toparent:))
- [func didMove(toParent: UIViewController?)](/documentation/swiftui/uihostingcontroller/didmove(toparent:))
- [func viewWillTransition(to: CGSize, with: any UIViewControllerTransitionCoordinator)](/documentation/swiftui/uihostingcontroller/viewwilltransition(to:with:))
- [func viewWillLayoutSubviews()](/documentation/swiftui/uihostingcontroller/viewwilllayoutsubviews())
- [func target(forAction: Selector, withSender: Any?) -> Any?](/documentation/swiftui/uihostingcontroller/target(foraction:withsender:))
- [var rootView: Content](/documentation/swiftui/uihostingcontroller/rootview)

#### Checking for modality

- [var isModalInPresentation: Bool](/documentation/swiftui/uihostingcontroller/ismodalinpresentation)

#### Managing the size

- [var sizingOptions: UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontroller/sizingoptions)
- [func preferredContentSizeDidChange(forChildContentContainer: any UIContentContainer)](/documentation/swiftui/uihostingcontroller/preferredcontentsizedidchange(forchildcontentcontainer:))
- [func sizeThatFits(in: CGSize) -> CGSize](/documentation/swiftui/uihostingcontroller/sizethatfits(in:))
- [var safeAreaRegions: SafeAreaRegions](/documentation/swiftui/uihostingcontroller/safearearegions)

#### Configuring the status bar

- [var preferredStatusBarStyle: UIStatusBarStyle](/documentation/swiftui/uihostingcontroller/preferredstatusbarstyle)
- [var preferredStatusBarUpdateAnimation: UIStatusBarAnimation](/documentation/swiftui/uihostingcontroller/preferredstatusbarupdateanimation)
- [var prefersStatusBarHidden: Bool](/documentation/swiftui/uihostingcontroller/prefersstatusbarhidden)
- [var childForStatusBarStyle: UIViewController?](/documentation/swiftui/uihostingcontroller/childforstatusbarstyle)
- [var childForStatusBarHidden: UIViewController?](/documentation/swiftui/uihostingcontroller/childforstatusbarhidden)

#### Configuring the home indicator

- [var prefersHomeIndicatorAutoHidden: Bool](/documentation/swiftui/uihostingcontroller/prefershomeindicatorautohidden)
- [var childForHomeIndicatorAutoHidden: UIViewController?](/documentation/swiftui/uihostingcontroller/childforhomeindicatorautohidden)

#### Configuring the interface appearance

- [var preferredUserInterfaceStyle: UIUserInterfaceStyle](/documentation/swiftui/uihostingcontroller/preferreduserinterfacestyle)
- [var preferredScreenEdgesDeferringSystemGestures: UIRectEdge](/documentation/swiftui/uihostingcontroller/preferredscreenedgesdeferringsystemgestures)
- [var childForScreenEdgesDeferringSystemGestures: UIViewController?](/documentation/swiftui/uihostingcontroller/childforscreenedgesdeferringsystemgestures)

#### Accessing the available key commands

- [var keyCommands: [UIKeyCommand]?](/documentation/swiftui/uihostingcontroller/keycommands)

#### Managing undo

- [var undoManager: UndoManager?](/documentation/swiftui/uihostingcontroller/undomanager)

#### Instance Properties

- [var childViewControllerForPreferredContainerBackgroundStyle: UIViewController?](/documentation/swiftui/uihostingcontroller/childviewcontrollerforpreferredcontainerbackgroundstyle)
- [var preferredContainerBackgroundStyle: UIContainerBackgroundStyle](/documentation/swiftui/uihostingcontroller/preferredcontainerbackgroundstyle)

#### Instance Methods

- [func addChild(UIViewController)](/documentation/swiftui/uihostingcontroller/addchild(_:))
- [UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontrollersizingoptions)

#### Getting sizing options

- [static let intrinsicContentSize: UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontrollersizingoptions/intrinsiccontentsize)
- [static let preferredContentSize: UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontrollersizingoptions/preferredcontentsize)

#### Creating a sizing option

- [init(rawValue: Int)](/documentation/swiftui/uihostingcontrollersizingoptions/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/uihostingcontrollersizingoptions/rawvalue)
- [UIHostingConfiguration](/documentation/swiftui/uihostingconfiguration)

#### Creating and updating a configuration

- [init(content: () -> Content)](/documentation/swiftui/uihostingconfiguration/init(content:))

#### Setting the background

- [func background<S>(S) -> UIHostingConfiguration<Content, _UIHostingConfigurationBackgroundView<S>>](/documentation/swiftui/uihostingconfiguration/background(_:))
- [func background<B>(content: () -> B) -> UIHostingConfiguration<Content, B>](/documentation/swiftui/uihostingconfiguration/background(content:))

#### Setting margins

- [func margins(_:_:)](/documentation/swiftui/uihostingconfiguration/margins(_:_:))

#### Setting a size

- [func minSize(width: CGFloat?, height: CGFloat?) -> UIHostingConfiguration<Content, Background>](/documentation/swiftui/uihostingconfiguration/minsize(width:height:))
- [func minSize() -> UIHostingConfiguration<Content, Background>](/documentation/swiftui/uihostingconfiguration/minsize())
- [UIHostingSceneDelegate](/documentation/swiftui/uihostingscenedelegate)

#### Associated Types

- [RootScene](/documentation/swiftui/uihostingscenedelegate/rootscene-swift.associatedtype)

#### Type Properties

- [static var rootScene: Self.RootScene](/documentation/swiftui/uihostingscenedelegate/rootscene-swift.type.property)

### Adding UIKit views to SwiftUI view hierarchies

- [UIViewRepresentable](/documentation/swiftui/uiviewrepresentable)

#### Creating and updating the view

- [func makeUIView(context: Self.Context) -> Self.UIViewType](/documentation/swiftui/uiviewrepresentable/makeuiview(context:))
- [func updateUIView(Self.UIViewType, context: Self.Context)](/documentation/swiftui/uiviewrepresentable/updateuiview(_:context:))
- [UIViewRepresentable.Context](/documentation/swiftui/uiviewrepresentable/context)
- [UIViewType](/documentation/swiftui/uiviewrepresentable/uiviewtype)

#### Specifying a size

- [func sizeThatFits(ProposedViewSize, uiView: Self.UIViewType, context: Self.Context) -> CGSize?](/documentation/swiftui/uiviewrepresentable/sizethatfits(_:uiview:context:))

#### Cleaning up the view

- [static func dismantleUIView(Self.UIViewType, coordinator: Self.Coordinator)](/documentation/swiftui/uiviewrepresentable/dismantleuiview(_:coordinator:))

#### Providing a custom coordinator object

- [func makeCoordinator() -> Self.Coordinator](/documentation/swiftui/uiviewrepresentable/makecoordinator())
- [Coordinator](/documentation/swiftui/uiviewrepresentable/coordinator)

#### Performing layout

- [UIViewRepresentable.LayoutOptions](/documentation/swiftui/uiviewrepresentable/layoutoptions)
- [UIViewRepresentableContext](/documentation/swiftui/uiviewrepresentablecontext)

#### Coordinating view-related interactions

- [let coordinator: Representable.Coordinator](/documentation/swiftui/uiviewrepresentablecontext/coordinator)
- [var transaction: Transaction](/documentation/swiftui/uiviewrepresentablecontext/transaction)

#### Getting the current environment data

- [var environment: EnvironmentValues](/documentation/swiftui/uiviewrepresentablecontext/environment)

#### Instance Methods

- [func animate(changes: () -> Void, completion: (() -> Void)?)](/documentation/swiftui/uiviewrepresentablecontext/animate(changes:completion:))
- [UIViewControllerRepresentable](/documentation/swiftui/uiviewcontrollerrepresentable)

#### Creating and updating the view controller

- [func makeUIViewController(context: Self.Context) -> Self.UIViewControllerType](/documentation/swiftui/uiviewcontrollerrepresentable/makeuiviewcontroller(context:))
- [func updateUIViewController(Self.UIViewControllerType, context: Self.Context)](/documentation/swiftui/uiviewcontrollerrepresentable/updateuiviewcontroller(_:context:))
- [UIViewControllerRepresentable.Context](/documentation/swiftui/uiviewcontrollerrepresentable/context)
- [UIViewControllerType](/documentation/swiftui/uiviewcontrollerrepresentable/uiviewcontrollertype)

#### Specifying a size

- [func sizeThatFits(ProposedViewSize, uiViewController: Self.UIViewControllerType, context: Self.Context) -> CGSize?](/documentation/swiftui/uiviewcontrollerrepresentable/sizethatfits(_:uiviewcontroller:context:))

#### Cleaning up the view controller

- [static func dismantleUIViewController(Self.UIViewControllerType, coordinator: Self.Coordinator)](/documentation/swiftui/uiviewcontrollerrepresentable/dismantleuiviewcontroller(_:coordinator:))

#### Providing a custom coordinator object

- [func makeCoordinator() -> Self.Coordinator](/documentation/swiftui/uiviewcontrollerrepresentable/makecoordinator())
- [Coordinator](/documentation/swiftui/uiviewcontrollerrepresentable/coordinator)

#### Performing layout

- [UIViewControllerRepresentable.LayoutOptions](/documentation/swiftui/uiviewcontrollerrepresentable/layoutoptions)
- [UIViewControllerRepresentableContext](/documentation/swiftui/uiviewcontrollerrepresentablecontext)

#### Coordinating view controller interactions

- [let coordinator: Representable.Coordinator](/documentation/swiftui/uiviewcontrollerrepresentablecontext/coordinator)
- [var transaction: Transaction](/documentation/swiftui/uiviewcontrollerrepresentablecontext/transaction)

#### Getting the environment data

- [var environment: EnvironmentValues](/documentation/swiftui/uiviewcontrollerrepresentablecontext/environment)

#### Instance Methods

- [func animate(changes: () -> Void, completion: (() -> Void)?)](/documentation/swiftui/uiviewcontrollerrepresentablecontext/animate(changes:completion:))

### Adding UIKit gesture recognizers into SwiftUI view hierarchies

- [UIGestureRecognizerRepresentable](/documentation/swiftui/uigesturerecognizerrepresentable)

#### Associated Types

- [Coordinator](/documentation/swiftui/uigesturerecognizerrepresentable/coordinator)
- [UIGestureRecognizerType](/documentation/swiftui/uigesturerecognizerrepresentable/uigesturerecognizertype)

#### Instance Methods

- [func handleUIGestureRecognizerAction(Self.UIGestureRecognizerType, context: Self.Context)](/documentation/swiftui/uigesturerecognizerrepresentable/handleuigesturerecognizeraction(_:context:))
- [func makeCoordinator(converter: Self.CoordinateSpaceConverter) -> Self.Coordinator](/documentation/swiftui/uigesturerecognizerrepresentable/makecoordinator(converter:))
- [func makeUIGestureRecognizer(context: Self.Context) -> Self.UIGestureRecognizerType](/documentation/swiftui/uigesturerecognizerrepresentable/makeuigesturerecognizer(context:))
- [func updateUIGestureRecognizer(Self.UIGestureRecognizerType, context: Self.Context)](/documentation/swiftui/uigesturerecognizerrepresentable/updateuigesturerecognizer(_:context:))

#### Type Aliases

- [UIGestureRecognizerRepresentable.Context](/documentation/swiftui/uigesturerecognizerrepresentable/context)
- [UIGestureRecognizerRepresentable.CoordinateSpaceConverter](/documentation/swiftui/uigesturerecognizerrepresentable/coordinatespaceconverter)
- [UIGestureRecognizerRepresentableContext](/documentation/swiftui/uigesturerecognizerrepresentablecontext)

#### Instance Properties

- [let converter: UIGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/uigesturerecognizerrepresentablecontext/converter)
- [let coordinator: Representable.Coordinator](/documentation/swiftui/uigesturerecognizerrepresentablecontext/coordinator)
- [UIGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter)

#### Instance Properties

- [var localLocation: CGPoint](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/locallocation)
- [var localTranslation: CGPoint?](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/localtranslation)
- [var localVelocity: CGPoint?](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/localvelocity)

#### Instance Methods

- [func convert(globalPoint: CGPoint, to: some CoordinateSpaceProtocol) -> CGPoint](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/convert(globalpoint:to:))
- [func location(in: some CoordinateSpaceProtocol) -> CGPoint](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/location(in:))
- [func translation(in: some CoordinateSpaceProtocol) -> CGPoint?](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/translation(in:))
- [func velocity(in: some CoordinateSpaceProtocol) -> CGPoint?](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter/velocity(in:))

### Sharing configuration information

- [UITraitBridgedEnvironmentKey](/documentation/swiftui/uitraitbridgedenvironmentkey)

### Hosting an ornament in UIKit

- [UIHostingOrnament](/documentation/swiftui/uihostingornament)

#### Creating a hosting ornament

- [init(sceneAnchor:contentAlignment:content:)](/documentation/swiftui/uihostingornament/init(sceneanchor:contentalignment:content:))
- [var rootView: Content](/documentation/swiftui/uihostingornament/rootview)

#### Setting the alignment

- [var contentAlignment: Alignment](/documentation/swiftui/uihostingornament/contentalignment)
- [var sceneAnchor: UnitPoint](/documentation/swiftui/uihostingornament/sceneanchor)

#### Instance Properties

- [var contentAlignment3D: Alignment3D](/documentation/swiftui/uihostingornament/contentalignment3d)
- [UIOrnament](/documentation/swiftui/uiornament)
- [WatchKit integration](/documentation/swiftui/watchkit-integration)

### Displaying SwiftUI views in WatchKit

- [WKHostingController](/documentation/swiftui/wkhostingcontroller)

#### Creating a hosting controller object

- [init()](/documentation/swiftui/wkhostingcontroller/init())

#### Getting the root view

- [var body: Body](/documentation/swiftui/wkhostingcontroller/body)

#### Updating the root view

- [func updateBodyIfNeeded()](/documentation/swiftui/wkhostingcontroller/updatebodyifneeded())
- [func setNeedsBodyUpdate()](/documentation/swiftui/wkhostingcontroller/setneedsbodyupdate())
- [WKUserNotificationHostingController](/documentation/swiftui/wkusernotificationhostingcontroller)

#### Creating a hosting controller object

- [init()](/documentation/swiftui/wkusernotificationhostingcontroller/init())

#### Getting the root view

- [var body: Body](/documentation/swiftui/wkusernotificationhostingcontroller/body)

#### Configuring the notification

- [class var coalescedDescriptionFormat: String?](/documentation/swiftui/wkusernotificationhostingcontroller/coalesceddescriptionformat)
- [class var isInteractive: Bool](/documentation/swiftui/wkusernotificationhostingcontroller/isinteractive)
- [class var sashColor: Color?](/documentation/swiftui/wkusernotificationhostingcontroller/sashcolor)
- [class var subtitleColor: Color?](/documentation/swiftui/wkusernotificationhostingcontroller/subtitlecolor)
- [class var titleColor: Color?](/documentation/swiftui/wkusernotificationhostingcontroller/titlecolor)
- [class var wantsSashBlur: Bool](/documentation/swiftui/wkusernotificationhostingcontroller/wantssashblur)

### Adding WatchKit views to SwiftUI view hierarchies

- [WKInterfaceObjectRepresentable](/documentation/swiftui/wkinterfaceobjectrepresentable)

#### Creating and updating the interface object

- [func makeWKInterfaceObject(context: Self.Context) -> Self.WKInterfaceObjectType](/documentation/swiftui/wkinterfaceobjectrepresentable/makewkinterfaceobject(context:))
- [func updateWKInterfaceObject(Self.WKInterfaceObjectType, context: Self.Context)](/documentation/swiftui/wkinterfaceobjectrepresentable/updatewkinterfaceobject(_:context:))
- [WKInterfaceObjectRepresentable.Context](/documentation/swiftui/wkinterfaceobjectrepresentable/context)

#### Cleaning up the interface object

- [static func dismantleWKInterfaceObject(Self.WKInterfaceObjectType, coordinator: Self.Coordinator)](/documentation/swiftui/wkinterfaceobjectrepresentable/dismantlewkinterfaceobject(_:coordinator:))

#### Providing a custom coordinator object

- [func makeCoordinator() -> Self.Coordinator](/documentation/swiftui/wkinterfaceobjectrepresentable/makecoordinator())
- [Coordinator](/documentation/swiftui/wkinterfaceobjectrepresentable/coordinator)
- [WKInterfaceObjectType](/documentation/swiftui/wkinterfaceobjectrepresentable/wkinterfaceobjecttype)
- [WKInterfaceObjectRepresentableContext](/documentation/swiftui/wkinterfaceobjectrepresentablecontext)

#### Coordinating interactions

- [let coordinator: Representable.Coordinator](/documentation/swiftui/wkinterfaceobjectrepresentablecontext/coordinator)
- [var transaction: Transaction](/documentation/swiftui/wkinterfaceobjectrepresentablecontext/transaction)

#### Getting the current environment data

- [var environment: EnvironmentValues](/documentation/swiftui/wkinterfaceobjectrepresentablecontext/environment)
- [Technology-specific views](/documentation/swiftui/technology-specific-views)

### Displaying web content

- [WebView](/documentation/webkit/webview-swift.struct)
- [WebPage](/documentation/webkit/webpage)
- [func webViewBackForwardNavigationGestures(WebView.BackForwardNavigationGesturesBehavior) -> some View](/documentation/swiftui/view/webviewbackforwardnavigationgestures(_:))
- [func webViewContentBackground(Visibility) -> some View](/documentation/swiftui/view/webviewcontentbackground(_:))
- [func webViewContextMenu(menu: (WebView.ActivatedElementInfo) -> some View) -> some View](/documentation/swiftui/view/webviewcontextmenu(menu:))
- [func webViewElementFullscreenBehavior(WebView.ElementFullscreenBehavior) -> some View](/documentation/swiftui/view/webviewelementfullscreenbehavior(_:))
- [func webViewLinkPreviews(WebView.LinkPreviewBehavior) -> some View](/documentation/swiftui/view/webviewlinkpreviews(_:))
- [func webViewMagnificationGestures(WebView.MagnificationGesturesBehavior) -> some View](/documentation/swiftui/view/webviewmagnificationgestures(_:))
- [func webViewOnScrollGeometryChange<T>(for: T.Type, of: (ScrollGeometry) -> T, action: (T, T) -> Void) -> some View](/documentation/swiftui/view/webviewonscrollgeometrychange(for:of:action:))
- [func webViewScrollInputBehavior(ScrollInputBehavior, for: ScrollInputKind) -> some View](/documentation/swiftui/view/webviewscrollinputbehavior(_:for:))
- [func webViewScrollPosition(Binding<ScrollPosition>) -> some View](/documentation/swiftui/view/webviewscrollposition(_:))
- [func webViewTextSelection<S>(S) -> some View](/documentation/swiftui/view/webviewtextselection(_:))

### Accessing Apple Pay and Wallet

- [PayWithApplePayButton](/documentation/passkit/paywithapplepaybutton)
- [AddPassToWalletButton](/documentation/passkit/addpasstowalletbutton)
- [VerifyIdentityWithWalletButton](/documentation/passkit/verifyidentitywithwalletbutton)
- [func addOrderToWalletButtonStyle(AddOrderToWalletButtonStyle) -> some View](/documentation/swiftui/view/addordertowalletbuttonstyle(_:))
- [func addPassToWalletButtonStyle(AddPassToWalletButtonStyle) -> some View](/documentation/swiftui/view/addpasstowalletbuttonstyle(_:))
- [func onApplePayCouponCodeChange(perform: (String) async -> PKPaymentRequestCouponCodeUpdate) -> some View](/documentation/swiftui/view/onapplepaycouponcodechange(perform:))
- [func onApplePayPaymentMethodChange(perform: (PKPaymentMethod) async -> PKPaymentRequestPaymentMethodUpdate) -> some View](/documentation/swiftui/view/onapplepaypaymentmethodchange(perform:))
- [func onApplePayShippingContactChange(perform: (PKContact) async -> PKPaymentRequestShippingContactUpdate) -> some View](/documentation/swiftui/view/onapplepayshippingcontactchange(perform:))
- [func onApplePayShippingMethodChange(perform: (PKShippingMethod) async -> PKPaymentRequestShippingMethodUpdate) -> some View](/documentation/swiftui/view/onapplepayshippingmethodchange(perform:))
- [func payLaterViewAction(PayLaterViewAction) -> some View](/documentation/swiftui/view/paylaterviewaction(_:))
- [func payLaterViewDisplayStyle(PayLaterViewDisplayStyle) -> some View](/documentation/swiftui/view/paylaterviewdisplaystyle(_:))
- [func payWithApplePayButtonStyle(PayWithApplePayButtonStyle) -> some View](/documentation/swiftui/view/paywithapplepaybuttonstyle(_:))
- [func verifyIdentityWithWalletButtonStyle(VerifyIdentityWithWalletButtonStyle) -> some View](/documentation/swiftui/view/verifyidentitywithwalletbuttonstyle(_:))
- [AsyncShareablePassConfiguration](/documentation/passkit/asyncshareablepassconfiguration)
- [func transactionTask(CredentialTransaction.Configuration?, action: (CredentialTransaction) async -> Void) -> some View](/documentation/swiftui/view/transactiontask(_:action:))

### Authorizing and authenticating

- [LocalAuthenticationView](/documentation/localauthentication/localauthenticationview)
- [SignInWithAppleButton](/documentation/authenticationservices/signinwithapplebutton)
- [func signInWithAppleButtonStyle(SignInWithAppleButton.Style) -> some View](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))
- [var authorizationController: AuthorizationController](/documentation/swiftui/environmentvalues/authorizationcontroller)
- [var webAuthenticationSession: WebAuthenticationSession](/documentation/swiftui/environmentvalues/webauthenticationsession)

### Configuring Family Sharing

- [FamilyActivityPicker](/documentation/familycontrols/familyactivitypicker)
- [func familyActivityPicker(isPresented: Binding<Bool>, selection: Binding<FamilyActivitySelection>) -> some View](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:))
- [func familyActivityPicker(headerText: String?, footerText: String?, isPresented: Binding<Bool>, selection: Binding<FamilyActivitySelection>) -> some View](/documentation/swiftui/view/familyactivitypicker(headertext:footertext:ispresented:selection:))

### Reporting on device activity

- [DeviceActivityReport](/documentation/deviceactivity/deviceactivityreport)

### Working with managed devices

- [func managedContentStyle(ManagedContentStyle) -> some View](/documentation/swiftui/view/managedcontentstyle(_:))
- [func automatedDeviceEnrollmentAddition(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/automateddeviceenrollmentaddition(ispresented:))

### Creating graphics

- [Chart](/documentation/charts/chart)
- [SceneView](/documentation/scenekit/sceneview)
- [SpriteView](/documentation/spritekit/spriteview)

### Getting location information

- [LocationButton](/documentation/corelocationui/locationbutton)
- [Map](/documentation/mapkit/map)
- [func mapStyle(MapStyle) -> some View](/documentation/swiftui/view/mapstyle(_:))
- [func mapScope(Namespace.ID) -> some View](/documentation/swiftui/view/mapscope(_:))
- [func mapFeatureSelectionDisabled((MapFeature) -> Bool) -> some View](/documentation/swiftui/view/mapfeatureselectiondisabled(_:))
- [func mapFeatureSelectionAccessory(MapItemDetailSelectionAccessoryStyle?) -> some View](/documentation/swiftui/view/mapfeatureselectionaccessory(_:))
- [func mapFeatureSelectionContent(content: (MapFeature) -> some MapContent) -> some View](/documentation/swiftui/view/mapfeatureselectioncontent(content:))
- [func mapControls(() -> some View) -> some View](/documentation/swiftui/view/mapcontrols(_:))
- [func mapControlVisibility(Visibility) -> some View](/documentation/swiftui/view/mapcontrolvisibility(_:))
- [func mapCameraKeyframeAnimator(trigger: some Equatable, keyframes: (MapCamera) -> some Keyframes<MapCamera>) -> some View](/documentation/swiftui/view/mapcamerakeyframeanimator(trigger:keyframes:))
- [func lookAroundViewer(isPresented: Binding<Bool>, scene: Binding<MKLookAroundScene?>, allowsNavigation: Bool, showsRoadLabels: Bool, pointsOfInterest: PointOfInterestCategories, onDismiss: (() -> Void)?) -> some View](/documentation/swiftui/view/lookaroundviewer(ispresented:scene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func lookAroundViewer(isPresented: Binding<Bool>, initialScene: MKLookAroundScene?, allowsNavigation: Bool, showsRoadLabels: Bool, pointsOfInterest: PointOfInterestCategories, onDismiss: (() -> Void)?) -> some View](/documentation/swiftui/view/lookaroundviewer(ispresented:initialscene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func onMapCameraChange(frequency:_:)](/documentation/swiftui/view/onmapcamerachange(frequency:_:))
- [func mapItemDetailPopover(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor) -> some View](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge) -> some View](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailPopover(item: Binding<MKMapItem?>, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor) -> some View](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(item: Binding<MKMapItem?>, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge) -> some View](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailSheet(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool) -> some View](/documentation/swiftui/view/mapitemdetailsheet(ispresented:item:displaysmap:))
- [func mapItemDetailSheet(item: Binding<MKMapItem?>, displaysMap: Bool) -> some View](/documentation/swiftui/view/mapitemdetailsheet(item:displaysmap:))

### Displaying media

- [CameraView](/documentation/homekit/cameraview)
- [NowPlayingView](/documentation/watchkit/nowplayingview)
- [VideoPlayer](/documentation/avkit/videoplayer)
- [func continuityDevicePicker(isPresented: Binding<Bool>, onDidConnect: ((AVContinuityDevice?) -> Void)?) -> some View](/documentation/swiftui/view/continuitydevicepicker(ispresented:ondidconnect:))
- [func cameraAnchor(isActive: Bool) -> some View](/documentation/swiftui/view/cameraanchor(isactive:))

### Selecting photos

- [PhotosPicker](/documentation/photosui/photospicker)
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<PhotosPickerItem?>, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<PhotosPickerItem?>, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy, photoLibrary: PHPhotoLibrary) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:photolibrary:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<[PhotosPickerItem]>, maxSelectionCount: Int?, selectionBehavior: PhotosPickerSelectionBehavior, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<[PhotosPickerItem]>, maxSelectionCount: Int?, selectionBehavior: PhotosPickerSelectionBehavior, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy, photoLibrary: PHPhotoLibrary) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:photolibrary:))
- [func photosPickerAccessoryVisibility(Visibility, edges: Edge.Set) -> some View](/documentation/swiftui/view/photospickeraccessoryvisibility(_:edges:))
- [func photosPickerDisabledCapabilities(PHPickerCapabilities) -> some View](/documentation/swiftui/view/photospickerdisabledcapabilities(_:))
- [func photosPickerStyle(PhotosPickerStyle) -> some View](/documentation/swiftui/view/photospickerstyle(_:))

### Previewing content

- [func quickLookPreview(Binding<URL?>) -> some View](/documentation/swiftui/view/quicklookpreview(_:))
- [func quickLookPreview<Items>(Binding<Items.Element?>, in: Items) -> some View](/documentation/swiftui/view/quicklookpreview(_:in:))

### Interacting with networked devices

- [DevicePicker](/documentation/devicediscoveryui/devicepicker)
- [var devicePickerSupports: DevicePickerSupportedAction](/documentation/swiftui/environmentvalues/devicepickersupports)

### Configuring a Live Activity

- [func activitySystemActionForegroundColor(Color?) -> some View](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:))
- [func activityBackgroundTint(Color?) -> some View](/documentation/swiftui/view/activitybackgroundtint(_:))
- [var isActivityFullscreen: Bool](/documentation/swiftui/environmentvalues/isactivityfullscreen)
- [var activityFamily: ActivityFamily](/documentation/swiftui/environmentvalues/activityfamily)

### Interacting with the App Store and Apple Music

- [func appStoreOverlay(isPresented: Binding<Bool>, configuration: () -> SKOverlay.Configuration) -> some View](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:))
- [func manageSubscriptionsSheet(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/managesubscriptionssheet(ispresented:))
- [func refundRequestSheet(for: Transaction.ID, isPresented: Binding<Bool>, onDismiss: ((Result<Transaction.RefundRequestStatus, Transaction.RefundRequestError>) -> ())?) -> some View](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:))
- [func offerCodeRedemption(isPresented: Binding<Bool>, onCompletion: (Result<Void, any Error>) -> Void) -> some View](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:))
- [func musicSubscriptionOffer(isPresented: Binding<Bool>, options: MusicSubscriptionOffer.Options, onLoadCompletion: ((any Error)?) -> Void) -> some View](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))
- [func currentEntitlementTask(for: String, priority: TaskPriority, action: (EntitlementTaskState<VerificationResult<Transaction>?>) async -> ()) -> some View](/documentation/swiftui/view/currententitlementtask(for:priority:action:))
- [func inAppPurchaseOptions(((Product) async -> Set<Product.PurchaseOption>)?) -> some View](/documentation/swiftui/view/inapppurchaseoptions(_:))
- [func manageSubscriptionsSheet(isPresented: Binding<Bool>, subscriptionGroupID: String) -> some View](/documentation/swiftui/view/managesubscriptionssheet(ispresented:subscriptiongroupid:))
- [func onInAppPurchaseCompletion(perform: ((Product, Result<Product.PurchaseResult, any Error>) async -> ())?) -> some View](/documentation/swiftui/view/oninapppurchasecompletion(perform:))
- [func onInAppPurchaseStart(perform: ((Product) async -> ())?) -> some View](/documentation/swiftui/view/oninapppurchasestart(perform:))
- [func productIconBorder() -> some View](/documentation/swiftui/view/producticonborder())
- [func productViewStyle(some ProductViewStyle) -> some View](/documentation/swiftui/view/productviewstyle(_:))
- [func productDescription(Visibility) -> some View](/documentation/swiftui/view/productdescription(_:))
- [func storeButton(Visibility, for: StoreButtonKind...) -> some View](/documentation/swiftui/view/storebutton(_:for:))
- [func storeProductTask(for: Product.ID, priority: TaskPriority, action: (Product.TaskState) async -> ()) -> some View](/documentation/swiftui/view/storeproducttask(for:priority:action:))
- [func storeProductsTask(for: some Collection<String> & Equatable & Sendable, priority: TaskPriority, action: (Product.CollectionTaskState) async -> ()) -> some View](/documentation/swiftui/view/storeproductstask(for:priority:action:))
- [func subscriptionStatusTask(for: String, priority: TaskPriority, action: (EntitlementTaskState<[Product.SubscriptionInfo.Status]>) async -> ()) -> some View](/documentation/swiftui/view/subscriptionstatustask(for:priority:action:))
- [func subscriptionStoreButtonLabel(SubscriptionStoreButtonLabel) -> some View](/documentation/swiftui/view/subscriptionstorebuttonlabel(_:))
- [func subscriptionStoreControlIcon(icon: (Product, Product.SubscriptionInfo) -> some View) -> some View](/documentation/swiftui/view/subscriptionstorecontrolicon(icon:))
- [func subscriptionStoreControlStyle(some SubscriptionStoreControlStyle) -> some View](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:))
- [func subscriptionStoreControlStyle<S>(S, placement: S.Placement) -> some View](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:placement:))
- [func subscriptionStoreOptionGroupStyle(some SubscriptionOptionGroupStyle) -> some View](/documentation/swiftui/view/subscriptionstoreoptiongroupstyle(_:))
- [func subscriptionStorePickerItemBackground(some ShapeStyle) -> some View](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:))
- [func subscriptionStorePickerItemBackground(some ShapeStyle, in: some Shape) -> some View](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:in:))
- [func subscriptionStorePolicyDestination(for: SubscriptionStorePolicyKind, destination: () -> some View) -> some View](/documentation/swiftui/view/subscriptionstorepolicydestination(for:destination:))
- [func subscriptionStorePolicyDestination(url: URL, for: SubscriptionStorePolicyKind) -> some View](/documentation/swiftui/view/subscriptionstorepolicydestination(url:for:))
- [func subscriptionStorePolicyForegroundStyle(some ShapeStyle) -> some View](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:))
- [func subscriptionStorePolicyForegroundStyle(some ShapeStyle, some ShapeStyle) -> some View](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:_:))
- [func subscriptionStoreSignInAction((() -> ())?) -> some View](/documentation/swiftui/view/subscriptionstoresigninaction(_:))
- [func subscriptionStoreControlBackground(_:)](/documentation/swiftui/view/subscriptionstorecontrolbackground(_:))
- [func subscriptionPromotionalOffer(offer: (Product, Product.SubscriptionInfo) -> Product.SubscriptionOffer?, signature: (Product, Product.SubscriptionInfo, Product.SubscriptionOffer) async throws -> Product.SubscriptionOffer.Signature) -> some View](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:signature:))
- [func preferredSubscriptionOffer((Product, Product.SubscriptionInfo, [Product.SubscriptionOffer]) -> Product.SubscriptionOffer?) -> some View](/documentation/swiftui/view/preferredsubscriptionoffer(_:))

### Accessing health data

- [func healthDataAccessRequest(store: HKHealthStore, objectType: HKObjectType, predicate: NSPredicate?, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:objecttype:predicate:trigger:completion:))
- [func healthDataAccessRequest(store: HKHealthStore, readTypes: Set<HKObjectType>, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:readtypes:trigger:completion:))
- [func healthDataAccessRequest(store: HKHealthStore, shareTypes: Set<HKSampleType>, readTypes: Set<HKObjectType>?, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:sharetypes:readtypes:trigger:completion:))
- [func workoutPreview(WorkoutPlan, isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/workoutpreview(_:ispresented:))

### Providing tips

- [func popoverTip((any Tip)?, arrowEdge: Edge?, action: (Tips.Action) -> Void) -> some View](/documentation/swiftui/view/popovertip(_:arrowedge:action:))
- [func tipBackground<S>(S) -> some View](/documentation/swiftui/view/tipbackground(_:))
- [func tipCornerRadius(CGFloat, antialiased: Bool) -> some View](/documentation/swiftui/view/tipcornerradius(_:antialiased:))
- [func tipImageSize(CGSize) -> some View](/documentation/swiftui/view/tipimagesize(_:))
- [func tipViewStyle(some TipViewStyle) -> some View](/documentation/swiftui/view/tipviewstyle(_:))
- [func tipImageStyle<S>(S) -> some View](/documentation/swiftui/view/tipimagestyle(_:))
- [func tipImageStyle<S1, S2>(S1, S2) -> some View](/documentation/swiftui/view/tipimagestyle(_:_:))
- [func tipImageStyle<S1, S2, S3>(S1, S2, S3) -> some View](/documentation/swiftui/view/tipimagestyle(_:_:_:))

### Showing a translation

- [func translationPresentation(isPresented: Binding<Bool>, text: String, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge, replacementAction: ((String) -> Void)?) -> some View](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:))
- [func translationTask(TranslationSession.Configuration?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(_:action:))
- [func translationTask(source: Locale.Language?, target: Locale.Language?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(source:target:action:))
- [func translationTask(source: Locale.Language?, target: Locale.Language?, preferredStrategy: TranslationSession.Strategy, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(source:target:preferredstrategy:action:))

### Presenting journaling suggestions

- [func journalingSuggestionsPicker(isPresented: Binding<Bool>, onCompletion: (JournalingSuggestion) async -> Void) -> some View](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:oncompletion:))

### Managing contact access

- [func contactAccessButtonCaption(ContactAccessButton.Caption) -> some View](/documentation/swiftui/view/contactaccessbuttoncaption(_:))
- [func contactAccessButtonStyle(ContactAccessButton.Style) -> some View](/documentation/swiftui/view/contactaccessbuttonstyle(_:))
- [func contactAccessPicker(isPresented: Binding<Bool>, completionHandler: ([String]) -> Void) -> some View](/documentation/swiftui/view/contactaccesspicker(ispresented:completionhandler:))

### Handling game controller events

- [func handlesGameControllerEvents(matching: GCUIEventTypes) -> some View](/documentation/swiftui/view/handlesgamecontrollerevents(matching:))

### Creating a tabletop game

- [func tabletopGame(TabletopGame, parent: Entity, automaticUpdate: Bool) -> some View](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:))
- [func tabletopGame(TabletopGame, parent: Entity, automaticUpdate: Bool, interaction: (TabletopInteraction.Value) -> any TabletopInteraction.Delegate) -> some View](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:interaction:))

### Configuring camera controls

- [var realityViewCameraControls: CameraControls](/documentation/swiftui/environmentvalues/realityviewcameracontrols)
- [func realityViewCameraControls(CameraControls) -> some View](/documentation/swiftui/view/realityviewcameracontrols(_:))

### Interacting with transactions

- [func transactionPicker(isPresented: Binding<Bool>, selection: Binding<[Transaction]>) -> some View](/documentation/swiftui/view/transactionpicker(ispresented:selection:))

## Tool support

- [Previews in Xcode](/documentation/swiftui/previews-in-xcode)

### Essentials

- [Previewing your app’s interface in Xcode](/documentation/xcode/previewing-your-apps-interface-in-xcode)

### Creating a preview

- [macro Preview(String?, body: () -> any View)](/documentation/swiftui/preview(_:body:))
- [macro Preview(String?, traits: PreviewTrait<Preview.ViewTraits>, PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:traits:_:body:))
- [macro Preview(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:traits:body:cameras:))

### Creating a preview in the context of a scene

- [macro Preview<Style>(String?, immersionStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:immersionstyle:traits:body:))
- [macro Preview<Style>(String?, immersionStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:immersionstyle:traits:body:cameras:))
- [macro Preview<Style>(String?, windowStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:windowstyle:traits:body:))
- [macro Preview<Style>(String?, windowStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:windowstyle:traits:body:cameras:))

### Defining a preview

- [macro Previewable()](/documentation/swiftui/previewable())
- [PreviewProvider](/documentation/swiftui/previewprovider)

#### Creating a preview

- [static var previews: Self.Previews](/documentation/swiftui/previewprovider/previews-swift.type.property)
- [Previews](/documentation/swiftui/previewprovider/previews-swift.associatedtype)

#### Specifying the platform

- [static var platform: PreviewPlatform?](/documentation/swiftui/previewprovider/platform)
- [PreviewPlatform](/documentation/swiftui/previewplatform)

#### Getting an operating system

- [case iOS](/documentation/swiftui/previewplatform/ios)
- [case macOS](/documentation/swiftui/previewplatform/macos)
- [case tvOS](/documentation/swiftui/previewplatform/tvos)
- [case watchOS](/documentation/swiftui/previewplatform/watchos)
- [func previewDisplayName(String?) -> some View](/documentation/swiftui/view/previewdisplayname(_:))
- [PreviewModifier](/documentation/swiftui/previewmodifier)

#### Associated Types

- [Body](/documentation/swiftui/previewmodifier/body)
- [Context](/documentation/swiftui/previewmodifier/context)

#### Instance Methods

- [func body(content: Self.Content, context: Self.Context) -> Self.Body](/documentation/swiftui/previewmodifier/body(content:context:))

#### Type Aliases

- [PreviewModifier.Content](/documentation/swiftui/previewmodifier/content)

#### Type Methods

- [static func makeSharedContext() async throws -> Self.Context](/documentation/swiftui/previewmodifier/makesharedcontext())
- [PreviewModifierContent](/documentation/swiftui/previewmodifiercontent)

### Customizing a preview

- [func previewDevice(PreviewDevice?) -> some View](/documentation/swiftui/view/previewdevice(_:))
- [PreviewDevice](/documentation/swiftui/previewdevice)
- [func previewLayout(PreviewLayout) -> some View](/documentation/swiftui/view/previewlayout(_:))
- [func previewInterfaceOrientation(InterfaceOrientation) -> some View](/documentation/swiftui/view/previewinterfaceorientation(_:))
- [InterfaceOrientation](/documentation/swiftui/interfaceorientation)

#### Getting an orientation

- [static let portrait: InterfaceOrientation](/documentation/swiftui/interfaceorientation/portrait)
- [static let portraitUpsideDown: InterfaceOrientation](/documentation/swiftui/interfaceorientation/portraitupsidedown)
- [static let landscapeLeft: InterfaceOrientation](/documentation/swiftui/interfaceorientation/landscapeleft)
- [static let landscapeRight: InterfaceOrientation](/documentation/swiftui/interfaceorientation/landscaperight)

### Setting a context

- [func previewContext<C>(C) -> some View](/documentation/swiftui/view/previewcontext(_:))
- [PreviewContext](/documentation/swiftui/previewcontext)

#### Accessing a preview context

- [subscript<Key>(Key.Type) -> Key.Value](/documentation/swiftui/previewcontext/subscript(_:))
- [PreviewContextKey](/documentation/swiftui/previewcontextkey)

#### Setting a default

- [static var defaultValue: Self.Value](/documentation/swiftui/previewcontextkey/defaultvalue)
- [Value](/documentation/swiftui/previewcontextkey/value)

### Building in debug mode

- [DebugReplaceableView](/documentation/swiftui/debugreplaceableview)
- [Xcode library customization](/documentation/swiftui/xcode-library-customization)

### Creating library items

- [LibraryContentProvider](/documentation/developertoolssupport/librarycontentprovider)
- [LibraryItem](/documentation/developertoolssupport/libraryitem)
- [Performance analysis](/documentation/swiftui/performance-analysis)

### Essentials

- [Understanding user interface responsiveness](/documentation/xcode/understanding-user-interface-responsiveness)
- [Understanding hangs in your app](/documentation/xcode/understanding-hangs-in-your-app)
- [Understanding hitches in your app](/documentation/xcode/understanding-hitches-in-your-app)

### Analyzing SwiftUI performance

- [Understanding and improving SwiftUI performance](/documentation/xcode/understanding-and-improving-swiftui-performance)

