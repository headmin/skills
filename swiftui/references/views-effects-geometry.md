# Views: Effects and Geometry — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Controlling text style](#controlling-text-style)
- [Managing text layout](#managing-text-layout)
- [Rendering text](#rendering-text)
- [Limiting line count](#limiting-line-count-for-multiline-text)
- [Formatting multiline text](#formatting-multiline-text)
- [Formatting date and time](#formatting-date-and-time)
- [Managing text entry](#managing-text-entry)
- [Dictating text](#dictating-text)
- [Writing Tools behavior](#configuring-the-writing-tools-behavior)
- [Specifying text equivalents](#specifying-text-equivalents)
- [Localizing text](#localizing-text)
- [Images](#creating-an-image)
- [Loading images async](#loading-images-asynchronously)
- [Symbol variants & effects](#setting-a-symbol-variant)
- [Symbol rendering modes](#setting-symbol-rendering-modes)
- [Rendering images from views](#rendering-images-from-views)
- [Buttons](#creating-buttons)
- [Special-purpose buttons](#creating-special-purpose-buttons)
- [Links](#linking-to-other-content)
- [Numeric inputs](#getting-numeric-inputs)
- [Pickers](#choosing-from-a-set-of-options)
- [Date pickers](#choosing-dates)
- [Color picker](#choosing-a-color)
- [Gauges & progress](#indicating-a-value)
- [Missing content](#indicating-missing-content)
- [Haptic feedback](#providing-haptic-feedback)
- [Sizing controls](#sizing-controls)
- [Menus & commands](#creating-a-menu)
- [Shapes](#creating-rectangular-shapes)
- [Drawing custom shapes](#drawing-custom-shapes)
- [Shape behavior](#defining-shape-behavior)
- [Canvas & GraphicsContext](#immediate-mode-drawing)
- [Color](#setting-a-color)
- [Styling content](#styling-content)
- [Transforming colors](#transforming-colors)
- [Scaling, rotating, transforming](#scaling-rotating-or-transforming-a-view)
- [Masking and clipping](#masking-and-clipping)
- [Blur and shadows](#applying-blur-and-shadows)
- [Effects based on geometry](#applying-effects-based-on-geometry)
- [Compositing views](#compositing-views)
- [Measuring a view](#measuring-a-view)
- [Geometry change](#responding-to-a-geometry-change)
- [Metal shaders](#accessing-metal-shaders)
- [Geometric constructs](#accessing-geometric-constructs)

---

- [DynamicTypeSize](/documentation/swiftui/dynamictypesize) — enum: xSmall, small, medium, large, xLarge, xxLarge, xxxLarge, accessibility1-5; `isAccessibilitySize`
- [ScaledMetric](/documentation/swiftui/scaledmetric) — property wrapper that scales a numeric value relative to Dynamic Type
- [TextVariantPreference](/documentation/swiftui/textvariantpreference) — values: `.fixed`, `.sizeDependent`

### Controlling text style

- [func bold(Bool) -> some View](/documentation/swiftui/view/bold(_:))
- [func italic(Bool) -> some View](/documentation/swiftui/view/italic(_:))
- [func underline(Bool, pattern:, color:) -> some View](/documentation/swiftui/view/underline(_:pattern:color:))
- [func strikethrough(Bool, pattern:, color:) -> some View](/documentation/swiftui/view/strikethrough(_:pattern:color:))
- [func textCase(Text.Case?) -> some View](/documentation/swiftui/view/textcase(_:))
- [func monospaced(Bool) -> some View](/documentation/swiftui/view/monospaced(_:))
- [func monospacedDigit() -> some View](/documentation/swiftui/view/monospaceddigit())
- [AttributedTextFormattingDefinition](/documentation/swiftui/attributedtextformattingdefinition) — protocol for attributed text formatting
- [AttributedTextValueConstraint](/documentation/swiftui/attributedtextvalueconstraint) — protocol for constraining attribute values
- [AttributedTextFormatting](/documentation/swiftui/attributedtextformatting) — namespace with AnyDefinition, AttributeContainerProxy, DefinitionBuilder, EmptyDefinition, Transferable, TupleDefinition, ValueConstraint

### Managing text layout

- [func truncationMode(Text.TruncationMode) -> some View](/documentation/swiftui/view/truncationmode(_:))
- [func allowsTightening(Bool) -> some View](/documentation/swiftui/view/allowstightening(_:))
- [func minimumScaleFactor(CGFloat) -> some View](/documentation/swiftui/view/minimumscalefactor(_:))
- [func baselineOffset(CGFloat) -> some View](/documentation/swiftui/view/baselineoffset(_:))
- [func kerning(CGFloat) -> some View](/documentation/swiftui/view/kerning(_:))
- [func tracking(CGFloat) -> some View](/documentation/swiftui/view/tracking(_:))
- [func flipsForRightToLeftLayoutDirection(Bool) -> some View](/documentation/swiftui/view/flipsforrighttoleftlayoutdirection(_:))
- [TextAlignment](/documentation/swiftui/textalignment) — enum: center, leading, trailing

### Rendering text

- [Creating visual effects with SwiftUI](/documentation/swiftui/creating-visual-effects-with-swiftui) (article)
- [TextAttribute](/documentation/swiftui/textattribute) — protocol for custom text attributes
- [func textRenderer<T>(T) -> some View](/documentation/swiftui/view/textrenderer(_:))
- [TextRenderer](/documentation/swiftui/textrenderer) — protocol: `draw(layout:in:)`, `sizeThatFits(proposal:text:)`, `displayPadding`
- [TextProxy](/documentation/swiftui/textproxy) — proxy for measuring rendered text

### Limiting line count for multiline text

- [func lineLimit(_:)](/documentation/swiftui/view/linelimit(_:))
- [func lineLimit(Int, reservesSpace: Bool) -> some View](/documentation/swiftui/view/linelimit(_:reservesspace:))

### Formatting multiline text

- [func lineSpacing(CGFloat) -> some View](/documentation/swiftui/view/linespacing(_:))
- [func multilineTextAlignment(TextAlignment) -> some View](/documentation/swiftui/view/multilinetextalignment(_:))

### Formatting date and time

- [SystemFormatStyle](/documentation/swiftui/systemformatstyle) — namespace with DateOffset, DateReference, Stopwatch, Timer
- [TimeDataSource](/documentation/swiftui/timedatasource) — `.currentDate`, `.dateRange(startingAt:)`, `.dateRange(endingAt:)`, `.durationOffset(to:)`

### Managing text entry

- [func autocorrectionDisabled(Bool) -> some View](/documentation/swiftui/view/autocorrectiondisabled(_:))
- [func keyboardType(UIKeyboardType) -> some View](/documentation/swiftui/view/keyboardtype(_:))
- [func scrollDismissesKeyboard(ScrollDismissesKeyboardMode) -> some View](/documentation/swiftui/view/scrolldismisseskeyboard(_:))
- [func textContentType(_:)](/documentation/swiftui/view/textcontenttype(_:))
- [func textInputAutocapitalization(TextInputAutocapitalization?) -> some View](/documentation/swiftui/view/textinputautocapitalization(_:))
- [TextInputAutocapitalization](/documentation/swiftui/textinputautocapitalization) — values: .characters, .sentences, .words, .never
- [func textInputCompletion(String) -> some View](/documentation/swiftui/view/textinputcompletion(_:))
- [func textInputSuggestions(_:)](/documentation/swiftui/view/textinputsuggestions(_:))
- [TextInputFormattingControlPlacement](/documentation/swiftui/textinputformattingcontrolplacement) — Set: .accessoryBar, .all, .contextMenu, .default, .fontPanel, .inputAssistant

### Dictating text

- [func searchDictationBehavior(TextInputDictationBehavior) -> some View](/documentation/swiftui/view/searchdictationbehavior(_:))
- [TextInputDictationActivation](/documentation/swiftui/textinputdictationactivation) — values: .onLook, .onSelect
- [TextInputDictationBehavior](/documentation/swiftui/textinputdictationbehavior) — values: .automatic, .inline(activation:), .preventDictation

### Configuring the Writing Tools behavior

- [func writingToolsBehavior(WritingToolsBehavior) -> some View](/documentation/swiftui/view/writingtoolsbehavior(_:))
- [WritingToolsBehavior](/documentation/swiftui/writingtoolsbehavior) — values: .automatic, .complete, .disabled, .limited

### Specifying text equivalents

- [func typeSelectEquivalent(_:)](/documentation/swiftui/view/typeselectequivalent(_:))

### Localizing text

- [Preparing views for localization](/documentation/swiftui/preparing-views-for-localization) (article)
- [LocalizedStringKey](/documentation/swiftui/localizedstringkey) — type for localized string lookup with interpolation support
- [func typesettingLanguage(_:isEnabled:)](/documentation/swiftui/view/typesettinglanguage(_:isenabled:))
- [TypesettingLanguage](/documentation/swiftui/typesettinglanguage) — values: .automatic, .explicit(Locale.Language)

### Deprecated types

- [ContentSizeCategory](/documentation/swiftui/contentsizecategory) [deprecated] — use DynamicTypeSize instead

### Creating an image

- [Image](/documentation/swiftui/image) — view that displays an image from assets, system symbols, UIImage/NSImage, or drawing instructions
- [Image.TemplateRenderingMode](/documentation/swiftui/image/templaterenderingmode) — enum: original, template
- [Image.Interpolation](/documentation/swiftui/image/interpolation) — enum: high, low, medium, none
- [Image.DynamicRange](/documentation/swiftui/image/dynamicrange) — values: .standard, .high, .constrainedHigh
- [Image.Orientation](/documentation/swiftui/image/orientation) — enum: up, down, left, right, upMirrored, downMirrored, leftMirrored, rightMirrored
- [Image.ResizingMode](/documentation/swiftui/image/resizingmode) — enum: stretch, tile
- [Image.Scale](/documentation/swiftui/image/scale) — enum: small, medium, large

### Configuring an image

- [Fitting images into available space](/documentation/swiftui/fitting-images-into-available-space) (article)
- [func imageScale(Image.Scale) -> some View](/documentation/swiftui/view/imagescale(_:))

### Loading images asynchronously

- [AsyncImage](/documentation/swiftui/asyncimage) — loads and displays an image from a URL
- [AsyncImagePhase](/documentation/swiftui/asyncimagephase) — enum: empty, success(Image), failure(Error); properties: .image, .error

### Setting a symbol variant

- [func symbolVariant(SymbolVariants) -> some View](/documentation/swiftui/view/symbolvariant(_:))
- [SymbolVariants](/documentation/swiftui/symbolvariants) — values: .none, .circle, .square, .rectangle, .fill, .slash; combinable via instance properties

### Managing symbol effects

- [func symbolEffect(_:options:isActive:) -> some View](/documentation/swiftui/view/symboleffect(_:options:isactive:))
- [func symbolEffect(_:options:value:) -> some View](/documentation/swiftui/view/symboleffect(_:options:value:))
- [func symbolEffectsRemoved(Bool) -> some View](/documentation/swiftui/view/symboleffectsremoved(_:))
- [SymbolEffectTransition](/documentation/swiftui/symboleffecttransition) — transition wrapping a symbol effect

### Setting symbol rendering modes

- [func symbolRenderingMode(SymbolRenderingMode?) -> some View](/documentation/swiftui/view/symbolrenderingmode(_:))
- [SymbolRenderingMode](/documentation/swiftui/symbolrenderingmode) — values: .hierarchical, .monochrome, .multicolor, .palette
- [SymbolColorRenderingMode](/documentation/swiftui/symbolcolorrenderingmode) — values: .flat, .gradient
- [SymbolVariableValueMode](/documentation/swiftui/symbolvariablevaluemode) — values: .color, .draw

### Rendering images from views

- [ImageRenderer](/documentation/swiftui/imagerenderer) — renders a SwiftUI view to CGImage/UIImage/NSImage

### Creating buttons

- [Button](/documentation/swiftui/button) — standard button with action + label; supports roles, App Intents
- [func buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [func buttonBorderShape(ButtonBorderShape) -> some View](/documentation/swiftui/view/buttonbordershape(_:))
- [func buttonRepeatBehavior(ButtonRepeatBehavior) -> some View](/documentation/swiftui/view/buttonrepeatbehavior(_:))
- [ButtonBorderShape](/documentation/swiftui/buttonbordershape) — values: .automatic, .capsule, .circle, .roundedRectangle, .roundedRectangle(radius:)
- [ButtonRole](/documentation/swiftui/buttonrole) — values: .cancel, .destructive, .close, .confirm
- [ButtonRepeatBehavior](/documentation/swiftui/buttonrepeatbehavior) — values: .automatic, .enabled, .disabled
- [ButtonSizing](/documentation/swiftui/buttonsizing) — values: .automatic, .fitted, .flexible

### Creating special-purpose buttons

- [EditButton](/documentation/swiftui/editbutton) — toggles edit mode
- [PasteButton](/documentation/swiftui/pastebutton) — reads from the pasteboard
- [RenameButton](/documentation/swiftui/renamebutton) — triggers rename action

### Linking to other content

- [Link](/documentation/swiftui/link) — opens a URL
- [ShareLink](/documentation/swiftui/sharelink) — presents share sheet for items with optional previews
- [SharePreview](/documentation/swiftui/sharepreview) — preview metadata for shared items
- [TextFieldLink](/documentation/swiftui/textfieldlink) — presents text input popover
- [HelpLink](/documentation/swiftui/helplink) — opens help content

### Getting numeric inputs

- [Slider](/documentation/swiftui/slider) — selects a value from a bounded range
- [SliderTick](/documentation/swiftui/slidertick) — tick mark for sliders
- [SliderTickContent](/documentation/swiftui/slidertickcontent) — protocol for slider tick content
- [Stepper](/documentation/swiftui/stepper) — increments/decrements a value
- [Toggle](/documentation/swiftui/toggle) — switches between on/off states; supports collections and App Intents
- [func toggleStyle<S>(S) -> some View](/documentation/swiftui/view/togglestyle(_:))

### Choosing from a set of options

- [Picker](/documentation/swiftui/picker) — selects from a set of mutually exclusive values
- [func pickerStyle<S>(S) -> some View](/documentation/swiftui/view/pickerstyle(_:))
- [func horizontalRadioGroupLayout() -> some View](/documentation/swiftui/view/horizontalradiogrouplayout())
- [func defaultWheelPickerItemHeight(CGFloat) -> some View](/documentation/swiftui/view/defaultwheelpickeritemheight(_:))
- [func paletteSelectionEffect(PaletteSelectionEffect) -> some View](/documentation/swiftui/view/paletteselectioneffect(_:))
- [PaletteSelectionEffect](/documentation/swiftui/paletteselectioneffect) — values: .automatic, .custom, .symbolVariant(_:)

### Choosing dates

- [DatePicker](/documentation/swiftui/datepicker) — selects a date, optionally within a range
- [DatePickerComponents](/documentation/swiftui/datepickercomponents) — options: .date, .hourAndMinute, .hourMinuteAndSecond
- [func datePickerStyle<S>(S) -> some View](/documentation/swiftui/view/datepickerstyle(_:))
- [MultiDatePicker](/documentation/swiftui/multidatepicker) — selects multiple dates

### Choosing a color

- [ColorPicker](/documentation/swiftui/colorpicker) — selects a color with optional opacity support

### Indicating a value

- [Gauge](/documentation/swiftui/gauge) — displays a value within a range with labels
- [func gaugeStyle<S>(S) -> some View](/documentation/swiftui/view/gaugestyle(_:))
- [ProgressView](/documentation/swiftui/progressview) — determinate or indeterminate progress; supports timer intervals
- [func progressViewStyle<S>(S) -> some View](/documentation/swiftui/view/progressviewstyle(_:))
- [ContentUnavailableView](/documentation/swiftui/contentunavailableview) — displays placeholder when content is missing; `.search` built-in

### Indicating missing content

- [ContentUnavailableView](/documentation/swiftui/contentunavailableview) — placeholder for empty states; built-in `.search` variant

### Providing haptic feedback

- [func sensoryFeedback(_:trigger:) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:))
- [func sensoryFeedback(_:trigger:condition:) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:condition:))
- [SensoryFeedback](/documentation/swiftui/sensoryfeedback) — values: .start, .stop, .alignment, .decrease, .increase, .levelChange, .selection, .pathComplete, .success, .warning, .error, .impact; nested: Flexibility(.rigid/.soft/.solid), Weight(.light/.medium/.heavy), PressFeedback, ReleaseFeedback, SelectionFeedback

### Sizing controls

- [func controlSize(_:)](/documentation/swiftui/view/controlsize(_:))
- [ControlSize](/documentation/swiftui/controlsize) — enum: mini, small, regular, large, extraLarge

### Building a menu bar

- [Building and customizing the menu bar with SwiftUI](/documentation/swiftui/building-and-customizing-the-menu-bar-with-swiftui) (article)

### Creating a menu

- [Populating SwiftUI menus with adaptive controls](/documentation/swiftui/populating-swiftui-menus-with-adaptive-controls) (article)
- [Menu](/documentation/swiftui/menu) — presents a menu of actions; supports primary action
- [func menuStyle<S>(S) -> some View](/documentation/swiftui/view/menustyle(_:))

### Creating context menus

- [func contextMenu(menuItems:) -> some View](/documentation/swiftui/view/contextmenu(menuitems:))
- [func contextMenu(menuItems:preview:) -> some View](/documentation/swiftui/view/contextmenu(menuitems:preview:))
- [func contextMenu(forSelectionType:menu:primaryAction:) -> some View](/documentation/swiftui/view/contextmenu(forselectiontype:menu:primaryaction:))

### Defining commands

- [func commands(content:) -> some Scene](/documentation/swiftui/scene/commands(content:))
- [func commandsRemoved() -> some Scene](/documentation/swiftui/scene/commandsremoved())
- [func commandsReplaced(content:) -> some Scene](/documentation/swiftui/scene/commandsreplaced(content:))
- [Commands](/documentation/swiftui/commands) — protocol for defining keyboard commands
- [CommandMenu](/documentation/swiftui/commandmenu) — a menu in the command menu bar
- [CommandGroup](/documentation/swiftui/commandgroup) — places commands relative to a placement (after/before/replacing)
- [CommandGroupPlacement](/documentation/swiftui/commandgroupplacement) — values: .appInfo, .appSettings, .appTermination, .appVisibility, .systemServices, .importExport, .newItem, .printItem, .saveItem, .pasteboard, .textEditing, .textFormatting, .undoRedo, .sidebar, .toolbar, .singleWindowList, .windowArrangement, .windowList, .windowSize, .help

### Getting built-in command groups

- [SidebarCommands](/documentation/swiftui/sidebarcommands), [TextEditingCommands](/documentation/swiftui/texteditingcommands), [TextFormattingCommands](/documentation/swiftui/textformattingcommands), [ToolbarCommands](/documentation/swiftui/toolbarcommands), [ImportFromDevicesCommands](/documentation/swiftui/importfromdevicescommands), [InspectorCommands](/documentation/swiftui/inspectorcommands), [EmptyCommands](/documentation/swiftui/emptycommands)

### Showing a menu indicator

- [func menuIndicator(Visibility) -> some View](/documentation/swiftui/view/menuindicator(_:))

### Configuring menu dismissal

- [func menuActionDismissBehavior(MenuActionDismissBehavior) -> some View](/documentation/swiftui/view/menuactiondismissbehavior(_:))
- [MenuActionDismissBehavior](/documentation/swiftui/menuactiondismissbehavior) — values: .automatic, .disabled, .enabled

### Setting a preferred order

- [func menuOrder(MenuOrder) -> some View](/documentation/swiftui/view/menuorder(_:))
- [MenuOrder](/documentation/swiftui/menuorder) — values: .automatic, .fixed, .priority

### Deprecated types

- [MenuButton](/documentation/swiftui/menubutton) [deprecated] — use Menu instead
- [MenuButtonStyle](/documentation/swiftui/menubuttonstyle) [deprecated] — BorderlessButtonMenuButtonStyle, BorderlessPullDownMenuButtonStyle, DefaultMenuButtonStyle, PullDownMenuButtonStyle
- [PullDownButton](/documentation/swiftui/pulldownbutton) [deprecated]
- [ContextMenu](/documentation/swiftui/contextmenu) [deprecated] — use .contextMenu(menuItems:) modifier instead

### Creating rectangular shapes

- [Rectangle](/documentation/swiftui/rectangle) — fills its frame
- [RoundedRectangle](/documentation/swiftui/roundedrectangle) — rounded corners with cornerRadius or cornerSize; style: RoundedCornerStyle (.circular, .continuous)
- [RoundedRectangularShape](/documentation/swiftui/roundedrectangularshape) — protocol for shapes with rounded corners
- [RoundedRectangularShapeCorners](/documentation/swiftui/roundedrectangularshapecorners) — per-corner style configuration
- [UnevenRoundedRectangle](/documentation/swiftui/unevenroundedrectangle) — different radius per corner
- [RectangleCornerRadii](/documentation/swiftui/rectanglecornerradii) — per-corner radius values
- [RectangleCornerInsets](/documentation/swiftui/rectanglecornerinsets) — per-corner inset sizes
- [ConcentricRectangle](/documentation/swiftui/concentricrectangle) — rectangle with concentric corner styles

### Creating circular shapes

- [Circle](/documentation/swiftui/circle) — circle centered in its frame
- [Ellipse](/documentation/swiftui/ellipse) — ellipse aligned to its frame
- [Capsule](/documentation/swiftui/capsule) — rectangle with fully rounded short sides

### Drawing custom shapes

- [Path](/documentation/swiftui/path) — 2D shape with lines, curves, arcs; supports boolean operations (union, intersection, subtraction, symmetricDifference)

### Defining shape behavior

- [ShapeView](/documentation/swiftui/shapeview) — protocol for views that display a shape with fill/stroke
- [Shape](/documentation/swiftui/shape) — protocol: `path(in:)`, `sizeThatFits(_:)`; static shapes: .rect, .circle, .capsule, .ellipse, .containerRelative, .buttonBorder; supports trim, transform, scale, rotation, offset, fill, stroke, boolean ops
- [AnyShape](/documentation/swiftui/anyshape) — type-erased shape
- [ShapeRole](/documentation/swiftui/shaperole) — enum: fill, stroke, separator
- [StrokeStyle](/documentation/swiftui/strokestyle) — configures lineWidth, lineCap, lineJoin, miterLimit, dash, dashPhase
- [StrokeShapeView](/documentation/swiftui/strokeshapeview) — view displaying a stroked shape
- [StrokeBorderShapeView](/documentation/swiftui/strokebordershapeview) — view displaying a stroke-bordered shape
- [FillStyle](/documentation/swiftui/fillstyle) — eoFill and antialiased settings
- [FillShapeView](/documentation/swiftui/fillshapeview) — view displaying a filled shape

### Transforming a shape

- [ScaledShape](/documentation/swiftui/scaledshape) — shape with scale + anchor
- [RotatedShape](/documentation/swiftui/rotatedshape) — shape with angle + anchor
- [OffsetShape](/documentation/swiftui/offsetshape) — shape with offset
- [TransformedShape](/documentation/swiftui/transformedshape) — shape with CGAffineTransform

### Setting a container shape

- [func containerShape(_:)](/documentation/swiftui/view/containershape(_:))
- [InsettableShape](/documentation/swiftui/insettableshape) — protocol: strokeBorder, inset(by:)
- [ContainerRelativeShape](/documentation/swiftui/containerrelativeshape) — shape matching container

### Immediate mode drawing

- [Add rich graphics to your SwiftUI app](/documentation/swiftui/add-rich-graphics-to-your-swiftui-app) (article)
- [Canvas](/documentation/swiftui/canvas) — immediate mode 2D drawing view using GraphicsContext
- [GraphicsContext](/documentation/swiftui/graphicscontext) — context for drawing paths, images, text, symbols; supports filters, transforms, clipping, blend modes, layers
- [GraphicsContext.Shading](/documentation/swiftui/graphicscontext/shading) — color, gradient (linear/radial/conic/mesh), tiledImage, style, shader, palette, backdrop
- [GraphicsContext.GradientOptions](/documentation/swiftui/graphicscontext/gradientoptions) — .linearColor, .mirror, .repeat
- [GraphicsContext.Filter](/documentation/swiftui/graphicscontext/filter) — brightness, contrast, saturation, colorInvert, colorMultiply, hueRotation, grayscale, colorMatrix, blur, shadow, luminanceToAlpha, alphaThreshold, projectionTransform, colorShader, distortionShader, layerShader
- [GraphicsContext.BlendMode](/documentation/swiftui/graphicscontext/blendmode-swift.struct) — normal, darken, multiply, colorBurn, plusDarker, lighten, screen, colorDodge, plusLighter, overlay, softLight, hardLight, difference, exclusion, hue, saturation, color, luminosity, Porter-Duff modes
- [GraphicsContext.ClipOptions](/documentation/swiftui/graphicscontext/clipoptions) — .inverse
- [GraphicsContext.BlurOptions](/documentation/swiftui/graphicscontext/bluroptions) — .dithersResult, .opaque
- [GraphicsContext.ShadowOptions](/documentation/swiftui/graphicscontext/shadowoptions) — .disablesGroup, .invertsAlpha, .shadowAbove, .shadowOnly
- [GraphicsContext.ResolvedSymbol](/documentation/swiftui/graphicscontext/resolvedsymbol), [ResolvedImage](/documentation/swiftui/graphicscontext/resolvedimage), [ResolvedText](/documentation/swiftui/graphicscontext/resolvedtext)

### Setting a color

- [func tint(_:)](/documentation/swiftui/view/tint(_:))
- [Color](/documentation/swiftui/color) — standard colors: black, blue, brown, clear, cyan, gray, green, indigo, mint, orange, pink, purple, red, teal, white, yellow; semantic: .accentColor, .primary, .secondary; methods: opacity, gradient, mix, exposureAdjust, headroom
- [Color.RGBColorSpace](/documentation/swiftui/color/rgbcolorspace) — enum: sRGB, sRGBLinear, displayP3
- [Color.Resolved](/documentation/swiftui/color/resolved) — concrete RGBA color value
- [Color.ResolvedHDR](/documentation/swiftui/color/resolvedhdr) — HDR-resolved color with headroom

### Styling content

- [func border<S>(S, width:) -> some View](/documentation/swiftui/view/border(_:width:))
- [func foregroundStyle(_:)](/documentation/swiftui/view/foregroundstyle(_:)) — 1, 2, or 3 style overloads
- [func backgroundStyle<S>(S) -> some View](/documentation/swiftui/view/backgroundstyle(_:))
- [ShapeStyle](/documentation/swiftui/shapestyle) — protocol: system colors, angular/conic/elliptical/linear/radial gradients, materials, image paint, hierarchical styles (primary-quinary), semantic styles (.foreground, .background, .selection, .separator, .tint, .placeholder, .link, .fill, .windowBackground); modifiers: blendMode, opacity, shadow
- [AngularGradient](/documentation/swiftui/angulargradient) — angular/conic gradient ShapeStyle
- [EllipticalGradient](/documentation/swiftui/ellipticalgradient) — elliptical gradient ShapeStyle
- [LinearGradient](/documentation/swiftui/lineargradient) — linear gradient ShapeStyle
- [RadialGradient](/documentation/swiftui/radialgradient) — radial gradient ShapeStyle
- [Material](/documentation/swiftui/material) — values: .ultraThin, .thin, .regular, .thick, .ultraThick, .bar
- [ImagePaint](/documentation/swiftui/imagepaint) — tiling image as ShapeStyle
- [HierarchicalShapeStyle](/documentation/swiftui/hierarchicalshapestyle) — primary, secondary, tertiary, quaternary, quinary
- [ForegroundStyle](/documentation/swiftui/foregroundstyle), [BackgroundStyle](/documentation/swiftui/backgroundstyle), [SelectionShapeStyle](/documentation/swiftui/selectionshapestyle), [SeparatorShapeStyle](/documentation/swiftui/separatorshapestyle), [TintShapeStyle](/documentation/swiftui/tintshapestyle), [FillShapeStyle](/documentation/swiftui/fillshapestyle), [LinkShapeStyle](/documentation/swiftui/linkshapestyle), [PlaceholderTextShapeStyle](/documentation/swiftui/placeholdertextshapestyle), [WindowBackgroundShapeStyle](/documentation/swiftui/windowbackgroundshapestyle)
- [AnyShapeStyle](/documentation/swiftui/anyshapestyle) — type-erased ShapeStyle
- [Gradient](/documentation/swiftui/gradient) — collection of color stops; Gradient.Stop, Gradient.ColorSpace (.device, .perceptual)
- [MeshGradient](/documentation/swiftui/meshgradient) — mesh-based gradient with BezierPoint control; supports points or bezierPoints
- [AnyGradient](/documentation/swiftui/anygradient) — type-erased gradient
- [ShadowStyle](/documentation/swiftui/shadowstyle) — `.drop(color:radius:x:y:)`, `.inner(color:radius:x:y:)`
- [Glass](/documentation/swiftui/glass) — glass material effect; values: .clear, .identity, .regular; modifiers: .interactive, .tint

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
- [MaterialActiveAppearance](/documentation/swiftui/materialactiveappearance) — values: .active, .automatic, .inactive, .matchWindow

### Scaling, rotating, or transforming a view

- [func scaledToFill() -> some View](/documentation/swiftui/view/scaledtofill())
- [func scaledToFit() -> some View](/documentation/swiftui/view/scaledtofit())
- [func scaleEffect(_:anchor:)](/documentation/swiftui/view/scaleeffect(_:anchor:))
- [func scaleEffect(x:y:anchor:) -> some View](/documentation/swiftui/view/scaleeffect(x:y:anchor:))
- [func scaleEffect(x:y:z:anchor:) -> some View](/documentation/swiftui/view/scaleeffect(x:y:z:anchor:))
- [func aspectRatio(_:contentMode:)](/documentation/swiftui/view/aspectratio(_:contentmode:))
- [func rotationEffect(Angle, anchor:) -> some View](/documentation/swiftui/view/rotationeffect(_:anchor:))
- [func rotation3DEffect(Angle, axis:, anchor:, anchorZ:, perspective:) -> some View](/documentation/swiftui/view/rotation3deffect(_:axis:anchor:anchorz:perspective:))
- [func perspectiveRotationEffect(Angle, axis:, anchor:, anchorZ:, perspective:) -> some View](/documentation/swiftui/view/perspectiverotationeffect(_:axis:anchor:anchorz:perspective:))
- [func rotation3DEffect(Rotation3D, anchor:) -> some View](/documentation/swiftui/view/rotation3deffect(_:anchor:))
- [func transformEffect(CGAffineTransform) -> some View](/documentation/swiftui/view/transformeffect(_:))
- [func transform3DEffect(AffineTransform3D) -> some View](/documentation/swiftui/view/transform3deffect(_:))
- [func projectionEffect(ProjectionTransform) -> some View](/documentation/swiftui/view/projectioneffect(_:))
- [ProjectionTransform](/documentation/swiftui/projectiontransform) — 3x3 projection matrix; isAffine, isIdentity, invert, concatenating
- [ContentMode](/documentation/swiftui/contentmode) — enum: fill, fit

### Masking and clipping

- [func mask(alignment:, _:) -> some View](/documentation/swiftui/view/mask(alignment:_:))
- [func clipped(antialiased:) -> some View](/documentation/swiftui/view/clipped(antialiased:))
- [func clipShape(_:style:) -> some View](/documentation/swiftui/view/clipshape(_:style:))

### Applying blur and shadows

- [func blur(radius:opaque:) -> some View](/documentation/swiftui/view/blur(radius:opaque:))
- [func shadow(color:radius:x:y:) -> some View](/documentation/swiftui/view/shadow(color:radius:x:y:))
- [ColorMatrix](/documentation/swiftui/colormatrix) — 5x4 color transformation matrix

### Applying effects based on geometry

- [func visualEffect(_:) -> some View](/documentation/swiftui/view/visualeffect(_:)) — apply effects using GeometryProxy
- [func visualEffect3D(_:) -> some View](/documentation/swiftui/view/visualeffect3d(_:)) — apply effects using GeometryProxy3D
- [VisualEffect](/documentation/swiftui/visualeffect) — protocol: brightness, colorEffect, contrast, grayscale, hueRotation, saturation, opacity, scaleEffect, rotationEffect, rotation3DEffect, perspectiveRotationEffect, offset, transform3DEffect, transformEffect, blur, distortionEffect, layerEffect, blendMode
- [EmptyVisualEffect](/documentation/swiftui/emptyvisualeffect) — identity visual effect

### Compositing views

- [func blendMode(BlendMode) -> some View](/documentation/swiftui/view/blendmode(_:))
- [func compositingGroup() -> some View](/documentation/swiftui/view/compositinggroup())
- [func drawingGroup(opaque:colorMode:) -> some View](/documentation/swiftui/view/drawinggroup(opaque:colormode:))
- [BlendMode](/documentation/swiftui/blendmode) — enum: normal, darken, multiply, colorBurn, plusDarker, lighten, screen, colorDodge, plusLighter, overlay, softLight, hardLight, difference, exclusion, hue, saturation, color, luminosity, sourceAtop, destinationOver, destinationOut
- [ColorRenderingMode](/documentation/swiftui/colorrenderingmode) — enum: extendedLinear, linear, nonLinear
- [CompositorContent](/documentation/swiftui/compositorcontent) — protocol for compositor layer content (visionOS)
- [AnyCompositorContent](/documentation/swiftui/anycompositorcontent) — type-erased CompositorContent

### Measuring a view

- [GeometryReader](/documentation/swiftui/geometryreader) — reads parent-proposed size via GeometryProxy
- [GeometryReader3D](/documentation/swiftui/geometryreader3d) — 3D geometry reader (visionOS)
- [GeometryProxy](/documentation/swiftui/geometryproxy) — provides: size, safeAreaInsets, frame(in:), bounds(of:), transform(in:), containerCornerInsets, anchor subscript
- [GeometryProxy3D](/documentation/swiftui/geometryproxy3d) — 3D variant: size (Size3D), safeAreaInsets (EdgeInsets3D), frame(in:), transform(in:)
- [func coordinateSpace(_:) -> some View](/documentation/swiftui/view/coordinatespace(_:))
- [CoordinateSpace](/documentation/swiftui/coordinatespace) — enum: .global, .local, .named(_:)
- [CoordinateSpaceProtocol](/documentation/swiftui/coordinatespaceprotocol) — static spaces: .global, .local, .named(_:), .scrollView, .scrollView(axis:), .immersiveSpace
- [GlobalCoordinateSpace](/documentation/swiftui/globalcoordinatespace), [LocalCoordinateSpace](/documentation/swiftui/localcoordinatespace), [NamedCoordinateSpace](/documentation/swiftui/namedcoordinatespace)
- [PhysicalMetric](/documentation/swiftui/physicalmetric) — property wrapper converting to physical units (visionOS)
- [PhysicalMetricsConverter](/documentation/swiftui/physicalmetricsconverter) — converts between unit lengths

### Responding to a geometry change

- [func onGeometryChange(for:of:action:)](/documentation/swiftui/view/ongeometrychange(for:of:action:))

### Accessing Metal shaders

- [func colorEffect(Shader, isEnabled:) -> some View](/documentation/swiftui/view/coloreffect(_:isenabled:))
- [func distortionEffect(Shader, maxSampleOffset:, isEnabled:) -> some View](/documentation/swiftui/view/distortioneffect(_:maxsampleoffset:isenabled:))
- [func layerEffect(Shader, maxSampleOffset:, isEnabled:) -> some View](/documentation/swiftui/view/layereffect(_:maxsampleoffset:isenabled:))
- [Shader](/documentation/swiftui/shader) — Metal shader reference with arguments (float, float2-4, color, colorArray, image, data, boundingRect, floatArray)
- [Shader.Argument](/documentation/swiftui/shader/argument) — shader argument types
- [ShaderFunction](/documentation/swiftui/shaderfunction) — named function in a ShaderLibrary
- [ShaderLibrary](/documentation/swiftui/shaderlibrary) — `.default`, `.bundle(_:)`, or from URL/Data

### Accessing geometric constructs

- [Axis](/documentation/swiftui/axis) — enum: horizontal, vertical; Axis.Set
- [Angle](/documentation/swiftui/angle) — measured in degrees or radians; .zero, .degrees(_:), .radians(_:)
- [UnitPoint](/documentation/swiftui/unitpoint) — 2D unit coordinate; named: zero, topLeading, top, topTrailing, leading, center, trailing, bottomLeading, bottom, bottomTrailing
- [UnitPoint3D](/documentation/swiftui/unitpoint3d) — 3D unit coordinate with 27 named positions (top/center/bottom x leading/center/trailing x back/center/front)
- [Anchor](/documentation/swiftui/anchor) — opaque position/rect value resolved via GeometryProxy; Source: point, unitPoint, rect, bounds, named positions, 3D variants
- [DepthAlignmentID](/documentation/swiftui/depthalignmentid) — custom depth alignment guide
- [Alignment3D](/documentation/swiftui/alignment3d) — 3D alignment with 27 named positions
- [GeometryProxyCoordinateSpace3D](/documentation/swiftui/geometryproxycoordinatespace3d) — 3D coordinate space from GeometryProxy3D
