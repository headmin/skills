# Event Handling — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Gestures](#gestures)
- [Keyboard input](#responding-to-keyboard-input)
- [Keyboard shortcuts](#creating-keyboard-shortcuts)
- [Modifier keys](#responding-to-modifier-keys)
- [Hover events](#responding-to-hover-events)
- [Pointer appearance](#modifying-pointer-appearance)
- [Hover effects](#changing-view-appearance-for-hover-events)
- [Submission events](#responding-to-submission-events)
- [Commands](#responding-to-commands)
- [Hit testing](#controlling-hit-testing)
- [Digital Crown](#interacting-with-the-digital-crown)
- [Touch Bar](#managing-touch-bar-input)
- [Capture events](#responding-to-capture-events)
- [Clipboard / copy-paste](#copying-transferable-items)
- [Drag and drop](#drag-and-drop)
- [Focus](#focus)
- [System events](#system-events)
- [Import / export](#importing-and-exporting-transferable-items)

---

## Gestures

- [Gestures](/documentation/swiftui/gestures) — topic group
- [Adding interactivity with gestures](/documentation/swiftui/adding-interactivity-with-gestures) (article)
- [Composing SwiftUI gestures](/documentation/swiftui/composing-swiftui-gestures) (article)

### Recognizing tap gestures

- [func onTapGesture(count:perform:)](/documentation/swiftui/view/ontapgesture(count:perform:)) — detect taps on a view
- [func onTapGesture(count:coordinateSpace:perform:)](/documentation/swiftui/view/ontapgesture(count:coordinatespace:perform:)) — tap with location info
- [TapGesture](/documentation/swiftui/tapgesture) — discrete tap gesture
- [SpatialTapGesture](/documentation/swiftui/spatialtapgesture) — tap with location/location3D

### Recognizing long press gestures

- [func onLongPressGesture(minimumDuration:maximumDistance:perform:onPressingChanged:)](/documentation/swiftui/view/onlongpressgesture(minimumduration:maximumdistance:perform:onpressingchanged:)) — also (minimumDuration:perform:onPressingChanged:) variant
- [func onLongTouchGesture(minimumDuration:perform:onTouchingChanged:)](/documentation/swiftui/view/onlongtouchgesture(minimumduration:perform:ontouchingchanged:)) — touch-only long press
- [LongPressGesture](/documentation/swiftui/longpressgesture) — configurable long-press gesture

### Recognizing spatial events

- [SpatialEventGesture](/documentation/swiftui/spatialeventgesture) — visionOS spatial input gesture
- [SpatialEventCollection](/documentation/swiftui/spatialeventcollection) — collection of spatial events; Event has phase, kind (directPinch/indirectPinch/pointer/touch/pencil), location/location3D
- [Chirality](/documentation/swiftui/chirality) — left/right hand enum

### Recognizing gestures that change over time

- [func gesture(_:)](/documentation/swiftui/view/gesture(_:)) — attach gesture; overloads: (isEnabled:), (name:isEnabled:), (including: GestureMask)
- [DragGesture](/documentation/swiftui/draggesture) — drag gesture; Value: startLocation, location, translation, velocity, 3D variants
- [WindowDragGesture](/documentation/swiftui/windowdraggesture) — drag to move a window (macOS/visionOS)
- [MagnifyGesture](/documentation/swiftui/magnifygesture) — pinch-to-zoom gesture
- [RotateGesture](/documentation/swiftui/rotategesture) — two-finger rotation
- [RotateGesture3D](/documentation/swiftui/rotategesture3d) — 3D rotation with axis constraint
- [GestureMask](/documentation/swiftui/gesturemask) — .all, .gesture, .subviews, .none

### Recognizing Apple Pencil gestures

- [func onPencilDoubleTap(perform:)](/documentation/swiftui/view/onpencildoubletap(perform:)) — respond to pencil double tap
- [func onPencilSqueeze(perform:)](/documentation/swiftui/view/onpencilsqueeze(perform:)) — respond to pencil squeeze
- [var preferredPencilDoubleTapAction](/documentation/swiftui/environmentvalues/preferredpencildoubletapaction) — environment: preferred double-tap action
- [var preferredPencilSqueezeAction](/documentation/swiftui/environmentvalues/preferredpencilsqueezeaction) — environment: preferred squeeze action
- [PencilPreferredAction](/documentation/swiftui/pencilpreferredaction) — ignore, showColorPalette, switchEraser, switchPrevious, etc.
- [PencilDoubleTapGestureValue](/documentation/swiftui/pencildoubletapgesturevalue) — value with hoverPose
- [PencilSqueezeGestureValue](/documentation/swiftui/pencilsqueezegesturevalue) — value with hoverPose
- [PencilSqueezeGesturePhase](/documentation/swiftui/pencilsqueezegesturephase) — active/ended/failed
- [PencilHoverPose](/documentation/swiftui/pencilhoverpose) — anchor, location, zDistance, altitude, azimuth, roll

### Combining gestures

- [func simultaneousGesture(_:including:)](/documentation/swiftui/view/simultaneousgesture(_:including:)) — overloads: (isEnabled:), (name:isEnabled:)
- [SequenceGesture](/documentation/swiftui/sequencegesture) — run gestures in sequence; Value: .first/.second
- [SimultaneousGesture](/documentation/swiftui/simultaneousgesture) — run at same time; Value: first?/second?
- [ExclusiveGesture](/documentation/swiftui/exclusivegesture) — only one wins; Value: .first/.second

### Defining custom gestures

- [func highPriorityGesture(_:including:)](/documentation/swiftui/view/highprioritygesture(_:including:)) — priority over children; overloads: (isEnabled:), (name:isEnabled:)
- [func handGestureShortcut(_:isEnabled:)](/documentation/swiftui/view/handgestureshortcut(_:isenabled:)) — visionOS hand gesture shortcut
- [func defersSystemGestures(on:)](/documentation/swiftui/view/deferssystemgestures(on:)) — defer system gestures on edges
- [Gesture](/documentation/swiftui/gesture) — protocol; methods: updating, onChanged, onEnded, simultaneously, sequenced, exclusively, modifiers, map, handActivationBehavior, targetedToEntity
- [AnyGesture](/documentation/swiftui/anygesture) — type-erased gesture
- [HandActivationBehavior](/documentation/swiftui/handactivationbehavior) — .automatic, .pinch (visionOS)
- [HandGestureShortcut](/documentation/swiftui/handgestureshortcut) — .primaryAction

### Managing gesture state

- [GestureState](/documentation/swiftui/gesturestate) — property wrapper for transient gesture state; resets when gesture ends
- [GestureStateGesture](/documentation/swiftui/gesturestategesture) — gesture that updates a GestureState

### Handling activation events

- [func allowsWindowActivationEvents(_:)](/documentation/swiftui/view/allowswindowactivationevents(_:)) — allow window activation on interaction

### Deprecated gestures

- [MagnificationGesture](/documentation/swiftui/magnificationgesture) [deprecated] — use MagnifyGesture instead
- [RotationGesture](/documentation/swiftui/rotationgesture) [deprecated] — use RotateGesture instead

---

## Input events

- [Input events](/documentation/swiftui/input-events) — topic group

### Responding to keyboard input

- [func onKeyPress(_:action:)](/documentation/swiftui/view/onkeypress(_:action:)) — respond to key; overloads: (phases:action:), (_:phases:action:), (characters:phases:action:), (keys:phases:action:)
- [KeyPress](/documentation/swiftui/keypress) — key, characters, modifiers, phase; Phases: .down/.up/.repeat/.all; Result: .handled/.ignored

### Creating keyboard shortcuts

- [func keyboardShortcut(_:)](/documentation/swiftui/view/keyboardshortcut(_:)) — assign shortcut; overloads: (_:modifiers:), (_:modifiers:localization:)
- [var keyboardShortcut](/documentation/swiftui/environmentvalues/keyboardshortcut) — environment: current shortcut
- [KeyboardShortcut](/documentation/swiftui/keyboardshortcut) — .cancelAction, .defaultAction; Localization: .automatic/.custom/.withoutMirroring
- [KeyEquivalent](/documentation/swiftui/keyequivalent) — arrow keys, special keys (delete, escape, return, tab, space, etc.)
- [EventModifiers](/documentation/swiftui/eventmodifiers) — .command, .control, .option, .shift, .capsLock, .numericPad, .all; .function [deprecated]

### Responding to modifier keys

- [func onModifierKeysChanged(mask:initial:_:)](/documentation/swiftui/view/onmodifierkeyschanged(mask:initial:_:)) — track modifier key changes
- [func modifierKeyAlternate(_:_:)](/documentation/swiftui/view/modifierkeyalternate(_:_:)) — show alternate content when modifier held

### Responding to hover events

- [func onHover(perform:)](/documentation/swiftui/view/onhover(perform:)) — Bool on hover enter/exit
- [func onContinuousHover(coordinateSpace:perform:)](/documentation/swiftui/view/oncontinuoushover(coordinatespace:perform:)) — continuous tracking
- [func hoverEffect(_:isEnabled:)](/documentation/swiftui/view/hovereffect(_:isenabled:)) — apply hover effect
- [func hoverEffectDisabled(_:)](/documentation/swiftui/view/hovereffectdisabled(_:)) — disable hover effects
- [func defaultHoverEffect(_:)](/documentation/swiftui/view/defaulthovereffect(_:)) — set default effect
- [var isHoverEffectEnabled](/documentation/swiftui/environmentvalues/ishovereffectenabled) — environment value
- [HoverPhase](/documentation/swiftui/hoverphase) — .active(CGPoint), .ended
- [HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride) — programmatic override: active/inactive/toggled (+ temporarily variants)
- [OrnamentHoverContentEffect](/documentation/swiftui/ornamenthovercontenteffect) | [OrnamentHoverEffect](/documentation/swiftui/ornamenthovereffect) — visionOS ornament hover effects

### Modifying pointer appearance

- [func pointerStyle(_:)](/documentation/swiftui/view/pointerstyle(_:)) — set cursor style
- [func pointerVisibility(_:)](/documentation/swiftui/view/pointervisibility(_:)) — control pointer visibility
- [PointerStyle](/documentation/swiftui/pointerstyle) — .default, .horizontalText, .verticalText, .rectSelection, .grabIdle, .grabActive, .link, .zoomIn, .zoomOut, frameResize, columnResize, rowResize, image, shape
- [HorizontalDirection](/documentation/swiftui/horizontaldirection) — .leading/.trailing with Set
- [VerticalDirection](/documentation/swiftui/verticaldirection) — .up/.down with Set
- [FrameResizePosition](/documentation/swiftui/frameresizeposition) — edge/corner positions for resize cursor
- [FrameResizeDirection](/documentation/swiftui/frameresizedirection) — .inward/.outward with Set

### Changing view appearance for hover events

- [func hoverEffect(_:)](/documentation/swiftui/view/hovereffect(_:)) — apply HoverEffect (.automatic/.highlight/.lift)
- [HoverEffect](/documentation/swiftui/hovereffect) — .automatic, .highlight, .lift
- [func hoverEffect(_:in:isEnabled:)](/documentation/swiftui/view/hovereffect(_:in:isenabled:)) — custom effect in group
- [func hoverEffect(in:isEnabled:body:)](/documentation/swiftui/view/hovereffect(in:isenabled:body:)) — inline effect with geometry
- [CustomHoverEffect](/documentation/swiftui/customhovereffect) — protocol; built-ins: .automatic, .empty, .highlight, .lift
- [AutomaticHoverEffect](/documentation/swiftui/automatichovereffect) | [EmptyHoverEffect](/documentation/swiftui/emptyhovereffect) | [HighlightHoverEffect](/documentation/swiftui/highlighthovereffect) | [LiftHoverEffect](/documentation/swiftui/lifthovereffect) — concrete hover effect types
- [ContentHoverEffect](/documentation/swiftui/contenthovereffect) — content-based hover effect
- [HoverEffectGroup](/documentation/swiftui/hovereffectgroup) — group effects; Behavior: activatesGroup/followsGroup/ignoresGroup/preservesGroup
- [func hoverEffectGroup()](/documentation/swiftui/view/hovereffectgroup()) — also (_:) and (id:in:behavior:) overloads
- [GroupHoverEffect](/documentation/swiftui/grouphovereffect) — group effect type
- [HoverEffectContent](/documentation/swiftui/hovereffectcontent) — protocol for effect content (animation, clipShape, offset, opacity, rotation, scale, transform)
- [EmptyHoverEffectContent](/documentation/swiftui/emptyhovereffectcontent) — empty effect content
- [func handPointerBehavior(_:)](/documentation/swiftui/view/handpointerbehavior(_:)) — visionOS hand pointer
- [HandPointerBehavior](/documentation/swiftui/handpointerbehavior) — .drawing, .inactive

### Responding to submission events

- [func onSubmit(of:_:)](/documentation/swiftui/view/onsubmit(of:_:)) — handle text/search submit
- [func submitScope(_:)](/documentation/swiftui/view/submitscope(_:)) — prevent submit propagation
- [SubmitTriggers](/documentation/swiftui/submittriggers) — .search, .text

### Labeling a submission event

- [func submitLabel(_:)](/documentation/swiftui/view/submitlabel(_:)) — set return key label
- [SubmitLabel](/documentation/swiftui/submitlabel) — .continue, .done, .go, .join, .next, .return, .route, .search, .send

### Responding to commands

- [func onMoveCommand(perform:)](/documentation/swiftui/view/onmovecommand(perform:)) — arrow/remote move
- [func onDeleteCommand(perform:)](/documentation/swiftui/view/ondeletecommand(perform:)) | [onExitCommand(perform:)](/documentation/swiftui/view/onexitcommand(perform:)) | [onPlayPauseCommand(perform:)](/documentation/swiftui/view/onplaypausecommand(perform:))
- [func pageCommand(value:in:step:)](/documentation/swiftui/view/pagecommand(value:in:step:)) — page up/down
- [func onCommand(_:perform:)](/documentation/swiftui/view/oncommand(_:perform:)) — Selector-based command
- [MoveCommandDirection](/documentation/swiftui/movecommanddirection) — .up, .down, .left, .right

### Controlling hit testing

- [func allowsTightening(_:)](/documentation/swiftui/view/allowstightening(_:)) — allow tighter character spacing
- [func contentShape(_:eoFill:)](/documentation/swiftui/view/contentshape(_:eofill:)) — define hit-test shape
- [func contentShape(_:_:eoFill:)](/documentation/swiftui/view/contentshape(_:_:eofill:)) — shape for specific kind
- [ContentShapeKinds](/documentation/swiftui/contentshapekinds) — .interaction, .dragPreview, .contextMenuPreview, .focusEffect, .hoverEffect, .accessibility

### Interacting with the Digital Crown

- [func digitalCrownAccessory(_:)](/documentation/swiftui/view/digitalcrownaccessory(_:)) — visibility; also (content:) for custom view
- [func digitalCrownRotation(_:)](/documentation/swiftui/view/digitalcrownrotation(_:)) — bind crown; overloads with from/through/by/sensitivity/detent/onChange/onIdle
- [DigitalCrownEvent](/documentation/swiftui/digitalcrownevent) — offset and velocity
- [DigitalCrownRotationalSensitivity](/documentation/swiftui/digitalcrownrotationalsensitivity) — .low, .medium, .high

### Managing Touch Bar input

- [func touchBar(content:)](/documentation/swiftui/view/touchbar(content:)) — set Touch Bar content; also touchBar(_:)
- [func touchBarItemPrincipal(_:)](/documentation/swiftui/view/touchbaritemprincipal(_:)) | [touchBarCustomizationLabel(_:)](/documentation/swiftui/view/touchbarcustomizationlabel(_:)) | [touchBarItemPresence(_:)](/documentation/swiftui/view/touchbaritempresence(_:))
- [TouchBar](/documentation/swiftui/touchbar) — container; [TouchBarItemPresence](/documentation/swiftui/touchbaritempresence) — .default, .optional, .required

### Responding to capture events

- [func onCameraCaptureEvent(isEnabled:action:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:action:)) — respond to camera capture button
- [func onCameraCaptureEvent(isEnabled:primaryAction:secondaryAction:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:primaryaction:secondaryaction:)) — primary + secondary capture
- [Clipboard](/documentation/swiftui/clipboard) — clipboard access

### Copying transferable items

- [func copyable(_:)](/documentation/swiftui/view/copyable(_:)) — make Transferable items copyable
- [func cuttable(for:action:)](/documentation/swiftui/view/cuttable(for:action:)) — make items cuttable
- [func pasteDestination(for:action:validator:)](/documentation/swiftui/view/pastedestination(for:action:validator:)) — paste Transferable items

### Copying items using item providers

- [func onCopyCommand(perform:)](/documentation/swiftui/view/oncopycommand(perform:)) — copy via NSItemProvider
- [func onCutCommand(perform:)](/documentation/swiftui/view/oncutcommand(perform:)) — cut via NSItemProvider
- [func onPasteCommand(of:perform:)](/documentation/swiftui/view/onpastecommand(of:perform:)) — paste via NSItemProvider
- [func onPasteCommand(of:validator:perform:)](/documentation/swiftui/view/onpastecommand(of:validator:perform:)) — paste with validation

---

## Drag and drop

- [Drag and drop](/documentation/swiftui/drag-and-drop) — topic group
- [Adopting drag and drop using SwiftUI](/documentation/swiftui/adopting-drag-and-drop-using-swiftui) (article)
- [Making a view into a drag source](/documentation/swiftui/making-a-view-into-a-drag-source) (article)

### Configuring drag and drop behavior

- [DragConfiguration](/documentation/swiftui/dragconfiguration) — configure drag operations; OperationsOutsideApp and OperationsWithinApp control copy/move/delete
- [DropConfiguration](/documentation/swiftui/dropconfiguration) — configure drop behavior with operation and acceptedItemCount

### Moving items

- [DragSession](/documentation/swiftui/dragsession) — active drag state; id, location, phase (initial/active/ending/ended/dataTransferCompleted), draggedItemIndex
- [DropSession](/documentation/swiftui/dropsession) — active drop state; id, location, phase (entering/active/exiting/ended/dataTransferCompleted), itemsCount, suggestedOperations, localSession

### Moving transferable items

- [func draggable(_:)](/documentation/swiftui/view/draggable(_:)) — make Transferable item draggable
- [func draggable(_:preview:)](/documentation/swiftui/view/draggable(_:preview:)) — draggable with custom preview
- [func dropDestination(for:action:isTargeted:)](/documentation/swiftui/view/dropdestination(for:action:istargeted:)) — receive Transferable drops

### Moving items using item providers

- [func itemProvider(_:)](/documentation/swiftui/view/itemprovider(_:)) — provide NSItemProvider for drag
- [func onDrag(_:preview:)](/documentation/swiftui/view/ondrag(_:preview:)) — drag with preview via NSItemProvider
- [func onDrag(_:)](/documentation/swiftui/view/ondrag(_:)) — drag via NSItemProvider
- [func onDrop(of:isTargeted:perform:)](/documentation/swiftui/view/ondrop(of:istargeted:perform:)) — drop with NSItemProvider
- [func onDrop(of:delegate:)](/documentation/swiftui/view/ondrop(of:delegate:)) — drop with DropDelegate
- [DropDelegate](/documentation/swiftui/dropdelegate) — protocol for custom drop handling (dropEntered, dropExited, dropUpdated, validateDrop, performDrop)
- [DropProposal](/documentation/swiftui/dropproposal) — proposed drop operation
- [DropOperation](/documentation/swiftui/dropoperation) — .cancel, .copy, .move, .forbidden, .alias, .delete; also DropOperation.Set
- [DropInfo](/documentation/swiftui/dropinfo) — drop location + item type checking

### Describing preview formations

- [DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation) — .default, .list, .none, .pile, .stack

### Configuring spring loading

- [func springLoadingBehavior(_:)](/documentation/swiftui/view/springloadingbehavior(_:)) — configure spring loading
- [var springLoadingBehavior](/documentation/swiftui/environmentvalues/springloadingbehavior) — environment value
- [SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior) — .automatic, .enabled, .disabled

---

## Focus

- [Focus](/documentation/swiftui/focus) — topic group
- [Focus Cookbook: Supporting and enhancing focus-driven interactions](/documentation/swiftui/focus-cookbook-sample) (article)

### Indicating that a view can receive focus

- [func focusable(_:)](/documentation/swiftui/view/focusable(_:)) — make view focusable
- [func focusable(_:interactions:)](/documentation/swiftui/view/focusable(_:interactions:)) — focusable with interaction types
- [FocusInteractions](/documentation/swiftui/focusinteractions) — .automatic, .activate, .edit

### Managing focus state

- [func focused(_:equals:)](/documentation/swiftui/view/focused(_:equals:)) — bind focus to enum; also focused(_:) for Bool
- [var isFocused](/documentation/swiftui/environmentvalues/isfocused) — environment: view is focused
- [FocusState](/documentation/swiftui/focusstate) — property wrapper for focus tracking
- [FocusedValue](/documentation/swiftui/focusedvalue) — property wrapper reading focused view's value
- [macro Entry()](/documentation/swiftui/entry()) — declare focused value entry
- [FocusedValueKey](/documentation/swiftui/focusedvaluekey) — protocol for focused value keys
- [FocusedBinding](/documentation/swiftui/focusedbinding) — property wrapper for focused bindings
- [func searchFocused(_:)](/documentation/swiftui/view/searchfocused(_:)) — bind search focus; also (_:equals:) overload

### Exposing value types to focused views

- [func focusedValue(_:)](/documentation/swiftui/view/focusedvalue(_:)) — expose value; also (_:_:) keyed variant
- [func focusedSceneValue(_:)](/documentation/swiftui/view/focusedscenevalue(_:)) — scene-scoped; also (_:_:) keyed variant
- [FocusedValues](/documentation/swiftui/focusedvalues) — collection of focused values

### Exposing reference types to focused views

- [func focusedObject(_:)](/documentation/swiftui/view/focusedobject(_:)) — expose ObservableObject
- [func focusedSceneObject(_:)](/documentation/swiftui/view/focusedsceneobject(_:)) — expose scene-scoped object
- [FocusedObject](/documentation/swiftui/focusedobject) — property wrapper for focused observable object

### Setting focus scope

- [func focusScope(_:)](/documentation/swiftui/view/focusscope(_:)) — define focus scope with namespace
- [func focusSection()](/documentation/swiftui/view/focussection()) — mark as focus section for tvOS

### Controlling default focus

- [func prefersDefaultFocus(_:in:)](/documentation/swiftui/view/prefersdefaultfocus(_:in:)) — prefer default focus in scope
- [func defaultFocus(_:_:priority:)](/documentation/swiftui/view/defaultfocus(_:_:priority:)) — set default focus target
- [DefaultFocusEvaluationPriority](/documentation/swiftui/defaultfocusevaluationpriority) — .automatic, .userInitiated

### Resetting focus

- [var resetFocus](/documentation/swiftui/environmentvalues/resetfocus) — environment: ResetFocusAction
- [ResetFocusAction](/documentation/swiftui/resetfocusaction) — callable action to reset focus in a namespace

### Configuring effects

- [func focusEffectDisabled(_:)](/documentation/swiftui/view/focuseffectdisabled(_:)) — disable focus visual effect
- [var isFocusEffectEnabled](/documentation/swiftui/environmentvalues/isfocuseffectenabled) — environment: focus effect enabled

---

## System events

- [System events](/documentation/swiftui/system-events) — topic group

### Sending and receiving user activities

- [Restoring your app's state with SwiftUI](/documentation/swiftui/restoring-your-app-s-state-with-swiftui) (article)
- [func userActivity(_:element:_:)](/documentation/swiftui/view/useractivity(_:element:_:)) — advertise user activity with element
- [func userActivity(_:isActive:_:)](/documentation/swiftui/view/useractivity(_:isactive:_:)) — advertise user activity
- [func onContinueUserActivity(_:perform:)](/documentation/swiftui/view/oncontinueuseractivity(_:perform:)) — handle incoming activity

### Sending and receiving URLs

- [var openURL](/documentation/swiftui/environmentvalues/openurl) — environment: OpenURLAction
- [OpenURLAction](/documentation/swiftui/openurlaction) — open URLs; Result: .discarded/.handled/.systemAction; callAsFunction with URL
- [func onOpenURL(perform:)](/documentation/swiftui/view/onopenurl(perform:)) — handle incoming URL

### Handling external events

- [func handlesExternalEvents(matching:)](/documentation/swiftui/scene/handlesexternalevents(matching:)) — scene handles external events
- [func handlesExternalEvents(preferring:allowing:)](/documentation/swiftui/view/handlesexternalevents(preferring:allowing:)) — view handles external events

### Handling background tasks

- [func backgroundTask(_:action:)](/documentation/swiftui/scene/backgroundtask(_:action:)) — handle background task in scene
- [BackgroundTask](/documentation/swiftui/backgroundtask) — .appRefresh, .snapshot, .bluetoothAlert, .watchConnectivity, .urlSession, .intentDidRun, .relevantShortcut
- [SnapshotData](/documentation/swiftui/snapshotdata) — snapshot task data; SnapshotReason: appBackgrounded/appScheduled/complicationUpdate/prelaunch/returnToDefaultState
- [SnapshotResponse](/documentation/swiftui/snapshotresponse) — snapshot task response

### Importing and exporting transferable items

- [func importableFromServices(for:action:)](/documentation/swiftui/view/importablefromservices(for:action:)) — import Transferable from services
- [func exportableToServices(_:)](/documentation/swiftui/view/exportabletoservices(_:)) — export Transferable to services
- [func exportableToServices(_:onEdit:)](/documentation/swiftui/view/exportabletoservices(_:onedit:)) — export with edit callback

### Importing and exporting using item providers

- [func importsItemProviders(_:onImport:)](/documentation/swiftui/view/importsitemproviders(_:onimport:)) — import via NSItemProvider
- [func exportsItemProviders(_:onExport:)](/documentation/swiftui/view/exportsitemproviders(_:onexport:)) — export via NSItemProvider
- [func exportsItemProviders(_:onExport:onEdit:)](/documentation/swiftui/view/exportsitemproviders(_:onexport:onedit:)) — export with edit
