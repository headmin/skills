# Accessibility — SwiftUI Reference

## Contents
- [Accessibility](#accessibility)
  - [Essentials](#essentials)
  - [Creating accessible elements](#creating-accessible-elements)
  - [Identifying elements](#identifying-elements)
  - [Hiding elements](#hiding-elements)
  - [Supporting types](#supporting-types)
  - [Managing color](#managing-color)
  - [Enlarging content](#enlarging-content)
  - [Improving legibility](#improving-legibility)
  - [Minimizing motion](#minimizing-motion)
  - [Using assistive access](#using-assistive-access)
  - [Adding actions to views](#adding-actions-to-views)
  - [Offering Quick Actions to people](#offering-quick-actions-to-people)
  - [Making gestures accessible](#making-gestures-accessible)
  - [Controlling focus](#controlling-focus)
  - [Managing interactivity](#managing-interactivity)
  - [Applying labels](#applying-labels)
  - [Describing values](#describing-values)
  - [Describing content](#describing-content)
  - [Describing charts](#describing-charts)
  - [Adding custom descriptions](#adding-custom-descriptions)
  - [Assigning traits to content](#assigning-traits-to-content)
  - [Offering hints](#offering-hints)
  - [Configuring VoiceOver](#configuring-voiceover)
  - [Working with rotors](#working-with-rotors)
  - [Creating rotors](#creating-rotors)
  - [Replacing system rotors](#replacing-system-rotors)
  - [Configuring rotors](#configuring-rotors)

---
## Accessibility

- [Accessibility fundamentals](/documentation/swiftui/accessibility-fundamentals)

### Essentials

- [Creating accessible views](/documentation/swiftui/creating-accessible-views)

### Creating accessible elements

- [func accessibilityElement(children: AccessibilityChildBehavior) -> some View](/documentation/swiftui/view/accessibilityelement(children:))
- [func accessibilityChildren<V>(children: () -> V) -> some View](/documentation/swiftui/view/accessibilitychildren(children:))
- [func accessibilityRepresentation<V>(representation: () -> V) -> some View](/documentation/swiftui/view/accessibilityrepresentation(representation:))
- [AccessibilityChildBehavior](/documentation/swiftui/accessibilitychildbehavior)

#### Getting behaviors

- [static let combine: AccessibilityChildBehavior](/documentation/swiftui/accessibilitychildbehavior/combine)
- [static let contain: AccessibilityChildBehavior](/documentation/swiftui/accessibilitychildbehavior/contain)
- [static let ignore: AccessibilityChildBehavior](/documentation/swiftui/accessibilitychildbehavior/ignore)

### Identifying elements

- [func accessibilityIdentifier(String) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityidentifier(_:))
- [func accessibilityIdentifier(String, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityidentifier(_:isenabled:))

### Hiding elements

- [func accessibilityHidden(Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityhidden(_:))
- [func accessibilityHidden(Bool, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityhidden(_:isenabled:))

### Supporting types

- [AccessibilityTechnologies](/documentation/swiftui/accessibilitytechnologies)

#### Getting technology types

- [static let switchControl: AccessibilityTechnologies](/documentation/swiftui/accessibilitytechnologies/switchcontrol)
- [static let voiceOver: AccessibilityTechnologies](/documentation/swiftui/accessibilitytechnologies/voiceover)

#### Creating a technology type

- [init()](/documentation/swiftui/accessibilitytechnologies/init())
- [AccessibilityAttachmentModifier](/documentation/swiftui/accessibilityattachmentmodifier)
- [Accessible appearance](/documentation/swiftui/accessible-appearance)

### Managing color

- [func accessibilityIgnoresInvertColors(Bool) -> some View](/documentation/swiftui/view/accessibilityignoresinvertcolors(_:))
- [var accessibilityInvertColors: Bool](/documentation/swiftui/environmentvalues/accessibilityinvertcolors)
- [var accessibilityDifferentiateWithoutColor: Bool](/documentation/swiftui/environmentvalues/accessibilitydifferentiatewithoutcolor)

### Enlarging content

- [func accessibilityShowsLargeContentViewer() -> some View](/documentation/swiftui/view/accessibilityshowslargecontentviewer())
- [func accessibilityShowsLargeContentViewer<V>(() -> V) -> some View](/documentation/swiftui/view/accessibilityshowslargecontentviewer(_:))
- [var accessibilityLargeContentViewerEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilitylargecontentviewerenabled)

### Improving legibility

- [var accessibilityShowButtonShapes: Bool](/documentation/swiftui/environmentvalues/accessibilityshowbuttonshapes)
- [var accessibilityReduceTransparency: Bool](/documentation/swiftui/environmentvalues/accessibilityreducetransparency)
- [var legibilityWeight: LegibilityWeight?](/documentation/swiftui/environmentvalues/legibilityweight)
- [LegibilityWeight](/documentation/swiftui/legibilityweight)

#### Getting weights

- [case regular](/documentation/swiftui/legibilityweight/regular)
- [case bold](/documentation/swiftui/legibilityweight/bold)

#### Creating a weight

- [init?(UILegibilityWeight)](/documentation/swiftui/legibilityweight/init(_:))

### Minimizing motion

- [var accessibilityDimFlashingLights: Bool](/documentation/swiftui/environmentvalues/accessibilitydimflashinglights)
- [var accessibilityPlayAnimatedImages: Bool](/documentation/swiftui/environmentvalues/accessibilityplayanimatedimages)
- [var accessibilityReduceMotion: Bool](/documentation/swiftui/environmentvalues/accessibilityreducemotion)

### Using assistive access

- [var accessibilityAssistiveAccessEnabled: Bool](/documentation/swiftui/environmentvalues/accessibilityassistiveaccessenabled)
- [AssistiveAccess](/documentation/swiftui/assistiveaccess)

#### Initializers

- [init(content: () -> Content)](/documentation/swiftui/assistiveaccess/init(content:))
- [Accessible controls](/documentation/swiftui/accessible-controls)

### Adding actions to views

- [func accessibilityAction(AccessibilityActionKind, () -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaction(_:_:))
- [func accessibilityActions<Content>(() -> Content) -> some View](/documentation/swiftui/view/accessibilityactions(_:))
- [func accessibilityAction(named:_:)](/documentation/swiftui/view/accessibilityaction(named:_:))
- [func accessibilityAction<Label>(action: () -> Void, label: () -> Label) -> some View](/documentation/swiftui/view/accessibilityaction(action:label:))
- [func accessibilityAction<I, Label>(intent: I, label: () -> Label) -> some View](/documentation/swiftui/view/accessibilityaction(intent:label:))
- [func accessibilityAction<I>(AccessibilityActionKind, intent: I) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaction(_:intent:))
- [func accessibilityAction(named:intent:)](/documentation/swiftui/view/accessibilityaction(named:intent:))
- [func accessibilityAdjustableAction((AccessibilityAdjustmentDirection) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityadjustableaction(_:))
- [func accessibilityScrollAction((Edge) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityscrollaction(_:))
- [func accessibilityActions<Content>(category: AccessibilityActionCategory, () -> Content) -> some View](/documentation/swiftui/view/accessibilityactions(category:_:))
- [AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind)

#### Getting the kind of action

- [static let `default`: AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind/default)
- [static let delete: AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind/delete)
- [static let escape: AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind/escape)
- [static let magicTap: AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind/magictap)
- [static let showMenu: AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind/showmenu)

#### Creating an action type

- [init(named: Text)](/documentation/swiftui/accessibilityactionkind/init(named:))
- [AccessibilityAdjustmentDirection](/documentation/swiftui/accessibilityadjustmentdirection)

#### Getting an adjustment direction

- [case decrement](/documentation/swiftui/accessibilityadjustmentdirection/decrement)
- [case increment](/documentation/swiftui/accessibilityadjustmentdirection/increment)
- [AccessibilityActionCategory](/documentation/swiftui/accessibilityactioncategory)

#### Initializers

- [init(_:)](/documentation/swiftui/accessibilityactioncategory/init(_:))

#### Type Properties

- [static let `default`: AccessibilityActionCategory](/documentation/swiftui/accessibilityactioncategory/default)
- [static let edit: AccessibilityActionCategory](/documentation/swiftui/accessibilityactioncategory/edit)

### Offering Quick Actions to people

- [func accessibilityQuickAction<Style, Content>(style: Style, content: () -> Content) -> some View](/documentation/swiftui/view/accessibilityquickaction(style:content:))
- [func accessibilityQuickAction<Style, Content>(style: Style, isActive: Binding<Bool>, content: () -> Content) -> some View](/documentation/swiftui/view/accessibilityquickaction(style:isactive:content:))
- [AccessibilityQuickActionStyle](/documentation/swiftui/accessibilityquickactionstyle)

#### Getting built-in menu styles

- [static var outline: AccessibilityQuickActionOutlineStyle](/documentation/swiftui/accessibilityquickactionstyle/outline)
- [static var prompt: AccessibilityQuickActionPromptStyle](/documentation/swiftui/accessibilityquickactionstyle/prompt)

#### Supporting types

- [AccessibilityQuickActionOutlineStyle](/documentation/swiftui/accessibilityquickactionoutlinestyle)
- [AccessibilityQuickActionPromptStyle](/documentation/swiftui/accessibilityquickactionpromptstyle)

### Making gestures accessible

- [func accessibilityActivationPoint(_:)](/documentation/swiftui/view/accessibilityactivationpoint(_:))
- [func accessibilityActivationPoint(_:isEnabled:)](/documentation/swiftui/view/accessibilityactivationpoint(_:isenabled:))
- [func accessibilityDragPoint(_:description:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:))
- [func accessibilityDragPoint(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:isenabled:))
- [func accessibilityDropPoint(_:description:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:))
- [func accessibilityDropPoint(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:isenabled:))
- [func accessibilityDirectTouch(Bool, options: AccessibilityDirectTouchOptions) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitydirecttouch(_:options:))
- [func accessibilityZoomAction((AccessibilityZoomGestureAction) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityzoomaction(_:))
- [AccessibilityDirectTouchOptions](/documentation/swiftui/accessibilitydirecttouchoptions)

#### Getting the options

- [static let requiresActivation: AccessibilityDirectTouchOptions](/documentation/swiftui/accessibilitydirecttouchoptions/requiresactivation)
- [static let silentOnTouch: AccessibilityDirectTouchOptions](/documentation/swiftui/accessibilitydirecttouchoptions/silentontouch)

#### Creating a set of options

- [init(rawValue: AccessibilityDirectTouchOptions.RawValue)](/documentation/swiftui/accessibilitydirecttouchoptions/init(rawvalue:))
- [AccessibilityZoomGestureAction](/documentation/swiftui/accessibilityzoomgestureaction)

#### Getting the action’s direction

- [let direction: AccessibilityZoomGestureAction.Direction](/documentation/swiftui/accessibilityzoomgestureaction/direction-swift.property)
- [AccessibilityZoomGestureAction.Direction](/documentation/swiftui/accessibilityzoomgestureaction/direction-swift.enum)

##### Getting the direction

- [case zoomIn](/documentation/swiftui/accessibilityzoomgestureaction/direction-swift.enum/zoomin)
- [case zoomOut](/documentation/swiftui/accessibilityzoomgestureaction/direction-swift.enum/zoomout)

#### Getting location information

- [let location: UnitPoint](/documentation/swiftui/accessibilityzoomgestureaction/location)
- [let point: CGPoint](/documentation/swiftui/accessibilityzoomgestureaction/point)

### Controlling focus

- [func accessibilityFocused(AccessibilityFocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/accessibilityfocused(_:))
- [func accessibilityFocused<Value>(AccessibilityFocusState<Value>.Binding, equals: Value) -> some View](/documentation/swiftui/view/accessibilityfocused(_:equals:))
- [AccessibilityFocusState](/documentation/swiftui/accessibilityfocusstate)

#### Creating a focus state

- [init()](/documentation/swiftui/accessibilityfocusstate/init())
- [init(for:)](/documentation/swiftui/accessibilityfocusstate/init(for:))

#### Getting the state

- [var projectedValue: AccessibilityFocusState<Value>.Binding](/documentation/swiftui/accessibilityfocusstate/projectedvalue)
- [var wrappedValue: Value](/documentation/swiftui/accessibilityfocusstate/wrappedvalue)
- [AccessibilityFocusState.Binding](/documentation/swiftui/accessibilityfocusstate/binding)

##### Getting the state

- [var projectedValue: AccessibilityFocusState<Value>.Binding](/documentation/swiftui/accessibilityfocusstate/binding/projectedvalue)
- [var wrappedValue: Value](/documentation/swiftui/accessibilityfocusstate/binding/wrappedvalue)

### Managing interactivity

- [func accessibilityRespondsToUserInteraction(Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:))
- [func accessibilityRespondsToUserInteraction(Bool, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:isenabled:))
- [Accessible descriptions](/documentation/swiftui/accessible-descriptions)

### Applying labels

- [func accessibilityLabel(_:)](/documentation/swiftui/view/accessibilitylabel(_:))
- [func accessibilityLabel(_:isEnabled:)](/documentation/swiftui/view/accessibilitylabel(_:isenabled:))
- [func accessibilityLabel<V>(content: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/accessibilitylabel(content:))
- [func accessibilityInputLabels(_:)](/documentation/swiftui/view/accessibilityinputlabels(_:))
- [func accessibilityInputLabels(_:isEnabled:)](/documentation/swiftui/view/accessibilityinputlabels(_:isenabled:))
- [func accessibilityLabeledPair<ID>(role: AccessibilityLabeledPairRole, id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilitylabeledpair(role:id:in:))
- [AccessibilityLabeledPairRole](/documentation/swiftui/accessibilitylabeledpairrole)

#### Getting roles

- [case content](/documentation/swiftui/accessibilitylabeledpairrole/content)
- [case label](/documentation/swiftui/accessibilitylabeledpairrole/label)

### Describing values

- [func accessibilityValue(_:)](/documentation/swiftui/view/accessibilityvalue(_:))
- [func accessibilityValue(_:isEnabled:)](/documentation/swiftui/view/accessibilityvalue(_:isenabled:))

### Describing content

- [func accessibilityTextContentType(AccessibilityTextContentType) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitytextcontenttype(_:))
- [func accessibilityHeading(AccessibilityHeadingLevel) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityheading(_:))
- [AccessibilityHeadingLevel](/documentation/swiftui/accessibilityheadinglevel)

#### Getting the heading level

- [case h1](/documentation/swiftui/accessibilityheadinglevel/h1)
- [case h2](/documentation/swiftui/accessibilityheadinglevel/h2)
- [case h3](/documentation/swiftui/accessibilityheadinglevel/h3)
- [case h4](/documentation/swiftui/accessibilityheadinglevel/h4)
- [case h5](/documentation/swiftui/accessibilityheadinglevel/h5)
- [case h6](/documentation/swiftui/accessibilityheadinglevel/h6)
- [case unspecified](/documentation/swiftui/accessibilityheadinglevel/unspecified)
- [AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype)

#### Getting content types

- [static let console: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/console)
- [static let fileSystem: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/filesystem)
- [static let messaging: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/messaging)
- [static let narrative: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/narrative)
- [static let plain: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/plain)
- [static let sourceCode: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/sourcecode)
- [static let spreadsheet: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/spreadsheet)
- [static let wordProcessing: AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype/wordprocessing)

### Describing charts

- [func accessibilityChartDescriptor<R>(R) -> some View](/documentation/swiftui/view/accessibilitychartdescriptor(_:))
- [AXChartDescriptorRepresentable](/documentation/swiftui/axchartdescriptorrepresentable)

#### Managing a descriptor

- [func makeChartDescriptor() -> AXChartDescriptor](/documentation/swiftui/axchartdescriptorrepresentable/makechartdescriptor())
- [func updateChartDescriptor(AXChartDescriptor)](/documentation/swiftui/axchartdescriptorrepresentable/updatechartdescriptor(_:))

### Adding custom descriptions

- [func accessibilityCustomContent(_:_:importance:)](/documentation/swiftui/view/accessibilitycustomcontent(_:_:importance:))
- [AccessibilityCustomContentKey](/documentation/swiftui/accessibilitycustomcontentkey)

#### Creating a key

- [init(_:)](/documentation/swiftui/accessibilitycustomcontentkey/init(_:))
- [init(_:id:)](/documentation/swiftui/accessibilitycustomcontentkey/init(_:id:))

### Assigning traits to content

- [func accessibilityAddTraits(AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaddtraits(_:))
- [func accessibilityRemoveTraits(AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityremovetraits(_:))
- [AccessibilityTraits](/documentation/swiftui/accessibilitytraits)

#### Getting traits

- [static let allowsDirectInteraction: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/allowsdirectinteraction)
- [static let causesPageTurn: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/causespageturn)
- [static let isButton: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/isbutton)
- [static let isHeader: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/isheader)
- [static let isImage: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/isimage)
- [static let isKeyboardKey: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/iskeyboardkey)
- [static let isLink: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/islink)
- [static let isModal: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/ismodal)
- [static let isSearchField: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/issearchfield)
- [static let isSelected: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/isselected)
- [static let isStaticText: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/isstatictext)
- [static let isSummaryElement: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/issummaryelement)
- [static let isToggle: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/istoggle)
- [static let playsSound: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/playssound)
- [static let startsMediaSession: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/startsmediasession)
- [static let updatesFrequently: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/updatesfrequently)

#### Type Properties

- [static let isTabBar: AccessibilityTraits](/documentation/swiftui/accessibilitytraits/istabbar)

### Offering hints

- [func accessibilityHint(_:)](/documentation/swiftui/view/accessibilityhint(_:))
- [func accessibilityHint(_:isEnabled:)](/documentation/swiftui/view/accessibilityhint(_:isenabled:))

### Configuring VoiceOver

- [func speechAdjustedPitch(Double) -> some View](/documentation/swiftui/view/speechadjustedpitch(_:))
- [func speechAlwaysIncludesPunctuation(Bool) -> some View](/documentation/swiftui/view/speechalwaysincludespunctuation(_:))
- [func speechAnnouncementsQueued(Bool) -> some View](/documentation/swiftui/view/speechannouncementsqueued(_:))
- [func speechSpellsOutCharacters(Bool) -> some View](/documentation/swiftui/view/speechspellsoutcharacters(_:))
- [Accessible navigation](/documentation/swiftui/accessible-navigation)

### Working with rotors

- [func accessibilityRotor(_:entries:)](/documentation/swiftui/view/accessibilityrotor(_:entries:))
- [func accessibilityRotor(_:entries:entryID:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entryid:entrylabel:))
- [func accessibilityRotor(_:entries:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entrylabel:))
- [func accessibilityRotor(_:textRanges:)](/documentation/swiftui/view/accessibilityrotor(_:textranges:))

### Creating rotors

- [AccessibilityRotorContent](/documentation/swiftui/accessibilityrotorcontent)

#### Supporting types

- [var body: Self.Body](/documentation/swiftui/accessibilityrotorcontent/body-swift.property)
- [Body](/documentation/swiftui/accessibilityrotorcontent/body-swift.associatedtype)
- [AccessibilityRotorContentBuilder](/documentation/swiftui/accessibilityrotorcontentbuilder)

#### Building navigation content

- [static buildBlock(_:)](/documentation/swiftui/accessibilityrotorcontentbuilder/buildblock(_:))
- [static func buildIf<Content>(Content?) -> some AccessibilityRotorContent](/documentation/swiftui/accessibilityrotorcontentbuilder/buildif(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/accessibilityrotorcontentbuilder/buildexpression(_:))
- [AccessibilityRotorEntry](/documentation/swiftui/accessibilityrotorentry)

#### Creating a rotor entry

- [init(_:textRange:prepare:)](/documentation/swiftui/accessibilityrotorentry/init(_:textrange:prepare:))
- [init(_:id:textRange:prepare:)](/documentation/swiftui/accessibilityrotorentry/init(_:id:textrange:prepare:))

#### Creating an identified rotor entry in a namespace

- [init(_:id:in:textRange:prepare:)](/documentation/swiftui/accessibilityrotorentry/init(_:id:in:textrange:prepare:))
- [init<L>(L, ID, in: Namespace.ID, textRange: Range<String.Index>?, prepare: () -> Void)](/documentation/swiftui/accessibilityrotorentry/init(_:_:in:textrange:prepare:))

### Replacing system rotors

- [AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor)

#### Iterating through text

- [static var textFields: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/textfields)
- [static var boldText: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/boldtext)
- [static var italicText: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/italictext)
- [static var underlineText: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/underlinetext)
- [static var misspelledWords: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/misspelledwords)

#### Iterating through headings

- [static var headings: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/headings)
- [static func headings(level: AccessibilityHeadingLevel) -> AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/headings(level:))

#### Iterating through links

- [static var links: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/links)
- [static func links(visited: Bool) -> AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/links(visited:))

#### Iterating through other elements

- [static var images: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/images)
- [static var landmarks: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/landmarks)
- [static var lists: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/lists)
- [static var tables: AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor/tables)

### Configuring rotors

- [func accessibilityRotorEntry<ID>(id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilityrotorentry(id:in:))
- [func accessibilityLinkedGroup<ID>(id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilitylinkedgroup(id:in:))
- [func accessibilitySortPriority(Double) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitysortpriority(_:))

