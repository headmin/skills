# Views: Effects and Geometry — SwiftUI Reference

## Contents
  - [Controlling text style](#controlling-text-style)
  - [Managing text layout](#managing-text-layout)
  - [Rendering text](#rendering-text)
  - [Limiting line count for multiline text](#limiting-line-count-for-multiline-text)
  - [Formatting multiline text](#formatting-multiline-text)
  - [Formatting date and time](#formatting-date-and-time)
  - [Managing text entry](#managing-text-entry)
  - [Dictating text](#dictating-text)
  - [Configuring the Writing Tools behavior](#configuring-the-writing-tools-behavior)
  - [Specifying text equivalents](#specifying-text-equivalents)
  - [Localizing text](#localizing-text)
  - [Deprecated types](#deprecated-types)
  - [Creating an image](#creating-an-image)
  - [Configuring an image](#configuring-an-image)
  - [Loading images asynchronously](#loading-images-asynchronously)
  - [Setting a symbol variant](#setting-a-symbol-variant)
  - [Managing symbol effects](#managing-symbol-effects)
  - [Setting symbol rendering modes](#setting-symbol-rendering-modes)
  - [Rendering images from views](#rendering-images-from-views)
  - [Creating buttons](#creating-buttons)
  - [Creating special-purpose buttons](#creating-special-purpose-buttons)
  - [Linking to other content](#linking-to-other-content)
  - [Getting numeric inputs](#getting-numeric-inputs)
  - [Choosing from a set of options](#choosing-from-a-set-of-options)
  - [Choosing dates](#choosing-dates)
  - [Choosing a color](#choosing-a-color)
  - [Indicating a value](#indicating-a-value)
  - [Indicating missing content](#indicating-missing-content)
  - [Providing haptic feedback](#providing-haptic-feedback)
  - [Sizing controls](#sizing-controls)
  - [Building a menu bar](#building-a-menu-bar)
  - [Creating a menu](#creating-a-menu)
  - [Creating context menus](#creating-context-menus)
  - [Defining commands](#defining-commands)
  - [Getting built-in command groups](#getting-built-in-command-groups)
  - [Showing a menu indicator](#showing-a-menu-indicator)
  - [Configuring menu dismissal](#configuring-menu-dismissal)
  - [Setting a preferred order](#setting-a-preferred-order)
  - [Deprecated types](#deprecated-types)
  - [Creating rectangular shapes](#creating-rectangular-shapes)
  - [Creating circular shapes](#creating-circular-shapes)
  - [Drawing custom shapes](#drawing-custom-shapes)
  - [Defining shape behavior](#defining-shape-behavior)
  - [Transforming a shape](#transforming-a-shape)
  - [Setting a container shape](#setting-a-container-shape)
  - [Immediate mode drawing](#immediate-mode-drawing)
  - [Setting a color](#setting-a-color)
  - [Styling content](#styling-content)
  - [Transforming colors](#transforming-colors)
  - [Scaling, rotating, or transforming a view](#scaling-rotating-or-transforming-a-view)
  - [Masking and clipping](#masking-and-clipping)
  - [Applying blur and shadows](#applying-blur-and-shadows)
  - [Applying effects based on geometry](#applying-effects-based-on-geometry)
  - [Compositing views](#compositing-views)
  - [Measuring a view](#measuring-a-view)
  - [Responding to a geometry change](#responding-to-a-geometry-change)
  - [Accessing Metal shaders](#accessing-metal-shaders)
  - [Accessing geometric constructs](#accessing-geometric-constructs)

---

- [case xSmall](/documentation/swiftui/dynamictypesize/xsmall)
- [case small](/documentation/swiftui/dynamictypesize/small)
- [case medium](/documentation/swiftui/dynamictypesize/medium)
- [case large](/documentation/swiftui/dynamictypesize/large)
- [case xLarge](/documentation/swiftui/dynamictypesize/xlarge)
- [case xxLarge](/documentation/swiftui/dynamictypesize/xxlarge)
- [case xxxLarge](/documentation/swiftui/dynamictypesize/xxxlarge)

#### Getting accessibility type sizes

- [case accessibility1](/documentation/swiftui/dynamictypesize/accessibility1)
- [case accessibility2](/documentation/swiftui/dynamictypesize/accessibility2)
- [case accessibility3](/documentation/swiftui/dynamictypesize/accessibility3)
- [case accessibility4](/documentation/swiftui/dynamictypesize/accessibility4)
- [case accessibility5](/documentation/swiftui/dynamictypesize/accessibility5)
- [var isAccessibilitySize: Bool](/documentation/swiftui/dynamictypesize/isaccessibilitysize)

#### Creating a type size

- [init?(UIContentSizeCategory)](/documentation/swiftui/dynamictypesize/init(_:))
- [ScaledMetric](/documentation/swiftui/scaledmetric)

#### Creating the metric

- [init(wrappedValue: Value)](/documentation/swiftui/scaledmetric/init(wrappedvalue:))
- [init(wrappedValue: Value, relativeTo: Font.TextStyle)](/documentation/swiftui/scaledmetric/init(wrappedvalue:relativeto:))

#### Getting the metric

- [var wrappedValue: Value](/documentation/swiftui/scaledmetric/wrappedvalue)
- [TextVariantPreference](/documentation/swiftui/textvariantpreference)

#### Type Properties

- [static var fixed: FixedTextVariant](/documentation/swiftui/textvariantpreference/fixed)
- [static var sizeDependent: SizeDependentTextVariant](/documentation/swiftui/textvariantpreference/sizedependent)
- [FixedTextVariant](/documentation/swiftui/fixedtextvariant)
- [SizeDependentTextVariant](/documentation/swiftui/sizedependenttextvariant)

### Controlling text style

- [func bold(Bool) -> some View](/documentation/swiftui/view/bold(_:))
- [func italic(Bool) -> some View](/documentation/swiftui/view/italic(_:))
- [func underline(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> some View](/documentation/swiftui/view/underline(_:pattern:color:))
- [func strikethrough(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> some View](/documentation/swiftui/view/strikethrough(_:pattern:color:))
- [func textCase(Text.Case?) -> some View](/documentation/swiftui/view/textcase(_:))
- [var textCase: Text.Case?](/documentation/swiftui/environmentvalues/textcase)
- [func monospaced(Bool) -> some View](/documentation/swiftui/view/monospaced(_:))
- [func monospacedDigit() -> some View](/documentation/swiftui/view/monospaceddigit())
- [AttributedTextFormattingDefinition](/documentation/swiftui/attributedtextformattingdefinition)

#### Associated Types

- [Body](/documentation/swiftui/attributedtextformattingdefinition/body-swift.associatedtype)
- [Scope](/documentation/swiftui/attributedtextformattingdefinition/scope)

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/attributedtextformattingdefinition/body-1b01t)

#### Instance Methods

- [func constrain(_:)](/documentation/swiftui/attributedtextformattingdefinition/constrain(_:))

#### Type Aliases

- [AttributedTextFormattingDefinition.ValueConstraint](/documentation/swiftui/attributedtextformattingdefinition/valueconstraint)
- [AttributedTextValueConstraint](/documentation/swiftui/attributedtextvalueconstraint)

#### Associated Types

- [AttributeKey](/documentation/swiftui/attributedtextvalueconstraint/attributekey)

#### Instance Methods

- [func constrain(inout Self.Attributes)](/documentation/swiftui/attributedtextvalueconstraint/constrain(_:))

#### Type Aliases

- [AttributedTextValueConstraint.Attributes](/documentation/swiftui/attributedtextvalueconstraint/attributes)
- [AttributedTextFormatting](/documentation/swiftui/attributedtextformatting)

#### Structures

- [AttributedTextFormatting.AnyDefinition](/documentation/swiftui/attributedtextformatting/anydefinition)

##### Initializers

- [init<D>(D)](/documentation/swiftui/attributedtextformatting/anydefinition/init(_:))
- [AttributedTextFormatting.AttributeContainerProxy](/documentation/swiftui/attributedtextformatting/attributecontainerproxy)

##### Structures

- [AttributedTextFormatting.AttributeContainerProxy.Scoped](/documentation/swiftui/attributedtextformatting/attributecontainerproxy/scoped)

###### Subscripts

- [subscript(dynamicMember:)](/documentation/swiftui/attributedtextformatting/attributecontainerproxy/scoped/subscript(dynamicmember:))

##### Subscripts

- [subscript(_:)](/documentation/swiftui/attributedtextformatting/attributecontainerproxy/subscript(_:))
- [subscript(dynamicMember:)](/documentation/swiftui/attributedtextformatting/attributecontainerproxy/subscript(dynamicmember:))
- [AttributedTextFormatting.DefinitionBuilder](/documentation/swiftui/attributedtextformatting/definitionbuilder)

##### Type Methods

- [static func buildBlock<S>() -> AttributedTextFormatting.EmptyDefinition<S>](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildblock())
- [static func buildBlock<D>(D) -> D](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildblock(_:))
- [static func buildBlock<F, each D>(F, repeat each D) -> AttributedTextFormatting.TupleDefinition<F.Scope, F, repeat each D>](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildblock(_:_:))
- [static func buildEither<T, F>(first: T) -> _ConditionalContent<T, F>](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildeither(first:))
- [static func buildEither<T, F>(second: F) -> _ConditionalContent<T, F>](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildeither(second:))
- [static func buildExpression<D>(D) -> D](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildexpression(_:))
- [static func buildIf<D>(D?) -> D?](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildif(_:))
- [static func buildLimitedAvailability<D>(D) -> AttributedTextFormatting.AnyDefinition<Scope>](/documentation/swiftui/attributedtextformatting/definitionbuilder/buildlimitedavailability(_:))
- [AttributedTextFormatting.EmptyDefinition](/documentation/swiftui/attributedtextformatting/emptydefinition)

##### Initializers

- [init()](/documentation/swiftui/attributedtextformatting/emptydefinition/init())
- [AttributedTextFormatting.Transferable](/documentation/swiftui/attributedtextformatting/transferable)

##### Initializers

- [init(text: AttributedString, in: EnvironmentValues)](/documentation/swiftui/attributedtextformatting/transferable/init(text:in:))
- [AttributedTextFormatting.TupleDefinition](/documentation/swiftui/attributedtextformatting/tupledefinition)

##### Initializers

- [init(definition: repeat each Definition)](/documentation/swiftui/attributedtextformatting/tupledefinition/init(definition:))
- [AttributedTextFormatting.ValueConstraint](/documentation/swiftui/attributedtextformatting/valueconstraint)

##### Initializers

- [init(for:values:default:)](/documentation/swiftui/attributedtextformatting/valueconstraint/init(for:values:default:))

### Managing text layout

- [func truncationMode(Text.TruncationMode) -> some View](/documentation/swiftui/view/truncationmode(_:))
- [var truncationMode: Text.TruncationMode](/documentation/swiftui/environmentvalues/truncationmode)
- [func allowsTightening(Bool) -> some View](/documentation/swiftui/view/allowstightening(_:))
- [var allowsTightening: Bool](/documentation/swiftui/environmentvalues/allowstightening)
- [func minimumScaleFactor(CGFloat) -> some View](/documentation/swiftui/view/minimumscalefactor(_:))
- [var minimumScaleFactor: CGFloat](/documentation/swiftui/environmentvalues/minimumscalefactor)
- [func baselineOffset(CGFloat) -> some View](/documentation/swiftui/view/baselineoffset(_:))
- [func kerning(CGFloat) -> some View](/documentation/swiftui/view/kerning(_:))
- [func tracking(CGFloat) -> some View](/documentation/swiftui/view/tracking(_:))
- [func flipsForRightToLeftLayoutDirection(Bool) -> some View](/documentation/swiftui/view/flipsforrighttoleftlayoutdirection(_:))
- [TextAlignment](/documentation/swiftui/textalignment)

#### Getting text alignments

- [case center](/documentation/swiftui/textalignment/center)
- [case leading](/documentation/swiftui/textalignment/leading)
- [case trailing](/documentation/swiftui/textalignment/trailing)

### Rendering text

- [Creating visual effects with SwiftUI](/documentation/swiftui/creating-visual-effects-with-swiftui)
- [TextAttribute](/documentation/swiftui/textattribute)
- [func textRenderer<T>(T) -> some View](/documentation/swiftui/view/textrenderer(_:))
- [TextRenderer](/documentation/swiftui/textrenderer)

#### Instance Properties

- [var displayPadding: EdgeInsets](/documentation/swiftui/textrenderer/displaypadding)

#### Instance Methods

- [func draw(layout: Text.Layout, in: inout GraphicsContext)](/documentation/swiftui/textrenderer/draw(layout:in:))
- [func sizeThatFits(proposal: ProposedViewSize, text: TextProxy) -> CGSize](/documentation/swiftui/textrenderer/sizethatfits(proposal:text:))
- [TextProxy](/documentation/swiftui/textproxy)

#### Instance Methods

- [func sizeThatFits(ProposedViewSize) -> CGSize](/documentation/swiftui/textproxy/sizethatfits(_:))

### Limiting line count for multiline text

- [func lineLimit(_:)](/documentation/swiftui/view/linelimit(_:))
- [func lineLimit(Int, reservesSpace: Bool) -> some View](/documentation/swiftui/view/linelimit(_:reservesspace:))
- [var lineLimit: Int?](/documentation/swiftui/environmentvalues/linelimit)

### Formatting multiline text

- [func lineSpacing(CGFloat) -> some View](/documentation/swiftui/view/linespacing(_:))
- [var lineSpacing: CGFloat](/documentation/swiftui/environmentvalues/linespacing)
- [func multilineTextAlignment(TextAlignment) -> some View](/documentation/swiftui/view/multilinetextalignment(_:))
- [var multilineTextAlignment: TextAlignment](/documentation/swiftui/environmentvalues/multilinetextalignment)

### Formatting date and time

- [SystemFormatStyle](/documentation/swiftui/systemformatstyle)

#### Structures

- [SystemFormatStyle.DateOffset](/documentation/swiftui/systemformatstyle/dateoffset)

##### Initializers

- [init(to: Date, allowedFields: Set<Date.ComponentsFormatStyle.Field>, maxFieldCount: Int, sign: NumberFormatStyleConfiguration.SignDisplayStrategy)](/documentation/swiftui/systemformatstyle/dateoffset/init(to:allowedfields:maxfieldcount:sign:))

##### Instance Methods

- [func calendar(Calendar) -> SystemFormatStyle.DateOffset](/documentation/swiftui/systemformatstyle/dateoffset/calendar(_:))
- [SystemFormatStyle.DateReference](/documentation/swiftui/systemformatstyle/datereference)

##### Initializers

- [init(to: Date, allowedFields: Set<Date.RelativeFormatStyle.Field>, maxFieldCount: Int, thresholdField: Date.RelativeFormatStyle.Field)](/documentation/swiftui/systemformatstyle/datereference/init(to:allowedfields:maxfieldcount:thresholdfield:))

##### Instance Methods

- [func calendar(Calendar) -> SystemFormatStyle.DateReference](/documentation/swiftui/systemformatstyle/datereference/calendar(_:))
- [SystemFormatStyle.Stopwatch](/documentation/swiftui/systemformatstyle/stopwatch)

##### Initializers

- [init(startingAt: Date, showsHours: Bool, maxFieldCount: Int, maxPrecision: Duration)](/documentation/swiftui/systemformatstyle/stopwatch/init(startingat:showshours:maxfieldcount:maxprecision:))
- [SystemFormatStyle.Timer](/documentation/swiftui/systemformatstyle/timer)

##### Initializers

- [init(countingDownIn: Range<Date>, showsHours: Bool, maxFieldCount: Int, maxPrecision: Duration)](/documentation/swiftui/systemformatstyle/timer/init(countingdownin:showshours:maxfieldcount:maxprecision:))
- [init(countingUpIn: Range<Date>, showsHours: Bool, maxFieldCount: Int, maxPrecision: Duration)](/documentation/swiftui/systemformatstyle/timer/init(countingupin:showshours:maxfieldcount:maxprecision:))
- [TimeDataSource](/documentation/swiftui/timedatasource)

#### Type Properties

- [static var currentDate: TimeDataSource<Date>](/documentation/swiftui/timedatasource/currentdate)

#### Type Methods

- [static func dateRange(endingAt: Date) -> TimeDataSource<Range<Date>>](/documentation/swiftui/timedatasource/daterange(endingat:))
- [static func dateRange(startingAt: Date) -> TimeDataSource<Range<Date>>](/documentation/swiftui/timedatasource/daterange(startingat:))
- [static func durationOffset(to: Date) -> TimeDataSource<Duration>](/documentation/swiftui/timedatasource/durationoffset(to:))

### Managing text entry

- [func autocorrectionDisabled(Bool) -> some View](/documentation/swiftui/view/autocorrectiondisabled(_:))
- [var autocorrectionDisabled: Bool](/documentation/swiftui/environmentvalues/autocorrectiondisabled)
- [func keyboardType(UIKeyboardType) -> some View](/documentation/swiftui/view/keyboardtype(_:))
- [func scrollDismissesKeyboard(ScrollDismissesKeyboardMode) -> some View](/documentation/swiftui/view/scrolldismisseskeyboard(_:))
- [func textContentType(_:)](/documentation/swiftui/view/textcontenttype(_:))
- [func textInputAutocapitalization(TextInputAutocapitalization?) -> some View](/documentation/swiftui/view/textinputautocapitalization(_:))
- [TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization)

#### Getting autocapitalization options

- [static var characters: TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization/characters)
- [static var sentences: TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization/sentences)
- [static var words: TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization/words)
- [static var never: TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization/never)

#### Creating an autocapitalization type

- [init?(UITextAutocapitalizationType)](/documentation/swiftui/textinputautocapitalization/init(_:))
- [func textInputCompletion(String) -> some View](/documentation/swiftui/view/textinputcompletion(_:))
- [func textInputSuggestions<S>(() -> S) -> some View](/documentation/swiftui/view/textinputsuggestions(_:))
- [func textInputSuggestions<Data, Content>(Data, content: (Data.Element) -> Content) -> some View](/documentation/swiftui/view/textinputsuggestions(_:content:))
- [func textInputSuggestions<Data, ID, Content>(Data, id: KeyPath<Data.Element, ID>, content: (Data.Element) -> Content) -> some View](/documentation/swiftui/view/textinputsuggestions(_:id:content:))
- [func textContentType(WKTextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-4dqqb)
- [func textContentType(NSTextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-6fic1)
- [func textContentType(UITextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-ufdv)
- [TextInputFormattingControlPlacement](/documentation/swiftui/textinputformattingcontrolplacement)

#### Structures

- [TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set)

##### Type Properties

- [static let accessoryBar: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/accessorybar)
- [static let all: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/all)
- [static let contextMenu: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/contextmenu)
- [static let `default`: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/default)
- [static let fontPanel: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/fontpanel)
- [static let inputAssistant: TextInputFormattingControlPlacement.Set](/documentation/swiftui/textinputformattingcontrolplacement/set/inputassistant)

### Dictating text

- [func searchDictationBehavior(TextInputDictationBehavior) -> some View](/documentation/swiftui/view/searchdictationbehavior(_:))
- [TextInputDictationActivation](/documentation/swiftui/textinputdictationactivation)

#### Getting activation values

- [static let onLook: TextInputDictationActivation](/documentation/swiftui/textinputdictationactivation/onlook)
- [static let onSelect: TextInputDictationActivation](/documentation/swiftui/textinputdictationactivation/onselect)
- [TextInputDictationBehavior](/documentation/swiftui/textinputdictationbehavior)

#### Getting behavior values

- [static let automatic: TextInputDictationBehavior](/documentation/swiftui/textinputdictationbehavior/automatic)
- [static func inline(activation: TextInputDictationActivation) -> TextInputDictationBehavior](/documentation/swiftui/textinputdictationbehavior/inline(activation:))
- [static let preventDictation: TextInputDictationBehavior](/documentation/swiftui/textinputdictationbehavior/preventdictation)

### Configuring the Writing Tools behavior

- [func writingToolsBehavior(WritingToolsBehavior) -> some View](/documentation/swiftui/view/writingtoolsbehavior(_:))
- [WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior)

#### Type Properties

- [static let automatic: WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior/automatic)
- [static let complete: WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior/complete)
- [static let disabled: WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior/disabled)
- [static let limited: WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior/limited)

### Specifying text equivalents

- [func typeSelectEquivalent(_:)](/documentation/swiftui/view/typeselectequivalent(_:))

### Localizing text

- [Preparing views for localization](/documentation/swiftui/preparing-views-for-localization)
- [LocalizedStringKey](/documentation/swiftui/localizedstringkey)

#### Creating a key from a literal value

- [init(String)](/documentation/swiftui/localizedstringkey/init(_:))
- [init(stringLiteral: String)](/documentation/swiftui/localizedstringkey/init(stringliteral:))

#### Creating a key from an interpolation

- [init(stringInterpolation: LocalizedStringKey.StringInterpolation)](/documentation/swiftui/localizedstringkey/init(stringinterpolation:))
- [LocalizedStringKey.StringInterpolation](/documentation/swiftui/localizedstringkey/stringinterpolation)

##### Appending to an interpolation

- [func appendInterpolation(_:)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(_:))
- [func appendInterpolation<T>(T, specifier: String)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(_:specifier:))
- [func appendInterpolation(_:format:)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(_:format:))
- [func appendInterpolation(_:formatter:)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(_:formatter:))
- [func appendInterpolation(Date, style: Text.DateStyle)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(_:style:))
- [func appendInterpolation(timerInterval: ClosedRange<Date>, pauseTime: Date?, countsDown: Bool, showsHours: Bool)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(timerinterval:pausetime:countsdown:showshours:))
- [func appendLiteral(String)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendliteral(_:))

##### Instance Methods

- [func appendInterpolation(accessibilityName: Color)](/documentation/swiftui/localizedstringkey/stringinterpolation/appendinterpolation(accessibilityname:))
- [var locale: Locale](/documentation/swiftui/environmentvalues/locale)
- [func typesettingLanguage(_:isEnabled:)](/documentation/swiftui/view/typesettinglanguage(_:isenabled:))
- [TypesettingLanguage](/documentation/swiftui/typesettinglanguage)

#### Getting language behavior

- [static let automatic: TypesettingLanguage](/documentation/swiftui/typesettinglanguage/automatic)
- [static func explicit(Locale.Language) -> TypesettingLanguage](/documentation/swiftui/typesettinglanguage/explicit(_:))

### Deprecated types

- [ContentSizeCategory](/documentation/swiftui/contentsizecategory)

#### Content size categories

- [case accessibilityExtraExtraExtraLarge](/documentation/swiftui/contentsizecategory/accessibilityextraextraextralarge)
- [case accessibilityExtraExtraLarge](/documentation/swiftui/contentsizecategory/accessibilityextraextralarge)
- [case accessibilityExtraLarge](/documentation/swiftui/contentsizecategory/accessibilityextralarge)
- [case accessibilityLarge](/documentation/swiftui/contentsizecategory/accessibilitylarge)
- [case accessibilityMedium](/documentation/swiftui/contentsizecategory/accessibilitymedium)
- [case extraExtraExtraLarge](/documentation/swiftui/contentsizecategory/extraextraextralarge)
- [case extraExtraLarge](/documentation/swiftui/contentsizecategory/extraextralarge)
- [case extraLarge](/documentation/swiftui/contentsizecategory/extralarge)
- [case extraSmall](/documentation/swiftui/contentsizecategory/extrasmall)
- [case large](/documentation/swiftui/contentsizecategory/large)
- [case medium](/documentation/swiftui/contentsizecategory/medium)
- [case small](/documentation/swiftui/contentsizecategory/small)

#### Creating a size category

- [init?(UIContentSizeCategory)](/documentation/swiftui/contentsizecategory/init(_:))

#### Comparing content size categories

- [var isAccessibilityCategory: Bool](/documentation/swiftui/contentsizecategory/isaccessibilitycategory)

#### Operators

- [static func < (ContentSizeCategory, ContentSizeCategory) -> Bool](/documentation/swiftui/contentsizecategory/_(_:_:)-1iyos)
- [static func > (ContentSizeCategory, ContentSizeCategory) -> Bool](/documentation/swiftui/contentsizecategory/_(_:_:)-61nui)
- [static func <= (ContentSizeCategory, ContentSizeCategory) -> Bool](/documentation/swiftui/contentsizecategory/_=(_:_:)-3lvd8)
- [static func >= (ContentSizeCategory, ContentSizeCategory) -> Bool](/documentation/swiftui/contentsizecategory/_=(_:_:)-3tkt4)
- [Images](/documentation/swiftui/images)

### Creating an image

- [Image](/documentation/swiftui/image)

#### Creating an image

- [init(String, bundle: Bundle?)](/documentation/swiftui/image/init(_:bundle:))
- [init(String, variableValue: Double?, bundle: Bundle?)](/documentation/swiftui/image/init(_:variablevalue:bundle:))
- [init(ImageResource)](/documentation/swiftui/image/init(_:))

#### Creating an image for use as a control

- [init(String, bundle: Bundle?, label: Text)](/documentation/swiftui/image/init(_:bundle:label:))
- [init(String, variableValue: Double?, bundle: Bundle?, label: Text)](/documentation/swiftui/image/init(_:variablevalue:bundle:label:))
- [init(CGImage, scale: CGFloat, orientation: Image.Orientation, label: Text)](/documentation/swiftui/image/init(_:scale:orientation:label:))

#### Creating an image for decorative use

- [init(decorative: String, bundle: Bundle?)](/documentation/swiftui/image/init(decorative:bundle:))
- [init(decorative: String, variableValue: Double?, bundle: Bundle?)](/documentation/swiftui/image/init(decorative:variablevalue:bundle:))
- [init(decorative: CGImage, scale: CGFloat, orientation: Image.Orientation)](/documentation/swiftui/image/init(decorative:scale:orientation:))

#### Creating a system symbol image

- [init(systemName: String)](/documentation/swiftui/image/init(systemname:))
- [init(systemName: String, variableValue: Double?)](/documentation/swiftui/image/init(systemname:variablevalue:))

#### Creating an image from another image

- [init(uiImage: UIImage)](/documentation/swiftui/image/init(uiimage:))
- [init(nsImage: NSImage)](/documentation/swiftui/image/init(nsimage:))

#### Creating an image from drawing instructions

- [init(size: CGSize, label: Text?, opaque: Bool, colorMode: ColorRenderingMode, renderer: (inout GraphicsContext) -> Void)](/documentation/swiftui/image/init(size:label:opaque:colormode:renderer:))

#### Resizing images

- [func resizable(capInsets: EdgeInsets, resizingMode: Image.ResizingMode) -> Image](/documentation/swiftui/image/resizable(capinsets:resizingmode:))

#### Specifying rendering behavior

- [func antialiased(Bool) -> Image](/documentation/swiftui/image/antialiased(_:))
- [func symbolRenderingMode(SymbolRenderingMode?) -> Image](/documentation/swiftui/image/symbolrenderingmode(_:))
- [func renderingMode(Image.TemplateRenderingMode?) -> Image](/documentation/swiftui/image/renderingmode(_:))
- [func interpolation(Image.Interpolation) -> Image](/documentation/swiftui/image/interpolation(_:))
- [Image.TemplateRenderingMode](/documentation/swiftui/image/templaterenderingmode)

##### Getting rendering modes

- [case original](/documentation/swiftui/image/templaterenderingmode/original)
- [case template](/documentation/swiftui/image/templaterenderingmode/template)
- [Image.Interpolation](/documentation/swiftui/image/interpolation)

##### Getting interpolation options

- [case high](/documentation/swiftui/image/interpolation/high)
- [case low](/documentation/swiftui/image/interpolation/low)
- [case medium](/documentation/swiftui/image/interpolation/medium)
- [case none](/documentation/swiftui/image/interpolation/none)

#### Specifying dynamic range

- [func allowedDynamicRange(Image.DynamicRange?) -> Image](/documentation/swiftui/image/alloweddynamicrange(_:))
- [var allowedDynamicRange: Image.DynamicRange?](/documentation/swiftui/environmentvalues/alloweddynamicrange)
- [Image.DynamicRange](/documentation/swiftui/image/dynamicrange)

##### Getting dynamic range values

- [static let standard: Image.DynamicRange](/documentation/swiftui/image/dynamicrange/standard)
- [static let high: Image.DynamicRange](/documentation/swiftui/image/dynamicrange/high)
- [static let constrainedHigh: Image.DynamicRange](/documentation/swiftui/image/dynamicrange/constrainedhigh)

#### Instance Methods

- [func symbolColorRenderingMode(SymbolColorRenderingMode?) -> Image](/documentation/swiftui/image/symbolcolorrenderingmode(_:))
- [func symbolVariableValueMode(SymbolVariableValueMode?) -> Image](/documentation/swiftui/image/symbolvariablevaluemode(_:))
- [func widgetAccentedRenderingMode(WidgetAccentedRenderingMode?) -> some View](/documentation/swiftui/image/widgetaccentedrenderingmode(_:))

#### Enumerations

- [Image.Orientation](/documentation/swiftui/image/orientation)

##### Getting image orientations

- [case up](/documentation/swiftui/image/orientation/up)
- [case down](/documentation/swiftui/image/orientation/down)
- [case left](/documentation/swiftui/image/orientation/left)
- [case right](/documentation/swiftui/image/orientation/right)

##### Getting mirrored image orientation

- [case upMirrored](/documentation/swiftui/image/orientation/upmirrored)
- [case downMirrored](/documentation/swiftui/image/orientation/downmirrored)
- [case leftMirrored](/documentation/swiftui/image/orientation/leftmirrored)
- [case rightMirrored](/documentation/swiftui/image/orientation/rightmirrored)
- [Image.ResizingMode](/documentation/swiftui/image/resizingmode)

##### Getting resizing modes

- [case stretch](/documentation/swiftui/image/resizingmode/stretch)
- [case tile](/documentation/swiftui/image/resizingmode/tile)
- [Image.Scale](/documentation/swiftui/image/scale)

##### Getting image scales

- [case small](/documentation/swiftui/image/scale/small)
- [case medium](/documentation/swiftui/image/scale/medium)
- [case large](/documentation/swiftui/image/scale/large)

### Configuring an image

- [Fitting images into available space](/documentation/swiftui/fitting-images-into-available-space)
- [func imageScale(Image.Scale) -> some View](/documentation/swiftui/view/imagescale(_:))
- [var imageScale: Image.Scale](/documentation/swiftui/environmentvalues/imagescale)
- [Image.Scale](/documentation/swiftui/image/scale)

#### Getting image scales

- [case small](/documentation/swiftui/image/scale/small)
- [case medium](/documentation/swiftui/image/scale/medium)
- [case large](/documentation/swiftui/image/scale/large)
- [Image.Orientation](/documentation/swiftui/image/orientation)

#### Getting image orientations

- [case up](/documentation/swiftui/image/orientation/up)
- [case down](/documentation/swiftui/image/orientation/down)
- [case left](/documentation/swiftui/image/orientation/left)
- [case right](/documentation/swiftui/image/orientation/right)

#### Getting mirrored image orientation

- [case upMirrored](/documentation/swiftui/image/orientation/upmirrored)
- [case downMirrored](/documentation/swiftui/image/orientation/downmirrored)
- [case leftMirrored](/documentation/swiftui/image/orientation/leftmirrored)
- [case rightMirrored](/documentation/swiftui/image/orientation/rightmirrored)
- [Image.ResizingMode](/documentation/swiftui/image/resizingmode)

#### Getting resizing modes

- [case stretch](/documentation/swiftui/image/resizingmode/stretch)
- [case tile](/documentation/swiftui/image/resizingmode/tile)

### Loading images asynchronously

- [AsyncImage](/documentation/swiftui/asyncimage)

#### Loading an image

- [init(url: URL?, scale: CGFloat)](/documentation/swiftui/asyncimage/init(url:scale:))
- [init<I, P>(url: URL?, scale: CGFloat, content: (Image) -> I, placeholder: () -> P)](/documentation/swiftui/asyncimage/init(url:scale:content:placeholder:))

#### Loading an image in phases

- [init(url: URL?, scale: CGFloat, transaction: Transaction, content: (AsyncImagePhase) -> Content)](/documentation/swiftui/asyncimage/init(url:scale:transaction:content:))
- [AsyncImagePhase](/documentation/swiftui/asyncimagephase)

#### Getting load phases

- [case empty](/documentation/swiftui/asyncimagephase/empty)
- [case success(Image)](/documentation/swiftui/asyncimagephase/success(_:))
- [case failure(any Error)](/documentation/swiftui/asyncimagephase/failure(_:))

#### Getting the image

- [var image: Image?](/documentation/swiftui/asyncimagephase/image)

#### Getting the error

- [var error: (any Error)?](/documentation/swiftui/asyncimagephase/error)

### Setting a symbol variant

- [func symbolVariant(SymbolVariants) -> some View](/documentation/swiftui/view/symbolvariant(_:))
- [var symbolVariants: SymbolVariants](/documentation/swiftui/environmentvalues/symbolvariants)
- [SymbolVariants](/documentation/swiftui/symbolvariants)

#### Getting symbol variants

- [static let none: SymbolVariants](/documentation/swiftui/symbolvariants/none)
- [static let circle: SymbolVariants](/documentation/swiftui/symbolvariants/circle-swift.type.property)
- [static let square: SymbolVariants](/documentation/swiftui/symbolvariants/square-swift.type.property)
- [static let rectangle: SymbolVariants](/documentation/swiftui/symbolvariants/rectangle-swift.type.property)
- [static let fill: SymbolVariants](/documentation/swiftui/symbolvariants/fill-swift.type.property)
- [static let slash: SymbolVariants](/documentation/swiftui/symbolvariants/slash-swift.type.property)

#### Modifying a variant

- [var circle: SymbolVariants](/documentation/swiftui/symbolvariants/circle-swift.property)
- [var square: SymbolVariants](/documentation/swiftui/symbolvariants/square-swift.property)
- [var rectangle: SymbolVariants](/documentation/swiftui/symbolvariants/rectangle-swift.property)
- [var fill: SymbolVariants](/documentation/swiftui/symbolvariants/fill-swift.property)
- [var slash: SymbolVariants](/documentation/swiftui/symbolvariants/slash-swift.property)

#### Comparing variants

- [func contains(SymbolVariants) -> Bool](/documentation/swiftui/symbolvariants/contains(_:))

### Managing symbol effects

- [func symbolEffect<T>(T, options: SymbolEffectOptions, isActive: Bool) -> some View](/documentation/swiftui/view/symboleffect(_:options:isactive:))
- [func symbolEffect<T, U>(T, options: SymbolEffectOptions, value: U) -> some View](/documentation/swiftui/view/symboleffect(_:options:value:))
- [func symbolEffectsRemoved(Bool) -> some View](/documentation/swiftui/view/symboleffectsremoved(_:))
- [SymbolEffectTransition](/documentation/swiftui/symboleffecttransition)

#### Creating a transition

- [init<T>(effect: T, options: SymbolEffectOptions)](/documentation/swiftui/symboleffecttransition/init(effect:options:))

### Setting symbol rendering modes

- [func symbolRenderingMode(SymbolRenderingMode?) -> some View](/documentation/swiftui/view/symbolrenderingmode(_:))
- [var symbolRenderingMode: SymbolRenderingMode?](/documentation/swiftui/environmentvalues/symbolrenderingmode)
- [SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode)

#### Getting symbol rendering modes

- [static let hierarchical: SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode/hierarchical)
- [static let monochrome: SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode/monochrome)
- [static let multicolor: SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode/multicolor)
- [static let palette: SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode/palette)
- [SymbolColorRenderingMode](/documentation/swiftui/symbolcolorrenderingmode)

#### Type Properties

- [static let flat: SymbolColorRenderingMode](/documentation/swiftui/symbolcolorrenderingmode/flat)
- [static let gradient: SymbolColorRenderingMode](/documentation/swiftui/symbolcolorrenderingmode/gradient)
- [SymbolVariableValueMode](/documentation/swiftui/symbolvariablevaluemode)

#### Type Properties

- [static let color: SymbolVariableValueMode](/documentation/swiftui/symbolvariablevaluemode/color)
- [static let draw: SymbolVariableValueMode](/documentation/swiftui/symbolvariablevaluemode/draw)

### Rendering images from views

- [ImageRenderer](/documentation/swiftui/imagerenderer)

#### Creating an image renderer

- [init(content: Content)](/documentation/swiftui/imagerenderer/init(content:))

#### Providing the source view

- [var content: Content](/documentation/swiftui/imagerenderer/content)

#### Accessing renderer properties

- [var proposedSize: ProposedViewSize](/documentation/swiftui/imagerenderer/proposedsize)
- [var scale: CGFloat](/documentation/swiftui/imagerenderer/scale)
- [var isOpaque: Bool](/documentation/swiftui/imagerenderer/isopaque)
- [var colorMode: ColorRenderingMode](/documentation/swiftui/imagerenderer/colormode)
- [var allowedDynamicRange: Image.DynamicRange?](/documentation/swiftui/imagerenderer/alloweddynamicrange)

#### Rendering images

- [func render(rasterizationScale: CGFloat, renderer: (CGSize, (CGContext) -> Void) -> Void)](/documentation/swiftui/imagerenderer/render(rasterizationscale:renderer:))
- [var cgImage: CGImage?](/documentation/swiftui/imagerenderer/cgimage)
- [var nsImage: NSImage?](/documentation/swiftui/imagerenderer/nsimage)
- [var uiImage: UIImage?](/documentation/swiftui/imagerenderer/uiimage)

#### Producing a stream of images

- [let objectWillChange: PassthroughSubject<Void, Never>](/documentation/swiftui/imagerenderer/objectwillchange)
- [var isObservationEnabled: Bool](/documentation/swiftui/imagerenderer/isobservationenabled)
- [Controls and indicators](/documentation/swiftui/controls-and-indicators)

### Creating buttons

- [Button](/documentation/swiftui/button)

#### Creating a button

- [init(action: () -> Void, label: () -> Label)](/documentation/swiftui/button/init(action:label:))
- [init(_:action:)](/documentation/swiftui/button/init(_:action:))
- [init(_:image:action:)](/documentation/swiftui/button/init(_:image:action:))
- [init(_:systemImage:action:)](/documentation/swiftui/button/init(_:systemimage:action:))

#### Creating a button with a role

- [init(role: ButtonRole?, action: () -> Void, label: () -> Label)](/documentation/swiftui/button/init(role:action:label:))
- [init(_:role:action:)](/documentation/swiftui/button/init(_:role:action:))
- [init(_:image:role:action:)](/documentation/swiftui/button/init(_:image:role:action:))
- [init(_:systemImage:role:action:)](/documentation/swiftui/button/init(_:systemimage:role:action:))

#### Creating a button from a configuration

- [init(PrimitiveButtonStyleConfiguration)](/documentation/swiftui/button/init(_:))

#### Creating a button to perform an App Intent

- [init(_:intent:)](/documentation/swiftui/button/init(_:intent:))
- [init<I>(intent: I, label: () -> Label)](/documentation/swiftui/button/init(intent:label:))
- [init(_:role:intent:)](/documentation/swiftui/button/init(_:role:intent:))
- [init(role: ButtonRole?, intent: some AppIntent, label: () -> Label)](/documentation/swiftui/button/init(role:intent:label:))
- [init(_:image:role:intent:)](/documentation/swiftui/button/init(_:image:role:intent:))
- [init(_:systemImage:role:intent:)](/documentation/swiftui/button/init(_:systemimage:role:intent:))

#### Initializers

- [init(role: ButtonRole, action: () -> Void)](/documentation/swiftui/button/init(role:action:))
- [func buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [func buttonBorderShape(ButtonBorderShape) -> some View](/documentation/swiftui/view/buttonbordershape(_:))
- [func buttonRepeatBehavior(ButtonRepeatBehavior) -> some View](/documentation/swiftui/view/buttonrepeatbehavior(_:))
- [var buttonRepeatBehavior: ButtonRepeatBehavior](/documentation/swiftui/environmentvalues/buttonrepeatbehavior)
- [ButtonBorderShape](/documentation/swiftui/buttonbordershape)

#### Getting border shapes

- [static let automatic: ButtonBorderShape](/documentation/swiftui/buttonbordershape/automatic)
- [static let capsule: ButtonBorderShape](/documentation/swiftui/buttonbordershape/capsule)
- [static let circle: ButtonBorderShape](/documentation/swiftui/buttonbordershape/circle)
- [static let roundedRectangle: ButtonBorderShape](/documentation/swiftui/buttonbordershape/roundedrectangle)
- [static func roundedRectangle(radius: CGFloat) -> ButtonBorderShape](/documentation/swiftui/buttonbordershape/roundedrectangle(radius:))
- [ButtonRole](/documentation/swiftui/buttonrole)

#### Getting button roles

- [static let cancel: ButtonRole](/documentation/swiftui/buttonrole/cancel)
- [static let destructive: ButtonRole](/documentation/swiftui/buttonrole/destructive)

#### Type Properties

- [static let close: ButtonRole](/documentation/swiftui/buttonrole/close)
- [static let confirm: ButtonRole](/documentation/swiftui/buttonrole/confirm)
- [ButtonRepeatBehavior](/documentation/swiftui/buttonrepeatbehavior)

#### Getting repeat behaviors

- [static let automatic: ButtonRepeatBehavior](/documentation/swiftui/buttonrepeatbehavior/automatic)
- [static let enabled: ButtonRepeatBehavior](/documentation/swiftui/buttonrepeatbehavior/enabled)
- [static let disabled: ButtonRepeatBehavior](/documentation/swiftui/buttonrepeatbehavior/disabled)
- [ButtonSizing](/documentation/swiftui/buttonsizing)

#### Type Properties

- [static var automatic: ButtonSizing](/documentation/swiftui/buttonsizing/automatic)
- [static var fitted: ButtonSizing](/documentation/swiftui/buttonsizing/fitted)
- [static var flexible: ButtonSizing](/documentation/swiftui/buttonsizing/flexible)

### Creating special-purpose buttons

- [EditButton](/documentation/swiftui/editbutton)

#### Creating an edit button

- [init()](/documentation/swiftui/editbutton/init())
- [PasteButton](/documentation/swiftui/pastebutton)

#### Creating a paste button

- [init(supportedContentTypes: [UTType], payloadAction: ([NSItemProvider]) -> Void)](/documentation/swiftui/pastebutton/init(supportedcontenttypes:payloadaction:))
- [init<T>(payloadType: T.Type, onPaste: ([T]) -> Void)](/documentation/swiftui/pastebutton/init(payloadtype:onpaste:))

#### Deprecated initializers

- [init(supportedTypes: [String], payloadAction: ([NSItemProvider]) -> Void)](/documentation/swiftui/pastebutton/init(supportedtypes:payloadaction:))
- [init<Payload>(supportedTypes: [String], validator: ([NSItemProvider]) -> Payload?, payloadAction: (Payload) -> Void)](/documentation/swiftui/pastebutton/init(supportedtypes:validator:payloadaction:))
- [init<Payload>(supportedContentTypes: [UTType], validator: ([NSItemProvider]) -> Payload?, payloadAction: (Payload) -> Void)](/documentation/swiftui/pastebutton/init(supportedcontenttypes:validator:payloadaction:))
- [RenameButton](/documentation/swiftui/renamebutton)

#### Creating an rename button

- [init()](/documentation/swiftui/renamebutton/init())

### Linking to other content

- [Link](/documentation/swiftui/link)

#### Creating a link

- [init(_:destination:)](/documentation/swiftui/link/init(_:destination:))
- [init(destination: URL, label: () -> Label)](/documentation/swiftui/link/init(destination:label:))
- [ShareLink](/documentation/swiftui/sharelink)

#### Sharing an item

- [init(item:subject:message:)](/documentation/swiftui/sharelink/init(item:subject:message:))
- [init(_:item:subject:message:)](/documentation/swiftui/sharelink/init(_:item:subject:message:))
- [init(item:subject:message:label:)](/documentation/swiftui/sharelink/init(item:subject:message:label:))

#### Sharing an item with a preview

- [init<I>(item: I, subject: Text?, message: Text?, preview: SharePreview<PreviewImage, PreviewIcon>)](/documentation/swiftui/sharelink/init(item:subject:message:preview:))
- [init(_:item:subject:message:preview:)](/documentation/swiftui/sharelink/init(_:item:subject:message:preview:))
- [init<I>(item: I, subject: Text?, message: Text?, preview: SharePreview<PreviewImage, PreviewIcon>, label: () -> Label)](/documentation/swiftui/sharelink/init(item:subject:message:preview:label:))

#### Sharing items

- [init(items:subject:message:)](/documentation/swiftui/sharelink/init(items:subject:message:))
- [init(_:items:subject:message:)](/documentation/swiftui/sharelink/init(_:items:subject:message:))
- [init(items:subject:message:label:)](/documentation/swiftui/sharelink/init(items:subject:message:label:))

#### Sharing items with a preview

- [init(items: Data, subject: Text?, message: Text?, preview: (Data.Element) -> SharePreview<PreviewImage, PreviewIcon>)](/documentation/swiftui/sharelink/init(items:subject:message:preview:))
- [init(_:items:subject:message:preview:)](/documentation/swiftui/sharelink/init(_:items:subject:message:preview:))
- [init(items: Data, subject: Text?, message: Text?, preview: (Data.Element) -> SharePreview<PreviewImage, PreviewIcon>, label: () -> Label)](/documentation/swiftui/sharelink/init(items:subject:message:preview:label:))

#### Supporting types

- [DefaultShareLinkLabel](/documentation/swiftui/defaultsharelinklabel)
- [SharePreview](/documentation/swiftui/sharepreview)

#### Creating a preview

- [init(_:)](/documentation/swiftui/sharepreview/init(_:))
- [init(_:image:)](/documentation/swiftui/sharepreview/init(_:image:))
- [init(_:icon:)](/documentation/swiftui/sharepreview/init(_:icon:))
- [init(_:image:icon:)](/documentation/swiftui/sharepreview/init(_:image:icon:))
- [TextFieldLink](/documentation/swiftui/textfieldlink)

#### Creating a text field link

- [init(_:prompt:onSubmit:)](/documentation/swiftui/textfieldlink/init(_:prompt:onsubmit:))
- [init(prompt: Text?, label: () -> Label, onSubmit: (String) -> Void)](/documentation/swiftui/textfieldlink/init(prompt:label:onsubmit:))
- [HelpLink](/documentation/swiftui/helplink)

#### Creating a help link

- [init(action: () -> Void)](/documentation/swiftui/helplink/init(action:))
- [init(destination: URL)](/documentation/swiftui/helplink/init(destination:))
- [init(anchor: NSHelpManager.AnchorName)](/documentation/swiftui/helplink/init(anchor:))
- [init(anchor: NSHelpManager.AnchorName, book: NSHelpManager.BookName)](/documentation/swiftui/helplink/init(anchor:book:))

### Getting numeric inputs

- [Slider](/documentation/swiftui/slider)

#### Creating a slider

- [init<V>(value: Binding<V>, in: ClosedRange<V>, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:step:oneditingchanged:))

#### Creating a slider with labels

- [init<V>(value: Binding<V>, in: ClosedRange<V>, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:label:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:step:label:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, label: () -> Label, minimumValueLabel: () -> ValueLabel, maximumValueLabel: () -> ValueLabel, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:label:minimumvaluelabel:maximumvaluelabel:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, label: () -> Label, minimumValueLabel: () -> ValueLabel, maximumValueLabel: () -> ValueLabel, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:step:label:minimumvaluelabel:maximumvaluelabel:oneditingchanged:))

#### Adding ticks to a slider

- [SliderTick](/documentation/swiftui/slidertick)

##### Structures

- [SliderTick.ID](/documentation/swiftui/slidertick/id-swift.struct)

##### Initializers

- [init(V)](/documentation/swiftui/slidertick/init(_:))
- [init(_:_:)](/documentation/swiftui/slidertick/init(_:_:))
- [init(V, label: () -> some View)](/documentation/swiftui/slidertick/init(_:label:))

##### Instance Properties

- [var id: SliderTick<V>.ID](/documentation/swiftui/slidertick/id-swift.property)
- [SliderTickBuilder](/documentation/swiftui/slidertickbuilder)

##### Type Methods

- [static func buildBlock() -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock())
- [static func buildBlock(some SliderTickContent<V>) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:))
- [static func buildBlock<C0, C1>(C0, C1) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:))
- [static func buildBlock<C0, C1, C2>(C0, C1, C2) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:))
- [static func buildBlock<C0, C1, C2, C3>(C0, C1, C2, C3) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4>(C0, C1, C2, C3, C4) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5>(C0, C1, C2, C3, C4, C5) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6>(C0, C1, C2, C3, C4, C5, C6) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7>(C0, C1, C2, C3, C4, C5, C6, C7) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8>(C0, C1, C2, C3, C4, C5, C6, C7, C8) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8, C9>(C0, C1, C2, C3, C4, C5, C6, C7, C8, C9) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))
- [static func buildEither<T, F>(first: T) -> _ConditionalContent<T, F>](/documentation/swiftui/slidertickbuilder/buildeither(first:))
- [static func buildEither<T, F>(second: F) -> _ConditionalContent<T, F>](/documentation/swiftui/slidertickbuilder/buildeither(second:))
- [static func buildExpression(some SliderTickContent<V>) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildexpression(_:))
- [static func buildIf(some SliderTickContent<V>) -> some SliderTickContent<V>
](/documentation/swiftui/slidertickbuilder/buildif(_:))
- [SliderTickContentForEach](/documentation/swiftui/slidertickcontentforeach)

##### Initializers

- [init(_:content:)](/documentation/swiftui/slidertickcontentforeach/init(_:content:))
- [init<V>(Data, id: KeyPath<Data.Element, ID>, content: (Data.Element) -> Content)](/documentation/swiftui/slidertickcontentforeach/init(_:id:content:))
- [TupleSliderTickContent](/documentation/swiftui/tupleslidertickcontent)

##### Instance Properties

- [var value: T](/documentation/swiftui/tupleslidertickcontent/value)

##### Type Aliases

- [TupleSliderTickContent.TicksCollection](/documentation/swiftui/tupleslidertickcontent/tickscollection)
- [SliderTickContent](/documentation/swiftui/slidertickcontent)

##### Associated Types

- [Body](/documentation/swiftui/slidertickcontent/body-swift.associatedtype)
- [Value](/documentation/swiftui/slidertickcontent/value)

##### Instance Properties

- [var body: Self.Body](/documentation/swiftui/slidertickcontent/body-swift.property)

#### Deprecated initializers

- [init<V>(value: Binding<V>, in: ClosedRange<V>, onEditingChanged: (Bool) -> Void, label: () -> Label)](/documentation/swiftui/slider/init(value:in:oneditingchanged:label:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, onEditingChanged: (Bool) -> Void, label: () -> Label)](/documentation/swiftui/slider/init(value:in:step:oneditingchanged:label:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, onEditingChanged: (Bool) -> Void, minimumValueLabel: ValueLabel, maximumValueLabel: ValueLabel, label: () -> Label)](/documentation/swiftui/slider/init(value:in:oneditingchanged:minimumvaluelabel:maximumvaluelabel:label:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, onEditingChanged: (Bool) -> Void, minimumValueLabel: ValueLabel, maximumValueLabel: ValueLabel, label: () -> Label)](/documentation/swiftui/slider/init(value:in:step:oneditingchanged:minimumvaluelabel:maximumvaluelabel:label:))

#### Initializers

- [init<V>(value: Binding<V>, in: ClosedRange<V>, neutralValue: V?, enabledBounds: ClosedRange<V>?, label: () -> Label, currentValueLabel: () -> some View, minimumValueLabel: () -> ValueLabel, maximumValueLabel: () -> ValueLabel, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:neutralvalue:enabledbounds:label:currentvaluelabel:minimumvaluelabel:maximumvaluelabel:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, neutralValue: V?, enabledBounds: ClosedRange<V>?, label: () -> Label, currentValueLabel: () -> some View, minimumValueLabel: () -> ValueLabel, maximumValueLabel: () -> ValueLabel, ticks: () -> some SliderTickContent, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:neutralvalue:enabledbounds:label:currentvaluelabel:minimumvaluelabel:maximumvaluelabel:ticks:oneditingchanged:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, neutralValue: V?, enabledBounds: ClosedRange<V>?, label: () -> Label, currentValueLabel: () -> some View, minimumValueLabel: () -> ValueLabel, maximumValueLabel: () -> ValueLabel, tick: (V) -> SliderTick<V>?, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/slider/init(value:in:step:neutralvalue:enabledbounds:label:currentvaluelabel:minimumvaluelabel:maximumvaluelabel:tick:oneditingchanged:))
- [Stepper](/documentation/swiftui/stepper)

#### Creating a stepper

- [init<V>(value: Binding<V>, step: V.Stride, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/stepper/init(value:step:label:oneditingchanged:))
- [init<F>(value: Binding<F.FormatInput>, step: F.FormatInput.Stride, format: F, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/stepper/init(value:step:format:label:oneditingchanged:))
- [init(_:value:step:onEditingChanged:)](/documentation/swiftui/stepper/init(_:value:step:oneditingchanged:))
- [init(_:value:step:format:onEditingChanged:)](/documentation/swiftui/stepper/init(_:value:step:format:oneditingchanged:))

#### Creating a stepper over a range

- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/stepper/init(value:in:step:label:oneditingchanged:))
- [init<F>(value: Binding<F.FormatInput>, in: ClosedRange<F.FormatInput>, step: F.FormatInput.Stride, format: F, label: () -> Label, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/stepper/init(value:in:step:format:label:oneditingchanged:))
- [init(_:value:in:step:onEditingChanged:)](/documentation/swiftui/stepper/init(_:value:in:step:oneditingchanged:))
- [init(_:value:in:step:format:onEditingChanged:)](/documentation/swiftui/stepper/init(_:value:in:step:format:oneditingchanged:))

#### Creating a stepper with change behavior

- [init(label: () -> Label, onIncrement: (() -> Void)?, onDecrement: (() -> Void)?, onEditingChanged: (Bool) -> Void)](/documentation/swiftui/stepper/init(label:onincrement:ondecrement:oneditingchanged:))
- [init(_:onIncrement:onDecrement:onEditingChanged:)](/documentation/swiftui/stepper/init(_:onincrement:ondecrement:oneditingchanged:))

#### Deprecated initializers

- [init<V>(value: Binding<V>, step: V.Stride, onEditingChanged: (Bool) -> Void, label: () -> Label)](/documentation/swiftui/stepper/init(value:step:oneditingchanged:label:))
- [init<V>(value: Binding<V>, in: ClosedRange<V>, step: V.Stride, onEditingChanged: (Bool) -> Void, label: () -> Label)](/documentation/swiftui/stepper/init(value:in:step:oneditingchanged:label:))
- [init(onIncrement: (() -> Void)?, onDecrement: (() -> Void)?, onEditingChanged: (Bool) -> Void, label: () -> Label)](/documentation/swiftui/stepper/init(onincrement:ondecrement:oneditingchanged:label:))
- [Toggle](/documentation/swiftui/toggle)

#### Creating a toggle

- [init(_:isOn:)](/documentation/swiftui/toggle/init(_:ison:))
- [init(isOn: Binding<Bool>, label: () -> Label)](/documentation/swiftui/toggle/init(ison:label:))
- [init(_:image:isOn:)](/documentation/swiftui/toggle/init(_:image:ison:))
- [init(_:systemImage:isOn:)](/documentation/swiftui/toggle/init(_:systemimage:ison:))

#### Creating a toggle for a collection

- [init(_:sources:isOn:)](/documentation/swiftui/toggle/init(_:sources:ison:))
- [init<C>(sources: C, isOn: KeyPath<C.Element, Binding<Bool>>, label: () -> Label)](/documentation/swiftui/toggle/init(sources:ison:label:))
- [init(_:image:sources:isOn:)](/documentation/swiftui/toggle/init(_:image:sources:ison:))
- [init(_:systemImage:sources:isOn:)](/documentation/swiftui/toggle/init(_:systemimage:sources:ison:))

#### Creating a toggle from a configuration

- [init(ToggleStyleConfiguration)](/documentation/swiftui/toggle/init(_:))

#### Creating a toggle for an App Intent

- [init<I>(isOn: Bool, intent: I, label: () -> Label)](/documentation/swiftui/toggle/init(ison:intent:label:))
- [init(_:isOn:intent:)](/documentation/swiftui/toggle/init(_:ison:intent:))
- [func toggleStyle<S>(S) -> some View](/documentation/swiftui/view/togglestyle(_:))

### Choosing from a set of options

- [Picker](/documentation/swiftui/picker)

#### Creating a picker

- [init(_:selection:content:)](/documentation/swiftui/picker/init(_:selection:content:))
- [init(selection: Binding<SelectionValue>, content: () -> Content, label: () -> Label)](/documentation/swiftui/picker/init(selection:content:label:))

#### Creating a picker for a collection

- [init(_:sources:selection:content:)](/documentation/swiftui/picker/init(_:sources:selection:content:))
- [init<C>(sources: C, selection: KeyPath<C.Element, Binding<SelectionValue>>, content: () -> Content, label: () -> Label)](/documentation/swiftui/picker/init(sources:selection:content:label:))

#### Creating a picker with an image label

- [init(_:image:selection:content:)](/documentation/swiftui/picker/init(_:image:selection:content:))
- [init(_:image:sources:selection:content:)](/documentation/swiftui/picker/init(_:image:sources:selection:content:))
- [init(_:systemImage:selection:content:)](/documentation/swiftui/picker/init(_:systemimage:selection:content:))
- [init(_:systemImage:sources:selection:content:)](/documentation/swiftui/picker/init(_:systemimage:sources:selection:content:))

#### Deprecated initializers

- [init(selection: Binding<SelectionValue>, label: Label, content: () -> Content)](/documentation/swiftui/picker/init(selection:label:content:))

#### Initializers

- [init(_:image:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:image:selection:content:currentvaluelabel:))
- [init(_:image:sources:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:image:sources:selection:content:currentvaluelabel:))
- [init(_:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:selection:content:currentvaluelabel:))
- [init(_:sources:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:sources:selection:content:currentvaluelabel:))
- [init(_:systemImage:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:systemimage:selection:content:currentvaluelabel:))
- [init(_:systemImage:sources:selection:content:currentValueLabel:)](/documentation/swiftui/picker/init(_:systemimage:sources:selection:content:currentvaluelabel:))
- [init(selection: Binding<SelectionValue>, content: () -> Content, label: () -> Label, currentValueLabel: () -> some View)](/documentation/swiftui/picker/init(selection:content:label:currentvaluelabel:))
- [init<C>(sources: C, selection: KeyPath<C.Element, Binding<SelectionValue>>, content: () -> Content, label: () -> Label, currentValueLabel: () -> some View)](/documentation/swiftui/picker/init(sources:selection:content:label:currentvaluelabel:))
- [func pickerStyle<S>(S) -> some View](/documentation/swiftui/view/pickerstyle(_:))
- [func horizontalRadioGroupLayout() -> some View](/documentation/swiftui/view/horizontalradiogrouplayout())
- [func defaultWheelPickerItemHeight(CGFloat) -> some View](/documentation/swiftui/view/defaultwheelpickeritemheight(_:))
- [var defaultWheelPickerItemHeight: CGFloat](/documentation/swiftui/environmentvalues/defaultwheelpickeritemheight)
- [func paletteSelectionEffect(PaletteSelectionEffect) -> some View](/documentation/swiftui/view/paletteselectioneffect(_:))
- [PaletteSelectionEffect](/documentation/swiftui/paletteselectioneffect)

#### Getting palette selection effects

- [static let automatic: PaletteSelectionEffect](/documentation/swiftui/paletteselectioneffect/automatic)
- [static let custom: PaletteSelectionEffect](/documentation/swiftui/paletteselectioneffect/custom)
- [static func symbolVariant(SymbolVariants) -> PaletteSelectionEffect](/documentation/swiftui/paletteselectioneffect/symbolvariant(_:))

### Choosing dates

- [DatePicker](/documentation/swiftui/datepicker)

#### Creating a date picker for any date

- [init(_:selection:displayedComponents:)](/documentation/swiftui/datepicker/init(_:selection:displayedcomponents:))
- [init(selection: Binding<Date>, displayedComponents: DatePicker<Label>.Components, label: () -> Label)](/documentation/swiftui/datepicker/init(selection:displayedcomponents:label:))

#### Creating a date picker for specific dates

- [init(_:selection:in:displayedComponents:)](/documentation/swiftui/datepicker/init(_:selection:in:displayedcomponents:))
- [init(selection:in:displayedComponents:label:)](/documentation/swiftui/datepicker/init(selection:in:displayedcomponents:label:))

#### Setting date picker components

- [DatePicker.Components](/documentation/swiftui/datepicker/components)
- [DatePickerComponents](/documentation/swiftui/datepickercomponents)

##### Getting date picker components

- [static let date: DatePickerComponents](/documentation/swiftui/datepickercomponents/date)
- [static let hourAndMinute: DatePickerComponents](/documentation/swiftui/datepickercomponents/hourandminute)
- [static let hourMinuteAndSecond: DatePickerComponents](/documentation/swiftui/datepickercomponents/hourminuteandsecond)
- [func datePickerStyle<S>(S) -> some View](/documentation/swiftui/view/datepickerstyle(_:))
- [MultiDatePicker](/documentation/swiftui/multidatepicker)

#### Picking dates

- [init(_:selection:)](/documentation/swiftui/multidatepicker/init(_:selection:))
- [init(selection: Binding<Set<DateComponents>>, label: () -> Label)](/documentation/swiftui/multidatepicker/init(selection:label:))

#### Picking dates in a range

- [init(_:selection:in:)](/documentation/swiftui/multidatepicker/init(_:selection:in:))
- [init(selection:in:label:)](/documentation/swiftui/multidatepicker/init(selection:in:label:))
- [var calendar: Calendar](/documentation/swiftui/environmentvalues/calendar)
- [var timeZone: TimeZone](/documentation/swiftui/environmentvalues/timezone)

### Choosing a color

- [ColorPicker](/documentation/swiftui/colorpicker)

#### Creating a color picker

- [init(_:selection:supportsOpacity:)](/documentation/swiftui/colorpicker/init(_:selection:supportsopacity:))
- [init(selection:supportsOpacity:label:)](/documentation/swiftui/colorpicker/init(selection:supportsopacity:label:))

### Indicating a value

- [Gauge](/documentation/swiftui/gauge)

#### Creating a gauge

- [init<V>(value: V, in: ClosedRange<V>, label: () -> Label)](/documentation/swiftui/gauge/init(value:in:label:))
- [init<V>(value: V, in: ClosedRange<V>, label: () -> Label, currentValueLabel: () -> CurrentValueLabel)](/documentation/swiftui/gauge/init(value:in:label:currentvaluelabel:))
- [init<V>(value: V, in: ClosedRange<V>, label: () -> Label, currentValueLabel: () -> CurrentValueLabel, markedValueLabels: () -> MarkedValueLabels)](/documentation/swiftui/gauge/init(value:in:label:currentvaluelabel:markedvaluelabels:))
- [init<V>(value: V, in: ClosedRange<V>, label: () -> Label, currentValueLabel: () -> CurrentValueLabel, minimumValueLabel: () -> BoundsLabel, maximumValueLabel: () -> BoundsLabel)](/documentation/swiftui/gauge/init(value:in:label:currentvaluelabel:minimumvaluelabel:maximumvaluelabel:))
- [init<V>(value: V, in: ClosedRange<V>, label: () -> Label, currentValueLabel: () -> CurrentValueLabel, minimumValueLabel: () -> BoundsLabel, maximumValueLabel: () -> BoundsLabel, markedValueLabels: () -> MarkedValueLabels)](/documentation/swiftui/gauge/init(value:in:label:currentvaluelabel:minimumvaluelabel:maximumvaluelabel:markedvaluelabels:))
- [func gaugeStyle<S>(S) -> some View](/documentation/swiftui/view/gaugestyle(_:))
- [ProgressView](/documentation/swiftui/progressview)

#### Creating an indeterminate progress view

- [init()](/documentation/swiftui/progressview/init())
- [init(label: () -> Label)](/documentation/swiftui/progressview/init(label:))
- [init(LocalizedStringKey)](/documentation/swiftui/progressview/init(_:)-6k5se)
- [init<S>(S)](/documentation/swiftui/progressview/init(_:)-3q5nf)

#### Creating a determinate progress view

- [init(Progress)](/documentation/swiftui/progressview/init(_:)-l5vj)
- [init<V>(value: V?, total: V)](/documentation/swiftui/progressview/init(value:total:))
- [init(_:value:total:)](/documentation/swiftui/progressview/init(_:value:total:))
- [init<V>(value: V?, total: V, label: () -> Label)](/documentation/swiftui/progressview/init(value:total:label:))
- [init<V>(value: V?, total: V, label: () -> Label, currentValueLabel: () -> CurrentValueLabel)](/documentation/swiftui/progressview/init(value:total:label:currentvaluelabel:))

#### Create a progress view spanning a date range

- [init(timerInterval: ClosedRange<Date>, countsDown: Bool)](/documentation/swiftui/progressview/init(timerinterval:countsdown:))
- [init(timerInterval: ClosedRange<Date>, countsDown: Bool, label: () -> Label)](/documentation/swiftui/progressview/init(timerinterval:countsdown:label:))
- [init(timerInterval: ClosedRange<Date>, countsDown: Bool, label: () -> Label, currentValueLabel: () -> CurrentValueLabel)](/documentation/swiftui/progressview/init(timerinterval:countsdown:label:currentvaluelabel:))

#### Initializers

- [init(_:)](/documentation/swiftui/progressview/init(_:))
- [func progressViewStyle<S>(S) -> some View](/documentation/swiftui/view/progressviewstyle(_:))
- [DefaultDateProgressLabel](/documentation/swiftui/defaultdateprogresslabel)
- [DefaultButtonLabel](/documentation/swiftui/defaultbuttonlabel)

### Indicating missing content

- [ContentUnavailableView](/documentation/swiftui/contentunavailableview)

#### Getting built-in unavailable views

- [static var search: ContentUnavailableView<SearchUnavailableContent.Label, SearchUnavailableContent.Description, SearchUnavailableContent.Actions>](/documentation/swiftui/contentunavailableview/search)
- [static func search(text: String) -> ContentUnavailableView<Label, Description, Actions>](/documentation/swiftui/contentunavailableview/search(text:))

#### Creating an unavailable view

- [init(label: () -> Label, description: () -> Description, actions: () -> Actions)](/documentation/swiftui/contentunavailableview/init(label:description:actions:))
- [init(_:image:description:)](/documentation/swiftui/contentunavailableview/init(_:image:description:))
- [init(_:systemImage:description:)](/documentation/swiftui/contentunavailableview/init(_:systemimage:description:))

#### Supporting types

- [SearchUnavailableContent](/documentation/swiftui/searchunavailablecontent)

##### Getting content types

- [SearchUnavailableContent.Actions](/documentation/swiftui/searchunavailablecontent/actions)
- [SearchUnavailableContent.Description](/documentation/swiftui/searchunavailablecontent/description)
- [SearchUnavailableContent.Label](/documentation/swiftui/searchunavailablecontent/label)

### Providing haptic feedback

- [func sensoryFeedback<T>(SensoryFeedback, trigger: T) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:))
- [func sensoryFeedback(trigger:_:)](/documentation/swiftui/view/sensoryfeedback(trigger:_:))
- [func sensoryFeedback<T>(SensoryFeedback, trigger: T, condition: (T, T) -> Bool) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:condition:))
- [SensoryFeedback](/documentation/swiftui/sensoryfeedback)

#### Indicating start and stop

- [static let start: SensoryFeedback](/documentation/swiftui/sensoryfeedback/start)
- [static let stop: SensoryFeedback](/documentation/swiftui/sensoryfeedback/stop)

#### Indicating changes and selections

- [static let alignment: SensoryFeedback](/documentation/swiftui/sensoryfeedback/alignment)
- [static let decrease: SensoryFeedback](/documentation/swiftui/sensoryfeedback/decrease)
- [static let increase: SensoryFeedback](/documentation/swiftui/sensoryfeedback/increase)
- [static let levelChange: SensoryFeedback](/documentation/swiftui/sensoryfeedback/levelchange)
- [static let selection: SensoryFeedback](/documentation/swiftui/sensoryfeedback/selection)
- [static let pathComplete: SensoryFeedback](/documentation/swiftui/sensoryfeedback/pathcomplete)

#### Indicating the outcome of an operation

- [static let success: SensoryFeedback](/documentation/swiftui/sensoryfeedback/success)
- [static let warning: SensoryFeedback](/documentation/swiftui/sensoryfeedback/warning)
- [static let error: SensoryFeedback](/documentation/swiftui/sensoryfeedback/error)

#### Producing a physical impact

- [static let impact: SensoryFeedback](/documentation/swiftui/sensoryfeedback/impact)
- [static func impact(weight: SensoryFeedback.Weight, intensity: Double) -> SensoryFeedback](/documentation/swiftui/sensoryfeedback/impact(weight:intensity:))
- [static func impact(flexibility: SensoryFeedback.Flexibility, intensity: Double) -> SensoryFeedback](/documentation/swiftui/sensoryfeedback/impact(flexibility:intensity:))
- [SensoryFeedback.Flexibility](/documentation/swiftui/sensoryfeedback/flexibility)

##### Getting flexibility values

- [static let rigid: SensoryFeedback.Flexibility](/documentation/swiftui/sensoryfeedback/flexibility/rigid)
- [static let soft: SensoryFeedback.Flexibility](/documentation/swiftui/sensoryfeedback/flexibility/soft)
- [static let solid: SensoryFeedback.Flexibility](/documentation/swiftui/sensoryfeedback/flexibility/solid)
- [SensoryFeedback.Weight](/documentation/swiftui/sensoryfeedback/weight)

##### Getting flexibility values

- [static let light: SensoryFeedback.Weight](/documentation/swiftui/sensoryfeedback/weight/light)
- [static let medium: SensoryFeedback.Weight](/documentation/swiftui/sensoryfeedback/weight/medium)
- [static let heavy: SensoryFeedback.Weight](/documentation/swiftui/sensoryfeedback/weight/heavy)

#### Structures

- [SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback)

##### Type Properties

- [static let button: SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback/button)
- [static let buttonIconOnly: SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback/buttonicononly)
- [static let slider: SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback/slider)
- [static let tab: SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback/tab)
- [static let toggle: SensoryFeedback.PressFeedback](/documentation/swiftui/sensoryfeedback/pressfeedback/toggle)
- [SensoryFeedback.ReleaseFeedback](/documentation/swiftui/sensoryfeedback/releasefeedback)

##### Type Properties

- [static let slider: SensoryFeedback.ReleaseFeedback](/documentation/swiftui/sensoryfeedback/releasefeedback/slider)
- [SensoryFeedback.SelectionFeedback](/documentation/swiftui/sensoryfeedback/selectionfeedback)

##### Type Properties

- [static let maximum: SensoryFeedback.SelectionFeedback](/documentation/swiftui/sensoryfeedback/selectionfeedback/maximum)
- [static let minimum: SensoryFeedback.SelectionFeedback](/documentation/swiftui/sensoryfeedback/selectionfeedback/minimum)
- [static let off: SensoryFeedback.SelectionFeedback](/documentation/swiftui/sensoryfeedback/selectionfeedback/off)
- [static let on: SensoryFeedback.SelectionFeedback](/documentation/swiftui/sensoryfeedback/selectionfeedback/on)

#### Type Methods

- [static func press(SensoryFeedback.PressFeedback) -> SensoryFeedback](/documentation/swiftui/sensoryfeedback/press(_:))
- [static func release(SensoryFeedback.ReleaseFeedback) -> SensoryFeedback](/documentation/swiftui/sensoryfeedback/release(_:))
- [static func selection(SensoryFeedback.SelectionFeedback) -> SensoryFeedback](/documentation/swiftui/sensoryfeedback/selection(_:))

### Sizing controls

- [func controlSize(_:)](/documentation/swiftui/view/controlsize(_:))
- [var controlSize: ControlSize](/documentation/swiftui/environmentvalues/controlsize)
- [ControlSize](/documentation/swiftui/controlsize)

#### Getting control sizes

- [case mini](/documentation/swiftui/controlsize/mini)
- [case small](/documentation/swiftui/controlsize/small)
- [case regular](/documentation/swiftui/controlsize/regular)
- [case large](/documentation/swiftui/controlsize/large)
- [case extraLarge](/documentation/swiftui/controlsize/extralarge)

#### Initializers

- [init(NSControl.ControlSize)](/documentation/swiftui/controlsize/init(_:))
- [Menus and commands](/documentation/swiftui/menus-and-commands)

### Building a menu bar

- [Building and customizing the menu bar with SwiftUI](/documentation/swiftui/building-and-customizing-the-menu-bar-with-swiftui)

### Creating a menu

- [Populating SwiftUI menus with adaptive controls](/documentation/swiftui/populating-swiftui-menus-with-adaptive-controls)
- [Menu](/documentation/swiftui/menu)

#### Creating a menu from content

- [init(_:content:)](/documentation/swiftui/menu/init(_:content:))
- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/menu/init(content:label:))
- [init(_:image:content:)](/documentation/swiftui/menu/init(_:image:content:))
- [init(_:systemImage:content:)](/documentation/swiftui/menu/init(_:systemimage:content:))

#### Creating a menu with a primary action

- [init(_:content:primaryAction:)](/documentation/swiftui/menu/init(_:content:primaryaction:))
- [init(content: () -> Content, label: () -> Label, primaryAction: () -> Void)](/documentation/swiftui/menu/init(content:label:primaryaction:))
- [init(_:image:content:primaryAction:)](/documentation/swiftui/menu/init(_:image:content:primaryaction:))
- [init(_:systemImage:content:primaryAction:)](/documentation/swiftui/menu/init(_:systemimage:content:primaryaction:))

#### Creating a menu from a configuration

- [init(MenuStyleConfiguration)](/documentation/swiftui/menu/init(_:))
- [func menuStyle<S>(S) -> some View](/documentation/swiftui/view/menustyle(_:))

### Creating context menus

- [func contextMenu<MenuItems>(menuItems: () -> MenuItems) -> some View](/documentation/swiftui/view/contextmenu(menuitems:))
- [func contextMenu<M, P>(menuItems: () -> M, preview: () -> P) -> some View](/documentation/swiftui/view/contextmenu(menuitems:preview:))
- [func contextMenu<I, M>(forSelectionType: I.Type, menu: (Set<I>) -> M, primaryAction: ((Set<I>) -> Void)?) -> some View](/documentation/swiftui/view/contextmenu(forselectiontype:menu:primaryaction:))

### Defining commands

- [func commands<Content>(content: () -> Content) -> some Scene](/documentation/swiftui/scene/commands(content:))
- [func commandsRemoved() -> some Scene](/documentation/swiftui/scene/commandsremoved())
- [func commandsReplaced<Content>(content: () -> Content) -> some Scene](/documentation/swiftui/scene/commandsreplaced(content:))
- [Commands](/documentation/swiftui/commands)

#### Implementing commands

- [var body: Self.Body](/documentation/swiftui/commands/body-swift.property)
- [Body](/documentation/swiftui/commands/body-swift.associatedtype)
- [CommandMenu](/documentation/swiftui/commandmenu)

#### Creating a command menu

- [init(_:content:)](/documentation/swiftui/commandmenu/init(_:content:))
- [CommandGroup](/documentation/swiftui/commandgroup)

#### Creating a command group

- [init(after: CommandGroupPlacement, addition: () -> Content)](/documentation/swiftui/commandgroup/init(after:addition:))
- [init(before: CommandGroupPlacement, addition: () -> Content)](/documentation/swiftui/commandgroup/init(before:addition:))
- [init(replacing: CommandGroupPlacement, addition: () -> Content)](/documentation/swiftui/commandgroup/init(replacing:addition:))
- [CommandsBuilder](/documentation/swiftui/commandsbuilder)

#### Building content

- [static func buildBlock() -> EmptyCommands](/documentation/swiftui/commandsbuilder/buildblock())
- [static func buildBlock<C>(C) -> C](/documentation/swiftui/commandsbuilder/buildblock(_:))
- [static func buildBlock<C0, C1>(C0, C1) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:))
- [static func buildBlock<C0, C1, C2>(C0, C1, C2) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:))
- [static func buildBlock<C0, C1, C2, C3>(C0, C1, C2, C3) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4>(C0, C1, C2, C3, C4) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5>(C0, C1, C2, C3, C4, C5) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6>(C0, C1, C2, C3, C4, C5, C6) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7>(C0, C1, C2, C3, C4, C5, C6, C7) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8>(C0, C1, C2, C3, C4, C5, C6, C7, C8) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8, C9>(C0, C1, C2, C3, C4, C5, C6, C7, C8, C9) -> some Commands](/documentation/swiftui/commandsbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))

#### Building conditionally

- [static func buildEither<T, F>(first: T) -> _ConditionalContent<T, F>](/documentation/swiftui/commandsbuilder/buildeither(first:))
- [static func buildEither<T, F>(second: F) -> _ConditionalContent<T, F>](/documentation/swiftui/commandsbuilder/buildeither(second:))
- [static func buildIf<C>(C?) -> C?](/documentation/swiftui/commandsbuilder/buildif(_:))
- [static buildLimitedAvailability(_:)](/documentation/swiftui/commandsbuilder/buildlimitedavailability(_:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/commandsbuilder/buildexpression(_:))
- [CommandGroupPlacement](/documentation/swiftui/commandgroupplacement)

#### App interactions

- [static let appInfo: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/appinfo)
- [static let appSettings: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/appsettings)
- [static let appTermination: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/apptermination)
- [static let appVisibility: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/appvisibility)
- [static let systemServices: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/systemservices)

#### File manipulation

- [static let importExport: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/importexport)
- [static let newItem: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/newitem)
- [static let printItem: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/printitem)
- [static let saveItem: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/saveitem)

#### Content updates

- [static let pasteboard: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/pasteboard)
- [static let textEditing: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/textediting)
- [static let textFormatting: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/textformatting)
- [static let undoRedo: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/undoredo)

#### Bars

- [static let sidebar: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/sidebar)
- [static let toolbar: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/toolbar)

#### Windows

- [static let singleWindowList: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/singlewindowlist)
- [static let windowArrangement: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/windowarrangement)
- [static let windowList: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/windowlist)
- [static let windowSize: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/windowsize)

#### Help

- [static let help: CommandGroupPlacement](/documentation/swiftui/commandgroupplacement/help)

### Getting built-in command groups

- [SidebarCommands](/documentation/swiftui/sidebarcommands)

#### Creating the command group

- [init()](/documentation/swiftui/sidebarcommands/init())
- [TextEditingCommands](/documentation/swiftui/texteditingcommands)

#### Creating the command group

- [init()](/documentation/swiftui/texteditingcommands/init())
- [TextFormattingCommands](/documentation/swiftui/textformattingcommands)

#### Creating the command group

- [init()](/documentation/swiftui/textformattingcommands/init())
- [ToolbarCommands](/documentation/swiftui/toolbarcommands)

#### Creating the command group

- [init()](/documentation/swiftui/toolbarcommands/init())
- [ImportFromDevicesCommands](/documentation/swiftui/importfromdevicescommands)

#### Creating the command group

- [init()](/documentation/swiftui/importfromdevicescommands/init())
- [InspectorCommands](/documentation/swiftui/inspectorcommands)

#### Creating a command

- [init()](/documentation/swiftui/inspectorcommands/init())
- [EmptyCommands](/documentation/swiftui/emptycommands)

#### Creating the command group

- [init()](/documentation/swiftui/emptycommands/init())

### Showing a menu indicator

- [func menuIndicator(Visibility) -> some View](/documentation/swiftui/view/menuindicator(_:))
- [var menuIndicatorVisibility: Visibility](/documentation/swiftui/environmentvalues/menuindicatorvisibility)

### Configuring menu dismissal

- [func menuActionDismissBehavior(MenuActionDismissBehavior) -> some View](/documentation/swiftui/view/menuactiondismissbehavior(_:))
- [MenuActionDismissBehavior](/documentation/swiftui/menuactiondismissbehavior)

#### Getting dismiss behaviors

- [static let automatic: MenuActionDismissBehavior](/documentation/swiftui/menuactiondismissbehavior/automatic)
- [static let disabled: MenuActionDismissBehavior](/documentation/swiftui/menuactiondismissbehavior/disabled)
- [static let enabled: MenuActionDismissBehavior](/documentation/swiftui/menuactiondismissbehavior/enabled)

### Setting a preferred order

- [func menuOrder(MenuOrder) -> some View](/documentation/swiftui/view/menuorder(_:))
- [var menuOrder: MenuOrder](/documentation/swiftui/environmentvalues/menuorder)
- [MenuOrder](/documentation/swiftui/menuorder)

#### Getting menu orders

- [static let automatic: MenuOrder](/documentation/swiftui/menuorder/automatic)
- [static let fixed: MenuOrder](/documentation/swiftui/menuorder/fixed)
- [static let priority: MenuOrder](/documentation/swiftui/menuorder/priority)

### Deprecated types

- [MenuButton](/documentation/swiftui/menubutton)

#### Creating a menu button

- [init(_:content:)](/documentation/swiftui/menubutton/init(_:content:))
- [init(label: Label, content: () -> Content)](/documentation/swiftui/menubutton/init(label:content:))

#### Styling a menu button

- [func menuButtonStyle<S>(S) -> some View](/documentation/swiftui/view/menubuttonstyle(_:))
- [MenuButtonStyle](/documentation/swiftui/menubuttonstyle)

##### Supporting types

- [BorderlessButtonMenuButtonStyle](/documentation/swiftui/borderlessbuttonmenubuttonstyle)

###### Creating a borderless button menu button style

- [init()](/documentation/swiftui/borderlessbuttonmenubuttonstyle/init())
- [BorderlessPullDownMenuButtonStyle](/documentation/swiftui/borderlesspulldownmenubuttonstyle)

###### Creating a borderless pull down menu button style

- [init()](/documentation/swiftui/borderlesspulldownmenubuttonstyle/init())
- [DefaultMenuButtonStyle](/documentation/swiftui/defaultmenubuttonstyle)

###### Creating a default menu button style

- [init()](/documentation/swiftui/defaultmenubuttonstyle/init())
- [PullDownMenuButtonStyle](/documentation/swiftui/pulldownmenubuttonstyle)

###### Creating a pull down menu button style

- [init()](/documentation/swiftui/pulldownmenubuttonstyle/init())
- [PullDownButton](/documentation/swiftui/pulldownbutton)
- [ContextMenu](/documentation/swiftui/contextmenu)

#### Creating a context menu

- [init(menuItems: () -> MenuItems)](/documentation/swiftui/contextmenu/init(menuitems:))
- [Shapes](/documentation/swiftui/shapes)

### Creating rectangular shapes

- [Rectangle](/documentation/swiftui/rectangle)

#### Creating a rectangle

- [init()](/documentation/swiftui/rectangle/init())
- [RoundedRectangle](/documentation/swiftui/roundedrectangle)

#### Creating a rounded rectangle

- [init(cornerRadius: CGFloat, style: RoundedCornerStyle)](/documentation/swiftui/roundedrectangle/init(cornerradius:style:))
- [init(cornerSize: CGSize, style: RoundedCornerStyle)](/documentation/swiftui/roundedrectangle/init(cornersize:style:))

#### Getting the shape’s characteristics

- [var cornerSize: CGSize](/documentation/swiftui/roundedrectangle/cornersize)
- [var style: RoundedCornerStyle](/documentation/swiftui/roundedrectangle/style)

#### Supporting types

- [var animatableData: CGSize.AnimatableData](/documentation/swiftui/roundedrectangle/animatabledata)
- [RoundedCornerStyle](/documentation/swiftui/roundedcornerstyle)

#### Getting corner styles

- [case circular](/documentation/swiftui/roundedcornerstyle/circular)
- [case continuous](/documentation/swiftui/roundedcornerstyle/continuous)
- [RoundedRectangularShape](/documentation/swiftui/roundedrectangularshape)

#### Instance Methods

- [func corners(in: CGSize?) -> Self.Corners?](/documentation/swiftui/roundedrectangularshape/corners(in:))

#### Type Aliases

- [RoundedRectangularShape.Corners](/documentation/swiftui/roundedrectangularshape/corners)
- [RoundedRectangularShapeCorners](/documentation/swiftui/roundedrectangularshapecorners)

#### Initializers

- [init(all: Edge.Corner.Style)](/documentation/swiftui/roundedrectangularshapecorners/init(all:))
- [init(topLeading: Edge.Corner.Style, topTrailing: Edge.Corner.Style, bottomLeading: Edge.Corner.Style, bottomTrailing: Edge.Corner.Style)](/documentation/swiftui/roundedrectangularshapecorners/init(topleading:toptrailing:bottomleading:bottomtrailing:))

#### Instance Properties

- [var bottomLeading: Edge.Corner.Style](/documentation/swiftui/roundedrectangularshapecorners/bottomleading)
- [var bottomTrailing: Edge.Corner.Style](/documentation/swiftui/roundedrectangularshapecorners/bottomtrailing)
- [var topLeading: Edge.Corner.Style](/documentation/swiftui/roundedrectangularshapecorners/topleading)
- [var topTrailing: Edge.Corner.Style](/documentation/swiftui/roundedrectangularshapecorners/toptrailing)

#### Subscripts

- [subscript(Edge.Corner) -> Edge.Corner.Style](/documentation/swiftui/roundedrectangularshapecorners/subscript(_:))

#### Type Properties

- [static var concentric: RoundedRectangularShapeCorners](/documentation/swiftui/roundedrectangularshapecorners/concentric)

#### Type Methods

- [static func concentric(minimum: Edge.Corner.Style?) -> RoundedRectangularShapeCorners](/documentation/swiftui/roundedrectangularshapecorners/concentric(minimum:))
- [static func fixed(CGFloat) -> RoundedRectangularShapeCorners](/documentation/swiftui/roundedrectangularshapecorners/fixed(_:))
- [UnevenRoundedRectangle](/documentation/swiftui/unevenroundedrectangle)

#### Creating an uneven rounded rectangle

- [init(cornerRadii: RectangleCornerRadii, style: RoundedCornerStyle)](/documentation/swiftui/unevenroundedrectangle/init(cornerradii:style:))
- [init(topLeadingRadius: CGFloat, bottomLeadingRadius: CGFloat, bottomTrailingRadius: CGFloat, topTrailingRadius: CGFloat, style: RoundedCornerStyle)](/documentation/swiftui/unevenroundedrectangle/init(topleadingradius:bottomleadingradius:bottomtrailingradius:toptrailingradius:style:))

#### Getting the shape’s characteristics

- [var cornerRadii: RectangleCornerRadii](/documentation/swiftui/unevenroundedrectangle/cornerradii)
- [var style: RoundedCornerStyle](/documentation/swiftui/unevenroundedrectangle/style)

#### Supporting types

- [var animatableData: RectangleCornerRadii.AnimatableData](/documentation/swiftui/unevenroundedrectangle/animatabledata)
- [RectangleCornerRadii](/documentation/swiftui/rectanglecornerradii)

#### Creating a set of radii

- [init(topLeading: CGFloat, bottomLeading: CGFloat, bottomTrailing: CGFloat, topTrailing: CGFloat)](/documentation/swiftui/rectanglecornerradii/init(topleading:bottomleading:bottomtrailing:toptrailing:))

#### Getting values for specific corners

- [var topLeading: CGFloat](/documentation/swiftui/rectanglecornerradii/topleading)
- [var topTrailing: CGFloat](/documentation/swiftui/rectanglecornerradii/toptrailing)
- [var bottomLeading: CGFloat](/documentation/swiftui/rectanglecornerradii/bottomleading)
- [var bottomTrailing: CGFloat](/documentation/swiftui/rectanglecornerradii/bottomtrailing)

#### Subscripts

- [subscript(Edge.Corner) -> CGFloat](/documentation/swiftui/rectanglecornerradii/subscript(_:))
- [RectangleCornerInsets](/documentation/swiftui/rectanglecornerinsets)

#### Initializers

- [init()](/documentation/swiftui/rectanglecornerinsets/init())
- [init(topLeading: CGSize, topTrailing: CGSize, bottomLeading: CGSize, bottomTrailing: CGSize)](/documentation/swiftui/rectanglecornerinsets/init(topleading:toptrailing:bottomleading:bottomtrailing:))

#### Instance Properties

- [var bottomLeading: CGSize](/documentation/swiftui/rectanglecornerinsets/bottomleading)
- [var bottomTrailing: CGSize](/documentation/swiftui/rectanglecornerinsets/bottomtrailing)
- [var topLeading: CGSize](/documentation/swiftui/rectanglecornerinsets/topleading)
- [var topTrailing: CGSize](/documentation/swiftui/rectanglecornerinsets/toptrailing)
- [ConcentricRectangle](/documentation/swiftui/concentricrectangle)

#### Initializers

- [init()](/documentation/swiftui/concentricrectangle/init())
- [init(corners: Edge.Corner.Style, isUniform: Bool)](/documentation/swiftui/concentricrectangle/init(corners:isuniform:))
- [init(topLeadingCorner: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(topleadingcorner:toptrailingcorner:bottomleadingcorner:bottomtrailingcorner:))
- [init(uniformBottomCorners: Edge.Corner.Style, topLeadingCorner: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformbottomcorners:topleadingcorner:toptrailingcorner:))
- [init(uniformLeadingCorners: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformleadingcorners:toptrailingcorner:bottomtrailingcorner:))
- [init(uniformLeadingCorners: Edge.Corner.Style, uniformTrailingCorners: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformleadingcorners:uniformtrailingcorners:))
- [init(uniformTopCorners: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformtopcorners:bottomleadingcorner:bottomtrailingcorner:))
- [init(uniformTopCorners: Edge.Corner.Style, uniformBottomCorners: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformtopcorners:uniformbottomcorners:))
- [init(uniformTrailingCorners: Edge.Corner.Style, topLeadingCorner: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style)](/documentation/swiftui/concentricrectangle/init(uniformtrailingcorners:topleadingcorner:bottomleadingcorner:))

### Creating circular shapes

- [Circle](/documentation/swiftui/circle)

#### Creating a circle

- [init()](/documentation/swiftui/circle/init())
- [Ellipse](/documentation/swiftui/ellipse)

#### Creating an ellipse

- [init()](/documentation/swiftui/ellipse/init())
- [Capsule](/documentation/swiftui/capsule)

#### Creating a capsule

- [init(style: RoundedCornerStyle)](/documentation/swiftui/capsule/init(style:))

#### Getting the shape’s characteristics

- [var style: RoundedCornerStyle](/documentation/swiftui/capsule/style)

### Drawing custom shapes

- [Path](/documentation/swiftui/path)

#### Creating a path

- [init()](/documentation/swiftui/path/init())
- [init(_:)](/documentation/swiftui/path/init(_:))
- [init(ellipseIn: CGRect)](/documentation/swiftui/path/init(ellipsein:))
- [init(roundedRect: CGRect, cornerRadius: CGFloat, style: RoundedCornerStyle)](/documentation/swiftui/path/init(roundedrect:cornerradius:style:))
- [init(roundedRect: CGRect, cornerSize: CGSize, style: RoundedCornerStyle)](/documentation/swiftui/path/init(roundedrect:cornersize:style:))
- [init(roundedRect: CGRect, cornerRadii: RectangleCornerRadii, style: RoundedCornerStyle)](/documentation/swiftui/path/init(roundedrect:cornerradii:style:))

#### Getting the path’s characteristics

- [var boundingRect: CGRect](/documentation/swiftui/path/boundingrect)
- [var cgPath: CGPath](/documentation/swiftui/path/cgpath)
- [func contains(CGPoint, eoFill: Bool) -> Bool](/documentation/swiftui/path/contains(_:eofill:))
- [var currentPoint: CGPoint?](/documentation/swiftui/path/currentpoint)
- [var description: String](/documentation/swiftui/path/description)
- [var isEmpty: Bool](/documentation/swiftui/path/isempty)

#### Drawing a path

- [func move(to: CGPoint)](/documentation/swiftui/path/move(to:))
- [func addArc(center: CGPoint, radius: CGFloat, startAngle: Angle, endAngle: Angle, clockwise: Bool, transform: CGAffineTransform)](/documentation/swiftui/path/addarc(center:radius:startangle:endangle:clockwise:transform:))
- [func addArc(tangent1End: CGPoint, tangent2End: CGPoint, radius: CGFloat, transform: CGAffineTransform)](/documentation/swiftui/path/addarc(tangent1end:tangent2end:radius:transform:))
- [func addCurve(to: CGPoint, control1: CGPoint, control2: CGPoint)](/documentation/swiftui/path/addcurve(to:control1:control2:))
- [func addEllipse(in: CGRect, transform: CGAffineTransform)](/documentation/swiftui/path/addellipse(in:transform:))
- [func addLine(to: CGPoint)](/documentation/swiftui/path/addline(to:))
- [func addLines([CGPoint])](/documentation/swiftui/path/addlines(_:))
- [func addPath(Path, transform: CGAffineTransform)](/documentation/swiftui/path/addpath(_:transform:))
- [func addQuadCurve(to: CGPoint, control: CGPoint)](/documentation/swiftui/path/addquadcurve(to:control:))
- [func addRect(CGRect, transform: CGAffineTransform)](/documentation/swiftui/path/addrect(_:transform:))
- [func addRects([CGRect], transform: CGAffineTransform)](/documentation/swiftui/path/addrects(_:transform:))
- [func addRelativeArc(center: CGPoint, radius: CGFloat, startAngle: Angle, delta: Angle, transform: CGAffineTransform)](/documentation/swiftui/path/addrelativearc(center:radius:startangle:delta:transform:))
- [func addRoundedRect(in: CGRect, cornerSize: CGSize, style: RoundedCornerStyle, transform: CGAffineTransform)](/documentation/swiftui/path/addroundedrect(in:cornersize:style:transform:))
- [func closeSubpath()](/documentation/swiftui/path/closesubpath())

#### Transforming the path

- [func applying(CGAffineTransform) -> Path](/documentation/swiftui/path/applying(_:))
- [func offsetBy(dx: CGFloat, dy: CGFloat) -> Path](/documentation/swiftui/path/offsetby(dx:dy:))
- [func trimmedPath(from: CGFloat, to: CGFloat) -> Path](/documentation/swiftui/path/trimmedpath(from:to:))

#### Performing operations on the path

- [func addRoundedRect(in: CGRect, cornerSize: CGSize, style: RoundedCornerStyle, transform: CGAffineTransform)](/documentation/swiftui/path/addroundedrect(in:cornersize:style:transform:))
- [func intersection(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/intersection(_:eofill:))
- [func lineIntersection(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/lineintersection(_:eofill:))
- [func lineSubtraction(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/linesubtraction(_:eofill:))
- [func normalized(eoFill: Bool) -> Path](/documentation/swiftui/path/normalized(eofill:))
- [func subtracting(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/subtracting(_:eofill:))
- [func symmetricDifference(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/symmetricdifference(_:eofill:))
- [func union(Path, eoFill: Bool) -> Path](/documentation/swiftui/path/union(_:eofill:))

#### Operating over path elements

- [func forEach((Path.Element) -> Void)](/documentation/swiftui/path/foreach(_:))
- [Path.Element](/documentation/swiftui/path/element)

##### Getting path elements

- [case closeSubpath](/documentation/swiftui/path/element/closesubpath)
- [case curve(to: CGPoint, control1: CGPoint, control2: CGPoint)](/documentation/swiftui/path/element/curve(to:control1:control2:))
- [case line(to: CGPoint)](/documentation/swiftui/path/element/line(to:))
- [case move(to: CGPoint)](/documentation/swiftui/path/element/move(to:))
- [case quadCurve(to: CGPoint, control: CGPoint)](/documentation/swiftui/path/element/quadcurve(to:control:))

#### Applying a style

- [func strokedPath(StrokeStyle) -> Path](/documentation/swiftui/path/strokedpath(_:))

#### Instance Methods

- [func addRoundedRect(in: CGRect, cornerRadii: RectangleCornerRadii, style: RoundedCornerStyle, transform: CGAffineTransform)](/documentation/swiftui/path/addroundedrect(in:cornerradii:style:transform:))

### Defining shape behavior

- [ShapeView](/documentation/swiftui/shapeview)

#### Getting the shape

- [var shape: Self.Content](/documentation/swiftui/shapeview/shape)
- [Content](/documentation/swiftui/shapeview/content)

#### Modify the shape

- [func fill<S>(S, style: FillStyle) -> FillShapeView<Self.Content, S, Self>](/documentation/swiftui/shapeview/fill(_:style:))
- [func stroke<S>(S, style: StrokeStyle, antialiased: Bool) -> StrokeShapeView<Self.Content, S, Self>](/documentation/swiftui/shapeview/stroke(_:style:antialiased:))
- [func stroke<S>(S, lineWidth: CGFloat, antialiased: Bool) -> StrokeShapeView<Self.Content, S, Self>](/documentation/swiftui/shapeview/stroke(_:linewidth:antialiased:))
- [func strokeBorder<S>(S, style: StrokeStyle, antialiased: Bool) -> StrokeBorderShapeView<Self.Content, S, Self>](/documentation/swiftui/shapeview/strokeborder(_:style:antialiased:))
- [func strokeBorder<S>(S, lineWidth: CGFloat, antialiased: Bool) -> StrokeBorderShapeView<Self.Content, S, Self>](/documentation/swiftui/shapeview/strokeborder(_:linewidth:antialiased:))
- [Shape](/documentation/swiftui/shape)

#### Getting standard shapes

- [static var buttonBorder: ButtonBorderShape](/documentation/swiftui/shape/buttonborder)
- [static var capsule: Capsule](/documentation/swiftui/shape/capsule)
- [static func capsule(style: RoundedCornerStyle) -> Self](/documentation/swiftui/shape/capsule(style:))
- [static var circle: Circle](/documentation/swiftui/shape/circle)
- [static var containerRelative: ContainerRelativeShape](/documentation/swiftui/shape/containerrelative)
- [static var ellipse: Ellipse](/documentation/swiftui/shape/ellipse)
- [static var rect: Rectangle](/documentation/swiftui/shape/rect)
- [static func rect(cornerRadii: RectangleCornerRadii, style: RoundedCornerStyle) -> Self](/documentation/swiftui/shape/rect(cornerradii:style:))
- [static func rect(cornerRadius: CGFloat, style: RoundedCornerStyle) -> Self](/documentation/swiftui/shape/rect(cornerradius:style:))
- [static func rect(cornerSize: CGSize, style: RoundedCornerStyle) -> Self](/documentation/swiftui/shape/rect(cornersize:style:))
- [static func rect(topLeadingRadius: CGFloat, bottomLeadingRadius: CGFloat, bottomTrailingRadius: CGFloat, topTrailingRadius: CGFloat, style: RoundedCornerStyle) -> Self](/documentation/swiftui/shape/rect(topleadingradius:bottomleadingradius:bottomtrailingradius:toptrailingradius:style:))

#### Defining a shape’s size and path

- [func sizeThatFits(ProposedViewSize) -> CGSize](/documentation/swiftui/shape/sizethatfits(_:))
- [func path(in: CGRect) -> Path](/documentation/swiftui/shape/path(in:))

#### Transforming a shape

- [func trim(from: CGFloat, to: CGFloat) -> some Shape](/documentation/swiftui/shape/trim(from:to:))
- [func transform(CGAffineTransform) -> TransformedShape<Self>](/documentation/swiftui/shape/transform(_:))
- [func size(CGSize) -> some Shape](/documentation/swiftui/shape/size(_:))
- [func size(width: CGFloat, height: CGFloat) -> some Shape](/documentation/swiftui/shape/size(width:height:))
- [func scale(CGFloat, anchor: UnitPoint) -> ScaledShape<Self>](/documentation/swiftui/shape/scale(_:anchor:))
- [func scale(x: CGFloat, y: CGFloat, anchor: UnitPoint) -> ScaledShape<Self>](/documentation/swiftui/shape/scale(x:y:anchor:))
- [func rotation(Angle, anchor: UnitPoint) -> RotatedShape<Self>](/documentation/swiftui/shape/rotation(_:anchor:))
- [func offset(_:)](/documentation/swiftui/shape/offset(_:))
- [func offset(x: CGFloat, y: CGFloat) -> OffsetShape<Self>](/documentation/swiftui/shape/offset(x:y:))

#### Setting the stroke characteristics

- [func stroke<S>(S, lineWidth: CGFloat) -> some View](/documentation/swiftui/shape/stroke(_:linewidth:))
- [func stroke<S>(S, lineWidth: CGFloat, antialiased: Bool) -> StrokeShapeView<Self, S, EmptyView>](/documentation/swiftui/shape/stroke(_:linewidth:antialiased:))
- [func stroke(lineWidth: CGFloat) -> some Shape](/documentation/swiftui/shape/stroke(linewidth:))
- [func stroke<S>(S, style: StrokeStyle) -> some View](/documentation/swiftui/shape/stroke(_:style:))
- [func stroke<S>(S, style: StrokeStyle, antialiased: Bool) -> StrokeShapeView<Self, S, EmptyView>](/documentation/swiftui/shape/stroke(_:style:antialiased:))
- [func stroke(style: StrokeStyle) -> some Shape](/documentation/swiftui/shape/stroke(style:))

#### Filling a shape

- [func fill(_:style:)](/documentation/swiftui/shape/fill(_:style:))
- [func fill(style: FillStyle) -> some View](/documentation/swiftui/shape/fill(style:))

#### Setting the role

- [static var role: ShapeRole](/documentation/swiftui/shape/role)

#### Indicating a layout direction

- [var layoutDirectionBehavior: LayoutDirectionBehavior](/documentation/swiftui/shape/layoutdirectionbehavior)

#### Performing operations on a shape

- [func intersection<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/intersection(_:eofill:))
- [func lineIntersection<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/lineintersection(_:eofill:))
- [func lineSubtraction<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/linesubtraction(_:eofill:))
- [func subtracting<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/subtracting(_:eofill:))
- [func symmetricDifference<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/symmetricdifference(_:eofill:))
- [func union<T>(T, eoFill: Bool) -> some Shape](/documentation/swiftui/shape/union(_:eofill:))

#### Instance Methods

- [func size(CGSize, anchor: UnitPoint) -> some Shape](/documentation/swiftui/shape/size(_:anchor:))
- [func size(width: CGFloat, height: CGFloat, anchor: UnitPoint) -> some Shape](/documentation/swiftui/shape/size(width:height:anchor:))

#### Type Methods

- [static func rect(corners: Edge.Corner.Style, isUniform: Bool) -> Self](/documentation/swiftui/shape/rect(corners:isuniform:))
- [static func rect(topLeadingCorner: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(topleadingcorner:toptrailingcorner:bottomleadingcorner:bottomtrailingcorner:))
- [static func rect(uniformBottomCorners: Edge.Corner.Style, topLeadingCorner: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformbottomcorners:topleadingcorner:toptrailingcorner:))
- [static func rect(uniformLeadingCorners: Edge.Corner.Style, topTrailingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformleadingcorners:toptrailingcorner:bottomtrailingcorner:))
- [static func rect(uniformLeadingCorners: Edge.Corner.Style, uniformTrailingCorners: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformleadingcorners:uniformtrailingcorners:))
- [static func rect(uniformTopCorners: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style, bottomTrailingCorner: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformtopcorners:bottomleadingcorner:bottomtrailingcorner:))
- [static func rect(uniformTopCorners: Edge.Corner.Style, uniformBottomCorners: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformtopcorners:uniformbottomcorners:))
- [static func rect(uniformTrailingCorners: Edge.Corner.Style, topLeadingCorner: Edge.Corner.Style, bottomLeadingCorner: Edge.Corner.Style) -> Self](/documentation/swiftui/shape/rect(uniformtrailingcorners:topleadingcorner:bottomleadingcorner:))
- [AnyShape](/documentation/swiftui/anyshape)

#### Creating a shape

- [init<S>(S)](/documentation/swiftui/anyshape/init(_:))
- [ShapeRole](/documentation/swiftui/shaperole)

#### Getting shape roles

- [case fill](/documentation/swiftui/shaperole/fill)
- [case stroke](/documentation/swiftui/shaperole/stroke)
- [case separator](/documentation/swiftui/shaperole/separator)
- [StrokeStyle](/documentation/swiftui/strokestyle)

#### Creating a stroke style

- [init(lineWidth: CGFloat, lineCap: CGLineCap, lineJoin: CGLineJoin, miterLimit: CGFloat, dash: [CGFloat], dashPhase: CGFloat)](/documentation/swiftui/strokestyle/init(linewidth:linecap:linejoin:miterlimit:dash:dashphase:))

#### Setting stroke style properties

- [var lineWidth: CGFloat](/documentation/swiftui/strokestyle/linewidth)
- [var lineCap: CGLineCap](/documentation/swiftui/strokestyle/linecap)
- [var lineJoin: CGLineJoin](/documentation/swiftui/strokestyle/linejoin)
- [var miterLimit: CGFloat](/documentation/swiftui/strokestyle/miterlimit)
- [var dash: [CGFloat]](/documentation/swiftui/strokestyle/dash)
- [var dashPhase: CGFloat](/documentation/swiftui/strokestyle/dashphase)
- [StrokeShapeView](/documentation/swiftui/strokeshapeview)

#### Creating a stroke shape view

- [init(shape: Content, style: Style, strokeStyle: StrokeStyle, isAntialiased: Bool, background: Background)](/documentation/swiftui/strokeshapeview/init(shape:style:strokestyle:isantialiased:background:))

#### Getting shape view properties

- [var background: Background](/documentation/swiftui/strokeshapeview/background)
- [var isAntialiased: Bool](/documentation/swiftui/strokeshapeview/isantialiased)
- [var shape: Content](/documentation/swiftui/strokeshapeview/shape)
- [var strokeStyle: StrokeStyle](/documentation/swiftui/strokeshapeview/strokestyle)
- [var style: Style](/documentation/swiftui/strokeshapeview/style)
- [StrokeBorderShapeView](/documentation/swiftui/strokebordershapeview)

#### Creating a stroke border shape view

- [init(shape: Content, style: Style, strokeStyle: StrokeStyle, isAntialiased: Bool, background: Background)](/documentation/swiftui/strokebordershapeview/init(shape:style:strokestyle:isantialiased:background:))

#### Getting shape view properties

- [var background: Background](/documentation/swiftui/strokebordershapeview/background)
- [var isAntialiased: Bool](/documentation/swiftui/strokebordershapeview/isantialiased)
- [var shape: Content](/documentation/swiftui/strokebordershapeview/shape)
- [var strokeStyle: StrokeStyle](/documentation/swiftui/strokebordershapeview/strokestyle)
- [var style: Style](/documentation/swiftui/strokebordershapeview/style)
- [FillStyle](/documentation/swiftui/fillstyle)

#### Creating a fill style

- [init(eoFill: Bool, antialiased: Bool)](/documentation/swiftui/fillstyle/init(eofill:antialiased:))

#### Setting fill style properties

- [var isEOFilled: Bool](/documentation/swiftui/fillstyle/iseofilled)
- [var isAntialiased: Bool](/documentation/swiftui/fillstyle/isantialiased)
- [FillShapeView](/documentation/swiftui/fillshapeview)

#### Creating a stroke shape view

- [init(shape: Content, style: Style, fillStyle: FillStyle, background: Background)](/documentation/swiftui/fillshapeview/init(shape:style:fillstyle:background:))

#### Getting shape view properties

- [var background: Background](/documentation/swiftui/fillshapeview/background)
- [var fillStyle: FillStyle](/documentation/swiftui/fillshapeview/fillstyle)
- [var shape: Content](/documentation/swiftui/fillshapeview/shape)
- [var style: Style](/documentation/swiftui/fillshapeview/style)

### Transforming a shape

- [ScaledShape](/documentation/swiftui/scaledshape)

#### Creating a scaled shape

- [init(shape: Content, scale: CGSize, anchor: UnitPoint)](/documentation/swiftui/scaledshape/init(shape:scale:anchor:))

#### Getting the shape’s characteristics

- [var anchor: UnitPoint](/documentation/swiftui/scaledshape/anchor)
- [var scale: CGSize](/documentation/swiftui/scaledshape/scale)
- [var shape: Content](/documentation/swiftui/scaledshape/shape)

#### Supporting types

- [var animatableData: ScaledShape<Content>.AnimatableData](/documentation/swiftui/scaledshape/animatabledata)
- [RotatedShape](/documentation/swiftui/rotatedshape)

#### Creating a rotated shape

- [init(shape: Content, angle: Angle, anchor: UnitPoint)](/documentation/swiftui/rotatedshape/init(shape:angle:anchor:))

#### Getting the shape’s characteristics

- [var anchor: UnitPoint](/documentation/swiftui/rotatedshape/anchor)
- [var angle: Angle](/documentation/swiftui/rotatedshape/angle)
- [var shape: Content](/documentation/swiftui/rotatedshape/shape)

#### Supporting types

- [var animatableData: RotatedShape<Content>.AnimatableData](/documentation/swiftui/rotatedshape/animatabledata)
- [OffsetShape](/documentation/swiftui/offsetshape)

#### Creating an offset shape

- [init(shape: Content, offset: CGSize)](/documentation/swiftui/offsetshape/init(shape:offset:))

#### Getting the shape’s characteristics

- [var offset: CGSize](/documentation/swiftui/offsetshape/offset)
- [var shape: Content](/documentation/swiftui/offsetshape/shape)

#### Supporting types

- [var animatableData: OffsetShape<Content>.AnimatableData](/documentation/swiftui/offsetshape/animatabledata)
- [TransformedShape](/documentation/swiftui/transformedshape)

#### Creating a transformed shape

- [init(shape: Content, transform: CGAffineTransform)](/documentation/swiftui/transformedshape/init(shape:transform:))

#### Getting the shape’s characteristics

- [var shape: Content](/documentation/swiftui/transformedshape/shape)
- [var transform: CGAffineTransform](/documentation/swiftui/transformedshape/transform)

### Setting a container shape

- [func containerShape(_:)](/documentation/swiftui/view/containershape(_:))
- [InsettableShape](/documentation/swiftui/insettableshape)

#### Setting the stroke border characteristics

- [func strokeBorder(_:lineWidth:antialiased:)](/documentation/swiftui/insettableshape/strokeborder(_:linewidth:antialiased:))
- [func strokeBorder(lineWidth: CGFloat, antialiased: Bool) -> some View](/documentation/swiftui/insettableshape/strokeborder(linewidth:antialiased:))
- [func strokeBorder(_:style:antialiased:)](/documentation/swiftui/insettableshape/strokeborder(_:style:antialiased:))
- [func strokeBorder(style: StrokeStyle, antialiased: Bool) -> some View](/documentation/swiftui/insettableshape/strokeborder(style:antialiased:))

#### Setting the inset

- [func inset(by: CGFloat) -> Self.InsetShape](/documentation/swiftui/insettableshape/inset(by:))
- [InsetShape](/documentation/swiftui/insettableshape/insetshape)
- [ContainerRelativeShape](/documentation/swiftui/containerrelativeshape)

#### Creating the shape

- [init()](/documentation/swiftui/containerrelativeshape/init())
- [Drawing and graphics](/documentation/swiftui/drawing-and-graphics)

### Immediate mode drawing

- [Add rich graphics to your SwiftUI app](/documentation/swiftui/add-rich-graphics-to-your-swiftui-app)
- [Canvas](/documentation/swiftui/canvas)

#### Creating a canvas

- [init(opaque: Bool, colorMode: ColorRenderingMode, rendersAsynchronously: Bool, renderer: (inout GraphicsContext, CGSize) -> Void)](/documentation/swiftui/canvas/init(opaque:colormode:rendersasynchronously:renderer:))
- [init(opaque: Bool, colorMode: ColorRenderingMode, rendersAsynchronously: Bool, renderer: (inout GraphicsContext, CGSize) -> Void, symbols: () -> Symbols)](/documentation/swiftui/canvas/init(opaque:colormode:rendersasynchronously:renderer:symbols:))

#### Managing opacity and color

- [var isOpaque: Bool](/documentation/swiftui/canvas/isopaque)
- [var colorMode: ColorRenderingMode](/documentation/swiftui/canvas/colormode)

#### Referencing symbols

- [var symbols: Symbols](/documentation/swiftui/canvas/symbols)

#### Rendering

- [var rendersAsynchronously: Bool](/documentation/swiftui/canvas/rendersasynchronously)
- [var renderer: (inout GraphicsContext, CGSize) -> Void](/documentation/swiftui/canvas/renderer)
- [GraphicsContext](/documentation/swiftui/graphicscontext)

#### Drawing a path

- [func stroke(Path, with: GraphicsContext.Shading, lineWidth: CGFloat)](/documentation/swiftui/graphicscontext/stroke(_:with:linewidth:))
- [func stroke(Path, with: GraphicsContext.Shading, style: StrokeStyle)](/documentation/swiftui/graphicscontext/stroke(_:with:style:))
- [func fill(Path, with: GraphicsContext.Shading, style: FillStyle)](/documentation/swiftui/graphicscontext/fill(_:with:style:))
- [GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading)

##### Colors

- [static func color(Color) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/color(_:))
- [static func color(Color.RGBColorSpace, red: Double, green: Double, blue: Double, opacity: Double) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/color(_:red:green:blue:opacity:))
- [static func color(Color.RGBColorSpace, white: Double, opacity: Double) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/color(_:white:opacity:))

##### Gradients

- [static func linearGradient(Gradient, startPoint: CGPoint, endPoint: CGPoint, options: GraphicsContext.GradientOptions) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/lineargradient(_:startpoint:endpoint:options:))
- [static func radialGradient(Gradient, center: CGPoint, startRadius: CGFloat, endRadius: CGFloat, options: GraphicsContext.GradientOptions) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/radialgradient(_:center:startradius:endradius:options:))
- [static func conicGradient(Gradient, center: CGPoint, angle: Angle, options: GraphicsContext.GradientOptions) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/conicgradient(_:center:angle:options:))

##### Other shape styles

- [static func style<S>(S) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/style(_:))
- [static var foreground: GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/foreground)

##### Images

- [static func tiledImage(Image, origin: CGPoint, sourceRect: CGRect, scale: CGFloat) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/tiledimage(_:origin:sourcerect:scale:))

##### Composite shading types

- [static func palette([GraphicsContext.Shading]) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/palette(_:))
- [static var backdrop: GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/backdrop)

##### Using a custom Metal shader

- [static func shader(Shader, bounds: CGRect) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/shader(_:bounds:))

##### Type Methods

- [static func meshGradient(MeshGradient) -> GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading/meshgradient(_:))
- [GraphicsContext.GradientOptions](/documentation/swiftui/graphicscontext/gradientoptions)

##### Getting gradient options

- [static var linearColor: GraphicsContext.GradientOptions](/documentation/swiftui/graphicscontext/gradientoptions/linearcolor)
- [static var mirror: GraphicsContext.GradientOptions](/documentation/swiftui/graphicscontext/gradientoptions/mirror)
- [static var `repeat`: GraphicsContext.GradientOptions](/documentation/swiftui/graphicscontext/gradientoptions/repeat)

#### Drawing images, text, and views

- [func draw(_:in:)](/documentation/swiftui/graphicscontext/draw(_:in:))
- [func draw(_:in:style:)](/documentation/swiftui/graphicscontext/draw(_:in:style:))
- [func draw(_:at:anchor:)](/documentation/swiftui/graphicscontext/draw(_:at:anchor:))

#### Drawing into a new layer

- [func drawLayer(content: (inout GraphicsContext) throws -> Void) rethrows](/documentation/swiftui/graphicscontext/drawlayer(content:))

#### Resolving a drawn entity

- [func resolve(_:)](/documentation/swiftui/graphicscontext/resolve(_:))
- [func resolveSymbol<ID>(id: ID) -> GraphicsContext.ResolvedSymbol?](/documentation/swiftui/graphicscontext/resolvesymbol(id:))
- [GraphicsContext.ResolvedSymbol](/documentation/swiftui/graphicscontext/resolvedsymbol)

##### Getting the symbol properties

- [var size: CGSize](/documentation/swiftui/graphicscontext/resolvedsymbol/size)
- [GraphicsContext.ResolvedImage](/documentation/swiftui/graphicscontext/resolvedimage)

##### Getting the image properties

- [var size: CGSize](/documentation/swiftui/graphicscontext/resolvedimage/size)
- [let baseline: CGFloat](/documentation/swiftui/graphicscontext/resolvedimage/baseline)
- [var shading: GraphicsContext.Shading?](/documentation/swiftui/graphicscontext/resolvedimage/shading)
- [GraphicsContext.ResolvedText](/documentation/swiftui/graphicscontext/resolvedtext)

##### Getting the text properties

- [func firstBaseline(in: CGSize) -> CGFloat](/documentation/swiftui/graphicscontext/resolvedtext/firstbaseline(in:))
- [func lastBaseline(in: CGSize) -> CGFloat](/documentation/swiftui/graphicscontext/resolvedtext/lastbaseline(in:))
- [func measure(in: CGSize) -> CGSize](/documentation/swiftui/graphicscontext/resolvedtext/measure(in:))
- [var shading: GraphicsContext.Shading](/documentation/swiftui/graphicscontext/resolvedtext/shading)

#### Masking

- [func clip(to: Path, style: FillStyle, options: GraphicsContext.ClipOptions)](/documentation/swiftui/graphicscontext/clip(to:style:options:))
- [func clipToLayer(opacity: Double, options: GraphicsContext.ClipOptions, content: (inout GraphicsContext) throws -> Void) rethrows](/documentation/swiftui/graphicscontext/cliptolayer(opacity:options:content:))
- [var clipBoundingRect: CGRect](/documentation/swiftui/graphicscontext/clipboundingrect)
- [GraphicsContext.ClipOptions](/documentation/swiftui/graphicscontext/clipoptions)

##### Getting clip options

- [static var inverse: GraphicsContext.ClipOptions](/documentation/swiftui/graphicscontext/clipoptions/inverse)

#### Setting opacity and the blend mode

- [var opacity: Double](/documentation/swiftui/graphicscontext/opacity)
- [var blendMode: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.property)
- [GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct)

##### Getting the default

- [static var normal: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/normal)

##### Darkening

- [static var darken: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/darken)
- [static var multiply: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/multiply)
- [static var colorBurn: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/colorburn)
- [static var plusDarker: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/plusdarker)

##### Lightening

- [static var lighten: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/lighten)
- [static var screen: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/screen)
- [static var colorDodge: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/colordodge)
- [static var plusLighter: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/pluslighter)

##### Adding contrast

- [static var overlay: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/overlay)
- [static var softLight: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/softlight)
- [static var hardLight: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/hardlight)

##### Inverting

- [static var difference: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/difference)
- [static var exclusion: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/exclusion)

##### Mixing color components

- [static var hue: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/hue)
- [static var saturation: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/saturation)
- [static var color: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/color)
- [static var luminosity: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/luminosity)

##### Accessing Porter-Duff modes

- [static var clear: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/clear)
- [static var copy: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/copy)
- [static var sourceIn: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/sourcein)
- [static var sourceOut: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/sourceout)
- [static var sourceAtop: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/sourceatop)
- [static var destinationOver: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/destinationover)
- [static var destinationIn: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/destinationin)
- [static var destinationOut: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/destinationout)
- [static var destinationAtop: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/destinationatop)
- [static var xor: GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct/xor)

#### Filtering

- [func addFilter(GraphicsContext.Filter, options: GraphicsContext.FilterOptions)](/documentation/swiftui/graphicscontext/addfilter(_:options:))
- [GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter)

##### Changing brightness and contrast

- [static func brightness(Double) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/brightness(_:))
- [static func contrast(Double) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/contrast(_:))

##### Manipulating color

- [static func saturation(Double) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/saturation(_:))
- [static func colorInvert(Double) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/colorinvert(_:))
- [static func colorMultiply(Color) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/colormultiply(_:))
- [static func hueRotation(Angle) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/huerotation(_:))
- [static func grayscale(Double) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/grayscale(_:))
- [static func colorMatrix(ColorMatrix) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/colormatrix(_:))

##### Adding blur

- [static func blur(radius: CGFloat, options: GraphicsContext.BlurOptions) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/blur(radius:options:))

##### Adding a shadow

- [static func shadow(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat, blendMode: GraphicsContext.BlendMode, options: GraphicsContext.ShadowOptions) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/shadow(color:radius:x:y:blendmode:options:))

##### Adjusting opacity

- [static var luminanceToAlpha: GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/luminancetoalpha)
- [static func alphaThreshold(min: Double, max: Double, color: Color) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/alphathreshold(min:max:color:))

##### Adding a transformation

- [static func projectionTransform(ProjectionTransform) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/projectiontransform(_:))

##### Using a custom Metal shader

- [static func colorShader(Shader) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/colorshader(_:))
- [static func distortionShader(Shader, maxSampleOffset: CGSize) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/distortionshader(_:maxsampleoffset:))
- [static func layerShader(Shader, maxSampleOffset: CGSize) -> GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter/layershader(_:maxsampleoffset:))
- [GraphicsContext.FilterOptions](/documentation/swiftui/graphicscontext/filteroptions)

##### Getting filter options

- [static var linearColor: GraphicsContext.FilterOptions](/documentation/swiftui/graphicscontext/filteroptions/linearcolor)
- [GraphicsContext.BlurOptions](/documentation/swiftui/graphicscontext/bluroptions)

##### Getting blur options

- [static var dithersResult: GraphicsContext.BlurOptions](/documentation/swiftui/graphicscontext/bluroptions/dithersresult)
- [static var opaque: GraphicsContext.BlurOptions](/documentation/swiftui/graphicscontext/bluroptions/opaque)
- [GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions)

##### Getting shadow options

- [static var disablesGroup: GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions/disablesgroup)
- [static var invertsAlpha: GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions/invertsalpha)
- [static var shadowAbove: GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions/shadowabove)
- [static var shadowOnly: GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions/shadowonly)

#### Applying transforms

- [func scaleBy(x: CGFloat, y: CGFloat)](/documentation/swiftui/graphicscontext/scaleby(x:y:))
- [func rotate(by: Angle)](/documentation/swiftui/graphicscontext/rotate(by:))
- [func translateBy(x: CGFloat, y: CGFloat)](/documentation/swiftui/graphicscontext/translateby(x:y:))
- [func concatenate(CGAffineTransform)](/documentation/swiftui/graphicscontext/concatenate(_:))
- [var transform: CGAffineTransform](/documentation/swiftui/graphicscontext/transform)

#### Drawing with a core graphics context

- [func withCGContext(content: (CGContext) throws -> Void) rethrows](/documentation/swiftui/graphicscontext/withcgcontext(content:))

#### Accessing the environment

- [var environment: EnvironmentValues](/documentation/swiftui/graphicscontext/environment)

#### Instance Methods

- [func draw(_:options:)](/documentation/swiftui/graphicscontext/draw(_:options:))

### Setting a color

- [func tint(_:)](/documentation/swiftui/view/tint(_:))
- [Color](/documentation/swiftui/color)

#### Creating a color

- [init(String, bundle: Bundle?)](/documentation/swiftui/color/init(_:bundle:))
- [init(_:)](/documentation/swiftui/color/init(_:))
- [func resolve(in: EnvironmentValues) -> Color.Resolved](/documentation/swiftui/color/resolve(in:))

#### Creating a color from component values

- [init(hue: Double, saturation: Double, brightness: Double, opacity: Double)](/documentation/swiftui/color/init(hue:saturation:brightness:opacity:))
- [init(Color.RGBColorSpace, white: Double, opacity: Double)](/documentation/swiftui/color/init(_:white:opacity:))
- [init(Color.RGBColorSpace, red: Double, green: Double, blue: Double, opacity: Double)](/documentation/swiftui/color/init(_:red:green:blue:opacity:))
- [Color.RGBColorSpace](/documentation/swiftui/color/rgbcolorspace)

##### Getting color spaces

- [case sRGB](/documentation/swiftui/color/rgbcolorspace/srgb)
- [case sRGBLinear](/documentation/swiftui/color/rgbcolorspace/srgblinear)
- [case displayP3](/documentation/swiftui/color/rgbcolorspace/displayp3)

#### Creating a color from another color

- [init(uiColor: UIColor)](/documentation/swiftui/color/init(uicolor:))
- [init(nsColor: NSColor)](/documentation/swiftui/color/init(nscolor:))
- [init(cgColor: CGColor)](/documentation/swiftui/color/init(cgcolor:))

#### Getting standard colors

- [static let black: Color](/documentation/swiftui/color/black)
- [static let blue: Color](/documentation/swiftui/color/blue)
- [static let brown: Color](/documentation/swiftui/color/brown)
- [static let clear: Color](/documentation/swiftui/color/clear)
- [static let cyan: Color](/documentation/swiftui/color/cyan)
- [static let gray: Color](/documentation/swiftui/color/gray)
- [static let green: Color](/documentation/swiftui/color/green)
- [static let indigo: Color](/documentation/swiftui/color/indigo)
- [static let mint: Color](/documentation/swiftui/color/mint)
- [static let orange: Color](/documentation/swiftui/color/orange)
- [static let pink: Color](/documentation/swiftui/color/pink)
- [static let purple: Color](/documentation/swiftui/color/purple)
- [static let red: Color](/documentation/swiftui/color/red)
- [static let teal: Color](/documentation/swiftui/color/teal)
- [static let white: Color](/documentation/swiftui/color/white)
- [static let yellow: Color](/documentation/swiftui/color/yellow)

#### Getting semantic colors

- [static var accentColor: Color](/documentation/swiftui/color/accentcolor)
- [static let primary: Color](/documentation/swiftui/color/primary)
- [static let secondary: Color](/documentation/swiftui/color/secondary)

#### Modifying a color

- [func opacity(Double) -> Color](/documentation/swiftui/color/opacity(_:))
- [var gradient: AnyGradient](/documentation/swiftui/color/gradient)
- [func mix(with: Color, by: Double, in: Gradient.ColorSpace) -> Color](/documentation/swiftui/color/mix(with:by:in:))
- [func exposureAdjust(Double) -> Color](/documentation/swiftui/color/exposureadjust(_:))
- [func headroom(Double?) -> Color](/documentation/swiftui/color/headroom(_:))

#### Working with high dynamic range (HDR) colors

- [func resolveHDR(in: EnvironmentValues) -> Color.ResolvedHDR](/documentation/swiftui/color/resolvehdr(in:))
- [Color.ResolvedHDR](/documentation/swiftui/color/resolvedhdr)

##### Creating a concrete color value

- [init(Color.Resolved, headroom: Float?)](/documentation/swiftui/color/resolvedhdr/init(_:headroom:))

##### Getting color properties

- [var red: Float](/documentation/swiftui/color/resolvedhdr/red)
- [var green: Float](/documentation/swiftui/color/resolvedhdr/green)
- [var blue: Float](/documentation/swiftui/color/resolvedhdr/blue)
- [var linearRed: Float](/documentation/swiftui/color/resolvedhdr/linearred)
- [var linearGreen: Float](/documentation/swiftui/color/resolvedhdr/lineargreen)
- [var linearBlue: Float](/documentation/swiftui/color/resolvedhdr/linearblue)
- [var opacity: Float](/documentation/swiftui/color/resolvedhdr/opacity)
- [var headroom: Float?](/documentation/swiftui/color/resolvedhdr/headroom)

#### Describing a color

- [var description: String](/documentation/swiftui/color/description)

#### Comparing colors

- [static func == (Color, Color) -> Bool](/documentation/swiftui/color/==(_:_:))
- [func hash(into: inout Hasher)](/documentation/swiftui/color/hash(into:))

#### Deprecated symbols

- [var cgColor: CGColor?](/documentation/swiftui/color/cgcolor)

#### Default Implementations

- [ShapeStyle Implementations](/documentation/swiftui/color/shapestyle-implementations)

##### Structures

- [Color.Resolved](/documentation/swiftui/color/resolved)

###### Initializers

- [init(colorSpace: Color.RGBColorSpace, red: Float, green: Float, blue: Float, opacity: Float)](/documentation/swiftui/color/resolved/init(colorspace:red:green:blue:opacity:))

###### Instance Properties

- [var blue: Float](/documentation/swiftui/color/resolved/blue)
- [var cgColor: CGColor](/documentation/swiftui/color/resolved/cgcolor)
- [var green: Float](/documentation/swiftui/color/resolved/green)
- [var linearBlue: Float](/documentation/swiftui/color/resolved/linearblue)
- [var linearGreen: Float](/documentation/swiftui/color/resolved/lineargreen)
- [var linearRed: Float](/documentation/swiftui/color/resolved/linearred)
- [var opacity: Float](/documentation/swiftui/color/resolved/opacity)
- [var red: Float](/documentation/swiftui/color/resolved/red)
- [Transferable Implementations](/documentation/swiftui/color/transferable-implementations)

##### Type Properties

- [static var transferRepresentation: some TransferRepresentation](/documentation/swiftui/color/transferrepresentation)

### Styling content

- [func border<S>(S, width: CGFloat) -> some View](/documentation/swiftui/view/border(_:width:))
- [func foregroundStyle<S>(S) -> some View](/documentation/swiftui/view/foregroundstyle(_:))
- [func foregroundStyle<S1, S2>(S1, S2) -> some View](/documentation/swiftui/view/foregroundstyle(_:_:))
- [func foregroundStyle<S1, S2, S3>(S1, S2, S3) -> some View](/documentation/swiftui/view/foregroundstyle(_:_:_:))
- [func backgroundStyle<S>(S) -> some View](/documentation/swiftui/view/backgroundstyle(_:))
- [var backgroundStyle: AnyShapeStyle?](/documentation/swiftui/environmentvalues/backgroundstyle)
- [ShapeStyle](/documentation/swiftui/shapestyle)

#### System colors

- [static var black: Color](/documentation/swiftui/shapestyle/black)
- [static var blue: Color](/documentation/swiftui/shapestyle/blue)
- [static var brown: Color](/documentation/swiftui/shapestyle/brown)
- [static var clear: Color](/documentation/swiftui/shapestyle/clear)
- [static var cyan: Color](/documentation/swiftui/shapestyle/cyan)
- [static var gray: Color](/documentation/swiftui/shapestyle/gray)
- [static var green: Color](/documentation/swiftui/shapestyle/green)
- [static var indigo: Color](/documentation/swiftui/shapestyle/indigo)
- [static var mint: Color](/documentation/swiftui/shapestyle/mint)
- [static var orange: Color](/documentation/swiftui/shapestyle/orange)
- [static var pink: Color](/documentation/swiftui/shapestyle/pink)
- [static var purple: Color](/documentation/swiftui/shapestyle/purple)
- [static var red: Color](/documentation/swiftui/shapestyle/red)
- [static var teal: Color](/documentation/swiftui/shapestyle/teal)
- [static var white: Color](/documentation/swiftui/shapestyle/white)
- [static var yellow: Color](/documentation/swiftui/shapestyle/yellow)

#### Angular gradients

- [static angularGradient(_:center:startAngle:endAngle:)](/documentation/swiftui/shapestyle/angulargradient(_:center:startangle:endangle:))
- [static func angularGradient(colors: [Color], center: UnitPoint, startAngle: Angle, endAngle: Angle) -> AngularGradient](/documentation/swiftui/shapestyle/angulargradient(colors:center:startangle:endangle:))
- [static func angularGradient(stops: [Gradient.Stop], center: UnitPoint, startAngle: Angle, endAngle: Angle) -> AngularGradient](/documentation/swiftui/shapestyle/angulargradient(stops:center:startangle:endangle:))

#### Conic gradients

- [static conicGradient(_:center:angle:)](/documentation/swiftui/shapestyle/conicgradient(_:center:angle:))
- [static func conicGradient(colors: [Color], center: UnitPoint, angle: Angle) -> AngularGradient](/documentation/swiftui/shapestyle/conicgradient(colors:center:angle:))
- [static func conicGradient(stops: [Gradient.Stop], center: UnitPoint, angle: Angle) -> AngularGradient](/documentation/swiftui/shapestyle/conicgradient(stops:center:angle:))

#### Elliptical gradients

- [static ellipticalGradient(_:center:startRadiusFraction:endRadiusFraction:)](/documentation/swiftui/shapestyle/ellipticalgradient(_:center:startradiusfraction:endradiusfraction:))
- [static func ellipticalGradient(colors: [Color], center: UnitPoint, startRadiusFraction: CGFloat, endRadiusFraction: CGFloat) -> EllipticalGradient](/documentation/swiftui/shapestyle/ellipticalgradient(colors:center:startradiusfraction:endradiusfraction:))
- [static func ellipticalGradient(stops: [Gradient.Stop], center: UnitPoint, startRadiusFraction: CGFloat, endRadiusFraction: CGFloat) -> EllipticalGradient](/documentation/swiftui/shapestyle/ellipticalgradient(stops:center:startradiusfraction:endradiusfraction:))

#### Linear gradients

- [static linearGradient(_:startPoint:endPoint:)](/documentation/swiftui/shapestyle/lineargradient(_:startpoint:endpoint:))
- [static func linearGradient(colors: [Color], startPoint: UnitPoint, endPoint: UnitPoint) -> LinearGradient](/documentation/swiftui/shapestyle/lineargradient(colors:startpoint:endpoint:))
- [static func linearGradient(stops: [Gradient.Stop], startPoint: UnitPoint, endPoint: UnitPoint) -> LinearGradient](/documentation/swiftui/shapestyle/lineargradient(stops:startpoint:endpoint:))

#### Radial gradients

- [static radialGradient(_:center:startRadius:endRadius:)](/documentation/swiftui/shapestyle/radialgradient(_:center:startradius:endradius:))
- [static func radialGradient(colors: [Color], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat) -> RadialGradient](/documentation/swiftui/shapestyle/radialgradient(colors:center:startradius:endradius:))
- [static func radialGradient(stops: [Gradient.Stop], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat) -> RadialGradient](/documentation/swiftui/shapestyle/radialgradient(stops:center:startradius:endradius:))

#### Materials

- [static var ultraThinMaterial: Material](/documentation/swiftui/shapestyle/ultrathinmaterial)
- [static var thinMaterial: Material](/documentation/swiftui/shapestyle/thinmaterial)
- [static var regularMaterial: Material](/documentation/swiftui/shapestyle/regularmaterial)
- [static var thickMaterial: Material](/documentation/swiftui/shapestyle/thickmaterial)
- [static var ultraThickMaterial: Material](/documentation/swiftui/shapestyle/ultrathickmaterial)
- [static var bar: Material](/documentation/swiftui/shapestyle/bar)

#### Image paint styles

- [static func image(Image, sourceRect: CGRect, scale: CGFloat) -> ImagePaint](/documentation/swiftui/shapestyle/image(_:sourcerect:scale:))

#### Hierarchical styles

- [var secondary: some ShapeStyle](/documentation/swiftui/shapestyle/secondary-swift.property)
- [var tertiary: some ShapeStyle](/documentation/swiftui/shapestyle/tertiary-swift.property)
- [var quaternary: some ShapeStyle](/documentation/swiftui/shapestyle/quaternary-swift.property)
- [var quinary: some ShapeStyle](/documentation/swiftui/shapestyle/quinary-swift.property)
- [static var primary: HierarchicalShapeStyle](/documentation/swiftui/shapestyle/primary)
- [static var secondary: HierarchicalShapeStyle](/documentation/swiftui/shapestyle/secondary-swift.type.property)
- [static var tertiary: HierarchicalShapeStyle](/documentation/swiftui/shapestyle/tertiary-swift.type.property)
- [static var quaternary: HierarchicalShapeStyle](/documentation/swiftui/shapestyle/quaternary-swift.type.property)
- [static var quinary: HierarchicalShapeStyle](/documentation/swiftui/shapestyle/quinary-swift.type.property)

#### Semantic styles

- [static var foreground: ForegroundStyle](/documentation/swiftui/shapestyle/foreground)
- [static var background: BackgroundStyle](/documentation/swiftui/shapestyle/background)
- [static var selection: SelectionShapeStyle](/documentation/swiftui/shapestyle/selection)
- [static var separator: SeparatorShapeStyle](/documentation/swiftui/shapestyle/separator)
- [static var tint: TintShapeStyle](/documentation/swiftui/shapestyle/tint)
- [static var placeholder: PlaceholderTextShapeStyle](/documentation/swiftui/shapestyle/placeholder)
- [static var link: LinkShapeStyle](/documentation/swiftui/shapestyle/link)
- [static var fill: FillShapeStyle](/documentation/swiftui/shapestyle/fill)
- [static var windowBackground: WindowBackgroundShapeStyle](/documentation/swiftui/shapestyle/windowbackground)

#### Modifying a shape style

- [func blendMode(BlendMode) -> some ShapeStyle](/documentation/swiftui/shapestyle/blendmode(_:)-swift.method)
- [func opacity(Double) -> some ShapeStyle](/documentation/swiftui/shapestyle/opacity(_:)-swift.method)
- [func shadow(ShadowStyle) -> some ShapeStyle](/documentation/swiftui/shapestyle/shadow(_:)-swift.method)

#### Configuring the default shape style

- [static func blendMode(BlendMode) -> some ShapeStyle](/documentation/swiftui/shapestyle/blendmode(_:)-swift.type.method)
- [static func opacity(Double) -> some ShapeStyle](/documentation/swiftui/shapestyle/opacity(_:)-swift.type.method)
- [static func shadow(ShadowStyle) -> some ShapeStyle](/documentation/swiftui/shapestyle/shadow(_:)-swift.type.method)

#### Mapping to absolute coordinates

- [func `in`(CGRect) -> some ShapeStyle](/documentation/swiftui/shapestyle/in(_:))

#### Resolving a shape style in an environment

- [func resolve(in: EnvironmentValues) -> Self.Resolved](/documentation/swiftui/shapestyle/resolve(in:))
- [Resolved](/documentation/swiftui/shapestyle/resolved)

#### Using a shape style as a view

- [var body: _ShapeView<Rectangle, Self>](/documentation/swiftui/shapestyle/body)

#### Supporting types

- [AngularGradient](/documentation/swiftui/angulargradient)

##### Creating a full rotation angular gradient

- [init(gradient: Gradient, center: UnitPoint, angle: Angle)](/documentation/swiftui/angulargradient/init(gradient:center:angle:))
- [init(colors: [Color], center: UnitPoint, angle: Angle)](/documentation/swiftui/angulargradient/init(colors:center:angle:))
- [init(stops: [Gradient.Stop], center: UnitPoint, angle: Angle)](/documentation/swiftui/angulargradient/init(stops:center:angle:))

##### Creating a partial rotation angular gradient

- [init(gradient: Gradient, center: UnitPoint, startAngle: Angle, endAngle: Angle)](/documentation/swiftui/angulargradient/init(gradient:center:startangle:endangle:))
- [init(colors: [Color], center: UnitPoint, startAngle: Angle, endAngle: Angle)](/documentation/swiftui/angulargradient/init(colors:center:startangle:endangle:))
- [init(stops: [Gradient.Stop], center: UnitPoint, startAngle: Angle, endAngle: Angle)](/documentation/swiftui/angulargradient/init(stops:center:startangle:endangle:))
- [EllipticalGradient](/documentation/swiftui/ellipticalgradient)

##### Creating an elliptical gradient

- [init(gradient: Gradient, center: UnitPoint, startRadiusFraction: CGFloat, endRadiusFraction: CGFloat)](/documentation/swiftui/ellipticalgradient/init(gradient:center:startradiusfraction:endradiusfraction:))
- [init(colors: [Color], center: UnitPoint, startRadiusFraction: CGFloat, endRadiusFraction: CGFloat)](/documentation/swiftui/ellipticalgradient/init(colors:center:startradiusfraction:endradiusfraction:))
- [init(stops: [Gradient.Stop], center: UnitPoint, startRadiusFraction: CGFloat, endRadiusFraction: CGFloat)](/documentation/swiftui/ellipticalgradient/init(stops:center:startradiusfraction:endradiusfraction:))
- [LinearGradient](/documentation/swiftui/lineargradient)

##### Creating a linear gradient

- [init(gradient: Gradient, startPoint: UnitPoint, endPoint: UnitPoint)](/documentation/swiftui/lineargradient/init(gradient:startpoint:endpoint:))
- [init(colors: [Color], startPoint: UnitPoint, endPoint: UnitPoint)](/documentation/swiftui/lineargradient/init(colors:startpoint:endpoint:))
- [init(stops: [Gradient.Stop], startPoint: UnitPoint, endPoint: UnitPoint)](/documentation/swiftui/lineargradient/init(stops:startpoint:endpoint:))
- [RadialGradient](/documentation/swiftui/radialgradient)

##### Creating a radial gradient

- [init(gradient: Gradient, center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat)](/documentation/swiftui/radialgradient/init(gradient:center:startradius:endradius:))
- [init(colors: [Color], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat)](/documentation/swiftui/radialgradient/init(colors:center:startradius:endradius:))
- [init(stops: [Gradient.Stop], center: UnitPoint, startRadius: CGFloat, endRadius: CGFloat)](/documentation/swiftui/radialgradient/init(stops:center:startradius:endradius:))
- [Material](/documentation/swiftui/material)

##### Getting material types

- [static let ultraThin: Material](/documentation/swiftui/material/ultrathin)
- [static let thin: Material](/documentation/swiftui/material/thin)
- [static let regular: Material](/documentation/swiftui/material/regular)
- [static let thick: Material](/documentation/swiftui/material/thick)
- [static let ultraThick: Material](/documentation/swiftui/material/ultrathick)
- [static let bar: Material](/documentation/swiftui/material/bar)

##### Instance Methods

- [func materialActiveAppearance(MaterialActiveAppearance) -> Material](/documentation/swiftui/material/materialactiveappearance(_:))
- [ImagePaint](/documentation/swiftui/imagepaint)

##### Creating an image paint style

- [init(image: Image, sourceRect: CGRect, scale: CGFloat)](/documentation/swiftui/imagepaint/init(image:sourcerect:scale:))

##### Configuring the image paint style

- [var image: Image](/documentation/swiftui/imagepaint/image)
- [var scale: CGFloat](/documentation/swiftui/imagepaint/scale)
- [var sourceRect: CGRect](/documentation/swiftui/imagepaint/sourcerect)
- [HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle)

##### Getting hierarchical shape styles

- [static let primary: HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle/primary)
- [static let secondary: HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle/secondary)
- [static let tertiary: HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle/tertiary)
- [static let quaternary: HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle/quaternary)

##### Type Properties

- [static let quinary: HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle/quinary)
- [HierarchicalShapeStyleModifier](/documentation/swiftui/hierarchicalshapestylemodifier)
- [ForegroundStyle](/documentation/swiftui/foregroundstyle)

##### Creating a foreground style

- [init()](/documentation/swiftui/foregroundstyle/init())
- [BackgroundStyle](/documentation/swiftui/backgroundstyle)

##### Creating a background style

- [init()](/documentation/swiftui/backgroundstyle/init())
- [SelectionShapeStyle](/documentation/swiftui/selectionshapestyle)

##### Creating a selection shape style

- [init()](/documentation/swiftui/selectionshapestyle/init())
- [SeparatorShapeStyle](/documentation/swiftui/separatorshapestyle)

##### Creating a separator shape style

- [init()](/documentation/swiftui/separatorshapestyle/init())
- [TintShapeStyle](/documentation/swiftui/tintshapestyle)

##### Creating a tint shape style

- [init()](/documentation/swiftui/tintshapestyle/init())
- [FillShapeStyle](/documentation/swiftui/fillshapestyle)

##### Creating the style

- [init()](/documentation/swiftui/fillshapestyle/init())
- [LinkShapeStyle](/documentation/swiftui/linkshapestyle)

##### Creating the style

- [init()](/documentation/swiftui/linkshapestyle/init())
- [PlaceholderTextShapeStyle](/documentation/swiftui/placeholdertextshapestyle)

##### Creating the style

- [init()](/documentation/swiftui/placeholdertextshapestyle/init())
- [WindowBackgroundShapeStyle](/documentation/swiftui/windowbackgroundshapestyle)

##### Creating the style

- [init()](/documentation/swiftui/windowbackgroundshapestyle/init())

#### Instance Methods

- [func materialActiveAppearance(MaterialActiveAppearance) -> some ShapeStyle](/documentation/swiftui/shapestyle/materialactiveappearance(_:))
- [AnyShapeStyle](/documentation/swiftui/anyshapestyle)

#### Creating a shape style

- [init<S>(S)](/documentation/swiftui/anyshapestyle/init(_:))
- [Gradient](/documentation/swiftui/gradient)

#### Creating a gradient from colors

- [init(colors: [Color])](/documentation/swiftui/gradient/init(colors:))

#### Creating a gradient from stops

- [init(stops: [Gradient.Stop])](/documentation/swiftui/gradient/init(stops:))
- [var stops: [Gradient.Stop]](/documentation/swiftui/gradient/stops)
- [Gradient.Stop](/documentation/swiftui/gradient/stop)

##### Creating a gradient stop

- [init(color: Color, location: CGFloat)](/documentation/swiftui/gradient/stop/init(color:location:))

##### Configuring a gradient stop

- [var color: Color](/documentation/swiftui/gradient/stop/color)
- [var location: CGFloat](/documentation/swiftui/gradient/stop/location)

#### Working with color spaces

- [func colorSpace(Gradient.ColorSpace) -> AnyGradient](/documentation/swiftui/gradient/colorspace(_:))
- [Gradient.ColorSpace](/documentation/swiftui/gradient/colorspace)

##### Getting an interpolation method

- [static let device: Gradient.ColorSpace](/documentation/swiftui/gradient/colorspace/device)
- [static let perceptual: Gradient.ColorSpace](/documentation/swiftui/gradient/colorspace/perceptual)
- [MeshGradient](/documentation/swiftui/meshgradient)

#### Structures

- [MeshGradient.BezierPoint](/documentation/swiftui/meshgradient/bezierpoint)

##### Initializers

- [init(position: SIMD2<Float>, leadingControlPoint: SIMD2<Float>, topControlPoint: SIMD2<Float>, trailingControlPoint: SIMD2<Float>, bottomControlPoint: SIMD2<Float>)](/documentation/swiftui/meshgradient/bezierpoint/init(position:leadingcontrolpoint:topcontrolpoint:trailingcontrolpoint:bottomcontrolpoint:))

##### Instance Properties

- [var bottomControlPoint: SIMD2<Float>](/documentation/swiftui/meshgradient/bezierpoint/bottomcontrolpoint)
- [var leadingControlPoint: SIMD2<Float>](/documentation/swiftui/meshgradient/bezierpoint/leadingcontrolpoint)
- [var position: SIMD2<Float>](/documentation/swiftui/meshgradient/bezierpoint/position)
- [var topControlPoint: SIMD2<Float>](/documentation/swiftui/meshgradient/bezierpoint/topcontrolpoint)
- [var trailingControlPoint: SIMD2<Float>](/documentation/swiftui/meshgradient/bezierpoint/trailingcontrolpoint)

#### Initializers

- [init(width: Int, height: Int, bezierPoints: [MeshGradient.BezierPoint], colors: [Color], background: Color, smoothsColors: Bool, colorSpace: Gradient.ColorSpace)](/documentation/swiftui/meshgradient/init(width:height:bezierpoints:colors:background:smoothscolors:colorspace:))
- [init(width: Int, height: Int, bezierPoints: [MeshGradient.BezierPoint], resolvedColors: [Color.Resolved], background: Color, smoothsColors: Bool, colorSpace: Gradient.ColorSpace)](/documentation/swiftui/meshgradient/init(width:height:bezierpoints:resolvedcolors:background:smoothscolors:colorspace:))
- [init(width: Int, height: Int, locations: MeshGradient.Locations, colors: MeshGradient.Colors, background: Color, smoothsColors: Bool, colorSpace: Gradient.ColorSpace)](/documentation/swiftui/meshgradient/init(width:height:locations:colors:background:smoothscolors:colorspace:))
- [init(width: Int, height: Int, points: [SIMD2<Float>], colors: [Color], background: Color, smoothsColors: Bool, colorSpace: Gradient.ColorSpace)](/documentation/swiftui/meshgradient/init(width:height:points:colors:background:smoothscolors:colorspace:))
- [init(width: Int, height: Int, points: [SIMD2<Float>], resolvedColors: [Color.Resolved], background: Color, smoothsColors: Bool, colorSpace: Gradient.ColorSpace)](/documentation/swiftui/meshgradient/init(width:height:points:resolvedcolors:background:smoothscolors:colorspace:))

#### Instance Properties

- [var background: Color](/documentation/swiftui/meshgradient/background)
- [var colorSpace: Gradient.ColorSpace](/documentation/swiftui/meshgradient/colorspace)
- [var colors: MeshGradient.Colors](/documentation/swiftui/meshgradient/colors-swift.property)
- [var height: Int](/documentation/swiftui/meshgradient/height)
- [var locations: MeshGradient.Locations](/documentation/swiftui/meshgradient/locations-swift.property)
- [var smoothsColors: Bool](/documentation/swiftui/meshgradient/smoothscolors)
- [var width: Int](/documentation/swiftui/meshgradient/width)

#### Enumerations

- [MeshGradient.Colors](/documentation/swiftui/meshgradient/colors-swift.enum)

##### Enumeration Cases

- [case colors([Color])](/documentation/swiftui/meshgradient/colors-swift.enum/colors(_:))
- [case resolvedColors([Color.Resolved])](/documentation/swiftui/meshgradient/colors-swift.enum/resolvedcolors(_:))
- [MeshGradient.Locations](/documentation/swiftui/meshgradient/locations-swift.enum)

##### Enumeration Cases

- [case bezierPoints([MeshGradient.BezierPoint])](/documentation/swiftui/meshgradient/locations-swift.enum/bezierpoints(_:))
- [case points([SIMD2<Float>])](/documentation/swiftui/meshgradient/locations-swift.enum/points(_:))
- [AnyGradient](/documentation/swiftui/anygradient)

#### Creating a gradient

- [init(Gradient)](/documentation/swiftui/anygradient/init(_:))

#### Working with color spaces

- [func colorSpace(Gradient.ColorSpace) -> AnyGradient](/documentation/swiftui/anygradient/colorspace(_:))
- [ShadowStyle](/documentation/swiftui/shadowstyle)

#### Getting shadow styles

- [static func drop(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat) -> ShadowStyle](/documentation/swiftui/shadowstyle/drop(color:radius:x:y:))
- [static func inner(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat) -> ShadowStyle](/documentation/swiftui/shadowstyle/inner(color:radius:x:y:))
- [Glass](/documentation/swiftui/glass)

#### Instance Methods

- [func interactive(Bool) -> Glass](/documentation/swiftui/glass/interactive(_:))
- [func tint(Color?) -> Glass](/documentation/swiftui/glass/tint(_:))

#### Type Properties

- [static var clear: Glass](/documentation/swiftui/glass/clear)
- [static var identity: Glass](/documentation/swiftui/glass/identity)
- [static var regular: Glass](/documentation/swiftui/glass/regular)

### Transforming colors

- [func brightness(Double) -> some View](/documentation/swiftui/view/brightness(_:))
- [func contrast(Double) -> some View](/documentation/swiftui/view/contrast(_:))
- [func colorInvert() -> some View](/documentation/swiftui/view/colorinvert())
- [func colorMultiply(Color) -> some View](/documentation/swiftui/view/colormultiply(_:))
- [func saturation(Double) -> some View](/documentation/swiftui/view/saturation(_:))
- [func grayscale(Double) -> some View](/documentation/swiftui/view/grayscale(_:))
- [func hueRotation(Angle) -> some View](/documentation/swiftui/view/huerotation(_:))
- [func luminanceToAlpha() -> some View](/documentation/swiftui/view/luminancetoalpha())
- [func materialActiveAppearance(MaterialActiveAppearance) -> some View](/documentation/swiftui/view/materialactiveappearance(_:))
- [var materialActiveAppearance: MaterialActiveAppearance](/documentation/swiftui/environmentvalues/materialactiveappearance)
- [MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance)

#### Type Properties

- [static let active: MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance/active)
- [static let automatic: MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance/automatic)
- [static let inactive: MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance/inactive)
- [static let matchWindow: MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance/matchwindow)

### Scaling, rotating, or transforming a view

- [func scaledToFill() -> some View](/documentation/swiftui/view/scaledtofill())
- [func scaledToFit() -> some View](/documentation/swiftui/view/scaledtofit())
- [func scaleEffect(_:anchor:)](/documentation/swiftui/view/scaleeffect(_:anchor:))
- [func scaleEffect(_:anchor:)](/documentation/swiftui/view/scaleeffect(_:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, anchor: UnitPoint) -> some View](/documentation/swiftui/view/scaleeffect(x:y:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, z: CGFloat, anchor: UnitPoint3D) -> some View](/documentation/swiftui/view/scaleeffect(x:y:z:anchor:))
- [func aspectRatio(_:contentMode:)](/documentation/swiftui/view/aspectratio(_:contentmode:))
- [func rotationEffect(Angle, anchor: UnitPoint) -> some View](/documentation/swiftui/view/rotationeffect(_:anchor:))
- [func rotation3DEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint, anchorZ: CGFloat, perspective: CGFloat) -> some View](/documentation/swiftui/view/rotation3deffect(_:axis:anchor:anchorz:perspective:))
- [func perspectiveRotationEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint, anchorZ: CGFloat, perspective: CGFloat) -> some View](/documentation/swiftui/view/perspectiverotationeffect(_:axis:anchor:anchorz:perspective:))
- [func rotation3DEffect(Rotation3D, anchor: UnitPoint3D) -> some View](/documentation/swiftui/view/rotation3deffect(_:anchor:))
- [func rotation3DEffect(_:axis:anchor:)](/documentation/swiftui/view/rotation3deffect(_:axis:anchor:))
- [func transformEffect(CGAffineTransform) -> some View](/documentation/swiftui/view/transformeffect(_:))
- [func transform3DEffect(AffineTransform3D) -> some View](/documentation/swiftui/view/transform3deffect(_:))
- [func projectionEffect(ProjectionTransform) -> some View](/documentation/swiftui/view/projectioneffect(_:))
- [ProjectionTransform](/documentation/swiftui/projectiontransform)

#### Creating a transform

- [init()](/documentation/swiftui/projectiontransform/init())
- [init(_:)](/documentation/swiftui/projectiontransform/init(_:))

#### Getting transform characteristics

- [var isAffine: Bool](/documentation/swiftui/projectiontransform/isaffine)
- [var isIdentity: Bool](/documentation/swiftui/projectiontransform/isidentity)

#### Manipulating transforms

- [func invert() -> Bool](/documentation/swiftui/projectiontransform/invert())
- [func inverted() -> ProjectionTransform](/documentation/swiftui/projectiontransform/inverted())
- [func concatenating(ProjectionTransform) -> ProjectionTransform](/documentation/swiftui/projectiontransform/concatenating(_:))

#### Accessing the transform’s coefficients

- [var m11: CGFloat](/documentation/swiftui/projectiontransform/m11)
- [var m12: CGFloat](/documentation/swiftui/projectiontransform/m12)
- [var m13: CGFloat](/documentation/swiftui/projectiontransform/m13)
- [var m21: CGFloat](/documentation/swiftui/projectiontransform/m21)
- [var m22: CGFloat](/documentation/swiftui/projectiontransform/m22)
- [var m23: CGFloat](/documentation/swiftui/projectiontransform/m23)
- [var m31: CGFloat](/documentation/swiftui/projectiontransform/m31)
- [var m32: CGFloat](/documentation/swiftui/projectiontransform/m32)
- [var m33: CGFloat](/documentation/swiftui/projectiontransform/m33)
- [ContentMode](/documentation/swiftui/contentmode)

#### Getting content modes

- [case fill](/documentation/swiftui/contentmode/fill)
- [case fit](/documentation/swiftui/contentmode/fit)

### Masking and clipping

- [func mask<Mask>(alignment: Alignment, () -> Mask) -> some View](/documentation/swiftui/view/mask(alignment:_:))
- [func clipped(antialiased: Bool) -> some View](/documentation/swiftui/view/clipped(antialiased:))
- [func clipShape<S>(S, style: FillStyle) -> some View](/documentation/swiftui/view/clipshape(_:style:))

### Applying blur and shadows

- [func blur(radius: CGFloat, opaque: Bool) -> some View](/documentation/swiftui/view/blur(radius:opaque:))
- [func shadow(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/shadow(color:radius:x:y:))
- [ColorMatrix](/documentation/swiftui/colormatrix)

#### Creating an identity matrix

- [init()](/documentation/swiftui/colormatrix/init())

#### First column

- [var r1: Float](/documentation/swiftui/colormatrix/r1)
- [var g1: Float](/documentation/swiftui/colormatrix/g1)
- [var b1: Float](/documentation/swiftui/colormatrix/b1)
- [var a1: Float](/documentation/swiftui/colormatrix/a1)

#### Second column

- [var r2: Float](/documentation/swiftui/colormatrix/r2)
- [var g2: Float](/documentation/swiftui/colormatrix/g2)
- [var b2: Float](/documentation/swiftui/colormatrix/b2)
- [var a2: Float](/documentation/swiftui/colormatrix/a2)

#### Third column

- [var r3: Float](/documentation/swiftui/colormatrix/r3)
- [var g3: Float](/documentation/swiftui/colormatrix/g3)
- [var b3: Float](/documentation/swiftui/colormatrix/b3)
- [var a3: Float](/documentation/swiftui/colormatrix/a3)

#### Fourth column

- [var r4: Float](/documentation/swiftui/colormatrix/r4)
- [var g4: Float](/documentation/swiftui/colormatrix/g4)
- [var b4: Float](/documentation/swiftui/colormatrix/b4)
- [var a4: Float](/documentation/swiftui/colormatrix/a4)

#### Fifth column

- [var r5: Float](/documentation/swiftui/colormatrix/r5)
- [var g5: Float](/documentation/swiftui/colormatrix/g5)
- [var b5: Float](/documentation/swiftui/colormatrix/b5)
- [var a5: Float](/documentation/swiftui/colormatrix/a5)

### Applying effects based on geometry

- [func visualEffect((EmptyVisualEffect, GeometryProxy) -> some VisualEffect) -> some View](/documentation/swiftui/view/visualeffect(_:))
- [func visualEffect3D((EmptyVisualEffect, GeometryProxy3D) -> some VisualEffect) -> some View](/documentation/swiftui/view/visualeffect3d(_:))
- [VisualEffect](/documentation/swiftui/visualeffect)

#### Adjusting Color

- [func brightness(Double) -> some VisualEffect](/documentation/swiftui/visualeffect/brightness(_:))
- [func colorEffect(Shader, isEnabled: Bool) -> some VisualEffect](/documentation/swiftui/visualeffect/coloreffect(_:isenabled:))
- [func contrast(Double) -> some VisualEffect](/documentation/swiftui/visualeffect/contrast(_:))
- [func grayscale(Double) -> some VisualEffect](/documentation/swiftui/visualeffect/grayscale(_:))
- [func hueRotation(Angle) -> some VisualEffect](/documentation/swiftui/visualeffect/huerotation(_:))
- [func saturation(Double) -> some VisualEffect](/documentation/swiftui/visualeffect/saturation(_:))
- [func opacity(Double) -> some VisualEffect](/documentation/swiftui/visualeffect/opacity(_:))

#### Scaling

- [func scaleEffect(_:anchor:)](/documentation/swiftui/visualeffect/scaleeffect(_:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, anchor: UnitPoint) -> some VisualEffect](/documentation/swiftui/visualeffect/scaleeffect(x:y:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, z: CGFloat, anchor: UnitPoint3D) -> some VisualEffect](/documentation/swiftui/visualeffect/scaleeffect(x:y:z:anchor:))

#### Rotating

- [func rotationEffect(Angle, anchor: UnitPoint) -> some VisualEffect](/documentation/swiftui/visualeffect/rotationeffect(_:anchor:))
- [func rotation3DEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint, anchorZ: CGFloat, perspective: CGFloat) -> some VisualEffect](/documentation/swiftui/visualeffect/rotation3deffect(_:axis:anchor:anchorz:perspective:))
- [func perspectiveRotationEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint3D, perspective: CGFloat) -> some VisualEffect](/documentation/swiftui/visualeffect/perspectiverotationeffect(_:axis:anchor:perspective:))
- [func rotation3DEffect(Rotation3D, anchor: UnitPoint3D) -> some VisualEffect](/documentation/swiftui/visualeffect/rotation3deffect(_:anchor:))
- [func rotation3DEffect(_:axis:anchor:)](/documentation/swiftui/visualeffect/rotation3deffect(_:axis:anchor:))

#### Translating

- [func offset(CGSize) -> some VisualEffect](/documentation/swiftui/visualeffect/offset(_:))
- [func offset(x: CGFloat, y: CGFloat) -> some VisualEffect](/documentation/swiftui/visualeffect/offset(x:y:))
- [func offset(z: CGFloat) -> some VisualEffect](/documentation/swiftui/visualeffect/offset(z:))

#### Applying a transform

- [func transform3DEffect(AffineTransform3D) -> some VisualEffect](/documentation/swiftui/visualeffect/transform3deffect(_:))
- [func transformEffect(_:)](/documentation/swiftui/visualeffect/transformeffect(_:))

#### Applying other effects

- [func blur(radius: CGFloat, opaque: Bool) -> some VisualEffect](/documentation/swiftui/visualeffect/blur(radius:opaque:))
- [func distortionEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some VisualEffect](/documentation/swiftui/visualeffect/distortioneffect(_:maxsampleoffset:isenabled:))
- [func layerEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some VisualEffect](/documentation/swiftui/visualeffect/layereffect(_:maxsampleoffset:isenabled:))

#### Instance Methods

- [func blendMode(BlendMode) -> some VisualEffect](/documentation/swiftui/visualeffect/blendmode(_:))
- [EmptyVisualEffect](/documentation/swiftui/emptyvisualeffect)

#### Creating an empty visual effect

- [init()](/documentation/swiftui/emptyvisualeffect/init())

### Compositing views

- [func blendMode(BlendMode) -> some View](/documentation/swiftui/view/blendmode(_:))
- [func compositingGroup() -> some View](/documentation/swiftui/view/compositinggroup())
- [func drawingGroup(opaque: Bool, colorMode: ColorRenderingMode) -> some View](/documentation/swiftui/view/drawinggroup(opaque:colormode:))
- [BlendMode](/documentation/swiftui/blendmode)

#### Getting the default

- [case normal](/documentation/swiftui/blendmode/normal)

#### Darkening

- [case darken](/documentation/swiftui/blendmode/darken)
- [case multiply](/documentation/swiftui/blendmode/multiply)
- [case colorBurn](/documentation/swiftui/blendmode/colorburn)
- [case plusDarker](/documentation/swiftui/blendmode/plusdarker)

#### Lightening

- [case lighten](/documentation/swiftui/blendmode/lighten)
- [case screen](/documentation/swiftui/blendmode/screen)
- [case colorDodge](/documentation/swiftui/blendmode/colordodge)
- [case plusLighter](/documentation/swiftui/blendmode/pluslighter)

#### Adding contrast

- [case overlay](/documentation/swiftui/blendmode/overlay)
- [case softLight](/documentation/swiftui/blendmode/softlight)
- [case hardLight](/documentation/swiftui/blendmode/hardlight)

#### Inverting

- [case difference](/documentation/swiftui/blendmode/difference)
- [case exclusion](/documentation/swiftui/blendmode/exclusion)

#### Mixing color components

- [case hue](/documentation/swiftui/blendmode/hue)
- [case saturation](/documentation/swiftui/blendmode/saturation)
- [case color](/documentation/swiftui/blendmode/color)
- [case luminosity](/documentation/swiftui/blendmode/luminosity)

#### Accessing Porter-Duff modes

- [case sourceAtop](/documentation/swiftui/blendmode/sourceatop)
- [case destinationOver](/documentation/swiftui/blendmode/destinationover)
- [case destinationOut](/documentation/swiftui/blendmode/destinationout)
- [ColorRenderingMode](/documentation/swiftui/colorrenderingmode)

#### Getting rendering modes

- [case extendedLinear](/documentation/swiftui/colorrenderingmode/extendedlinear)
- [case linear](/documentation/swiftui/colorrenderingmode/linear)
- [case nonLinear](/documentation/swiftui/colorrenderingmode/nonlinear)
- [CompositorContent](/documentation/swiftui/compositorcontent)

#### Associated Types

- [Body](/documentation/swiftui/compositorcontent/body-swift.associatedtype)

#### Instance Properties

- [var body: Self.Body](/documentation/swiftui/compositorcontent/body-swift.property)

#### Instance Methods

- [func contentCaptureProtected(Bool) -> some CompositorContent](/documentation/swiftui/compositorcontent/contentcaptureprotected(_:))
- [func onAppear(perform: (() -> Void)?) -> some CompositorContent](/documentation/swiftui/compositorcontent/onappear(perform:))
- [func onChange(of:initial:_:)](/documentation/swiftui/compositorcontent/onchange(of:initial:_:))
- [func onDisappear(perform: (() -> Void)?) -> some CompositorContent](/documentation/swiftui/compositorcontent/ondisappear(perform:))
- [func onImmersionChange(initial: Bool, (ImmersionChangeContext, ImmersionChangeContext) -> Void) -> some CompositorContent](/documentation/swiftui/compositorcontent/onimmersionchange(initial:_:))
- [func onWorldRecenter(action:)](/documentation/swiftui/compositorcontent/onworldrecenter(action:))
- [func persistentSystemOverlays(Visibility) -> some CompositorContent](/documentation/swiftui/compositorcontent/persistentsystemoverlays(_:))
- [func preferredSurroundingsEffect(SurroundingsEffect?) -> some CompositorContent](/documentation/swiftui/compositorcontent/preferredsurroundingseffect(_:))
- [func upperLimbVisibility(Visibility) -> some CompositorContent](/documentation/swiftui/compositorcontent/upperlimbvisibility(_:))
- [CompositorContentBuilder](/documentation/swiftui/compositorcontentbuilder)

#### Structures

- [CompositorContentBuilder.Content](/documentation/swiftui/compositorcontentbuilder/content)

#### Type Methods

- [static func buildBlock<C>(C) -> C](/documentation/swiftui/compositorcontentbuilder/buildblock(_:))
- [static buildEither(first:)](/documentation/swiftui/compositorcontentbuilder/buildeither(first:))
- [static func buildEither<F>(second: F) -> _ConditionalContent<_LimitedAvailabilityCompositorContent, F>](/documentation/swiftui/compositorcontentbuilder/buildeither(second:))
- [static func buildExpression<C>(C) -> C](/documentation/swiftui/compositorcontentbuilder/buildexpression(_:))
- [static func buildLimitedAvailability(some CompositorContent) -> _LimitedAvailabilityCompositorContent](/documentation/swiftui/compositorcontentbuilder/buildlimitedavailability(_:))
- [AnyCompositorContent](/documentation/swiftui/anycompositorcontent)

#### Initializers

- [init<T>(T)](/documentation/swiftui/anycompositorcontent/init(_:))
- [init<T>(erasing: T)](/documentation/swiftui/anycompositorcontent/init(erasing:))

### Measuring a view

- [GeometryReader](/documentation/swiftui/geometryreader)

#### Creating a geometry reader

- [init(content: (GeometryProxy) -> Content)](/documentation/swiftui/geometryreader/init(content:))
- [var content: (GeometryProxy) -> Content](/documentation/swiftui/geometryreader/content)
- [GeometryReader3D](/documentation/swiftui/geometryreader3d)

#### Creating a geometry reader

- [init(content: (GeometryProxy3D) -> Content)](/documentation/swiftui/geometryreader3d/init(content:))
- [var content: (GeometryProxy3D) -> Content](/documentation/swiftui/geometryreader3d/content)
- [GeometryProxy](/documentation/swiftui/geometryproxy)

#### Accessing geometry characteristics

- [func bounds(of: NamedCoordinateSpace) -> CGRect?](/documentation/swiftui/geometryproxy/bounds(of:))
- [func frame(in:)](/documentation/swiftui/geometryproxy/frame(in:))
- [var size: CGSize](/documentation/swiftui/geometryproxy/size)
- [var safeAreaInsets: EdgeInsets](/documentation/swiftui/geometryproxy/safeareainsets)
- [subscript<T>(Anchor<T>) -> T](/documentation/swiftui/geometryproxy/subscript(_:))
- [func transform(in: some CoordinateSpaceProtocol) -> AffineTransform3D?](/documentation/swiftui/geometryproxy/transform(in:))

#### Instance Properties

- [var containerCornerInsets: RectangleCornerInsets](/documentation/swiftui/geometryproxy/containercornerinsets)
- [GeometryProxy3D](/documentation/swiftui/geometryproxy3d)

#### Accessing geometry characteristics

- [func frame(in: some CoordinateSpaceProtocol) -> Rect3D](/documentation/swiftui/geometryproxy3d/frame(in:))
- [var size: Size3D](/documentation/swiftui/geometryproxy3d/size)
- [var safeAreaInsets: EdgeInsets3D](/documentation/swiftui/geometryproxy3d/safeareainsets)
- [subscript<T>(Anchor<T>) -> T](/documentation/swiftui/geometryproxy3d/subscript(_:))
- [func transform(in: some CoordinateSpaceProtocol) -> AffineTransform3D?](/documentation/swiftui/geometryproxy3d/transform(in:))

#### Instance Methods

- [func coordinateSpace3D(for: any CoordinateSpaceProtocol) -> GeometryProxyCoordinateSpace3D](/documentation/swiftui/geometryproxy3d/coordinatespace3d(for:))
- [func coordinateSpace(NamedCoordinateSpace) -> some View](/documentation/swiftui/view/coordinatespace(_:))
- [CoordinateSpace](/documentation/swiftui/coordinatespace)

#### Getting coordinate spaces

- [case global](/documentation/swiftui/coordinatespace/global)
- [case local](/documentation/swiftui/coordinatespace/local)
- [case named(AnyHashable)](/documentation/swiftui/coordinatespace/named(_:))

#### Testing a space

- [var isGlobal: Bool](/documentation/swiftui/coordinatespace/isglobal)
- [var isLocal: Bool](/documentation/swiftui/coordinatespace/islocal)
- [CoordinateSpaceProtocol](/documentation/swiftui/coordinatespaceprotocol)

#### Getting built-in coordinate spaces

- [static var immersiveSpace: NamedCoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/immersivespace)
- [static var global: GlobalCoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/global)
- [static var local: LocalCoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/local)
- [static func named(some Hashable) -> NamedCoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/named(_:))
- [static var scrollView: NamedCoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/scrollview)
- [static func scrollView(axis: Axis) -> Self](/documentation/swiftui/coordinatespaceprotocol/scrollview(axis:))

#### Getting the resolved coordinate space

- [var coordinateSpace: CoordinateSpace](/documentation/swiftui/coordinatespaceprotocol/coordinatespace)

#### Supporting types

- [GlobalCoordinateSpace](/documentation/swiftui/globalcoordinatespace)

##### Creating the coordinate space

- [init()](/documentation/swiftui/globalcoordinatespace/init())
- [LocalCoordinateSpace](/documentation/swiftui/localcoordinatespace)

##### Creating the coordinate space

- [init()](/documentation/swiftui/localcoordinatespace/init())
- [NamedCoordinateSpace](/documentation/swiftui/namedcoordinatespace)
- [PhysicalMetric](/documentation/swiftui/physicalmetric)

#### Creating a metric

- [init(wrappedValue:from:)](/documentation/swiftui/physicalmetric/init(wrappedvalue:from:))

#### Getting the value

- [var wrappedValue: Value](/documentation/swiftui/physicalmetric/wrappedvalue)
- [PhysicalMetricsConverter](/documentation/swiftui/physicalmetricsconverter)

#### Converting a unit length

- [func convert(_:from:)](/documentation/swiftui/physicalmetricsconverter/convert(_:from:))
- [func convert(_:to:)](/documentation/swiftui/physicalmetricsconverter/convert(_:to:))

#### Instance Properties

- [var worldScalingCompensation: WorldScalingCompensation](/documentation/swiftui/physicalmetricsconverter/worldscalingcompensation)

#### Instance Methods

- [func worldScalingCompensation(WorldScalingCompensation) -> PhysicalMetricsConverter](/documentation/swiftui/physicalmetricsconverter/worldscalingcompensation(_:))

### Responding to a geometry change

- [func onGeometryChange(for:of:action:)](/documentation/swiftui/view/ongeometrychange(for:of:action:))

### Accessing Metal shaders

- [func colorEffect(Shader, isEnabled: Bool) -> some View](/documentation/swiftui/view/coloreffect(_:isenabled:))
- [func distortionEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some View](/documentation/swiftui/view/distortioneffect(_:maxsampleoffset:isenabled:))
- [func layerEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some View](/documentation/swiftui/view/layereffect(_:maxsampleoffset:isenabled:))
- [Shader](/documentation/swiftui/shader)

#### Creating a shader

- [init(function: ShaderFunction, arguments: [Shader.Argument])](/documentation/swiftui/shader/init(function:arguments:))
- [Shader.Argument](/documentation/swiftui/shader/argument)

##### Creating argument values

- [static var boundingRect: Shader.Argument](/documentation/swiftui/shader/argument/boundingrect)
- [static func color(Color) -> Shader.Argument](/documentation/swiftui/shader/argument/color(_:))
- [static func colorArray([Color]) -> Shader.Argument](/documentation/swiftui/shader/argument/colorarray(_:))
- [static func data(Data) -> Shader.Argument](/documentation/swiftui/shader/argument/data(_:))
- [static func float<T>(T) -> Shader.Argument](/documentation/swiftui/shader/argument/float(_:))
- [static float2(_:)](/documentation/swiftui/shader/argument/float2(_:))
- [static func float2<T>(T, T) -> Shader.Argument](/documentation/swiftui/shader/argument/float2(_:_:))
- [static func float3<T>(T, T, T) -> Shader.Argument](/documentation/swiftui/shader/argument/float3(_:_:_:))
- [static func float4<T>(T, T, T, T) -> Shader.Argument](/documentation/swiftui/shader/argument/float4(_:_:_:_:))
- [static func floatArray([Float]) -> Shader.Argument](/documentation/swiftui/shader/argument/floatarray(_:))
- [static func image(Image) -> Shader.Argument](/documentation/swiftui/shader/argument/image(_:))

#### Getting the shader function

- [var function: ShaderFunction](/documentation/swiftui/shader/function)
- [var arguments: [Shader.Argument]](/documentation/swiftui/shader/arguments)

#### Configuring the shader

- [var dithersColor: Bool](/documentation/swiftui/shader/ditherscolor)

#### Structures

- [Shader.UsageType](/documentation/swiftui/shader/usagetype)

##### Type Properties

- [static let colorEffect: Shader.UsageType](/documentation/swiftui/shader/usagetype/coloreffect)
- [static let distortionEffect: Shader.UsageType](/documentation/swiftui/shader/usagetype/distortioneffect)
- [static let layerEffect: Shader.UsageType](/documentation/swiftui/shader/usagetype/layereffect)
- [static let shapeStyle: Shader.UsageType](/documentation/swiftui/shader/usagetype/shapestyle)

#### Instance Methods

- [func compile(as: Shader.UsageType) async throws](/documentation/swiftui/shader/compile(as:))
- [ShaderFunction](/documentation/swiftui/shaderfunction)

#### Creating a shader function

- [init(library: ShaderLibrary, name: String)](/documentation/swiftui/shaderfunction/init(library:name:))

#### Configuring a function

- [var library: ShaderLibrary](/documentation/swiftui/shaderfunction/library)
- [var name: String](/documentation/swiftui/shaderfunction/name)
- [func dynamicallyCall(withArguments: [Shader.Argument]) -> Shader](/documentation/swiftui/shaderfunction/dynamicallycall(witharguments:))
- [ShaderLibrary](/documentation/swiftui/shaderlibrary)

#### Getting the default shader library

- [static let `default`: ShaderLibrary](/documentation/swiftui/shaderlibrary/default)
- [static func bundle(Bundle) -> ShaderLibrary](/documentation/swiftui/shaderlibrary/bundle(_:))

#### Creating a shader library

- [init(url: URL)](/documentation/swiftui/shaderlibrary/init(url:))
- [init(data: Data)](/documentation/swiftui/shaderlibrary/init(data:))

#### Access shader functions

- [static subscript(dynamicMember _: String) -> ShaderFunction](/documentation/swiftui/shaderlibrary/subscript(dynamicmember:)-swift.type.subscript)

#### Subscripts

- [subscript(dynamicMember _: String) -> ShaderFunction](/documentation/swiftui/shaderlibrary/subscript(dynamicmember:)-swift.subscript)

### Accessing geometric constructs

- [Axis](/documentation/swiftui/axis)

#### Getting axes

- [case horizontal](/documentation/swiftui/axis/horizontal)
- [case vertical](/documentation/swiftui/axis/vertical)

#### Getting all axes

- [Axis.Set](/documentation/swiftui/axis/set)

##### Getting axis sets

- [static let horizontal: Axis.Set](/documentation/swiftui/axis/set/horizontal)
- [static let vertical: Axis.Set](/documentation/swiftui/axis/set/vertical)
- [Angle](/documentation/swiftui/angle)

#### Getting constant angles

- [static var zero: Angle](/documentation/swiftui/angle/zero)
- [static func degrees(Double) -> Angle](/documentation/swiftui/angle/degrees(_:))
- [static func radians(Double) -> Angle](/documentation/swiftui/angle/radians(_:))

#### Creating an angle

- [init()](/documentation/swiftui/angle/init())
- [init(degrees: Double)](/documentation/swiftui/angle/init(degrees:))
- [init(radians: Double)](/documentation/swiftui/angle/init(radians:))
- [init(Angle2D)](/documentation/swiftui/angle/init(_:))

#### Getting the angle size

- [var degrees: Double](/documentation/swiftui/angle/degrees)
- [var radians: Double](/documentation/swiftui/angle/radians)
- [UnitPoint](/documentation/swiftui/unitpoint)

#### Getting the origin

- [static let zero: UnitPoint](/documentation/swiftui/unitpoint/zero)

#### Getting top points

- [static let topLeading: UnitPoint](/documentation/swiftui/unitpoint/topleading)
- [static let top: UnitPoint](/documentation/swiftui/unitpoint/top)
- [static let topTrailing: UnitPoint](/documentation/swiftui/unitpoint/toptrailing)

#### Getting middle points

- [static let leading: UnitPoint](/documentation/swiftui/unitpoint/leading)
- [static let center: UnitPoint](/documentation/swiftui/unitpoint/center)
- [static let trailing: UnitPoint](/documentation/swiftui/unitpoint/trailing)

#### Getting bottom points

- [static let bottomLeading: UnitPoint](/documentation/swiftui/unitpoint/bottomleading)
- [static let bottom: UnitPoint](/documentation/swiftui/unitpoint/bottom)
- [static let bottomTrailing: UnitPoint](/documentation/swiftui/unitpoint/bottomtrailing)

#### Creating a point

- [init()](/documentation/swiftui/unitpoint/init())
- [init(x: CGFloat, y: CGFloat)](/documentation/swiftui/unitpoint/init(x:y:))

#### Getting the point’s coordinates

- [var x: CGFloat](/documentation/swiftui/unitpoint/x)
- [var y: CGFloat](/documentation/swiftui/unitpoint/y)
- [UnitPoint3D](/documentation/swiftui/unitpoint3d)

#### Getting the origin

- [static let origin: UnitPoint3D](/documentation/swiftui/unitpoint3d/origin)
- [static let zero: UnitPoint3D](/documentation/swiftui/unitpoint3d/zero)

#### Getting top points

- [static let topLeadingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/topleadingback)
- [static let topLeading: UnitPoint3D](/documentation/swiftui/unitpoint3d/topleading)
- [static let topLeadingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/topleadingfront)
- [static let topBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/topback)
- [static let top: UnitPoint3D](/documentation/swiftui/unitpoint3d/top)
- [static let topFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/topfront)
- [static let topTrailingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/toptrailingback)
- [static let topTrailing: UnitPoint3D](/documentation/swiftui/unitpoint3d/toptrailing)
- [static let topTrailingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/toptrailingfront)

#### Getting middle points

- [static let leadingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/leadingback)
- [static let leading: UnitPoint3D](/documentation/swiftui/unitpoint3d/leading)
- [static let leadingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/leadingfront)
- [static let back: UnitPoint3D](/documentation/swiftui/unitpoint3d/back)
- [static let center: UnitPoint3D](/documentation/swiftui/unitpoint3d/center)
- [static let front: UnitPoint3D](/documentation/swiftui/unitpoint3d/front)
- [static let trailingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/trailingback)
- [static let trailing: UnitPoint3D](/documentation/swiftui/unitpoint3d/trailing)
- [static let trailingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/trailingfront)

#### Getting bottom points

- [static let bottomLeadingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomleadingback)
- [static let bottomLeading: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomleading)
- [static let bottomLeadingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomleadingfront)
- [static let bottomBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomback)
- [static let bottom: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottom)
- [static let bottomFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomfront)
- [static let bottomTrailingBack: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomtrailingback)
- [static let bottomTrailing: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomtrailing)
- [static let bottomTrailingFront: UnitPoint3D](/documentation/swiftui/unitpoint3d/bottomtrailingfront)

#### Creating a point

- [init()](/documentation/swiftui/unitpoint3d/init())
- [init(x: CGFloat, y: CGFloat, z: CGFloat)](/documentation/swiftui/unitpoint3d/init(x:y:z:))

#### Getting the point’s coordinates

- [var x: CGFloat](/documentation/swiftui/unitpoint3d/x)
- [var y: CGFloat](/documentation/swiftui/unitpoint3d/y)
- [var z: CGFloat](/documentation/swiftui/unitpoint3d/z)
- [Anchor](/documentation/swiftui/anchor)

#### Getting the anchor’s source

- [Anchor.Source](/documentation/swiftui/anchor/source)

##### Getting point anchor sources

- [static point(_:)](/documentation/swiftui/anchor/source/point(_:))
- [static unitPoint(_:)](/documentation/swiftui/anchor/source/unitpoint(_:))

##### Getting rectangle anchor sources

- [static func rect(CGRect) -> Anchor<Value>.Source](/documentation/swiftui/anchor/source/rect(_:))
- [static var bounds: Anchor<CGRect>.Source](/documentation/swiftui/anchor/source/bounds)

##### Getting top anchor sources

- [static var topLeading: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/topleading)
- [static var top: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/top)
- [static var topTrailing: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/toptrailing)

##### Getting middle anchor sources

- [static var leading: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/leading)
- [static var center: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/center-869al)
- [static var trailing: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/trailing)

##### Getting bottom anchor sources

- [static var bottomTrailing: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/bottomtrailing)
- [static var bottom: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/bottom)
- [static var bottomLeading: Anchor<CGPoint>.Source](/documentation/swiftui/anchor/source/bottomleading)

##### Creating an anchor source

- [init(_:)](/documentation/swiftui/anchor/source/init(_:))

##### Type Properties

- [static var bounds3D: Anchor<Rect3D>.Source](/documentation/swiftui/anchor/source/bounds3d)
- [static var center: Anchor<Point3D>.Source](/documentation/swiftui/anchor/source/center-6w6ww)
- [static var center3D: Anchor<Point3D>.Source](/documentation/swiftui/anchor/source/center3d)

##### Type Methods

- [static func point3D(Point3D) -> Anchor<Value>.Source](/documentation/swiftui/anchor/source/point3d(_:))
- [static func rect3D(Rect3D) -> Anchor<Value>.Source](/documentation/swiftui/anchor/source/rect3d(_:))
- [static func unitPoint3D(UnitPoint3D) -> Anchor<Value>.Source](/documentation/swiftui/anchor/source/unitpoint3d(_:))
- [DepthAlignmentID](/documentation/swiftui/depthalignmentid)

#### Type Methods

- [static func defaultValue(in: ViewDimensions3D) -> CGFloat](/documentation/swiftui/depthalignmentid/defaultvalue(in:))
- [Alignment3D](/documentation/swiftui/alignment3d)

#### Initializers

- [init(horizontal: HorizontalAlignment, vertical: VerticalAlignment, depth: DepthAlignment)](/documentation/swiftui/alignment3d/init(horizontal:vertical:depth:))

#### Instance Properties

- [var depth: DepthAlignment](/documentation/swiftui/alignment3d/depth)
- [var horizontal: HorizontalAlignment](/documentation/swiftui/alignment3d/horizontal)
- [var vertical: VerticalAlignment](/documentation/swiftui/alignment3d/vertical)

#### Type Properties

- [static let back: Alignment3D](/documentation/swiftui/alignment3d/back)
- [static let bottom: Alignment3D](/documentation/swiftui/alignment3d/bottom)
- [static let bottomBack: Alignment3D](/documentation/swiftui/alignment3d/bottomback)
- [static let bottomFront: Alignment3D](/documentation/swiftui/alignment3d/bottomfront)
- [static let bottomLeading: Alignment3D](/documentation/swiftui/alignment3d/bottomleading)
- [static let bottomLeadingBack: Alignment3D](/documentation/swiftui/alignment3d/bottomleadingback)
- [static let bottomLeadingFront: Alignment3D](/documentation/swiftui/alignment3d/bottomleadingfront)
- [static let bottomTrailing: Alignment3D](/documentation/swiftui/alignment3d/bottomtrailing)
- [static let bottomTrailingBack: Alignment3D](/documentation/swiftui/alignment3d/bottomtrailingback)
- [static let bottomTrailingFront: Alignment3D](/documentation/swiftui/alignment3d/bottomtrailingfront)
- [static let center: Alignment3D](/documentation/swiftui/alignment3d/center)
- [static let front: Alignment3D](/documentation/swiftui/alignment3d/front)
- [static let leading: Alignment3D](/documentation/swiftui/alignment3d/leading)
- [static let leadingBack: Alignment3D](/documentation/swiftui/alignment3d/leadingback)
- [static let leadingFront: Alignment3D](/documentation/swiftui/alignment3d/leadingfront)
- [static let top: Alignment3D](/documentation/swiftui/alignment3d/top)
- [static let topBack: Alignment3D](/documentation/swiftui/alignment3d/topback)
- [static let topFront: Alignment3D](/documentation/swiftui/alignment3d/topfront)
- [static let topLeading: Alignment3D](/documentation/swiftui/alignment3d/topleading)
- [static let topLeadingBack: Alignment3D](/documentation/swiftui/alignment3d/topleadingback)
- [static let topLeadingFront: Alignment3D](/documentation/swiftui/alignment3d/topleadingfront)
- [static let topTrailing: Alignment3D](/documentation/swiftui/alignment3d/toptrailing)
- [static let topTrailingBack: Alignment3D](/documentation/swiftui/alignment3d/toptrailingback)
- [static let topTrailingFront: Alignment3D](/documentation/swiftui/alignment3d/toptrailingfront)
- [static let trailing: Alignment3D](/documentation/swiftui/alignment3d/trailing)
- [static let trailingBack: Alignment3D](/documentation/swiftui/alignment3d/trailingback)
- [static let trailingFront: Alignment3D](/documentation/swiftui/alignment3d/trailingfront)
- [GeometryProxyCoordinateSpace3D](/documentation/swiftui/geometryproxycoordinatespace3d)

#### Instance Methods

- [func anchored(in: UnitPoint3D) -> some CoordinateSpace3D](/documentation/swiftui/geometryproxycoordinatespace3d/anchored(in:))

