# Views: Styling and Animation — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [View Fundamentals](#view-fundamentals)
- [Previews](#previews)
- [Accessibility Modifiers](#accessibility-modifiers)
- [Appearance Modifiers](#appearance-modifiers)
- [Text and Symbol Modifiers](#text-and-symbol-modifiers)
- [Style Modifiers](#style-modifiers)
- [Layout Modifiers](#layout-modifiers)
- [Graphics and Rendering Modifiers](#graphics-and-rendering-modifiers)
- [Animation Modifiers](#animation-modifiers)
- [Input and Event Modifiers](#input-and-event-modifiers)
- [Search Modifiers](#search-modifiers)
- [Presentation Modifiers](#presentation-modifiers)

---

### View Fundamentals

- [View fundamentals](/documentation/swiftui/view-fundamentals) (article)
- [Declaring a custom view](/documentation/swiftui/declaring-a-custom-view) (article)
- [View](/documentation/swiftui/view) — base protocol for all views
- `var body: Self.Body` — required computed property for custom views
- `func modifier<T>(T) -> ModifiedContent<Self, T>` — apply a ViewModifier

### Previews

- [Previews in Xcode](/documentation/swiftui/previews-in-xcode) (article)
- [Previewing your app's interface in Xcode](/documentation/xcode/previewing-your-apps-interface-in-xcode) (article)
- `macro Preview(...)` — create a preview; variants for traits, cameras, windowStyle, immersionStyle at `/documentation/swiftui/preview(_:body:)` and related paths
- `macro Previewable()` — make @State usable in previews `/documentation/swiftui/previewable()`
- [PreviewProvider](/documentation/swiftui/previewprovider) — legacy preview protocol [legacy -> prefer macro Preview]
- [PreviewPlatform](/documentation/swiftui/previewplatform) — cases: iOS, macOS, tvOS, watchOS
- [PreviewModifier](/documentation/swiftui/previewmodifier) — shared context for preview customization
- [PreviewModifierContent](/documentation/swiftui/previewmodifiercontent) — content type for PreviewModifier
- [PreviewDevice](/documentation/swiftui/previewdevice) — specify preview device
- `func previewDevice(PreviewDevice?)` `/documentation/swiftui/view/previewdevice(_:)`
- `func previewDisplayName(String?)` `/documentation/swiftui/view/previewdisplayname(_:)`
- `func previewLayout(PreviewLayout)` `/documentation/swiftui/view/previewlayout(_:)`
- `func previewInterfaceOrientation(InterfaceOrientation)` `/documentation/swiftui/view/previewinterfaceorientation(_:)`
- [InterfaceOrientation](/documentation/swiftui/interfaceorientation) — portrait, portraitUpsideDown, landscapeLeft, landscapeRight
- `func previewContext<C>(C)` `/documentation/swiftui/view/previewcontext(_:)`
- [PreviewContext](/documentation/swiftui/previewcontext), [PreviewContextKey](/documentation/swiftui/previewcontextkey) — key-value context for previews
- [DebugReplaceableView](/documentation/swiftui/debugreplaceableview) — debug-mode view replacement

### Accessibility Modifiers

- [Accessibility modifiers](/documentation/swiftui/view-accessibility) (article)
- Labels: `accessibilityLabel(_:)`, `accessibilityInputLabels(_:)`, `accessibilityLabeledPair(role:id:in:)` — path base: `/documentation/swiftui/view/`
- Values: `accessibilityValue(_:)`, `accessibilityValue(_:isEnabled:)`
- Hints: `accessibilityHint(_:)`, `accessibilityHint(_:isEnabled:)`
- Actions: `accessibilityAction(...)` (multiple overloads for closures, intents, named), `accessibilityAdjustableAction(_:)`, `accessibilityScrollAction(_:)`
- Gestures: `accessibilityActivationPoint`, `accessibilityDragPoint`, `accessibilityDropPoint`, `accessibilityDirectTouch`, `accessibilityZoomAction`
- Elements: `accessibilityElement(children:)`, `accessibilityChildren(children:)`, `accessibilityHidden(_:)`
- Custom controls: `accessibilityRepresentation(representation:)`, `accessibilityRespondsToUserInteraction(_:)`
- Custom content: `accessibilityCustomContent(_:_:importance:)`
- Rotors: `accessibilityRotor(...)` (entries, textRanges), `accessibilityRotorEntry(id:in:)`, `accessibilityLinkedGroup(id:in:)`, `accessibilitySortPriority(_:)`
- Focus: `accessibilityFocused(_:)`, `accessibilityFocused(_:equals:)`
- Traits: `accessibilityAddTraits(_:)`, `accessibilityRemoveTraits(_:)`
- Identity: `accessibilityIdentifier(_:)`
- Color: `accessibilityIgnoresInvertColors(_:)`
- Content descriptions: `accessibilityTextContentType(_:)`, `accessibilityHeading(_:)`
- VoiceOver: `speechAdjustedPitch(_:)`, `speechAlwaysIncludesPunctuation(_:)`, `speechAnnouncementsQueued(_:)`, `speechSpellsOutCharacters(_:)`
- Charts: `accessibilityChartDescriptor(_:)`
- Large content: `accessibilityShowsLargeContentViewer()`, `accessibilityShowsLargeContentViewer(_:)`
- Quick actions: `accessibilityQuickAction(style:content:)`, `accessibilityQuickAction(style:isActive:content:)`

### Appearance Modifiers

- [Appearance modifiers](/documentation/swiftui/view-appearance) (article)
- Colors: `backgroundStyle(_:)`, `foregroundStyle(_:)` (1-3 style overloads), `allowedDynamicRange(_:)` — path base: `/documentation/swiftui/view/`
- Tint: `tint(_:)`, `listRowSeparatorTint(_:edges:)`, `listSectionSeparatorTint(_:edges:)`, `listItemTint(_:)`
- Color scheme: `preferredColorScheme(_:)`, `preferredSurroundingsEffect(_:)`
- Foreground: `border(_:width:)`, `overlay(alignment:content:)`, `overlay(_:ignoresSafeAreaEdges:)`, `overlay(_:in:fillStyle:)`
- Background: `background(alignment:content:)`, `background(_:ignoresSafeAreaEdges:)`, `background(ignoresSafeAreaEdges:)`, `background(_:in:fillStyle:)`, `background(in:fillStyle:)`, `alternatingRowBackgrounds(_:)`, `listRowBackground(_:)`, `scrollContentBackground(_:)`, `containerBackground(_:for:)`, `containerBackground(for:alignment:content:)`, `glassBackgroundEffect(displayMode:)`, `glassBackgroundEffect(in:displayMode:)`
- Control config: `defaultWheelPickerItemHeight(_:)`, `horizontalRadioGroupLayout()`, `controlSize(_:)`, `buttonBorderShape(_:)`, `buttonRepeatBehavior(_:)`, `headerProminence(_:)`, `scrollDisabled(_:)`, `scrollBounceBehavior(_:axes:)`, `scrollIndicatorsFlash(onAppear:)`, `scrollIndicatorsFlash(trigger:)`, `menuOrder(_:)`, `menuActionDismissBehavior(_:)`, `paletteSelectionEffect(_:)`, `typeSelectEquivalent(_:)`
- Symbol effects: `symbolEffect(_:options:isActive:)`, `symbolEffect(_:options:value:)`, `symbolEffectsRemoved(_:)`
- Privacy/redaction: `privacySensitive(_:)`, `redacted(reason:)`, `unredacted()`, `invalidatableContent(_:)`
- Visibility: `hidden()`, `labelsHidden()`, `menuIndicator(_:)`, `listRowSeparator(_:edges:)`, `listSectionSeparator(_:edges:)`, `persistentSystemOverlays(_:)`, `scrollIndicators(_:axes:)`, `scrollClipDisabled(_:)`, `tableColumnHeaders(_:)`, `upperLimbVisibility(_:)`, `volumeBaseplateVisibility(_:)`
- Sensory feedback: `sensoryFeedback(_:trigger:)`, `sensoryFeedback(trigger:_:)`, `sensoryFeedback(_:trigger:condition:)`
- Widget config: `widgetAccentable(_:)`, `widgetCurvesContent(_:)`, `widgetLabel(_:)`, `widgetLabel(label:)`, `dynamicIsland(verticalPlacement:)`, `accessoryWidgetGroupStyle(_:)`
- Window behaviors: `windowDismissBehavior(_:)`, `windowFullScreenBehavior(_:)`, `windowMinimizeBehavior(_:)`, `windowResizeBehavior(_:)`

### Text and Symbol Modifiers

- [Text and symbol modifiers](/documentation/swiftui/view-text-and-symbols) (article)
- Font: `font(_:)` `/documentation/swiftui/view/font(_:)`
- Dynamic type: `dynamicTypeSize(_:)`
- Text style: `bold(_:)`, `fontDesign(_:)`, `fontWeight(_:)`, `fontWidth(_:)`, `italic(_:)`, `monospaced(_:)`, `monospacedDigit()`, `strikethrough(_:pattern:color:)`, `textCase(_:)`, `textScale(_:isEnabled:)`, `underline(_:pattern:color:)`
- Text layout: `allowsTightening(_:)`, `baselineOffset(_:)`, `flipsForRightToLeftLayoutDirection(_:)`, `kerning(_:)`, `minimumScaleFactor(_:)`, `tracking(_:)`, `truncationMode(_:)`, `typesettingLanguage(_:isEnabled:)`
- Multiline: `lineLimit(_:)`, `lineLimit(_:reservesSpace:)`, `lineSpacing(_:)`, `multilineTextAlignment(_:)`, `multilineTextAlignment(strategy:)`
- Text selection: `textSelection(_:)`
- Text entry: `autocorrectionDisabled(_:)`, `keyboardType(_:)`, `scrollDismissesKeyboard(_:)`, `textInputAutocapitalization(_:)`, `textInputCompletion(_:)`, `textInputSuggestions(...)`, `textContentType(_:)` (WK/NS/UI variants)
- Find/replace: `findNavigator(isPresented:)`, `findDisabled(_:)`, `replaceDisabled(_:)`
- Symbol appearance: `symbolRenderingMode(_:)`, `symbolVariant(_:)`

### Style Modifiers

- [Style modifiers](/documentation/swiftui/view-style-modifiers) (article)
- [Auxiliary view modifiers](/documentation/swiftui/view-auxiliary-views) (article)
- Controls: `buttonStyle(_:)`, `datePickerStyle(_:)`, `menuStyle(_:)`, `pickerStyle(_:)`, `toggleStyle(_:)`
- Indicators: `gaugeStyle(_:)`, `progressViewStyle(_:)`
- Text: `labelStyle(_:)`, `textFieldStyle(_:)`, `textEditorStyle(_:)`
- Collections: `listStyle(_:)`, `tableStyle(_:)`, `disclosureGroupStyle(_:)`
- Presentation: `navigationSplitViewStyle(_:)`, `tabViewStyle(_:)`, `presentedWindowStyle(_:)`, `presentedWindowToolbarStyle(_:)`
- Groups: `controlGroupStyle(_:)`, `groupBoxStyle(_:)`, `indexViewStyle(_:)`

### Navigation and Toolbars

- [Configure your apps navigation titles](/documentation/swiftui/configure-your-apps-navigation-titles) (article)
- Navigation titles: `navigationTitle(_:)`, `navigationSubtitle(_:)`, `navigationDocument(_:)`, `navigationDocument(_:preview:)`
- Navigation bars: `navigationBarBackButtonHidden(_:)`, `navigationBarTitleDisplayMode(_:)`
- Navigation destinations: `navigationDestination(for:destination:)`, `navigationDestination(isPresented:destination:)`, `navigationDestination(item:destination:)`, `navigationSplitViewColumnWidth(_:)`, `navigationSplitViewColumnWidth(min:ideal:max:)`
- Tab views: `tabViewCustomization(_:)`, `defaultAdaptableTabBarPlacement(_:)`, `tabViewSidebarHeader(content:)`, `tabViewSidebarFooter(content:)`, `tabViewSidebarBottomBar(content:)`, `sectionActions(content:)`
- Toolbars: `toolbar(content:)`, `toolbar(id:content:)`, `toolbar(_:for:)`, `toolbar(removing:)`, `toolbarVisibility(_:for:)`, `toolbarBackground(_:for:)`, `toolbarBackgroundVisibility(_:for:)`, `toolbarForegroundStyle(_:for:)`, `toolbarColorScheme(_:for:)`, `toolbarRole(_:)`, `toolbarTitleMenu(content:)`, `toolbarTitleDisplayMode(_:)`, `ornament(visibility:attachmentAnchor:contentAlignment:ornament:)`
- Context menus: `contextMenu(menuItems:)`, `contextMenu(menuItems:preview:)`, `contextMenu(forSelectionType:menu:primaryAction:)`
- Badges: `badge(_:)`, `badgeProminence(_:)`
- Help: `help(_:)`
- Status bar: `statusBarHidden(_:)`
- Touch Bar: `touchBar(content:)`, `touchBar(_:)`, `touchBarItemPrincipal(_:)`, `touchBarCustomizationLabel(_:)`, `touchBarItemPresence(_:)`

### Chart View Modifiers

- [Chart view modifiers](/documentation/swiftui/view-chart-view) (article)
- Styles: `chartBackground(alignment:content:)`, `chartForegroundStyleScale(...)` (7 overloads), `chartPlotStyle(content:)`
- Legends: `chartLegend(_:)`, `chartLegend(position:alignment:spacing:)`, `chartLegend(position:alignment:spacing:content:)`
- Overlays: `chartOverlay(alignment:content:)`
- Axes: `chartXAxis(_:)`, `chartXAxis(content:)`, `chartXAxisStyle(content:)`, `chartYAxis(_:)`, `chartYAxis(content:)`, `chartYAxisStyle(content:)`
- Axis labels: `chartXAxisLabel(_:position:alignment:spacing:)`, `chartXAxisLabel(position:alignment:spacing:content:)`, `chartYAxisLabel(_:position:alignment:spacing:)`, `chartYAxisLabel(position:alignment:spacing:content:)`
- Axis scales: `chartXScale(...)`, `chartYScale(...)` — overloads for domain, range, type at `/documentation/swiftui/view/chartxscale(...)` and `chartyscale(...)`
- Symbol scales: `chartSymbolScale(...)` — overloads for domain, range, mapping at `/documentation/swiftui/view/chartsymbolscale(...)`
- Symbol size scales: `chartSymbolSizeScale(...)` — overloads for domain, range, mapping, type at `/documentation/swiftui/view/chartsymbolsizescale(...)`
- Line style scales: `chartLineStyleScale(...)` — overloads for domain, range, mapping at `/documentation/swiftui/view/chartlinestylescale(...)`
- Scrolling: `chartScrollPosition(initialX:)`, `chartScrollPosition(initialY:)`, `chartScrollPosition(x:)`, `chartScrollPosition(y:)`, `chartScrollTargetBehavior(_:)`, `chartScrollableAxes(_:)`
- Selection: `chartXSelection(range:)`, `chartXSelection(value:)`, `chartYSelection(range:)`, `chartYSelection(value:)`, `chartAngleSelection(value:)`
- Visible domain: `chartXVisibleDomain(length:)`, `chartYVisibleDomain(length:)`
- Interaction: `chartGesture(_:)`

### Layout Modifiers

- [Layout modifiers](/documentation/swiftui/view-layout) (article)
- Size: `frame(width:height:alignment:)`, `frame(depth:alignment:)`, `frame(minWidth:idealWidth:maxWidth:minHeight:idealHeight:maxHeight:alignment:)`, `frame(minDepth:idealDepth:maxDepth:alignment:)`, `containerRelativeFrame(...)` (3 overloads), `fixedSize()`, `fixedSize(horizontal:vertical:)`, `layoutPriority(_:)`
- Position: `position(_:)`, `position(x:y:)`, `offset(_:)`, `offset(x:y:)`, `offset(z:)`, `coordinateSpace(_:)`
- Alignment: `alignmentGuide(_:computeValue:)`
- Padding/spacing: `padding(_:)`, `padding(_:_:)`, `padding3D(_:)`, `padding3D(_:_:)`, `listRowInsets(_:)`, `scenePadding(_:)`, `scenePadding(_:edges:)`, `listRowSpacing(_:)`, `listSectionSpacing(_:)`
- Grid config: `gridCellColumns(_:)`, `gridCellAnchor(_:)`, `gridCellUnsizedAxes(_:)`, `gridColumnAlignment(_:)`
- Safe area/margins: `ignoresSafeArea(_:edges:)`, `safeAreaInset(edge:alignment:spacing:content:)`, `safeAreaPadding(_:)`, `safeAreaPadding(_:_:)`, `contentMargins(_:for:)`, `contentMargins(_:_:for:)`
- Layer order: `zIndex(_:)`
- Layout direction: `layoutDirectionBehavior(_:)`
- Custom layout: `layoutValue(key:value:)`

### Graphics and Rendering Modifiers

- [Graphics and rendering modifiers](/documentation/swiftui/view-graphics-and-rendering) (article)
- Masks/clipping: `mask(alignment:_:)`, `clipped(antialiased:)`, `clipShape(_:style:)`, `containerShape(_:)`
- Scale: `scaledToFill()`, `scaledToFit()`, `scaleEffect(_:anchor:)`, `scaleEffect(x:y:anchor:)`, `scaleEffect(x:y:z:anchor:)`, `imageScale(_:)`, `aspectRatio(_:contentMode:)`
- Rotation/transform: `rotationEffect(_:anchor:)`, `rotation3DEffect(...)` (multiple overloads), `perspectiveRotationEffect(...)`, `projectionEffect(_:)`, `transformEffect(_:)`, `transform3DEffect(_:)`
- Graphical effects: `blur(radius:opaque:)`, `opacity(_:)`, `brightness(_:)`, `contrast(_:)`, `colorInvert()`, `colorMultiply(_:)`, `saturation(_:)`, `grayscale(_:)`, `hueRotation(_:)`, `luminanceToAlpha()`, `shadow(color:radius:x:y:)`, `visualEffect(_:)`, `visualEffect3D(_:)`
- Shaders: `colorEffect(_:isEnabled:)`, `distortionEffect(_:maxSampleOffset:isEnabled:)`, `layerEffect(_:maxSampleOffset:isEnabled:)`
- Composites: `blendMode(_:)`, `compositingGroup()`, `drawingGroup(opaque:colorMode:)`

### Animation Modifiers

- `func animation(_:)` `/documentation/swiftui/view/animation(_:)` [deprecated]
- `func animation(_:value:)` `/documentation/swiftui/view/animation(_:value:)` — animate when value changes
- `func animation(_:body:)` `/documentation/swiftui/view/animation(_:body:)` — scope animation to body content
- `func keyframeAnimator(initialValue:repeating:content:keyframes:)` `/documentation/swiftui/view/keyframeanimator(initialvalue:repeating:content:keyframes:)` — looping keyframe animation
- `func keyframeAnimator(initialValue:trigger:content:keyframes:)` `/documentation/swiftui/view/keyframeanimator(initialvalue:trigger:content:keyframes:)` — triggered keyframe animation
- `func phaseAnimator(_:content:animation:)` `/documentation/swiftui/view/phaseanimator(_:content:animation:)` — multi-phase animation
- `func phaseAnimator(_:trigger:content:animation:)` `/documentation/swiftui/view/phaseanimator(_:trigger:content:animation:)` — triggered phase animation
- `func contentTransition(_:)` `/documentation/swiftui/view/contenttransition(_:)` — transition for content changes
- `func transition(_:)` `/documentation/swiftui/view/transition(_:)` — insertion/removal transition
- `func transaction(_:)` `/documentation/swiftui/view/transaction(_:)` — modify transaction
- `func transaction(value:_:)` `/documentation/swiftui/view/transaction(value:_:)` — transaction on value change
- `func transaction(_:body:)` `/documentation/swiftui/view/transaction(_:body:)` — scoped transaction
- `func matchedGeometryEffect(id:in:properties:anchor:isSource:)` `/documentation/swiftui/view/matchedgeometryeffect(id:in:properties:anchor:issource:)` — sync geometry across views
- `func geometryGroup()` `/documentation/swiftui/view/geometrygroup()` — resolve geometry before children

### Input and Event Modifiers

- [Input and event modifiers](/documentation/swiftui/view-input-and-events) (article)
- Interactivity: `disabled(_:)`, `interactionActivityTrackingTag(_:)`
- List controls: `swipeActions(edge:allowsFullSwipe:content:)`, `refreshable(action:)`, `selectionDisabled(_:)`
- Scroll controls: `scrollPosition(_:anchor:)`, `scrollPosition(id:anchor:)`, `defaultScrollAnchor(_:)`, `defaultScrollAnchor(_:for:)`, `scrollTargetBehavior(_:)`, `scrollTargetLayout(isEnabled:)`, `scrollTransition(...)` (2 overloads), `onScrollGeometryChange(for:of:action:)`, `onScrollTargetVisibilityChange(idType:threshold:_:)`, `onScrollVisibilityChange(threshold:_:)`, `onScrollPhaseChange(_:)`
- Geometry: `onGeometryChange(for:of:action:)`
- Taps/gestures: `onTapGesture(count:perform:)`, `onTapGesture(count:coordinateSpace:perform:)`, `onLongPressGesture(...)`, `onLongTouchGesture(...)`, `gesture(_:)` (multiple overloads), `highPriorityGesture(...)`, `simultaneousGesture(...)`, `defersSystemGestures(on:)`, `onPencilDoubleTap(perform:)`, `onPencilSqueeze(perform:)`, `allowsWindowActivationEvents(_:)`
- Keyboard input: `onKeyPress(...)` (5 overloads), `onModifierKeysChanged(mask:initial:_:)`
- Keyboard shortcuts: `keyboardShortcut(_:)`, `keyboardShortcut(_:modifiers:)`, `keyboardShortcut(_:modifiers:localization:)`, `modifierKeyAlternate(_:_:)`
- Hover: `onHover(perform:)`, `onContinuousHover(coordinateSpace:perform:)`, `hoverEffect(...)` (4 overloads), `hoverEffectGroup(...)` (3 overloads), `hoverEffectDisabled(_:)`, `defaultHoverEffect(_:)`, `listRowHoverEffect(_:)`, `listRowHoverEffectDisabled(_:)`
- Pointer: `pointerVisibility(_:)`, `pointerStyle(_:)`
- Focus: `focused(_:)`, `focused(_:equals:)`, `focusedValue(...)`, `focusedSceneValue(...)`, `focusedObject(_:)`, `focusedSceneObject(_:)`, `prefersDefaultFocus(_:in:)`, `focusScope(_:)`, `focusSection()`, `focusable(_:)`, `focusable(_:interactions:)`, `focusEffectDisabled(_:)`, `defaultFocus(_:_:priority:)`, `searchFocused(_:)`, `searchFocused(_:equals:)`
- Copy/paste: `copyable(_:)`, `cuttable(for:action:)`, `pasteDestination(for:action:validator:)`, `onCopyCommand(perform:)`, `onCutCommand(perform:)`, `onPasteCommand(of:perform:)`, `onPasteCommand(of:validator:perform:)`
- Drag/drop: `onDrag(_:preview:)`, `onDrag(_:)`, `itemProvider(_:)`, `onDrop(of:isTargeted:perform:)`, `onDrop(of:delegate:)`, `dropDestination(for:action:isTargeted:)`, `draggable(_:)`, `draggable(_:preview:)`, `springLoadingBehavior(_:)`
- Submission: `onAssignedDocumentDidSubmit(_:)`, `onAssignedDocumentDidWithdraw(_:)`, `onAssignedDocumentWillSubmit(_:)`, `onAssignedDocumentWillWithdraw(_:)`, `onSubmit(of:_:)`, `submitScope(_:)`, `submitLabel(_:)`
- Movement: `onMoveCommand(perform:)`, `moveDisabled(_:)`
- Deletion: `onDeleteCommand(perform:)`, `deleteDisabled(_:)`
- Commands: `pageCommand(value:in:step:)`, `onExitCommand(perform:)`, `onPlayPauseCommand(perform:)`, `onCommand(_:perform:)`
- Digital crown: `digitalCrownAccessory(_:)`, `digitalCrownAccessory(content:)`, `digitalCrownRotation(...)` (5 overloads)
- Immersive spaces: `onImmersionChange(initial:_:)`
- Volumes: `onVolumeViewpointChange(updateStrategy:initial:_:)`, `supportedVolumeViewpoints(_:)`
- User activities: `userActivity(_:element:_:)`, `userActivity(_:isActive:_:)`, `onContinueUserActivity(_:perform:)`, `handlesExternalEvents(preferring:allowing:)`
- View lifecycle: `onAppear(perform:)`, `onDisappear(perform:)`, `onChange(of:initial:_:)`
- File renaming: `renameAction(_:)`
- URLs: `onOpenURL(perform:)`, `widgetURL(_:)`
- Publisher events: `onReceive(_:perform:)`
- Hit testing: `allowsHitTesting(_:)`
- Content shape: `contentShape(_:eoFill:)`, `contentShape(_:_:eoFill:)`
- Import/export: `exportsItemProviders(_:onExport:)`, `exportsItemProviders(_:onExport:onEdit:)`, `importsItemProviders(_:onImport:)`, `exportableToServices(_:)`, `exportableToServices(_:onEdit:)`, `importableFromServices(for:action:)`
- App intents: `shortcutsLinkStyle(_:)`, `siriTipViewStyle(_:)`
- Camera: `onCameraCaptureEvent(isEnabled:action:)`, `onCameraCaptureEvent(isEnabled:primaryAction:secondaryAction:)`, `cameraAnchor(isActive:)`

### Search Modifiers

- [Search modifiers](/documentation/swiftui/view-search) (article)
- Display: `searchable(text:placement:prompt:)`, `searchable(text:isPresented:placement:prompt:)`, `searchPresentationToolbarBehavior(_:)`
- Tokens: `searchable(text:tokens:placement:prompt:token:)`, `searchable(text:tokens:isPresented:placement:prompt:token:)`
- Editable tokens: `searchable(text:editableTokens:isPresented:placement:prompt:token:)`, `searchable(text:editableTokens:placement:prompt:token:)`
- Suggestions: `searchSuggestions(_:)`, `searchSuggestions(_:for:)`, `searchCompletion(_:)`, `searchable(text:tokens:suggestedTokens:placement:prompt:token:)`, `searchable(text:tokens:suggestedTokens:isPresented:placement:prompt:token:)`
- Scopes: `searchScopes(_:scopes:)`, `searchScopes(_:activation:_:)`
- Dictation: `searchDictationBehavior(_:)`

### Presentation Modifiers

- [Presentation modifiers](/documentation/swiftui/view-presentation) (article)
- Alerts: see full docs at `/documentation/swiftui/view-presentation`
