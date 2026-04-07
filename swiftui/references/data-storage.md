# Data and Storage — SwiftUI Reference

## Contents
- [Data and storage](#data-and-storage)
  - [Creating and sharing view state](#creating-and-sharing-view-state)
  - [Creating model data](#creating-model-data)
  - [Responding to data changes](#responding-to-data-changes)
  - [Distributing model data throughout your app](#distributing-model-data-throughout-your-app)
  - [Managing dynamic data](#managing-dynamic-data)
  - [Accessing environment values](#accessing-environment-values)
  - [Creating custom environment values](#creating-custom-environment-values)
  - [Modifying the environment of a view](#modifying-the-environment-of-a-view)
  - [Modifying the environment of a scene](#modifying-the-environment-of-a-scene)
  - [Setting preferences](#setting-preferences)
  - [Creating custom preferences](#creating-custom-preferences)
  - [Setting preferences based on geometry](#setting-preferences-based-on-geometry)
  - [Responding to changes in preferences](#responding-to-changes-in-preferences)
  - [Generating backgrounds and overlays from preferences](#generating-backgrounds-and-overlays-from-preferences)
  - [Saving state across app launches](#saving-state-across-app-launches)
  - [Accessing Core Data](#accessing-core-data)

---
## Data and storage

- [Model data](/documentation/swiftui/model-data)

### Creating and sharing view state

- [Managing user interface state](/documentation/swiftui/managing-user-interface-state)
- [State](/documentation/swiftui/state)

#### Creating a state

- [init(wrappedValue: Value)](/documentation/swiftui/state/init(wrappedvalue:))
- [init(initialValue: Value)](/documentation/swiftui/state/init(initialvalue:))
- [init()](/documentation/swiftui/state/init())

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/state/wrappedvalue)
- [var projectedValue: Binding<Value>](/documentation/swiftui/state/projectedvalue)
- [Bindable](/documentation/swiftui/bindable)

#### Creating a bindable value

- [init(Value)](/documentation/swiftui/bindable/init(_:))
- [init(wrappedValue: Value)](/documentation/swiftui/bindable/init(wrappedvalue:))
- [init(projectedValue: Bindable<Value>)](/documentation/swiftui/bindable/init(projectedvalue:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/bindable/wrappedvalue)
- [var projectedValue: Bindable<Value>](/documentation/swiftui/bindable/projectedvalue)
- [subscript<Subject>(dynamicMember _: ReferenceWritableKeyPath<Value, Subject>) -> Binding<Subject>](/documentation/swiftui/bindable/subscript(dynamicmember:))
- [Binding](/documentation/swiftui/binding)

#### Creating a binding

- [init(_:)](/documentation/swiftui/binding/init(_:))
- [init(projectedValue: Binding<Value>)](/documentation/swiftui/binding/init(projectedvalue:))
- [init(get:set:)](/documentation/swiftui/binding/init(get:set:))
- [static func constant(Value) -> Binding<Value>](/documentation/swiftui/binding/constant(_:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/binding/wrappedvalue)
- [var projectedValue: Binding<Value>](/documentation/swiftui/binding/projectedvalue)
- [subscript<Subject>(dynamicMember _: WritableKeyPath<Value, Subject>) -> Binding<Subject>](/documentation/swiftui/binding/subscript(dynamicmember:))

#### Managing changes

- [var id: Value.ID](/documentation/swiftui/binding/id)
- [func animation(Animation?) -> Binding<Value>](/documentation/swiftui/binding/animation(_:))
- [func transaction(Transaction) -> Binding<Value>](/documentation/swiftui/binding/transaction(_:))
- [var transaction: Transaction](/documentation/swiftui/binding/transaction)

#### Subscripts

- [subscript(_:)](/documentation/swiftui/binding/subscript(_:))

#### Default Implementations

- [Identifiable Implementations](/documentation/swiftui/binding/identifiable-implementations)

##### Instance Properties

- [var id: Value.ID](/documentation/swiftui/binding/id)

### Creating model data

- [Managing model data in your app](/documentation/swiftui/managing-model-data-in-your-app)
- [Migrating from the Observable Object protocol to the Observable macro](/documentation/swiftui/migrating-from-the-observable-object-protocol-to-the-observable-macro)
- [macro Observable()](/documentation/observation/observable())
- [Monitoring data changes in your app](/documentation/swiftui/monitoring-model-data-changes-in-your-app)
- [StateObject](/documentation/swiftui/stateobject)

#### Creating a state object

- [init(wrappedValue: @autoclosure () -> ObjectType)](/documentation/swiftui/stateobject/init(wrappedvalue:))

#### Getting the value

- [var wrappedValue: ObjectType](/documentation/swiftui/stateobject/wrappedvalue)
- [var projectedValue: ObservedObject<ObjectType>.Wrapper](/documentation/swiftui/stateobject/projectedvalue)
- [ObservedObject](/documentation/swiftui/observedobject)

#### Creating an observed object

- [init(wrappedValue: ObjectType)](/documentation/swiftui/observedobject/init(wrappedvalue:))
- [init(initialValue: ObjectType)](/documentation/swiftui/observedobject/init(initialvalue:))

#### Getting the value

- [var wrappedValue: ObjectType](/documentation/swiftui/observedobject/wrappedvalue)
- [var projectedValue: ObservedObject<ObjectType>.Wrapper](/documentation/swiftui/observedobject/projectedvalue)
- [ObservedObject.Wrapper](/documentation/swiftui/observedobject/wrapper)

##### Subscripts

- [subscript<Subject>(dynamicMember _: ReferenceWritableKeyPath<ObjectType, Subject>) -> Binding<Subject>](/documentation/swiftui/observedobject/wrapper/subscript(dynamicmember:))
- [ObservableObject](/documentation/combine/observableobject)

### Responding to data changes

- [func onChange(of:initial:_:)](/documentation/swiftui/view/onchange(of:initial:_:))
- [func onReceive<P>(P, perform: (P.Output) -> Void) -> some View](/documentation/swiftui/view/onreceive(_:perform:))

### Distributing model data throughout your app

- [func environmentObject<T>(T) -> some View](/documentation/swiftui/view/environmentobject(_:))
- [func environmentObject<T>(T) -> some Scene](/documentation/swiftui/scene/environmentobject(_:))
- [EnvironmentObject](/documentation/swiftui/environmentobject)

#### Creating an environment object

- [init()](/documentation/swiftui/environmentobject/init())

#### Getting the value

- [var wrappedValue: ObjectType](/documentation/swiftui/environmentobject/wrappedvalue)
- [var projectedValue: EnvironmentObject<ObjectType>.Wrapper](/documentation/swiftui/environmentobject/projectedvalue)
- [EnvironmentObject.Wrapper](/documentation/swiftui/environmentobject/wrapper)

##### Getting a binding value

- [subscript<Subject>(dynamicMember _: ReferenceWritableKeyPath<ObjectType, Subject>) -> Binding<Subject>](/documentation/swiftui/environmentobject/wrapper/subscript(dynamicmember:))

### Managing dynamic data

- [DynamicProperty](/documentation/swiftui/dynamicproperty)

#### Updating the value

- [func update()](/documentation/swiftui/dynamicproperty/update())
- [Environment values](/documentation/swiftui/environment-values)

### Accessing environment values

- [Environment](/documentation/swiftui/environment)

#### Creating an environment instance

- [init(_:)](/documentation/swiftui/environment/init(_:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/environment/wrappedvalue)
- [EnvironmentValues](/documentation/swiftui/environmentvalues)

#### Creating and accessing values

- [init()](/documentation/swiftui/environmentvalues/init())
- [subscript(_:)](/documentation/swiftui/environmentvalues/subscript(_:))
- [var description: String](/documentation/swiftui/environmentvalues/description)

#### Accessibility

- [var accessibilityAssistiveAccessEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityassistiveaccessenabled)
- [var accessibilityDimFlashingLights: Bool](/documentation/swiftui/environmentvalues/accessibilitydimflashinglights)
- [var accessibilityDifferentiateWithoutColor: Bool](/documentation/swiftui/environmentvalues/accessibilitydifferentiatewithoutcolor)
- [var accessibilityEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityenabled)
- [var accessibilityInvertColors: Bool](/documentation/swiftui/environmentvalues/accessibilityinvertcolors)
- [var accessibilityLargeContentViewerEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilitylargecontentviewerenabled)
- [var accessibilityPlayAnimatedImages: Bool](/documentation/swiftui/environmentvalues/accessibilityplayanimatedimages)
- [var accessibilityPrefersHeadAnchorAlternative: Bool](/documentation/swiftui/environmentvalues/accessibilityprefersheadanchoralternative)
- [var accessibilityQuickActionsEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityquickactionsenabled)
- [var accessibilityReduceMotion: Bool](/documentation/swiftui/environmentvalues/accessibilityreducemotion)
- [var accessibilityReduceTransparency: Bool](/documentation/swiftui/environmentvalues/accessibilityreducetransparency)
- [var accessibilityShowButtonShapes: Bool](/documentation/swiftui/environmentvalues/accessibilityshowbuttonshapes)
- [var accessibilitySwitchControlEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityswitchcontrolenabled)
- [var accessibilityVoiceOverEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityvoiceoverenabled)
- [var legibilityWeight: LegibilityWeight?](/documentation/swiftui/environmentvalues/legibilityweight)

#### Actions

- [var dismiss: DismissAction](/documentation/swiftui/environmentvalues/dismiss)
- [var dismissSearch: DismissSearchAction](/documentation/swiftui/environmentvalues/dismisssearch)
- [var dismissWindow: DismissWindowAction](/documentation/swiftui/environmentvalues/dismisswindow)
- [var openImmersiveSpace: OpenImmersiveSpaceAction](/documentation/swiftui/environmentvalues/openimmersivespace)
- [var dismissImmersiveSpace: DismissImmersiveSpaceAction](/documentation/swiftui/environmentvalues/dismissimmersivespace)
- [var newDocument: NewDocumentAction](/documentation/swiftui/environmentvalues/newdocument)
- [var openDocument: OpenDocumentAction](/documentation/swiftui/environmentvalues/opendocument)
- [var openURL: OpenURLAction](/documentation/swiftui/environmentvalues/openurl)
- [var openWindow: OpenWindowAction](/documentation/swiftui/environmentvalues/openwindow)
- [var pushWindow: PushWindowAction](/documentation/swiftui/environmentvalues/pushwindow)
- [var purchase: PurchaseAction](/documentation/swiftui/environmentvalues/purchase)
- [var refresh: RefreshAction?](/documentation/swiftui/environmentvalues/refresh)
- [var rename: RenameAction?](/documentation/swiftui/environmentvalues/rename)
- [var resetFocus: ResetFocusAction](/documentation/swiftui/environmentvalues/resetfocus)
- [var openSettings: OpenSettingsAction](/documentation/swiftui/environmentvalues/opensettings)

#### Authentication

- [var authorizationController: AuthorizationController](/documentation/swiftui/environmentvalues/authorizationcontroller)
- [var webAuthenticationSession: WebAuthenticationSession](/documentation/swiftui/environmentvalues/webauthenticationsession)

#### Controls and input

- [var buttonRepeatBehavior: ButtonRepeatBehavior](/documentation/swiftui/environmentvalues/buttonrepeatbehavior)
- [var controlSize: ControlSize](/documentation/swiftui/environmentvalues/controlsize)
- [var defaultWheelPickerItemHeight: CGFloat](/documentation/swiftui/environmentvalues/defaultwheelpickeritemheight)
- [var keyboardShortcut: KeyboardShortcut?](/documentation/swiftui/environmentvalues/keyboardshortcut)
- [var menuIndicatorVisibility: Visibility](/documentation/swiftui/environmentvalues/menuindicatorvisibility)
- [var menuOrder: MenuOrder](/documentation/swiftui/environmentvalues/menuorder)
- [var searchSuggestionsPlacement: SearchSuggestionsPlacement](/documentation/swiftui/environmentvalues/searchsuggestionsplacement)
- [var preferredPencilDoubleTapAction: PencilPreferredAction](/documentation/swiftui/environmentvalues/preferredpencildoubletapaction)
- [var preferredPencilSqueezeAction: PencilPreferredAction](/documentation/swiftui/environmentvalues/preferredpencilsqueezeaction)

#### Display characteristics

- [var appearsActive: Bool](/documentation/swiftui/environmentvalues/appearsactive)
- [var colorScheme: ColorScheme](/documentation/swiftui/environmentvalues/colorscheme)
- [var colorSchemeContrast: ColorSchemeContrast](/documentation/swiftui/environmentvalues/colorschemecontrast)
- [var displayScale: CGFloat](/documentation/swiftui/environmentvalues/displayscale)
- [var horizontalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/horizontalsizeclass)
- [var imageScale: Image.Scale](/documentation/swiftui/environmentvalues/imagescale)
- [var pixelLength: CGFloat](/documentation/swiftui/environmentvalues/pixellength)
- [var sidebarRowSize: SidebarRowSize](/documentation/swiftui/environmentvalues/sidebarrowsize)
- [var verticalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/verticalsizeclass)
- [var immersiveSpaceDisplacement: Pose3D](/documentation/swiftui/environmentvalues/immersivespacedisplacement)
- [var labelsVisibility: Visibility](/documentation/swiftui/environmentvalues/labelsvisibility)
- [var materialActiveAppearance: MaterialActiveAppearance](/documentation/swiftui/environmentvalues/materialactiveappearance)
- [TabBarPlacement](/documentation/swiftui/tabbarplacement)

##### Type Properties

- [static let bottomBar: TabBarPlacement](/documentation/swiftui/tabbarplacement/bottombar)
- [static let ornament: TabBarPlacement](/documentation/swiftui/tabbarplacement/ornament)
- [static let pageIndicator: TabBarPlacement](/documentation/swiftui/tabbarplacement/pageindicator)
- [static let sidebar: TabBarPlacement](/documentation/swiftui/tabbarplacement/sidebar)
- [static let topBar: TabBarPlacement](/documentation/swiftui/tabbarplacement/topbar)
- [var toolbarLabelStyle: ToolbarLabelStyle?](/documentation/swiftui/environmentvalues/toolbarlabelstyle)

#### Global objects

- [var calendar: Calendar](/documentation/swiftui/environmentvalues/calendar)
- [var documentConfiguration: DocumentConfiguration?](/documentation/swiftui/environmentvalues/documentconfiguration)
- [var locale: Locale](/documentation/swiftui/environmentvalues/locale)
- [var managedObjectContext: NSManagedObjectContext](/documentation/swiftui/environmentvalues/managedobjectcontext)
- [var modelContext: ModelContext](/documentation/swiftui/environmentvalues/modelcontext)
- [var timeZone: TimeZone](/documentation/swiftui/environmentvalues/timezone)
- [var undoManager: UndoManager?](/documentation/swiftui/environmentvalues/undomanager)

#### Scrolling

- [var isScrollEnabled: Bool](/documentation/swiftui/environmentvalues/isscrollenabled)
- [var horizontalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/horizontalscrollindicatorvisibility)
- [var verticalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/verticalscrollindicatorvisibility)
- [var scrollDismissesKeyboardMode: ScrollDismissesKeyboardMode](/documentation/swiftui/environmentvalues/scrolldismisseskeyboardmode)
- [var horizontalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/horizontalscrollbouncebehavior)
- [var verticalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/verticalscrollbouncebehavior)

#### State

- [var editMode: Binding<EditMode>?](/documentation/swiftui/environmentvalues/editmode)
- [var isActivityFullscreen: Bool](/documentation/swiftui/environmentvalues/isactivityfullscreen)
- [var isEnabled: Bool](/documentation/swiftui/environmentvalues/isenabled)
- [var isFocused: Bool](/documentation/swiftui/environmentvalues/isfocused)
- [var isFocusEffectEnabled: Bool](/documentation/swiftui/environmentvalues/isfocuseffectenabled)
- [var isHoverEffectEnabled: Bool](/documentation/swiftui/environmentvalues/ishovereffectenabled)
- [var isLuminanceReduced: Bool](/documentation/swiftui/environmentvalues/isluminancereduced)
- [var isPresented: Bool](/documentation/swiftui/environmentvalues/ispresented)
- [var isSceneCaptured: Bool](/documentation/swiftui/environmentvalues/isscenecaptured)
- [var isSearching: Bool](/documentation/swiftui/environmentvalues/issearching)
- [var isTabBarShowingSections: Bool](/documentation/swiftui/environmentvalues/istabbarshowingsections)
- [var scenePhase: ScenePhase](/documentation/swiftui/environmentvalues/scenephase)
- [var supportsMultipleWindows: Bool](/documentation/swiftui/environmentvalues/supportsmultiplewindows)

#### StoreKit configuration

- [var displayStoreKitMessage: DisplayMessageAction](/documentation/swiftui/environmentvalues/displaystorekitmessage)
- [var requestReview: RequestReviewAction](/documentation/swiftui/environmentvalues/requestreview)

#### Text styles

- [var allowsTightening: Bool](/documentation/swiftui/environmentvalues/allowstightening)
- [var autocorrectionDisabled: Bool](/documentation/swiftui/environmentvalues/autocorrectiondisabled)
- [var dynamicTypeSize: DynamicTypeSize](/documentation/swiftui/environmentvalues/dynamictypesize)
- [var font: Font?](/documentation/swiftui/environmentvalues/font)
- [var layoutDirection: LayoutDirection](/documentation/swiftui/environmentvalues/layoutdirection)
- [var lineLimit: Int?](/documentation/swiftui/environmentvalues/linelimit)
- [var lineSpacing: CGFloat](/documentation/swiftui/environmentvalues/linespacing)
- [var minimumScaleFactor: CGFloat](/documentation/swiftui/environmentvalues/minimumscalefactor)
- [var multilineTextAlignment: TextAlignment](/documentation/swiftui/environmentvalues/multilinetextalignment)
- [var textCase: Text.Case?](/documentation/swiftui/environmentvalues/textcase)
- [var truncationMode: Text.TruncationMode](/documentation/swiftui/environmentvalues/truncationmode)
- [var textSelectionAffinity: TextSelectionAffinity](/documentation/swiftui/environmentvalues/textselectionaffinity)

#### View attributes

- [var allowedDynamicRange: Image.DynamicRange?](/documentation/swiftui/environmentvalues/alloweddynamicrange)
- [var backgroundMaterial: Material?](/documentation/swiftui/environmentvalues/backgroundmaterial)
- [var backgroundProminence: BackgroundProminence](/documentation/swiftui/environmentvalues/backgroundprominence)
- [var backgroundStyle: AnyShapeStyle?](/documentation/swiftui/environmentvalues/backgroundstyle)
- [var badgeProminence: BadgeProminence](/documentation/swiftui/environmentvalues/badgeprominence)
- [var contentTransition: ContentTransition](/documentation/swiftui/environmentvalues/contenttransition)
- [var contentTransitionAddsDrawingGroup: Bool](/documentation/swiftui/environmentvalues/contenttransitionaddsdrawinggroup)
- [var defaultMinListHeaderHeight: CGFloat?](/documentation/swiftui/environmentvalues/defaultminlistheaderheight)
- [var defaultMinListRowHeight: CGFloat](/documentation/swiftui/environmentvalues/defaultminlistrowheight)
- [var headerProminence: Prominence](/documentation/swiftui/environmentvalues/headerprominence)
- [var physicalMetrics: PhysicalMetricsConverter](/documentation/swiftui/environmentvalues/physicalmetrics)
- [var realityKitScene: Scene?](/documentation/swiftui/environmentvalues/realitykitscene)
- [var realityViewCameraControls: CameraControls](/documentation/swiftui/environmentvalues/realityviewcameracontrols)
- [var redactionReasons: RedactionReasons](/documentation/swiftui/environmentvalues/redactionreasons)
- [var springLoadingBehavior: SpringLoadingBehavior](/documentation/swiftui/environmentvalues/springloadingbehavior)
- [var symbolRenderingMode: SymbolRenderingMode?](/documentation/swiftui/environmentvalues/symbolrenderingmode)
- [var symbolVariants: SymbolVariants](/documentation/swiftui/environmentvalues/symbolvariants)
- [var worldTrackingLimitations: Set<WorldTrackingLimitation>](/documentation/swiftui/environmentvalues/worldtrackinglimitations)

#### Widgets

- [var showsWidgetContainerBackground: Bool](/documentation/swiftui/environmentvalues/showswidgetcontainerbackground)
- [var showsWidgetLabel: Bool](/documentation/swiftui/environmentvalues/showswidgetlabel)
- [var widgetFamily: WidgetFamily](/documentation/swiftui/environmentvalues/widgetfamily)
- [var widgetRenderingMode: WidgetRenderingMode](/documentation/swiftui/environmentvalues/widgetrenderingmode)
- [var widgetContentMargins: EdgeInsets](/documentation/swiftui/environmentvalues/widgetcontentmargins)

#### Deprecated environment values

- [var disableAutocorrection: Bool?](/documentation/swiftui/environmentvalues/disableautocorrection)
- [var sizeCategory: ContentSizeCategory](/documentation/swiftui/environmentvalues/sizecategory)
- [var presentationMode: Binding<PresentationMode>](/documentation/swiftui/environmentvalues/presentationmode)
- [PresentationMode](/documentation/swiftui/presentationmode)

##### Checking presentation

- [var isPresented: Bool](/documentation/swiftui/presentationmode/ispresented)

##### Dismissing presentation

- [func dismiss()](/documentation/swiftui/presentationmode/dismiss())
- [var complicationRenderingMode: ComplicationRenderingMode](/documentation/swiftui/environmentvalues/complicationrenderingmode)
- [var controlActiveState: ControlActiveState](/documentation/swiftui/environmentvalues/controlactivestate)

#### Instance Properties

- [var accessibilityReduceHighlightingEffects: Bool](/documentation/swiftui/environmentvalues/accessibilityreducehighlightingeffects)
- [var accessibilityShowBorders: Bool](/documentation/swiftui/environmentvalues/accessibilityshowborders)
- [var activityFamily: ActivityFamily](/documentation/swiftui/environmentvalues/activityfamily)
- [var askPermission: AskPermissionAction](/documentation/swiftui/environmentvalues/askpermission) **Beta**
- [var buttonSizing: ButtonSizing](/documentation/swiftui/environmentvalues/buttonsizing)
- [var credentialDataManager: CredentialDataManager](/documentation/swiftui/environmentvalues/credentialdatamanager)
- [var credentialExportManager: ASCredentialExportManager](/documentation/swiftui/environmentvalues/credentialexportmanager)
- [var credentialImportManager: ASCredentialImportManager](/documentation/swiftui/environmentvalues/credentialimportmanager)
- [var devicePickerSupports: DevicePickerSupportedAction](/documentation/swiftui/environmentvalues/devicepickersupports)
- [var findContext: FindContext?](/documentation/swiftui/environmentvalues/findcontext)
- [var fontResolutionContext: Font.Context](/documentation/swiftui/environmentvalues/fontresolutioncontext)
- [var imagePlaygroundAllowedGenerationStyles: [ImagePlaygroundStyle]](/documentation/swiftui/environmentvalues/imageplaygroundallowedgenerationstyles)
- [var imagePlaygroundOptions: ImagePlaygroundOptions](/documentation/swiftui/environmentvalues/imageplaygroundoptions)
- [var imagePlaygroundPersonalizationPolicy: ImagePlaygroundPersonalizationPolicy](/documentation/swiftui/environmentvalues/imageplaygroundpersonalizationpolicy)
- [var imagePlaygroundSelectedGenerationStyle: ImagePlaygroundStyle](/documentation/swiftui/environmentvalues/imageplaygroundselectedgenerationstyle)
- [var isActivityUpdateReduced: Bool](/documentation/swiftui/environmentvalues/isactivityupdatereduced)
- [var isUserAuthenticationEnabled: Bool](/documentation/swiftui/environmentvalues/isuserauthenticationenabled)
- [var labelIconToTitleSpacing: CGFloat?](/documentation/swiftui/environmentvalues/labelicontotitlespacing)
- [var labelReservedIconWidth: CGFloat?](/documentation/swiftui/environmentvalues/labelreservediconwidth)
- [var levelOfDetail: LevelOfDetail](/documentation/swiftui/environmentvalues/levelofdetail)
- [var lineHeight: AttributedString.LineHeight?](/documentation/swiftui/environmentvalues/lineheight)
- [var navigationLinkIndicatorVisibility: Visibility](/documentation/swiftui/environmentvalues/navigationlinkindicatorvisibility)
- [var remoteDeviceIdentifier: RemoteDeviceIdentifier?](/documentation/swiftui/environmentvalues/remotedeviceidentifier)
- [var requestAgeRange: DeclaredAgeRangeAction](/documentation/swiftui/environmentvalues/requestagerange)
- [var requestAppDeletion: RequestAppDeletionAction](/documentation/swiftui/environmentvalues/requestappdeletion)
- [var showSignificantUpdateAcknowledgment: SignificantUpdateAction](/documentation/swiftui/environmentvalues/showsignificantupdateacknowledgment)
- [var supportedActivityFamilies: Set<ActivityFamily>](/documentation/swiftui/environmentvalues/supportedactivityfamilies)
- [var supportsImagePlayground: Bool](/documentation/swiftui/environmentvalues/supportsimageplayground)
- [var supportsRemoteScenes: Bool](/documentation/swiftui/environmentvalues/supportsremotescenes)
- [var surfaceSnappingInfo: SurfaceSnappingInfo](/documentation/swiftui/environmentvalues/surfacesnappinginfo)
- [var symbolColorRenderingMode: SymbolColorRenderingMode?](/documentation/swiftui/environmentvalues/symbolcolorrenderingmode)
- [var symbolVariableValueMode: SymbolVariableValueMode?](/documentation/swiftui/environmentvalues/symbolvariablevaluemode)
- [var tabBarPlacement: TabBarPlacement?](/documentation/swiftui/environmentvalues/tabbarplacement)
- [var tabViewBottomAccessoryPlacement: TabViewBottomAccessoryPlacement?](/documentation/swiftui/environmentvalues/tabviewbottomaccessoryplacement)
- [var windowClippingMargins: EdgeInsets3D](/documentation/swiftui/environmentvalues/windowclippingmargins)
- [var writingToolsBehavior: WritingToolsBehavior?](/documentation/swiftui/environmentvalues/writingtoolsbehavior)

### Creating custom environment values

- [macro Entry()](/documentation/swiftui/entry())
- [EnvironmentKey](/documentation/swiftui/environmentkey)

#### Getting the default value

- [static var defaultValue: Self.Value](/documentation/swiftui/environmentkey/defaultvalue)
- [Value](/documentation/swiftui/environmentkey/value)

### Modifying the environment of a view

- [func environment<T>(T?) -> some View](/documentation/swiftui/view/environment(_:))
- [func environment<V>(WritableKeyPath<EnvironmentValues, V>, V) -> some View](/documentation/swiftui/view/environment(_:_:))
- [func transformEnvironment<V>(WritableKeyPath<EnvironmentValues, V>, transform: (inout V) -> Void) -> some View](/documentation/swiftui/view/transformenvironment(_:transform:))

### Modifying the environment of a scene

- [func environment<T>(T?) -> some Scene](/documentation/swiftui/scene/environment(_:))
- [func environment<V>(WritableKeyPath<EnvironmentValues, V>, V) -> some Scene](/documentation/swiftui/scene/environment(_:_:))
- [func transformEnvironment<V>(WritableKeyPath<EnvironmentValues, V>, transform: (inout V) -> Void) -> some Scene](/documentation/swiftui/scene/transformenvironment(_:transform:))
- [Preferences](/documentation/swiftui/preferences)

### Setting preferences

- [func preference<K>(key: K.Type, value: K.Value) -> some View](/documentation/swiftui/view/preference(key:value:))
- [func transformPreference<K>(K.Type, (inout K.Value) -> Void) -> some View](/documentation/swiftui/view/transformpreference(_:_:))

### Creating custom preferences

- [PreferenceKey](/documentation/swiftui/preferencekey)

#### Getting the default value

- [static var defaultValue: Self.Value](/documentation/swiftui/preferencekey/defaultvalue)
- [Value](/documentation/swiftui/preferencekey/value)

#### Combining preferences

- [static func reduce(value: inout Self.Value, nextValue: () -> Self.Value)](/documentation/swiftui/preferencekey/reduce(value:nextvalue:))

### Setting preferences based on geometry

- [func anchorPreference<A, K>(key: K.Type, value: Anchor<A>.Source, transform: (Anchor<A>) -> K.Value) -> some View](/documentation/swiftui/view/anchorpreference(key:value:transform:))
- [func transformAnchorPreference<A, K>(key: K.Type, value: Anchor<A>.Source, transform: (inout K.Value, Anchor<A>) -> Void) -> some View](/documentation/swiftui/view/transformanchorpreference(key:value:transform:))

### Responding to changes in preferences

- [func onPreferenceChange<K>(K.Type, perform: (K.Value) -> Void) -> some View](/documentation/swiftui/view/onpreferencechange(_:perform:))

### Generating backgrounds and overlays from preferences

- [func backgroundPreferenceValue<Key, T>(Key.Type, (Key.Value) -> T) -> some View](/documentation/swiftui/view/backgroundpreferencevalue(_:_:))
- [func backgroundPreferenceValue<K, V>(K.Type, alignment: Alignment, (K.Value) -> V) -> some View](/documentation/swiftui/view/backgroundpreferencevalue(_:alignment:_:))
- [func overlayPreferenceValue<Key, T>(Key.Type, (Key.Value) -> T) -> some View](/documentation/swiftui/view/overlaypreferencevalue(_:_:))
- [func overlayPreferenceValue<K, V>(K.Type, alignment: Alignment, (K.Value) -> V) -> some View](/documentation/swiftui/view/overlaypreferencevalue(_:alignment:_:))
- [Persistent storage](/documentation/swiftui/persistent-storage)

### Saving state across app launches

- [Restoring your app’s state with SwiftUI](/documentation/swiftui/restoring-your-app-s-state-with-swiftui)
- [func defaultAppStorage(UserDefaults) -> some View](/documentation/swiftui/view/defaultappstorage(_:))
- [AppStorage](/documentation/swiftui/appstorage)

#### Storing a value

- [init(wrappedValue:_:store:)](/documentation/swiftui/appstorage/init(wrappedvalue:_:store:))
- [init(_:store:)](/documentation/swiftui/appstorage/init(_:store:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/appstorage/wrappedvalue)
- [var projectedValue: Binding<Value>](/documentation/swiftui/appstorage/projectedvalue)
- [SceneStorage](/documentation/swiftui/scenestorage)

#### Storing a value

- [init(wrappedValue:_:)](/documentation/swiftui/scenestorage/init(wrappedvalue:_:))
- [init(_:)](/documentation/swiftui/scenestorage/init(_:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/scenestorage/wrappedvalue)
- [var projectedValue: Binding<Value>](/documentation/swiftui/scenestorage/projectedvalue)

#### Initializers

- [init(wrappedValue: Value, String, store: UserDefaults?)](/documentation/swiftui/scenestorage/init(wrappedvalue:_:store:))

### Accessing Core Data

- [Loading and displaying a large data feed](/documentation/swiftui/loading-and-displaying-a-large-data-feed)
- [var managedObjectContext: NSManagedObjectContext](/documentation/swiftui/environmentvalues/managedobjectcontext)
- [FetchRequest](/documentation/swiftui/fetchrequest)

#### Creating a fetch request

- [init(sortDescriptors:predicate:animation:)](/documentation/swiftui/fetchrequest/init(sortdescriptors:predicate:animation:))
- [init(entity: NSEntityDescription, sortDescriptors: [NSSortDescriptor], predicate: NSPredicate?, animation: Animation?)](/documentation/swiftui/fetchrequest/init(entity:sortdescriptors:predicate:animation:))

#### Creating a fully configured fetch request

- [init(fetchRequest: NSFetchRequest<Result>, animation: Animation?)](/documentation/swiftui/fetchrequest/init(fetchrequest:animation:))
- [init(fetchRequest: NSFetchRequest<Result>, transaction: Transaction)](/documentation/swiftui/fetchrequest/init(fetchrequest:transaction:))

#### Configuring a request dynamically

- [FetchRequest.Configuration](/documentation/swiftui/fetchrequest/configuration)

##### Setting a predicate

- [var nsPredicate: NSPredicate?](/documentation/swiftui/fetchrequest/configuration/nspredicate)

##### Setting sort descriptors

- [var sortDescriptors: [SortDescriptor<Result>]](/documentation/swiftui/fetchrequest/configuration/sortdescriptors)
- [var nsSortDescriptors: [NSSortDescriptor]](/documentation/swiftui/fetchrequest/configuration/nssortdescriptors)
- [var projectedValue: Binding<FetchRequest<Result>.Configuration>](/documentation/swiftui/fetchrequest/projectedvalue)

#### Getting the fetched results

- [func update()](/documentation/swiftui/fetchrequest/update())
- [var wrappedValue: FetchedResults<Result>](/documentation/swiftui/fetchrequest/wrappedvalue)

#### Default Implementations

- [DynamicProperty Implementations](/documentation/swiftui/fetchrequest/dynamicproperty-implementations)

##### Instance Methods

- [func update()](/documentation/swiftui/fetchrequest/update())
- [FetchedResults](/documentation/swiftui/fetchedresults)

#### Configuring the associated fetch request

- [var nsPredicate: NSPredicate?](/documentation/swiftui/fetchedresults/nspredicate)
- [var sortDescriptors: [SortDescriptor<Result>]](/documentation/swiftui/fetchedresults/sortdescriptors)
- [var nsSortDescriptors: [NSSortDescriptor]](/documentation/swiftui/fetchedresults/nssortdescriptors)

#### Getting indices

- [var startIndex: Int](/documentation/swiftui/fetchedresults/startindex)
- [var endIndex: Int](/documentation/swiftui/fetchedresults/endindex)

#### Getting results

- [subscript(Int) -> Result](/documentation/swiftui/fetchedresults/subscript(_:))
- [SectionedFetchRequest](/documentation/swiftui/sectionedfetchrequest)

#### Creating a fetch request

- [init(sectionIdentifier:sortDescriptors:predicate:animation:)](/documentation/swiftui/sectionedfetchrequest/init(sectionidentifier:sortdescriptors:predicate:animation:))
- [init(entity: NSEntityDescription, sectionIdentifier: KeyPath<Result, SectionIdentifier>, sortDescriptors: [NSSortDescriptor], predicate: NSPredicate?, animation: Animation?)](/documentation/swiftui/sectionedfetchrequest/init(entity:sectionidentifier:sortdescriptors:predicate:animation:))

#### Creating a fully configured fetch request

- [init(fetchRequest: NSFetchRequest<Result>, sectionIdentifier: KeyPath<Result, SectionIdentifier>, animation: Animation?)](/documentation/swiftui/sectionedfetchrequest/init(fetchrequest:sectionidentifier:animation:))
- [init(fetchRequest: NSFetchRequest<Result>, sectionIdentifier: KeyPath<Result, SectionIdentifier>, transaction: Transaction)](/documentation/swiftui/sectionedfetchrequest/init(fetchrequest:sectionidentifier:transaction:))

#### Configuring a request dynamically

- [SectionedFetchRequest.Configuration](/documentation/swiftui/sectionedfetchrequest/configuration)

##### Setting the section identifier

- [var sectionIdentifier: KeyPath<Result, SectionIdentifier>](/documentation/swiftui/sectionedfetchrequest/configuration/sectionidentifier)

##### Setting a predicate

- [var nsPredicate: NSPredicate?](/documentation/swiftui/sectionedfetchrequest/configuration/nspredicate)

##### Setting sort descriptors

- [var sortDescriptors: [SortDescriptor<Result>]](/documentation/swiftui/sectionedfetchrequest/configuration/sortdescriptors)
- [var nsSortDescriptors: [NSSortDescriptor]](/documentation/swiftui/sectionedfetchrequest/configuration/nssortdescriptors)
- [var projectedValue: Binding<SectionedFetchRequest<SectionIdentifier, Result>.Configuration>](/documentation/swiftui/sectionedfetchrequest/projectedvalue)

#### Getting the fetched results

- [func update()](/documentation/swiftui/sectionedfetchrequest/update())
- [var wrappedValue: SectionedFetchResults<SectionIdentifier, Result>](/documentation/swiftui/sectionedfetchrequest/wrappedvalue)

#### Default Implementations

- [DynamicProperty Implementations](/documentation/swiftui/sectionedfetchrequest/dynamicproperty-implementations)

##### Instance Methods

- [func update()](/documentation/swiftui/sectionedfetchrequest/update())
- [SectionedFetchResults](/documentation/swiftui/sectionedfetchresults)

#### Configuring the associated sectioned fetch request

- [var nsPredicate: NSPredicate?](/documentation/swiftui/sectionedfetchresults/nspredicate)
- [var sortDescriptors: [SortDescriptor<Result>]](/documentation/swiftui/sectionedfetchresults/sortdescriptors)
- [var nsSortDescriptors: [NSSortDescriptor]](/documentation/swiftui/sectionedfetchresults/nssortdescriptors)
- [var sectionIdentifier: KeyPath<Result, SectionIdentifier>](/documentation/swiftui/sectionedfetchresults/sectionidentifier)
- [SectionedFetchResults.Section](/documentation/swiftui/sectionedfetchresults/section)

##### Identifying the section

- [let id: SectionIdentifier](/documentation/swiftui/sectionedfetchresults/section/id)

##### Getting indices

- [var startIndex: Int](/documentation/swiftui/sectionedfetchresults/section/startindex)
- [var endIndex: Int](/documentation/swiftui/sectionedfetchresults/section/endindex)

##### Getting results

- [subscript(Int) -> Result](/documentation/swiftui/sectionedfetchresults/section/subscript(_:))

#### Getting indices

- [var startIndex: Int](/documentation/swiftui/sectionedfetchresults/startindex)
- [var endIndex: Int](/documentation/swiftui/sectionedfetchresults/endindex)

#### Getting results

- [subscript(Int) -> SectionedFetchResults<SectionIdentifier, Result>.Section](/documentation/swiftui/sectionedfetchresults/subscript(_:))

