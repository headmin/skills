# Event Handling — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
[Gestures](#gestures) | [Keyboard](#responding-to-keyboard-input) | [Shortcuts](#creating-keyboard-shortcuts) | [Hover](#responding-to-hover-events) | [Pointer](#modifying-pointer-appearance) | [Hover effects](#changing-view-appearance-for-hover-events) | [Submission](#responding-to-submission-events) | [Commands](#responding-to-commands) | [Hit testing](#controlling-hit-testing) | [Digital Crown](#interacting-with-the-digital-crown) | [Touch Bar](#managing-touch-bar-input) | [Clipboard](#copying-transferable-items) | [Drag and drop](#drag-and-drop) | [Focus](#focus) | [System events](#system-events) | [Import/export](#importing-and-exporting-transferable-items)

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
- [DragGesture](/documentation/swiftui/draggesture) — Value: startLocation, location, translation, velocity, 3D variants
- [WindowDragGesture](/documentation/swiftui/windowdraggesture) — drag to move window (macOS/visionOS)
- [MagnifyGesture](/documentation/swiftui/magnifygesture) | [RotateGesture](/documentation/swiftui/rotategesture) | [RotateGesture3D](/documentation/swiftui/rotategesture3d) — pinch/rotate gestures
- [GestureMask](/documentation/swiftui/gesturemask) — .all, .gesture, .subviews, .none

### Recognizing Apple Pencil gestures

- [func onPencilDoubleTap(perform:)](/documentation/swiftui/view/onpencildoubletap(perform:)) | [onPencilSqueeze(perform:)](/documentation/swiftui/view/onpencilsqueeze(perform:)) — pencil interactions
- [var preferredPencilDoubleTapAction](/documentation/swiftui/environmentvalues/preferredpencildoubletapaction) | [preferredPencilSqueezeAction](/documentation/swiftui/environmentvalues/preferredpencilsqueezeaction) — user preferences
- [PencilPreferredAction](/documentation/swiftui/pencilpreferredaction) — ignore, showColorPalette, switchEraser, switchPrevious, etc.
- [PencilDoubleTapGestureValue](/documentation/swiftui/pencildoubletapgesturevalue) | [PencilSqueezeGestureValue](/documentation/swiftui/pencilsqueezegesturevalue) — values with hoverPose
- [PencilSqueezeGesturePhase](/documentation/swiftui/pencilsqueezegesturephase) — active/ended/failed
- [PencilHoverPose](/documentation/swiftui/pencilhoverpose) — anchor, location, zDistance, altitude, azimuth, roll

### Combining gestures

- [func simultaneousGesture(_:including:)](/documentation/swiftui/view/simultaneousgesture(_:including:)) — also (isEnabled:), (name:isEnabled:)
- [SequenceGesture](/documentation/swiftui/sequencegesture) | [SimultaneousGesture](/documentation/swiftui/simultaneousgesture) | [ExclusiveGesture](/documentation/swiftui/exclusivegesture) — compose gestures; Values: .first/.second

### Defining custom gestures

- [func highPriorityGesture(_:including:)](/documentation/swiftui/view/highprioritygesture(_:including:)) — priority over children; overloads: (isEnabled:), (name:isEnabled:)
- [func handGestureShortcut(_:isEnabled:)](/documentation/swiftui/view/handgestureshortcut(_:isenabled:)) — visionOS hand shortcut
- [func defersSystemGestures(on:)](/documentation/swiftui/view/deferssystemgestures(on:)) — defer system gestures on edges
- [Gesture](/documentation/swiftui/gesture) — protocol; updating, onChanged, onEnded, simultaneously, sequenced, exclusively, modifiers, map, handActivationBehavior, targetedToEntity
- [AnyGesture](/documentation/swiftui/anygesture) — type-erased; [HandActivationBehavior](/documentation/swiftui/handactivationbehavior): .automatic, .pinch; [HandGestureShortcut](/documentation/swiftui/handgestureshortcut): .primaryAction

### Managing gesture state

- [GestureState](/documentation/swiftui/gesturestate) — property wrapper for transient gesture state; resets when gesture ends
- [GestureStateGesture](/documentation/swiftui/gesturestategesture) — gesture that updates a GestureState
- [func allowsWindowActivationEvents(_:)](/documentation/swiftui/view/allowswindowactivationevents(_:)) — allow window activation on interaction

### Deprecated gestures

- [MagnificationGesture](/documentation/swiftui/magnificationgesture) [deprecated] use MagnifyGesture | [RotationGesture](/documentation/swiftui/rotationgesture) [deprecated] use RotateGesture

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

- [func onModifierKeysChanged(mask:initial:_:)](/documentation/swiftui/view/onmodifierkeyschanged(mask:initial:_:)) — track modifier changes
- [func modifierKeyAlternate(_:_:)](/documentation/swiftui/view/modifierkeyalternate(_:_:)) — alternate content when modifier held

### Responding to hover events

- [func onHover(perform:)](/documentation/swiftui/view/onhover(perform:)) — Bool on enter/exit; [onContinuousHover(coordinateSpace:perform:)](/documentation/swiftui/view/oncontinuoushover(coordinatespace:perform:)) — tracking
- [func hoverEffect(_:isEnabled:)](/documentation/swiftui/view/hovereffect(_:isenabled:)) | [hoverEffectDisabled(_:)](/documentation/swiftui/view/hovereffectdisabled(_:)) | [defaultHoverEffect(_:)](/documentation/swiftui/view/defaulthovereffect(_:))
- [var isHoverEffectEnabled](/documentation/swiftui/environmentvalues/ishovereffectenabled) — environment value
- [HoverPhase](/documentation/swiftui/hoverphase) — .active(CGPoint), .ended
- [HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride) — active/inactive/toggled (+ temporarily variants)
- [OrnamentHoverContentEffect](/documentation/swiftui/ornamenthovercontenteffect) | [OrnamentHoverEffect](/documentation/swiftui/ornamenthovereffect) — visionOS ornament effects

### Modifying pointer appearance

- [func pointerStyle(_:)](/documentation/swiftui/view/pointerstyle(_:)) — set cursor style
- [func pointerVisibility(_:)](/documentation/swiftui/view/pointervisibility(_:)) — control pointer visibility
- [PointerStyle](/documentation/swiftui/pointerstyle) — .default, .horizontalText, .verticalText, .grabIdle, .grabActive, .link, .zoomIn/Out, frameResize, columnResize, rowResize, image, shape
- [HorizontalDirection](/documentation/swiftui/horizontaldirection) | [VerticalDirection](/documentation/swiftui/verticaldirection) | [FrameResizePosition](/documentation/swiftui/frameresizeposition) | [FrameResizeDirection](/documentation/swiftui/frameresizedirection) — supporting types for resize cursors

### Changing view appearance for hover events

- [func hoverEffect(_:)](/documentation/swiftui/view/hovereffect(_:)) — apply effect; also (_:in:isEnabled:) and (in:isEnabled:body:) overloads
- [HoverEffect](/documentation/swiftui/hovereffect) — .automatic, .highlight, .lift
- [CustomHoverEffect](/documentation/swiftui/customhovereffect) — protocol; built-ins: .automatic, .empty, .highlight, .lift
- [AutomaticHoverEffect](/documentation/swiftui/automatichovereffect) | [EmptyHoverEffect](/documentation/swiftui/emptyhovereffect) | [HighlightHoverEffect](/documentation/swiftui/highlighthovereffect) | [LiftHoverEffect](/documentation/swiftui/lifthovereffect) | [ContentHoverEffect](/documentation/swiftui/contenthovereffect)
- [HoverEffectGroup](/documentation/swiftui/hovereffectgroup) — group effects; Behavior: activatesGroup/followsGroup/ignoresGroup/preservesGroup
- [func hoverEffectGroup()](/documentation/swiftui/view/hovereffectgroup()) — also (_:) and (id:in:behavior:); [GroupHoverEffect](/documentation/swiftui/grouphovereffect)
- [HoverEffectContent](/documentation/swiftui/hovereffectcontent) — effect content (animation, clip, offset, opacity, rotation, scale, transform); [EmptyHoverEffectContent](/documentation/swiftui/emptyhovereffectcontent)
- [func handPointerBehavior(_:)](/documentation/swiftui/view/handpointerbehavior(_:)) — visionOS; [HandPointerBehavior](/documentation/swiftui/handpointerbehavior): .drawing, .inactive

### Responding to submission events

- [func onSubmit(of:_:)](/documentation/swiftui/view/onsubmit(of:_:)) — handle submit; [SubmitTriggers](/documentation/swiftui/submittriggers): .search, .text
- [func submitScope(_:)](/documentation/swiftui/view/submitscope(_:)) — prevent propagation
- [func submitLabel(_:)](/documentation/swiftui/view/submitlabel(_:)) — set return key; [SubmitLabel](/documentation/swiftui/submitlabel): .continue, .done, .go, .join, .next, .return, .route, .search, .send

### Responding to commands

- [func onMoveCommand(perform:)](/documentation/swiftui/view/onmovecommand(perform:)) — arrow/remote move
- [func onDeleteCommand(perform:)](/documentation/swiftui/view/ondeletecommand(perform:)) | [onExitCommand(perform:)](/documentation/swiftui/view/onexitcommand(perform:)) | [onPlayPauseCommand(perform:)](/documentation/swiftui/view/onplaypausecommand(perform:))
- [func pageCommand(value:in:step:)](/documentation/swiftui/view/pagecommand(value:in:step:)) — page up/down
- [func onCommand(_:perform:)](/documentation/swiftui/view/oncommand(_:perform:)) — Selector-based command
- [MoveCommandDirection](/documentation/swiftui/movecommanddirection) — .up, .down, .left, .right

### Controlling hit testing

- [func allowsTightening(_:)](/documentation/swiftui/view/allowstightening(_:)) — tighter character spacing
- [func contentShape(_:eoFill:)](/documentation/swiftui/view/contentshape(_:eofill:)) — hit-test shape; also (_:_:eoFill:) for specific ContentShapeKinds
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

- [func onCameraCaptureEvent(isEnabled:action:)](/documentation/swiftui/view/oncameracaptureevent(isenabled:action:)) — camera button; also (primaryAction:secondaryAction:) overload
- [Clipboard](/documentation/swiftui/clipboard) — clipboard access

### Copying transferable items

- [func copyable(_:)](/documentation/swiftui/view/copyable(_:)) | [cuttable(for:action:)](/documentation/swiftui/view/cuttable(for:action:)) | [pasteDestination(for:action:validator:)](/documentation/swiftui/view/pastedestination(for:action:validator:)) — Transferable copy/cut/paste

### Copying items using item providers

- [func onCopyCommand(perform:)](/documentation/swiftui/view/oncopycommand(perform:)) | [onCutCommand(perform:)](/documentation/swiftui/view/oncutcommand(perform:)) — NSItemProvider copy/cut
- [func onPasteCommand(of:perform:)](/documentation/swiftui/view/onpastecommand(of:perform:)) — paste; also (of:validator:perform:) overload

---

## Drag and drop

- [Drag and drop](/documentation/swiftui/drag-and-drop) — topic group
- [Adopting drag and drop using SwiftUI](/documentation/swiftui/adopting-drag-and-drop-using-swiftui) (article)
- [Making a view into a drag source](/documentation/swiftui/making-a-view-into-a-drag-source) (article)

### Configuring drag and drop behavior

- [DragConfiguration](/documentation/swiftui/dragconfiguration) — configure drag ops (OperationsOutsideApp/OperationsWithinApp)
- [DropConfiguration](/documentation/swiftui/dropconfiguration) — configure drop: operation, acceptedItemCount

### Moving items

- [DragSession](/documentation/swiftui/dragsession) — active drag: id, location, phase, draggedItemIndex
- [DropSession](/documentation/swiftui/dropsession) — active drop: id, location, phase, itemsCount, suggestedOperations, localSession

### Moving transferable items

- [func draggable(_:)](/documentation/swiftui/view/draggable(_:)) — make Transferable draggable; also (_:preview:) overload
- [func dropDestination(for:action:isTargeted:)](/documentation/swiftui/view/dropdestination(for:action:istargeted:)) — receive Transferable drops

### Moving items using item providers

- [func itemProvider(_:)](/documentation/swiftui/view/itemprovider(_:)) — provide NSItemProvider for drag
- [func onDrag(_:)](/documentation/swiftui/view/ondrag(_:)) — drag via NSItemProvider; also (_:preview:) overload
- [func onDrop(of:isTargeted:perform:)](/documentation/swiftui/view/ondrop(of:istargeted:perform:)) — drop; also (of:delegate:) overload
- [DropDelegate](/documentation/swiftui/dropdelegate) — protocol: dropEntered, dropExited, dropUpdated, validateDrop, performDrop
- [DropProposal](/documentation/swiftui/dropproposal) — proposed operation; [DropOperation](/documentation/swiftui/dropoperation) — .cancel, .copy, .move, .forbidden, .alias, .delete
- [DropInfo](/documentation/swiftui/dropinfo) — drop location + item type checking

### Describing preview formations

- [DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation) — .default, .list, .none, .pile, .stack

### Configuring spring loading

- [func springLoadingBehavior(_:)](/documentation/swiftui/view/springloadingbehavior(_:)) — configure; [SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior): .automatic, .enabled, .disabled
- [var springLoadingBehavior](/documentation/swiftui/environmentvalues/springloadingbehavior) — environment value

---

## Focus

- [Focus](/documentation/swiftui/focus) — topic group
- [Focus Cookbook: Supporting and enhancing focus-driven interactions](/documentation/swiftui/focus-cookbook-sample) (article)

### Indicating that a view can receive focus

- [func focusable(_:)](/documentation/swiftui/view/focusable(_:)) — make focusable; also (_:interactions:) with [FocusInteractions](/documentation/swiftui/focusinteractions) (.automatic, .activate, .edit)

### Managing focus state

- [func focused(_:equals:)](/documentation/swiftui/view/focused(_:equals:)) — bind focus to enum; also focused(_:) for Bool
- [var isFocused](/documentation/swiftui/environmentvalues/isfocused) — environment value
- [FocusState](/documentation/swiftui/focusstate) — property wrapper for focus tracking
- [FocusedValue](/documentation/swiftui/focusedvalue) — property wrapper for focused view's value; [macro Entry()](/documentation/swiftui/entry()) | [FocusedValueKey](/documentation/swiftui/focusedvaluekey)
- [FocusedBinding](/documentation/swiftui/focusedbinding) — property wrapper for focused bindings
- [func searchFocused(_:)](/documentation/swiftui/view/searchfocused(_:)) — bind search focus; also (_:equals:) overload

### Exposing value types to focused views

- [func focusedValue(_:)](/documentation/swiftui/view/focusedvalue(_:)) — expose value; also (_:_:) keyed variant
- [func focusedSceneValue(_:)](/documentation/swiftui/view/focusedscenevalue(_:)) — scene-scoped; also (_:_:) keyed variant
- [FocusedValues](/documentation/swiftui/focusedvalues) — collection of focused values

### Exposing reference types to focused views

- [func focusedObject(_:)](/documentation/swiftui/view/focusedobject(_:)) | [focusedSceneObject(_:)](/documentation/swiftui/view/focusedsceneobject(_:)) — expose ObservableObject (view/scene scoped)
- [FocusedObject](/documentation/swiftui/focusedobject) — property wrapper for focused observable object

### Setting focus scope

- [func focusScope(_:)](/documentation/swiftui/view/focusscope(_:)) — define focus scope; [focusSection()](/documentation/swiftui/view/focussection()) — tvOS focus section

### Controlling default focus

- [func prefersDefaultFocus(_:in:)](/documentation/swiftui/view/prefersdefaultfocus(_:in:)) | [defaultFocus(_:_:priority:)](/documentation/swiftui/view/defaultfocus(_:_:priority:)) — set default focus
- [DefaultFocusEvaluationPriority](/documentation/swiftui/defaultfocusevaluationpriority) — .automatic, .userInitiated

### Resetting focus

- [var resetFocus](/documentation/swiftui/environmentvalues/resetfocus) — environment: [ResetFocusAction](/documentation/swiftui/resetfocusaction), reset focus in a namespace

### Configuring effects

- [func focusEffectDisabled(_:)](/documentation/swiftui/view/focuseffectdisabled(_:)) — disable focus effect; [var isFocusEffectEnabled](/documentation/swiftui/environmentvalues/isfocuseffectenabled)

---

## System events

- [System events](/documentation/swiftui/system-events) — topic group

### Sending and receiving user activities

- [Restoring your app's state with SwiftUI](/documentation/swiftui/restoring-your-app-s-state-with-swiftui) (article)
- [func userActivity(_:element:_:)](/documentation/swiftui/view/useractivity(_:element:_:)) — advertise activity; also (_:isActive:_:)
- [func onContinueUserActivity(_:perform:)](/documentation/swiftui/view/oncontinueuseractivity(_:perform:)) — handle incoming activity

### Sending and receiving URLs

- [var openURL](/documentation/swiftui/environmentvalues/openurl) — environment: [OpenURLAction](/documentation/swiftui/openurlaction) (Result: .discarded/.handled/.systemAction)
- [func onOpenURL(perform:)](/documentation/swiftui/view/onopenurl(perform:)) — handle incoming URL

### Handling external events

- [func handlesExternalEvents(matching:)](/documentation/swiftui/scene/handlesexternalevents(matching:)) — scene; also [view (preferring:allowing:)](/documentation/swiftui/view/handlesexternalevents(preferring:allowing:))

### Handling background tasks

- [func backgroundTask(_:action:)](/documentation/swiftui/scene/backgroundtask(_:action:)) — handle background task in scene
- [BackgroundTask](/documentation/swiftui/backgroundtask) — .appRefresh, .snapshot, .bluetoothAlert, .watchConnectivity, .urlSession, .intentDidRun, .relevantShortcut
- [SnapshotData](/documentation/swiftui/snapshotdata) | [SnapshotResponse](/documentation/swiftui/snapshotresponse) — snapshot task data/response

### Importing and exporting transferable items

- [func importableFromServices(for:action:)](/documentation/swiftui/view/importablefromservices(for:action:)) — import Transferable from services
- [func exportableToServices(_:)](/documentation/swiftui/view/exportabletoservices(_:)) — export Transferable; also (_:onEdit:) overload

### Importing and exporting using item providers

- [func importsItemProviders(_:onImport:)](/documentation/swiftui/view/importsitemproviders(_:onimport:)) — import via NSItemProvider
- [func exportsItemProviders(_:onExport:)](/documentation/swiftui/view/exportsitemproviders(_:onexport:)) — export via NSItemProvider; also (_:onExport:onEdit:)
