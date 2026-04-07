# Views: Text and Images — SwiftUI Reference

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

- [func alert(_:isPresented:actions:)](/documentation/swiftui/view/alert(_:ispresented:actions:))
- [func alert(_:isPresented:presenting:actions:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:))
- [func alert<E, A>(isPresented: Binding<Bool>, error: E?, actions: () -> A) -> some View](/documentation/swiftui/view/alert(ispresented:error:actions:))

##### Alerts with a message

- [func alert(_:isPresented:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:actions:message:))
- [func alert(_:isPresented:presenting:actions:message:)](/documentation/swiftui/view/alert(_:ispresented:presenting:actions:message:))
- [func alert<E, A, M>(isPresented: Binding<Bool>, error: E?, actions: (E) -> A, message: (E) -> M) -> some View](/documentation/swiftui/view/alert(ispresented:error:actions:message:))

##### Confirmation dialogs

- [func confirmationDialog(_:isPresented:titleVisibility:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:))

##### Confirmation dialogs with a message

- [func confirmationDialog(_:isPresented:titleVisibility:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:actions:message:))
- [func confirmationDialog(_:isPresented:titleVisibility:presenting:actions:message:)](/documentation/swiftui/view/confirmationdialog(_:ispresented:titlevisibility:presenting:actions:message:))
- [func dismissalConfirmationDialog(_:shouldPresent:actions:message:)](/documentation/swiftui/view/dismissalconfirmationdialog(_:shouldpresent:actions:message:))

##### Dialog configuration

- [func dialogIcon(Image?) -> some View](/documentation/swiftui/view/dialogicon(_:))
- [func dialogSeverity(DialogSeverity) -> some View](/documentation/swiftui/view/dialogseverity(_:))
- [func dialogSuppressionToggle(isSuppressed: Binding<Bool>) -> some View](/documentation/swiftui/view/dialogsuppressiontoggle(issuppressed:))
- [func dialogSuppressionToggle(_:isSuppressed:)](/documentation/swiftui/view/dialogsuppressiontoggle(_:issuppressed:))

##### Sheets

- [func sheet<Content>(isPresented: Binding<Bool>, onDismiss: (() -> Void)?, content: () -> Content) -> some View](/documentation/swiftui/view/sheet(ispresented:ondismiss:content:))
- [func sheet<Item, Content>(item: Binding<Item?>, onDismiss: (() -> Void)?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/sheet(item:ondismiss:content:))
- [func fullScreenCover<Content>(isPresented: Binding<Bool>, onDismiss: (() -> Void)?, content: () -> Content) -> some View](/documentation/swiftui/view/fullscreencover(ispresented:ondismiss:content:))
- [func fullScreenCover<Item, Content>(item: Binding<Item?>, onDismiss: (() -> Void)?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/fullscreencover(item:ondismiss:content:))

##### Popovers

- [func popover<Item, Content>(item: Binding<Item?>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: (Item) -> Content) -> some View](/documentation/swiftui/view/popover(item:attachmentanchor:arrowedge:content:))
- [func popover<Content>(isPresented: Binding<Bool>, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, content: () -> Content) -> some View](/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:))

##### Sheet and popover configuration

- [func interactiveDismissDisabled(Bool) -> some View](/documentation/swiftui/view/interactivedismissdisabled(_:))
- [func presentationDetents(Set<PresentationDetent>) -> some View](/documentation/swiftui/view/presentationdetents(_:))
- [func presentationDetents(Set<PresentationDetent>, selection: Binding<PresentationDetent>) -> some View](/documentation/swiftui/view/presentationdetents(_:selection:))
- [func presentationDragIndicator(Visibility) -> some View](/documentation/swiftui/view/presentationdragindicator(_:))
- [func presentationBackground<S>(S) -> some View](/documentation/swiftui/view/presentationbackground(_:))
- [func presentationBackground<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/presentationbackground(alignment:content:))
- [func presentationBackgroundInteraction(PresentationBackgroundInteraction) -> some View](/documentation/swiftui/view/presentationbackgroundinteraction(_:))
- [func presentationCompactAdaptation(horizontal: PresentationAdaptation, vertical: PresentationAdaptation) -> some View](/documentation/swiftui/view/presentationcompactadaptation(horizontal:vertical:))
- [func presentationCompactAdaptation(PresentationAdaptation) -> some View](/documentation/swiftui/view/presentationcompactadaptation(_:))
- [func presentationContentInteraction(PresentationContentInteraction) -> some View](/documentation/swiftui/view/presentationcontentinteraction(_:))
- [func presentationCornerRadius(CGFloat?) -> some View](/documentation/swiftui/view/presentationcornerradius(_:))
- [func presentationSizing(some PresentationSizing) -> some View](/documentation/swiftui/view/presentationsizing(_:))

##### File exporter

- [func fileExporter(isPresented:document:contentType:defaultFilename:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttype:defaultfilename:oncompletion:))
- [func fileExporter(isPresented:documents:contentType:onCompletion:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttype:oncompletion:))
- [func fileExporter(isPresented:document:contentTypes:defaultFilename:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:document:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter(isPresented:documents:contentTypes:onCompletion:onCancellation:)](/documentation/swiftui/view/fileexporter(ispresented:documents:contenttypes:oncompletion:oncancellation:))
- [func fileExporter<T>(isPresented: Binding<Bool>, item: T?, contentTypes: [UTType], defaultFilename: String?, onCompletion: (Result<URL, any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileexporter(ispresented:item:contenttypes:defaultfilename:oncompletion:oncancellation:))
- [func fileExporter<C, T>(isPresented: Binding<Bool>, items: C, contentTypes: [UTType], onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileexporter(ispresented:items:contenttypes:oncompletion:oncancellation:))
- [func fileExporterFilenameLabel(_:)](/documentation/swiftui/view/fileexporterfilenamelabel(_:))

##### File importer

- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], allowsMultipleSelection: Bool, onCompletion: (Result<[URL], any Error>) -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:))
- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], onCompletion: (Result<URL, any Error>) -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:oncompletion:))
- [func fileImporter(isPresented: Binding<Bool>, allowedContentTypes: [UTType], allowsMultipleSelection: Bool, onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/fileimporter(ispresented:allowedcontenttypes:allowsmultipleselection:oncompletion:oncancellation:))

##### File mover

- [func fileMover(isPresented: Binding<Bool>, file: URL?, onCompletion: (Result<URL, any Error>) -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:))
- [func fileMover<C>(isPresented: Binding<Bool>, files: C, onCompletion: (Result<[URL], any Error>) -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:))
- [func fileMover(isPresented: Binding<Bool>, file: URL?, onCompletion: (Result<URL, any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:file:oncompletion:oncancellation:))
- [func fileMover<C>(isPresented: Binding<Bool>, files: C, onCompletion: (Result<[URL], any Error>) -> Void, onCancellation: () -> Void) -> some View](/documentation/swiftui/view/filemover(ispresented:files:oncompletion:oncancellation:))

##### File dialog configuration

- [func fileDialogBrowserOptions(FileDialogBrowserOptions) -> some View](/documentation/swiftui/view/filedialogbrowseroptions(_:))
- [func fileDialogConfirmationLabel(_:)](/documentation/swiftui/view/filedialogconfirmationlabel(_:))
- [func fileDialogCustomizationID(String) -> some View](/documentation/swiftui/view/filedialogcustomizationid(_:))
- [func fileDialogDefaultDirectory(URL?) -> some View](/documentation/swiftui/view/filedialogdefaultdirectory(_:))
- [func fileDialogImportsUnresolvedAliases(Bool) -> some View](/documentation/swiftui/view/filedialogimportsunresolvedaliases(_:))
- [func fileDialogMessage(_:)](/documentation/swiftui/view/filedialogmessage(_:))
- [func fileDialogURLEnabled(Predicate<URL>) -> some View](/documentation/swiftui/view/filedialogurlenabled(_:))

##### Inspectors

- [func inspector<V>(isPresented: Binding<Bool>, content: () -> V) -> some View](/documentation/swiftui/view/inspector(ispresented:content:))
- [func inspectorColumnWidth(CGFloat) -> some View](/documentation/swiftui/view/inspectorcolumnwidth(_:))
- [func inspectorColumnWidth(min: CGFloat?, ideal: CGFloat, max: CGFloat?) -> some View](/documentation/swiftui/view/inspectorcolumnwidth(min:ideal:max:))

##### Quick look previews

- [func quickLookPreview(Binding<URL?>) -> some View](/documentation/swiftui/view/quicklookpreview(_:))
- [func quickLookPreview<Items>(Binding<Items.Element?>, in: Items) -> some View](/documentation/swiftui/view/quicklookpreview(_:in:))

##### Family Sharing

- [func familyActivityPicker(isPresented: Binding<Bool>, selection: Binding<FamilyActivitySelection>) -> some View](/documentation/swiftui/view/familyactivitypicker(ispresented:selection:))
- [func familyActivityPicker(headerText: String?, footerText: String?, isPresented: Binding<Bool>, selection: Binding<FamilyActivitySelection>) -> some View](/documentation/swiftui/view/familyactivitypicker(headertext:footertext:ispresented:selection:))

##### Live Activities

- [func activitySystemActionForegroundColor(Color?) -> some View](/documentation/swiftui/view/activitysystemactionforegroundcolor(_:))
- [func activityBackgroundTint(Color?) -> some View](/documentation/swiftui/view/activitybackgroundtint(_:))

##### Apple Music

- [func musicSubscriptionOffer(isPresented: Binding<Bool>, options: MusicSubscriptionOffer.Options, onLoadCompletion: ((any Error)?) -> Void) -> some View](/documentation/swiftui/view/musicsubscriptionoffer(ispresented:options:onloadcompletion:))

##### StoreKit

- [func appStoreOverlay(isPresented: Binding<Bool>, configuration: () -> SKOverlay.Configuration) -> some View](/documentation/swiftui/view/appstoreoverlay(ispresented:configuration:))
- [func manageSubscriptionsSheet(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/managesubscriptionssheet(ispresented:))
- [func refundRequestSheet(for: Transaction.ID, isPresented: Binding<Bool>, onDismiss: ((Result<Transaction.RefundRequestStatus, Transaction.RefundRequestError>) -> ())?) -> some View](/documentation/swiftui/view/refundrequestsheet(for:ispresented:ondismiss:))
- [func offerCodeRedemption(isPresented: Binding<Bool>, onCompletion: (Result<Void, any Error>) -> Void) -> some View](/documentation/swiftui/view/offercoderedemption(ispresented:oncompletion:))

##### PhotoKit

- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<PhotosPickerItem?>, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<PhotosPickerItem?>, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy, photoLibrary: PHPhotoLibrary) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:matching:preferreditemencoding:photolibrary:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<[PhotosPickerItem]>, maxSelectionCount: Int?, selectionBehavior: PhotosPickerSelectionBehavior, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:))
- [func photosPicker(isPresented: Binding<Bool>, selection: Binding<[PhotosPickerItem]>, maxSelectionCount: Int?, selectionBehavior: PhotosPickerSelectionBehavior, matching: PHPickerFilter?, preferredItemEncoding: PhotosPickerItem.EncodingDisambiguationPolicy, photoLibrary: PHPhotoLibrary) -> some View](/documentation/swiftui/view/photospicker(ispresented:selection:maxselectioncount:selectionbehavior:matching:preferreditemencoding:photolibrary:))
- [func photosPickerAccessoryVisibility(Visibility, edges: Edge.Set) -> some View](/documentation/swiftui/view/photospickeraccessoryvisibility(_:edges:))
- [func photosPickerDisabledCapabilities(PHPickerCapabilities) -> some View](/documentation/swiftui/view/photospickerdisabledcapabilities(_:))
- [func photosPickerStyle(PhotosPickerStyle) -> some View](/documentation/swiftui/view/photospickerstyle(_:))

##### Translation

- [func translationPresentation(isPresented: Binding<Bool>, text: String, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge, replacementAction: ((String) -> Void)?) -> some View](/documentation/swiftui/view/translationpresentation(ispresented:text:attachmentanchor:arrowedge:replacementaction:))
- [func translationTask(TranslationSession.Configuration?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(_:action:))
- [func translationTask(source: Locale.Language?, target: Locale.Language?, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(source:target:action:))
- [func translationTask(source: Locale.Language?, target: Locale.Language?, preferredStrategy: TranslationSession.Strategy, action: (TranslationSession) async -> Void) -> some View](/documentation/swiftui/view/translationtask(source:target:preferredstrategy:action:))
- [State modifiers](/documentation/swiftui/view-state)

##### Identity

- [func tag<V>(V, includeOptional: Bool) -> some View](/documentation/swiftui/view/tag(_:includeoptional:))
- [func id<ID>(ID) -> some View](/documentation/swiftui/view/id(_:))
- [func equatable() -> EquatableView<Self>](/documentation/swiftui/view/equatable())

##### Environment values

- [func environment<T>(T?) -> some View](/documentation/swiftui/view/environment(_:))
- [func environment<V>(WritableKeyPath<EnvironmentValues, V>, V) -> some View](/documentation/swiftui/view/environment(_:_:))
- [func environmentObject<T>(T) -> some View](/documentation/swiftui/view/environmentobject(_:))
- [func transformEnvironment<V>(WritableKeyPath<EnvironmentValues, V>, transform: (inout V) -> Void) -> some View](/documentation/swiftui/view/transformenvironment(_:transform:))

##### Preferences

- [func preference<K>(key: K.Type, value: K.Value) -> some View](/documentation/swiftui/view/preference(key:value:))
- [func transformPreference<K>(K.Type, (inout K.Value) -> Void) -> some View](/documentation/swiftui/view/transformpreference(_:_:))
- [func anchorPreference<A, K>(key: K.Type, value: Anchor<A>.Source, transform: (Anchor<A>) -> K.Value) -> some View](/documentation/swiftui/view/anchorpreference(key:value:transform:))
- [func transformAnchorPreference<A, K>(key: K.Type, value: Anchor<A>.Source, transform: (inout K.Value, Anchor<A>) -> Void) -> some View](/documentation/swiftui/view/transformanchorpreference(key:value:transform:))
- [func onPreferenceChange<K>(K.Type, perform: (K.Value) -> Void) -> some View](/documentation/swiftui/view/onpreferencechange(_:perform:))
- [func backgroundPreferenceValue<Key, T>(Key.Type, (Key.Value) -> T) -> some View](/documentation/swiftui/view/backgroundpreferencevalue(_:_:))
- [func backgroundPreferenceValue<K, V>(K.Type, alignment: Alignment, (K.Value) -> V) -> some View](/documentation/swiftui/view/backgroundpreferencevalue(_:alignment:_:))
- [func overlayPreferenceValue<Key, T>(Key.Type, (Key.Value) -> T) -> some View](/documentation/swiftui/view/overlaypreferencevalue(_:_:))
- [func overlayPreferenceValue<K, V>(K.Type, alignment: Alignment, (K.Value) -> V) -> some View](/documentation/swiftui/view/overlaypreferencevalue(_:alignment:_:))

##### Default storage

- [func defaultAppStorage(UserDefaults) -> some View](/documentation/swiftui/view/defaultappstorage(_:))

##### Configuring a model

- [func modelContext(ModelContext) -> some View](/documentation/swiftui/view/modelcontext(_:))
- [func modelContainer(ModelContainer) -> some View](/documentation/swiftui/view/modelcontainer(_:))
- [func modelContainer(for:inMemory:isAutosaveEnabled:isUndoEnabled:onSetup:)](/documentation/swiftui/view/modelcontainer(for:inmemory:isautosaveenabled:isundoenabled:onsetup:))

#### Deprecated modifiers

- [Deprecated modifiers](/documentation/swiftui/view-deprecated)

##### Accessibility modifiers

- [func accessibility(label: Text) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(label:))
- [func accessibility(value: Text) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(value:))
- [func accessibility(hidden: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(hidden:))
- [func accessibility(identifier: String) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(identifier:))
- [func accessibility(selectionIdentifier: AnyHashable) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(selectionidentifier:))
- [func accessibility(hint: Text) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(hint:))
- [func accessibility(activationPoint:)](/documentation/swiftui/view/accessibility(activationpoint:))
- [func accessibility(inputLabels: [Text]) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(inputlabels:))
- [func accessibility(addTraits: AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(addtraits:))
- [func accessibility(removeTraits: AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(removetraits:))
- [func accessibility(sortPriority: Double) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibility(sortpriority:))

##### Appearance modifiers

- [func colorScheme(ColorScheme) -> some View](/documentation/swiftui/view/colorscheme(_:))
- [func listRowPlatterColor(Color?) -> some View](/documentation/swiftui/view/listrowplattercolor(_:))
- [func background<Background>(Background, alignment: Alignment) -> some View](/documentation/swiftui/view/background(_:alignment:))
- [func overlay<Overlay>(Overlay, alignment: Alignment) -> some View](/documentation/swiftui/view/overlay(_:alignment:))
- [func foregroundColor(Color?) -> some View](/documentation/swiftui/view/foregroundcolor(_:))
- [func complicationForeground() -> some View](/documentation/swiftui/view/complicationforeground())

##### Text modifiers

- [func autocapitalization(UITextAutocapitalizationType) -> some View](/documentation/swiftui/view/autocapitalization(_:))
- [func disableAutocorrection(Bool?) -> some View](/documentation/swiftui/view/disableautocorrection(_:))

##### Auxiliary view modifiers

- [func navigationBarTitle(_:)](/documentation/swiftui/view/navigationbartitle(_:))
- [func navigationBarTitle(_:displayMode:)](/documentation/swiftui/view/navigationbartitle(_:displaymode:))
- [func navigationBarItems<L>(leading: L) -> some View](/documentation/swiftui/view/navigationbaritems(leading:))
- [func navigationBarItems<L, T>(leading: L, trailing: T) -> some View](/documentation/swiftui/view/navigationbaritems(leading:trailing:))
- [func navigationBarItems<T>(trailing: T) -> some View](/documentation/swiftui/view/navigationbaritems(trailing:))
- [func navigationBarHidden(Bool) -> some View](/documentation/swiftui/view/navigationbarhidden(_:))
- [func statusBar(hidden: Bool) -> some View](/documentation/swiftui/view/statusbar(hidden:))
- [func contextMenu<MenuItems>(ContextMenu<MenuItems>?) -> some View](/documentation/swiftui/view/contextmenu(_:))

##### Style modifiers

- [func menuButtonStyle<S>(S) -> some View](/documentation/swiftui/view/menubuttonstyle(_:))
- [func navigationViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationviewstyle(_:))

##### Layout modifiers

- [func frame() -> some View](/documentation/swiftui/view/frame())
- [func edgesIgnoringSafeArea(Edge.Set) -> some View](/documentation/swiftui/view/edgesignoringsafearea(_:))
- [func coordinateSpace<T>(name: T) -> some View](/documentation/swiftui/view/coordinatespace(name:))

##### Graphics and rendering modifiers

- [func accentColor(Color?) -> some View](/documentation/swiftui/view/accentcolor(_:))
- [func mask<Mask>(Mask) -> some View](/documentation/swiftui/view/mask(_:))
- [func animation(Animation?) -> some View](/documentation/swiftui/view/animation(_:)-1hc0p)
- [func cornerRadius(CGFloat, antialiased: Bool) -> some View](/documentation/swiftui/view/cornerradius(_:antialiased:))

##### Input and events modifiers

- [func onChange<V>(of: V, perform: (V) -> Void) -> some View](/documentation/swiftui/view/onchange(of:perform:))
- [func onTapGesture(count: Int, coordinateSpace: CoordinateSpace, perform: (CGPoint) -> Void) -> some View](/documentation/swiftui/view/ontapgesture(count:coordinatespace:perform:)-36x9h)
- [func onLongPressGesture(minimumDuration: Double, maximumDistance: CGFloat, pressing: ((Bool) -> Void)?, perform: () -> Void) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:maximumdistance:pressing:perform:))
- [func onLongPressGesture(minimumDuration: Double, pressing: ((Bool) -> Void)?, perform: () -> Void) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:pressing:perform:))
- [func onPasteCommand(of: [String], perform: ([NSItemProvider]) -> Void) -> some View](/documentation/swiftui/view/onpastecommand(of:perform:)-4f78f)
- [func onPasteCommand<Payload>(of: [String], validator: ([NSItemProvider]) -> Payload?, perform: (Payload) -> Void) -> some View](/documentation/swiftui/view/onpastecommand(of:validator:perform:)-964k1)
- [func onDrop(of: [String], delegate: any DropDelegate) -> some View](/documentation/swiftui/view/ondrop(of:delegate:)-2vr9o)
- [func onDrop(of:isTargeted:perform:)](/documentation/swiftui/view/ondrop(of:istargeted:perform:))
- [func focusable(Bool, onFocusChange: (Bool) -> Void) -> some View](/documentation/swiftui/view/focusable(_:onfocuschange:))
- [func onContinuousHover(coordinateSpace: CoordinateSpace, perform: (HoverPhase) -> Void) -> some View](/documentation/swiftui/view/oncontinuoushover(coordinatespace:perform:)-8gyrl)

##### View presentation modifiers

- [func actionSheet(isPresented: Binding<Bool>, content: () -> ActionSheet) -> some View](/documentation/swiftui/view/actionsheet(ispresented:content:))
- [func actionSheet<T>(item: Binding<T?>, content: (T) -> ActionSheet) -> some View](/documentation/swiftui/view/actionsheet(item:content:))
- [func alert(isPresented: Binding<Bool>, content: () -> Alert) -> some View](/documentation/swiftui/view/alert(ispresented:content:))
- [func alert<Item>(item: Binding<Item?>, content: (Item) -> Alert) -> some View](/documentation/swiftui/view/alert(item:content:))

##### Search modifiers

- [func searchable(text:placement:prompt:suggestions:)](/documentation/swiftui/view/searchable(text:placement:prompt:suggestions:))

##### Tab modifiers

- [func tabItem<V>(() -> V) -> some View](/documentation/swiftui/view/tabitem(_:))

#### Instance Methods

- [func accessibilityActions<Content>(category: AccessibilityActionCategory, () -> Content) -> some View](/documentation/swiftui/view/accessibilityactions(category:_:))
- [func accessibilityDefaultFocus<Value>(AccessibilityFocusState<Value>.Binding, Value) -> some View](/documentation/swiftui/view/accessibilitydefaultfocus(_:_:))
- [func accessibilityScrollStatus(_:isEnabled:)](/documentation/swiftui/view/accessibilityscrollstatus(_:isenabled:))
- [func addOrderToWalletButtonStyle(AddOrderToWalletButtonStyle) -> some View](/documentation/swiftui/view/addordertowalletbuttonstyle(_:))
- [func addPassToWalletButtonStyle(AddPassToWalletButtonStyle) -> some View](/documentation/swiftui/view/addpasstowalletbuttonstyle(_:))
- [func allowsWindowActivationEvents() -> some View](/documentation/swiftui/view/allowswindowactivationevents())
- [func appStoreMerchandising(isPresented: Binding<Bool>, kind: AppStoreMerchandisingKind, onDismiss: ((Result<AppStoreMerchandisingKind.PresentationResult, any Error>) async -> ())?) -> some View](/documentation/swiftui/view/appstoremerchandising(ispresented:kind:ondismiss:))
- [func aspectRatio3D(Size3D?, contentMode: ContentMode) -> some View](/documentation/swiftui/view/aspectratio3d(_:contentmode:))
- [func assistiveAccessNavigationIcon(Image) -> some View](/documentation/swiftui/view/assistiveaccessnavigationicon(_:))
- [func assistiveAccessNavigationIcon(systemImage: String) -> some View](/documentation/swiftui/view/assistiveaccessnavigationicon(systemimage:))
- [func attributedTextFormattingDefinition(_:)](/documentation/swiftui/view/attributedtextformattingdefinition(_:))
- [func automatedDeviceEnrollmentAddition(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/automateddeviceenrollmentaddition(ispresented:))
- [func backgroundExtensionEffect() -> some View](/documentation/swiftui/view/backgroundextensioneffect())
- [func backgroundExtensionEffect(isEnabled: Bool) -> some View](/documentation/swiftui/view/backgroundextensioneffect(isenabled:))
- [func breakthroughEffect(BreakthroughEffect) -> some View](/documentation/swiftui/view/breakthrougheffect(_:))
- [func buttonSizing(ButtonSizing) -> some View](/documentation/swiftui/view/buttonsizing(_:))
- [func certificateSheet(trust: Binding<SecTrust?>, title: String?, message: String?, help: URL?) -> some View](/documentation/swiftui/view/certificatesheet(trust:title:message:help:))
- [func chart3DCameraProjection(Chart3DCameraProjection) -> some View](/documentation/swiftui/view/chart3dcameraprojection(_:))
- [func chart3DPose(_:)](/documentation/swiftui/view/chart3dpose(_:))
- [func chart3DRenderingStyle(Chart3DRenderingStyle) -> some View](/documentation/swiftui/view/chart3drenderingstyle(_:))
- [func chartZAxis(Visibility) -> some View](/documentation/swiftui/view/chartzaxis(_:))
- [func chartZAxis<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/chartzaxis(content:))
- [func chartZAxisLabel(_:position:alignment:spacing:)](/documentation/swiftui/view/chartzaxislabel(_:position:alignment:spacing:))
- [func chartZScale<Domain, Range>(domain: Domain, range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartzscale(domain:range:type:))
- [func chartZScale<Domain>(domain: Domain, type: ScaleType?) -> some View](/documentation/swiftui/view/chartzscale(domain:type:))
- [func chartZScale<Range>(range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartzscale(range:type:))
- [func chartZSelection<P>(range: Binding<ClosedRange<P>?>) -> some View](/documentation/swiftui/view/chartzselection(range:))
- [func chartZSelection<P>(value: Binding<P?>) -> some View](/documentation/swiftui/view/chartzselection(value:))
- [func contactAccessButtonCaption(ContactAccessButton.Caption) -> some View](/documentation/swiftui/view/contactaccessbuttoncaption(_:))
- [func contactAccessButtonStyle(ContactAccessButton.Style) -> some View](/documentation/swiftui/view/contactaccessbuttonstyle(_:))
- [func contactAccessPicker(isPresented: Binding<Bool>, completionHandler: ([String]) -> Void) -> some View](/documentation/swiftui/view/contactaccesspicker(ispresented:completionhandler:))
- [func containerCornerOffset(Edge.Set, sizeToFit: Bool) -> some View](/documentation/swiftui/view/containercorneroffset(_:sizetofit:))
- [func containerValue<V>(WritableKeyPath<ContainerValues, V>, V) -> some View](/documentation/swiftui/view/containervalue(_:_:))
- [func contentCaptureProtected(Bool) -> some View](/documentation/swiftui/view/contentcaptureprotected(_:))
- [func contentToolbar(for:content:)](/documentation/swiftui/view/contenttoolbar(for:content:))
- [func continuityDevicePicker(isPresented: Binding<Bool>, onDidConnect: ((AVContinuityDevice?) -> Void)?) -> some View](/documentation/swiftui/view/continuitydevicepicker(ispresented:ondidconnect:))
- [func controlWidgetActionHint(_:)](/documentation/swiftui/view/controlwidgetactionhint(_:))
- [func controlWidgetStatus(_:)](/documentation/swiftui/view/controlwidgetstatus(_:))
- [func currentEntitlementTask(for: String, priority: TaskPriority, action: (EntitlementTaskState<VerificationResult<Transaction>?>) async -> ()) -> some View](/documentation/swiftui/view/currententitlementtask(for:priority:action:))
- [func dialogPreventsAppTermination(Bool?) -> some View](/documentation/swiftui/view/dialogpreventsapptermination(_:))
- [func documentBrowserContextMenu(([URL]?) -> some View) -> some View](/documentation/swiftui/view/documentbrowsercontextmenu(_:))
- [func dragConfiguration(DragConfiguration) -> some View](/documentation/swiftui/view/dragconfiguration(_:))
- [func dragContainer(for:in:_:)](/documentation/swiftui/view/dragcontainer(for:in:_:))
- [func dragContainer(for:itemID:in:_:)](/documentation/swiftui/view/dragcontainer(for:itemid:in:_:))
- [func dragContainerSelection<ItemID>(@autoclosure () -> Array<ItemID>, containerNamespace: Namespace.ID?) -> some View](/documentation/swiftui/view/dragcontainerselection(_:containernamespace:))
- [func dragPreviewsFormation(DragDropPreviewsFormation) -> some View](/documentation/swiftui/view/dragpreviewsformation(_:))
- [func draggable<Item>(Item.Type, containerNamespace: Namespace.ID?, () -> Item?) -> some View](/documentation/swiftui/view/draggable(_:containernamespace:_:))
- [func draggable<Item, ItemID>(Item.Type, id: KeyPath<Item, ItemID>, containerNamespace: Namespace.ID?, () -> Item?) -> some View](/documentation/swiftui/view/draggable(_:id:containernamespace:_:))
- [func draggable<Item, ItemID>(Item.Type, id: KeyPath<Item, ItemID>, item: @autoclosure () -> Item?, containerNamespace: Namespace.ID?) -> some View](/documentation/swiftui/view/draggable(_:id:item:containernamespace:))
- [func draggable<Item>(Item.Type, item: @autoclosure () -> Item?, containerNamespace: Namespace.ID?) -> some View](/documentation/swiftui/view/draggable(_:item:containernamespace:))
- [func draggable<ItemID>(containerItemID: ItemID, containerNamespace: Namespace.ID?) -> some View](/documentation/swiftui/view/draggable(containeritemid:containernamespace:))
- [func dropConfiguration((DropSession) -> DropConfiguration) -> some View](/documentation/swiftui/view/dropconfiguration(_:))
- [func dropDestination<T>(for: T.Type, isEnabled: Bool, action: ([T], DropSession) -> Void) -> some View](/documentation/swiftui/view/dropdestination(for:isenabled:action:))
- [func dropPreviewsFormation(DragDropPreviewsFormation) -> some View](/documentation/swiftui/view/droppreviewsformation(_:))
- [func familyActivityPicker(title: String?, headerText: String?, footerText: String?, isPresented: Binding<Bool>, selection: Binding<FamilyActivitySelection>) -> some View](/documentation/swiftui/view/familyactivitypicker(title:headertext:footertext:ispresented:selection:))
- [func formStyle<S>(S) -> some View](/documentation/swiftui/view/formstyle(_:))
- [func foveatedStreamingPauseSheet(session: Binding<FoveatedStreamingSession?>) -> some View](/documentation/swiftui/view/foveatedstreamingpausesheet(session:))
- [func gameSaveSyncingAlert(directory: Binding<GameSaveSyncedDirectory?>, finishedLoading: () -> Void) -> some View](/documentation/swiftui/view/gamesavesyncingalert(directory:finishedloading:))
- [func glassBackgroundEffect<S>(S, displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(_:displaymode:))
- [func glassBackgroundEffect<T, S>(S, in: T, displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(_:in:displaymode:))
- [func glassEffect(Glass, in: some Shape) -> some View](/documentation/swiftui/view/glasseffect(_:in:))
- [func glassEffectID((some Hashable & Sendable)?, in: Namespace.ID) -> some View](/documentation/swiftui/view/glasseffectid(_:in:))
- [func glassEffectTransition(GlassEffectTransition) -> some View](/documentation/swiftui/view/glasseffecttransition(_:))
- [func glassEffectUnion(id: (some Hashable & Sendable)?, namespace: Namespace.ID) -> some View](/documentation/swiftui/view/glasseffectunion(id:namespace:))
- [func groupActivityAssociation(GroupActivityAssociationKind?) -> some View](/documentation/swiftui/view/groupactivityassociation(_:))
- [func handGestureShortcut(HandGestureShortcut, isEnabled: Bool) -> some View](/documentation/swiftui/view/handgestureshortcut(_:isenabled:))
- [func handPointerBehavior(HandPointerBehavior?) -> some View](/documentation/swiftui/view/handpointerbehavior(_:))
- [func handlesGameControllerEvents(matching: GCUIEventTypes) -> some View](/documentation/swiftui/view/handlesgamecontrollerevents(matching:))
- [func handlesGameControllerEvents(matching: GCUIEventTypes, withOptions: GameControllerEventHandlingOptions?) -> some View](/documentation/swiftui/view/handlesgamecontrollerevents(matching:withoptions:))
- [func healthDataAccessRequest(store: HKHealthStore, objectType: HKObjectType, predicate: NSPredicate?, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:objecttype:predicate:trigger:completion:))
- [func healthDataAccessRequest(store: HKHealthStore, readTypes: Set<HKObjectType>, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:readtypes:trigger:completion:))
- [func healthDataAccessRequest(store: HKHealthStore, shareTypes: Set<HKSampleType>, readTypes: Set<HKObjectType>?, trigger: some Equatable, completion: (Result<Bool, any Error>) -> Void) -> some View](/documentation/swiftui/view/healthdataaccessrequest(store:sharetypes:readtypes:trigger:completion:))
- [func imagePlaygroundGenerationStyle(ImagePlaygroundStyle, in: [ImagePlaygroundStyle]) -> some View](/documentation/swiftui/view/imageplaygroundgenerationstyle(_:in:))
- [func imagePlaygroundOptions(ImagePlaygroundOptions) -> some View](/documentation/swiftui/view/imageplaygroundoptions(_:))
- [func imagePlaygroundPersonalizationPolicy(ImagePlaygroundPersonalizationPolicy) -> some View](/documentation/swiftui/view/imageplaygroundpersonalizationpolicy(_:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concept: String, sourceImage: Image?, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concept:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concept: String, sourceImageURL: URL, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concept:sourceimageurl:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concepts: [ImagePlaygroundConcept], sourceImage: Image?, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimage:oncompletion:oncancellation:))
- [func imagePlaygroundSheet(isPresented: Binding<Bool>, concepts: [ImagePlaygroundConcept], sourceImageURL: URL, onCompletion: (URL) -> Void, onCancellation: (() -> Void)?) -> some View](/documentation/swiftui/view/imageplaygroundsheet(ispresented:concepts:sourceimageurl:oncompletion:oncancellation:))
- [func immersiveEnvironmentPicker<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/immersiveenvironmentpicker(content:))
- [func inAppPurchaseOptions(((Product) async -> Set<Product.PurchaseOption>)?) -> some View](/documentation/swiftui/view/inapppurchaseoptions(_:))
- [func journalingSuggestionsPicker(isPresented: Binding<Bool>, journalingSuggestionToken: JournalingSuggestionPresentationToken?, onCompletion: (JournalingSuggestion) async -> Void) -> some View](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:journalingsuggestiontoken:oncompletion:))
- [func journalingSuggestionsPicker(isPresented: Binding<Bool>, onCompletion: (JournalingSuggestion) async -> Void) -> some View](/documentation/swiftui/view/journalingsuggestionspicker(ispresented:oncompletion:))
- [func labelIconToTitleSpacing(CGFloat) -> some View](/documentation/swiftui/view/labelicontotitlespacing(_:))
- [func labelReservedIconWidth(CGFloat) -> some View](/documentation/swiftui/view/labelreservediconwidth(_:))
- [func labeledContentStyle<S>(S) -> some View](/documentation/swiftui/view/labeledcontentstyle(_:))
- [func labelsVisibility(Visibility) -> some View](/documentation/swiftui/view/labelsvisibility(_:))
- [func lineHeight(AttributedString.LineHeight?) -> some View](/documentation/swiftui/view/lineheight(_:))
- [func listRowInsets(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/listrowinsets(_:_:))
- [func listSectionIndexVisibility(Visibility) -> some View](/documentation/swiftui/view/listsectionindexvisibility(_:))
- [func listSectionMargins(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/listsectionmargins(_:_:))
- [func lookAroundViewer(isPresented: Binding<Bool>, initialScene: MKLookAroundScene?, allowsNavigation: Bool, showsRoadLabels: Bool, pointsOfInterest: PointOfInterestCategories, onDismiss: (() -> Void)?) -> some View](/documentation/swiftui/view/lookaroundviewer(ispresented:initialscene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func lookAroundViewer(isPresented: Binding<Bool>, scene: Binding<MKLookAroundScene?>, allowsNavigation: Bool, showsRoadLabels: Bool, pointsOfInterest: PointOfInterestCategories, onDismiss: (() -> Void)?) -> some View](/documentation/swiftui/view/lookaroundviewer(ispresented:scene:allowsnavigation:showsroadlabels:pointsofinterest:ondismiss:))
- [func manageSubscriptionsSheet(isPresented: Binding<Bool>, subscriptionGroupID: String) -> some View](/documentation/swiftui/view/managesubscriptionssheet(ispresented:subscriptiongroupid:))
- [func managedContentStyle(ManagedContentStyle) -> some View](/documentation/swiftui/view/managedcontentstyle(_:))
- [func manipulable(coordinateSpace: some CoordinateSpaceProtocol, operations: Manipulable.Operation.Set, inertia: Manipulable.Inertia, isEnabled: Bool, onChanged: ((Manipulable.Event) -> Void)?) -> some View](/documentation/swiftui/view/manipulable(coordinatespace:operations:inertia:isenabled:onchanged:))
- [func manipulable(transform: Binding<AffineTransform3D>, coordinateSpace: some CoordinateSpaceProtocol, operations: Manipulable.Operation.Set, inertia: Manipulable.Inertia, isEnabled: Bool, onChanged: ((Manipulable.Event) -> Void)?) -> some View](/documentation/swiftui/view/manipulable(transform:coordinatespace:operations:inertia:isenabled:onchanged:))
- [func manipulable(using: Manipulable.GestureState) -> some View](/documentation/swiftui/view/manipulable(using:))
- [func manipulationGesture(updating: Binding<Manipulable.GestureState>, coordinateSpace: some CoordinateSpaceProtocol, operations: Manipulable.Operation.Set, inertia: Manipulable.Inertia, isEnabled: Bool, onChanged: ((Manipulable.Event) -> Void)?) -> some View](/documentation/swiftui/view/manipulationgesture(updating:coordinatespace:operations:inertia:isenabled:onchanged:))
- [func mapCameraKeyframeAnimator(trigger: some Equatable, keyframes: (MapCamera) -> some Keyframes<MapCamera>) -> some View](/documentation/swiftui/view/mapcamerakeyframeanimator(trigger:keyframes:))
- [func mapControlVisibility(Visibility) -> some View](/documentation/swiftui/view/mapcontrolvisibility(_:))
- [func mapControls(() -> some View) -> some View](/documentation/swiftui/view/mapcontrols(_:))
- [func mapFeatureSelectionAccessory(MapItemDetailSelectionAccessoryStyle?) -> some View](/documentation/swiftui/view/mapfeatureselectionaccessory(_:))
- [func mapFeatureSelectionContent(content: (MapFeature) -> some MapContent) -> some View](/documentation/swiftui/view/mapfeatureselectioncontent(content:))
- [func mapFeatureSelectionDisabled((MapFeature) -> Bool) -> some View](/documentation/swiftui/view/mapfeatureselectiondisabled(_:))
- [func mapItemDetailPopover(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor) -> some View](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge) -> some View](/documentation/swiftui/view/mapitemdetailpopover(ispresented:item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailPopover(item: Binding<MKMapItem?>, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor) -> some View](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:))
- [func mapItemDetailPopover(item: Binding<MKMapItem?>, displaysMap: Bool, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge) -> some View](/documentation/swiftui/view/mapitemdetailpopover(item:displaysmap:attachmentanchor:arrowedge:))
- [func mapItemDetailSheet(isPresented: Binding<Bool>, item: MKMapItem?, displaysMap: Bool) -> some View](/documentation/swiftui/view/mapitemdetailsheet(ispresented:item:displaysmap:))
- [func mapItemDetailSheet(item: Binding<MKMapItem?>, displaysMap: Bool) -> some View](/documentation/swiftui/view/mapitemdetailsheet(item:displaysmap:))
- [func mapScope(Namespace.ID) -> some View](/documentation/swiftui/view/mapscope(_:))
- [func mapStyle(MapStyle) -> some View](/documentation/swiftui/view/mapstyle(_:))
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:))
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID, configuration: (EmptyMatchedTransitionSourceConfiguration) -> some MatchedTransitionSourceConfiguration) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:configuration:))
- [func materialActiveAppearance(MaterialActiveAppearance) -> some View](/documentation/swiftui/view/materialactiveappearance(_:))
- [func navigationLinkIndicatorVisibility(Visibility) -> some View](/documentation/swiftui/view/navigationlinkindicatorvisibility(_:))
- [func navigationTransition(some NavigationTransition) -> some View](/documentation/swiftui/view/navigationtransition(_:))
- [func onAppIntentExecution<I>(I.Type, perform: (I) -> Void) -> some View](/documentation/swiftui/view/onappintentexecution(_:perform:))
- [func onApplePayCouponCodeChange(perform: (String) async -> PKPaymentRequestCouponCodeUpdate) -> some View](/documentation/swiftui/view/onapplepaycouponcodechange(perform:))
- [func onApplePayPaymentMethodChange(perform: (PKPaymentMethod) async -> PKPaymentRequestPaymentMethodUpdate) -> some View](/documentation/swiftui/view/onapplepaypaymentmethodchange(perform:))
- [func onApplePayShippingContactChange(perform: (PKContact) async -> PKPaymentRequestShippingContactUpdate) -> some View](/documentation/swiftui/view/onapplepayshippingcontactchange(perform:))
- [func onApplePayShippingMethodChange(perform: (PKShippingMethod) async -> PKPaymentRequestShippingMethodUpdate) -> some View](/documentation/swiftui/view/onapplepayshippingmethodchange(perform:))
- [func onCameraCaptureEvent(isEnabled:defaultSoundDisabled:action:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:defaultsounddisabled:action:))
- [func onCameraCaptureEvent(isEnabled:defaultSoundDisabled:primaryAction:secondaryAction:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:defaultsounddisabled:primaryaction:secondaryaction:))
- [func onDragSessionUpdated((DragSession) -> Void) -> some View](/documentation/swiftui/view/ondragsessionupdated(_:))
- [func onDropSessionUpdated((DropSession) -> Void) -> some View](/documentation/swiftui/view/ondropsessionupdated(_:))
- [func onGeometryChange3D(for:of:action:)](/documentation/swiftui/view/ongeometrychange3d(for:of:action:))
- [func onInAppPurchaseCompletion(perform: ((Product, Result<Product.PurchaseResult, any Error>) async -> ())?) -> some View](/documentation/swiftui/view/oninapppurchasecompletion(perform:))
- [func onInAppPurchaseStart(perform: ((Product) async -> ())?) -> some View](/documentation/swiftui/view/oninapppurchasestart(perform:))
- [func onInteractiveResizeChange((Bool) -> Void) -> some View](/documentation/swiftui/view/oninteractiveresizechange(_:))
- [func onMapCameraChange(frequency:_:)](/documentation/swiftui/view/onmapcamerachange(frequency:_:))
- [func onOpenURL(prefersInApp: Bool) -> some View](/documentation/swiftui/view/onopenurl(prefersinapp:))
- [func onWorldRecenter(action:)](/documentation/swiftui/view/onworldrecenter(action:))
- [func payLaterViewAction(PayLaterViewAction) -> some View](/documentation/swiftui/view/paylaterviewaction(_:))
- [func payLaterViewDisplayStyle(PayLaterViewDisplayStyle) -> some View](/documentation/swiftui/view/paylaterviewdisplaystyle(_:))
- [func payWithApplePayButtonDisableCardArt() -> some View](/documentation/swiftui/view/paywithapplepaybuttondisablecardart())
- [func payWithApplePayButtonStyle(PayWithApplePayButtonStyle) -> some View](/documentation/swiftui/view/paywithapplepaybuttonstyle(_:))
- [func popoverTip((any Tip)?, arrowEdge: Edge?, action: (Tips.Action) -> Void) -> some View](/documentation/swiftui/view/popovertip(_:arrowedge:action:))
- [func popoverTip((any Tip)?, isPresented: Binding<Bool>?, attachmentAnchor: PopoverAttachmentAnchor, arrowEdge: Edge?, action: (Tips.Action) -> Void) -> some View](/documentation/swiftui/view/popovertip(_:ispresented:attachmentanchor:arrowedge:action:))
- [func popoverTip((any Tip)?, isPresented: Binding<Bool>?, attachmentAnchor: PopoverAttachmentAnchor, arrowEdges: Edge.Set, action: (Tips.Action) -> Void) -> some View](/documentation/swiftui/view/popovertip(_:ispresented:attachmentanchor:arrowedges:action:))
- [func postToPhotosSharedAlbumSheet(isPresented:items:photoLibrary:defaultAlbumIdentifier:completion:)](/documentation/swiftui/view/posttophotossharedalbumsheet(ispresented:items:photolibrary:defaultalbumidentifier:completion:))
- [func preferredSubscriptionOffer((Product, Product.SubscriptionInfo, [Product.SubscriptionOffer]) -> Product.SubscriptionOffer?) -> some View](/documentation/swiftui/view/preferredsubscriptionoffer(_:))
- [func preferredSubscriptionPricingTerms((Product, SubscriptionInfo) -> SubscriptionInfo.PricingTerms?) -> some View](/documentation/swiftui/view/preferredsubscriptionpricingterms(_:))
- [func preferredWindowClippingMargins(_:_:)](/documentation/swiftui/view/preferredwindowclippingmargins(_:_:))
- [func presentationBreakthroughEffect(BreakthroughEffect) -> some View](/documentation/swiftui/view/presentationbreakthrougheffect(_:))
- [func presentationPreventsAppTermination(Bool?) -> some View](/documentation/swiftui/view/presentationpreventsapptermination(_:))
- [func productDescription(Visibility) -> some View](/documentation/swiftui/view/productdescription(_:))
- [func productIconBorder() -> some View](/documentation/swiftui/view/producticonborder())
- [func productViewStyle(some ProductViewStyle) -> some View](/documentation/swiftui/view/productviewstyle(_:))
- [func realityViewCameraControls(CameraControls) -> some View](/documentation/swiftui/view/realityviewcameracontrols(_:))
- [func realityViewLayoutBehavior(RealityViewLayoutOption) -> some View](/documentation/swiftui/view/realityviewlayoutbehavior(_:))
- [func rotation3DLayout(Rotation3D) -> some View](/documentation/swiftui/view/rotation3dlayout(_:))
- [func rotation3DLayout(_:axis:)](/documentation/swiftui/view/rotation3dlayout(_:axis:))
- [func safeAreaBar(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareabar(edge:alignment:spacing:content:))
- [func scaledToFill3D() -> some View](/documentation/swiftui/view/scaledtofill3d())
- [func scaledToFit3D() -> some View](/documentation/swiftui/view/scaledtofit3d())
- [func scrollEdgeEffectHidden(Bool, for: Edge.Set) -> some View](/documentation/swiftui/view/scrolledgeeffecthidden(_:for:))
- [func scrollEdgeEffectStyle(ScrollEdgeEffectStyle?, for: Edge.Set) -> some View](/documentation/swiftui/view/scrolledgeeffectstyle(_:for:))
- [func scrollInputBehavior(ScrollInputBehavior, for: ScrollInputKind) -> some View](/documentation/swiftui/view/scrollinputbehavior(_:for:))
- [func searchSelection(Binding<TextSelection?>) -> some View](/documentation/swiftui/view/searchselection(_:))
- [func searchToolbarBehavior(SearchToolbarBehavior) -> some View](/documentation/swiftui/view/searchtoolbarbehavior(_:))
- [func sectionIndexLabel(_:)](/documentation/swiftui/view/sectionindexlabel(_:))
- [func signInWithAppleButtonStyle(SignInWithAppleButton.Style) -> some View](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))
- [func sliderThumbVisibility(Visibility) -> some View](/documentation/swiftui/view/sliderthumbvisibility(_:))
- [func spatialOverlay<V>(alignment: Alignment3D, content: () -> V) -> some View](/documentation/swiftui/view/spatialoverlay(alignment:content:))
- [func spatialOverlayPreferenceValue<K, V>(K.Type, alignment: Alignment3D, (K.Value) -> V) -> some View](/documentation/swiftui/view/spatialoverlaypreferencevalue(_:alignment:_:))
- [func storeButton(Visibility, for: StoreButtonKind...) -> some View](/documentation/swiftui/view/storebutton(_:for:))
- [func storeProductTask(for: Product.ID, priority: TaskPriority, action: (Product.TaskState) async -> ()) -> some View](/documentation/swiftui/view/storeproducttask(for:priority:action:))
- [func storeProductsTask(for: some Collection<String> & Equatable & Sendable, priority: TaskPriority, action: (Product.CollectionTaskState) async -> ()) -> some View](/documentation/swiftui/view/storeproductstask(for:priority:action:))
- [func subscriptionIntroductoryOffer(applyOffer: (Product, Product.SubscriptionInfo) -> Bool, compactJWS: (Product, Product.SubscriptionInfo) async throws -> String) -> some View](/documentation/swiftui/view/subscriptionintroductoryoffer(applyoffer:compactjws:))
- [func subscriptionOfferViewButtonVisibility(Visibility, for: SubscriptionOfferViewButtonKind...) -> some View](/documentation/swiftui/view/subscriptionofferviewbuttonvisibility(_:for:))
- [func subscriptionOfferViewDetailAction((() -> ())?) -> some View](/documentation/swiftui/view/subscriptionofferviewdetailaction(_:))
- [func subscriptionOfferViewStyle(some SubscriptionOfferViewStyle) -> some View](/documentation/swiftui/view/subscriptionofferviewstyle(_:))
- [func subscriptionPromotionalOffer(offer: (Product, Product.SubscriptionInfo) -> Product.SubscriptionOffer?, compactJWS: (Product, Product.SubscriptionInfo, Product.SubscriptionOffer) async throws -> String) -> some View](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:compactjws:))
- [func subscriptionPromotionalOffer(offer: (Product, Product.SubscriptionInfo) -> Product.SubscriptionOffer?, signature: (Product, Product.SubscriptionInfo, Product.SubscriptionOffer) async throws -> Product.SubscriptionOffer.Signature) -> some View](/documentation/swiftui/view/subscriptionpromotionaloffer(offer:signature:))
- [func subscriptionStatusTask(for: String, priority: TaskPriority, action: (EntitlementTaskState<[Product.SubscriptionInfo.Status]>) async -> ()) -> some View](/documentation/swiftui/view/subscriptionstatustask(for:priority:action:))
- [func subscriptionStoreButtonLabel(SubscriptionStoreButtonLabel) -> some View](/documentation/swiftui/view/subscriptionstorebuttonlabel(_:))
- [func subscriptionStoreControlBackground(_:)](/documentation/swiftui/view/subscriptionstorecontrolbackground(_:))
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
- [func symbolColorRenderingMode(SymbolColorRenderingMode?) -> some View](/documentation/swiftui/view/symbolcolorrenderingmode(_:))
- [func symbolVariableValueMode(SymbolVariableValueMode?) -> some View](/documentation/swiftui/view/symbolvariablevaluemode(_:))
- [func tabBarMinimizeBehavior(TabBarMinimizeBehavior) -> some View](/documentation/swiftui/view/tabbarminimizebehavior(_:))
- [func tabViewBottomAccessory<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewbottomaccessory(content:))
- [func tabViewBottomAccessory<Content>(isEnabled: Bool, content: () -> Content) -> some View](/documentation/swiftui/view/tabviewbottomaccessory(isenabled:content:))
- [func tabViewSearchActivation(TabSearchActivation) -> some View](/documentation/swiftui/view/tabviewsearchactivation(_:))
- [func tabletopGame(TabletopGame, parent: Entity, automaticUpdate: Bool) -> some View](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:))
- [func tabletopGame(TabletopGame, parent: Entity, automaticUpdate: Bool, interaction: (TabletopInteraction.Value) -> any TabletopInteraction.Delegate) -> some View](/documentation/swiftui/view/tabletopgame(_:parent:automaticupdate:interaction:))
- [func task<T>(id: T, name: String?, executorPreference: any TaskExecutor, priority: TaskPriority, file: String, line: Int, sending () async -> Void) -> some View](/documentation/swiftui/view/task(id:name:executorpreference:priority:file:line:_:))
- [func task<T>(id: T, name: String?, priority: TaskPriority, file: String, line: Int, sending () async -> Void) -> some View](/documentation/swiftui/view/task(id:name:priority:file:line:_:))
- [func task(name: String?, executorPreference: any TaskExecutor, priority: TaskPriority, file: String, line: Int, action: sending () async -> Void) -> some View](/documentation/swiftui/view/task(name:executorpreference:priority:file:line:action:))
- [func task(name: String?, priority: TaskPriority, file: String, line: Int, sending () async -> Void) -> some View](/documentation/swiftui/view/task(name:priority:file:line:_:))
- [func textContentType(_:)](/documentation/swiftui/view/textcontenttype(_:))
- [func textInputFormattingControlVisibility(Visibility, for: TextInputFormattingControlPlacement.Set) -> some View](/documentation/swiftui/view/textinputformattingcontrolvisibility(_:for:))
- [func textRenderer<T>(T) -> some View](/documentation/swiftui/view/textrenderer(_:))
- [func textSelectionAffinity(TextSelectionAffinity) -> some View](/documentation/swiftui/view/textselectionaffinity(_:))
- [func tipAnchor<AnchorID>(AnchorID) -> some View](/documentation/swiftui/view/tipanchor(_:))
- [func tipBackground<S>(S) -> some View](/documentation/swiftui/view/tipbackground(_:))
- [func tipBackgroundInteraction(PresentationBackgroundInteraction) -> some View](/documentation/swiftui/view/tipbackgroundinteraction(_:))
- [func tipCornerRadius(CGFloat, antialiased: Bool) -> some View](/documentation/swiftui/view/tipcornerradius(_:antialiased:))
- [func tipImageSize(CGSize) -> some View](/documentation/swiftui/view/tipimagesize(_:))
- [func tipImageStyle<S>(S) -> some View](/documentation/swiftui/view/tipimagestyle(_:))
- [func tipImageStyle<S1, S2>(S1, S2) -> some View](/documentation/swiftui/view/tipimagestyle(_:_:))
- [func tipImageStyle<S1, S2, S3>(S1, S2, S3) -> some View](/documentation/swiftui/view/tipimagestyle(_:_:_:))
- [func tipViewStyle(some TipViewStyle) -> some View](/documentation/swiftui/view/tipviewstyle(_:))
- [func toolbarItemHidden(Bool) -> some View](/documentation/swiftui/view/toolbaritemhidden(_:))
- [func transactionPicker(isPresented: Binding<Bool>, selection: Binding<[Transaction]>) -> some View](/documentation/swiftui/view/transactionpicker(ispresented:selection:))
- [func transactionTask(CredentialTransaction.Configuration?, action: (CredentialTransaction) async -> Void) -> some View](/documentation/swiftui/view/transactiontask(_:action:))
- [func verifyIdentityWithWalletButtonStyle(VerifyIdentityWithWalletButtonStyle) -> some View](/documentation/swiftui/view/verifyidentitywithwalletbuttonstyle(_:))
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
- [func windowResizeAnchor(UnitPoint?) -> some View](/documentation/swiftui/view/windowresizeanchor(_:))
- [func windowToolbarFullScreenVisibility(WindowToolbarFullScreenVisibility) -> some View](/documentation/swiftui/view/windowtoolbarfullscreenvisibility(_:))
- [func workoutPreview(WorkoutPlan, isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/workoutpreview(_:ispresented:))
- [func writingDirection(strategy: Text.WritingDirectionStrategy) -> some View](/documentation/swiftui/view/writingdirection(strategy:))
- [func writingToolsAffordanceVisibility(Visibility) -> some View](/documentation/swiftui/view/writingtoolsaffordancevisibility(_:))
- [func writingToolsBehavior(WritingToolsBehavior) -> some View](/documentation/swiftui/view/writingtoolsbehavior(_:))
- [ViewBuilder](/documentation/swiftui/viewbuilder)

#### Building content

- [static func buildBlock() -> EmptyView](/documentation/swiftui/viewbuilder/buildblock())
- [static buildBlock(_:)](/documentation/swiftui/viewbuilder/buildblock(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/viewbuilder/buildexpression(_:))

#### Conditionally building content

- [static func buildEither<TrueContent, FalseContent>(first: TrueContent) -> _ConditionalContent<TrueContent, FalseContent>](/documentation/swiftui/viewbuilder/buildeither(first:))
- [static func buildEither<TrueContent, FalseContent>(second: FalseContent) -> _ConditionalContent<TrueContent, FalseContent>](/documentation/swiftui/viewbuilder/buildeither(second:))
- [static func buildIf<Content>(Content?) -> Content?](/documentation/swiftui/viewbuilder/buildif(_:))
- [static func buildLimitedAvailability<Content>(Content) -> AnyView](/documentation/swiftui/viewbuilder/buildlimitedavailability(_:))

### Modifying a view

- [Configuring views](/documentation/swiftui/configuring-views)
- [Reducing view modifier maintenance](/documentation/swiftui/reducing-view-modifier-maintenance)
- [func modifier<T>(T) -> ModifiedContent<Self, T>](/documentation/swiftui/view/modifier(_:))
- [ViewModifier](/documentation/swiftui/viewmodifier)

#### Creating a view modifier

- [func body(content: Self.Content) -> Self.Body](/documentation/swiftui/viewmodifier/body(content:))
- [Body](/documentation/swiftui/viewmodifier/body)
- [ViewModifier.Content](/documentation/swiftui/viewmodifier/content)

#### Adding animations to a view

- [func animation(Animation?) -> some ViewModifier](/documentation/swiftui/viewmodifier/animation(_:))
- [func concat<T>(T) -> ModifiedContent<Self, T>](/documentation/swiftui/viewmodifier/concat(_:))

#### Handling view taps and gestures

- [func transaction((inout Transaction) -> Void) -> some ViewModifier](/documentation/swiftui/viewmodifier/transaction(_:))
- [EmptyModifier](/documentation/swiftui/emptymodifier)

#### Creating an empty modifier

- [init()](/documentation/swiftui/emptymodifier/init())

#### Getting the identity modifier

- [static let identity: EmptyModifier](/documentation/swiftui/emptymodifier/identity)
- [ModifiedContent](/documentation/swiftui/modifiedcontent)

#### Creating a modified content view

- [init(content: Content, modifier: Modifier)](/documentation/swiftui/modifiedcontent/init(content:modifier:))
- [var content: Content](/documentation/swiftui/modifiedcontent/content)
- [var modifier: Modifier](/documentation/swiftui/modifiedcontent/modifier)

#### Instance Methods

- [func accessibility(activationPoint:)](/documentation/swiftui/modifiedcontent/accessibility(activationpoint:))
- [func accessibility(addTraits: AccessibilityTraits) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(addtraits:))
- [func accessibility(hidden: Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(hidden:))
- [func accessibility(hint: Text) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(hint:))
- [func accessibility(identifier: String) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(identifier:))
- [func accessibility(inputLabels: [Text]) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(inputlabels:))
- [func accessibility(label: Text) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(label:))
- [func accessibility(removeTraits: AccessibilityTraits) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(removetraits:))
- [func accessibility(selectionIdentifier: AnyHashable) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(selectionidentifier:))
- [func accessibility(sortPriority: Double) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(sortpriority:))
- [func accessibility(value: Text) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibility(value:))
- [func accessibilityAction(AccessibilityActionKind, () -> Void) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityaction(_:_:))
- [func accessibilityAction<I>(AccessibilityActionKind, intent: I) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityaction(_:intent:))
- [func accessibilityAction(named:_:)](/documentation/swiftui/modifiedcontent/accessibilityaction(named:_:))
- [func accessibilityAction(named:intent:)](/documentation/swiftui/modifiedcontent/accessibilityaction(named:intent:))
- [func accessibilityActivationPoint(_:)](/documentation/swiftui/modifiedcontent/accessibilityactivationpoint(_:))
- [func accessibilityActivationPoint(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilityactivationpoint(_:isenabled:))
- [func accessibilityAddTraits(AccessibilityTraits) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityaddtraits(_:))
- [func accessibilityAdjustableAction((AccessibilityAdjustmentDirection) -> Void) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityadjustableaction(_:))
- [func accessibilityCustomContent(_:_:importance:)](/documentation/swiftui/modifiedcontent/accessibilitycustomcontent(_:_:importance:))
- [func accessibilityDirectTouch(Bool, options: AccessibilityDirectTouchOptions) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilitydirecttouch(_:options:))
- [func accessibilityDragPoint(_:description:)](/documentation/swiftui/modifiedcontent/accessibilitydragpoint(_:description:))
- [func accessibilityDragPoint(_:description:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilitydragpoint(_:description:isenabled:))
- [func accessibilityDropPoint(_:description:)](/documentation/swiftui/modifiedcontent/accessibilitydroppoint(_:description:))
- [func accessibilityDropPoint(_:description:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilitydroppoint(_:description:isenabled:))
- [func accessibilityHeading(AccessibilityHeadingLevel) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityheading(_:))
- [func accessibilityHidden(Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityhidden(_:))
- [func accessibilityHidden(Bool, isEnabled: Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityhidden(_:isenabled:))
- [func accessibilityHint(_:)](/documentation/swiftui/modifiedcontent/accessibilityhint(_:))
- [func accessibilityHint(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilityhint(_:isenabled:))
- [func accessibilityIdentifier(String) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityidentifier(_:))
- [func accessibilityIdentifier(String, isEnabled: Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityidentifier(_:isenabled:))
- [func accessibilityInputLabels(_:)](/documentation/swiftui/modifiedcontent/accessibilityinputlabels(_:))
- [func accessibilityInputLabels(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilityinputlabels(_:isenabled:))
- [func accessibilityLabel(_:)](/documentation/swiftui/modifiedcontent/accessibilitylabel(_:))
- [func accessibilityLabel(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilitylabel(_:isenabled:))
- [func accessibilityRemoveTraits(AccessibilityTraits) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityremovetraits(_:))
- [func accessibilityRespondsToUserInteraction(Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityrespondstouserinteraction(_:))
- [func accessibilityRespondsToUserInteraction(Bool, isEnabled: Bool) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityrespondstouserinteraction(_:isenabled:))
- [func accessibilityScrollAction((Edge) -> Void) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityscrollaction(_:))
- [func accessibilityScrollStatus(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilityscrollstatus(_:isenabled:))
- [func accessibilitySortPriority(Double) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilitysortpriority(_:))
- [func accessibilityTextContentType(AccessibilityTextContentType) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilitytextcontenttype(_:))
- [func accessibilityValue(_:)](/documentation/swiftui/modifiedcontent/accessibilityvalue(_:))
- [func accessibilityValue(_:isEnabled:)](/documentation/swiftui/modifiedcontent/accessibilityvalue(_:isenabled:))
- [func accessibilityZoomAction((AccessibilityZoomGestureAction) -> Void) -> ModifiedContent<Content, Modifier>](/documentation/swiftui/modifiedcontent/accessibilityzoomaction(_:))
- [EnvironmentalModifier](/documentation/swiftui/environmentalmodifier)

#### Resolving a modifier

- [func resolve(in: EnvironmentValues) -> Self.ResolvedModifier](/documentation/swiftui/environmentalmodifier/resolve(in:))
- [ResolvedModifier](/documentation/swiftui/environmentalmodifier/resolvedmodifier)
- [ManipulableModifier](/documentation/swiftui/manipulablemodifier)
- [ManipulableResponderModifier](/documentation/swiftui/manipulablerespondermodifier)
- [ManipulableTransformBindingModifier](/documentation/swiftui/manipulabletransformbindingmodifier)
- [ManipulationGeometryModifier](/documentation/swiftui/manipulationgeometrymodifier)
- [ManipulationGestureModifier](/documentation/swiftui/manipulationgesturemodifier)
- [ManipulationUsingGestureStateModifier](/documentation/swiftui/manipulationusinggesturestatemodifier)
- [Manipulable](/documentation/swiftui/manipulable)

#### Structures

- [Manipulable.Event](/documentation/swiftui/manipulable/event)

##### Structures

- [Manipulable.Event.Value](/documentation/swiftui/manipulable/event/value-swift.struct)

###### Instance Properties

- [let frame: Rect3D](/documentation/swiftui/manipulable/event/value-swift.struct/frame)
- [let inputDevices: [Manipulable.InputDevice]](/documentation/swiftui/manipulable/event/value-swift.struct/inputdevices)
- [let interactionPoint: Point3D](/documentation/swiftui/manipulable/event/value-swift.struct/interactionpoint)
- [let timestamp: TimeInterval](/documentation/swiftui/manipulable/event/value-swift.struct/timestamp)
- [let transform: AffineTransform3D?](/documentation/swiftui/manipulable/event/value-swift.struct/transform)

##### Instance Properties

- [var phase: Manipulable.Event.Phase](/documentation/swiftui/manipulable/event/phase-swift.property)
- [var value: Manipulable.Event.Value?](/documentation/swiftui/manipulable/event/value-swift.property)

##### Enumerations

- [Manipulable.Event.Phase](/documentation/swiftui/manipulable/event/phase-swift.enum)

###### Enumeration Cases

- [case active(Manipulable.Event.Value)](/documentation/swiftui/manipulable/event/phase-swift.enum/active(_:))
- [case ended(Manipulable.Event.Value)](/documentation/swiftui/manipulable/event/phase-swift.enum/ended(_:))
- [case failed](/documentation/swiftui/manipulable/event/phase-swift.enum/failed)
- [Manipulable.GestureState](/documentation/swiftui/manipulable/gesturestate)

##### Initializers

- [init(transform: AffineTransform3D)](/documentation/swiftui/manipulable/gesturestate/init(transform:))

##### Instance Properties

- [var isActive: Bool](/documentation/swiftui/manipulable/gesturestate/isactive)
- [var transform: AffineTransform3D](/documentation/swiftui/manipulable/gesturestate/transform)
- [Manipulable.Inertia](/documentation/swiftui/manipulable/inertia)

##### Type Properties

- [static let high: Manipulable.Inertia](/documentation/swiftui/manipulable/inertia/high)
- [static let low: Manipulable.Inertia](/documentation/swiftui/manipulable/inertia/low)
- [static let medium: Manipulable.Inertia](/documentation/swiftui/manipulable/inertia/medium)
- [static let none: Manipulable.Inertia](/documentation/swiftui/manipulable/inertia/none)
- [Manipulable.InputDevice](/documentation/swiftui/manipulable/inputdevice)

##### Instance Properties

- [let chirality: Manipulable.InputDevice.Chirality?](/documentation/swiftui/manipulable/inputdevice/chirality-swift.property)
- [let kind: Manipulable.InputDevice.Kind](/documentation/swiftui/manipulable/inputdevice/kind-swift.property)
- [let pose: Pose3D?](/documentation/swiftui/manipulable/inputdevice/pose)

##### Enumerations

- [Manipulable.InputDevice.Chirality](/documentation/swiftui/manipulable/inputdevice/chirality-swift.enum)

###### Enumeration Cases

- [case left](/documentation/swiftui/manipulable/inputdevice/chirality-swift.enum/left)
- [case right](/documentation/swiftui/manipulable/inputdevice/chirality-swift.enum/right)
- [Manipulable.InputDevice.Kind](/documentation/swiftui/manipulable/inputdevice/kind-swift.enum)

###### Enumeration Cases

- [case directPinch](/documentation/swiftui/manipulable/inputdevice/kind-swift.enum/directpinch)
- [case indirectPinch](/documentation/swiftui/manipulable/inputdevice/kind-swift.enum/indirectpinch)
- [case pointer](/documentation/swiftui/manipulable/inputdevice/kind-swift.enum/pointer)
- [Manipulable.Operation](/documentation/swiftui/manipulable/operation)

##### Structures

- [Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set)

###### Initializers

- [init(Manipulable.Operation)](/documentation/swiftui/manipulable/operation/set/init(_:))

###### Type Properties

- [static let all: Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set/all)
- [static let primaryRotation: Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set/primaryrotation)
- [static let scale: Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set/scale)
- [static let secondaryRotation: Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set/secondaryrotation)
- [static let translate: Manipulable.Operation.Set](/documentation/swiftui/manipulable/operation/set/translate)

##### Type Properties

- [static let primaryRotation: Manipulable.Operation](/documentation/swiftui/manipulable/operation/primaryrotation)
- [static let scale: Manipulable.Operation](/documentation/swiftui/manipulable/operation/scale)
- [static let secondaryRotation: Manipulable.Operation](/documentation/swiftui/manipulable/operation/secondaryrotation)
- [static let translate: Manipulable.Operation](/documentation/swiftui/manipulable/operation/translate)

### Responding to view life cycle updates

- [func onAppear(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onappear(perform:))
- [func onDisappear(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/ondisappear(perform:))

### Managing the view hierarchy

- [func id<ID>(ID) -> some View](/documentation/swiftui/view/id(_:))
- [func tag<V>(V, includeOptional: Bool) -> some View](/documentation/swiftui/view/tag(_:includeoptional:))
- [func equatable() -> EquatableView<Self>](/documentation/swiftui/view/equatable())

### Supporting view types

- [AnyView](/documentation/swiftui/anyview)

#### Creating a view

- [init<V>(V)](/documentation/swiftui/anyview/init(_:))
- [init<V>(erasing: V)](/documentation/swiftui/anyview/init(erasing:))
- [EmptyView](/documentation/swiftui/emptyview)

#### Creating an empty view

- [init()](/documentation/swiftui/emptyview/init())
- [EquatableView](/documentation/swiftui/equatableview)

#### Creating an equatable view

- [init(content: Content)](/documentation/swiftui/equatableview/init(content:))
- [var content: Content](/documentation/swiftui/equatableview/content)
- [SubscriptionView](/documentation/swiftui/subscriptionview)

#### Creating a subscription view

- [init(content: Content, publisher: PublisherType, action: (PublisherType.Output) -> Void)](/documentation/swiftui/subscriptionview/init(content:publisher:action:))

#### Managing the subscription

- [var publisher: PublisherType](/documentation/swiftui/subscriptionview/publisher)
- [var action: (PublisherType.Output) -> Void](/documentation/swiftui/subscriptionview/action)
- [var content: Content](/documentation/swiftui/subscriptionview/content)
- [TupleView](/documentation/swiftui/tupleview)

#### Creating a tuple view

- [init(T)](/documentation/swiftui/tupleview/init(_:))
- [var value: T](/documentation/swiftui/tupleview/value)
- [View configuration](/documentation/swiftui/view-configuration)

### Hiding views

- [func opacity(Double) -> some View](/documentation/swiftui/view/opacity(_:))
- [func hidden() -> some View](/documentation/swiftui/view/hidden())

### Hiding system elements

- [func labelsHidden() -> some View](/documentation/swiftui/view/labelshidden())
- [func labelsVisibility(Visibility) -> some View](/documentation/swiftui/view/labelsvisibility(_:))
- [var labelsVisibility: Visibility](/documentation/swiftui/environmentvalues/labelsvisibility)
- [func menuIndicator(Visibility) -> some View](/documentation/swiftui/view/menuindicator(_:))
- [func statusBarHidden(Bool) -> some View](/documentation/swiftui/view/statusbarhidden(_:))
- [func persistentSystemOverlays(Visibility) -> some View](/documentation/swiftui/view/persistentsystemoverlays(_:))
- [Visibility](/documentation/swiftui/visibility)

#### Getting visibility options

- [case automatic](/documentation/swiftui/visibility/automatic)
- [case visible](/documentation/swiftui/visibility/visible)
- [case hidden](/documentation/swiftui/visibility/hidden)

### Managing view interaction

- [func disabled(Bool) -> some View](/documentation/swiftui/view/disabled(_:))
- [var isEnabled: Bool](/documentation/swiftui/environmentvalues/isenabled)
- [func interactionActivityTrackingTag(String) -> some View](/documentation/swiftui/view/interactionactivitytrackingtag(_:))
- [func invalidatableContent(Bool) -> some View](/documentation/swiftui/view/invalidatablecontent(_:))

### Providing contextual help

- [func help(_:)](/documentation/swiftui/view/help(_:))

### Detecting and requesting the light or dark appearance

- [func preferredColorScheme(ColorScheme?) -> some View](/documentation/swiftui/view/preferredcolorscheme(_:))
- [var colorScheme: ColorScheme](/documentation/swiftui/environmentvalues/colorscheme)
- [ColorScheme](/documentation/swiftui/colorscheme)

#### Getting color schemes

- [case light](/documentation/swiftui/colorscheme/light)
- [case dark](/documentation/swiftui/colorscheme/dark)

#### Creating a color scheme

- [init?(UIUserInterfaceStyle)](/documentation/swiftui/colorscheme/init(_:))

#### Supporting types

- [PreferredColorSchemeKey](/documentation/swiftui/preferredcolorschemekey)

### Getting the color scheme contrast

- [var colorSchemeContrast: ColorSchemeContrast](/documentation/swiftui/environmentvalues/colorschemecontrast)
- [ColorSchemeContrast](/documentation/swiftui/colorschemecontrast)

#### Getting contrast options

- [case standard](/documentation/swiftui/colorschemecontrast/standard)
- [case increased](/documentation/swiftui/colorschemecontrast/increased)

#### Creating a color scheme contrast

- [init?(UIAccessibilityContrast)](/documentation/swiftui/colorschemecontrast/init(_:))

### Configuring passthrough

- [func preferredSurroundingsEffect(SurroundingsEffect?) -> some View](/documentation/swiftui/view/preferredsurroundingseffect(_:))
- [SurroundingsEffect](/documentation/swiftui/surroundingseffect)

#### Getting the effect

- [static var systemDark: SurroundingsEffect](/documentation/swiftui/surroundingseffect/systemdark)

#### Type Properties

- [static var dark: SurroundingsEffect](/documentation/swiftui/surroundingseffect/dark)
- [static var semiDark: SurroundingsEffect](/documentation/swiftui/surroundingseffect/semidark)
- [static var ultraDark: SurroundingsEffect](/documentation/swiftui/surroundingseffect/ultradark)

#### Type Methods

- [static func colorMultiply(Color) -> SurroundingsEffect](/documentation/swiftui/surroundingseffect/colormultiply(_:))
- [static func dim(intensity: Double) -> SurroundingsEffect](/documentation/swiftui/surroundingseffect/dim(intensity:))
- [BreakthroughEffect](/documentation/swiftui/breakthrougheffect)

#### Type Properties

- [static let automatic: BreakthroughEffect](/documentation/swiftui/breakthrougheffect/automatic)
- [static let none: BreakthroughEffect](/documentation/swiftui/breakthrougheffect/none)
- [static let prominent: BreakthroughEffect](/documentation/swiftui/breakthrougheffect/prominent)
- [static let subtle: BreakthroughEffect](/documentation/swiftui/breakthrougheffect/subtle)

### Redacting private content

- [Designing your app for the Always On state](/documentation/watchos-apps/designing-your-app-for-the-always-on-state)
- [func privacySensitive(Bool) -> some View](/documentation/swiftui/view/privacysensitive(_:))
- [func redacted(reason: RedactionReasons) -> some View](/documentation/swiftui/view/redacted(reason:))
- [func unredacted() -> some View](/documentation/swiftui/view/unredacted())
- [var redactionReasons: RedactionReasons](/documentation/swiftui/environmentvalues/redactionreasons)
- [var isSceneCaptured: Bool](/documentation/swiftui/environmentvalues/isscenecaptured)
- [RedactionReasons](/documentation/swiftui/redactionreasons)

#### Getting redaction reasons

- [static let invalidated: RedactionReasons](/documentation/swiftui/redactionreasons/invalidated)
- [static let placeholder: RedactionReasons](/documentation/swiftui/redactionreasons/placeholder)
- [static let privacy: RedactionReasons](/documentation/swiftui/redactionreasons/privacy)

#### Creating redaction reasons

- [init(rawValue: Int)](/documentation/swiftui/redactionreasons/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/redactionreasons/rawvalue)
- [View styles](/documentation/swiftui/view-styles)

### Styling views with Liquid Glass

- [Applying Liquid Glass to custom views](/documentation/swiftui/applying-liquid-glass-to-custom-views)
- [Landmarks: Building an app with Liquid Glass](/documentation/swiftui/landmarks-building-an-app-with-liquid-glass)

#### App features

- [Landmarks: Applying a background extension effect](/documentation/swiftui/landmarks-applying-a-background-extension-effect)
- [Landmarks: Extending horizontal scrolling under a sidebar or inspector](/documentation/swiftui/landmarks-extending-horizontal-scrolling-under-a-sidebar-or-inspector)
- [Landmarks: Refining the system provided Liquid Glass effect in toolbars](/documentation/swiftui/landmarks-refining-the-system-provided-glass-effect-in-toolbars)
- [Landmarks: Displaying custom activity badges](/documentation/swiftui/landmarks-displaying-custom-activity-badges)
- [func glassEffect(Glass, in: some Shape) -> some View](/documentation/swiftui/view/glasseffect(_:in:))
- [func interactive(Bool) -> Glass](/documentation/swiftui/glass/interactive(_:))
- [GlassEffectContainer](/documentation/swiftui/glasseffectcontainer)

#### Initializers

- [init(spacing: CGFloat?, content: () -> Content)](/documentation/swiftui/glasseffectcontainer/init(spacing:content:))
- [GlassEffectTransition](/documentation/swiftui/glasseffecttransition)

#### Type Properties

- [static var identity: GlassEffectTransition](/documentation/swiftui/glasseffecttransition/identity)
- [static var matchedGeometry: GlassEffectTransition](/documentation/swiftui/glasseffecttransition/matchedgeometry)
- [static var materialize: GlassEffectTransition](/documentation/swiftui/glasseffecttransition/materialize)
- [GlassButtonStyle](/documentation/swiftui/glassbuttonstyle)

#### Initializers

- [init()](/documentation/swiftui/glassbuttonstyle/init())
- [init(Glass)](/documentation/swiftui/glassbuttonstyle/init(_:))

#### Instance Methods

- [func makeBody(configuration: GlassButtonStyle.Configuration) -> some View](/documentation/swiftui/glassbuttonstyle/makebody(configuration:))
- [GlassProminentButtonStyle](/documentation/swiftui/glassprominentbuttonstyle)

#### Initializers

- [init()](/documentation/swiftui/glassprominentbuttonstyle/init())

#### Instance Methods

- [func makeBody(configuration: GlassProminentButtonStyle.Configuration) -> some View](/documentation/swiftui/glassprominentbuttonstyle/makebody(configuration:))
- [DefaultGlassEffectShape](/documentation/swiftui/defaultglasseffectshape)

#### Initializers

- [init()](/documentation/swiftui/defaultglasseffectshape/init())

### Styling buttons

- [func buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [ButtonStyle](/documentation/swiftui/buttonstyle)

#### Custom button styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/buttonstyle/makebody(configuration:))
- [ButtonStyle.Configuration](/documentation/swiftui/buttonstyle/configuration)
- [Body](/documentation/swiftui/buttonstyle/body)
- [ButtonStyleConfiguration](/documentation/swiftui/buttonstyleconfiguration)

#### Configuring a button’s label

- [let label: ButtonStyleConfiguration.Label](/documentation/swiftui/buttonstyleconfiguration/label-swift.property)
- [ButtonStyleConfiguration.Label](/documentation/swiftui/buttonstyleconfiguration/label-swift.struct)

#### Configuring a button’s interaction state

- [let isPressed: Bool](/documentation/swiftui/buttonstyleconfiguration/ispressed)

#### Defining the button’s purpose

- [let role: ButtonRole?](/documentation/swiftui/buttonstyleconfiguration/role)
- [PrimitiveButtonStyle](/documentation/swiftui/primitivebuttonstyle)

#### Getting built-in button styles

- [static var automatic: DefaultButtonStyle](/documentation/swiftui/primitivebuttonstyle/automatic)
- [static var accessoryBar: AccessoryBarButtonStyle](/documentation/swiftui/primitivebuttonstyle/accessorybar)
- [static var accessoryBarAction: AccessoryBarActionButtonStyle](/documentation/swiftui/primitivebuttonstyle/accessorybaraction)
- [static var bordered: BorderedButtonStyle](/documentation/swiftui/primitivebuttonstyle/bordered)
- [static var borderedProminent: BorderedProminentButtonStyle](/documentation/swiftui/primitivebuttonstyle/borderedprominent)
- [static var borderless: BorderlessButtonStyle](/documentation/swiftui/primitivebuttonstyle/borderless)
- [static var card: CardButtonStyle](/documentation/swiftui/primitivebuttonstyle/card)
- [static var glass: GlassButtonStyle](/documentation/swiftui/primitivebuttonstyle/glass)
- [static var glassProminent: GlassProminentButtonStyle](/documentation/swiftui/primitivebuttonstyle/glassprominent)
- [static func glass(Glass) -> Self](/documentation/swiftui/primitivebuttonstyle/glass(_:))
- [static var link: LinkButtonStyle](/documentation/swiftui/primitivebuttonstyle/link)
- [static var plain: PlainButtonStyle](/documentation/swiftui/primitivebuttonstyle/plain)

#### Creating custom button styles

