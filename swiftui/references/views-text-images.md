# Views: Text and Images — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Modifying a view](#modifying-a-view)
- [Responding to view life cycle updates](#responding-to-view-life-cycle-updates)
- [Managing the view hierarchy](#managing-the-view-hierarchy)
- [Supporting view types](#supporting-view-types)
- [Hiding views](#hiding-views)
- [Hiding system elements](#hiding-system-elements)
- [Managing view interaction](#managing-view-interaction)
- [Providing contextual help](#providing-contextual-help)
- [Detecting and requesting the light or dark appearance](#detecting-and-requesting-the-light-or-dark-appearance)
- [Getting the color scheme contrast](#getting-the-color-scheme-contrast)
- [Configuring passthrough](#configuring-passthrough)
- [Redacting private content](#redacting-private-content)
- [Styling views with Liquid Glass](#styling-views-with-liquid-glass)
- [Styling buttons](#styling-buttons)

---

### Alerts

- [func alert(_:isPresented:actions:)](/documentation/swiftui/view/alert(_:ispresented:actions:))
- [func alert(_:isPresented:presenting:actions:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:))
- [func alert(isPresented:error:actions:)](/documentation/swiftui/view/alert(ispresented:error:actions:))
- [func alert(_:isPresented:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:actions:message:))
- [func alert(_:isPresented:presenting:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:message:))
- [func alert(isPresented:error:actions:message:)](/documentation/swiftui/view/alert(ispresented:error:actions:message:))

### Confirmation dialogs

- [func confirmationDialog(_:isPresented:titleVisibility:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:))
- [func confirmationDialog(_:isPresented:titleVisibility:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:message:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:message:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:message:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:message:))

### Dialog configuration

- [func dialogIcon(Image?)](/documentation/swiftui/view/dialogicon(_:))
- [func dialogSeverity(DialogSeverity)](/documentation/swiftui/view/dialogseverity(_:))
- [func dialogSuppressionToggle(isSuppressed:)](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:))
- [func dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/view/dialogsuppressiontoggle(_:issuppressed:))

### Sheets

- [func sheet(isPresented:onDismiss:content:)](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:))
- [func sheet(item:onDismiss:content:)](/documentation/swiftui/view/sheet(item:ondismiss:content:))
- [func fullScreenCover(isPresented:onDismiss:content:)](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:))
- [func fullScreenCover(item:onDismiss:content:)](/documentation/swiftui/view/fullscreencover(item:ondismiss:content:))

### Popovers

- [func popover(item:attachmentAnchor:arrowEdge:content:)](/documentation/swiftui/view/popover(item:attachmentanchor:arrowedge:content:))
- [func popover(isPresented:attachmentAnchor:arrowEdge:content:)](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:))

### Sheet and popover configuration

- [func interactiveDismissDisabled(Bool)](/documentation/swiftui/view/interactivedismissdisabled(_:))
- [func presentationDetents(_:)](/documentation/swiftui/view/presentationdetents(_:))
- [func presentationDetents(_:selection:)](/documentation/swiftui/view/presentationdetents(_:selection:))
- [func presentationDragIndicator(Visibility)](/documentation/swiftui/view/presentationdragindicator(_:))
- [func presentationBackground(_:)](/documentation/swiftui/view/presentationbackground(_:))
- [func presentationBackground(alignment:content:)](/documentation/swiftui/view/presentationbackground(alignment:content:))
- [func presentationBackgroundInteraction(_:)](/documentation/swiftui/view/presentationbackgroundinteraction(_:))
- [func presentationCompactAdaptation(horizontal:vertical:)](/documentation/swiftui/view/presentationcompactadaptation(horizontal:vertical:))
- [func presentationCompactAdaptation(_:)](/documentation/swiftui/view/presentationcompactadaptation(_:))
- [func presentationContentInteraction(_:)](/documentation/swiftui/view/presentationcontentinteraction(_:))
- [func presentationCornerRadius(CGFloat?)](/documentation/swiftui/view/presentationcornerradius(_:))
- [func presentationSizing(_:)](/documentation/swiftui/view/presentationsizing(_:))

### File exporter

- [func fileExporter(isPresented:document:contentType:defaultFilename:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:))
- [func fileExporter(isPresented:documents:contentType:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttype:oncompletion:))
- [func fileExporter(isPresented:document:contentTypes:defaultFilename:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter(isPresented:documents:contentTypes:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttypes:oncompletion:oncancellation:))
- [func fileExporter(isPresented:item:contentTypes:defaultFilename:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:item:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter(isPresented:items:contentTypes:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:items:contenttypes:oncompletion:oncancellation:))
- [func fileExporterFilenameLabel(_:)](/documentation/swiftui/view/fileexporterfilenamelabel(_:))

### File importer

- [func fileImporter(isPresented:allowedContentTypes:allowsMultipleSelection:onCompletion:)](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:))
- [func fileImporter(isPresented:allowedContentTypes:onCompletion:)](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:))
- [func fileImporter(isPresented:allowedContentTypes:allowsMultipleSelection:onCompletion:onCancellation:)](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:oncancellation:))

### File mover

- [func fileMover(isPresented:file:onCompletion:)](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:))
- [func fileMover(isPresented:files:onCompletion:)](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:))
- [func fileMover(isPresented:file:onCompletion:onCancellation:)](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:oncancellation:))
- [func fileMover(isPresented:files:onCompletion:onCancellation:)](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:oncancellation:))

### File dialog configuration

- [func fileDialogBrowserOptions(_:)](/documentation/swiftui/view/filedialogbrowseroptions(_:))
- [func fileDialogConfirmationLabel(_:)](/documentation/swiftui/view/filedialogconfirmationlabel(_:))
- [func fileDialogCustomizationID(_:)](/documentation/swiftui/view/filedialogcustomizationid(_:))
- [func fileDialogDefaultDirectory(_:)](/documentation/swiftui/view/filedialogdefaultdirectory(_:))
- [func fileDialogImportsUnresolvedAliases(_:)](/documentation/swiftui/view/filedialogimportsunresolvedaliases(_:))
- [func fileDialogMessage(_:)](/documentation/swiftui/view/filedialogmessage(_:))
- [func fileDialogURLEnabled(_:)](/documentation/swiftui/view/filedialogurlenabled(_:))

### Inspectors

- [func inspector(isPresented:content:)](/documentation/swiftui/view/inspector(ispresented:content:))
- [func inspectorColumnWidth(_:)](/documentation/swiftui/view/inspectorcolumnwidth(_:))
- [func inspectorColumnWidth(min:ideal:max:)](/documentation/swiftui/view/inspectorcolumnwidth(min:ideal:max:))

### Quick look previews

- [func quickLookPreview(_:)](/documentation/swiftui/view/quicklookpreview(_:))
- [func quickLookPreview(_:in:)](/documentation/swiftui/view/quicklookpreview(_:in:))

### Family Sharing

- [func familyActivityPicker(isPresented:selection:)](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:))
- [func familyActivityPicker(headerText:footerText:isPresented:selection:)](/documentation/swiftui/view/familyactivitypicker(headertext:footertext:ispresented:selection:))
- [func familyActivityPicker(title:headerText:footerText:isPresented:selection:)](/documentation/swiftui/view/familyactivitypicker(title:headertext:footertext:ispresented:selection:))

### Live Activities

- [func activitySystemActionForegroundColor(Color?)](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:))
- [func activityBackgroundTint(Color?)](/documentation/swiftui/view/activitybackgroundtint(_:))

### Apple Music

- [func musicSubscriptionOffer(isPresented:options:onLoadCompletion:)](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))

### StoreKit

- [func appStoreOverlay(isPresented:configuration:)](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:))
- [func manageSubscriptionsSheet(isPresented:)](/documentation/swiftui/view/managesubscriptionssheet(ispresented:))
- [func refundRequestSheet(for:isPresented:onDismiss:)](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:))
- [func offerCodeRedemption(isPresented:onCompletion:)](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:))

### PhotoKit

- [func photosPicker(isPresented:selection:matching:preferredItemEncoding:)](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:))
- [func photosPicker(isPresented:selection:matching:preferredItemEncoding:photoLibrary:)](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:photolibrary:))
- [func photosPicker(isPresented:selection:maxSelectionCount:selectionBehavior:matching:preferredItemEncoding:)](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:))
- [func photosPicker(isPresented:selection:maxSelectionCount:selectionBehavior:matching:preferredItemEncoding:photoLibrary:)](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:photolibrary:))
- [func photosPickerAccessoryVisibility(_:edges:)](/documentation/swiftui/view/photospickeraccessoryvisibility(_:edges:))
- [func photosPickerDisabledCapabilities(_:)](/documentation/swiftui/view/photospickerdisabledcapabilities(_:))
- [func photosPickerStyle(_:)](/documentation/swiftui/view/photospickerstyle(_:))

### Translation

- [func translationPresentation(isPresented:text:attachmentAnchor:arrowEdge:replacementAction:)](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:))
- [func translationTask(_:action:)](/documentation/swiftui/view/translationtask(_:action:))
- [func translationTask(source:target:action:)](/documentation/swiftui/view/translationtask(source:target:action:))
- [func translationTask(source:target:preferredStrategy:action:)](/documentation/swiftui/view/translationtask(source:target:preferredstrategy:action:))
- [State modifiers](/documentation/swiftui/view-state)

### Identity

- [func tag(_:includeOptional:)](/documentation/swiftui/view/tag(_:includeoptional:))
- [func id(_:)](/documentation/swiftui/view/id(_:))
- [func equatable()](/documentation/swiftui/view/equatable())

### Environment values

- [func environment(_:)](/documentation/swiftui/view/environment(_:)) — set environment value by type
- [func environment(_:_:)](/documentation/swiftui/view/environment(_:_:)) — set environment value by key path
- [func environmentObject(_:)](/documentation/swiftui/view/environmentobject(_:))
- [func transformEnvironment(_:transform:)](/documentation/swiftui/view/transformenvironment(_:transform:))

### Preferences

- [func preference(key:value:)](/documentation/swiftui/view/preference(key:value:))
- [func transformPreference(_:_:)](/documentation/swiftui/view/transformpreference(_:_:))
- [func anchorPreference(key:value:transform:)](/documentation/swiftui/view/anchorpreference(key:value:transform:))
- [func transformAnchorPreference(key:value:transform:)](/documentation/swiftui/view/transformanchorpreference(key:value:transform:))
- [func onPreferenceChange(_:perform:)](/documentation/swiftui/view/onpreferencechange(_:perform:))
- [func backgroundPreferenceValue(_:_:)](/documentation/swiftui/view/backgroundpreferencevalue(_:_:))
- [func backgroundPreferenceValue(_:alignment:_:)](/documentation/swiftui/view/backgroundpreferencevalue(_:alignment:_:))
- [func overlayPreferenceValue(_:_:)](/documentation/swiftui/view/overlaypreferencevalue(_:_:))
- [func overlayPreferenceValue(_:alignment:_:)](/documentation/swiftui/view/overlaypreferencevalue(_:alignment:_:))

### Default storage

- [func defaultAppStorage(UserDefaults)](/documentation/swiftui/view/defaultappstorage(_:))

### Configuring a model

- [func modelContext(ModelContext)](/documentation/swiftui/view/modelcontext(_:))
- [func modelContainer(ModelContainer)](/documentation/swiftui/view/modelcontainer(_:))
- [func modelContainer(for:inMemory:isAutosaveEnabled:isUndoEnabled:onSetup:)](/documentation/swiftui/view/modelcontainer(for:inmemory:isautosaveenabled:isundoenabled:onsetup:))

### Deprecated modifiers [deprecated]

- [Deprecated modifiers](/documentation/swiftui/view-deprecated)
- accessibility(label:), accessibility(value:), accessibility(hidden:), accessibility(identifier:), accessibility(selectionIdentifier:), accessibility(hint:), accessibility(activationPoint:), accessibility(inputLabels:), accessibility(addTraits:), accessibility(removeTraits:), accessibility(sortPriority:) — use accessibilityLabel, accessibilityValue, etc. instead
- colorScheme(_:), listRowPlatterColor(_:), background(_:alignment:), overlay(_:alignment:), foregroundColor(_:), complicationForeground() [deprecated]
- autocapitalization(_:), disableAutocorrection(_:) [deprecated]
- navigationBarTitle(_:), navigationBarTitle(_:displayMode:), navigationBarItems(leading:), navigationBarItems(leading:trailing:), navigationBarItems(trailing:), navigationBarHidden(_:), statusBar(hidden:), contextMenu(_:) [deprecated]
- menuButtonStyle(_:), navigationViewStyle(_:) [deprecated]
- frame(), edgesIgnoringSafeArea(_:), coordinateSpace(name:) [deprecated]
- accentColor(_:), mask(_:), animation(_:), cornerRadius(_:antialiased:) [deprecated]
- onChange(of:perform:), onTapGesture(count:coordinateSpace:perform:), onLongPressGesture (old signatures), onPasteCommand(of:perform:), onDrop(of:delegate:), focusable(_:onFocusChange:), onContinuousHover(coordinateSpace:perform:) [deprecated]
- actionSheet(isPresented:content:), actionSheet(item:content:), alert(isPresented:content:), alert(item:content:) [deprecated]
- searchable(text:placement:prompt:suggestions:), tabItem(_:) [deprecated]

### Instance methods (additional view modifiers)

- [func accessibilityActions(category:_:)](/documentation/swiftui/view/accessibilityactions(category:_:))
- [func accessibilityDefaultFocus(_:_:)](/documentation/swiftui/view/accessibilitydefaultfocus(_:_:))
- [func accessibilityScrollStatus(_:isEnabled:)](/documentation/swiftui/view/accessibilityscrollstatus(_:isenabled:))
- [func addOrderToWalletButtonStyle(_:)](/documentation/swiftui/view/addordertowalletbuttonstyle(_:))
- [func addPassToWalletButtonStyle(_:)](/documentation/swiftui/view/addpasstowalletbuttonstyle(_:))
- [func allowsWindowActivationEvents()](/documentation/swiftui/view/allowswindowactivationevents())
- [func appStoreMerchandising(isPresented:kind:onDismiss:)](/documentation/swiftui/view/appstoremerchandising(ispresented:kind:ondismiss:))
- [func aspectRatio3D(_:contentMode:)](/documentation/swiftui/view/aspectratio3d(_:contentmode:))
- [func assistiveAccessNavigationIcon(_:)](/documentation/swiftui/view/assistiveaccessnavigationicon(_:))
- [func assistiveAccessNavigationIcon(systemImage:)](/documentation/swiftui/view/assistiveaccessnavigationicon(systemimage:))
- [func attributedTextFormattingDefinition(_:)](/documentation/swiftui/view/attributedtextformattingdefinition(_:))
- [func automatedDeviceEnrollmentAddition(isPresented:)](/documentation/swiftui/view/automateddeviceenrollmentaddition(ispresented:))
- [func backgroundExtensionEffect()](/documentation/swiftui/view/backgroundextensioneffect())
- [func backgroundExtensionEffect(isEnabled:)](/documentation/swiftui/view/backgroundextensioneffect(isenabled:))
- [func breakthroughEffect(_:)](/documentation/swiftui/view/breakthrougheffect(_:))
- [func buttonSizing(_:)](/documentation/swiftui/view/buttonsizing(_:))
- [func certificateSheet(trust:title:message:help:)](/documentation/swiftui/view/certificatesheet(trust:title:message:help:))
- [func chart3DCameraProjection(_:)](/documentation/swiftui/view/chart3dcameraprojection(_:))
- [func chart3DPose(_:)](/documentation/swiftui/view/chart3dpose(_:))
- [func chart3DRenderingStyle(_:)](/documentation/swiftui/view/chart3drenderingstyle(_:))
- [func chartZAxis(_:)](/documentation/swiftui/view/chartzaxis(_:))
- [func chartZAxis(content:)](/documentation/swiftui/view/chartzaxis(content:))
- [func chartZAxisLabel(_:position:alignment:spacing:)](/documentation/swiftui/view/chartzaxislabel(_:position:alignment:spacing:))
- [func chartZScale(domain:range:type:)](/documentation/swiftui/view/chartzscale(domain:range:type:))
- [func chartZScale(domain:type:)](/documentation/swiftui/view/chartzscale(domain:type:))
- [func chartZScale(range:type:)](/documentation/swiftui/view/chartzscale(range:type:))
- [func chartZSelection(range:)](/documentation/swiftui/view/chartzselection(range:))
- [func chartZSelection(value:)](/documentation/swiftui/view/chartzselection(value:))
- [func contactAccessButtonCaption(_:)](/documentation/swiftui/view/contactaccessbuttoncaption(_:))
- [func contactAccessButtonStyle(_:)](/documentation/swiftui/view/contactaccessbuttonstyle(_:))
- [func contactAccessPicker(isPresented:completionHandler:)](/documentation/swiftui/view/contactaccesspicker(ispresented:completionhandler:))
- [func containerCornerOffset(_:sizeToFit:)](/documentation/swiftui/view/containercorneroffset(_:sizetofit:))
- [func containerValue(_:_:)](/documentation/swiftui/view/containervalue(_:_:))
- [func contentCaptureProtected(_:)](/documentation/swiftui/view/contentcaptureprotected(_:))
- [func contentToolbar(for:content:)](/documentation/swiftui/view/contenttoolbar(for:content:))
- [func continuityDevicePicker(isPresented:onDidConnect:)](/documentation/swiftui/view/continuitydevicepicker(ispresented:ondidconnect:))
- [func controlWidgetActionHint(_:)](/documentation/swiftui/view/controlwidgetactionhint(_:))
- [func controlWidgetStatus(_:)](/documentation/swiftui/view/controlwidgetstatus(_:))
- [func currentEntitlementTask(for:priority:action:)](/documentation/swiftui/view/currententitlementtask(for:priority:action:))
- [func dialogPreventsAppTermination(_:)](/documentation/swiftui/view/dialogpreventsapptermination(_:))
- [func documentBrowserContextMenu(_:)](/documentation/swiftui/view/documentbrowsercontextmenu(_:))
- [func dragConfiguration(_:)](/documentation/swiftui/view/dragconfiguration(_:))
- [func dragContainer(for:in:_:)](/documentation/swiftui/view/dragcontainer(for:in:_:))
- [func dragContainer(for:itemID:in:_:)](/documentation/swiftui/view/dragcontainer(for:itemid:in:_:))
- [func dragContainerSelection(_:containerNamespace:)](/documentation/swiftui/view/dragcontainerselection(_:containernamespace:))
- [func dragPreviewsFormation(_:)](/documentation/swiftui/view/dragpreviewsformation(_:))
- [func draggable(_:containerNamespace:_:)](/documentation/swiftui/view/draggable(_:containernamespace:_:))
- [func draggable(_:id:containerNamespace:_:)](/documentation/swiftui/view/draggable(_:id:containernamespace:_:))
- [func draggable(_:id:item:containerNamespace:)](/documentation/swiftui/view/draggable(_:id:item:containernamespace:))
- [func draggable(_:item:containerNamespace:)](/documentation/swiftui/view/draggable(_:item:containernamespace:))
- [func draggable(containerItemID:containerNamespace:)](/documentation/swiftui/view/draggable(containeritemid:containernamespace:))
- [func dropConfiguration(_:)](/documentation/swiftui/view/dropconfiguration(_:))
- [func dropDestination(for:isEnabled:action:)](/documentation/swiftui/view/dropdestination(for:isenabled:action:))
- [func dropPreviewsFormation(_:)](/documentation/swiftui/view/droppreviewsformation(_:))
- [func formStyle(_:)](/documentation/swiftui/view/formstyle(_:))
- [func foveatedStreamingPauseSheet(session:)](/documentation/swiftui/view/foveatedstreamingpausesheet(session:))
- [func gameSaveSyncingAlert(directory:finishedLoading:)](/documentation/swiftui/view/gamesavesyncingalert(directory:finishedloading:))
- [func glassBackgroundEffect(_:displayMode:)](/documentation/swiftui/view/glassbackgroundeffect(_:displaymode:))
- [func glassBackgroundEffect(_:in:displayMode:)](/documentation/swiftui/view/glassbackgroundeffect(_:in:displaymode:))
- [func glassEffect(_:in:)](/documentation/swiftui/view/glasseffect(_:in:))
- [func glassEffectID(_:in:)](/documentation/swiftui/view/glasseffectid(_:in:))
- [func glassEffectTransition(_:)](/documentation/swiftui/view/glasseffecttransition(_:))
- [func glassEffectUnion(id:namespace:)](/documentation/swiftui/view/glasseffectunion(id:namespace:))
- [func groupActivityAssociation(_:)](/documentation/swiftui/view/groupactivityassociation(_:))
- [func handGestureShortcut(_:isEnabled:)](/documentation/swiftui/view/handgestureshortcut(_:isenabled:))
- [func handPointerBehavior(_:)](/documentation/swiftui/view/handpointerbehavior(_:))
- [func handlesGameControllerEvents(matching:)](/documentation/swiftui/view/handlesgamecontrollerevents(matching:))
- [func handlesGameControllerEvents(matching:withOptions:)](/documentation/swiftui/view/handlesgamecontrollerevents(matching:withoptions:))
- [func healthDataAccessRequest(store:objectType:predicate:trigger:completion:)](/documentation/swiftui/view/healthdataaccessrequest(store:objecttype:predicate:trigger:completion:))
- [func healthDataAccessRequest(store:readTypes:trigger:completion:)](/documentation/swiftui/view/healthdataaccessrequest(store:readtypes:trigger:completion:))
- [func healthDataAccessRequest(store:shareTypes:readTypes:trigger:completion:)](/documentation/swiftui/view/healthdataaccessrequest(store:sharetypes:readtypes:trigger:completion:))
- [func imagePlaygroundGenerationStyle(_:in:)](/documentation/swiftui/view/imageplaygroundgenerationstyle(_:in:))
- [func imagePlaygroundOptions(_:)](/documentation/swiftui/view/imageplaygroundoptions(_:))
- [func imagePlaygroundPersonalizationPolicy(_:)](/documentation/swiftui/view/imageplaygroundpersonalizationpolicy(_:))
- [func imagePlaygroundSheet(isPresented:concept:sourceImage:onCompletion:onCancellation:)](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concept:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented:concept:sourceImageURL:onCompletion:onCancellation:)](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concept:sourceimageurl:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented:concepts:sourceImage:onCompletion:onCancellation:)](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented:concepts:sourceImageURL:onCompletion:onCancellation:)](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimageurl:oncompletion:oncancellation:))
- [func immersiveEnvironmentPicker(content:)](/documentation/swiftui/view/immersiveenvironmentpicker(content:))
- [func inAppPurchaseOptions(_:)](/documentation/swiftui/view/inapppurchaseoptions(_:))
- [func journalingSuggestionsPicker(isPresented:journalingSuggestionToken:onCompletion:)](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:journalingsuggestiontoken:oncompletion:))
- [func journalingSuggestionsPicker(isPresented:onCompletion:)](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:oncompletion:))
- [func labelIconToTitleSpacing(_:)](/documentation/swiftui/view/labelicontotitlespacing(_:))
- [func labelReservedIconWidth(_:)](/documentation/swiftui/view/labelreservediconwidth(_:))
- [func labeledContentStyle(_:)](/documentation/swiftui/view/labeledcontentstyle(_:))
- [func labelsVisibility(_:)](/documentation/swiftui/view/labelsvisibility(_:))
- [func lineHeight(_:)](/documentation/swiftui/view/lineheight(_:))
- [func listRowInsets(_:_:)](/documentation/swiftui/view/listrowinsets(_:_:))
- [func listSectionIndexVisibility(_:)](/documentation/swiftui/view/listsectionindexvisibility(_:))
- [func listSectionMargins(_:_:)](/documentation/swiftui/view/listsectionmargins(_:_:))
- [func lookAroundViewer(isPresented:initialScene:allowsNavigation:showsRoadLabels:pointsOfInterest:onDismiss:)](/documentation/swiftui/view/lookaroundviewer(ispresented:initialscene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func lookAroundViewer(isPresented:scene:allowsNavigation:showsRoadLabels:pointsOfInterest:onDismiss:)](/documentation/swiftui/view/lookaroundviewer(ispresented:scene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func manageSubscriptionsSheet(isPresented:subscriptionGroupID:)](/documentation/swiftui/view/managesubscriptionssheet(ispresented:subscriptiongroupid:))
- [func managedContentStyle(_:)](/documentation/swiftui/view/managedcontentstyle(_:))
- [func manipulable(coordinateSpace:operations:inertia:isEnabled:onChanged:)](/documentation/swiftui/view/manipulable(coordinatespace:operations:inertia:isenabled:onchanged:))
- [func manipulable(transform:coordinateSpace:operations:inertia:isEnabled:onChanged:)](/documentation/swiftui/view/manipulable(transform:coordinatespace:operations:inertia:isenabled:onchanged:))
- [func manipulable(using:)](/documentation/swiftui/view/manipulable(using:))
- [func manipulationGesture(updating:coordinateSpace:operations:inertia:isEnabled:onChanged:)](/documentation/swiftui/view/manipulationgesture(updating:coordinatespace:operations:inertia:isenabled:onchanged:))
- [func mapCameraKeyframeAnimator(trigger:keyframes:)](/documentation/swiftui/view/mapcamerakeyframeanimator(trigger:keyframes:))
- [func mapControlVisibility(_:)](/documentation/swiftui/view/mapcontrolvisibility(_:))
- [func mapControls(_:)](/documentation/swiftui/view/mapcontrols(_:))
- [func mapFeatureSelectionAccessory(_:)](/documentation/swiftui/view/mapfeatureselectionaccessory(_:))
- [func mapFeatureSelectionContent(content:)](/documentation/swiftui/view/mapfeatureselectioncontent(content:))
- [func mapFeatureSelectionDisabled(_:)](/documentation/swiftui/view/mapfeatureselectiondisabled(_:))
- [func mapItemDetailPopover(isPresented:item:displaysMap:attachmentAnchor:)](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(isPresented:item:displaysMap:attachmentAnchor:arrowEdge:)](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailPopover(item:displaysMap:attachmentAnchor:)](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(item:displaysMap:attachmentAnchor:arrowEdge:)](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailSheet(isPresented:item:displaysMap:)](/documentation/swiftui/view/mapitemdetailsheet(ispresented:item:displaysmap:))
- [func mapItemDetailSheet(item:displaysMap:)](/documentation/swiftui/view/mapitemdetailsheet(item:displaysmap:))
- [func mapScope(_:)](/documentation/swiftui/view/mapscope(_:))
- [func mapStyle(_:)](/documentation/swiftui/view/mapstyle(_:))
- [func matchedTransitionSource(id:in:)](/documentation/swiftui/view/matchedtransitionsource(id:in:))
- [func matchedTransitionSource(id:in:configuration:)](/documentation/swiftui/view/matchedtransitionsource(id:in:configuration:))
- [func materialActiveAppearance(_:)](/documentation/swiftui/view/materialactiveappearance(_:))
- [func navigationLinkIndicatorVisibility(_:)](/documentation/swiftui/view/navigationlinkindicatorvisibility(_:))
- [func navigationTransition(_:)](/documentation/swiftui/view/navigationtransition(_:))
- [func onAppIntentExecution(_:perform:)](/documentation/swiftui/view/onappintentexecution(_:perform:))
- [func onApplePayCouponCodeChange(perform:)](/documentation/swiftui/view/onapplepaycouponcodechange(perform:))
- [func onApplePayPaymentMethodChange(perform:)](/documentation/swiftui/view/onapplepaypaymentmethodchange(perform:))
- [func onApplePayShippingContactChange(perform:)](/documentation/swiftui/view/onapplepayshippingcontactchange(perform:))
- [func onApplePayShippingMethodChange(perform:)](/documentation/swiftui/view/onapplepayshippingmethodchange(perform:))
- [func onCameraCaptureEvent(isEnabled:defaultSoundDisabled:action:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:defaultsounddisabled:action:))
- [func onCameraCaptureEvent(isEnabled:defaultSoundDisabled:primaryAction:secondaryAction:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:defaultsounddisabled:primaryaction:secondaryaction:))
- [func onDragSessionUpdated(_:)](/documentation/swiftui/view/ondragsessionupdated(_:))
- [func onDropSessionUpdated(_:)](/documentation/swiftui/view/ondropsessionupdated(_:))
- [func onGeometryChange3D(for:of:action:)](/documentation/swiftui/view/ongeometrychange3d(for:of:action:))
- [func onInAppPurchaseCompletion(perform:)](/documentation/swiftui/view/oninapppurchasecompletion(perform:))
- [func onInAppPurchaseStart(perform:)](/documentation/swiftui/view/oninapppurchasestart(perform:))
- [func onInteractiveResizeChange(_:)](/documentation/swiftui/view/oninteractiveresizechange(_:))
- [func onMapCameraChange(frequency:_:)](/documentation/swiftui/view/onmapcamerachange(frequency:_:))
- [func onOpenURL(prefersInApp:)](/documentation/swiftui/view/onopenurl(prefersinapp:))
- [func onWorldRecenter(action:)](/documentation/swiftui/view/onworldrecenter(action:))
- [func payLaterViewAction(_:)](/documentation/swiftui/view/paylaterviewaction(_:))
- [func payLaterViewDisplayStyle(_:)](/documentation/swiftui/view/paylaterviewdisplaystyle(_:))
- [func payWithApplePayButtonDisableCardArt()](/documentation/swiftui/view/paywithapplepaybuttondisablecardart())
- [func payWithApplePayButtonStyle(_:)](/documentation/swiftui/view/paywithapplepaybuttonstyle(_:))
- [func popoverTip(_:arrowEdge:action:)](/documentation/swiftui/view/popovertip(_:arrowedge:action:))
- [func popoverTip(_:isPresented:attachmentAnchor:arrowEdge:action:)](/documentation/swiftui/view/popovertip(_:ispresented:attachmentanchor:arrowedge:action:))
- [func popoverTip(_:isPresented:attachmentAnchor:arrowEdges:action:)](/documentation/swiftui/view/popovertip(_:ispresented:attachmentanchor:arrowedges:action:))
- [func postToPhotosSharedAlbumSheet(isPresented:items:photoLibrary:defaultAlbumIdentifier:completion:)](/documentation/swiftui/view/posttophotossharedalbumsheet(ispresented:items:photolibrary:defaultalbumidentifier:completion:))
- [func preferredSubscriptionOffer(_:)](/documentation/swiftui/view/preferredsubscriptionoffer(_:))
- [func preferredSubscriptionPricingTerms(_:)](/documentation/swiftui/view/preferredsubscriptionpricingterms(_:))
- [func preferredWindowClippingMargins(_:_:)](/documentation/swiftui/view/preferredwindowclippingmargins(_:_:))
- [func presentationBreakthroughEffect(_:)](/documentation/swiftui/view/presentationbreakthrougheffect(_:))
- [func presentationPreventsAppTermination(_:)](/documentation/swiftui/view/presentationpreventsapptermination(_:))
- [func productDescription(_:)](/documentation/swiftui/view/productdescription(_:))
- [func productIconBorder()](/documentation/swiftui/view/producticonborder())
- [func productViewStyle(_:)](/documentation/swiftui/view/productviewstyle(_:))
- [func realityViewCameraControls(_:)](/documentation/swiftui/view/realityviewcameracontrols(_:))
- [func realityViewLayoutBehavior(_:)](/documentation/swiftui/view/realityviewlayoutbehavior(_:))
- [func rotation3DLayout(_:)](/documentation/swiftui/view/rotation3dlayout(_:))
- [func rotation3DLayout(_:axis:)](/documentation/swiftui/view/rotation3dlayout(_:axis:))
- [func safeAreaBar(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareabar(edge:alignment:spacing:content:))
- [func scaledToFill3D()](/documentation/swiftui/view/scaledtofill3d())
- [func scaledToFit3D()](/documentation/swiftui/view/scaledtofit3d())
- [func scrollEdgeEffectHidden(_:for:)](/documentation/swiftui/view/scrolledgeeffecthidden(_:for:))
- [func scrollEdgeEffectStyle(_:for:)](/documentation/swiftui/view/scrolledgeeffectstyle(_:for:))
- [func scrollInputBehavior(_:for:)](/documentation/swiftui/view/scrollinputbehavior(_:for:))
- [func searchSelection(_:)](/documentation/swiftui/view/searchselection(_:))
- [func searchToolbarBehavior(_:)](/documentation/swiftui/view/searchtoolbarbehavior(_:))
- [func sectionIndexLabel(_:)](/documentation/swiftui/view/sectionindexlabel(_:))
- [func signInWithAppleButtonStyle(_:)](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))
- [func sliderThumbVisibility(_:)](/documentation/swiftui/view/sliderthumbvisibility(_:))
- [func spatialOverlay(alignment:content:)](/documentation/swiftui/view/spatialoverlay(alignment:content:))
- [func spatialOverlayPreferenceValue(_:alignment:_:)](/documentation/swiftui/view/spatialoverlaypreferencevalue(_:alignment:_:))
- [func storeButton(_:for:)](/documentation/swiftui/view/storebutton(_:for:))
- [func storeProductTask(for:priority:action:)](/documentation/swiftui/view/storeproducttask(for:priority:action:))
- [func storeProductsTask(for:priority:action:)](/documentation/swiftui/view/storeproductstask(for:priority:action:))
- [func subscriptionIntroductoryOffer(applyOffer:compactJWS:)](/documentation/swiftui/view/subscriptionintroductoryoffer(applyoffer:compactjws:))
- [func subscriptionOfferViewButtonVisibility(_:for:)](/documentation/swiftui/view/subscriptionofferviewbuttonvisibility(_:for:))
- [func subscriptionOfferViewDetailAction(_:)](/documentation/swiftui/view/subscriptionofferviewdetailaction(_:))
- [func subscriptionOfferViewStyle(_:)](/documentation/swiftui/view/subscriptionofferviewstyle(_:))
- [func subscriptionPromotionalOffer(offer:compactJWS:)](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:compactjws:))
- [func subscriptionPromotionalOffer(offer:signature:)](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:signature:))
- [func subscriptionStatusTask(for:priority:action:)](/documentation/swiftui/view/subscriptionstatustask(for:priority:action:))
- [func subscriptionStoreButtonLabel(_:)](/documentation/swiftui/view/subscriptionstorebuttonlabel(_:))
- [func subscriptionStoreControlBackground(_:)](/documentation/swiftui/view/subscriptionstorecontrolbackground(_:))
- [func subscriptionStoreControlIcon(icon:)](/documentation/swiftui/view/subscriptionstorecontrolicon(icon:))
- [func subscriptionStoreControlStyle(_:)](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:))
- [func subscriptionStoreControlStyle(_:placement:)](/documentation/swiftui/view/subscriptionstorecontrolstyle(_:placement:))
- [func subscriptionStoreOptionGroupStyle(_:)](/documentation/swiftui/view/subscriptionstoreoptiongroupstyle(_:))
- [func subscriptionStorePickerItemBackground(_:)](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:))
- [func subscriptionStorePickerItemBackground(_:in:)](/documentation/swiftui/view/subscriptionstorepickeritembackground(_:in:))
- [func subscriptionStorePolicyDestination(for:destination:)](/documentation/swiftui/view/subscriptionstorepolicydestination(for:destination:))
- [func subscriptionStorePolicyDestination(url:for:)](/documentation/swiftui/view/subscriptionstorepolicydestination(url:for:))
- [func subscriptionStorePolicyForegroundStyle(_:)](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:))
- [func subscriptionStorePolicyForegroundStyle(_:_:)](/documentation/swiftui/view/subscriptionstorepolicyforegroundstyle(_:_:))
- [func subscriptionStoreSignInAction(_:)](/documentation/swiftui/view/subscriptionstoresigninaction(_:))
- [func symbolColorRenderingMode(_:)](/documentation/swiftui/view/symbolcolorrenderingmode(_:))
- [func symbolVariableValueMode(_:)](/documentation/swiftui/view/symbolvariablevaluemode(_:))
- [func tabBarMinimizeBehavior(_:)](/documentation/swiftui/view/tabbarminimizebehavior(_:))
- [func tabViewBottomAccessory(content:)](/documentation/swiftui/view/tabviewbottomaccessory(content:))
- [func tabViewBottomAccessory(isEnabled:content:)](/documentation/swiftui/view/tabviewbottomaccessory(isenabled:content:))
- [func tabViewSearchActivation(_:)](/documentation/swiftui/view/tabviewsearchactivation(_:))
- [func tabletopGame(_:parent:automaticUpdate:)](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:))
- [func tabletopGame(_:parent:automaticUpdate:interaction:)](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:interaction:))
- [func task(id:name:executorPreference:priority:file:line:_:)](/documentation/swiftui/view/task(id:name:executorpreference:priority:file:line:_:))
- [func task(id:name:priority:file:line:_:)](/documentation/swiftui/view/task(id:name:priority:file:line:_:))
- [func task(name:executorPreference:priority:file:line:action:)](/documentation/swiftui/view/task(name:executorpreference:priority:file:line:action:))
- [func task(name:priority:file:line:_:)](/documentation/swiftui/view/task(name:priority:file:line:_:))
- [func textContentType(_:)](/documentation/swiftui/view/textcontenttype(_:))
- [func textInputFormattingControlVisibility(_:for:)](/documentation/swiftui/view/textinputformattingcontrolvisibility(_:for:))
- [func textRenderer(_:)](/documentation/swiftui/view/textrenderer(_:))
- [func textSelectionAffinity(_:)](/documentation/swiftui/view/textselectionaffinity(_:))
- [func tipAnchor(_:)](/documentation/swiftui/view/tipanchor(_:))
- [func tipBackground(_:)](/documentation/swiftui/view/tipbackground(_:))
- [func tipBackgroundInteraction(_:)](/documentation/swiftui/view/tipbackgroundinteraction(_:))
- [func tipCornerRadius(_:antialiased:)](/documentation/swiftui/view/tipcornerradius(_:antialiased:))
- [func tipImageSize(_:)](/documentation/swiftui/view/tipimagesize(_:))
- [func tipImageStyle(_:)](/documentation/swiftui/view/tipimagestyle(_:))
- [func tipViewStyle(_:)](/documentation/swiftui/view/tipviewstyle(_:))
- [func toolbarItemHidden(_:)](/documentation/swiftui/view/toolbaritemhidden(_:))
- [func transactionPicker(isPresented:selection:)](/documentation/swiftui/view/transactionpicker(ispresented:selection:))
- [func transactionTask(_:action:)](/documentation/swiftui/view/transactiontask(_:action:))
- [func verifyIdentityWithWalletButtonStyle(_:)](/documentation/swiftui/view/verifyidentitywithwalletbuttonstyle(_:))
- [func webViewBackForwardNavigationGestures(_:)](/documentation/swiftui/view/webviewbackforwardnavigationgestures(_:))
- [func webViewContentBackground(_:)](/documentation/swiftui/view/webviewcontentbackground(_:))
- [func webViewContextMenu(menu:)](/documentation/swiftui/view/webviewcontextmenu(menu:))
- [func webViewElementFullscreenBehavior(_:)](/documentation/swiftui/view/webviewelementfullscreenbehavior(_:))
- [func webViewLinkPreviews(_:)](/documentation/swiftui/view/webviewlinkpreviews(_:))
- [func webViewMagnificationGestures(_:)](/documentation/swiftui/view/webviewmagnificationgestures(_:))
- [func webViewOnScrollGeometryChange(for:of:action:)](/documentation/swiftui/view/webviewonscrollgeometrychange(for:of:action:))
- [func webViewScrollInputBehavior(_:for:)](/documentation/swiftui/view/webviewscrollinputbehavior(_:for:))
- [func webViewScrollPosition(_:)](/documentation/swiftui/view/webviewscrollposition(_:))
- [func webViewTextSelection(_:)](/documentation/swiftui/view/webviewtextselection(_:))
- [func windowResizeAnchor(_:)](/documentation/swiftui/view/windowresizeanchor(_:))
- [func windowToolbarFullScreenVisibility(_:)](/documentation/swiftui/view/windowtoolbarfullscreenvisibility(_:))
- [func workoutPreview(_:isPresented:)](/documentation/swiftui/view/workoutpreview(_:ispresented:))
- [func writingDirection(strategy:)](/documentation/swiftui/view/writingdirection(strategy:))
- [func writingToolsAffordanceVisibility(_:)](/documentation/swiftui/view/writingtoolsaffordancevisibility(_:))
- [func writingToolsBehavior(_:)](/documentation/swiftui/view/writingtoolsbehavior(_:))

### ViewBuilder

- [ViewBuilder](/documentation/swiftui/viewbuilder) — result builder for composing views
- buildBlock, buildExpression, buildEither(first:), buildEither(second:), buildIf, buildLimitedAvailability

### Modifying a view

- [Configuring views](/documentation/swiftui/configuring-views) (article)
- [Reducing view modifier maintenance](/documentation/swiftui/reducing-view-modifier-maintenance) (article)
- [func modifier(_:)](/documentation/swiftui/view/modifier(_:))
- [ViewModifier](/documentation/swiftui/viewmodifier) — protocol for reusable view transformations; body(content:), Body, Content, animation(_:), concat(_:), transaction(_:)
- [EmptyModifier](/documentation/swiftui/emptymodifier) — no-op modifier; static identity
- [ModifiedContent](/documentation/swiftui/modifiedcontent) — pairs content + modifier; has content/modifier properties. Accessibility methods mirror View's. [deprecated]
- [EnvironmentalModifier](/documentation/swiftui/environmentalmodifier) — resolves modifier from environment; resolve(in:), ResolvedModifier

### Manipulation modifiers (visionOS)

- [ManipulableModifier](/documentation/swiftui/manipulablemodifier), [ManipulableResponderModifier](/documentation/swiftui/manipulablerespondermodifier), [ManipulableTransformBindingModifier](/documentation/swiftui/manipulabletransformbindingmodifier), [ManipulationGeometryModifier](/documentation/swiftui/manipulationgeometrymodifier), [ManipulationGestureModifier](/documentation/swiftui/manipulationgesturemodifier), [ManipulationUsingGestureStateModifier](/documentation/swiftui/manipulationusinggesturestatemodifier)
- [Manipulable](/documentation/swiftui/manipulable) — namespace for manipulation types
- Manipulable.Event — phase (active, ended, failed), value (frame, inputDevices, interactionPoint, timestamp, transform)
- Manipulable.GestureState — init(transform:), isActive, transform
- Manipulable.Inertia — none, low, medium, high
- Manipulable.InputDevice — chirality (left, right), kind (directPinch, indirectPinch, pointer), pose
- Manipulable.Operation — primaryRotation, scale, secondaryRotation, translate; Operation.Set: all, primaryRotation, scale, secondaryRotation, translate

### Responding to view life cycle updates

- [func onAppear(perform:)](/documentation/swiftui/view/onappear(perform:))
- [func onDisappear(perform:)](/documentation/swiftui/view/ondisappear(perform:))

### Managing the view hierarchy

- [func id(_:)](/documentation/swiftui/view/id(_:))
- [func tag(_:includeOptional:)](/documentation/swiftui/view/tag(_:includeoptional:))
- [func equatable()](/documentation/swiftui/view/equatable())

### Supporting view types

- [AnyView](/documentation/swiftui/anyview) — type-erased view; init(_:), init(erasing:)
- [EmptyView](/documentation/swiftui/emptyview) — view with no content
- [EquatableView](/documentation/swiftui/equatableview) — skips re-render when content is equal; init(content:)
- [SubscriptionView](/documentation/swiftui/subscriptionview) — subscribes to a publisher; init(content:publisher:action:)
- [TupleView](/documentation/swiftui/tupleview) — groups multiple views; init(_:), value
- [View configuration](/documentation/swiftui/view-configuration) (article)

### Hiding views

- [func opacity(Double)](/documentation/swiftui/view/opacity(_:))
- [func hidden()](/documentation/swiftui/view/hidden())

### Hiding system elements

- [func labelsHidden()](/documentation/swiftui/view/labelshidden())
- [func labelsVisibility(Visibility)](/documentation/swiftui/view/labelsvisibility(_:))
- [var labelsVisibility: Visibility](/documentation/swiftui/environmentvalues/labelsvisibility)
- [func menuIndicator(Visibility)](/documentation/swiftui/view/menuindicator(_:))
- [func statusBarHidden(Bool)](/documentation/swiftui/view/statusbarhidden(_:))
- [func persistentSystemOverlays(Visibility)](/documentation/swiftui/view/persistentsystemoverlays(_:))
- [Visibility](/documentation/swiftui/visibility) — cases: automatic, visible, hidden

### Managing view interaction

- [func disabled(Bool)](/documentation/swiftui/view/disabled(_:))
- [var isEnabled: Bool](/documentation/swiftui/environmentvalues/isenabled)
- [func interactionActivityTrackingTag(String)](/documentation/swiftui/view/interactionactivitytrackingtag(_:))
- [func invalidatableContent(Bool)](/documentation/swiftui/view/invalidatablecontent(_:))

### Providing contextual help

- [func help(_:)](/documentation/swiftui/view/help(_:))

### Detecting and requesting the light or dark appearance

- [func preferredColorScheme(ColorScheme?)](/documentation/swiftui/view/preferredcolorscheme(_:))
- [var colorScheme: ColorScheme](/documentation/swiftui/environmentvalues/colorscheme)
- [ColorScheme](/documentation/swiftui/colorscheme) — cases: light, dark; init?(UIUserInterfaceStyle)
- [PreferredColorSchemeKey](/documentation/swiftui/preferredcolorschemekey)

### Getting the color scheme contrast

- [var colorSchemeContrast: ColorSchemeContrast](/documentation/swiftui/environmentvalues/colorschemecontrast)
- [ColorSchemeContrast](/documentation/swiftui/colorschemecontrast) — cases: standard, increased; init?(UIAccessibilityContrast)

### Configuring passthrough

- [func preferredSurroundingsEffect(SurroundingsEffect?)](/documentation/swiftui/view/preferredsurroundingseffect(_:))
- [SurroundingsEffect](/documentation/swiftui/surroundingseffect) — systemDark, dark, semiDark, ultraDark; colorMultiply(_:), dim(intensity:)
- [BreakthroughEffect](/documentation/swiftui/breakthrougheffect) — automatic, none, prominent, subtle

### Redacting private content

- [Designing your app for the Always On state](/documentation/watchos-apps/designing-your-app-for-the-always-on-state) (article)
- [func privacySensitive(Bool)](/documentation/swiftui/view/privacysensitive(_:))
- [func redacted(reason:)](/documentation/swiftui/view/redacted(reason:))
- [func unredacted()](/documentation/swiftui/view/unredacted())
- [var redactionReasons: RedactionReasons](/documentation/swiftui/environmentvalues/redactionreasons)
- [var isSceneCaptured: Bool](/documentation/swiftui/environmentvalues/isscenecaptured)
- [RedactionReasons](/documentation/swiftui/redactionreasons) — invalidated, placeholder, privacy; init(rawValue: Int)
- [View styles](/documentation/swiftui/view-styles) (article)

### Styling views with Liquid Glass

- [Applying Liquid Glass to custom views](/documentation/swiftui/applying-liquid-glass-to-custom-views) (article)
- [Landmarks: Building an app with Liquid Glass](/documentation/swiftui/landmarks-building-an-app-with-liquid-glass) (article)
- [Landmarks: Applying a background extension effect](/documentation/swiftui/landmarks-applying-a-background-extension-effect) (article)
- [Landmarks: Extending horizontal scrolling under a sidebar or inspector](/documentation/swiftui/landmarks-extending-horizontal-scrolling-under-a-sidebar-or-inspector) (article)
- [Landmarks: Refining the system provided Liquid Glass effect in toolbars](/documentation/swiftui/landmarks-refining-the-system-provided-glass-effect-in-toolbars) (article)
- [Landmarks: Displaying custom activity badges](/documentation/swiftui/landmarks-displaying-custom-activity-badges) (article)
- [func glassEffect(_:in:)](/documentation/swiftui/view/glasseffect(_:in:))
- [func interactive(Bool) -> Glass](/documentation/swiftui/glass/interactive(_:))
- [GlassEffectContainer](/documentation/swiftui/glasseffectcontainer) — init(spacing:content:)
- [GlassEffectTransition](/documentation/swiftui/glasseffecttransition) — identity, matchedGeometry, materialize
- [GlassButtonStyle](/documentation/swiftui/glassbuttonstyle) — init(), init(Glass)
- [GlassProminentButtonStyle](/documentation/swiftui/glassprominentbuttonstyle) — init()
- [DefaultGlassEffectShape](/documentation/swiftui/defaultglasseffectshape) — init()

### Styling buttons

- [func buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [ButtonStyle](/documentation/swiftui/buttonstyle) — protocol; makeBody(configuration:), Configuration, Body
- [ButtonStyleConfiguration](/documentation/swiftui/buttonstyleconfiguration) — label, isPressed, role
- [PrimitiveButtonStyle](/documentation/swiftui/primitivebuttonstyle) — built-in styles: automatic, accessoryBar, accessoryBarAction, bordered, borderedProminent, borderless, card, glass, glassProminent, glass(_:), link, plain
