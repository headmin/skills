# Views: Shapes and Drawing — SwiftUI Reference

## Contents
  - [Styling groups](#styling-groups)
  - [Styling windows from a view inside the window](#styling-windows-from-a-view-inside-the-window)
  - [Adding a glass background on views in visionOS](#adding-a-glass-background-on-views-in-visionos)
  - [Adding state-based animation to an action](#adding-state-based-animation-to-an-action)
  - [Adding state-based animation to a view](#adding-state-based-animation-to-a-view)
  - [Creating phase-based animation](#creating-phase-based-animation)
  - [Creating keyframe-based animation](#creating-keyframe-based-animation)
  - [Creating custom animations](#creating-custom-animations)
  - [Making data animatable](#making-data-animatable)
  - [Updating a view on a schedule](#updating-a-view-on-a-schedule)
  - [Synchronizing geometries](#synchronizing-geometries)
  - [Defining transitions](#defining-transitions)
  - [Moving an animation to another view](#moving-an-animation-to-another-view)
  - [Deprecated types](#deprecated-types)
  - [Displaying text](#displaying-text)
  - [Getting text input](#getting-text-input)
  - [Selecting text](#selecting-text)
  - [Setting a font](#setting-a-font)
  - [Adjusting text size](#adjusting-text-size)

---
##### Creating the navigation split view style

- [init()](/documentation/swiftui/automaticnavigationsplitviewstyle/init())
- [BalancedNavigationSplitViewStyle](/documentation/swiftui/balancednavigationsplitviewstyle)

##### Creating the navigation split view style

- [init()](/documentation/swiftui/balancednavigationsplitviewstyle/init())
- [ProminentDetailNavigationSplitViewStyle](/documentation/swiftui/prominentdetailnavigationsplitviewstyle)

##### Creating the navigation split view style

- [init()](/documentation/swiftui/prominentdetailnavigationsplitviewstyle/init())
- [NavigationSplitViewStyleConfiguration](/documentation/swiftui/navigationsplitviewstyleconfiguration)
- [func tabViewStyle<S>(S) -> some View](/documentation/swiftui/view/tabviewstyle(_:))
- [TabViewStyle](/documentation/swiftui/tabviewstyle)

#### Getting built-in tab view styles

- [static var automatic: DefaultTabViewStyle](/documentation/swiftui/tabviewstyle/automatic)
- [static var sidebarAdaptable: SidebarAdaptableTabViewStyle](/documentation/swiftui/tabviewstyle/sidebaradaptable)
- [static var tabBarOnly: TabBarOnlyTabViewStyle](/documentation/swiftui/tabviewstyle/tabbaronly)
- [static var grouped: GroupedTabViewStyle](/documentation/swiftui/tabviewstyle/grouped)
- [static var page: PageTabViewStyle](/documentation/swiftui/tabviewstyle/page)
- [static func page(indexDisplayMode: PageTabViewStyle.IndexDisplayMode) -> PageTabViewStyle](/documentation/swiftui/tabviewstyle/page(indexdisplaymode:))
- [static var verticalPage: VerticalPageTabViewStyle](/documentation/swiftui/tabviewstyle/verticalpage)
- [static func verticalPage(transitionStyle: VerticalPageTabViewStyle.TransitionStyle) -> VerticalPageTabViewStyle](/documentation/swiftui/tabviewstyle/verticalpage(transitionstyle:))
- [static var carousel: CarouselTabViewStyle](/documentation/swiftui/tabviewstyle/carousel)

#### Supporting types

- [DefaultTabViewStyle](/documentation/swiftui/defaulttabviewstyle)

##### Creating the tab view style

- [init()](/documentation/swiftui/defaulttabviewstyle/init())
- [SidebarAdaptableTabViewStyle](/documentation/swiftui/sidebaradaptabletabviewstyle)

##### Initializers

- [init()](/documentation/swiftui/sidebaradaptabletabviewstyle/init())
- [TabBarOnlyTabViewStyle](/documentation/swiftui/tabbaronlytabviewstyle)

##### Initializers

- [init()](/documentation/swiftui/tabbaronlytabviewstyle/init())
- [GroupedTabViewStyle](/documentation/swiftui/groupedtabviewstyle)

##### Initializers

- [init()](/documentation/swiftui/groupedtabviewstyle/init())
- [PageTabViewStyle](/documentation/swiftui/pagetabviewstyle)

##### Creating a page tab view style

- [init(indexDisplayMode: PageTabViewStyle.IndexDisplayMode)](/documentation/swiftui/pagetabviewstyle/init(indexdisplaymode:))
- [PageTabViewStyle.IndexDisplayMode](/documentation/swiftui/pagetabviewstyle/indexdisplaymode)

###### Getting the modes

- [static let always: PageTabViewStyle.IndexDisplayMode](/documentation/swiftui/pagetabviewstyle/indexdisplaymode/always)
- [static let automatic: PageTabViewStyle.IndexDisplayMode](/documentation/swiftui/pagetabviewstyle/indexdisplaymode/automatic)
- [static let never: PageTabViewStyle.IndexDisplayMode](/documentation/swiftui/pagetabviewstyle/indexdisplaymode/never)
- [VerticalPageTabViewStyle](/documentation/swiftui/verticalpagetabviewstyle)

##### Creating the tab view style

- [init()](/documentation/swiftui/verticalpagetabviewstyle/init())
- [init(transitionStyle: VerticalPageTabViewStyle.TransitionStyle)](/documentation/swiftui/verticalpagetabviewstyle/init(transitionstyle:))
- [VerticalPageTabViewStyle.TransitionStyle](/documentation/swiftui/verticalpagetabviewstyle/transitionstyle)

###### Getting the transition styles

- [static let automatic: VerticalPageTabViewStyle.TransitionStyle](/documentation/swiftui/verticalpagetabviewstyle/transitionstyle/automatic)
- [static let blur: VerticalPageTabViewStyle.TransitionStyle](/documentation/swiftui/verticalpagetabviewstyle/transitionstyle/blur)
- [static let identity: VerticalPageTabViewStyle.TransitionStyle](/documentation/swiftui/verticalpagetabviewstyle/transitionstyle/identity)
- [CarouselTabViewStyle](/documentation/swiftui/carouseltabviewstyle)

##### Creating the tab view style

- [init()](/documentation/swiftui/carouseltabviewstyle/init())

### Styling groups

- [func controlGroupStyle<S>(S) -> some View](/documentation/swiftui/view/controlgroupstyle(_:))
- [ControlGroupStyle](/documentation/swiftui/controlgroupstyle)

#### Getting built-in control group styles

- [static var automatic: AutomaticControlGroupStyle](/documentation/swiftui/controlgroupstyle/automatic)
- [static var compactMenu: CompactMenuControlGroupStyle](/documentation/swiftui/controlgroupstyle/compactmenu)
- [static var menu: MenuControlGroupStyle](/documentation/swiftui/controlgroupstyle/menu)
- [static var navigation: NavigationControlGroupStyle](/documentation/swiftui/controlgroupstyle/navigation)
- [static var palette: PaletteControlGroupStyle](/documentation/swiftui/controlgroupstyle/palette)

#### Creating custom control group styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/controlgroupstyle/makebody(configuration:))
- [ControlGroupStyle.Configuration](/documentation/swiftui/controlgroupstyle/configuration)
- [Body](/documentation/swiftui/controlgroupstyle/body)

#### Supporting types

- [AutomaticControlGroupStyle](/documentation/swiftui/automaticcontrolgroupstyle)
- [CompactMenuControlGroupStyle](/documentation/swiftui/compactmenucontrolgroupstyle)

##### Creating the control group style

- [init()](/documentation/swiftui/compactmenucontrolgroupstyle/init())
- [MenuControlGroupStyle](/documentation/swiftui/menucontrolgroupstyle)

##### Creating the control group style

- [init()](/documentation/swiftui/menucontrolgroupstyle/init())
- [NavigationControlGroupStyle](/documentation/swiftui/navigationcontrolgroupstyle)

##### Creating the control group style

- [init()](/documentation/swiftui/navigationcontrolgroupstyle/init())
- [PaletteControlGroupStyle](/documentation/swiftui/palettecontrolgroupstyle)

##### Creating the control group style

- [init()](/documentation/swiftui/palettecontrolgroupstyle/init())
- [ControlGroupStyleConfiguration](/documentation/swiftui/controlgroupstyleconfiguration)

#### Configuring the label

- [let label: ControlGroupStyleConfiguration.Label](/documentation/swiftui/controlgroupstyleconfiguration/label-swift.property)
- [ControlGroupStyleConfiguration.Label](/documentation/swiftui/controlgroupstyleconfiguration/label-swift.struct)

#### Configuring the content

- [let content: ControlGroupStyleConfiguration.Content](/documentation/swiftui/controlgroupstyleconfiguration/content-swift.property)
- [ControlGroupStyleConfiguration.Content](/documentation/swiftui/controlgroupstyleconfiguration/content-swift.struct)
- [func formStyle<S>(S) -> some View](/documentation/swiftui/view/formstyle(_:))
- [FormStyle](/documentation/swiftui/formstyle)

#### Getting built-in form styles

- [static var automatic: AutomaticFormStyle](/documentation/swiftui/formstyle/automatic)
- [static var columns: ColumnsFormStyle](/documentation/swiftui/formstyle/columns)
- [static var grouped: GroupedFormStyle](/documentation/swiftui/formstyle/grouped)

#### Creating custom form styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/formstyle/makebody(configuration:))
- [FormStyle.Configuration](/documentation/swiftui/formstyle/configuration)
- [Body](/documentation/swiftui/formstyle/body)

#### Supporting types

- [AutomaticFormStyle](/documentation/swiftui/automaticformstyle)

##### Creating the form style

- [init()](/documentation/swiftui/automaticformstyle/init())
- [ColumnsFormStyle](/documentation/swiftui/columnsformstyle)

##### Creating the form style

- [init()](/documentation/swiftui/columnsformstyle/init())
- [GroupedFormStyle](/documentation/swiftui/groupedformstyle)

##### Creating the form style

- [init()](/documentation/swiftui/groupedformstyle/init())
- [FormStyleConfiguration](/documentation/swiftui/formstyleconfiguration)

#### Getting configuration content

- [let content: FormStyleConfiguration.Content](/documentation/swiftui/formstyleconfiguration/content-swift.property)
- [FormStyleConfiguration.Content](/documentation/swiftui/formstyleconfiguration/content-swift.struct)
- [func groupBoxStyle<S>(S) -> some View](/documentation/swiftui/view/groupboxstyle(_:))
- [GroupBoxStyle](/documentation/swiftui/groupboxstyle)

#### Getting built-in group box styles

- [static var automatic: DefaultGroupBoxStyle](/documentation/swiftui/groupboxstyle/automatic)

#### Creating custom group box styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/groupboxstyle/makebody(configuration:))
- [GroupBoxStyle.Configuration](/documentation/swiftui/groupboxstyle/configuration)
- [Body](/documentation/swiftui/groupboxstyle/body)

#### Supporting types

- [DefaultGroupBoxStyle](/documentation/swiftui/defaultgroupboxstyle)

##### Creating the group box style

- [init()](/documentation/swiftui/defaultgroupboxstyle/init())
- [GroupBoxStyleConfiguration](/documentation/swiftui/groupboxstyleconfiguration)

#### Configuring the label

- [let label: GroupBoxStyleConfiguration.Label](/documentation/swiftui/groupboxstyleconfiguration/label-swift.property)
- [GroupBoxStyleConfiguration.Label](/documentation/swiftui/groupboxstyleconfiguration/label-swift.struct)

#### Configuring the content

- [let content: GroupBoxStyleConfiguration.Content](/documentation/swiftui/groupboxstyleconfiguration/content-swift.property)
- [GroupBoxStyleConfiguration.Content](/documentation/swiftui/groupboxstyleconfiguration/content-swift.struct)
- [func indexViewStyle<S>(S) -> some View](/documentation/swiftui/view/indexviewstyle(_:))
- [IndexViewStyle](/documentation/swiftui/indexviewstyle)

#### Getting built-in index view styles

- [static var page: PageIndexViewStyle](/documentation/swiftui/indexviewstyle/page)
- [static func page(backgroundDisplayMode: PageIndexViewStyle.BackgroundDisplayMode) -> PageIndexViewStyle](/documentation/swiftui/indexviewstyle/page(backgrounddisplaymode:))

#### Supporting types

- [PageIndexViewStyle](/documentation/swiftui/pageindexviewstyle)

##### Creating the control group style

- [init(backgroundDisplayMode: PageIndexViewStyle.BackgroundDisplayMode)](/documentation/swiftui/pageindexviewstyle/init(backgrounddisplaymode:))
- [PageIndexViewStyle.BackgroundDisplayMode](/documentation/swiftui/pageindexviewstyle/backgrounddisplaymode)

###### Getting the display modes

- [static let automatic: PageIndexViewStyle.BackgroundDisplayMode](/documentation/swiftui/pageindexviewstyle/backgrounddisplaymode/automatic)
- [static let always: PageIndexViewStyle.BackgroundDisplayMode](/documentation/swiftui/pageindexviewstyle/backgrounddisplaymode/always)
- [static let interactive: PageIndexViewStyle.BackgroundDisplayMode](/documentation/swiftui/pageindexviewstyle/backgrounddisplaymode/interactive)
- [static let never: PageIndexViewStyle.BackgroundDisplayMode](/documentation/swiftui/pageindexviewstyle/backgrounddisplaymode/never)
- [func labeledContentStyle<S>(S) -> some View](/documentation/swiftui/view/labeledcontentstyle(_:))
- [LabeledContentStyle](/documentation/swiftui/labeledcontentstyle)

#### Getting built-in labeled content styles

- [static var automatic: AutomaticLabeledContentStyle](/documentation/swiftui/labeledcontentstyle/automatic)

#### Creating custom labeled content styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/labeledcontentstyle/makebody(configuration:))
- [LabeledContentStyle.Configuration](/documentation/swiftui/labeledcontentstyle/configuration)
- [Body](/documentation/swiftui/labeledcontentstyle/body)

#### Supporting types

- [AutomaticLabeledContentStyle](/documentation/swiftui/automaticlabeledcontentstyle)

##### Creating the labeled content style

- [init()](/documentation/swiftui/automaticlabeledcontentstyle/init())
- [LabeledContentStyleConfiguration](/documentation/swiftui/labeledcontentstyleconfiguration)

#### Configuring the label

- [let label: LabeledContentStyleConfiguration.Label](/documentation/swiftui/labeledcontentstyleconfiguration/label-swift.property)
- [LabeledContentStyleConfiguration.Label](/documentation/swiftui/labeledcontentstyleconfiguration/label-swift.struct)

#### Configuring the content

- [let content: LabeledContentStyleConfiguration.Content](/documentation/swiftui/labeledcontentstyleconfiguration/content-swift.property)
- [LabeledContentStyleConfiguration.Content](/documentation/swiftui/labeledcontentstyleconfiguration/content-swift.struct)

### Styling windows from a view inside the window

- [func presentedWindowStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowstyle(_:))
- [func presentedWindowToolbarStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowtoolbarstyle(_:))

### Adding a glass background on views in visionOS

- [func glassBackgroundEffect(displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(displaymode:))
- [func glassBackgroundEffect<S>(in: S, displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(in:displaymode:))
- [GlassBackgroundDisplayMode](/documentation/swiftui/glassbackgrounddisplaymode)

#### Getting the mode

- [case always](/documentation/swiftui/glassbackgrounddisplaymode/always)
- [case implicit](/documentation/swiftui/glassbackgrounddisplaymode/implicit)
- [case never](/documentation/swiftui/glassbackgrounddisplaymode/never)
- [GlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect)

#### Associated Types

- [Body](/documentation/swiftui/glassbackgroundeffect/body)

#### Instance Methods

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/glassbackgroundeffect/makebody(configuration:))

#### Type Aliases

- [GlassBackgroundEffect.Configuration](/documentation/swiftui/glassbackgroundeffect/configuration)

#### Type Properties

- [static var automatic: AutomaticGlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect/automatic)
- [static var feathered: FeatheredGlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect/feathered)
- [static var plate: PlateGlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect/plate)

#### Type Methods

- [static func feathered(padding: CGFloat, softEdgeRadius: CGFloat?) -> FeatheredGlassBackgroundEffect](/documentation/swiftui/glassbackgroundeffect/feathered(padding:softedgeradius:))
- [AutomaticGlassBackgroundEffect](/documentation/swiftui/automaticglassbackgroundeffect)

#### Initializers

- [init()](/documentation/swiftui/automaticglassbackgroundeffect/init())
- [GlassBackgroundEffectConfiguration](/documentation/swiftui/glassbackgroundeffectconfiguration)

#### Structures

- [GlassBackgroundEffectConfiguration.Content](/documentation/swiftui/glassbackgroundeffectconfiguration/content-swift.struct)

#### Instance Properties

- [let content: GlassBackgroundEffectConfiguration.Content](/documentation/swiftui/glassbackgroundeffectconfiguration/content-swift.property)
- [FeatheredGlassBackgroundEffect](/documentation/swiftui/featheredglassbackgroundeffect)

#### Initializers

- [init()](/documentation/swiftui/featheredglassbackgroundeffect/init())
- [init(padding: CGFloat, softEdgeRadius: CGFloat?)](/documentation/swiftui/featheredglassbackgroundeffect/init(padding:softedgeradius:))
- [PlateGlassBackgroundEffect](/documentation/swiftui/plateglassbackgroundeffect)

#### Initializers

- [init()](/documentation/swiftui/plateglassbackgroundeffect/init())
- [Animations](/documentation/swiftui/animations)

### Adding state-based animation to an action

- [func withAnimation<Result>(Animation?, () throws -> Result) rethrows -> Result](/documentation/swiftui/withanimation(_:_:))
- [func withAnimation<Result>(Animation?, completionCriteria: AnimationCompletionCriteria, () throws -> Result, completion: () -> Void) rethrows -> Result](/documentation/swiftui/withanimation(_:completioncriteria:_:completion:))
- [AnimationCompletionCriteria](/documentation/swiftui/animationcompletioncriteria)

#### Getting the completion criteria

- [static let logicallyComplete: AnimationCompletionCriteria](/documentation/swiftui/animationcompletioncriteria/logicallycomplete)
- [static let removed: AnimationCompletionCriteria](/documentation/swiftui/animationcompletioncriteria/removed)
- [Animation](/documentation/swiftui/animation)

#### Getting the default animation

- [static let `default`: Animation](/documentation/swiftui/animation/default)

#### Getting linear animations

- [static var linear: Animation](/documentation/swiftui/animation/linear)
- [static func linear(duration: TimeInterval) -> Animation](/documentation/swiftui/animation/linear(duration:))

#### Getting eased animations

- [static var easeIn: Animation](/documentation/swiftui/animation/easein)
- [static func easeIn(duration: TimeInterval) -> Animation](/documentation/swiftui/animation/easein(duration:))
- [static var easeOut: Animation](/documentation/swiftui/animation/easeout)
- [static func easeOut(duration: TimeInterval) -> Animation](/documentation/swiftui/animation/easeout(duration:))
- [static var easeInOut: Animation](/documentation/swiftui/animation/easeinout)
- [static func easeInOut(duration: TimeInterval) -> Animation](/documentation/swiftui/animation/easeinout(duration:))

#### Getting built-in spring animations

- [static var bouncy: Animation](/documentation/swiftui/animation/bouncy)
- [static func bouncy(duration: TimeInterval, extraBounce: Double) -> Animation](/documentation/swiftui/animation/bouncy(duration:extrabounce:))
- [static var smooth: Animation](/documentation/swiftui/animation/smooth)
- [static func smooth(duration: TimeInterval, extraBounce: Double) -> Animation](/documentation/swiftui/animation/smooth(duration:extrabounce:))
- [static var snappy: Animation](/documentation/swiftui/animation/snappy)
- [static func snappy(duration: TimeInterval, extraBounce: Double) -> Animation](/documentation/swiftui/animation/snappy(duration:extrabounce:))

#### Customizing spring animations

- [static var spring: Animation](/documentation/swiftui/animation/spring)
- [static func spring(Spring, blendDuration: TimeInterval) -> Animation](/documentation/swiftui/animation/spring(_:blendduration:))
- [static func spring(duration: TimeInterval, bounce: Double, blendDuration: Double) -> Animation](/documentation/swiftui/animation/spring(duration:bounce:blendduration:))
- [static func spring(response: Double, dampingFraction: Double, blendDuration: TimeInterval) -> Animation](/documentation/swiftui/animation/spring(response:dampingfraction:blendduration:))
- [static var interactiveSpring: Animation](/documentation/swiftui/animation/interactivespring)
- [static func interactiveSpring(response: Double, dampingFraction: Double, blendDuration: TimeInterval) -> Animation](/documentation/swiftui/animation/interactivespring(response:dampingfraction:blendduration:))
- [static var interpolatingSpring: Animation](/documentation/swiftui/animation/interpolatingspring)
- [static func interpolatingSpring(Spring, initialVelocity: Double) -> Animation](/documentation/swiftui/animation/interpolatingspring(_:initialvelocity:))
- [static func interpolatingSpring(duration: TimeInterval, bounce: Double, initialVelocity: Double) -> Animation](/documentation/swiftui/animation/interpolatingspring(duration:bounce:initialvelocity:))
- [static func interpolatingSpring(mass: Double, stiffness: Double, damping: Double, initialVelocity: Double) -> Animation](/documentation/swiftui/animation/interpolatingspring(mass:stiffness:damping:initialvelocity:))

#### Creating custom animations

- [init<A>(A)](/documentation/swiftui/animation/init(_:))
- [static func timingCurve(UnitCurve, duration: TimeInterval) -> Animation](/documentation/swiftui/animation/timingcurve(_:duration:))
- [static func timingCurve(Double, Double, Double, Double, duration: TimeInterval) -> Animation](/documentation/swiftui/animation/timingcurve(_:_:_:_:duration:))

#### Configuring an animation

- [func delay(TimeInterval) -> Animation](/documentation/swiftui/animation/delay(_:))
- [func repeatCount(Int, autoreverses: Bool) -> Animation](/documentation/swiftui/animation/repeatcount(_:autoreverses:))
- [func repeatForever(autoreverses: Bool) -> Animation](/documentation/swiftui/animation/repeatforever(autoreverses:))
- [func speed(Double) -> Animation](/documentation/swiftui/animation/speed(_:))

#### Instance Properties

- [var base: any CustomAnimation](/documentation/swiftui/animation/base)

#### Instance Methods

- [func animate<V>(value: V, time: TimeInterval, context: inout AnimationContext<V>) -> V?](/documentation/swiftui/animation/animate(value:time:context:))
- [func logicallyComplete(after: TimeInterval) -> Animation](/documentation/swiftui/animation/logicallycomplete(after:))
- [func shouldMerge<V>(previous: Animation, value: V, time: TimeInterval, context: inout AnimationContext<V>) -> Bool](/documentation/swiftui/animation/shouldmerge(previous:value:time:context:))
- [func velocity<V>(value: V, time: TimeInterval, context: AnimationContext<V>) -> V?](/documentation/swiftui/animation/velocity(value:time:context:))

#### Type Properties

- [static var systemOverlayAppearance: Animation](/documentation/swiftui/animation/systemoverlayappearance)
- [static var systemOverlayDelayedDisappearance: Animation](/documentation/swiftui/animation/systemoverlaydelayeddisappearance)
- [static var systemOverlayDisappearance: Animation](/documentation/swiftui/animation/systemoverlaydisappearance)
- [static var systemOverlayDisappearanceDelay: TimeInterval](/documentation/swiftui/animation/systemoverlaydisappearancedelay)

#### Type Methods

- [static func interactiveSpring(duration: TimeInterval, extraBounce: Double, blendDuration: TimeInterval) -> Animation](/documentation/swiftui/animation/interactivespring(duration:extrabounce:blendduration:))

### Adding state-based animation to a view

- [func animation(_:)](/documentation/swiftui/view/animation(_:))
- [func animation<V>(Animation?, value: V) -> some View](/documentation/swiftui/view/animation(_:value:))
- [func animation<V>(Animation?, body: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/animation(_:body:))

### Creating phase-based animation

- [Controlling the timing and movements of your animations](/documentation/swiftui/controlling-the-timing-and-movements-of-your-animations)
- [func phaseAnimator<Phase>(some Sequence, content: (PlaceholderContentView<Self>, Phase) -> some View, animation: (Phase) -> Animation?) -> some View](/documentation/swiftui/view/phaseanimator(_:content:animation:))
- [func phaseAnimator<Phase>(some Sequence, trigger: some Equatable, content: (PlaceholderContentView<Self>, Phase) -> some View, animation: (Phase) -> Animation?) -> some View](/documentation/swiftui/view/phaseanimator(_:trigger:content:animation:))
- [PhaseAnimator](/documentation/swiftui/phaseanimator)

#### Creating a phase animator

- [init(some Sequence<Phase>, content: (Phase) -> Content, animation: (Phase) -> Animation?)](/documentation/swiftui/phaseanimator/init(_:content:animation:))
- [init(some Sequence<Phase>, trigger: some Equatable, content: (Phase) -> Content, animation: (Phase) -> Animation?)](/documentation/swiftui/phaseanimator/init(_:trigger:content:animation:))

### Creating keyframe-based animation

- [func keyframeAnimator<Value>(initialValue: Value, repeating: Bool, content: (PlaceholderContentView<Self>, Value) -> some View, keyframes: (Value) -> some Keyframes) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:repeating:content:keyframes:))
- [func keyframeAnimator<Value>(initialValue: Value, trigger: some Equatable, content: (PlaceholderContentView<Self>, Value) -> some View, keyframes: (Value) -> some Keyframes) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:trigger:content:keyframes:))
- [KeyframeAnimator](/documentation/swiftui/keyframeanimator)

#### Creating a phase animator

- [init(initialValue: Value, repeating: Bool, content: (Value) -> Content, keyframes: (Value) -> KeyframePath)](/documentation/swiftui/keyframeanimator/init(initialvalue:repeating:content:keyframes:))
- [init(initialValue: Value, trigger: some Equatable, content: (Value) -> Content, keyframes: (Value) -> KeyframePath)](/documentation/swiftui/keyframeanimator/init(initialvalue:trigger:content:keyframes:))
- [Keyframes](/documentation/swiftui/keyframes)

#### Creating a keyframe

- [var body: Self.Body](/documentation/swiftui/keyframes/body-swift.property)
- [Body](/documentation/swiftui/keyframes/body-swift.associatedtype)
- [Value](/documentation/swiftui/keyframes/value)
- [KeyframeTimeline](/documentation/swiftui/keyframetimeline)

#### Creating a keyframe timeline

- [init(initialValue: Value, content: () -> some Keyframes<Value>)](/documentation/swiftui/keyframetimeline/init(initialvalue:content:))

#### Getting the duration

- [var duration: TimeInterval](/documentation/swiftui/keyframetimeline/duration)

#### Getting an interpolated value

- [func value(time: Double) -> Value](/documentation/swiftui/keyframetimeline/value(time:))
- [func value(progress: Double) -> Value](/documentation/swiftui/keyframetimeline/value(progress:))
- [KeyframeTrack](/documentation/swiftui/keyframetrack)

#### Creating a keyframe track

- [init(content: () -> Content)](/documentation/swiftui/keyframetrack/init(content:))
- [init(WritableKeyPath<Root, Value>, content: () -> Content)](/documentation/swiftui/keyframetrack/init(_:content:))
- [KeyframeTrackContentBuilder](/documentation/swiftui/keyframetrackcontentbuilder)

#### Building keyframe track content

- [static func buildArray([some KeyframeTrackContent<Value>]) -> some KeyframeTrackContent<Value>
](/documentation/swiftui/keyframetrackcontentbuilder/buildarray(_:))
- [static func buildBlock() -> some KeyframeTrackContent<Value>
](/documentation/swiftui/keyframetrackcontentbuilder/buildblock())
- [static func buildEither<First, Second>(first: First) -> KeyframeTrackContentBuilder<Value>.Conditional<Value, First, Second>](/documentation/swiftui/keyframetrackcontentbuilder/buildeither(first:))
- [static func buildEither<First, Second>(second: Second) -> KeyframeTrackContentBuilder<Value>.Conditional<Value, First, Second>](/documentation/swiftui/keyframetrackcontentbuilder/buildeither(second:))
- [static func buildExpression<K>(K) -> K](/documentation/swiftui/keyframetrackcontentbuilder/buildexpression(_:))
- [static func buildPartialBlock(accumulated: some KeyframeTrackContent<Value>, next: some KeyframeTrackContent<Value>) -> some KeyframeTrackContent<Value>
](/documentation/swiftui/keyframetrackcontentbuilder/buildpartialblock(accumulated:next:))
- [static func buildPartialBlock<K>(first: K) -> K](/documentation/swiftui/keyframetrackcontentbuilder/buildpartialblock(first:))
- [KeyframeTrackContentBuilder.Conditional](/documentation/swiftui/keyframetrackcontentbuilder/conditional)
- [KeyframesBuilder](/documentation/swiftui/keyframesbuilder)

#### Building keyframes

- [static func buildArray([some KeyframeTrackContent<Value>]) -> some KeyframeTrackContent<Value>
](/documentation/swiftui/keyframesbuilder/buildarray(_:))
- [static buildBlock()](/documentation/swiftui/keyframesbuilder/buildblock())
- [static func buildEither<First, Second>(first: First) -> KeyframeTrackContentBuilder<Value>.Conditional<Value, First, Second>](/documentation/swiftui/keyframesbuilder/buildeither(first:))
- [static func buildEither<First, Second>(second: Second) -> KeyframeTrackContentBuilder<Value>.Conditional<Value, First, Second>](/documentation/swiftui/keyframesbuilder/buildeither(second:))
- [static buildExpression(_:)](/documentation/swiftui/keyframesbuilder/buildexpression(_:))
- [static buildFinalResult(_:)](/documentation/swiftui/keyframesbuilder/buildfinalresult(_:))
- [static buildPartialBlock(accumulated:next:)](/documentation/swiftui/keyframesbuilder/buildpartialblock(accumulated:next:))
- [static buildPartialBlock(first:)](/documentation/swiftui/keyframesbuilder/buildpartialblock(first:))
- [KeyframeTrackContent](/documentation/swiftui/keyframetrackcontent)

#### Creating a keyframe

- [var body: Self.Body](/documentation/swiftui/keyframetrackcontent/body-swift.property)
- [Body](/documentation/swiftui/keyframetrackcontent/body-swift.associatedtype)
- [Value](/documentation/swiftui/keyframetrackcontent/value)
- [CubicKeyframe](/documentation/swiftui/cubickeyframe)

#### Creating the keyframe

- [init(Value, duration: TimeInterval, startVelocity: Value?, endVelocity: Value?)](/documentation/swiftui/cubickeyframe/init(_:duration:startvelocity:endvelocity:))
- [LinearKeyframe](/documentation/swiftui/linearkeyframe)

#### Creating the keyframe

- [init(Value, duration: TimeInterval, timingCurve: UnitCurve)](/documentation/swiftui/linearkeyframe/init(_:duration:timingcurve:))
- [MoveKeyframe](/documentation/swiftui/movekeyframe)

#### Creating the keyframe

- [init(Value)](/documentation/swiftui/movekeyframe/init(_:))
- [SpringKeyframe](/documentation/swiftui/springkeyframe)

#### Creating the keyframe

- [init(Value, duration: TimeInterval?, spring: Spring, startVelocity: Value?)](/documentation/swiftui/springkeyframe/init(_:duration:spring:startvelocity:))

### Creating custom animations

- [CustomAnimation](/documentation/swiftui/customanimation)

#### Animating a value

- [func animate<V>(value: V, time: TimeInterval, context: inout AnimationContext<V>) -> V?](/documentation/swiftui/customanimation/animate(value:time:context:))

#### Getting the velocity

- [func velocity<V>(value: V, time: TimeInterval, context: AnimationContext<V>) -> V?](/documentation/swiftui/customanimation/velocity(value:time:context:))

#### Determining whether to merge

- [func shouldMerge<V>(previous: Animation, value: V, time: TimeInterval, context: inout AnimationContext<V>) -> Bool](/documentation/swiftui/customanimation/shouldmerge(previous:value:time:context:))
- [AnimationContext](/documentation/swiftui/animationcontext)

#### Managing state

- [var state: AnimationState<Value>](/documentation/swiftui/animationcontext/state)

#### Retrieving view environment values

- [var environment: EnvironmentValues](/documentation/swiftui/animationcontext/environment)

#### Creating context

- [func withState<T>(AnimationState<T>) -> AnimationContext<T>](/documentation/swiftui/animationcontext/withstate(_:))

#### Instance Properties

- [var isLogicallyComplete: Bool](/documentation/swiftui/animationcontext/islogicallycomplete)
- [AnimationState](/documentation/swiftui/animationstate)

#### Creating animation state

- [init()](/documentation/swiftui/animationstate/init())

#### Accessing custom keys

- [subscript<K>(K.Type) -> K.Value](/documentation/swiftui/animationstate/subscript(_:))
- [AnimationStateKey](/documentation/swiftui/animationstatekey)

#### Setting the default value

- [static var defaultValue: Self.Value](/documentation/swiftui/animationstatekey/defaultvalue)
- [Value](/documentation/swiftui/animationstatekey/value)
- [UnitCurve](/documentation/swiftui/unitcurve)

#### Getting a linear curve

- [static let linear: UnitCurve](/documentation/swiftui/unitcurve/linear)

#### Getting easing curves

- [static let easeIn: UnitCurve](/documentation/swiftui/unitcurve/easein)
- [static let easeOut: UnitCurve](/documentation/swiftui/unitcurve/easeout)
- [static let easeInOut: UnitCurve](/documentation/swiftui/unitcurve/easeinout)
- [static let circularEaseIn: UnitCurve](/documentation/swiftui/unitcurve/circulareasein)
- [static let circularEaseOut: UnitCurve](/documentation/swiftui/unitcurve/circulareaseout)
- [static let circularEaseInOut: UnitCurve](/documentation/swiftui/unitcurve/circulareaseinout)

#### Creating a general Bezier curve

- [static func bezier(startControlPoint: UnitPoint, endControlPoint: UnitPoint) -> UnitCurve](/documentation/swiftui/unitcurve/bezier(startcontrolpoint:endcontrolpoint:))

#### Inverting a curve

- [var inverse: UnitCurve](/documentation/swiftui/unitcurve/inverse)

#### Getting curve characteristics

- [func value(at: Double) -> Double](/documentation/swiftui/unitcurve/value(at:))
- [func velocity(at: Double) -> Double](/documentation/swiftui/unitcurve/velocity(at:))

#### Deprecated symbols

- [static let easeInEaseOut: UnitCurve](/documentation/swiftui/unitcurve/easeineaseout)
- [Spring](/documentation/swiftui/spring)

#### Creating a spring

- [init(duration: TimeInterval, bounce: Double)](/documentation/swiftui/spring/init(duration:bounce:))
- [init(mass: Double, stiffness: Double, damping: Double, allowOverDamping: Bool)](/documentation/swiftui/spring/init(mass:stiffness:damping:allowoverdamping:))
- [init(response: Double, dampingRatio: Double)](/documentation/swiftui/spring/init(response:dampingratio:))
- [init(settlingDuration: TimeInterval, dampingRatio: Double, epsilon: Double)](/documentation/swiftui/spring/init(settlingduration:dampingratio:epsilon:))

#### Getting built-in springs

- [static var bouncy: Spring](/documentation/swiftui/spring/bouncy)
- [static func bouncy(duration: TimeInterval, extraBounce: Double) -> Spring](/documentation/swiftui/spring/bouncy(duration:extrabounce:))
- [static var smooth: Spring](/documentation/swiftui/spring/smooth)
- [static func smooth(duration: TimeInterval, extraBounce: Double) -> Spring](/documentation/swiftui/spring/smooth(duration:extrabounce:))
- [static var snappy: Spring](/documentation/swiftui/spring/snappy)
- [static func snappy(duration: TimeInterval, extraBounce: Double) -> Spring](/documentation/swiftui/spring/snappy(duration:extrabounce:))

#### Getting spring characteristics

- [var bounce: Double](/documentation/swiftui/spring/bounce)
- [var damping: Double](/documentation/swiftui/spring/damping)
- [var dampingRatio: Double](/documentation/swiftui/spring/dampingratio)
- [var duration: TimeInterval](/documentation/swiftui/spring/duration)
- [var mass: Double](/documentation/swiftui/spring/mass)
- [var response: Double](/documentation/swiftui/spring/response)
- [var settlingDuration: TimeInterval](/documentation/swiftui/spring/settlingduration)
- [var stiffness: Double](/documentation/swiftui/spring/stiffness)

#### Getting spring state

- [func value<V>(target: V, initialVelocity: V, time: TimeInterval) -> V](/documentation/swiftui/spring/value(target:initialvelocity:time:))
- [func value<V>(fromValue: V, toValue: V, initialVelocity: V, time: TimeInterval) -> V](/documentation/swiftui/spring/value(fromvalue:tovalue:initialvelocity:time:))
- [func velocity<V>(target: V, initialVelocity: V, time: TimeInterval) -> V](/documentation/swiftui/spring/velocity(target:initialvelocity:time:))
- [func velocity<V>(fromValue: V, toValue: V, initialVelocity: V, time: TimeInterval) -> V](/documentation/swiftui/spring/velocity(fromvalue:tovalue:initialvelocity:time:))

#### Setting spring state

- [func update<V>(value: inout V, velocity: inout V, target: V, deltaTime: TimeInterval)](/documentation/swiftui/spring/update(value:velocity:target:deltatime:))

#### Calculating forces and durations

- [func force<V>(target: V, position: V, velocity: V) -> V](/documentation/swiftui/spring/force(target:position:velocity:))
- [func force<V>(fromValue: V, toValue: V, position: V, velocity: V) -> V](/documentation/swiftui/spring/force(fromvalue:tovalue:position:velocity:))
- [func settlingDuration<V>(target: V, initialVelocity: V, epsilon: Double) -> TimeInterval](/documentation/swiftui/spring/settlingduration(target:initialvelocity:epsilon:))
- [func settlingDuration<V>(fromValue: V, toValue: V, initialVelocity: V, epsilon: Double) -> TimeInterval](/documentation/swiftui/spring/settlingduration(fromvalue:tovalue:initialvelocity:epsilon:))

### Making data animatable

- [Animatable](/documentation/swiftui/animatable)

#### Animating data

- [macro Animatable()](/documentation/swiftui/animatable())
- [macro AnimatableIgnored()](/documentation/swiftui/animatableignored())
- [var animatableData: Self.AnimatableData](/documentation/swiftui/animatable/animatabledata-6nydg)
- [AnimatableData](/documentation/swiftui/animatable/animatabledata-swift.associatedtype)
- [AnimatableValues](/documentation/swiftui/animatablevalues)

#### Initializers

- [init(repeat each Value)](/documentation/swiftui/animatablevalues/init(_:))

#### Instance Properties

- [var magnitudeSquared: Double](/documentation/swiftui/animatablevalues/magnitudesquared)
- [var value: (repeat each Value)](/documentation/swiftui/animatablevalues/value)
- [AnimatablePair](/documentation/swiftui/animatablepair)

#### Creating an animatable pair

- [init(First, Second)](/documentation/swiftui/animatablepair/init(_:_:))

#### Getting the constituent animations

- [var first: First](/documentation/swiftui/animatablepair/first)
- [var second: Second](/documentation/swiftui/animatablepair/second)

#### Manipulating values

- [var magnitudeSquared: Double](/documentation/swiftui/animatablepair/magnitudesquared)
- [VectorArithmetic](/documentation/swiftui/vectorarithmetic)

#### Manipulating values

- [var magnitudeSquared: Double](/documentation/swiftui/vectorarithmetic/magnitudesquared)
- [func scale(by: Double)](/documentation/swiftui/vectorarithmetic/scale(by:))
- [func scaled(by: Double) -> Self](/documentation/swiftui/vectorarithmetic/scaled(by:))
- [func interpolate(towards: Self, amount: Double)](/documentation/swiftui/vectorarithmetic/interpolate(towards:amount:))
- [func interpolated(towards: Self, amount: Double) -> Self](/documentation/swiftui/vectorarithmetic/interpolated(towards:amount:))
- [EmptyAnimatableData](/documentation/swiftui/emptyanimatabledata)

#### Creating the data

- [init()](/documentation/swiftui/emptyanimatabledata/init())

#### Manipulating the data

- [var magnitudeSquared: Double](/documentation/swiftui/emptyanimatabledata/magnitudesquared)

### Updating a view on a schedule

- [Updating watchOS apps with timelines](/documentation/watchos-apps/updating-watchos-apps-with-timelines)
- [TimelineView](/documentation/swiftui/timelineview)

#### Creating a timeline

- [init(Schedule, content: (TimelineViewDefaultContext) -> Content)](/documentation/swiftui/timelineview/init(_:content:)-1mlmj)
- [TimelineView.Context](/documentation/swiftui/timelineview/context)

##### Getting the date

- [let date: Date](/documentation/swiftui/timelineview/context/date)

##### Getting the cadence

- [let cadence: TimelineView<Schedule, Content>.Context.Cadence](/documentation/swiftui/timelineview/context/cadence-swift.property)
- [TimelineView.Context.Cadence](/documentation/swiftui/timelineview/context/cadence-swift.enum)

###### Getting cadences

- [case live](/documentation/swiftui/timelineview/context/cadence-swift.enum/live)
- [case seconds](/documentation/swiftui/timelineview/context/cadence-swift.enum/seconds)
- [case minutes](/documentation/swiftui/timelineview/context/cadence-swift.enum/minutes)

##### Invalidating the context

- [func invalidateTimelineContent()](/documentation/swiftui/timelineview/context/invalidatetimelinecontent())

#### Deprecated symbols

- [init(Schedule, content: (TimelineView<Schedule, Content>.Context) -> Content)](/documentation/swiftui/timelineview/init(_:content:)-67h35)

#### Initializers

- [init(_:content:)](/documentation/swiftui/timelineview/init(_:content:))
- [TimelineSchedule](/documentation/swiftui/timelineschedule)

#### Getting built-in schedules

- [static var animation: AnimationTimelineSchedule](/documentation/swiftui/timelineschedule/animation)
- [static func animation(minimumInterval: Double?, paused: Bool) -> AnimationTimelineSchedule](/documentation/swiftui/timelineschedule/animation(minimuminterval:paused:))
- [static var everyMinute: EveryMinuteTimelineSchedule](/documentation/swiftui/timelineschedule/everyminute)
- [static func explicit<S>(S) -> ExplicitTimelineSchedule<S>](/documentation/swiftui/timelineschedule/explicit(_:))
- [static func periodic(from: Date, by: TimeInterval) -> PeriodicTimelineSchedule](/documentation/swiftui/timelineschedule/periodic(from:by:))

#### Getting a sequence of dates

- [func entries(from: Date, mode: Self.Mode) -> Self.Entries](/documentation/swiftui/timelineschedule/entries(from:mode:))
- [Entries](/documentation/swiftui/timelineschedule/entries)

#### Specifying a mode

- [TimelineSchedule.Mode](/documentation/swiftui/timelineschedule/mode)
- [TimelineScheduleMode](/documentation/swiftui/timelineschedulemode)

##### Getting timeline schedule modes

- [case normal](/documentation/swiftui/timelineschedulemode/normal)
- [case lowFrequency](/documentation/swiftui/timelineschedulemode/lowfrequency)

#### Supporting types

- [AnimationTimelineSchedule](/documentation/swiftui/animationtimelineschedule)

##### Creating a schedule

- [init(minimumInterval: Double?, paused: Bool)](/documentation/swiftui/animationtimelineschedule/init(minimuminterval:paused:))

##### Getting the sequence of dates

- [func entries(from: Date, mode: TimelineScheduleMode) -> AnimationTimelineSchedule.Entries](/documentation/swiftui/animationtimelineschedule/entries(from:mode:))
- [EveryMinuteTimelineSchedule](/documentation/swiftui/everyminutetimelineschedule)

##### Creating a schedule

- [init()](/documentation/swiftui/everyminutetimelineschedule/init())

##### Getting the sequence of dates

- [func entries(from: Date, mode: TimelineScheduleMode) -> EveryMinuteTimelineSchedule.Entries](/documentation/swiftui/everyminutetimelineschedule/entries(from:mode:))
- [EveryMinuteTimelineSchedule.Entries](/documentation/swiftui/everyminutetimelineschedule/entries)
- [ExplicitTimelineSchedule](/documentation/swiftui/explicittimelineschedule)

##### Creating a schedule

- [init(Entries)](/documentation/swiftui/explicittimelineschedule/init(_:))

##### Getting the sequence of dates

- [func entries(from: Date, mode: TimelineScheduleMode) -> Entries](/documentation/swiftui/explicittimelineschedule/entries(from:mode:))
- [PeriodicTimelineSchedule](/documentation/swiftui/periodictimelineschedule)

##### Creating a schedule

- [init(from: Date, by: TimeInterval)](/documentation/swiftui/periodictimelineschedule/init(from:by:))

##### Getting the sequence of dates

- [func entries(from: Date, mode: TimelineScheduleMode) -> PeriodicTimelineSchedule.Entries](/documentation/swiftui/periodictimelineschedule/entries(from:mode:))
- [PeriodicTimelineSchedule.Entries](/documentation/swiftui/periodictimelineschedule/entries)
- [TimelineViewDefaultContext](/documentation/swiftui/timelineviewdefaultcontext)

### Synchronizing geometries

- [func matchedGeometryEffect<ID>(id: ID, in: Namespace.ID, properties: MatchedGeometryProperties, anchor: UnitPoint, isSource: Bool) -> some View](/documentation/swiftui/view/matchedgeometryeffect(id:in:properties:anchor:issource:))
- [MatchedGeometryProperties](/documentation/swiftui/matchedgeometryproperties)

#### Matching properties

- [static let frame: MatchedGeometryProperties](/documentation/swiftui/matchedgeometryproperties/frame)
- [static let position: MatchedGeometryProperties](/documentation/swiftui/matchedgeometryproperties/position)
- [static let size: MatchedGeometryProperties](/documentation/swiftui/matchedgeometryproperties/size)
- [GeometryEffect](/documentation/swiftui/geometryeffect)

#### Applying effects

- [func effectValue(size: CGSize) -> ProjectionTransform](/documentation/swiftui/geometryeffect/effectvalue(size:))
- [func ignoredByLayout() -> _IgnoredByLayoutEffect<Self>](/documentation/swiftui/geometryeffect/ignoredbylayout())
- [Namespace](/documentation/swiftui/namespace)

#### Creating a namespace

- [init()](/documentation/swiftui/namespace/init())

#### Getting the namespace

- [var wrappedValue: Namespace.ID](/documentation/swiftui/namespace/wrappedvalue)
- [Namespace.ID](/documentation/swiftui/namespace/id)
- [func geometryGroup() -> some View](/documentation/swiftui/view/geometrygroup())

### Defining transitions

- [func transition(_:)](/documentation/swiftui/view/transition(_:))
- [Transition](/documentation/swiftui/transition)

#### Getting built-in transitions

- [static var blurReplace: BlurReplaceTransition](/documentation/swiftui/transition/blurreplace)
- [static func blurReplace(BlurReplaceTransition.Configuration) -> Self](/documentation/swiftui/transition/blurreplace(_:))
- [static var identity: IdentityTransition](/documentation/swiftui/transition/identity)
- [static func move(edge: Edge) -> Self](/documentation/swiftui/transition/move(edge:))
- [static func offset(CGSize) -> Self](/documentation/swiftui/transition/offset(_:))
- [static func offset(x: CGFloat, y: CGFloat) -> Self](/documentation/swiftui/transition/offset(x:y:))
- [static var opacity: OpacityTransition](/documentation/swiftui/transition/opacity)
- [static func push(from: Edge) -> Self](/documentation/swiftui/transition/push(from:))
- [static var scale: ScaleTransition](/documentation/swiftui/transition/scale)
- [static func scale(Double, anchor: UnitPoint) -> Self](/documentation/swiftui/transition/scale(_:anchor:))
- [static var slide: SlideTransition](/documentation/swiftui/transition/slide)
- [static var symbolEffect: SymbolEffectTransition](/documentation/swiftui/transition/symboleffect)
- [static func symbolEffect<T>(T, options: SymbolEffectOptions) -> SymbolEffectTransition](/documentation/swiftui/transition/symboleffect(_:options:))

#### Configuring a transition

- [func animation(Animation?) -> some Transition](/documentation/swiftui/transition/animation(_:))
- [static var properties: TransitionProperties](/documentation/swiftui/transition/properties)

#### Using a transition

- [func apply<V>(content: V, phase: TransitionPhase) -> some View](/documentation/swiftui/transition/apply(content:phase:))
- [func combined<T>(with: T) -> some Transition](/documentation/swiftui/transition/combined(with:))

#### Creating a custom transition

- [func body(content: Self.Content, phase: TransitionPhase) -> Self.Body](/documentation/swiftui/transition/body(content:phase:))
- [Body](/documentation/swiftui/transition/body)
- [Transition.Content](/documentation/swiftui/transition/content)

#### Supporting types

- [BlurReplaceTransition](/documentation/swiftui/blurreplacetransition)

##### Creating the transition

- [init(configuration: BlurReplaceTransition.Configuration)](/documentation/swiftui/blurreplacetransition/init(configuration:))
- [var configuration: BlurReplaceTransition.Configuration](/documentation/swiftui/blurreplacetransition/configuration-swift.property)
- [BlurReplaceTransition.Configuration](/documentation/swiftui/blurreplacetransition/configuration-swift.struct)

###### Getting the transition configuration

- [static let downUp: BlurReplaceTransition.Configuration](/documentation/swiftui/blurreplacetransition/configuration-swift.struct/downup)
- [static let upUp: BlurReplaceTransition.Configuration](/documentation/swiftui/blurreplacetransition/configuration-swift.struct/upup)
- [IdentityTransition](/documentation/swiftui/identitytransition)

##### Creating the transition

- [init()](/documentation/swiftui/identitytransition/init())
- [MoveTransition](/documentation/swiftui/movetransition)

##### Creating the transition

- [init(edge: Edge)](/documentation/swiftui/movetransition/init(edge:))
- [var edge: Edge](/documentation/swiftui/movetransition/edge)
- [OffsetTransition](/documentation/swiftui/offsettransition)

##### Creating the transition

- [init(CGSize)](/documentation/swiftui/offsettransition/init(_:))
- [var offset: CGSize](/documentation/swiftui/offsettransition/offset)
- [OpacityTransition](/documentation/swiftui/opacitytransition)

##### Creating the transition

- [init()](/documentation/swiftui/opacitytransition/init())
- [PushTransition](/documentation/swiftui/pushtransition)

##### Creating the transition

- [init(edge: Edge)](/documentation/swiftui/pushtransition/init(edge:))
- [var edge: Edge](/documentation/swiftui/pushtransition/edge)
- [ScaleTransition](/documentation/swiftui/scaletransition)

##### Creating the transition

- [init(Double, anchor: UnitPoint)](/documentation/swiftui/scaletransition/init(_:anchor:))
- [var anchor: UnitPoint](/documentation/swiftui/scaletransition/anchor)
- [var scale: Double](/documentation/swiftui/scaletransition/scale)
- [SlideTransition](/documentation/swiftui/slidetransition)

##### Creating the transition

- [init()](/documentation/swiftui/slidetransition/init())
- [TransitionProperties](/documentation/swiftui/transitionproperties)

#### Creating the transition properties

- [init(hasMotion: Bool)](/documentation/swiftui/transitionproperties/init(hasmotion:))
- [var hasMotion: Bool](/documentation/swiftui/transitionproperties/hasmotion)
- [TransitionPhase](/documentation/swiftui/transitionphase)

#### Getting the phase

- [case identity](/documentation/swiftui/transitionphase/identity)
- [case willAppear](/documentation/swiftui/transitionphase/willappear)
- [case didDisappear](/documentation/swiftui/transitionphase/diddisappear)

#### Getting phase characteristics

- [var isIdentity: Bool](/documentation/swiftui/transitionphase/isidentity)
- [var value: Double](/documentation/swiftui/transitionphase/value)
- [AsymmetricTransition](/documentation/swiftui/asymmetrictransition)

#### Creating the transition

- [init(insertion: Insertion, removal: Removal)](/documentation/swiftui/asymmetrictransition/init(insertion:removal:))

#### Getting transition properties

- [var insertion: Insertion](/documentation/swiftui/asymmetrictransition/insertion)
- [var removal: Removal](/documentation/swiftui/asymmetrictransition/removal)
- [AnyTransition](/documentation/swiftui/anytransition)

#### Getting built-in transitions

- [static var identity: AnyTransition](/documentation/swiftui/anytransition/identity)
- [static func move(edge: Edge) -> AnyTransition](/documentation/swiftui/anytransition/move(edge:))
- [static func offset(CGSize) -> AnyTransition](/documentation/swiftui/anytransition/offset(_:))
- [static func offset(x: CGFloat, y: CGFloat) -> AnyTransition](/documentation/swiftui/anytransition/offset(x:y:))
- [static let opacity: AnyTransition](/documentation/swiftui/anytransition/opacity)
- [static func push(from: Edge) -> AnyTransition](/documentation/swiftui/anytransition/push(from:))
- [static var scale: AnyTransition](/documentation/swiftui/anytransition/scale)
- [static func scale(scale: CGFloat, anchor: UnitPoint) -> AnyTransition](/documentation/swiftui/anytransition/scale(scale:anchor:))
- [static var slide: AnyTransition](/documentation/swiftui/anytransition/slide)

#### Combining and configuring transitions

- [func animation(Animation?) -> AnyTransition](/documentation/swiftui/anytransition/animation(_:))
- [static func asymmetric(insertion: AnyTransition, removal: AnyTransition) -> AnyTransition](/documentation/swiftui/anytransition/asymmetric(insertion:removal:))
- [func combined(with: AnyTransition) -> AnyTransition](/documentation/swiftui/anytransition/combined(with:))

#### Creating a custom transition

- [init<T>(T)](/documentation/swiftui/anytransition/init(_:))
- [static func modifier<E>(active: E, identity: E) -> AnyTransition](/documentation/swiftui/anytransition/modifier(active:identity:))
- [func contentTransition(ContentTransition) -> some View](/documentation/swiftui/view/contenttransition(_:))
- [var contentTransition: ContentTransition](/documentation/swiftui/environmentvalues/contenttransition)
- [var contentTransitionAddsDrawingGroup: Bool](/documentation/swiftui/environmentvalues/contenttransitionaddsdrawinggroup)
- [ContentTransition](/documentation/swiftui/contenttransition)

#### Getting content transitions

- [static let identity: ContentTransition](/documentation/swiftui/contenttransition/identity)
- [static let interpolate: ContentTransition](/documentation/swiftui/contenttransition/interpolate)
- [static func numericText(countsDown: Bool) -> ContentTransition](/documentation/swiftui/contenttransition/numerictext(countsdown:))
- [static func numericText(value: Double) -> ContentTransition](/documentation/swiftui/contenttransition/numerictext(value:))
- [static let opacity: ContentTransition](/documentation/swiftui/contenttransition/opacity)
- [static var symbolEffect: ContentTransition](/documentation/swiftui/contenttransition/symboleffect)
- [static func symbolEffect<T>(T, options: SymbolEffectOptions) -> ContentTransition](/documentation/swiftui/contenttransition/symboleffect(_:options:))
- [PlaceholderContentView](/documentation/swiftui/placeholdercontentview)
- [func navigationTransition(some NavigationTransition) -> some View](/documentation/swiftui/view/navigationtransition(_:))
- [NavigationTransition](/documentation/swiftui/navigationtransition)

#### Getting built-in transitions

- [static var automatic: AutomaticNavigationTransition](/documentation/swiftui/navigationtransition/automatic)
- [static func zoom(sourceID: some Hashable, in: Namespace.ID) -> ZoomNavigationTransition](/documentation/swiftui/navigationtransition/zoom(sourceid:in:))

#### Supporting Types

- [AutomaticNavigationTransition](/documentation/swiftui/automaticnavigationtransition)
- [ZoomNavigationTransition](/documentation/swiftui/zoomnavigationtransition)
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:))
- [func matchedTransitionSource(id: some Hashable, in: Namespace.ID, configuration: (EmptyMatchedTransitionSourceConfiguration) -> some MatchedTransitionSourceConfiguration) -> some View](/documentation/swiftui/view/matchedtransitionsource(id:in:configuration:))
- [MatchedTransitionSourceConfiguration](/documentation/swiftui/matchedtransitionsourceconfiguration)

#### Instance Methods

- [func background(Color) -> some MatchedTransitionSourceConfiguration](/documentation/swiftui/matchedtransitionsourceconfiguration/background(_:))
- [func clipShape(RoundedRectangle) -> some MatchedTransitionSourceConfiguration](/documentation/swiftui/matchedtransitionsourceconfiguration/clipshape(_:))
- [func shadow(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat) -> some MatchedTransitionSourceConfiguration](/documentation/swiftui/matchedtransitionsourceconfiguration/shadow(color:radius:x:y:))
- [EmptyMatchedTransitionSourceConfiguration](/documentation/swiftui/emptymatchedtransitionsourceconfiguration)

### Moving an animation to another view

- [func withTransaction<Result>(Transaction, () throws -> Result) rethrows -> Result](/documentation/swiftui/withtransaction(_:_:))
- [func withTransaction<R, V>(WritableKeyPath<Transaction, V>, V, () throws -> R) rethrows -> R](/documentation/swiftui/withtransaction(_:_:_:))
- [func transaction((inout Transaction) -> Void) -> some View](/documentation/swiftui/view/transaction(_:))
- [func transaction(value: some Equatable, (inout Transaction) -> Void) -> some View](/documentation/swiftui/view/transaction(value:_:))
- [func transaction<V>((inout Transaction) -> Void, body: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/transaction(_:body:))
- [Transaction](/documentation/swiftui/transaction)

#### Creating a transaction

- [init()](/documentation/swiftui/transaction/init())
- [init(animation: Animation?)](/documentation/swiftui/transaction/init(animation:))

#### Managing animations

- [var animation: Animation?](/documentation/swiftui/transaction/animation)
- [var disablesAnimations: Bool](/documentation/swiftui/transaction/disablesanimations)
- [func addAnimationCompletion(criteria: AnimationCompletionCriteria, () -> Void)](/documentation/swiftui/transaction/addanimationcompletion(criteria:_:))

#### Managing window dismissal

- [var dismissBehavior: DismissBehavior](/documentation/swiftui/transaction/dismissbehavior)

#### Getting information about a transaction

- [var isContinuous: Bool](/documentation/swiftui/transaction/iscontinuous)
- [var scrollTargetAnchor: UnitPoint?](/documentation/swiftui/transaction/scrolltargetanchor)
- [var tracksVelocity: Bool](/documentation/swiftui/transaction/tracksvelocity)
- [subscript<K>(K.Type) -> K.Value](/documentation/swiftui/transaction/subscript(_:))

#### Instance Properties

- [var scrollContentOffsetAdjustmentBehavior: ScrollContentOffsetAdjustmentBehavior](/documentation/swiftui/transaction/scrollcontentoffsetadjustmentbehavior)
- [var scrollPositionUpdatePreservesVelocity: Bool](/documentation/swiftui/transaction/scrollpositionupdatepreservesvelocity)
- [macro Entry()](/documentation/swiftui/entry())
- [TransactionKey](/documentation/swiftui/transactionkey)

#### Setting a default value

- [static var defaultValue: Self.Value](/documentation/swiftui/transactionkey/defaultvalue)
- [Value](/documentation/swiftui/transactionkey/value)

### Deprecated types

- [AnimatableModifier](/documentation/swiftui/animatablemodifier)
- [Text input and output](/documentation/swiftui/text-input-and-output)

### Displaying text

- [Text](/documentation/swiftui/text)

#### Creating a text view

- [init(LocalizedStringKey, tableName: String?, bundle: Bundle?, comment: StaticString?)](/documentation/swiftui/text/init(_:tablename:bundle:comment:))
- [init(_:)](/documentation/swiftui/text/init(_:))
- [init(verbatim: String)](/documentation/swiftui/text/init(verbatim:))
- [init(Date, style: Text.DateStyle)](/documentation/swiftui/text/init(_:style:))
- [init(_:format:)](/documentation/swiftui/text/init(_:format:))
- [init(_:formatter:)](/documentation/swiftui/text/init(_:formatter:))
- [init(timerInterval: ClosedRange<Date>, pauseTime: Date?, countsDown: Bool, showsHours: Bool)](/documentation/swiftui/text/init(timerinterval:pausetime:countsdown:showshours:))

#### Choosing a font

- [func font(Font?) -> Text](/documentation/swiftui/text/font(_:))
- [func fontWeight(Font.Weight?) -> Text](/documentation/swiftui/text/fontweight(_:))
- [func fontDesign(Font.Design?) -> Text](/documentation/swiftui/text/fontdesign(_:))
- [func fontWidth(Font.Width?) -> Text](/documentation/swiftui/text/fontwidth(_:))

#### Styling the view’s text

- [func foregroundStyle<S>(S) -> Text](/documentation/swiftui/text/foregroundstyle(_:))
- [func bold() -> Text](/documentation/swiftui/text/bold())
- [func bold(Bool) -> Text](/documentation/swiftui/text/bold(_:))
- [func italic() -> Text](/documentation/swiftui/text/italic())
- [func italic(Bool) -> Text](/documentation/swiftui/text/italic(_:))
- [func strikethrough(Bool, color: Color?) -> Text](/documentation/swiftui/text/strikethrough(_:color:))
- [func strikethrough(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> Text](/documentation/swiftui/text/strikethrough(_:pattern:color:))
- [func underline(Bool, color: Color?) -> Text](/documentation/swiftui/text/underline(_:color:))
- [func underline(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> Text](/documentation/swiftui/text/underline(_:pattern:color:))
- [func monospaced(Bool) -> Text](/documentation/swiftui/text/monospaced(_:))
- [func monospacedDigit() -> Text](/documentation/swiftui/text/monospaceddigit())
- [func kerning(CGFloat) -> Text](/documentation/swiftui/text/kerning(_:))
- [func tracking(CGFloat) -> Text](/documentation/swiftui/text/tracking(_:))
- [func baselineOffset(CGFloat) -> Text](/documentation/swiftui/text/baselineoffset(_:))
- [Text.Case](/documentation/swiftui/text/case)

##### Getting text cases

- [case lowercase](/documentation/swiftui/text/case/lowercase)
- [case uppercase](/documentation/swiftui/text/case/uppercase)
- [Text.DateStyle](/documentation/swiftui/text/datestyle)

##### Getting text date styles

- [static let date: Text.DateStyle](/documentation/swiftui/text/datestyle/date)
- [static let offset: Text.DateStyle](/documentation/swiftui/text/datestyle/offset)
- [static let relative: Text.DateStyle](/documentation/swiftui/text/datestyle/relative)
- [static let time: Text.DateStyle](/documentation/swiftui/text/datestyle/time)
- [static let timer: Text.DateStyle](/documentation/swiftui/text/datestyle/timer)
- [Text.LineStyle](/documentation/swiftui/text/linestyle)

##### Getting text line styles

- [static let single: Text.LineStyle](/documentation/swiftui/text/linestyle/single)

##### Creating a text line style

- [init?(nsUnderlineStyle: NSUnderlineStyle)](/documentation/swiftui/text/linestyle/init(nsunderlinestyle:))
- [init(pattern: Text.LineStyle.Pattern, color: Color?)](/documentation/swiftui/text/linestyle/init(pattern:color:))
- [Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern)

###### Getting line style patterns

- [static let solid: Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern/solid)
- [static let dot: Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern/dot)
- [static let dash: Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern/dash)
- [static let dashDot: Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern/dashdot)
- [static let dashDotDot: Text.LineStyle.Pattern](/documentation/swiftui/text/linestyle/pattern/dashdotdot)

#### Fitting text into available space

- [func textScale(Text.Scale, isEnabled: Bool) -> Text](/documentation/swiftui/text/textscale(_:isenabled:))
- [Text.Scale](/documentation/swiftui/text/scale)

##### Getting built-in text scales

- [static let `default`: Text.Scale](/documentation/swiftui/text/scale/default)
- [static let secondary: Text.Scale](/documentation/swiftui/text/scale/secondary)
- [Text.TruncationMode](/documentation/swiftui/text/truncationmode)

##### Getting text truncation modes

- [case head](/documentation/swiftui/text/truncationmode/head)
- [case middle](/documentation/swiftui/text/truncationmode/middle)
- [case tail](/documentation/swiftui/text/truncationmode/tail)

#### Localizing text

- [func typesettingLanguage(_:isEnabled:)](/documentation/swiftui/text/typesettinglanguage(_:isenabled:))

#### Configuring voiceover

- [func speechAdjustedPitch(Double) -> Text](/documentation/swiftui/text/speechadjustedpitch(_:))
- [func speechAlwaysIncludesPunctuation(Bool) -> Text](/documentation/swiftui/text/speechalwaysincludespunctuation(_:))
- [func speechAnnouncementsQueued(Bool) -> Text](/documentation/swiftui/text/speechannouncementsqueued(_:))
- [func speechSpellsOutCharacters(Bool) -> Text](/documentation/swiftui/text/speechspellsoutcharacters(_:))

#### Providing accessibility information

- [func accessibilityHeading(AccessibilityHeadingLevel) -> Text](/documentation/swiftui/text/accessibilityheading(_:))
- [func accessibilityLabel(_:)](/documentation/swiftui/text/accessibilitylabel(_:))
- [func accessibilityTextContentType(AccessibilityTextContentType) -> Text](/documentation/swiftui/text/accessibilitytextcontenttype(_:))

#### Combining text views

- [static func + (Text, Text) -> Text](/documentation/swiftui/text/+(_:_:))

#### Deprecated symbols

- [func foregroundColor(Color?) -> Text](/documentation/swiftui/text/foregroundcolor(_:))

#### Structures

- [Text.AlignmentStrategy](/documentation/swiftui/text/alignmentstrategy)

##### Type Properties

- [static let `default`: Text.AlignmentStrategy](/documentation/swiftui/text/alignmentstrategy/default)
- [static let layoutBased: Text.AlignmentStrategy](/documentation/swiftui/text/alignmentstrategy/layoutbased)
- [static let writingDirectionBased: Text.AlignmentStrategy](/documentation/swiftui/text/alignmentstrategy/writingdirectionbased)
- [Text.Layout](/documentation/swiftui/text/layout)

##### Structures

- [Text.Layout.CharacterIndex](/documentation/swiftui/text/layout/characterindex)
- [Text.Layout.DrawingOptions](/documentation/swiftui/text/layout/drawingoptions)

###### Type Properties

- [static var disablesSubpixelQuantization: Text.Layout.DrawingOptions](/documentation/swiftui/text/layout/drawingoptions/disablessubpixelquantization)
- [Text.Layout.Line](/documentation/swiftui/text/layout/line)

###### Instance Properties

- [var origin: CGPoint](/documentation/swiftui/text/layout/line/origin)
- [var typographicBounds: Text.Layout.TypographicBounds](/documentation/swiftui/text/layout/line/typographicbounds)
- [Text.Layout.Run](/documentation/swiftui/text/layout/run)

###### Instance Properties

- [var characterIndices: [Text.Layout.CharacterIndex]](/documentation/swiftui/text/layout/run/characterindices)
- [var layoutDirection: LayoutDirection](/documentation/swiftui/text/layout/run/layoutdirection)
- [var typographicBounds: Text.Layout.TypographicBounds](/documentation/swiftui/text/layout/run/typographicbounds)

###### Subscripts

- [subscript<T>(T.Type) -> T?](/documentation/swiftui/text/layout/run/subscript(_:))
- [Text.Layout.RunSlice](/documentation/swiftui/text/layout/runslice)

###### Initializers

- [init(run: Text.Layout.Run, indices: Range<Int>)](/documentation/swiftui/text/layout/runslice/init(run:indices:))

###### Instance Properties

- [var characterIndices: [Text.Layout.CharacterIndex]](/documentation/swiftui/text/layout/runslice/characterindices)
- [var run: Text.Layout.Run](/documentation/swiftui/text/layout/runslice/run)
- [var typographicBounds: Text.Layout.TypographicBounds](/documentation/swiftui/text/layout/runslice/typographicbounds)

###### Subscripts

- [subscript<T>(T.Type) -> T?](/documentation/swiftui/text/layout/runslice/subscript(_:))
- [Text.Layout.TypographicBounds](/documentation/swiftui/text/layout/typographicbounds)

###### Initializers

- [init()](/documentation/swiftui/text/layout/typographicbounds/init())

###### Instance Properties

- [var ascent: CGFloat](/documentation/swiftui/text/layout/typographicbounds/ascent)
- [var descent: CGFloat](/documentation/swiftui/text/layout/typographicbounds/descent)
- [var leading: CGFloat](/documentation/swiftui/text/layout/typographicbounds/leading)
- [var origin: CGPoint](/documentation/swiftui/text/layout/typographicbounds/origin)
- [var rect: CGRect](/documentation/swiftui/text/layout/typographicbounds/rect)
- [var width: CGFloat](/documentation/swiftui/text/layout/typographicbounds/width)

##### Instance Properties

- [var isTruncated: Bool](/documentation/swiftui/text/layout/istruncated)
- [Text.LayoutKey](/documentation/swiftui/text/layoutkey)

##### Structures

- [Text.LayoutKey.AnchoredLayout](/documentation/swiftui/text/layoutkey/anchoredlayout)

###### Instance Properties

- [var layout: Text.Layout](/documentation/swiftui/text/layoutkey/anchoredlayout/layout)
- [var origin: Anchor<CGPoint>](/documentation/swiftui/text/layoutkey/anchoredlayout/origin)
- [Text.WritingDirectionStrategy](/documentation/swiftui/text/writingdirectionstrategy)

##### Type Properties

- [static let contentBased: Text.WritingDirectionStrategy](/documentation/swiftui/text/writingdirectionstrategy/contentbased)
- [static let `default`: Text.WritingDirectionStrategy](/documentation/swiftui/text/writingdirectionstrategy/default)
- [static let layoutBased: Text.WritingDirectionStrategy](/documentation/swiftui/text/writingdirectionstrategy/layoutbased)

#### Instance Methods

- [func customAttribute<T>(T) -> Text](/documentation/swiftui/text/customattribute(_:))
- [func textVariant<V>(V) -> some View](/documentation/swiftui/text/textvariant(_:))
- [Label](/documentation/swiftui/label)

#### Creating a label

- [init(_:image:)](/documentation/swiftui/label/init(_:image:))
- [init(_:systemImage:)](/documentation/swiftui/label/init(_:systemimage:))
- [init(title: () -> Title, icon: () -> Icon)](/documentation/swiftui/label/init(title:icon:))
- [init(_:)](/documentation/swiftui/label/init(_:))
- [init(_:image:)](/documentation/swiftui/label/init(_:image:))
- [func labelStyle<S>(S) -> some View](/documentation/swiftui/view/labelstyle(_:))

### Getting text input

- [Building rich SwiftUI text experiences](/documentation/swiftui/building-rich-swiftui-text-experiences)
- [TextField](/documentation/swiftui/textfield)

#### Creating a text field with a string

- [init(_:text:)](/documentation/swiftui/textfield/init(_:text:))
- [init(_:text:prompt:)](/documentation/swiftui/textfield/init(_:text:prompt:))
- [init(text: Binding<String>, prompt: Text?, label: () -> Label)](/documentation/swiftui/textfield/init(text:prompt:label:))

#### Creating a scrollable text field

- [init(_:text:axis:)](/documentation/swiftui/textfield/init(_:text:axis:))
- [init(_:text:prompt:axis:)](/documentation/swiftui/textfield/init(_:text:prompt:axis:))
- [init(text: Binding<String>, prompt: Text?, axis: Axis, label: () -> Label)](/documentation/swiftui/textfield/init(text:prompt:axis:label:))

#### Creating a text field with a value

- [init(_:value:format:prompt:)](/documentation/swiftui/textfield/init(_:value:format:prompt:))
- [init(value:format:prompt:label:)](/documentation/swiftui/textfield/init(value:format:prompt:label:))
- [init(_:value:formatter:)](/documentation/swiftui/textfield/init(_:value:formatter:))
- [init(_:value:formatter:prompt:)](/documentation/swiftui/textfield/init(_:value:formatter:prompt:))
- [init<V>(value: Binding<V>, formatter: Formatter, prompt: Text?, label: () -> Label)](/documentation/swiftui/textfield/init(value:formatter:prompt:label:))

#### Deprecated initializers

- [Deprecated initializers](/documentation/swiftui/textfield-deprecated)

##### Creating a text field with a string

- [init(_:text:onEditingChanged:onCommit:)](/documentation/swiftui/textfield/init(_:text:oneditingchanged:oncommit:))
- [init(_:text:onCommit:)](/documentation/swiftui/textfield/init(_:text:oncommit:))
- [init(_:text:onEditingChanged:)](/documentation/swiftui/textfield/init(_:text:oneditingchanged:))

##### Creating a text field with a value

- [init(_:value:formatter:onEditingChanged:onCommit:)](/documentation/swiftui/textfield/init(_:value:formatter:oneditingchanged:oncommit:))
- [init(_:value:formatter:onCommit:)](/documentation/swiftui/textfield/init(_:value:formatter:oncommit:))
- [init(_:value:formatter:onEditingChanged:)](/documentation/swiftui/textfield/init(_:value:formatter:oneditingchanged:))

#### Initializers

- [init(_:text:selection:prompt:axis:)](/documentation/swiftui/textfield/init(_:text:selection:prompt:axis:))
- [init(text: Binding<String>, selection: Binding<TextSelection?>, prompt: Text?, axis: Axis?, label: () -> Label)](/documentation/swiftui/textfield/init(text:selection:prompt:axis:label:))
- [func textFieldStyle<S>(S) -> some View](/documentation/swiftui/view/textfieldstyle(_:))
- [SecureField](/documentation/swiftui/securefield)

#### Creating a secure text field

- [init(_:text:)](/documentation/swiftui/securefield/init(_:text:))
- [init(_:text:prompt:)](/documentation/swiftui/securefield/init(_:text:prompt:))
- [init(text: Binding<String>, prompt: Text?, label: () -> Label)](/documentation/swiftui/securefield/init(text:prompt:label:))

#### Deprecated initializers

- [init(_:text:onCommit:)](/documentation/swiftui/securefield/init(_:text:oncommit:))
- [TextEditor](/documentation/swiftui/texteditor)

#### Creating a text editor

- [init(text: Binding<String>)](/documentation/swiftui/texteditor/init(text:))

#### Initializers

- [init(text:selection:)](/documentation/swiftui/texteditor/init(text:selection:))

### Selecting text

- [func textSelection<S>(S) -> some View](/documentation/swiftui/view/textselection(_:))
- [TextSelectability](/documentation/swiftui/textselectability)

#### Getting selectability options

- [static var enabled: EnabledTextSelectability](/documentation/swiftui/textselectability/enabled)
- [static var disabled: DisabledTextSelectability](/documentation/swiftui/textselectability/disabled)

#### Specifying selectability

- [static var allowsSelection: Bool](/documentation/swiftui/textselectability/allowsselection)

#### Supporting types

- [EnabledTextSelectability](/documentation/swiftui/enabledtextselectability)
- [DisabledTextSelectability](/documentation/swiftui/disabledtextselectability)
- [TextSelection](/documentation/swiftui/textselection)

#### Initializers

- [init(insertionPoint: String.Index)](/documentation/swiftui/textselection/init(insertionpoint:))
- [init(range: Range<String.Index>)](/documentation/swiftui/textselection/init(range:))
- [init(ranges: RangeSet<String.Index>)](/documentation/swiftui/textselection/init(ranges:))

#### Instance Properties

- [var affinity: TextSelectionAffinity](/documentation/swiftui/textselection/affinity)
- [var indices: TextSelection.Indices](/documentation/swiftui/textselection/indices-swift.property)
- [var isInsertion: Bool](/documentation/swiftui/textselection/isinsertion)

#### Enumerations

- [TextSelection.Indices](/documentation/swiftui/textselection/indices-swift.enum)

##### Enumeration Cases

- [case multiSelection(RangeSet<String.Index>)](/documentation/swiftui/textselection/indices-swift.enum/multiselection(_:))
- [case selection(Range<String.Index>)](/documentation/swiftui/textselection/indices-swift.enum/selection(_:))
- [func textSelectionAffinity(TextSelectionAffinity) -> some View](/documentation/swiftui/view/textselectionaffinity(_:))
- [var textSelectionAffinity: TextSelectionAffinity](/documentation/swiftui/environmentvalues/textselectionaffinity)
- [TextSelectionAffinity](/documentation/swiftui/textselectionaffinity)

#### Enumeration Cases

- [case automatic](/documentation/swiftui/textselectionaffinity/automatic)
- [case downstream](/documentation/swiftui/textselectionaffinity/downstream)
- [case upstream](/documentation/swiftui/textselectionaffinity/upstream)
- [AttributedTextSelection](/documentation/swiftui/attributedtextselection)

#### Structures

- [AttributedTextSelection.Attributes](/documentation/swiftui/attributedtextselection/attributes)

##### Subscripts

- [subscript(_:)](/documentation/swiftui/attributedtextselection/attributes/subscript(_:))

#### Initializers

- [init()](/documentation/swiftui/attributedtextselection/init())
- [init(insertionPoint: AttributedString.Index, typingAttributes: AttributeContainer?)](/documentation/swiftui/attributedtextselection/init(insertionpoint:typingattributes:))
- [init(range: Range<AttributedString.Index>)](/documentation/swiftui/attributedtextselection/init(range:))
- [init(ranges: RangeSet<AttributedString.Index>)](/documentation/swiftui/attributedtextselection/init(ranges:))

#### Instance Methods

- [func affinity(in: AttributedString) -> TextSelectionAffinity](/documentation/swiftui/attributedtextselection/affinity(in:))
- [func attributes(in: AttributedString) -> AttributedTextSelection.Attributes<AttributedString>](/documentation/swiftui/attributedtextselection/attributes(in:))
- [func indices(in: AttributedString) -> AttributedTextSelection.Indices](/documentation/swiftui/attributedtextselection/indices(in:))
- [func typingAttributes(in: AttributedString) -> AttributeContainer](/documentation/swiftui/attributedtextselection/typingattributes(in:))

#### Enumerations

- [AttributedTextSelection.Indices](/documentation/swiftui/attributedtextselection/indices)

##### Enumeration Cases

- [case insertionPoint(AttributedString.Index)](/documentation/swiftui/attributedtextselection/indices/insertionpoint(_:))
- [case ranges(RangeSet<AttributedString.Index>)](/documentation/swiftui/attributedtextselection/indices/ranges(_:))

### Setting a font

- [Applying custom fonts to text](/documentation/swiftui/applying-custom-fonts-to-text)
- [func font(Font?) -> some View](/documentation/swiftui/view/font(_:))
- [func fontDesign(Font.Design?) -> some View](/documentation/swiftui/view/fontdesign(_:))
- [func fontWeight(Font.Weight?) -> some View](/documentation/swiftui/view/fontweight(_:))
- [func fontWidth(Font.Width?) -> some View](/documentation/swiftui/view/fontwidth(_:))
- [var font: Font?](/documentation/swiftui/environmentvalues/font)
- [Font](/documentation/swiftui/font)

#### Getting standard fonts

- [static let extraLargeTitle2: Font](/documentation/swiftui/font/extralargetitle2)
- [static let extraLargeTitle: Font](/documentation/swiftui/font/extralargetitle)
- [static let largeTitle: Font](/documentation/swiftui/font/largetitle)
- [static let title: Font](/documentation/swiftui/font/title)
- [static let title2: Font](/documentation/swiftui/font/title2)
- [static let title3: Font](/documentation/swiftui/font/title3)
- [static let headline: Font](/documentation/swiftui/font/headline)
- [static let subheadline: Font](/documentation/swiftui/font/subheadline)
- [static let body: Font](/documentation/swiftui/font/body)
- [static let callout: Font](/documentation/swiftui/font/callout)
- [static let caption: Font](/documentation/swiftui/font/caption)
- [static let caption2: Font](/documentation/swiftui/font/caption2)
- [static let footnote: Font](/documentation/swiftui/font/footnote)

#### Getting system fonts

- [static func system(Font.TextStyle, design: Font.Design?, weight: Font.Weight?) -> Font](/documentation/swiftui/font/system(_:design:weight:))
- [static func system(size: CGFloat, weight: Font.Weight?, design: Font.Design?) -> Font](/documentation/swiftui/font/system(size:weight:design:)-697b2)
- [Font.Design](/documentation/swiftui/font/design)

##### Getting font designs

- [case `default`](/documentation/swiftui/font/design/default)
- [case monospaced](/documentation/swiftui/font/design/monospaced)
- [case rounded](/documentation/swiftui/font/design/rounded)
- [case serif](/documentation/swiftui/font/design/serif)
- [Font.TextStyle](/documentation/swiftui/font/textstyle)

##### Getting font text styles

- [case extraLargeTitle2](/documentation/swiftui/font/textstyle/extralargetitle2)
- [case extraLargeTitle](/documentation/swiftui/font/textstyle/extralargetitle)
- [case largeTitle](/documentation/swiftui/font/textstyle/largetitle)
- [case title](/documentation/swiftui/font/textstyle/title)
- [case title2](/documentation/swiftui/font/textstyle/title2)
- [case title3](/documentation/swiftui/font/textstyle/title3)
- [case headline](/documentation/swiftui/font/textstyle/headline)
- [case subheadline](/documentation/swiftui/font/textstyle/subheadline)
- [case body](/documentation/swiftui/font/textstyle/body)
- [case callout](/documentation/swiftui/font/textstyle/callout)
- [case caption](/documentation/swiftui/font/textstyle/caption)
- [case caption2](/documentation/swiftui/font/textstyle/caption2)
- [case footnote](/documentation/swiftui/font/textstyle/footnote)
- [Font.Weight](/documentation/swiftui/font/weight)

##### Getting font weights

- [static let black: Font.Weight](/documentation/swiftui/font/weight/black)
- [static let bold: Font.Weight](/documentation/swiftui/font/weight/bold)
- [static let heavy: Font.Weight](/documentation/swiftui/font/weight/heavy)
- [static let light: Font.Weight](/documentation/swiftui/font/weight/light)
- [static let medium: Font.Weight](/documentation/swiftui/font/weight/medium)
- [static let regular: Font.Weight](/documentation/swiftui/font/weight/regular)
- [static let semibold: Font.Weight](/documentation/swiftui/font/weight/semibold)
- [static let thin: Font.Weight](/documentation/swiftui/font/weight/thin)
- [static let ultraLight: Font.Weight](/documentation/swiftui/font/weight/ultralight)

#### Creating custom fonts

- [static func custom(String, fixedSize: CGFloat) -> Font](/documentation/swiftui/font/custom(_:fixedsize:))
- [static func custom(String, size: CGFloat, relativeTo: Font.TextStyle) -> Font](/documentation/swiftui/font/custom(_:size:relativeto:))
- [static func custom(String, size: CGFloat) -> Font](/documentation/swiftui/font/custom(_:size:))

#### Getting a font from another font

- [init(CTFont)](/documentation/swiftui/font/init(_:))

#### Styling a font

- [func bold() -> Font](/documentation/swiftui/font/bold())
- [func italic() -> Font](/documentation/swiftui/font/italic())
- [func monospaced() -> Font](/documentation/swiftui/font/monospaced())
- [func monospacedDigit() -> Font](/documentation/swiftui/font/monospaceddigit())
- [func smallCaps() -> Font](/documentation/swiftui/font/smallcaps())
- [func lowercaseSmallCaps() -> Font](/documentation/swiftui/font/lowercasesmallcaps())
- [func uppercaseSmallCaps() -> Font](/documentation/swiftui/font/uppercasesmallcaps())
- [func weight(Font.Weight) -> Font](/documentation/swiftui/font/weight(_:))
- [func width(Font.Width) -> Font](/documentation/swiftui/font/width(_:))
- [Font.Width](/documentation/swiftui/font/width)

##### Getting standard font widths

- [static let compressed: Font.Width](/documentation/swiftui/font/width/compressed)
- [static let condensed: Font.Width](/documentation/swiftui/font/width/condensed)
- [static let expanded: Font.Width](/documentation/swiftui/font/width/expanded)
- [static let standard: Font.Width](/documentation/swiftui/font/width/standard)

##### Creating an explicit font width

- [init(CGFloat)](/documentation/swiftui/font/width/init(_:))

##### Accessing the width’s value

- [var value: CGFloat](/documentation/swiftui/font/width/value)
- [func leading(Font.Leading) -> Font](/documentation/swiftui/font/leading(_:))
- [Font.Leading](/documentation/swiftui/font/leading)

##### Getting leading line spacing options

- [case standard](/documentation/swiftui/font/leading/standard)
- [case loose](/documentation/swiftui/font/leading/loose)
- [case tight](/documentation/swiftui/font/leading/tight)

#### Deprecated symbols

- [static func system(Font.TextStyle, design: Font.Design) -> Font](/documentation/swiftui/font/system(_:design:))
- [static func system(size: CGFloat, weight: Font.Weight, design: Font.Design) -> Font](/documentation/swiftui/font/system(size:weight:design:)-73a88)

#### Structures

- [Font.Context](/documentation/swiftui/font/context)
- [Font.Resolved](/documentation/swiftui/font/resolved)

##### Instance Properties

- [var ctFont: CTFont](/documentation/swiftui/font/resolved/ctfont)
- [var isBold: Bool](/documentation/swiftui/font/resolved/isbold)
- [var isItalic: Bool](/documentation/swiftui/font/resolved/isitalic)
- [var isLowercaseSmallCaps: Bool](/documentation/swiftui/font/resolved/islowercasesmallcaps)
- [var isMonospaced: Bool](/documentation/swiftui/font/resolved/ismonospaced)
- [var isSmallCaps: Bool](/documentation/swiftui/font/resolved/issmallcaps)
- [var isUppercaseSmallCaps: Bool](/documentation/swiftui/font/resolved/isuppercasesmallcaps)
- [var leading: Font.Leading](/documentation/swiftui/font/resolved/leading)
- [var pointSize: CGFloat](/documentation/swiftui/font/resolved/pointsize)
- [var weight: Font.Weight](/documentation/swiftui/font/resolved/weight)
- [var width: Font.Width](/documentation/swiftui/font/resolved/width)

#### Instance Methods

- [func bold(Bool) -> Font](/documentation/swiftui/font/bold(_:))
- [func italic(Bool) -> Font](/documentation/swiftui/font/italic(_:))
- [func lowercaseSmallCaps(Bool) -> Font](/documentation/swiftui/font/lowercasesmallcaps(_:))
- [func monospaced(Bool) -> Font](/documentation/swiftui/font/monospaced(_:))
- [func pointSize(CGFloat) -> Font](/documentation/swiftui/font/pointsize(_:))
- [func resolve(in: Font.Context) -> Font.Resolved](/documentation/swiftui/font/resolve(in:))
- [func scaled(by: CGFloat) -> Font](/documentation/swiftui/font/scaled(by:))
- [func smallCaps(Bool) -> Font](/documentation/swiftui/font/smallcaps(_:))
- [func uppercaseSmallCaps(Bool) -> Font](/documentation/swiftui/font/uppercasesmallcaps(_:))

#### Type Properties

- [static var `default`: Font](/documentation/swiftui/font/default)

#### Type Methods

- [static system(size:weight:design:)](/documentation/swiftui/font/system(size:weight:design:))

### Adjusting text size

- [func textScale(Text.Scale, isEnabled: Bool) -> some View](/documentation/swiftui/view/textscale(_:isenabled:))
- [func dynamicTypeSize(_:)](/documentation/swiftui/view/dynamictypesize(_:))
- [var dynamicTypeSize: DynamicTypeSize](/documentation/swiftui/environmentvalues/dynamictypesize)
- [DynamicTypeSize](/documentation/swiftui/dynamictypesize)

#### Getting type sizes
