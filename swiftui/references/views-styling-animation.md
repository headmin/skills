# Views: Styling and Animation — SwiftUI Reference

## Contents
- [Views](#views)
  - [Creating a view](#creating-a-view)

---
## Views

- [View fundamentals](/documentation/swiftui/view-fundamentals)

### Creating a view

- [Declaring a custom view](/documentation/swiftui/declaring-a-custom-view)
- [View](/documentation/swiftui/view)

#### Implementing a custom view

- [var body: Self.Body](/documentation/swiftui/view/body-8kl5o)
- [Body](/documentation/swiftui/view/body-swift.associatedtype)
- [func modifier<T>(T) -> ModifiedContent<Self, T>](/documentation/swiftui/view/modifier(_:))
- [Previews in Xcode](/documentation/swiftui/previews-in-xcode)

##### Essentials

- [Previewing your app’s interface in Xcode](/documentation/xcode/previewing-your-apps-interface-in-xcode)

##### Creating a preview

- [macro Preview(String?, body: () -> any View)](/documentation/swiftui/preview(_:body:))
- [macro Preview(String?, traits: PreviewTrait<Preview.ViewTraits>, PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:traits:_:body:))
- [macro Preview(String?, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:traits:body:cameras:))

##### Creating a preview in the context of a scene

- [macro Preview<Style>(String?, immersionStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:immersionstyle:traits:body:))
- [macro Preview<Style>(String?, immersionStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:immersionstyle:traits:body:cameras:))
- [macro Preview<Style>(String?, windowStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View)](/documentation/swiftui/preview(_:windowstyle:traits:body:))
- [macro Preview<Style>(String?, windowStyle: Style, traits: PreviewTrait<Preview.ViewTraits>..., body: () -> any View, cameras: () -> [PreviewCamera])](/documentation/swiftui/preview(_:windowstyle:traits:body:cameras:))

##### Defining a preview

- [macro Previewable()](/documentation/swiftui/previewable())
- [PreviewProvider](/documentation/swiftui/previewprovider)

###### Creating a preview

- [static var previews: Self.Previews](/documentation/swiftui/previewprovider/previews-swift.type.property)
- [Previews](/documentation/swiftui/previewprovider/previews-swift.associatedtype)

###### Specifying the platform

- [static var platform: PreviewPlatform?](/documentation/swiftui/previewprovider/platform)
- [PreviewPlatform](/documentation/swiftui/previewplatform)

###### Getting an operating system

- [case iOS](/documentation/swiftui/previewplatform/ios)
- [case macOS](/documentation/swiftui/previewplatform/macos)
- [case tvOS](/documentation/swiftui/previewplatform/tvos)
- [case watchOS](/documentation/swiftui/previewplatform/watchos)
- [func previewDisplayName(String?) -> some View](/documentation/swiftui/view/previewdisplayname(_:))
- [PreviewModifier](/documentation/swiftui/previewmodifier)

###### Associated Types

- [Body](/documentation/swiftui/previewmodifier/body)
- [Context](/documentation/swiftui/previewmodifier/context)

###### Instance Methods

- [func body(content: Self.Content, context: Self.Context) -> Self.Body](/documentation/swiftui/previewmodifier/body(content:context:))

###### Type Aliases

- [PreviewModifier.Content](/documentation/swiftui/previewmodifier/content)

###### Type Methods

- [static func makeSharedContext() async throws -> Self.Context](/documentation/swiftui/previewmodifier/makesharedcontext())
- [PreviewModifierContent](/documentation/swiftui/previewmodifiercontent)

##### Customizing a preview

- [func previewDevice(PreviewDevice?) -> some View](/documentation/swiftui/view/previewdevice(_:))
- [PreviewDevice](/documentation/swiftui/previewdevice)
- [func previewLayout(PreviewLayout) -> some View](/documentation/swiftui/view/previewlayout(_:))
- [func previewInterfaceOrientation(InterfaceOrientation) -> some View](/documentation/swiftui/view/previewinterfaceorientation(_:))
- [InterfaceOrientation](/documentation/swiftui/interfaceorientation)

###### Getting an orientation

- [static let portrait: InterfaceOrientation](/documentation/swiftui/interfaceorientation/portrait)
- [static let portraitUpsideDown: InterfaceOrientation](/documentation/swiftui/interfaceorientation/portraitupsidedown)
- [static let landscapeLeft: InterfaceOrientation](/documentation/swiftui/interfaceorientation/landscapeleft)
- [static let landscapeRight: InterfaceOrientation](/documentation/swiftui/interfaceorientation/landscaperight)

##### Setting a context

- [func previewContext<C>(C) -> some View](/documentation/swiftui/view/previewcontext(_:))
- [PreviewContext](/documentation/swiftui/previewcontext)

###### Accessing a preview context

- [subscript<Key>(Key.Type) -> Key.Value](/documentation/swiftui/previewcontext/subscript(_:))
- [PreviewContextKey](/documentation/swiftui/previewcontextkey)

###### Setting a default

- [static var defaultValue: Self.Value](/documentation/swiftui/previewcontextkey/defaultvalue)
- [Value](/documentation/swiftui/previewcontextkey/value)

##### Building in debug mode

- [DebugReplaceableView](/documentation/swiftui/debugreplaceableview)

#### Configuring view elements

- [Accessibility modifiers](/documentation/swiftui/view-accessibility)

##### Labels

- [func accessibilityLabel(_:)](/documentation/swiftui/view/accessibilitylabel(_:))
- [func accessibilityLabel(_:isEnabled:)](/documentation/swiftui/view/accessibilitylabel(_:isenabled:))
- [func accessibilityLabel<V>(content: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/accessibilitylabel(content:))
- [func accessibilityInputLabels(_:)](/documentation/swiftui/view/accessibilityinputlabels(_:))
- [func accessibilityInputLabels(_:isEnabled:)](/documentation/swiftui/view/accessibilityinputlabels(_:isenabled:))
- [func accessibilityLabeledPair<ID>(role: AccessibilityLabeledPairRole, id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilitylabeledpair(role:id:in:))

##### Values

- [func accessibilityValue(_:)](/documentation/swiftui/view/accessibilityvalue(_:))
- [func accessibilityValue(_:isEnabled:)](/documentation/swiftui/view/accessibilityvalue(_:isenabled:))

##### Hints

- [func accessibilityHint(_:)](/documentation/swiftui/view/accessibilityhint(_:))
- [func accessibilityHint(_:isEnabled:)](/documentation/swiftui/view/accessibilityhint(_:isenabled:))

##### Actions

- [func accessibilityAction(AccessibilityActionKind, () -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaction(_:_:))
- [func accessibilityActions<Content>(() -> Content) -> some View](/documentation/swiftui/view/accessibilityactions(_:))
- [func accessibilityAction(named:_:)](/documentation/swiftui/view/accessibilityaction(named:_:))
- [func accessibilityAction<Label>(action: () -> Void, label: () -> Label) -> some View](/documentation/swiftui/view/accessibilityaction(action:label:))
- [func accessibilityAction<I, Label>(intent: I, label: () -> Label) -> some View](/documentation/swiftui/view/accessibilityaction(intent:label:))
- [func accessibilityAction<I>(AccessibilityActionKind, intent: I) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaction(_:intent:))
- [func accessibilityAction(named:intent:)](/documentation/swiftui/view/accessibilityaction(named:intent:))
- [func accessibilityAdjustableAction((AccessibilityAdjustmentDirection) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityadjustableaction(_:))
- [func accessibilityScrollAction((Edge) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityscrollaction(_:))

##### Gestures

- [func accessibilityActivationPoint(_:)](/documentation/swiftui/view/accessibilityactivationpoint(_:))
- [func accessibilityActivationPoint(_:isEnabled:)](/documentation/swiftui/view/accessibilityactivationpoint(_:isenabled:))
- [func accessibilityDragPoint(_:description:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:))
- [func accessibilityDragPoint(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:isenabled:))
- [func accessibilityDropPoint(_:description:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:))
- [func accessibilityDropPoint(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:isenabled:))
- [func accessibilityDirectTouch(Bool, options: AccessibilityDirectTouchOptions) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitydirecttouch(_:options:))
- [func accessibilityZoomAction((AccessibilityZoomGestureAction) -> Void) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityzoomaction(_:))

##### Elements

- [func accessibilityElement(children: AccessibilityChildBehavior) -> some View](/documentation/swiftui/view/accessibilityelement(children:))
- [func accessibilityChildren<V>(children: () -> V) -> some View](/documentation/swiftui/view/accessibilitychildren(children:))
- [func accessibilityHidden(Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityhidden(_:))
- [func accessibilityHidden(Bool, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityhidden(_:isenabled:))

##### Custom controls

- [func accessibilityRepresentation<V>(representation: () -> V) -> some View](/documentation/swiftui/view/accessibilityrepresentation(representation:))
- [func accessibilityRespondsToUserInteraction(Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:))
- [func accessibilityRespondsToUserInteraction(Bool, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:isenabled:))

##### Custom content

- [func accessibilityCustomContent(_:_:importance:)](/documentation/swiftui/view/accessibilitycustomcontent(_:_:importance:))

##### Working with rotors

- [func accessibilityRotor(_:entries:)](/documentation/swiftui/view/accessibilityrotor(_:entries:))
- [func accessibilityRotor(_:entries:entryID:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entryid:entrylabel:))
- [func accessibilityRotor(_:entries:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entrylabel:))
- [func accessibilityRotor(_:textRanges:)](/documentation/swiftui/view/accessibilityrotor(_:textranges:))

##### Configuring rotors

- [func accessibilityRotorEntry<ID>(id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilityrotorentry(id:in:))
- [func accessibilityLinkedGroup<ID>(id: ID, in: Namespace.ID) -> some View](/documentation/swiftui/view/accessibilitylinkedgroup(id:in:))
- [func accessibilitySortPriority(Double) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitysortpriority(_:))

##### Focus

- [func accessibilityFocused(AccessibilityFocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/accessibilityfocused(_:))
- [func accessibilityFocused<Value>(AccessibilityFocusState<Value>.Binding, equals: Value) -> some View](/documentation/swiftui/view/accessibilityfocused(_:equals:))

##### Traits

- [func accessibilityAddTraits(AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityaddtraits(_:))
- [func accessibilityRemoveTraits(AccessibilityTraits) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityremovetraits(_:))

##### Identity

- [func accessibilityIdentifier(String) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityidentifier(_:))
- [func accessibilityIdentifier(String, isEnabled: Bool) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityidentifier(_:isenabled:))

##### Color inversion

- [func accessibilityIgnoresInvertColors(Bool) -> some View](/documentation/swiftui/view/accessibilityignoresinvertcolors(_:))

##### Content descriptions

- [func accessibilityTextContentType(AccessibilityTextContentType) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilitytextcontenttype(_:))
- [func accessibilityHeading(AccessibilityHeadingLevel) -> ModifiedContent<Self, AccessibilityAttachmentModifier>](/documentation/swiftui/view/accessibilityheading(_:))

##### VoiceOver

- [func speechAdjustedPitch(Double) -> some View](/documentation/swiftui/view/speechadjustedpitch(_:))
- [func speechAlwaysIncludesPunctuation(Bool) -> some View](/documentation/swiftui/view/speechalwaysincludespunctuation(_:))
- [func speechAnnouncementsQueued(Bool) -> some View](/documentation/swiftui/view/speechannouncementsqueued(_:))
- [func speechSpellsOutCharacters(Bool) -> some View](/documentation/swiftui/view/speechspellsoutcharacters(_:))

##### Charts

- [func accessibilityChartDescriptor<R>(R) -> some View](/documentation/swiftui/view/accessibilitychartdescriptor(_:))

##### Large content

- [func accessibilityShowsLargeContentViewer() -> some View](/documentation/swiftui/view/accessibilityshowslargecontentviewer())
- [func accessibilityShowsLargeContentViewer<V>(() -> V) -> some View](/documentation/swiftui/view/accessibilityshowslargecontentviewer(_:))

##### Quick actions

- [func accessibilityQuickAction<Style, Content>(style: Style, content: () -> Content) -> some View](/documentation/swiftui/view/accessibilityquickaction(style:content:))
- [func accessibilityQuickAction<Style, Content>(style: Style, isActive: Binding<Bool>, content: () -> Content) -> some View](/documentation/swiftui/view/accessibilityquickaction(style:isactive:content:))
- [Appearance modifiers](/documentation/swiftui/view-appearance)

##### Colors and patterns

- [func backgroundStyle<S>(S) -> some View](/documentation/swiftui/view/backgroundstyle(_:))
- [func foregroundStyle<S>(S) -> some View](/documentation/swiftui/view/foregroundstyle(_:))
- [func foregroundStyle<S1, S2>(S1, S2) -> some View](/documentation/swiftui/view/foregroundstyle(_:_:))
- [func foregroundStyle<S1, S2, S3>(S1, S2, S3) -> some View](/documentation/swiftui/view/foregroundstyle(_:_:_:))
- [func allowedDynamicRange(Image.DynamicRange?) -> some View](/documentation/swiftui/view/alloweddynamicrange(_:))

##### Tint

- [func tint(_:)](/documentation/swiftui/view/tint(_:))
- [func listRowSeparatorTint(Color?, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listrowseparatortint(_:edges:))
- [func listSectionSeparatorTint(Color?, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listsectionseparatortint(_:edges:))
- [func listItemTint(_:)](/documentation/swiftui/view/listitemtint(_:))

##### Light and dark appearance

- [func preferredColorScheme(ColorScheme?) -> some View](/documentation/swiftui/view/preferredcolorscheme(_:))
- [func preferredSurroundingsEffect(SurroundingsEffect?) -> some View](/documentation/swiftui/view/preferredsurroundingseffect(_:))

##### Foreground elements

- [func border<S>(S, width: CGFloat) -> some View](/documentation/swiftui/view/border(_:width:))
- [func overlay<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/overlay(alignment:content:))
- [func overlay<S>(S, ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/overlay(_:ignoressafeareaedges:))
- [func overlay<S, T>(S, in: T, fillStyle: FillStyle) -> some View](/documentation/swiftui/view/overlay(_:in:fillstyle:))

##### Background elements

- [func background<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/background(alignment:content:))
- [func background<S>(S, ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/background(_:ignoressafeareaedges:))
- [func background(ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/background(ignoressafeareaedges:))
- [func background(_:in:fillStyle:)](/documentation/swiftui/view/background(_:in:fillstyle:))
- [func background(in:fillStyle:)](/documentation/swiftui/view/background(in:fillstyle:))
- [func alternatingRowBackgrounds(AlternatingRowBackgroundBehavior) -> some View](/documentation/swiftui/view/alternatingrowbackgrounds(_:))
- [func listRowBackground<V>(V?) -> some View](/documentation/swiftui/view/listrowbackground(_:))
- [func scrollContentBackground(Visibility) -> some View](/documentation/swiftui/view/scrollcontentbackground(_:))
- [func containerBackground<S>(S, for: ContainerBackgroundPlacement) -> some View](/documentation/swiftui/view/containerbackground(_:for:))
- [func containerBackground<V>(for: ContainerBackgroundPlacement, alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/containerbackground(for:alignment:content:))
- [func glassBackgroundEffect(displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(displaymode:))
- [func glassBackgroundEffect<S>(in: S, displayMode: GlassBackgroundDisplayMode) -> some View](/documentation/swiftui/view/glassbackgroundeffect(in:displaymode:))

##### Control configuration

- [func defaultWheelPickerItemHeight(CGFloat) -> some View](/documentation/swiftui/view/defaultwheelpickeritemheight(_:))
- [func horizontalRadioGroupLayout() -> some View](/documentation/swiftui/view/horizontalradiogrouplayout())
- [func controlSize(_:)](/documentation/swiftui/view/controlsize(_:))
- [func buttonBorderShape(ButtonBorderShape) -> some View](/documentation/swiftui/view/buttonbordershape(_:))
- [func buttonRepeatBehavior(ButtonRepeatBehavior) -> some View](/documentation/swiftui/view/buttonrepeatbehavior(_:))
- [func headerProminence(Prominence) -> some View](/documentation/swiftui/view/headerprominence(_:))
- [func scrollDisabled(Bool) -> some View](/documentation/swiftui/view/scrolldisabled(_:))
- [func scrollBounceBehavior(ScrollBounceBehavior, axes: Axis.Set) -> some View](/documentation/swiftui/view/scrollbouncebehavior(_:axes:))
- [func scrollIndicatorsFlash(onAppear: Bool) -> some View](/documentation/swiftui/view/scrollindicatorsflash(onappear:))
- [func scrollIndicatorsFlash(trigger: some Equatable) -> some View](/documentation/swiftui/view/scrollindicatorsflash(trigger:))
- [func menuOrder(MenuOrder) -> some View](/documentation/swiftui/view/menuorder(_:))
- [func menuActionDismissBehavior(MenuActionDismissBehavior) -> some View](/documentation/swiftui/view/menuactiondismissbehavior(_:))
- [func paletteSelectionEffect(PaletteSelectionEffect) -> some View](/documentation/swiftui/view/paletteselectioneffect(_:))
- [func typeSelectEquivalent(_:)](/documentation/swiftui/view/typeselectequivalent(_:))

##### Symbol effects

- [func symbolEffect<T>(T, options: SymbolEffectOptions, isActive: Bool) -> some View](/documentation/swiftui/view/symboleffect(_:options:isactive:))
- [func symbolEffect<T, U>(T, options: SymbolEffectOptions, value: U) -> some View](/documentation/swiftui/view/symboleffect(_:options:value:))
- [func symbolEffectsRemoved(Bool) -> some View](/documentation/swiftui/view/symboleffectsremoved(_:))

##### Privacy and redaction

- [func privacySensitive(Bool) -> some View](/documentation/swiftui/view/privacysensitive(_:))
- [func redacted(reason: RedactionReasons) -> some View](/documentation/swiftui/view/redacted(reason:))
- [func unredacted() -> some View](/documentation/swiftui/view/unredacted())
- [func invalidatableContent(Bool) -> some View](/documentation/swiftui/view/invalidatablecontent(_:))

##### Visibility

- [func hidden() -> some View](/documentation/swiftui/view/hidden())
- [func labelsHidden() -> some View](/documentation/swiftui/view/labelshidden())
- [func menuIndicator(Visibility) -> some View](/documentation/swiftui/view/menuindicator(_:))
- [func listRowSeparator(Visibility, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listrowseparator(_:edges:))
- [func listSectionSeparator(Visibility, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listsectionseparator(_:edges:))
- [func persistentSystemOverlays(Visibility) -> some View](/documentation/swiftui/view/persistentsystemoverlays(_:))
- [func scrollIndicators(ScrollIndicatorVisibility, axes: Axis.Set) -> some View](/documentation/swiftui/view/scrollindicators(_:axes:))
- [func scrollClipDisabled(Bool) -> some View](/documentation/swiftui/view/scrollclipdisabled(_:))
- [func tableColumnHeaders(Visibility) -> some View](/documentation/swiftui/view/tablecolumnheaders(_:))
- [func upperLimbVisibility(Visibility) -> some View](/documentation/swiftui/view/upperlimbvisibility(_:))
- [func volumeBaseplateVisibility(Visibility) -> some View](/documentation/swiftui/view/volumebaseplatevisibility(_:))

##### Sensory feedback

- [func sensoryFeedback<T>(SensoryFeedback, trigger: T) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:))
- [func sensoryFeedback(trigger:_:)](/documentation/swiftui/view/sensoryfeedback(trigger:_:))
- [func sensoryFeedback<T>(SensoryFeedback, trigger: T, condition: (T, T) -> Bool) -> some View](/documentation/swiftui/view/sensoryfeedback(_:trigger:condition:))

##### Widget configuration

- [func widgetAccentable(Bool) -> some View](/documentation/swiftui/view/widgetaccentable(_:))
- [func widgetCurvesContent(Bool) -> some View](/documentation/swiftui/view/widgetcurvescontent(_:))
- [func widgetLabel(_:)](/documentation/swiftui/view/widgetlabel(_:))
- [func widgetLabel<Label>(label: () -> Label) -> some View](/documentation/swiftui/view/widgetlabel(label:))
- [func dynamicIsland(verticalPlacement: DynamicIslandExpandedRegionVerticalPlacement) -> some View](/documentation/swiftui/view/dynamicisland(verticalplacement:))
- [func accessoryWidgetGroupStyle(AccessoryWidgetGroupStyle) -> some View](/documentation/swiftui/view/accessorywidgetgroupstyle(_:))

##### Window behaviors

- [func windowDismissBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowdismissbehavior(_:))
- [func windowFullScreenBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowfullscreenbehavior(_:))
- [func windowMinimizeBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowminimizebehavior(_:))
- [func windowResizeBehavior(WindowInteractionBehavior) -> some View](/documentation/swiftui/view/windowresizebehavior(_:))
- [Text and symbol modifiers](/documentation/swiftui/view-text-and-symbols)

##### Fonts

- [func font(Font?) -> some View](/documentation/swiftui/view/font(_:))

##### Dynamic type

- [func dynamicTypeSize(_:)](/documentation/swiftui/view/dynamictypesize(_:))

##### Text style

- [func bold(Bool) -> some View](/documentation/swiftui/view/bold(_:))
- [func fontDesign(Font.Design?) -> some View](/documentation/swiftui/view/fontdesign(_:))
- [func fontWeight(Font.Weight?) -> some View](/documentation/swiftui/view/fontweight(_:))
- [func fontWidth(Font.Width?) -> some View](/documentation/swiftui/view/fontwidth(_:))
- [func italic(Bool) -> some View](/documentation/swiftui/view/italic(_:))
- [func monospaced(Bool) -> some View](/documentation/swiftui/view/monospaced(_:))
- [func monospacedDigit() -> some View](/documentation/swiftui/view/monospaceddigit())
- [func strikethrough(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> some View](/documentation/swiftui/view/strikethrough(_:pattern:color:))
- [func textCase(Text.Case?) -> some View](/documentation/swiftui/view/textcase(_:))
- [func textScale(Text.Scale, isEnabled: Bool) -> some View](/documentation/swiftui/view/textscale(_:isenabled:))
- [func underline(Bool, pattern: Text.LineStyle.Pattern, color: Color?) -> some View](/documentation/swiftui/view/underline(_:pattern:color:))

##### Text layout

- [func allowsTightening(Bool) -> some View](/documentation/swiftui/view/allowstightening(_:))
- [func baselineOffset(CGFloat) -> some View](/documentation/swiftui/view/baselineoffset(_:))
- [func flipsForRightToLeftLayoutDirection(Bool) -> some View](/documentation/swiftui/view/flipsforrighttoleftlayoutdirection(_:))
- [func kerning(CGFloat) -> some View](/documentation/swiftui/view/kerning(_:))
- [func minimumScaleFactor(CGFloat) -> some View](/documentation/swiftui/view/minimumscalefactor(_:))
- [func tracking(CGFloat) -> some View](/documentation/swiftui/view/tracking(_:))
- [func truncationMode(Text.TruncationMode) -> some View](/documentation/swiftui/view/truncationmode(_:))
- [func typesettingLanguage(_:isEnabled:)](/documentation/swiftui/view/typesettinglanguage(_:isenabled:))

##### Multiline text

- [func lineLimit(_:)](/documentation/swiftui/view/linelimit(_:))
- [func lineLimit(Int, reservesSpace: Bool) -> some View](/documentation/swiftui/view/linelimit(_:reservesspace:))
- [func lineSpacing(CGFloat) -> some View](/documentation/swiftui/view/linespacing(_:))
- [func multilineTextAlignment(TextAlignment) -> some View](/documentation/swiftui/view/multilinetextalignment(_:))
- [func multilineTextAlignment(strategy: Text.AlignmentStrategy) -> some View](/documentation/swiftui/view/multilinetextalignment(strategy:))

##### Text selection

- [func textSelection<S>(S) -> some View](/documentation/swiftui/view/textselection(_:))

##### Text entry

- [func autocorrectionDisabled(Bool) -> some View](/documentation/swiftui/view/autocorrectiondisabled(_:))
- [func keyboardType(UIKeyboardType) -> some View](/documentation/swiftui/view/keyboardtype(_:))
- [func scrollDismissesKeyboard(ScrollDismissesKeyboardMode) -> some View](/documentation/swiftui/view/scrolldismisseskeyboard(_:))
- [func textInputAutocapitalization(TextInputAutocapitalization?) -> some View](/documentation/swiftui/view/textinputautocapitalization(_:))
- [func textInputCompletion(String) -> some View](/documentation/swiftui/view/textinputcompletion(_:))
- [func textInputSuggestions<S>(() -> S) -> some View](/documentation/swiftui/view/textinputsuggestions(_:))
- [func textInputSuggestions<Data, Content>(Data, content: (Data.Element) -> Content) -> some View](/documentation/swiftui/view/textinputsuggestions(_:content:))
- [func textInputSuggestions<Data, ID, Content>(Data, id: KeyPath<Data.Element, ID>, content: (Data.Element) -> Content) -> some View](/documentation/swiftui/view/textinputsuggestions(_:id:content:))
- [func textContentType(WKTextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-4dqqb)
- [func textContentType(NSTextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-6fic1)
- [func textContentType(UITextContentType?) -> some View](/documentation/swiftui/view/textcontenttype(_:)-ufdv)

##### Find and replace

- [func findNavigator(isPresented: Binding<Bool>) -> some View](/documentation/swiftui/view/findnavigator(ispresented:))
- [func findDisabled(Bool) -> some View](/documentation/swiftui/view/finddisabled(_:))
- [func replaceDisabled(Bool) -> some View](/documentation/swiftui/view/replacedisabled(_:))

##### Symbol appearance

- [func symbolRenderingMode(SymbolRenderingMode?) -> some View](/documentation/swiftui/view/symbolrenderingmode(_:))
- [func symbolVariant(SymbolVariants) -> some View](/documentation/swiftui/view/symbolvariant(_:))
- [Auxiliary view modifiers](/documentation/swiftui/view-auxiliary-views)

##### Navigation titles

- [Configure your apps navigation titles](/documentation/swiftui/configure-your-apps-navigation-titles)
- [func navigationTitle(_:)](/documentation/swiftui/view/navigationtitle(_:))
- [func navigationSubtitle(_:)](/documentation/swiftui/view/navigationsubtitle(_:))

##### Navigation title configuration

- [func navigationDocument(_:)](/documentation/swiftui/view/navigationdocument(_:))
- [func navigationDocument(_:preview:)](/documentation/swiftui/view/navigationdocument(_:preview:))

##### Navigation bars

- [func navigationBarBackButtonHidden(Bool) -> some View](/documentation/swiftui/view/navigationbarbackbuttonhidden(_:))
- [func navigationBarTitleDisplayMode(NavigationBarItem.TitleDisplayMode) -> some View](/documentation/swiftui/view/navigationbartitledisplaymode(_:))

##### Navigation stacks and columns

- [func navigationDestination<D, C>(for: D.Type, destination: (D) -> C) -> some View](/documentation/swiftui/view/navigationdestination(for:destination:))
- [func navigationDestination<V>(isPresented: Binding<Bool>, destination: () -> V) -> some View](/documentation/swiftui/view/navigationdestination(ispresented:destination:))
- [func navigationDestination<D, C>(item: Binding<Optional<D>>, destination: (D) -> C) -> some View](/documentation/swiftui/view/navigationdestination(item:destination:))
- [func navigationSplitViewColumnWidth(CGFloat) -> some View](/documentation/swiftui/view/navigationsplitviewcolumnwidth(_:))
- [func navigationSplitViewColumnWidth(min: CGFloat?, ideal: CGFloat, max: CGFloat?) -> some View](/documentation/swiftui/view/navigationsplitviewcolumnwidth(min:ideal:max:))

##### Tab views

- [func tabViewCustomization(Binding<TabViewCustomization>?) -> some View](/documentation/swiftui/view/tabviewcustomization(_:))
- [func defaultAdaptableTabBarPlacement(AdaptableTabBarPlacement) -> some View](/documentation/swiftui/view/defaultadaptabletabbarplacement(_:))
- [func tabViewSidebarHeader<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarheader(content:))
- [func tabViewSidebarFooter<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarfooter(content:))
- [func tabViewSidebarBottomBar<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/tabviewsidebarbottombar(content:))
- [func sectionActions<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/sectionactions(content:))

##### Toolbars

- [func toolbar(content:)](/documentation/swiftui/view/toolbar(content:))
- [func toolbar<Content>(id: String, content: () -> Content) -> some View](/documentation/swiftui/view/toolbar(id:content:))
- [func toolbar(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbar(_:for:))
- [func toolbar(removing: ToolbarDefaultItemKind?) -> some View](/documentation/swiftui/view/toolbar(removing:))
- [func toolbarVisibility(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarvisibility(_:for:))
- [func toolbarBackground(_:for:)](/documentation/swiftui/view/toolbarbackground(_:for:))
- [func toolbarBackgroundVisibility(Visibility, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarbackgroundvisibility(_:for:))
- [func toolbarForegroundStyle<S>(S, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarforegroundstyle(_:for:))
- [func toolbarColorScheme(ColorScheme?, for: ToolbarPlacement...) -> some View](/documentation/swiftui/view/toolbarcolorscheme(_:for:))
- [func toolbarRole(ToolbarRole) -> some View](/documentation/swiftui/view/toolbarrole(_:))
- [func toolbarTitleMenu<C>(content: () -> C) -> some View](/documentation/swiftui/view/toolbartitlemenu(content:))
- [func toolbarTitleDisplayMode(ToolbarTitleDisplayMode) -> some View](/documentation/swiftui/view/toolbartitledisplaymode(_:))
- [func ornament(visibility:attachmentAnchor:contentAlignment:ornament:)](/documentation/swiftui/view/ornament(visibility:attachmentanchor:contentalignment:ornament:))

##### Context menus

- [func contextMenu<MenuItems>(menuItems: () -> MenuItems) -> some View](/documentation/swiftui/view/contextmenu(menuitems:))
- [func contextMenu<M, P>(menuItems: () -> M, preview: () -> P) -> some View](/documentation/swiftui/view/contextmenu(menuitems:preview:))
- [func contextMenu<I, M>(forSelectionType: I.Type, menu: (Set<I>) -> M, primaryAction: ((Set<I>) -> Void)?) -> some View](/documentation/swiftui/view/contextmenu(forselectiontype:menu:primaryaction:))

##### Badges

- [func badge(_:)](/documentation/swiftui/view/badge(_:))
- [func badgeProminence(BadgeProminence) -> some View](/documentation/swiftui/view/badgeprominence(_:))

##### Help text

- [func help(_:)](/documentation/swiftui/view/help(_:))

##### Status bar

- [func statusBarHidden(Bool) -> some View](/documentation/swiftui/view/statusbarhidden(_:))

##### Touch Bar

- [func touchBar<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/touchbar(content:))
- [func touchBar<Content>(TouchBar<Content>) -> some View](/documentation/swiftui/view/touchbar(_:))
- [func touchBarItemPrincipal(Bool) -> some View](/documentation/swiftui/view/touchbaritemprincipal(_:))
- [func touchBarCustomizationLabel(Text) -> some View](/documentation/swiftui/view/touchbarcustomizationlabel(_:))
- [func touchBarItemPresence(TouchBarItemPresence) -> some View](/documentation/swiftui/view/touchbaritempresence(_:))
- [Chart view modifiers](/documentation/swiftui/view-chart-view)

##### Styles

- [func chartBackground<V>(alignment: Alignment, content: (ChartProxy) -> V) -> some View](/documentation/swiftui/view/chartbackground(alignment:content:))
- [func chartForegroundStyleScale<DataValue, S>(KeyValuePairs<DataValue, S>) -> some View](/documentation/swiftui/view/chartforegroundstylescale(_:))
- [func chartForegroundStyleScale<Domain, Range>(domain: Domain, range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartforegroundstylescale(domain:range:type:))
- [func chartForegroundStyleScale<Domain>(domain: Domain, type: ScaleType?) -> some View](/documentation/swiftui/view/chartforegroundstylescale(domain:type:))
- [func chartForegroundStyleScale<Domain, S>(domain: Domain, mapping: (Domain.Element) -> S) -> some View](/documentation/swiftui/view/chartforegroundstylescale(domain:mapping:))
- [func chartForegroundStyleScale<DataValue, S>(mapping: (DataValue) -> S) -> some View](/documentation/swiftui/view/chartforegroundstylescale(mapping:))
- [func chartForegroundStyleScale<Range>(range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartforegroundstylescale(range:type:))
- [func chartForegroundStyleScale(type: ScaleType?) -> some View](/documentation/swiftui/view/chartforegroundstylescale(type:))
- [func chartPlotStyle<Content>(content: (ChartPlotContent) -> Content) -> some View](/documentation/swiftui/view/chartplotstyle(content:))

##### Legends

- [func chartLegend(Visibility) -> some View](/documentation/swiftui/view/chartlegend(_:))
- [func chartLegend(position: AnnotationPosition, alignment: Alignment?, spacing: CGFloat?) -> some View](/documentation/swiftui/view/chartlegend(position:alignment:spacing:))
- [func chartLegend<Content>(position: AnnotationPosition, alignment: Alignment?, spacing: CGFloat?, content: () -> Content) -> some View](/documentation/swiftui/view/chartlegend(position:alignment:spacing:content:))

##### Overlays

- [func chartOverlay<V>(alignment: Alignment, content: (ChartProxy) -> V) -> some View](/documentation/swiftui/view/chartoverlay(alignment:content:))

##### Axes

- [func chartXAxis(Visibility) -> some View](/documentation/swiftui/view/chartxaxis(_:))
- [func chartXAxis<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/chartxaxis(content:))
- [func chartXAxisStyle<Content>(content: (ChartAxisContent) -> Content) -> some View](/documentation/swiftui/view/chartxaxisstyle(content:))
- [func chartYAxis(Visibility) -> some View](/documentation/swiftui/view/chartyaxis(_:))
- [func chartYAxis<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/chartyaxis(content:))
- [func chartYAxisStyle<Content>(content: (ChartAxisContent) -> Content) -> some View](/documentation/swiftui/view/chartyaxisstyle(content:))

##### Axis Labels

- [func chartXAxisLabel(_:position:alignment:spacing:)](/documentation/swiftui/view/chartxaxislabel(_:position:alignment:spacing:))
- [func chartXAxisLabel<C>(position: AnnotationPosition, alignment: Alignment?, spacing: CGFloat?, content: () -> C) -> some View](/documentation/swiftui/view/chartxaxislabel(position:alignment:spacing:content:))
- [func chartYAxisLabel(_:position:alignment:spacing:)](/documentation/swiftui/view/chartyaxislabel(_:position:alignment:spacing:))
- [func chartYAxisLabel<C>(position: AnnotationPosition, alignment: Alignment?, spacing: CGFloat?, content: () -> C) -> some View](/documentation/swiftui/view/chartyaxislabel(position:alignment:spacing:content:))

##### Axis scales

- [func chartXScale<Domain, Range>(domain: Domain, range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartxscale(domain:range:type:))
- [func chartXScale<Domain>(domain: Domain, type: ScaleType?) -> some View](/documentation/swiftui/view/chartxscale(domain:type:))
- [func chartXScale<Range>(range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartxscale(range:type:))
- [func chartXScale(type: ScaleType?) -> some View](/documentation/swiftui/view/chartxscale(type:))
- [func chartYScale<Domain, Range>(domain: Domain, range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartyscale(domain:range:type:))
- [func chartYScale<Domain>(domain: Domain, type: ScaleType?) -> some View](/documentation/swiftui/view/chartyscale(domain:type:))
- [func chartYScale<Range>(range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartyscale(range:type:))
- [func chartYScale(type: ScaleType?) -> some View](/documentation/swiftui/view/chartyscale(type:))

##### Symbol scales

- [func chartSymbolScale(_:)](/documentation/swiftui/view/chartsymbolscale(_:))
- [func chartSymbolScale<Domain>(domain: Domain) -> some View](/documentation/swiftui/view/chartsymbolscale(domain:))
- [func chartSymbolScale(domain:range:)](/documentation/swiftui/view/chartsymbolscale(domain:range:))
- [func chartSymbolScale<Domain, S>(domain: Domain, mapping: (Domain.Element) -> S) -> some View](/documentation/swiftui/view/chartsymbolscale(domain:mapping:))
- [func chartSymbolScale<DataValue, S>(mapping: (DataValue) -> S) -> some View](/documentation/swiftui/view/chartsymbolscale(mapping:))
- [func chartSymbolScale(range:)](/documentation/swiftui/view/chartsymbolscale(range:))

##### Symbol size scales

- [func chartSymbolSizeScale<DataValue>(KeyValuePairs<DataValue, CGFloat>) -> some View](/documentation/swiftui/view/chartsymbolsizescale(_:))
- [func chartSymbolSizeScale<Domain, Range>(domain: Domain, range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartsymbolsizescale(domain:range:type:))
- [func chartSymbolSizeScale<Domain>(domain: Domain, type: ScaleType?) -> some View](/documentation/swiftui/view/chartsymbolsizescale(domain:type:))
- [func chartSymbolSizeScale<Domain>(domain: Domain, mapping: (Domain.Element) -> CGFloat) -> some View](/documentation/swiftui/view/chartsymbolsizescale(domain:mapping:))
- [func chartSymbolSizeScale<DataValue>(mapping: (DataValue) -> CGFloat) -> some View](/documentation/swiftui/view/chartsymbolsizescale(mapping:))
- [func chartSymbolSizeScale<Range>(range: Range, type: ScaleType?) -> some View](/documentation/swiftui/view/chartsymbolsizescale(range:type:))
- [func chartSymbolSizeScale(type: ScaleType?) -> some View](/documentation/swiftui/view/chartsymbolsizescale(type:))

##### Line style scales

- [func chartLineStyleScale<DataValue>(KeyValuePairs<DataValue, StrokeStyle>) -> some View](/documentation/swiftui/view/chartlinestylescale(_:))
- [func chartLineStyleScale<Domain>(domain: Domain) -> some View](/documentation/swiftui/view/chartlinestylescale(domain:))
- [func chartLineStyleScale<Domain, Range>(domain: Domain, range: Range) -> some View](/documentation/swiftui/view/chartlinestylescale(domain:range:))
- [func chartLineStyleScale<Range>(range: Range) -> some View](/documentation/swiftui/view/chartlinestylescale(range:))
- [func chartLineStyleScale<Domain>(domain: Domain, mapping: (Domain.Element) -> StrokeStyle) -> some View](/documentation/swiftui/view/chartlinestylescale(domain:mapping:))
- [func chartLineStyleScale<DataValue>(mapping: (DataValue) -> StrokeStyle) -> some View](/documentation/swiftui/view/chartlinestylescale(mapping:))

##### Scrolling

- [func chartScrollPosition(initialX: some Plottable) -> some View](/documentation/swiftui/view/chartscrollposition(initialx:))
- [func chartScrollPosition(initialY: some Plottable) -> some View](/documentation/swiftui/view/chartscrollposition(initialy:))
- [func chartScrollPosition(x: Binding<some Plottable>) -> some View](/documentation/swiftui/view/chartscrollposition(x:))
- [func chartScrollPosition(y: Binding<some Plottable>) -> some View](/documentation/swiftui/view/chartscrollposition(y:))
- [func chartScrollTargetBehavior(some ChartScrollTargetBehavior) -> some View](/documentation/swiftui/view/chartscrolltargetbehavior(_:))
- [func chartScrollableAxes(Axis.Set) -> some View](/documentation/swiftui/view/chartscrollableaxes(_:))

##### Selection

- [func chartXSelection<P>(range: Binding<ClosedRange<P>?>) -> some View](/documentation/swiftui/view/chartxselection(range:))
- [func chartXSelection<P>(value: Binding<P?>) -> some View](/documentation/swiftui/view/chartxselection(value:))
- [func chartYSelection<P>(range: Binding<ClosedRange<P>?>) -> some View](/documentation/swiftui/view/chartyselection(range:))
- [func chartYSelection<P>(value: Binding<P?>) -> some View](/documentation/swiftui/view/chartyselection(value:))
- [func chartAngleSelection<P>(value: Binding<P?>) -> some View](/documentation/swiftui/view/chartangleselection(value:))

##### Visible domain

- [func chartXVisibleDomain<P>(length: P) -> some View](/documentation/swiftui/view/chartxvisibledomain(length:))
- [func chartYVisibleDomain<P>(length: P) -> some View](/documentation/swiftui/view/chartyvisibledomain(length:))

##### Interaction

- [func chartGesture((ChartProxy) -> some Gesture) -> some View](/documentation/swiftui/view/chartgesture(_:))

#### Drawing views

- [Style modifiers](/documentation/swiftui/view-style-modifiers)

##### Controls

- [func buttonStyle(_:)](/documentation/swiftui/view/buttonstyle(_:))
- [func datePickerStyle<S>(S) -> some View](/documentation/swiftui/view/datepickerstyle(_:))
- [func menuStyle<S>(S) -> some View](/documentation/swiftui/view/menustyle(_:))
- [func pickerStyle<S>(S) -> some View](/documentation/swiftui/view/pickerstyle(_:))
- [func toggleStyle<S>(S) -> some View](/documentation/swiftui/view/togglestyle(_:))

##### Indicators

- [func gaugeStyle<S>(S) -> some View](/documentation/swiftui/view/gaugestyle(_:))
- [func progressViewStyle<S>(S) -> some View](/documentation/swiftui/view/progressviewstyle(_:))

##### Text

- [func labelStyle<S>(S) -> some View](/documentation/swiftui/view/labelstyle(_:))
- [func textFieldStyle<S>(S) -> some View](/documentation/swiftui/view/textfieldstyle(_:))
- [func textEditorStyle(some TextEditorStyle) -> some View](/documentation/swiftui/view/texteditorstyle(_:))

##### Collections

- [func listStyle<S>(S) -> some View](/documentation/swiftui/view/liststyle(_:))
- [func tableStyle<S>(S) -> some View](/documentation/swiftui/view/tablestyle(_:))
- [func disclosureGroupStyle<S>(S) -> some View](/documentation/swiftui/view/disclosuregroupstyle(_:))

##### Presentation

- [func navigationSplitViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationsplitviewstyle(_:))
- [func tabViewStyle<S>(S) -> some View](/documentation/swiftui/view/tabviewstyle(_:))
- [func presentedWindowStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowstyle(_:))
- [func presentedWindowToolbarStyle<S>(S) -> some View](/documentation/swiftui/view/presentedwindowtoolbarstyle(_:))

##### Groups

- [func controlGroupStyle<S>(S) -> some View](/documentation/swiftui/view/controlgroupstyle(_:))
- [func groupBoxStyle<S>(S) -> some View](/documentation/swiftui/view/groupboxstyle(_:))
- [func indexViewStyle<S>(S) -> some View](/documentation/swiftui/view/indexviewstyle(_:))
- [Layout modifiers](/documentation/swiftui/view-layout)

##### Size

- [func frame(width: CGFloat?, height: CGFloat?, alignment: Alignment) -> some View](/documentation/swiftui/view/frame(width:height:alignment:))
- [func frame(depth: CGFloat?, alignment: DepthAlignment) -> some View](/documentation/swiftui/view/frame(depth:alignment:))
- [func frame(minWidth: CGFloat?, idealWidth: CGFloat?, maxWidth: CGFloat?, minHeight: CGFloat?, idealHeight: CGFloat?, maxHeight: CGFloat?, alignment: Alignment) -> some View](/documentation/swiftui/view/frame(minwidth:idealwidth:maxwidth:minheight:idealheight:maxheight:alignment:))
- [func frame(minDepth: CGFloat?, idealDepth: CGFloat?, maxDepth: CGFloat?, alignment: DepthAlignment) -> some View](/documentation/swiftui/view/frame(mindepth:idealdepth:maxdepth:alignment:))
- [func containerRelativeFrame(Axis.Set, alignment: Alignment) -> some View](/documentation/swiftui/view/containerrelativeframe(_:alignment:))
- [func containerRelativeFrame(Axis.Set, alignment: Alignment, (CGFloat, Axis) -> CGFloat) -> some View](/documentation/swiftui/view/containerrelativeframe(_:alignment:_:))
- [func containerRelativeFrame(Axis.Set, count: Int, span: Int, spacing: CGFloat, alignment: Alignment) -> some View](/documentation/swiftui/view/containerrelativeframe(_:count:span:spacing:alignment:))
- [func fixedSize() -> some View](/documentation/swiftui/view/fixedsize())
- [func fixedSize(horizontal: Bool, vertical: Bool) -> some View](/documentation/swiftui/view/fixedsize(horizontal:vertical:))
- [func layoutPriority(Double) -> some View](/documentation/swiftui/view/layoutpriority(_:))

##### Position

- [func position(CGPoint) -> some View](/documentation/swiftui/view/position(_:))
- [func position(x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/position(x:y:))
- [func offset(CGSize) -> some View](/documentation/swiftui/view/offset(_:))
- [func offset(x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/offset(x:y:))
- [func offset(z: CGFloat) -> some View](/documentation/swiftui/view/offset(z:))
- [func coordinateSpace(NamedCoordinateSpace) -> some View](/documentation/swiftui/view/coordinatespace(_:))

##### Alignment

- [func alignmentGuide(_:computeValue:)](/documentation/swiftui/view/alignmentguide(_:computevalue:))

##### Padding and spacing

- [func padding(_:)](/documentation/swiftui/view/padding(_:))
- [func padding(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding(_:_:))
- [func padding3D(_:)](/documentation/swiftui/view/padding3d(_:))
- [func padding3D(Edge3D.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding3d(_:_:))
- [func listRowInsets(EdgeInsets?) -> some View](/documentation/swiftui/view/listrowinsets(_:))
- [func scenePadding(Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:))
- [func scenePadding(ScenePadding, edges: Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:edges:))
- [func listRowSpacing(CGFloat?) -> some View](/documentation/swiftui/view/listrowspacing(_:))
- [func listSectionSpacing(_:)](/documentation/swiftui/view/listsectionspacing(_:))

##### Grid configuration

- [func gridCellColumns(Int) -> some View](/documentation/swiftui/view/gridcellcolumns(_:))
- [func gridCellAnchor(UnitPoint) -> some View](/documentation/swiftui/view/gridcellanchor(_:))
- [func gridCellUnsizedAxes(Axis.Set) -> some View](/documentation/swiftui/view/gridcellunsizedaxes(_:))
- [func gridColumnAlignment(HorizontalAlignment) -> some View](/documentation/swiftui/view/gridcolumnalignment(_:))

##### Safe area and margins

- [func ignoresSafeArea(SafeAreaRegions, edges: Edge.Set) -> some View](/documentation/swiftui/view/ignoressafearea(_:edges:))
- [func safeAreaInset(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareainset(edge:alignment:spacing:content:))
- [func safeAreaPadding(_:)](/documentation/swiftui/view/safeareapadding(_:))
- [func safeAreaPadding(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/safeareapadding(_:_:))
- [func contentMargins(CGFloat, for: ContentMarginPlacement) -> some View](/documentation/swiftui/view/contentmargins(_:for:))
- [func contentMargins(_:_:for:)](/documentation/swiftui/view/contentmargins(_:_:for:))

##### Layer order

- [func zIndex(Double) -> some View](/documentation/swiftui/view/zindex(_:))

##### Layout direction

- [func layoutDirectionBehavior(LayoutDirectionBehavior) -> some View](/documentation/swiftui/view/layoutdirectionbehavior(_:))

##### Custom layout characteristics

- [func layoutValue<K>(key: K.Type, value: K.Value) -> some View](/documentation/swiftui/view/layoutvalue(key:value:))
- [Graphics and rendering modifiers](/documentation/swiftui/view-graphics-and-rendering)

##### Masks and clipping

- [func mask<Mask>(alignment: Alignment, () -> Mask) -> some View](/documentation/swiftui/view/mask(alignment:_:))
- [func clipped(antialiased: Bool) -> some View](/documentation/swiftui/view/clipped(antialiased:))
- [func clipShape<S>(S, style: FillStyle) -> some View](/documentation/swiftui/view/clipshape(_:style:))
- [func containerShape(_:)](/documentation/swiftui/view/containershape(_:))

##### Scale

- [func scaledToFill() -> some View](/documentation/swiftui/view/scaledtofill())
- [func scaledToFit() -> some View](/documentation/swiftui/view/scaledtofit())
- [func scaleEffect(_:anchor:)](/documentation/swiftui/view/scaleeffect(_:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, anchor: UnitPoint) -> some View](/documentation/swiftui/view/scaleeffect(x:y:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, z: CGFloat, anchor: UnitPoint3D) -> some View](/documentation/swiftui/view/scaleeffect(x:y:z:anchor:))
- [func imageScale(Image.Scale) -> some View](/documentation/swiftui/view/imagescale(_:))
- [func aspectRatio(_:contentMode:)](/documentation/swiftui/view/aspectratio(_:contentmode:))

##### Rotation and transformation

- [func rotationEffect(Angle, anchor: UnitPoint) -> some View](/documentation/swiftui/view/rotationeffect(_:anchor:))
- [func rotation3DEffect(Rotation3D, anchor: UnitPoint3D) -> some View](/documentation/swiftui/view/rotation3deffect(_:anchor:))
- [func rotation3DEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint, anchorZ: CGFloat, perspective: CGFloat) -> some View](/documentation/swiftui/view/rotation3deffect(_:axis:anchor:anchorz:perspective:))
- [func rotation3DEffect(_:axis:anchor:)](/documentation/swiftui/view/rotation3deffect(_:axis:anchor:))
- [func perspectiveRotationEffect(Angle, axis: (x: CGFloat, y: CGFloat, z: CGFloat), anchor: UnitPoint, anchorZ: CGFloat, perspective: CGFloat) -> some View](/documentation/swiftui/view/perspectiverotationeffect(_:axis:anchor:anchorz:perspective:))
- [func projectionEffect(ProjectionTransform) -> some View](/documentation/swiftui/view/projectioneffect(_:))
- [func transformEffect(CGAffineTransform) -> some View](/documentation/swiftui/view/transformeffect(_:))
- [func transform3DEffect(AffineTransform3D) -> some View](/documentation/swiftui/view/transform3deffect(_:))

##### Graphical effects

- [func blur(radius: CGFloat, opaque: Bool) -> some View](/documentation/swiftui/view/blur(radius:opaque:))
- [func opacity(Double) -> some View](/documentation/swiftui/view/opacity(_:))
- [func brightness(Double) -> some View](/documentation/swiftui/view/brightness(_:))
- [func contrast(Double) -> some View](/documentation/swiftui/view/contrast(_:))
- [func colorInvert() -> some View](/documentation/swiftui/view/colorinvert())
- [func colorMultiply(Color) -> some View](/documentation/swiftui/view/colormultiply(_:))
- [func saturation(Double) -> some View](/documentation/swiftui/view/saturation(_:))
- [func grayscale(Double) -> some View](/documentation/swiftui/view/grayscale(_:))
- [func hueRotation(Angle) -> some View](/documentation/swiftui/view/huerotation(_:))
- [func luminanceToAlpha() -> some View](/documentation/swiftui/view/luminancetoalpha())
- [func shadow(color: Color, radius: CGFloat, x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/shadow(color:radius:x:y:))
- [func visualEffect((EmptyVisualEffect, GeometryProxy) -> some VisualEffect) -> some View](/documentation/swiftui/view/visualeffect(_:))
- [func visualEffect3D((EmptyVisualEffect, GeometryProxy3D) -> some VisualEffect) -> some View](/documentation/swiftui/view/visualeffect3d(_:))

##### Shaders

- [func colorEffect(Shader, isEnabled: Bool) -> some View](/documentation/swiftui/view/coloreffect(_:isenabled:))
- [func distortionEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some View](/documentation/swiftui/view/distortioneffect(_:maxsampleoffset:isenabled:))
- [func layerEffect(Shader, maxSampleOffset: CGSize, isEnabled: Bool) -> some View](/documentation/swiftui/view/layereffect(_:maxsampleoffset:isenabled:))

##### Composites

- [func blendMode(BlendMode) -> some View](/documentation/swiftui/view/blendmode(_:))
- [func compositingGroup() -> some View](/documentation/swiftui/view/compositinggroup())
- [func drawingGroup(opaque: Bool, colorMode: ColorRenderingMode) -> some View](/documentation/swiftui/view/drawinggroup(opaque:colormode:))

##### Animations

- [func animation(_:)](/documentation/swiftui/view/animation(_:))
- [func animation<V>(Animation?, value: V) -> some View](/documentation/swiftui/view/animation(_:value:))
- [func animation<V>(Animation?, body: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/animation(_:body:))
- [func keyframeAnimator<Value>(initialValue: Value, repeating: Bool, content: (PlaceholderContentView<Self>, Value) -> some View, keyframes: (Value) -> some Keyframes) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:repeating:content:keyframes:))
- [func keyframeAnimator<Value>(initialValue: Value, trigger: some Equatable, content: (PlaceholderContentView<Self>, Value) -> some View, keyframes: (Value) -> some Keyframes) -> some View](/documentation/swiftui/view/keyframeanimator(initialvalue:trigger:content:keyframes:))
- [func phaseAnimator<Phase>(some Sequence, content: (PlaceholderContentView<Self>, Phase) -> some View, animation: (Phase) -> Animation?) -> some View](/documentation/swiftui/view/phaseanimator(_:content:animation:))
- [func phaseAnimator<Phase>(some Sequence, trigger: some Equatable, content: (PlaceholderContentView<Self>, Phase) -> some View, animation: (Phase) -> Animation?) -> some View](/documentation/swiftui/view/phaseanimator(_:trigger:content:animation:))
- [func contentTransition(ContentTransition) -> some View](/documentation/swiftui/view/contenttransition(_:))
- [func transition(_:)](/documentation/swiftui/view/transition(_:))
- [func transaction((inout Transaction) -> Void) -> some View](/documentation/swiftui/view/transaction(_:))
- [func transaction(value: some Equatable, (inout Transaction) -> Void) -> some View](/documentation/swiftui/view/transaction(value:_:))
- [func transaction<V>((inout Transaction) -> Void, body: (PlaceholderContentView<Self>) -> V) -> some View](/documentation/swiftui/view/transaction(_:body:))
- [func contentTransition(ContentTransition) -> some View](/documentation/swiftui/view/contenttransition(_:))
- [func matchedGeometryEffect<ID>(id: ID, in: Namespace.ID, properties: MatchedGeometryProperties, anchor: UnitPoint, isSource: Bool) -> some View](/documentation/swiftui/view/matchedgeometryeffect(id:in:properties:anchor:issource:))
- [func geometryGroup() -> some View](/documentation/swiftui/view/geometrygroup())

#### Providing interactivity

- [Input and event modifiers](/documentation/swiftui/view-input-and-events)

##### Interactivity

- [func disabled(Bool) -> some View](/documentation/swiftui/view/disabled(_:))
- [func interactionActivityTrackingTag(String) -> some View](/documentation/swiftui/view/interactionactivitytrackingtag(_:))

##### List controls

- [func swipeActions<T>(edge: HorizontalEdge, allowsFullSwipe: Bool, content: () -> T) -> some View](/documentation/swiftui/view/swipeactions(edge:allowsfullswipe:content:))
- [func refreshable(action: () async -> Void) -> some View](/documentation/swiftui/view/refreshable(action:))
- [func selectionDisabled(Bool) -> some View](/documentation/swiftui/view/selectiondisabled(_:))

##### Scroll controls

- [func scrollPosition(Binding<ScrollPosition>, anchor: UnitPoint?) -> some View](/documentation/swiftui/view/scrollposition(_:anchor:))
- [func scrollPosition(id: Binding<(some Hashable)?>, anchor: UnitPoint?) -> some View](/documentation/swiftui/view/scrollposition(id:anchor:))
- [func defaultScrollAnchor(UnitPoint?) -> some View](/documentation/swiftui/view/defaultscrollanchor(_:))
- [func defaultScrollAnchor(UnitPoint?, for: ScrollAnchorRole) -> some View](/documentation/swiftui/view/defaultscrollanchor(_:for:))
- [func scrollTargetBehavior(some ScrollTargetBehavior) -> some View](/documentation/swiftui/view/scrolltargetbehavior(_:))
- [func scrollTargetLayout(isEnabled: Bool) -> some View](/documentation/swiftui/view/scrolltargetlayout(isenabled:))
- [func scrollTransition(ScrollTransitionConfiguration, axis: Axis?, transition: (EmptyVisualEffect, ScrollTransitionPhase) -> some VisualEffect) -> some View](/documentation/swiftui/view/scrolltransition(_:axis:transition:))
- [func scrollTransition(topLeading: ScrollTransitionConfiguration, bottomTrailing: ScrollTransitionConfiguration, axis: Axis?, transition: (EmptyVisualEffect, ScrollTransitionPhase) -> some VisualEffect) -> some View](/documentation/swiftui/view/scrolltransition(topleading:bottomtrailing:axis:transition:))
- [func onScrollGeometryChange<T>(for: T.Type, of: (ScrollGeometry) -> T, action: (T, T) -> Void) -> some View](/documentation/swiftui/view/onscrollgeometrychange(for:of:action:))
- [func onScrollTargetVisibilityChange<ID>(idType: ID.Type, threshold: Double, ([ID]) -> Void) -> some View](/documentation/swiftui/view/onscrolltargetvisibilitychange(idtype:threshold:_:))
- [func onScrollVisibilityChange(threshold: Double, (Bool) -> Void) -> some View](/documentation/swiftui/view/onscrollvisibilitychange(threshold:_:))
- [func onScrollPhaseChange(_:)](/documentation/swiftui/view/onscrollphasechange(_:))

##### Geometry

- [func onGeometryChange(for:of:action:)](/documentation/swiftui/view/ongeometrychange(for:of:action:))

##### Taps and gestures

- [func onTapGesture(count: Int, perform: () -> Void) -> some View](/documentation/swiftui/view/ontapgesture(count:perform:))
- [func onTapGesture(count:coordinateSpace:perform:)](/documentation/swiftui/view/ontapgesture(count:coordinatespace:perform:))
- [func onLongPressGesture(minimumDuration: Double, maximumDistance: CGFloat, perform: () -> Void, onPressingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:maximumdistance:perform:onpressingchanged:))
- [func onLongPressGesture(minimumDuration: Double, perform: () -> Void, onPressingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:perform:onpressingchanged:))
- [func onLongTouchGesture(minimumDuration: Double, perform: () -> Void, onTouchingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongtouchgesture(minimumduration:perform:ontouchingchanged:))
- [func gesture(_:)](/documentation/swiftui/view/gesture(_:))
- [func gesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/gesture(_:isenabled:))
- [func gesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/gesture(_:name:isenabled:))
- [func gesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/gesture(_:including:))
- [func highPriorityGesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/highprioritygesture(_:including:))
- [func highPriorityGesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/highprioritygesture(_:isenabled:))
- [func highPriorityGesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/highprioritygesture(_:name:isenabled:))
- [func simultaneousGesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/simultaneousgesture(_:including:))
- [func simultaneousGesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/simultaneousgesture(_:isenabled:))
- [func simultaneousGesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/simultaneousgesture(_:name:isenabled:))
- [func defersSystemGestures(on: Edge.Set) -> some View](/documentation/swiftui/view/deferssystemgestures(on:))
- [func onPencilDoubleTap(perform: (PencilDoubleTapGestureValue) -> Void) -> some View](/documentation/swiftui/view/onpencildoubletap(perform:))
- [func onPencilSqueeze(perform: (PencilSqueezeGesturePhase) -> Void) -> some View](/documentation/swiftui/view/onpencilsqueeze(perform:))
- [func allowsWindowActivationEvents(Bool?) -> some View](/documentation/swiftui/view/allowswindowactivationevents(_:))

##### Keyboard input

- [func onKeyPress(KeyEquivalent, action: () -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(_:action:))
- [func onKeyPress(phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(phases:action:))
- [func onKeyPress(KeyEquivalent, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(_:phases:action:))
- [func onKeyPress(characters: CharacterSet, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(characters:phases:action:))
- [func onKeyPress(keys: Set<KeyEquivalent>, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(keys:phases:action:))
- [func onModifierKeysChanged(mask: EventModifiers, initial: Bool, (EventModifiers, EventModifiers) -> Void) -> some View](/documentation/swiftui/view/onmodifierkeyschanged(mask:initial:_:))

##### Keyboard shortcuts

- [func keyboardShortcut(_:)](/documentation/swiftui/view/keyboardshortcut(_:))
- [func keyboardShortcut(KeyEquivalent, modifiers: EventModifiers) -> some View](/documentation/swiftui/view/keyboardshortcut(_:modifiers:))
- [func keyboardShortcut(KeyEquivalent, modifiers: EventModifiers, localization: KeyboardShortcut.Localization) -> some View](/documentation/swiftui/view/keyboardshortcut(_:modifiers:localization:))
- [func modifierKeyAlternate<V>(EventModifiers, () -> V) -> some View](/documentation/swiftui/view/modifierkeyalternate(_:_:))

##### Hover

- [func onHover(perform: (Bool) -> Void) -> some View](/documentation/swiftui/view/onhover(perform:))
- [func onContinuousHover(coordinateSpace:perform:)](/documentation/swiftui/view/oncontinuoushover(coordinatespace:perform:))
- [func hoverEffect(HoverEffect) -> some View](/documentation/swiftui/view/hovereffect(_:))
- [func hoverEffect(_:isEnabled:)](/documentation/swiftui/view/hovereffect(_:isenabled:))
- [func hoverEffect(some CustomHoverEffect, in: HoverEffectGroup?, isEnabled: Bool) -> some View](/documentation/swiftui/view/hovereffect(_:in:isenabled:))
- [func hoverEffect(in: HoverEffectGroup?, isEnabled: Bool, body: (EmptyHoverEffectContent, Bool, GeometryProxy) -> some HoverEffectContent) -> some View](/documentation/swiftui/view/hovereffect(in:isenabled:body:))
- [func hoverEffectGroup() -> some View](/documentation/swiftui/view/hovereffectgroup())
- [func hoverEffectGroup(HoverEffectGroup?) -> some View](/documentation/swiftui/view/hovereffectgroup(_:))
- [func hoverEffectGroup(id: String?, in: Namespace.ID, behavior: HoverEffectGroup.Behavior) -> some View](/documentation/swiftui/view/hovereffectgroup(id:in:behavior:))
- [func hoverEffectDisabled(Bool) -> some View](/documentation/swiftui/view/hovereffectdisabled(_:))
- [func defaultHoverEffect(_:)](/documentation/swiftui/view/defaulthovereffect(_:))
- [func listRowHoverEffect(HoverEffect?) -> some View](/documentation/swiftui/view/listrowhovereffect(_:))
- [func listRowHoverEffectDisabled(Bool) -> some View](/documentation/swiftui/view/listrowhovereffectdisabled(_:))

##### Pointer

- [func pointerVisibility(Visibility) -> some View](/documentation/swiftui/view/pointervisibility(_:))
- [func pointerStyle(PointerStyle?) -> some View](/documentation/swiftui/view/pointerstyle(_:))

##### Focus

- [func focused<Value>(FocusState<Value>.Binding, equals: Value) -> some View](/documentation/swiftui/view/focused(_:equals:))
- [func focused(FocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/focused(_:))
- [func focusedValue<T>(T?) -> some View](/documentation/swiftui/view/focusedvalue(_:))
- [func focusedValue(_:_:)](/documentation/swiftui/view/focusedvalue(_:_:))
- [func focusedSceneValue<T>(T?) -> some View](/documentation/swiftui/view/focusedscenevalue(_:))
- [func focusedSceneValue(_:_:)](/documentation/swiftui/view/focusedscenevalue(_:_:))
- [func focusedObject(_:)](/documentation/swiftui/view/focusedobject(_:))
- [func focusedSceneObject(_:)](/documentation/swiftui/view/focusedsceneobject(_:))
- [func prefersDefaultFocus(Bool, in: Namespace.ID) -> some View](/documentation/swiftui/view/prefersdefaultfocus(_:in:))
- [func focusScope(Namespace.ID) -> some View](/documentation/swiftui/view/focusscope(_:))
- [func focusSection() -> some View](/documentation/swiftui/view/focussection())
- [func focusable(Bool) -> some View](/documentation/swiftui/view/focusable(_:))
- [func focusable(Bool, interactions: FocusInteractions) -> some View](/documentation/swiftui/view/focusable(_:interactions:))
- [func focusEffectDisabled(Bool) -> some View](/documentation/swiftui/view/focuseffectdisabled(_:))
- [func defaultFocus<V>(FocusState<V>.Binding, V, priority: DefaultFocusEvaluationPriority) -> some View](/documentation/swiftui/view/defaultfocus(_:_:priority:))
- [func searchFocused(FocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/searchfocused(_:))
- [func searchFocused<V>(FocusState<V>.Binding, equals: V) -> some View](/documentation/swiftui/view/searchfocused(_:equals:))

##### Copy and paste

- [func copyable<T>(@autoclosure () -> [T]) -> some View](/documentation/swiftui/view/copyable(_:))
- [func cuttable<T>(for: T.Type, action: () -> [T]) -> some View](/documentation/swiftui/view/cuttable(for:action:))
- [func pasteDestination<T>(for: T.Type, action: ([T]) -> Void, validator: ([T]) -> [T]) -> some View](/documentation/swiftui/view/pastedestination(for:action:validator:))
- [func onCopyCommand(perform: (() -> [NSItemProvider])?) -> some View](/documentation/swiftui/view/oncopycommand(perform:))
- [func onCutCommand(perform: (() -> [NSItemProvider])?) -> some View](/documentation/swiftui/view/oncutcommand(perform:))
- [func onPasteCommand(of:perform:)](/documentation/swiftui/view/onpastecommand(of:perform:))
- [func onPasteCommand(of:validator:perform:)](/documentation/swiftui/view/onpastecommand(of:validator:perform:))

##### Drag and drop

- [func onDrag<V>(() -> NSItemProvider, preview: () -> V) -> some View](/documentation/swiftui/view/ondrag(_:preview:))
- [func onDrag(() -> NSItemProvider) -> some View](/documentation/swiftui/view/ondrag(_:))
- [func itemProvider(Optional<() -> NSItemProvider?>) -> some View](/documentation/swiftui/view/itemprovider(_:))
- [func onDrop(of:isTargeted:perform:)](/documentation/swiftui/view/ondrop(of:istargeted:perform:))
- [func onDrop(of:delegate:)](/documentation/swiftui/view/ondrop(of:delegate:))
- [func dropDestination<T>(for: T.Type, action: ([T], CGPoint) -> Bool, isTargeted: (Bool) -> Void) -> some View](/documentation/swiftui/view/dropdestination(for:action:istargeted:))
- [func draggable<T>(@autoclosure () -> T) -> some View](/documentation/swiftui/view/draggable(_:))
- [func draggable<V, T>(@autoclosure () -> T, preview: () -> V) -> some View](/documentation/swiftui/view/draggable(_:preview:))
- [func springLoadingBehavior(SpringLoadingBehavior) -> some View](/documentation/swiftui/view/springloadingbehavior(_:))

##### Submission

- [func onAssignedDocumentDidSubmit((URL) -> Void) -> some View](/documentation/swiftui/view/onassigneddocumentdidsubmit(_:))
- [func onAssignedDocumentDidWithdraw((URL) -> Void) -> some View](/documentation/swiftui/view/onassigneddocumentdidwithdraw(_:))
- [func onAssignedDocumentWillSubmit((URL) async -> Bool) -> some View](/documentation/swiftui/view/onassigneddocumentwillsubmit(_:))
- [func onAssignedDocumentWillWithdraw((URL) async -> Bool) -> some View](/documentation/swiftui/view/onassigneddocumentwillwithdraw(_:))
- [func onSubmit(of: SubmitTriggers, () -> Void) -> some View](/documentation/swiftui/view/onsubmit(of:_:))
- [func submitScope(Bool) -> some View](/documentation/swiftui/view/submitscope(_:))
- [func submitLabel(SubmitLabel) -> some View](/documentation/swiftui/view/submitlabel(_:))

##### Movement

- [func onMoveCommand(perform: ((MoveCommandDirection) -> Void)?) -> some View](/documentation/swiftui/view/onmovecommand(perform:))
- [func moveDisabled(Bool) -> some View](/documentation/swiftui/view/movedisabled(_:))

##### Deletion

- [func onDeleteCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/ondeletecommand(perform:))
- [func deleteDisabled(Bool) -> some View](/documentation/swiftui/view/deletedisabled(_:))

##### Commands

- [func pageCommand<V>(value: Binding<V>, in: ClosedRange<V>, step: V) -> some View](/documentation/swiftui/view/pagecommand(value:in:step:))
- [func onExitCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onexitcommand(perform:))
- [func onPlayPauseCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onplaypausecommand(perform:))
- [func onCommand(Selector, perform: (() -> Void)?) -> some View](/documentation/swiftui/view/oncommand(_:perform:))

##### Digital crown

- [func digitalCrownAccessory(Visibility) -> some View](/documentation/swiftui/view/digitalcrownaccessory(_:))
- [func digitalCrownAccessory<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/digitalcrownaccessory(content:))
- [func digitalCrownRotation<V>(Binding<V>, from: V, through: V, sensitivity: DigitalCrownRotationalSensitivity, isContinuous: Bool, isHapticFeedbackEnabled: Bool, onChange: (DigitalCrownEvent) -> Void, onIdle: () -> Void) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:from:through:sensitivity:iscontinuous:ishapticfeedbackenabled:onchange:onidle:))
- [func digitalCrownRotation<V>(Binding<V>, onChange: (DigitalCrownEvent) -> Void, onIdle: () -> Void) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:onchange:onidle:))
- [func digitalCrownRotation(detent:from:through:by:sensitivity:isContinuous:isHapticFeedbackEnabled:onChange:onIdle:)](/documentation/swiftui/view/digitalcrownrotation(detent:from:through:by:sensitivity:iscontinuous:ishapticfeedbackenabled:onchange:onidle:))
- [func digitalCrownRotation<V>(Binding<V>) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:))
- [func digitalCrownRotation<V>(Binding<V>, from: V, through: V, by: V.Stride?, sensitivity: DigitalCrownRotationalSensitivity, isContinuous: Bool, isHapticFeedbackEnabled: Bool) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:from:through:by:sensitivity:iscontinuous:ishapticfeedbackenabled:))

##### Immersive Spaces

- [func onImmersionChange(initial: Bool, (ImmersionChangeContext, ImmersionChangeContext) -> Void) -> some View](/documentation/swiftui/view/onimmersionchange(initial:_:))

##### Volumes

- [func onVolumeViewpointChange(updateStrategy: VolumeViewpointUpdateStrategy, initial: Bool, (Viewpoint3D, Viewpoint3D) -> Void) -> some View](/documentation/swiftui/view/onvolumeviewpointchange(updatestrategy:initial:_:))
- [func supportedVolumeViewpoints(SquareAzimuth.Set) -> some View](/documentation/swiftui/view/supportedvolumeviewpoints(_:))

##### User activities

- [func userActivity<P>(String, element: P?, (P, NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/useractivity(_:element:_:))
- [func userActivity(String, isActive: Bool, (NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/useractivity(_:isactive:_:))
- [func onContinueUserActivity(String, perform: (NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/oncontinueuseractivity(_:perform:))
- [func handlesExternalEvents(preferring: Set<String>, allowing: Set<String>) -> some View](/documentation/swiftui/view/handlesexternalevents(preferring:allowing:))

##### View life cycle

- [func onAppear(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onappear(perform:))
- [func onDisappear(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/ondisappear(perform:))
- [func onChange(of:initial:_:)](/documentation/swiftui/view/onchange(of:initial:_:))

##### File renaming

- [func renameAction(_:)](/documentation/swiftui/view/renameaction(_:))

##### URLs

- [func onOpenURL(perform: (URL) -> ()) -> some View](/documentation/swiftui/view/onopenurl(perform:))
- [func widgetURL(URL?) -> some View](/documentation/swiftui/view/widgeturl(_:))

##### Publisher events

- [func onReceive<P>(P, perform: (P.Output) -> Void) -> some View](/documentation/swiftui/view/onreceive(_:perform:))

##### Hit testing

- [func allowsHitTesting(Bool) -> some View](/documentation/swiftui/view/allowshittesting(_:))

##### Content shape

- [func contentShape<S>(S, eoFill: Bool) -> some View](/documentation/swiftui/view/contentshape(_:eofill:))
- [func contentShape<S>(ContentShapeKinds, S, eoFill: Bool) -> some View](/documentation/swiftui/view/contentshape(_:_:eofill:))

##### Import and export

- [func exportsItemProviders([UTType], onExport: () -> [NSItemProvider]) -> some View](/documentation/swiftui/view/exportsitemproviders(_:onexport:))
- [func exportsItemProviders([UTType], onExport: () -> [NSItemProvider], onEdit: ([NSItemProvider]) -> Bool) -> some View](/documentation/swiftui/view/exportsitemproviders(_:onexport:onedit:))
- [func importsItemProviders([UTType], onImport: ([NSItemProvider]) -> Bool) -> some View](/documentation/swiftui/view/importsitemproviders(_:onimport:))
- [func exportableToServices<T>(@autoclosure () -> [T]) -> some View](/documentation/swiftui/view/exportabletoservices(_:))
- [func exportableToServices<T>(@autoclosure () -> [T], onEdit: ([T]) -> Bool) -> some View](/documentation/swiftui/view/exportabletoservices(_:onedit:))
- [func importableFromServices<T>(for: T.Type, action: ([T]) -> Bool) -> some View](/documentation/swiftui/view/importablefromservices(for:action:))

##### App intents

- [func shortcutsLinkStyle(ShortcutsLinkStyle) -> some View](/documentation/swiftui/view/shortcutslinkstyle(_:))
- [func siriTipViewStyle(SiriTipViewStyle) -> some View](/documentation/swiftui/view/siritipviewstyle(_:))

##### Camera

- [func onCameraCaptureEvent(isEnabled: Bool, action: (AVCaptureEvent) -> Void) -> some View](/documentation/swiftui/view/oncameracaptureevent(isenabled:action:))
- [func onCameraCaptureEvent(isEnabled: Bool, primaryAction: (AVCaptureEvent) -> Void, secondaryAction: (AVCaptureEvent) -> Void) -> some View](/documentation/swiftui/view/oncameracaptureevent(isenabled:primaryaction:secondaryaction:))
- [func cameraAnchor(isActive: Bool) -> some View](/documentation/swiftui/view/cameraanchor(isactive:))
- [Search modifiers](/documentation/swiftui/view-search)

##### Displaying a search interface

- [func searchable(text:placement:prompt:)](/documentation/swiftui/view/searchable(text:placement:prompt:))
- [func searchable(text:isPresented:placement:prompt:)](/documentation/swiftui/view/searchable(text:ispresented:placement:prompt:))
- [func searchPresentationToolbarBehavior(SearchPresentationToolbarBehavior) -> some View](/documentation/swiftui/view/searchpresentationtoolbarbehavior(_:))

##### Searching with tokens

- [func searchable(text:tokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:placement:prompt:token:))
- [func searchable(text:tokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:ispresented:placement:prompt:token:))

##### Searching with editable tokens

- [func searchable(text:editableTokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:editabletokens:ispresented:placement:prompt:token:))
- [func searchable(text:editableTokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:editabletokens:placement:prompt:token:))

##### Making search suggestions

- [func searchSuggestions<S>(() -> S) -> some View](/documentation/swiftui/view/searchsuggestions(_:))
- [func searchSuggestions(Visibility, for: SearchSuggestionsPlacement.Set) -> some View](/documentation/swiftui/view/searchsuggestions(_:for:))
- [func searchCompletion(_:)](/documentation/swiftui/view/searchcompletion(_:))
- [func searchable(text:tokens:suggestedTokens:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:placement:prompt:token:))
- [func searchable(text:tokens:suggestedTokens:isPresented:placement:prompt:token:)](/documentation/swiftui/view/searchable(text:tokens:suggestedtokens:ispresented:placement:prompt:token:))

##### Limiting search scope

- [func searchScopes<V, S>(Binding<V>, scopes: () -> S) -> some View](/documentation/swiftui/view/searchscopes(_:scopes:))
- [func searchScopes<V, S>(Binding<V>, activation: SearchScopeActivation, () -> S) -> some View](/documentation/swiftui/view/searchscopes(_:activation:_:))

##### Searching through dictation

- [func searchDictationBehavior(TextInputDictationBehavior) -> some View](/documentation/swiftui/view/searchdictationbehavior(_:))
- [Presentation modifiers](/documentation/swiftui/view-presentation)

##### Alerts
