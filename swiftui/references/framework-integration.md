# Framework Integration — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Framework integration](#framework-integration) — AppKit, UIKit, WatchKit bridging; web, maps, media, StoreKit, HealthKit, etc.
- [Tool support](#tool-support) — Xcode previews, library items, performance analysis

---
## Framework integration

- [AppKit integration](/documentation/swiftui/appkit-integration) (article)

### Displaying SwiftUI views in AppKit

- [Unifying your app's animations](/documentation/swiftui/unifying-your-app-s-animations) (article)
- [NSHostingController](/documentation/swiftui/nshostingcontroller) — embed SwiftUI view hierarchy in an AppKit window via NSViewController
- [NSHostingView](/documentation/swiftui/nshostingview) — embed SwiftUI view hierarchy in an AppKit NSView
- [NSHostingMenu](/documentation/swiftui/nshostingmenu) — create AppKit NSMenu from SwiftUI views
- [NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions) — sizing options for NSHostingController/NSHostingView
- [NSHostingSceneRepresentation](/documentation/swiftui/nshostingscenerepresentation) — represent a SwiftUI scene in AppKit
- [NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions) — control what scene properties bridge to AppKit

### Adding AppKit views to SwiftUI view hierarchies

- [NSViewRepresentable](/documentation/swiftui/nsviewrepresentable) — protocol to wrap an AppKit NSView for use in SwiftUI
- [NSViewRepresentableContext](/documentation/swiftui/nsviewrepresentablecontext) — context for NSViewRepresentable updates
- [NSViewControllerRepresentable](/documentation/swiftui/nsviewcontrollerrepresentable) — protocol to wrap an AppKit NSViewController for use in SwiftUI
- [NSViewControllerRepresentableContext](/documentation/swiftui/nsviewcontrollerrepresentablecontext) — context for NSViewControllerRepresentable updates

### Adding AppKit gesture recognizers into SwiftUI view hierarchies

- [NSGestureRecognizerRepresentable](/documentation/swiftui/nsgesturerecognizerrepresentable) — protocol to wrap AppKit gesture recognizer for SwiftUI
- [NSGestureRecognizerRepresentableContext](/documentation/swiftui/nsgesturerecognizerrepresentablecontext) — context for gesture recognizer updates
- [NSGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter) — coordinate space conversion

- [UIKit integration](/documentation/swiftui/uikit-integration) (article)

### Displaying SwiftUI views in UIKit

- [Using SwiftUI with UIKit](/documentation/uikit/using-swiftui-with-uikit) (article)
- [Unifying your app's animations](/documentation/swiftui/unifying-your-app-s-animations) (article)
- [UIHostingController](/documentation/swiftui/uihostingcontroller) — embed SwiftUI view hierarchy in a UIKit view controller
- [UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontrollersizingoptions) — sizing options for UIHostingController
- [UIHostingConfiguration](/documentation/swiftui/uihostingconfiguration) — use SwiftUI views as UICollectionView/UITableView cell content
- [UIHostingSceneDelegate](/documentation/swiftui/uihostingscenedelegate) — protocol for UIScene delegate hosting SwiftUI scenes

### Adding UIKit views to SwiftUI view hierarchies

- [UIViewRepresentable](/documentation/swiftui/uiviewrepresentable) — protocol to wrap a UIKit UIView for use in SwiftUI
- [UIViewRepresentableContext](/documentation/swiftui/uiviewrepresentablecontext) — context for UIViewRepresentable updates
- [UIViewControllerRepresentable](/documentation/swiftui/uiviewcontrollerrepresentable) — protocol to wrap a UIKit UIViewController for use in SwiftUI
- [UIViewControllerRepresentableContext](/documentation/swiftui/uiviewcontrollerrepresentablecontext) — context for UIViewControllerRepresentable updates

### Adding UIKit gesture recognizers into SwiftUI view hierarchies

- [UIGestureRecognizerRepresentable](/documentation/swiftui/uigesturerecognizerrepresentable) — protocol to wrap UIKit gesture recognizer for SwiftUI
- [UIGestureRecognizerRepresentableContext](/documentation/swiftui/uigesturerecognizerrepresentablecontext) — context for gesture recognizer updates
- [UIGestureRecognizerRepresentableCoordinateSpaceConverter](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter) — coordinate space conversion

### Sharing configuration information

- [UITraitBridgedEnvironmentKey](/documentation/swiftui/uitraitbridgedenvironmentkey) — protocol to bridge UIKit traits and SwiftUI environment values

### Hosting an ornament in UIKit

- [UIHostingOrnament](/documentation/swiftui/uihostingornament) — host SwiftUI ornament content in UIKit (visionOS)
- [UIOrnament](/documentation/swiftui/uiornament) — UIKit ornament base

- [WatchKit integration](/documentation/swiftui/watchkit-integration) (article)

### Displaying SwiftUI views in WatchKit

- [WKHostingController](/documentation/swiftui/wkhostingcontroller) — embed SwiftUI view in a WatchKit interface controller
- [WKUserNotificationHostingController](/documentation/swiftui/wkusernotificationhostingcontroller) — host SwiftUI views in WatchKit notification interface

### Adding WatchKit views to SwiftUI view hierarchies

- [WKInterfaceObjectRepresentable](/documentation/swiftui/wkinterfaceobjectrepresentable) — protocol to wrap WatchKit interface object for SwiftUI
- [WKInterfaceObjectRepresentableContext](/documentation/swiftui/wkinterfaceobjectrepresentablecontext) — context for WKInterfaceObjectRepresentable updates

- [Technology-specific views](/documentation/swiftui/technology-specific-views) (article)

### Displaying web content

- [WebView](/documentation/webkit/webview-swift.struct) — SwiftUI wrapper for web content (WebKit)
- [WebPage](/documentation/webkit/webpage) — web page model
- View modifiers: [webViewBackForwardNavigationGestures(_:)](/documentation/swiftui/view/webviewbackforwardnavigationgestures(_:)), [webViewContentBackground(_:)](/documentation/swiftui/view/webviewcontentbackground(_:)), [webViewContextMenu(menu:)](/documentation/swiftui/view/webviewcontextmenu(menu:)), [webViewElementFullscreenBehavior(_:)](/documentation/swiftui/view/webviewelementfullscreenbehavior(_:)), [webViewLinkPreviews(_:)](/documentation/swiftui/view/webviewlinkpreviews(_:)), [webViewMagnificationGestures(_:)](/documentation/swiftui/view/webviewmagnificationgestures(_:)), [webViewOnScrollGeometryChange(for:of:action:)](/documentation/swiftui/view/webviewonscrollgeometrychange(for:of:action:)), [webViewScrollInputBehavior(_:for:)](/documentation/swiftui/view/webviewscrollinputbehavior(_:for:)), [webViewScrollPosition(_:)](/documentation/swiftui/view/webviewscrollposition(_:)), [webViewTextSelection(_:)](/documentation/swiftui/view/webviewtextselection(_:))

### Accessing Apple Pay and Wallet

- [PayWithApplePayButton](/documentation/passkit/paywithapplepaybutton) — Apple Pay payment button
- [AddPassToWalletButton](/documentation/passkit/addpasstowalletbutton) — add pass to Wallet button
- [VerifyIdentityWithWalletButton](/documentation/passkit/verifyidentitywithwalletbutton) — identity verification button
- [AsyncShareablePassConfiguration](/documentation/passkit/asyncshareablepassconfiguration) — async shareable pass config
- [func addOrderToWalletButtonStyle(_:)](/documentation/swiftui/view/addordertowalletbuttonstyle(_:))
- [func addPassToWalletButtonStyle(_:)](/documentation/swiftui/view/addpasstowalletbuttonstyle(_:))
- [func onApplePayCouponCodeChange(perform:)](/documentation/swiftui/view/onapplepaycouponcodechange(perform:)), [onApplePayPaymentMethodChange](/documentation/swiftui/view/onapplepaypaymentmethodchange(perform:)), [onApplePayShippingContactChange](/documentation/swiftui/view/onapplepayshippingcontactchange(perform:)), [onApplePayShippingMethodChange](/documentation/swiftui/view/onapplepayshippingmethodchange(perform:))
- [func payLaterViewAction(_:)](/documentation/swiftui/view/paylaterviewaction(_:)), [payLaterViewDisplayStyle(_:)](/documentation/swiftui/view/paylaterviewdisplaystyle(_:))
- [func payWithApplePayButtonStyle(_:)](/documentation/swiftui/view/paywithapplepaybuttonstyle(_:))
- [func verifyIdentityWithWalletButtonStyle(_:)](/documentation/swiftui/view/verifyidentitywithwalletbuttonstyle(_:))
- [func transactionTask(_:action:)](/documentation/swiftui/view/transactiontask(_:action:)) — credential transaction task

### Authorizing and authenticating

- [LocalAuthenticationView](/documentation/localauthentication/localauthenticationview) — biometric/passcode authentication view
- [SignInWithAppleButton](/documentation/authenticationservices/signinwithapplebutton) — Sign in with Apple button
- [func signInWithAppleButtonStyle(_:)](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))
- [var authorizationController: AuthorizationController](/documentation/swiftui/environmentvalues/authorizationcontroller)
- [var webAuthenticationSession: WebAuthenticationSession](/documentation/swiftui/environmentvalues/webauthenticationsession)

### Configuring Family Sharing

- [FamilyActivityPicker](/documentation/familycontrols/familyactivitypicker) — pick family activity restrictions
- [func familyActivityPicker(isPresented:selection:)](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:)) — also headerText:footerText: variant

### Reporting on device activity

- [DeviceActivityReport](/documentation/deviceactivity/deviceactivityreport) — display device activity report

### Working with managed devices

- [func managedContentStyle(_:)](/documentation/swiftui/view/managedcontentstyle(_:))
- [func automatedDeviceEnrollmentAddition(isPresented:)](/documentation/swiftui/view/automateddeviceenrollmentaddition(ispresented:))

### Creating graphics

- [Chart](/documentation/charts/chart) — Swift Charts chart view
- [SceneView](/documentation/scenekit/sceneview) — SceneKit 3D scene view
- [SpriteView](/documentation/spritekit/spriteview) — SpriteKit 2D sprite view

### Getting location information

- [LocationButton](/documentation/corelocationui/locationbutton) — one-time location access button
- [Map](/documentation/mapkit/map) — MapKit map view
- [func mapStyle(_:)](/documentation/swiftui/view/mapstyle(_:))
- [func mapScope(_:)](/documentation/swiftui/view/mapscope(_:))
- [func mapFeatureSelectionDisabled(_:)](/documentation/swiftui/view/mapfeatureselectiondisabled(_:)), [mapFeatureSelectionAccessory(_:)](/documentation/swiftui/view/mapfeatureselectionaccessory(_:)), [mapFeatureSelectionContent(content:)](/documentation/swiftui/view/mapfeatureselectioncontent(content:))
- [func mapControls(_:)](/documentation/swiftui/view/mapcontrols(_:)), [mapControlVisibility(_:)](/documentation/swiftui/view/mapcontrolvisibility(_:))
- [func mapCameraKeyframeAnimator(trigger:keyframes:)](/documentation/swiftui/view/mapcamerakeyframeanimator(trigger:keyframes:))
- [func lookAroundViewer(isPresented:scene:...)](/documentation/swiftui/view/lookaroundviewer(ispresented:scene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:)) — also initialScene: variant
- [func onMapCameraChange(frequency:_:)](/documentation/swiftui/view/onmapcamerachange(frequency:_:))
- [func mapItemDetailPopover(isPresented:item:displaysMap:attachmentAnchor:)](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:)) — also arrowEdge:, item: binding variants
- [func mapItemDetailSheet(isPresented:item:displaysMap:)](/documentation/swiftui/view/mapitemdetailsheet(ispresented:item:displaysmap:)) — also item: binding variant

### Displaying media

- [CameraView](/documentation/homekit/cameraview) — HomeKit camera feed view
- [NowPlayingView](/documentation/watchkit/nowplayingview) — WatchKit now-playing interface
- [VideoPlayer](/documentation/avkit/videoplayer) — AVKit video player view
- [func continuityDevicePicker(isPresented:onDidConnect:)](/documentation/swiftui/view/continuitydevicepicker(ispresented:ondidconnect:))
- [func cameraAnchor(isActive:)](/documentation/swiftui/view/cameraanchor(isactive:))

### Selecting photos

- [PhotosPicker](/documentation/photosui/photospicker) — system photo picker
- [func photosPicker(isPresented:selection:matching:preferredItemEncoding:)](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:)) — single; also photoLibrary:, multi (maxSelectionCount:selectionBehavior:) variants
- [func photosPickerAccessoryVisibility(_:edges:)](/documentation/swiftui/view/photospickeraccessoryvisibility(_:edges:))
- [func photosPickerDisabledCapabilities(_:)](/documentation/swiftui/view/photospickerdisabledcapabilities(_:))
- [func photosPickerStyle(_:)](/documentation/swiftui/view/photospickerstyle(_:))

### Previewing content

- [func quickLookPreview(_:)](/documentation/swiftui/view/quicklookpreview(_:)) — Quick Look single file
- [func quickLookPreview(_:in:)](/documentation/swiftui/view/quicklookpreview(_:in:)) — Quick Look file in collection

### Interacting with networked devices

- [DevicePicker](/documentation/devicediscoveryui/devicepicker) — discover and pick nearby devices
- [var devicePickerSupports: DevicePickerSupportedAction](/documentation/swiftui/environmentvalues/devicepickersupports)

### Configuring a Live Activity

- [func activitySystemActionForegroundColor(_:)](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:))
- [func activityBackgroundTint(_:)](/documentation/swiftui/view/activitybackgroundtint(_:))
- [var isActivityFullscreen: Bool](/documentation/swiftui/environmentvalues/isactivityfullscreen)
- [var activityFamily: ActivityFamily](/documentation/swiftui/environmentvalues/activityfamily)

### Interacting with the App Store and Apple Music

- [func appStoreOverlay(isPresented:configuration:)](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:))
- [func manageSubscriptionsSheet(isPresented:)](/documentation/swiftui/view/managesubscriptionssheet(ispresented:)) — also subscriptionGroupID: variant
- [func refundRequestSheet(for:isPresented:onDismiss:)](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:))
- [func offerCodeRedemption(isPresented:onCompletion:)](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:))
- [func musicSubscriptionOffer(isPresented:options:onLoadCompletion:)](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))
- [func currentEntitlementTask(for:priority:action:)](/documentation/swiftui/view/currententitlementtask(for:priority:action:))
- [func inAppPurchaseOptions(_:)](/documentation/swiftui/view/inapppurchaseoptions(_:))
- [func onInAppPurchaseCompletion(perform:)](/documentation/swiftui/view/oninapppurchasecompletion(perform:))
- [func onInAppPurchaseStart(perform:)](/documentation/swiftui/view/oninapppurchasestart(perform:))
- [func productIconBorder()](/documentation/swiftui/view/producticonborder())
- [func productViewStyle(_:)](/documentation/swiftui/view/productviewstyle(_:))
- [func productDescription(_:)](/documentation/swiftui/view/productdescription(_:))
- [func storeButton(_:for:)](/documentation/swiftui/view/storebutton(_:for:))
- [func storeProductTask(for:priority:action:)](/documentation/swiftui/view/storeproducttask(for:priority:action:))
- [func storeProductsTask(for:priority:action:)](/documentation/swiftui/view/storeproductstask(for:priority:action:))
- [func subscriptionStatusTask(for:priority:action:)](/documentation/swiftui/view/subscriptionstatustask(for:priority:action:))
- [func subscriptionStoreButtonLabel(_:)](/documentation/swiftui/view/subscriptionstorebuttonlabel(_:))
- [func subscriptionStoreControlIcon(icon:)](/documentation/swiftui/view/subscriptionstorecontrolicon(icon:))
- [func subscriptionStoreControlStyle(_:)](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:)) — also placement: variant
- [func subscriptionStoreOptionGroupStyle(_:)](/documentation/swiftui/view/subscriptionstoreoptiongroupstyle(_:))
- [func subscriptionStorePickerItemBackground(_:)](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:)) — also in: shape variant
- [func subscriptionStorePolicyDestination(for:destination:)](/documentation/swiftui/view/subscriptionstorepolicydestination(for:destination:)) — also url:for: variant
- [func subscriptionStorePolicyForegroundStyle(_:)](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:)) — also 2-style variant
- [func subscriptionStoreSignInAction(_:)](/documentation/swiftui/view/subscriptionstoresigninaction(_:))
- [func subscriptionStoreControlBackground(_:)](/documentation/swiftui/view/subscriptionstorecontrolbackground(_:))
- [func subscriptionPromotionalOffer(offer:signature:)](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:signature:))
- [func preferredSubscriptionOffer(_:)](/documentation/swiftui/view/preferredsubscriptionoffer(_:))

### Accessing health data

- [func healthDataAccessRequest(store:objectType:predicate:trigger:completion:)](/documentation/swiftui/view/healthdataaccessrequest(store:objecttype:predicate:trigger:completion:)) — also readTypes:, shareTypes:readTypes: variants
- [func workoutPreview(_:isPresented:)](/documentation/swiftui/view/workoutpreview(_:ispresented:))

### Providing tips

- [func popoverTip(_:arrowEdge:action:)](/documentation/swiftui/view/popovertip(_:arrowedge:action:))
- [func tipBackground(_:)](/documentation/swiftui/view/tipbackground(_:))
- [func tipCornerRadius(_:antialiased:)](/documentation/swiftui/view/tipcornerradius(_:antialiased:))
- [func tipImageSize(_:)](/documentation/swiftui/view/tipimagesize(_:))
- [func tipViewStyle(_:)](/documentation/swiftui/view/tipviewstyle(_:))
- [func tipImageStyle(_:)](/documentation/swiftui/view/tipimagestyle(_:)) — also 2- and 3-style overloads

### Showing a translation

- [func translationPresentation(isPresented:text:attachmentAnchor:arrowEdge:replacementAction:)](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:))
- [func translationTask(_:action:)](/documentation/swiftui/view/translationtask(_:action:)) — config-based; also source:target: and source:target:preferredStrategy: variants

### Presenting journaling suggestions

- [func journalingSuggestionsPicker(isPresented:onCompletion:)](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:oncompletion:))

### Managing contact access

- [func contactAccessButtonCaption(_:)](/documentation/swiftui/view/contactaccessbuttoncaption(_:))
- [func contactAccessButtonStyle(_:)](/documentation/swiftui/view/contactaccessbuttonstyle(_:))
- [func contactAccessPicker(isPresented:completionHandler:)](/documentation/swiftui/view/contactaccesspicker(ispresented:completionhandler:))

### Handling game controller events

- [func handlesGameControllerEvents(matching:)](/documentation/swiftui/view/handlesgamecontrollerevents(matching:))

### Creating a tabletop game

- [func tabletopGame(_:parent:automaticUpdate:)](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:)) — also interaction: variant

### Configuring camera controls

- [var realityViewCameraControls: CameraControls](/documentation/swiftui/environmentvalues/realityviewcameracontrols)
- [func realityViewCameraControls(_:)](/documentation/swiftui/view/realityviewcameracontrols(_:))

### Interacting with transactions

- [func transactionPicker(isPresented:selection:)](/documentation/swiftui/view/transactionpicker(ispresented:selection:))

---
## Tool support

- [Previews in Xcode](/documentation/swiftui/previews-in-xcode) (article)

### Essentials

- [Previewing your app's interface in Xcode](/documentation/xcode/previewing-your-apps-interface-in-xcode) (article)

### Creating a preview

- [macro Preview(_:body:)](/documentation/swiftui/preview(_:body:))
- [macro Preview(_:traits:_:body:)](/documentation/swiftui/preview(_:traits:_:body:)) — with traits
- [macro Preview(_:traits:body:cameras:)](/documentation/swiftui/preview(_:traits:body:cameras:)) — with cameras

### Creating a preview in the context of a scene

- [macro Preview(_:immersionStyle:traits:body:)](/documentation/swiftui/preview(_:immersionstyle:traits:body:)) — also cameras: variant
- [macro Preview(_:windowStyle:traits:body:)](/documentation/swiftui/preview(_:windowstyle:traits:body:)) — also cameras: variant

### Defining a preview

- [macro Previewable()](/documentation/swiftui/previewable()) — make @State usable in #Preview
- [PreviewProvider](/documentation/swiftui/previewprovider) — protocol for legacy preview definitions
- [PreviewPlatform](/documentation/swiftui/previewplatform) — target platform for preview (iOS, macOS, tvOS, watchOS)
- [func previewDisplayName(_:)](/documentation/swiftui/view/previewdisplayname(_:))
- [PreviewModifier](/documentation/swiftui/previewmodifier) — protocol to inject shared context into previews
- [PreviewModifierContent](/documentation/swiftui/previewmodifiercontent) — content type for PreviewModifier

### Customizing a preview

- [func previewDevice(_:)](/documentation/swiftui/view/previewdevice(_:))
- [PreviewDevice](/documentation/swiftui/previewdevice) — device specifier for previews
- [func previewLayout(_:)](/documentation/swiftui/view/previewlayout(_:))
- [func previewInterfaceOrientation(_:)](/documentation/swiftui/view/previewinterfaceorientation(_:))
- [InterfaceOrientation](/documentation/swiftui/interfaceorientation) — portrait, portraitUpsideDown, landscapeLeft, landscapeRight

### Setting a context

- [func previewContext(_:)](/documentation/swiftui/view/previewcontext(_:))
- [PreviewContext](/documentation/swiftui/previewcontext) — key-value context for previews
- [PreviewContextKey](/documentation/swiftui/previewcontextkey) — define custom preview context keys

### Building in debug mode

- [DebugReplaceableView](/documentation/swiftui/debugreplaceableview) — placeholder view replaced at runtime in debug
- [Xcode library customization](/documentation/swiftui/xcode-library-customization) (article)

### Creating library items

- [LibraryContentProvider](/documentation/developertoolssupport/librarycontentprovider) — provide custom items to Xcode library
- [LibraryItem](/documentation/developertoolssupport/libraryitem) — single Xcode library entry

- [Performance analysis](/documentation/swiftui/performance-analysis) (article)

### Essentials

- [Understanding user interface responsiveness](/documentation/xcode/understanding-user-interface-responsiveness) (article)
- [Understanding hangs in your app](/documentation/xcode/understanding-hangs-in-your-app) (article)
- [Understanding hitches in your app](/documentation/xcode/understanding-hitches-in-your-app) (article)

### Analyzing SwiftUI performance

- [Understanding and improving SwiftUI performance](/documentation/xcode/understanding-and-improving-swiftui-performance) (article)
