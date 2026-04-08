# Views: Shapes and Drawing — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

> **NOTE**: Despite the file name, this index currently covers styling, animations, transitions, and text — NOT core drawing primitives. Shape, Path, Canvas, Circle, Rectangle, Ellipse, Capsule, RoundedRectangle, Color, Gradient, GraphicsContext, fill/stroke modifiers, and ShapeStyle are **not yet indexed here**. They live under `/documentation/swiftui/shape`, `/documentation/swiftui/path`, `/documentation/swiftui/canvas`, `/documentation/swiftui/color`, `/documentation/swiftui/shapestyle`, etc.

## Contents
- [Styling groups](#styling-groups)
- [Styling windows](#styling-windows-from-a-view-inside-the-window)
- [Glass background (visionOS)](#adding-a-glass-background-on-views-in-visionos)
- [Animation (state-based)](#adding-state-based-animation-to-an-action)
- [Animation (view-based)](#adding-state-based-animation-to-a-view)
- [Phase animation](#creating-phase-based-animation)
- [Keyframe animation](#creating-keyframe-based-animation)
- [Custom animations](#creating-custom-animations)
- [Animatable data](#making-data-animatable)
- [Timeline views](#updating-a-view-on-a-schedule)
- [Geometry synchronization](#synchronizing-geometries)
- [Transitions](#defining-transitions)
- [Transactions](#moving-an-animation-to-another-view)
- [Deprecated animation types](#deprecated-types)
- [Displaying text](#displaying-text)
- [Text input](#getting-text-input)
- [Text selection](#selecting-text)
- [Fonts](#setting-a-font)
- [Text size](#adjusting-text-size)

---

### Missing Drawing Primitives (not yet in this file — fetch individually)
- [Shape](/documentation/swiftui/shape) — Protocol for 2D shapes; implement `path(in:)` to draw
- [InsettableShape](/documentation/swiftui/insettableshape) — Shape that can be inset
- [Path](/documentation/swiftui/path) — Outline of a 2D shape using lines, curves, arcs
- [Canvas](/documentation/swiftui/canvas) — Immediate-mode 2D drawing view
- [GraphicsContext](/documentation/swiftui/graphicscontext) — Drawing destination for Canvas
- [Circle](/documentation/swiftui/circle) — Circle shape centered in its frame
- [Ellipse](/documentation/swiftui/ellipse) — Ellipse aligned inside its frame
- [Rectangle](/documentation/swiftui/rectangle) — Rectangular shape aligned inside its frame
- [RoundedRectangle](/documentation/swiftui/roundedrectangle) — Rounded corners rectangle
- [UnevenRoundedRectangle](/documentation/swiftui/unevenroundedrectangle) — Per-corner radius rectangle
- [Capsule](/documentation/swiftui/capsule) — Capsule (stadium) shape
- [ContainerRelativeShape](/documentation/swiftui/containerrelativeshape) — Shape matching the nearest container
- [Color](/documentation/swiftui/color) — Environment-dependent color
- [ShapeStyle](/documentation/swiftui/shapestyle) — Protocol for fill/stroke styles
- [Gradient](/documentation/swiftui/gradient), [LinearGradient](/documentation/swiftui/lineargradient), [RadialGradient](/documentation/swiftui/radialgradient), [AngularGradient](/documentation/swiftui/angulargradient), [EllipticalGradient](/documentation/swiftui/ellipticalgradient), [MeshGradient](/documentation/swiftui/meshgradient)
- [Material](/documentation/swiftui/material) — Blur/vibrancy background materials
- `.fill(_:style:)`, `.stroke(_:lineWidth:)`, `.strokeBorder(_:lineWidth:)`, `.trim(from:to:)` — Shape view modifiers
- `.clipShape(_:)`, `.mask(_:)`, `.drawingGroup()` — Drawing modifiers

---

### Styling groups

- [func controlGroupStyle<S>(S) -> some View](/documentation/swiftui/view/controlgroupstyle(_:))
- [ControlGroupStyle](/documentation/swiftui/controlgroupstyle) — protocol for custom control group appearance
- [ControlGroupStyleConfiguration](/documentation/swiftui/controlgroupstyleconfiguration) — label + content config
- Built-in: `.automatic`, `.compactMenu`, `.menu`, `.navigation`, `.palette`
- Types: [AutomaticControlGroupStyle](/documentation/swiftui/automaticcontrolgroupstyle), [CompactMenuControlGroupStyle](/documentation/swiftui/compactmenucontrolgroupstyle), [MenuControlGroupStyle](/documentation/swiftui/menucontrolgroupstyle), [NavigationControlGroupStyle](/documentation/swiftui/navigationcontrolgroupstyle), [PaletteControlGroupStyle](/documentation/swiftui/palettecontrolgroupstyle)

- [func formStyle<S>(S) -> some View](/documentation/swiftui/view/formstyle(_:))
- [FormStyle](/documentation/swiftui/formstyle) — protocol for custom form appearance
- [FormStyleConfiguration](/documentation/swiftui/formstyleconfiguration)
- Built-in: `.automatic`, `.columns`, `.grouped`
- Types: [AutomaticFormStyle](/documentation/swiftui/automaticformstyle), [ColumnsFormStyle](/documentation/swiftui/columnsformstyle), [GroupedFormStyle](/documentation/swiftui/groupedformstyle)

- [func groupBoxStyle<S>(S) -> some View](/documentation/swiftui/view/groupboxstyle(_:))
- [GroupBoxStyle](/documentation/swiftui/groupboxstyle) — protocol for custom group box appearance
- [GroupBoxStyleConfiguration](/documentation/swiftui/groupboxstyleconfiguration) — label + content config
- Types: [DefaultGroupBoxStyle](/documentation/swiftui/defaultgroupboxstyle)

- [func indexViewStyle<S>(S) -> some View](/documentation/swiftui/view/indexviewstyle(_:))
- [IndexViewStyle](/documentation/swiftui/indexviewstyle) — page index dots style
- [PageIndexViewStyle](/documentation/swiftui/pageindexviewstyle) — backgroundDisplayMode: `.automatic`, `.always`, `.interactive`, `.never`

- [func labeledContentStyle<S>(S) -> some View](/documentation/swiftui/view/labeledcontentstyle(_:))
- [LabeledContentStyle](/documentation/swiftui/labeledcontentstyle) — protocol for labeled content appearance
- [LabeledContentStyleConfiguration](/documentation/swiftui/labeledcontentstyleconfiguration) — label + content config
- Types: [AutomaticLabeledContentStyle](/documentation/swiftui/automaticlabeledcontentstyle)

- [func tabViewStyle<S>(S) -> some View](/documentation/swiftui/view/tabviewstyle(_:))
- [TabViewStyle](/documentation/swiftui/tabviewstyle) — protocol for tab view appearance
- Built-in: `.automatic`, `.sidebarAdaptable`, `.tabBarOnly`, `.grouped`, `.page`, `.verticalPage`, `.carousel`
- Types: [DefaultTabViewStyle](/documentation/swiftui/defaulttabviewstyle), [SidebarAdaptableTabViewStyle](/documentation/swiftui/sidebaradaptabletabviewstyle), [TabBarOnlyTabViewStyle](/documentation/swiftui/tabbaronlytabviewstyle), [GroupedTabViewStyle](/documentation/swiftui/groupedtabviewstyle), [PageTabViewStyle](/documentation/swiftui/pagetabviewstyle), [VerticalPageTabViewStyle](/documentation/swiftui/verticalpagetabviewstyle), [CarouselTabViewStyle](/documentation/swiftui/carouseltabviewstyle)
- [PageTabViewStyle.IndexDisplayMode](/documentation/swiftui/pagetabviewstyle/indexdisplaymode) — `.always`, `.automatic`, `.never`
- [VerticalPageTabViewStyle.TransitionStyle](/documentation/swiftui/verticalpagetabviewstyle/transitionstyle) — `.automatic`, `.blur`, `.identity`

- [NavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle) (see also navigation reference)
- Types: [AutomaticNavigationSplitViewStyle](/documentation/swiftui/automaticnavigationsplitviewstyle), [BalancedNavigationSplitViewStyle](/documentation/swiftui/balancednavigationsplitviewstyle), [ProminentDetailNavigationSplitViewStyle](/documentation/swiftui/prominentdetailnavigationsplitviewstyle)
- [NavigationSplitViewStyleConfiguration](/documentation/swiftui/navigationsplitviewstyleconfiguration)

### Styling windows from a view inside the window

- [func presentedWindowStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowstyle(_:))
- [func presentedWindowToolbarStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowtoolbarstyle(_:))

### Adding a glass background on views in visionOS

- [func glassBackgroundEffect(displayMode:) -> some View](/documentation/swiftui/view/glassbackgroundeffect(displaymode:))
- [func glassBackgroundEffect(in:displayMode:) -> some View](/documentation/swiftui/view/glassbackgroundeffect(in:displaymode:))
- [GlassBackgroundDisplayMode](/documentation/swiftui/glassbackgrounddisplaymode) — `.always`, `.implicit`, `.never`
- [GlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect) — `.automatic`, `.feathered`, `.plate`
- [GlassBackgroundEffectConfiguration](/documentation/swiftui/glassbackgroundeffectconfiguration)
- Types: [AutomaticGlassBackgroundEffect](/documentation/swiftui/automaticglassbackgroundeffect), [FeatheredGlassBackgroundEffect](/documentation/swiftui/featheredglassbackgroundeffect), [PlateGlassBackgroundEffect](/documentation/swiftui/plateglassbackgroundeffect)

### Adding state-based animation to an action

- [func withAnimation<Result>(Animation?, body) rethrows -> Result](/documentation/swiftui/withanimation(_:_:))
- [func withAnimation<Result>(Animation?, completionCriteria:, body, completion:) rethrows -> Result](/documentation/swiftui/withanimation(_:completioncriteria:_:completion:))
- [AnimationCompletionCriteria](/documentation/swiftui/animationcompletioncriteria) — `.logicallyComplete`, `.removed`
- [Animation](/documentation/swiftui/animation) — configurable animation timing
  - Default: `.default`
  - Linear: `.linear`, `.linear(duration:)`
  - Ease: `.easeIn`, `.easeOut`, `.easeInOut` (+ duration variants)
  - Spring presets: `.bouncy`, `.smooth`, `.snappy` (+ duration/extraBounce variants)
  - Custom spring: `.spring`, `.spring(duration:bounce:blendDuration:)`, `.spring(response:dampingFraction:blendDuration:)`
  - Interactive: `.interactiveSpring`, `.interpolatingSpring`
  - Timing curve: `.timingCurve(_:duration:)`, `.timingCurve(_:_:_:_:duration:)`
  - Config: `.delay(_:)`, `.repeatCount(_:autoreverses:)`, `.repeatForever(autoreverses:)`, `.speed(_:)`

### Adding state-based animation to a view

- [func animation(_:)](/documentation/swiftui/view/animation(_:)) [deprecated]
- [func animation<V>(Animation?, value: V) -> some View](/documentation/swiftui/view/animation(_:value:))
- [func animation<V>(Animation?, body:) -> some View](/documentation/swiftui/view/animation(_:body:))

### Creating phase-based animation

- [Controlling the timing and movements of your animations](/documentation/swiftui/controlling-the-timing-and-movements-of-your-animations) (article)
- [func phaseAnimator(_:content:animation:) -> some View](/documentation/swiftui/view/phaseanimator(_:content:animation:))
- [func phaseAnimator(_:trigger:content:animation:) -> some View](/documentation/swiftui/view/phaseanimator(_:trigger:content:animation:))
- [PhaseAnimator](/documentation/swiftui/phaseanimator) — view that cycles through animation phases

### Creating keyframe-based animation

- [func keyframeAnimator(initialValue:repeating:content:keyframes:) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:repeating:content:keyframes:))
- [func keyframeAnimator(initialValue:trigger:content:keyframes:) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:trigger:content:keyframes:))
- [KeyframeAnimator](/documentation/swiftui/keyframeanimator) — view that animates via keyframes
- [Keyframes](/documentation/swiftui/keyframes) — protocol for keyframe definitions
- [KeyframeTimeline](/documentation/swiftui/keyframetimeline) — evaluated keyframe timeline with duration + value(time:)
- [KeyframeTrack](/documentation/swiftui/keyframetrack) — track animating a single property
- [KeyframeTrackContentBuilder](/documentation/swiftui/keyframetrackcontentbuilder) — result builder for keyframe tracks
- [KeyframesBuilder](/documentation/swiftui/keyframesbuilder) — result builder for keyframes
- [KeyframeTrackContent](/documentation/swiftui/keyframetrackcontent) — protocol for track content
- [CubicKeyframe](/documentation/swiftui/cubickeyframe) — cubic Bezier interpolated keyframe
- [LinearKeyframe](/documentation/swiftui/linearkeyframe) — linear interpolated keyframe
- [MoveKeyframe](/documentation/swiftui/movekeyframe) — immediate jump keyframe
- [SpringKeyframe](/documentation/swiftui/springkeyframe) — spring-based keyframe

### Creating custom animations

- [CustomAnimation](/documentation/swiftui/customanimation) — protocol for fully custom animation curves
- [AnimationContext](/documentation/swiftui/animationcontext) — context passed to custom animation methods
- [AnimationState](/documentation/swiftui/animationstate) — per-animation custom state storage
- [AnimationStateKey](/documentation/swiftui/animationstatekey) — key protocol for animation state
- [UnitCurve](/documentation/swiftui/unitcurve) — parametric timing curve
  - Presets: `.linear`, `.easeIn`, `.easeOut`, `.easeInOut`, `.circularEaseIn`, `.circularEaseOut`, `.circularEaseInOut`
  - Custom: `.bezier(startControlPoint:endControlPoint:)`
  - `.easeInEaseOut` [deprecated]
- [Spring](/documentation/swiftui/spring) — physics-based spring model
  - Init: `(duration:bounce:)`, `(mass:stiffness:damping:)`, `(response:dampingRatio:)`
  - Presets: `.bouncy`, `.smooth`, `.snappy`

### Making data animatable

- [Animatable](/documentation/swiftui/animatable) — protocol to make data types animatable
- [macro Animatable()](/documentation/swiftui/animatable()) — synthesize animatable conformance
- [macro AnimatableIgnored()](/documentation/swiftui/animatableignored()) — exclude property from animation
- [AnimatableValues](/documentation/swiftui/animatablevalues) — variadic animatable tuple
- [AnimatablePair](/documentation/swiftui/animatablepair) — pair of animatable values
- [VectorArithmetic](/documentation/swiftui/vectorarithmetic) — protocol for interpolatable values
- [EmptyAnimatableData](/documentation/swiftui/emptyanimatabledata) — no-op animatable data

### Updating a view on a schedule

- [Updating watchOS apps with timelines](/documentation/watchos-apps/updating-watchos-apps-with-timelines) (article)
- [TimelineView](/documentation/swiftui/timelineview) — view that updates on a schedule
- [TimelineView.Context](/documentation/swiftui/timelineview/context) — date + cadence (`.live`, `.seconds`, `.minutes`)
- [TimelineSchedule](/documentation/swiftui/timelineschedule) — protocol for timeline schedules
  - Built-in: `.animation`, `.everyMinute`, `.explicit(_:)`, `.periodic(from:by:)`
- [TimelineScheduleMode](/documentation/swiftui/timelineschedulemode) — `.normal`, `.lowFrequency`
- Types: [AnimationTimelineSchedule](/documentation/swiftui/animationtimelineschedule), [EveryMinuteTimelineSchedule](/documentation/swiftui/everyminutetimelineschedule), [ExplicitTimelineSchedule](/documentation/swiftui/explicittimelineschedule), [PeriodicTimelineSchedule](/documentation/swiftui/periodictimelineschedule)
- [TimelineViewDefaultContext](/documentation/swiftui/timelineviewdefaultcontext)

### Synchronizing geometries

- [func matchedGeometryEffect(id:in:properties:anchor:isSource:) -> some View](/documentation/swiftui/view/matchedgeometryeffect(id:in:properties:anchor:issource:))
- [MatchedGeometryProperties](/documentation/swiftui/matchedgeometryproperties) — `.frame`, `.position`, `.size`
- [GeometryEffect](/documentation/swiftui/geometryeffect) — protocol for geometry-based effects
- [Namespace](/documentation/swiftui/namespace) — property wrapper for matched geometry ID space
- [Namespace.ID](/documentation/swiftui/namespace/id)
- [func geometryGroup() -> some View](/documentation/swiftui/view/geometrygroup())

### Defining transitions

- [func transition(_:) -> some View](/documentation/swiftui/view/transition(_:))
- [Transition](/documentation/swiftui/transition) — protocol for view transitions
  - Built-in: `.blurReplace`, `.identity`, `.move(edge:)`, `.offset(_:)`, `.offset(x:y:)`, `.opacity`, `.push(from:)`, `.scale`, `.scale(_:anchor:)`, `.slide`, `.symbolEffect`
  - Config: `.animation(_:)`, `.combined(with:)`
- [BlurReplaceTransition](/documentation/swiftui/blurreplacetransition) — `.downUp`, `.upUp` configs
- [IdentityTransition](/documentation/swiftui/identitytransition), [MoveTransition](/documentation/swiftui/movetransition), [OffsetTransition](/documentation/swiftui/offsettransition), [OpacityTransition](/documentation/swiftui/opacitytransition), [PushTransition](/documentation/swiftui/pushtransition), [ScaleTransition](/documentation/swiftui/scaletransition), [SlideTransition](/documentation/swiftui/slidetransition)
- [TransitionProperties](/documentation/swiftui/transitionproperties) — hasMotion flag
- [TransitionPhase](/documentation/swiftui/transitionphase) — `.identity`, `.willAppear`, `.didDisappear`
- [AsymmetricTransition](/documentation/swiftui/asymmetrictransition) — different insert/remove transitions
- [AnyTransition](/documentation/swiftui/anytransition) — type-erased transition (same built-in set)
- [func contentTransition(ContentTransition) -> some View](/documentation/swiftui/view/contenttransition(_:))
- [ContentTransition](/documentation/swiftui/contenttransition) — `.identity`, `.interpolate`, `.numericText(countsDown:)`, `.numericText(value:)`, `.opacity`, `.symbolEffect`
- [PlaceholderContentView](/documentation/swiftui/placeholdercontentview)
- [func navigationTransition(some NavigationTransition) -> some View](/documentation/swiftui/view/navigationtransition(_:))
- [NavigationTransition](/documentation/swiftui/navigationtransition) — `.automatic`, `.zoom(sourceID:in:)`
- Types: [AutomaticNavigationTransition](/documentation/swiftui/automaticnavigationtransition), [ZoomNavigationTransition](/documentation/swiftui/zoomnavigationtransition)
- [func matchedTransitionSource(id:in:) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:))
- [func matchedTransitionSource(id:in:configuration:) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:configuration:))
- [MatchedTransitionSourceConfiguration](/documentation/swiftui/matchedtransitionsourceconfiguration) — `.background(_:)`, `.clipShape(_:)`, `.shadow(color:radius:x:y:)`
- [EmptyMatchedTransitionSourceConfiguration](/documentation/swiftui/emptymatchedtransitionsourceconfiguration)

### Moving an animation to another view

- [func withTransaction(Transaction, body) rethrows -> Result](/documentation/swiftui/withtransaction(_:_:))
- [func withTransaction(keyPath, value, body) rethrows -> Result](/documentation/swiftui/withtransaction(_:_:_:))
- [func transaction((inout Transaction) -> Void) -> some View](/documentation/swiftui/view/transaction(_:))
- [func transaction(value:_:) -> some View](/documentation/swiftui/view/transaction(value:_:))
- [func transaction(_:body:) -> some View](/documentation/swiftui/view/transaction(_:body:))
- [Transaction](/documentation/swiftui/transaction) — animation + metadata bundle for state changes
- [TransactionKey](/documentation/swiftui/transactionkey) — custom transaction key protocol
- [macro Entry()](/documentation/swiftui/entry()) — synthesize environment/transaction/container entry

### Deprecated types

- [AnimatableModifier](/documentation/swiftui/animatablemodifier) [deprecated]

### Displaying text

- [Text](/documentation/swiftui/text) — read-only text view with rich formatting
- [Text.Case](/documentation/swiftui/text/case) — `.lowercase`, `.uppercase`
- [Text.DateStyle](/documentation/swiftui/text/datestyle) — `.date`, `.offset`, `.relative`, `.time`, `.timer`
- [Text.LineStyle](/documentation/swiftui/text/linestyle) — strikethrough/underline style
- [Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern) — `.solid`, `.dot`, `.dash`, `.dashDot`, `.dashDotDot`
- [Text.Scale](/documentation/swiftui/text/scale) — `.default`, `.secondary`
- [Text.TruncationMode](/documentation/swiftui/text/truncationmode) — `.head`, `.middle`, `.tail`
- [Text.AlignmentStrategy](/documentation/swiftui/text/alignmentstrategy) — `.default`, `.layoutBased`, `.writingDirectionBased`
- [Text.Layout](/documentation/swiftui/text/layout) — text layout introspection (lines, runs, bounds)
- [Text.LayoutKey](/documentation/swiftui/text/layoutkey) — anchored layout preference key
- [Text.WritingDirectionStrategy](/documentation/swiftui/text/writingdirectionstrategy) — `.contentBased`, `.default`, `.layoutBased`
- [Label](/documentation/swiftui/label) — icon + title composite view
- [func labelStyle<S>(S) -> some View](/documentation/swiftui/view/labelstyle(_:))

### Getting text input

- [Building rich SwiftUI text experiences](/documentation/swiftui/building-rich-swiftui-text-experiences) (article)
- [TextField](/documentation/swiftui/textfield) — single/multi-line editable text field
- [func textFieldStyle<S>(S) -> some View](/documentation/swiftui/view/textfieldstyle(_:))
- [SecureField](/documentation/swiftui/securefield) — password entry field
- [TextEditor](/documentation/swiftui/texteditor) — multi-line text editor

### Selecting text

- [func textSelection<S>(S) -> some View](/documentation/swiftui/view/textselection(_:))
- [TextSelectability](/documentation/swiftui/textselectability) — `.enabled`, `.disabled`
- [EnabledTextSelectability](/documentation/swiftui/enabledtextselectability), [DisabledTextSelectability](/documentation/swiftui/disabledtextselectability)
- [TextSelection](/documentation/swiftui/textselection) — insertion point or range selection
- [func textSelectionAffinity(TextSelectionAffinity) -> some View](/documentation/swiftui/view/textselectionaffinity(_:))
- [TextSelectionAffinity](/documentation/swiftui/textselectionaffinity) — `.automatic`, `.downstream`, `.upstream`
- [AttributedTextSelection](/documentation/swiftui/attributedtextselection) — selection in attributed strings

### Setting a font

- [Applying custom fonts to text](/documentation/swiftui/applying-custom-fonts-to-text) (article)
- [func font(Font?) -> some View](/documentation/swiftui/view/font(_:))
- [func fontDesign(Font.Design?) -> some View](/documentation/swiftui/view/fontdesign(_:))
- [func fontWeight(Font.Weight?) -> some View](/documentation/swiftui/view/fontweight(_:))
- [func fontWidth(Font.Width?) -> some View](/documentation/swiftui/view/fontwidth(_:))
- [Font](/documentation/swiftui/font) — environment-dependent text font
  - Standard: `.extraLargeTitle2`, `.extraLargeTitle`, `.largeTitle`, `.title`, `.title2`, `.title3`, `.headline`, `.subheadline`, `.body`, `.callout`, `.caption`, `.caption2`, `.footnote`
  - System: `.system(_:design:weight:)`, `.system(size:weight:design:)`
  - Custom: `.custom(_:size:)`, `.custom(_:fixedSize:)`, `.custom(_:size:relativeTo:)`
- [Font.Design](/documentation/swiftui/font/design) — `.default`, `.monospaced`, `.rounded`, `.serif`
- [Font.TextStyle](/documentation/swiftui/font/textstyle) — semantic text style enum
- [Font.Weight](/documentation/swiftui/font/weight) — `.ultraLight` through `.black`
- [Font.Width](/documentation/swiftui/font/width) — `.compressed`, `.condensed`, `.standard`, `.expanded`
- [Font.Leading](/documentation/swiftui/font/leading) — `.standard`, `.loose`, `.tight`
- [Font.Context](/documentation/swiftui/font/context), [Font.Resolved](/documentation/swiftui/font/resolved) — font resolution types

### Adjusting text size

- [func textScale(Text.Scale, isEnabled: Bool) -> some View](/documentation/swiftui/view/textscale(_:isenabled:))
- [func dynamicTypeSize(_:) -> some View](/documentation/swiftui/view/dynamictypesize(_:))
- [DynamicTypeSize](/documentation/swiftui/dynamictypesize) — accessibility type size enum
