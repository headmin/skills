# Views: Text and Images — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Alerts and dialogs](#alerts-and-dialogs)
- [Sheets and popovers](#sheets-and-popovers)
- [File dialogs](#file-dialogs)
- [Inspectors and previews](#inspectors-and-previews)
- [Framework integrations](#framework-integrations)
- [State and identity](#state-and-identity)
- [Environment and preferences](#environment-and-preferences)
- [Modifying a view](#modifying-a-view)
- [View life cycle](#view-life-cycle)
- [View hierarchy](#view-hierarchy)
- [Supporting view types](#supporting-view-types)
- [Hiding views and elements](#hiding-views-and-elements)
- [View interaction](#view-interaction)
- [Appearance](#appearance)
- [Passthrough and redaction](#passthrough-and-redaction)
- [Liquid Glass](#liquid-glass)
- [Styling buttons](#styling-buttons)
- [Additional view modifiers](#additional-view-modifiers)

---

### Alerts and dialogs

- [alert(_:isPresented:actions:)](/documentation/swiftui/view/alert(_:ispresented:actions:)) — also presenting:, error:, message: variants
- [alert(_:isPresented:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:actions:message:)) — also presenting:, error: variants
- [confirmationDialog(_:isPresented:titleVisibility:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:)) — also presenting:, message: variants
- [dismissalConfirmationDialog(_:shouldPresent:actions:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:)) — also message: variant
- [dialogIcon(_:)](/documentation/swiftui/view/dialogicon(_:)), [dialogSeverity(_:)](/documentation/swiftui/view/dialogseverity(_:)), [dialogSuppressionToggle](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:))

### Sheets and popovers

- [sheet(isPresented:onDismiss:content:)](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:)) — also item: variant
- [fullScreenCover(isPresented:onDismiss:content:)](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:)) — also item: variant
- [popover(isPresented:attachmentAnchor:arrowEdge:content:)](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:)) — also item: variant
- [interactiveDismissDisabled(_:)](/documentation/swiftui/view/interactivedismissdisabled(_:))
- presentationDetents, presentationDragIndicator, presentationBackground, presentationBackgroundInteraction, presentationCompactAdaptation, presentationContentInteraction, presentationCornerRadius, presentationSizing — [base path](/documentation/swiftui/view/presentationdetents(_:))

### File dialogs

- [fileExporter](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:)) — 6 overloads: document/documents/item/items with contentType(s), also [fileExporterFilenameLabel](/documentation/swiftui/view/fileexporterfilenamelabel(_:))
- [fileImporter](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:)) — single/multiple selection, with/without onCancellation
- [fileMover](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:)) — file/files, with/without onCancellation
- fileDialogBrowserOptions, fileDialogConfirmationLabel, fileDialogCustomizationID, fileDialogDefaultDirectory, fileDialogImportsUnresolvedAliases, fileDialogMessage, fileDialogURLEnabled — [base path](/documentation/swiftui/view/filedialogbrowseroptions(_:))

### Inspectors and previews

- [inspector(isPresented:content:)](/documentation/swiftui/view/inspector(ispresented:content:)), [inspectorColumnWidth](/documentation/swiftui/view/inspectorcolumnwidth(_:))
- [quickLookPreview(_:)](/documentation/swiftui/view/quicklookpreview(_:)) — also in: variant

### Framework integrations

- **Family Sharing**: [familyActivityPicker](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:)) — 3 overloads
- **Live Activities**: [activitySystemActionForegroundColor](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:)), [activityBackgroundTint](/documentation/swiftui/view/activitybackgroundtint(_:))
- **Apple Music**: [musicSubscriptionOffer](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))
- **StoreKit**: [appStoreOverlay](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:)), [manageSubscriptionsSheet](/documentation/swiftui/view/managesubscriptionssheet(ispresented:)), [refundRequestSheet](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:)), [offerCodeRedemption](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:))
- **PhotoKit**: [photosPicker](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:)) — 4 overloads; photosPickerAccessoryVisibility, photosPickerDisabledCapabilities, photosPickerStyle
- **Translation**: [translationPresentation](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:)), [translationTask](/documentation/swiftui/view/translationtask(_:action:)) — 3 overloads
- [State modifiers](/documentation/swiftui/view-state)

### State and identity

- [tag(_:includeOptional:)](/documentation/swiftui/view/tag(_:includeoptional:)), [id(_:)](/documentation/swiftui/view/id(_:)), [equatable()](/documentation/swiftui/view/equatable())

### Environment and preferences

- [environment(_:)](/documentation/swiftui/view/environment(_:)), [environment(_:_:)](/documentation/swiftui/view/environment(_:_:)), [environmentObject(_:)](/documentation/swiftui/view/environmentobject(_:)), [transformEnvironment(_:transform:)](/documentation/swiftui/view/transformenvironment(_:transform:))
- [preference(key:value:)](/documentation/swiftui/view/preference(key:value:)), [transformPreference](/documentation/swiftui/view/transformpreference(_:_:)), [anchorPreference](/documentation/swiftui/view/anchorpreference(key:value:transform:)), [transformAnchorPreference](/documentation/swiftui/view/transformanchorpreference(key:value:transform:))
- [onPreferenceChange(_:perform:)](/documentation/swiftui/view/onpreferencechange(_:perform:)), [backgroundPreferenceValue](/documentation/swiftui/view/backgroundpreferencevalue(_:_:)), [overlayPreferenceValue](/documentation/swiftui/view/overlaypreferencevalue(_:_:))
- [defaultAppStorage(_:)](/documentation/swiftui/view/defaultappstorage(_:))
- [modelContext(_:)](/documentation/swiftui/view/modelcontext(_:)), [modelContainer(_:)](/documentation/swiftui/view/modelcontainer(_:)), [modelContainer(for:inMemory:...)](/documentation/swiftui/view/modelcontainer(for:inmemory:isautosaveenabled:isundoenabled:onsetup:))

### Deprecated modifiers [deprecated]

- [Deprecated modifiers](/documentation/swiftui/view-deprecated)
- accessibility(label:, value:, hidden:, identifier:, selectionIdentifier:, hint:, activationPoint:, inputLabels:, addTraits:, removeTraits:, sortPriority:) — use accessibilityLabel etc.
- colorScheme, listRowPlatterColor, foregroundColor, complicationForeground, accentColor, mask, animation, cornerRadius [deprecated]
- autocapitalization, disableAutocorrection [deprecated]
- navigationBarTitle, navigationBarItems, navigationBarHidden, statusBar(hidden:), contextMenu [deprecated]
- menuButtonStyle, navigationViewStyle, frame(), edgesIgnoringSafeArea, coordinateSpace(name:) [deprecated]
- onChange(of:perform:), onTapGesture(coordinateSpace:), onLongPressGesture(old), onPasteCommand(of:), onDrop(of:), focusable(onFocusChange:), onContinuousHover(coordinateSpace:) [deprecated]
- actionSheet, alert(isPresented:content:), alert(item:content:), searchable(old), tabItem [deprecated]

### Modifying a view

- [Configuring views](/documentation/swiftui/configuring-views) (article)
- [Reducing view modifier maintenance](/documentation/swiftui/reducing-view-modifier-maintenance) (article)
- [modifier(_:)](/documentation/swiftui/view/modifier(_:))
- [ViewModifier](/documentation/swiftui/viewmodifier) — protocol; body(content:), animation(_:), concat(_:), transaction(_:)
- [EmptyModifier](/documentation/swiftui/emptymodifier) — no-op; static identity
- [ModifiedContent](/documentation/swiftui/modifiedcontent) — pairs content + modifier; mirrors View accessibility methods [deprecated]
- [EnvironmentalModifier](/documentation/swiftui/environmentalmodifier) — resolve(in:), ResolvedModifier
- [ViewBuilder](/documentation/swiftui/viewbuilder) — result builder; buildBlock, buildExpression, buildEither, buildIf, buildLimitedAvailability

### Manipulation modifiers (visionOS)

- [Manipulable](/documentation/swiftui/manipulable) — Event (phase, value), GestureState, Inertia (none/low/medium/high), InputDevice (chirality, kind, pose), Operation (primaryRotation/scale/secondaryRotation/translate)
- Modifier types: [ManipulableModifier](/documentation/swiftui/manipulablemodifier), ManipulableResponderModifier, ManipulableTransformBindingModifier, ManipulationGeometryModifier, ManipulationGestureModifier, ManipulationUsingGestureStateModifier

### View life cycle

- [onAppear(perform:)](/documentation/swiftui/view/onappear(perform:)), [onDisappear(perform:)](/documentation/swiftui/view/ondisappear(perform:))

### View hierarchy

- [id(_:)](/documentation/swiftui/view/id(_:)), [tag(_:includeOptional:)](/documentation/swiftui/view/tag(_:includeoptional:)), [equatable()](/documentation/swiftui/view/equatable())

### Supporting view types

- [AnyView](/documentation/swiftui/anyview) — type-erased view
- [EmptyView](/documentation/swiftui/emptyview) — no content
- [EquatableView](/documentation/swiftui/equatableview) — skips re-render when equal
- [SubscriptionView](/documentation/swiftui/subscriptionview) — subscribes to publisher
- [TupleView](/documentation/swiftui/tupleview) — groups multiple views
- [View configuration](/documentation/swiftui/view-configuration) (article)

### Hiding views and elements

- [opacity(_:)](/documentation/swiftui/view/opacity(_:)), [hidden()](/documentation/swiftui/view/hidden())
- [labelsHidden()](/documentation/swiftui/view/labelshidden()), [labelsVisibility(_:)](/documentation/swiftui/view/labelsvisibility(_:)), [menuIndicator(_:)](/documentation/swiftui/view/menuindicator(_:)), [statusBarHidden(_:)](/documentation/swiftui/view/statusbarhidden(_:)), [persistentSystemOverlays(_:)](/documentation/swiftui/view/persistentsystemoverlays(_:))
- [Visibility](/documentation/swiftui/visibility) — automatic, visible, hidden

### View interaction

- [disabled(_:)](/documentation/swiftui/view/disabled(_:)), [isEnabled](/documentation/swiftui/environmentvalues/isenabled), [interactionActivityTrackingTag(_:)](/documentation/swiftui/view/interactionactivitytrackingtag(_:)), [invalidatableContent(_:)](/documentation/swiftui/view/invalidatablecontent(_:))
- [help(_:)](/documentation/swiftui/view/help(_:))

### Appearance

- [preferredColorScheme(_:)](/documentation/swiftui/view/preferredcolorscheme(_:)), [colorScheme](/documentation/swiftui/environmentvalues/colorscheme)
- [ColorScheme](/documentation/swiftui/colorscheme) — light, dark
- [colorSchemeContrast](/documentation/swiftui/environmentvalues/colorschemecontrast), [ColorSchemeContrast](/documentation/swiftui/colorschemecontrast) — standard, increased

### Passthrough and redaction

- [preferredSurroundingsEffect(_:)](/documentation/swiftui/view/preferredsurroundingseffect(_:)), [SurroundingsEffect](/documentation/swiftui/surroundingseffect) — systemDark, dark, semiDark, ultraDark, colorMultiply, dim
- [BreakthroughEffect](/documentation/swiftui/breakthrougheffect) — automatic, none, prominent, subtle
- [privacySensitive(_:)](/documentation/swiftui/view/privacysensitive(_:)), [redacted(reason:)](/documentation/swiftui/view/redacted(reason:)), [unredacted()](/documentation/swiftui/view/unredacted())
- [RedactionReasons](/documentation/swiftui/redactionreasons) — invalidated, placeholder, privacy
- [redactionReasons](/documentation/swiftui/environmentvalues/redactionreasons), [isSceneCaptured](/documentation/swiftui/environmentvalues/isscenecaptured)
- [Designing your app for the Always On state](/documentation/watchos-apps/designing-your-app-for-the-always-on-state) (article)
- [View styles](/documentation/swiftui/view-styles) (article)

### Liquid Glass

- [Applying Liquid Glass to custom views](/documentation/swiftui/applying-liquid-glass-to-custom-views) (article)
- [Landmarks: Building an app with Liquid Glass](/documentation/swiftui/landmarks-building-an-app-with-liquid-glass) (article)
- Landmarks articles: [background extension](/documentation/swiftui/landmarks-applying-a-background-extension-effect), [scrolling under sidebar](/documentation/swiftui/landmarks-extending-horizontal-scrolling-under-a-sidebar-or-inspector), [glass in toolbars](/documentation/swiftui/landmarks-refining-the-system-provided-glass-effect-in-toolbars), [activity badges](/documentation/swiftui/landmarks-displaying-custom-activity-badges) (articles)
- [glassEffect(_:in:)](/documentation/swiftui/view/glasseffect(_:in:)), [Glass.interactive(_:)](/documentation/swiftui/glass/interactive(_:))
- [GlassEffectContainer](/documentation/swiftui/glasseffectcontainer), [GlassEffectTransition](/documentation/swiftui/glasseffecttransition) — identity, matchedGeometry, materialize
- [GlassButtonStyle](/documentation/swiftui/glassbuttonstyle), [GlassProminentButtonStyle](/documentation/swiftui/glassprominentbuttonstyle), [DefaultGlassEffectShape](/documentation/swiftui/defaultglasseffectshape)

### Styling buttons

- [buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [ButtonStyle](/documentation/swiftui/buttonstyle) — protocol; makeBody(configuration:)
- [ButtonStyleConfiguration](/documentation/swiftui/buttonstyleconfiguration) — label, isPressed, role
- [PrimitiveButtonStyle](/documentation/swiftui/primitivebuttonstyle) — automatic, accessoryBar, accessoryBarAction, bordered, borderedProminent, borderless, card, glass, glassProminent, link, plain

### Additional view modifiers

Modifiers on View (path prefix: `/documentation/swiftui/view/`):

**Accessibility**: accessibilityActions(category:_:), accessibilityDefaultFocus(_:_:), accessibilityScrollStatus(_:isEnabled:)
**App Store / StoreKit**: appStoreMerchandising, inAppPurchaseOptions, onInAppPurchaseCompletion, onInAppPurchaseStart, currentEntitlementTask, storeButton, storeProductTask, storeProductsTask, productDescription, productIconBorder, productViewStyle
**Subscription Store**: subscriptionIntroductoryOffer, subscriptionOfferViewButtonVisibility, subscriptionOfferViewDetailAction, subscriptionOfferViewStyle, subscriptionPromotionalOffer, subscriptionStatusTask, subscriptionStoreButtonLabel, subscriptionStoreControlBackground, subscriptionStoreControlIcon, subscriptionStoreControlStyle, subscriptionStoreOptionGroupStyle, subscriptionStorePickerItemBackground, subscriptionStorePolicyDestination, subscriptionStorePolicyForegroundStyle, subscriptionStoreSignInAction, preferredSubscriptionOffer, preferredSubscriptionPricingTerms, manageSubscriptionsSheet(isPresented:subscriptionGroupID:)
**Apple Pay**: onApplePayCouponCodeChange, onApplePayPaymentMethodChange, onApplePayShippingContactChange, onApplePayShippingMethodChange, payLaterViewAction, payLaterViewDisplayStyle, payWithApplePayButtonDisableCardArt, payWithApplePayButtonStyle
**Wallet**: addOrderToWalletButtonStyle, addPassToWalletButtonStyle, verifyIdentityWithWalletButtonStyle, signInWithAppleButtonStyle
**Charts 3D**: chart3DCameraProjection, chart3DPose, chart3DRenderingStyle, chartZAxis, chartZAxisLabel, chartZScale, chartZSelection
**Contacts**: contactAccessButtonCaption, contactAccessButtonStyle, contactAccessPicker
**Drag & Drop**: dragConfiguration, dragContainer, dragContainerSelection, dragPreviewsFormation, draggable (5 overloads), dropConfiguration, dropDestination, dropPreviewsFormation, onDragSessionUpdated, onDropSessionUpdated
**Glass effects**: glassBackgroundEffect (2 overloads), glassEffect, glassEffectID, glassEffectTransition, glassEffectUnion
**Health**: healthDataAccessRequest (3 overloads)
**Image Playground**: imagePlaygroundGenerationStyle, imagePlaygroundOptions, imagePlaygroundPersonalizationPolicy, imagePlaygroundSheet (4 overloads)
**Journaling**: journalingSuggestionsPicker (2 overloads)
**Labels**: labelIconToTitleSpacing, labelReservedIconWidth, labeledContentStyle, labelsVisibility
**Lists**: listRowInsets, listSectionIndexVisibility, listSectionMargins, sectionIndexLabel
**Maps**: mapCameraKeyframeAnimator, mapControlVisibility, mapControls, mapFeatureSelectionAccessory, mapFeatureSelectionContent, mapFeatureSelectionDisabled, mapItemDetailPopover (4 overloads), mapItemDetailSheet (2 overloads), mapScope, mapStyle, onMapCameraChange, lookAroundViewer (2 overloads)
**Manipulation (visionOS)**: manipulable (3 overloads), manipulationGesture
**Navigation**: navigationLinkIndicatorVisibility, navigationTransition, matchedTransitionSource (2 overloads)
**Scroll**: scrollEdgeEffectHidden, scrollEdgeEffectStyle, scrollInputBehavior
**Tabs**: tabBarMinimizeBehavior, tabViewBottomAccessory (2 overloads), tabViewSearchActivation
**Task**: task (4 overloads with name/executorPreference/id variants)
**Text**: textContentType, textInputFormattingControlVisibility, textRenderer, textSelectionAffinity, attributedTextFormattingDefinition, lineHeight, writingDirection(strategy:), writingToolsAffordanceVisibility, writingToolsBehavior, searchSelection
**Tips**: tipAnchor, tipBackground, tipBackgroundInteraction, tipCornerRadius, tipImageSize, tipImageStyle, tipViewStyle, popoverTip (3 overloads)
**Toolbar**: toolbarItemHidden, contentToolbar, searchToolbarBehavior
**WebView**: webViewBackForwardNavigationGestures, webViewContentBackground, webViewContextMenu, webViewElementFullscreenBehavior, webViewLinkPreviews, webViewMagnificationGestures, webViewOnScrollGeometryChange, webViewScrollInputBehavior, webViewScrollPosition, webViewTextSelection
**Windows**: windowResizeAnchor, windowToolbarFullScreenVisibility, preferredWindowClippingMargins, allowsWindowActivationEvents, onInteractiveResizeChange
**3D / Spatial**: aspectRatio3D, rotation3DLayout (2 overloads), scaledToFill3D, scaledToFit3D, spatialOverlay, spatialOverlayPreferenceValue, onGeometryChange3D, immersiveEnvironmentPicker, onWorldRecenter
**Other**: assistiveAccessNavigationIcon (2 overloads), automatedDeviceEnrollmentAddition, backgroundExtensionEffect (2 overloads), breakthroughEffect, buttonSizing, certificateSheet, containerCornerOffset, containerValue, contentCaptureProtected, continuityDevicePicker, controlWidgetActionHint, controlWidgetStatus, dialogPreventsAppTermination, documentBrowserContextMenu, formStyle, foveatedStreamingPauseSheet, gameSaveSyncingAlert, groupActivityAssociation, handGestureShortcut, handPointerBehavior, handlesGameControllerEvents (2 overloads), managedContentStyle, materialActiveAppearance, onAppIntentExecution, onCameraCaptureEvent (2 overloads), onOpenURL(prefersInApp:), postToPhotosSharedAlbumSheet, presentationBreakthroughEffect, presentationPreventsAppTermination, realityViewCameraControls, realityViewLayoutBehavior, safeAreaBar, sliderThumbVisibility, symbolColorRenderingMode, symbolVariableValueMode, tabletopGame (2 overloads), transactionPicker, transactionTask, workoutPreview
