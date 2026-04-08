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
- [NSHostingController](/documentation/swiftui/nshostingcontroller) — embed SwiftUI in AppKit via NSViewController; [NSHostingSizingOptions](/documentation/swiftui/nshostingsizingoptions)
- [NSHostingView](/documentation/swiftui/nshostingview) — embed SwiftUI in AppKit NSView
- [NSHostingMenu](/documentation/swiftui/nshostingmenu) — NSMenu from SwiftUI views
- [NSHostingSceneRepresentation](/documentation/swiftui/nshostingscenerepresentation) — SwiftUI scene in AppKit; [NSHostingSceneBridgingOptions](/documentation/swiftui/nshostingscenebridgingoptions)

### Adding AppKit views to SwiftUI view hierarchies

- [NSViewRepresentable](/documentation/swiftui/nsviewrepresentable) — wrap AppKit NSView for SwiftUI; [Context](/documentation/swiftui/nsviewrepresentablecontext)
- [NSViewControllerRepresentable](/documentation/swiftui/nsviewcontrollerrepresentable) — wrap AppKit NSViewController for SwiftUI; [Context](/documentation/swiftui/nsviewcontrollerrepresentablecontext)

### Adding AppKit gesture recognizers into SwiftUI view hierarchies

- [NSGestureRecognizerRepresentable](/documentation/swiftui/nsgesturerecognizerrepresentable) — wrap AppKit gesture recognizer for SwiftUI; [Context](/documentation/swiftui/nsgesturerecognizerrepresentablecontext), [CoordinateSpaceConverter](/documentation/swiftui/nsgesturerecognizerrepresentablecoordinatespaceconverter)

- [UIKit integration](/documentation/swiftui/uikit-integration) (article)

### Displaying SwiftUI views in UIKit

- [Using SwiftUI with UIKit](/documentation/uikit/using-swiftui-with-uikit) (article)
- [Unifying your app's animations](/documentation/swiftui/unifying-your-app-s-animations) (article)
- [UIHostingController](/documentation/swiftui/uihostingcontroller) — embed SwiftUI in UIKit view controller; [UIHostingControllerSizingOptions](/documentation/swiftui/uihostingcontrollersizingoptions)
- [UIHostingConfiguration](/documentation/swiftui/uihostingconfiguration) — SwiftUI as UICollectionView/UITableView cell content
- [UIHostingSceneDelegate](/documentation/swiftui/uihostingscenedelegate) — UIScene delegate hosting SwiftUI scenes

### Adding UIKit views to SwiftUI view hierarchies

- [UIViewRepresentable](/documentation/swiftui/uiviewrepresentable) — wrap UIKit UIView for SwiftUI; [Context](/documentation/swiftui/uiviewrepresentablecontext)
- [UIViewControllerRepresentable](/documentation/swiftui/uiviewcontrollerrepresentable) — wrap UIKit UIViewController for SwiftUI; [Context](/documentation/swiftui/uiviewcontrollerrepresentablecontext)

### Adding UIKit gesture recognizers into SwiftUI view hierarchies

- [UIGestureRecognizerRepresentable](/documentation/swiftui/uigesturerecognizerrepresentable) — wrap UIKit gesture recognizer for SwiftUI; [Context](/documentation/swiftui/uigesturerecognizerrepresentablecontext), [CoordinateSpaceConverter](/documentation/swiftui/uigesturerecognizerrepresentablecoordinatespaceconverter)

### Sharing configuration / Hosting ornaments

- [UITraitBridgedEnvironmentKey](/documentation/swiftui/uitraitbridgedenvironmentkey) — bridge UIKit traits and SwiftUI environment values
- [UIHostingOrnament](/documentation/swiftui/uihostingornament) — host SwiftUI ornament in UIKit (visionOS); [UIOrnament](/documentation/swiftui/uiornament)

- [WatchKit integration](/documentation/swiftui/watchkit-integration) (article)

### Displaying SwiftUI views in WatchKit

- [WKHostingController](/documentation/swiftui/wkhostingcontroller) — embed SwiftUI in WatchKit; [WKUserNotificationHostingController](/documentation/swiftui/wkusernotificationhostingcontroller) — notification interface

### Adding WatchKit views to SwiftUI view hierarchies

- [WKInterfaceObjectRepresentable](/documentation/swiftui/wkinterfaceobjectrepresentable) — wrap WatchKit interface object for SwiftUI; [Context](/documentation/swiftui/wkinterfaceobjectrepresentablecontext)

- [Technology-specific views](/documentation/swiftui/technology-specific-views) (article)

### Displaying web content

- [WebView](/documentation/webkit/webview-swift.struct) — SwiftUI wrapper for web content (WebKit)
- [WebPage](/documentation/webkit/webpage) — web page model
- View modifiers: [webViewBackForwardNavigationGestures(_:)](/documentation/swiftui/view/webviewbackforwardnavigationgestures(_:)), [webViewContentBackground(_:)](/documentation/swiftui/view/webviewcontentbackground(_:)), [webViewContextMenu(menu:)](/documentation/swiftui/view/webviewcontextmenu(menu:)), [webViewElementFullscreenBehavior(_:)](/documentation/swiftui/view/webviewelementfullscreenbehavior(_:)), [webViewLinkPreviews(_:)](/documentation/swiftui/view/webviewlinkpreviews(_:)), [webViewMagnificationGestures(_:)](/documentation/swiftui/view/webviewmagnificationgestures(_:)), [webViewOnScrollGeometryChange(for:of:action:)](/documentation/swiftui/view/webviewonscrollgeometrychange(for:of:action:)), [webViewScrollInputBehavior(_:for:)](/documentation/swiftui/view/webviewscrollinputbehavior(_:for:)), [webViewScrollPosition(_:)](/documentation/swiftui/view/webviewscrollposition(_:)), [webViewTextSelection(_:)](/documentation/swiftui/view/webviewtextselection(_:))

### Accessing Apple Pay and Wallet

- Buttons: [PayWithApplePayButton](/documentation/passkit/paywithapplepaybutton), [AddPassToWalletButton](/documentation/passkit/addpasstowalletbutton), [VerifyIdentityWithWalletButton](/documentation/passkit/verifyidentitywithwalletbutton); [AsyncShareablePassConfiguration](/documentation/passkit/asyncshareablepassconfiguration)
- Button styles: [addOrderToWalletButtonStyle(_:)](/documentation/swiftui/view/addordertowalletbuttonstyle(_:)), [addPassToWalletButtonStyle(_:)](/documentation/swiftui/view/addpasstowalletbuttonstyle(_:)), [payWithApplePayButtonStyle(_:)](/documentation/swiftui/view/paywithapplepaybuttonstyle(_:)), [verifyIdentityWithWalletButtonStyle(_:)](/documentation/swiftui/view/verifyidentitywithwalletbuttonstyle(_:))
- Apple Pay callbacks: [onApplePayCouponCodeChange(perform:)](/documentation/swiftui/view/onapplepaycouponcodechange(perform:)), [onApplePayPaymentMethodChange](/documentation/swiftui/view/onapplepaypaymentmethodchange(perform:)), [onApplePayShippingContactChange](/documentation/swiftui/view/onapplepayshippingcontactchange(perform:)), [onApplePayShippingMethodChange](/documentation/swiftui/view/onapplepayshippingmethodchange(perform:))
- [payLaterViewAction(_:)](/documentation/swiftui/view/paylaterviewaction(_:)), [payLaterViewDisplayStyle(_:)](/documentation/swiftui/view/paylaterviewdisplaystyle(_:)), [transactionTask(_:action:)](/documentation/swiftui/view/transactiontask(_:action:))

### Authorizing and authenticating

- [LocalAuthenticationView](/documentation/localauthentication/localauthenticationview) — biometric/passcode auth; [SignInWithAppleButton](/documentation/authenticationservices/signinwithapplebutton), [signInWithAppleButtonStyle(_:)](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))
- [var authorizationController](/documentation/swiftui/environmentvalues/authorizationcontroller), [var webAuthenticationSession](/documentation/swiftui/environmentvalues/webauthenticationsession)

### Configuring Family Sharing

- [FamilyActivityPicker](/documentation/familycontrols/familyactivitypicker); [familyActivityPicker(isPresented:selection:)](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:)) — also headerText:footerText: variant

### Reporting on device activity / Working with managed devices

- [DeviceActivityReport](/documentation/deviceactivity/deviceactivityreport); [managedContentStyle(_:)](/documentation/swiftui/view/managedcontentstyle(_:)), [automatedDeviceEnrollmentAddition(isPresented:)](/documentation/swiftui/view/automateddeviceenrollmentaddition(ispresented:))

### Creating graphics

- [Chart](/documentation/charts/chart), [SceneView](/documentation/scenekit/sceneview), [SpriteView](/documentation/spritekit/spriteview) — Charts, SceneKit, SpriteKit

### Getting location information

- [LocationButton](/documentation/corelocationui/locationbutton) — one-time location access button
- [Map](/documentation/mapkit/map) — MapKit map view
- [func mapStyle(_:)](/documentation/swiftui/view/mapstyle(_:)), [mapScope(_:)](/documentation/swiftui/view/mapscope(_:))
- [func mapFeatureSelectionDisabled(_:)](/documentation/swiftui/view/mapfeatureselectiondisabled(_:)), [mapFeatureSelectionAccessory(_:)](/documentation/swiftui/view/mapfeatureselectionaccessory(_:)), [mapFeatureSelectionContent(content:)](/documentation/swiftui/view/mapfeatureselectioncontent(content:))
- [func mapControls(_:)](/documentation/swiftui/view/mapcontrols(_:)), [mapControlVisibility(_:)](/documentation/swiftui/view/mapcontrolvisibility(_:))
- [mapCameraKeyframeAnimator(trigger:keyframes:)](/documentation/swiftui/view/mapcamerakeyframeanimator(trigger:keyframes:)), [onMapCameraChange(frequency:_:)](/documentation/swiftui/view/onmapcamerachange(frequency:_:))
- [lookAroundViewer(isPresented:scene:...)](/documentation/swiftui/view/lookaroundviewer(ispresented:scene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:)) — also initialScene: variant
- [mapItemDetailPopover(isPresented:item:displaysMap:attachmentAnchor:)](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:)) — also arrowEdge:, binding variants; [mapItemDetailSheet](/documentation/swiftui/view/mapitemdetailsheet(ispresented:item:displaysmap:))

### Displaying media

- [CameraView](/documentation/homekit/cameraview) (HomeKit), [NowPlayingView](/documentation/watchkit/nowplayingview) (WatchKit), [VideoPlayer](/documentation/avkit/videoplayer) (AVKit)
- [continuityDevicePicker(isPresented:onDidConnect:)](/documentation/swiftui/view/continuitydevicepicker(ispresented:ondidconnect:)), [cameraAnchor(isActive:)](/documentation/swiftui/view/cameraanchor(isactive:))

### Selecting photos

- [PhotosPicker](/documentation/photosui/photospicker) — system photo picker
- [func photosPicker(isPresented:selection:matching:preferredItemEncoding:)](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:)) — single; also photoLibrary:, multi (maxSelectionCount:selectionBehavior:) variants
- [func photosPickerAccessoryVisibility(_:edges:)](/documentation/swiftui/view/photospickeraccessoryvisibility(_:edges:)), [photosPickerDisabledCapabilities(_:)](/documentation/swiftui/view/photospickerdisabledcapabilities(_:)), [photosPickerStyle(_:)](/documentation/swiftui/view/photospickerstyle(_:))

### Previewing content

- [quickLookPreview(_:)](/documentation/swiftui/view/quicklookpreview(_:)), [quickLookPreview(_:in:)](/documentation/swiftui/view/quicklookpreview(_:in:)) — Quick Look preview

### Interacting with networked devices

- [DevicePicker](/documentation/devicediscoveryui/devicepicker) — discover nearby devices; [var devicePickerSupports](/documentation/swiftui/environmentvalues/devicepickersupports)

### Configuring a Live Activity

- [activitySystemActionForegroundColor(_:)](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:)), [activityBackgroundTint(_:)](/documentation/swiftui/view/activitybackgroundtint(_:))
- [var isActivityFullscreen](/documentation/swiftui/environmentvalues/isactivityfullscreen), [var activityFamily](/documentation/swiftui/environmentvalues/activityfamily)

### Interacting with the App Store and Apple Music

- Overlays/sheets: [appStoreOverlay(isPresented:configuration:)](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:)), [manageSubscriptionsSheet(isPresented:)](/documentation/swiftui/view/managesubscriptionssheet(ispresented:)), [refundRequestSheet(for:isPresented:onDismiss:)](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:)), [offerCodeRedemption(isPresented:onCompletion:)](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:)), [musicSubscriptionOffer(isPresented:options:onLoadCompletion:)](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))
- IAP: [currentEntitlementTask(for:priority:action:)](/documentation/swiftui/view/currententitlementtask(for:priority:action:)), [inAppPurchaseOptions(_:)](/documentation/swiftui/view/inapppurchaseoptions(_:)), [onInAppPurchaseCompletion(perform:)](/documentation/swiftui/view/oninapppurchasecompletion(perform:)), [onInAppPurchaseStart(perform:)](/documentation/swiftui/view/oninapppurchasestart(perform:))
- Product: [productIconBorder()](/documentation/swiftui/view/producticonborder()), [productViewStyle(_:)](/documentation/swiftui/view/productviewstyle(_:)), [productDescription(_:)](/documentation/swiftui/view/productdescription(_:))
- Store: [storeButton(_:for:)](/documentation/swiftui/view/storebutton(_:for:)), [storeProductTask(for:priority:action:)](/documentation/swiftui/view/storeproducttask(for:priority:action:)), [storeProductsTask(for:priority:action:)](/documentation/swiftui/view/storeproductstask(for:priority:action:))
- [func subscriptionStatusTask(for:priority:action:)](/documentation/swiftui/view/subscriptionstatustask(for:priority:action:))
- Subscription store: [subscriptionStoreButtonLabel(_:)](/documentation/swiftui/view/subscriptionstorebuttonlabel(_:)), [subscriptionStoreControlIcon(icon:)](/documentation/swiftui/view/subscriptionstorecontrolicon(icon:)), [subscriptionStoreControlStyle(_:)](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:)), [subscriptionStoreControlBackground(_:)](/documentation/swiftui/view/subscriptionstorecontrolbackground(_:)), [subscriptionStoreOptionGroupStyle(_:)](/documentation/swiftui/view/subscriptionstoreoptiongroupstyle(_:))
- Subscription store extras: [subscriptionStorePickerItemBackground(_:)](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:)), [subscriptionStorePolicyDestination(for:destination:)](/documentation/swiftui/view/subscriptionstorepolicydestination(for:destination:)), [subscriptionStorePolicyForegroundStyle(_:)](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:)), [subscriptionStoreSignInAction(_:)](/documentation/swiftui/view/subscriptionstoresigninaction(_:))
- Offers: [subscriptionPromotionalOffer(offer:signature:)](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:signature:)), [preferredSubscriptionOffer(_:)](/documentation/swiftui/view/preferredsubscriptionoffer(_:))

### Accessing health data

- [func healthDataAccessRequest(store:objectType:predicate:trigger:completion:)](/documentation/swiftui/view/healthdataaccessrequest(store:objecttype:predicate:trigger:completion:)) — also readTypes:, shareTypes:readTypes: variants
- [func workoutPreview(_:isPresented:)](/documentation/swiftui/view/workoutpreview(_:ispresented:))

### Providing tips

- [popoverTip(_:arrowEdge:action:)](/documentation/swiftui/view/popovertip(_:arrowedge:action:)), [tipBackground(_:)](/documentation/swiftui/view/tipbackground(_:)), [tipCornerRadius(_:antialiased:)](/documentation/swiftui/view/tipcornerradius(_:antialiased:)), [tipImageSize(_:)](/documentation/swiftui/view/tipimagesize(_:)), [tipViewStyle(_:)](/documentation/swiftui/view/tipviewstyle(_:)), [tipImageStyle(_:)](/documentation/swiftui/view/tipimagestyle(_:))

### Showing a translation

- [translationPresentation(isPresented:text:attachmentAnchor:arrowEdge:replacementAction:)](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:)), [translationTask(_:action:)](/documentation/swiftui/view/translationtask(_:action:)) — also source:target: variants

### Presenting journaling suggestions

- [func journalingSuggestionsPicker(isPresented:onCompletion:)](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:oncompletion:))

### Managing contact access

- [contactAccessButtonCaption(_:)](/documentation/swiftui/view/contactaccessbuttoncaption(_:)), [contactAccessButtonStyle(_:)](/documentation/swiftui/view/contactaccessbuttonstyle(_:)), [contactAccessPicker(isPresented:completionHandler:)](/documentation/swiftui/view/contactaccesspicker(ispresented:completionhandler:))

### Games, camera, and transactions

- [func handlesGameControllerEvents(matching:)](/documentation/swiftui/view/handlesgamecontrollerevents(matching:)), [tabletopGame(_:parent:automaticUpdate:)](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:)) — also interaction: variant
- [var realityViewCameraControls](/documentation/swiftui/environmentvalues/realityviewcameracontrols), [func realityViewCameraControls(_:)](/documentation/swiftui/view/realityviewcameracontrols(_:))
- [func transactionPicker(isPresented:selection:)](/documentation/swiftui/view/transactionpicker(ispresented:selection:))

---
## Tool support

- [Previews in Xcode](/documentation/swiftui/previews-in-xcode) (article)

### Essentials

- [Previewing your app's interface in Xcode](/documentation/xcode/previewing-your-apps-interface-in-xcode) (article)

### Creating a preview

- [macro Preview(_:body:)](/documentation/swiftui/preview(_:body:)) — also traits:, cameras: variants
- [macro Preview(_:immersionStyle:traits:body:)](/documentation/swiftui/preview(_:immersionstyle:traits:body:)) — scene context; also cameras:, windowStyle: variants

### Defining a preview

- [macro Previewable()](/documentation/swiftui/previewable()) — make @State usable in #Preview; [func previewDisplayName(_:)](/documentation/swiftui/view/previewdisplayname(_:))
- [PreviewProvider](/documentation/swiftui/previewprovider) — legacy preview protocol; [PreviewPlatform](/documentation/swiftui/previewplatform) — iOS, macOS, tvOS, watchOS
- [PreviewModifier](/documentation/swiftui/previewmodifier) — inject shared context; [PreviewModifierContent](/documentation/swiftui/previewmodifiercontent)

### Customizing a preview

- [func previewDevice(_:)](/documentation/swiftui/view/previewdevice(_:)), [previewLayout(_:)](/documentation/swiftui/view/previewlayout(_:)), [previewInterfaceOrientation(_:)](/documentation/swiftui/view/previewinterfaceorientation(_:))
- [PreviewDevice](/documentation/swiftui/previewdevice), [InterfaceOrientation](/documentation/swiftui/interfaceorientation) — portrait, portraitUpsideDown, landscapeLeft, landscapeRight
- [func previewContext(_:)](/documentation/swiftui/view/previewcontext(_:)), [PreviewContext](/documentation/swiftui/previewcontext), [PreviewContextKey](/documentation/swiftui/previewcontextkey)

### Building in debug mode

- [DebugReplaceableView](/documentation/swiftui/debugreplaceableview) — placeholder view replaced at runtime in debug
- [Xcode library customization](/documentation/swiftui/xcode-library-customization) (article)
- [LibraryContentProvider](/documentation/developertoolssupport/librarycontentprovider), [LibraryItem](/documentation/developertoolssupport/libraryitem) — Xcode library items

### Analyzing SwiftUI performance

- [Performance analysis](/documentation/swiftui/performance-analysis) (article)
- [Understanding user interface responsiveness](/documentation/xcode/understanding-user-interface-responsiveness) (article), [Understanding hangs](/documentation/xcode/understanding-hangs-in-your-app) (article), [Understanding hitches](/documentation/xcode/understanding-hitches-in-your-app) (article)
- [Understanding and improving SwiftUI performance](/documentation/xcode/understanding-and-improving-swiftui-performance) (article)
