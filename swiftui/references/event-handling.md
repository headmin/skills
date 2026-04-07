# Event Handling — SwiftUI Reference

## Contents
- [Event handling](#event-handling)
  - [Essentials](#essentials)
  - [Recognizing tap gestures](#recognizing-tap-gestures)
  - [Recognizing long press gestures](#recognizing-long-press-gestures)
  - [Recognizing spatial events](#recognizing-spatial-events)
  - [Recognizing gestures that change over time](#recognizing-gestures-that-change-over-time)
  - [Recognizing Apple Pencil gestures](#recognizing-apple-pencil-gestures)
  - [Combining gestures](#combining-gestures)
  - [Defining custom gestures](#defining-custom-gestures)
  - [Managing gesture state](#managing-gesture-state)
  - [Handling activation events](#handling-activation-events)
  - [Deprecated gestures](#deprecated-gestures)
  - [Responding to keyboard input](#responding-to-keyboard-input)
  - [Creating keyboard shortcuts](#creating-keyboard-shortcuts)
  - [Responding to modifier keys](#responding-to-modifier-keys)
  - [Responding to hover events](#responding-to-hover-events)
  - [Modifying pointer appearance](#modifying-pointer-appearance)
  - [Changing view appearance for hover events](#changing-view-appearance-for-hover-events)
  - [Responding to submission events](#responding-to-submission-events)
  - [Labeling a submission event](#labeling-a-submission-event)
  - [Responding to commands](#responding-to-commands)
  - [Controlling hit testing](#controlling-hit-testing)
  - [Interacting with the Digital Crown](#interacting-with-the-digital-crown)
  - [Managing Touch Bar input](#managing-touch-bar-input)
  - [Responding to capture events](#responding-to-capture-events)
  - [Copying transferable items](#copying-transferable-items)
  - [Copying items using item providers](#copying-items-using-item-providers)
  - [Essentials](#essentials)
  - [Configuring drag and drop behavior](#configuring-drag-and-drop-behavior)
  - [Moving items](#moving-items)
  - [Moving transferable items](#moving-transferable-items)
  - [Moving items using item providers](#moving-items-using-item-providers)
  - [Describing preview formations](#describing-preview-formations)
  - [Configuring spring loading](#configuring-spring-loading)
  - [Essentials](#essentials)
  - [Indicating that a view can receive focus](#indicating-that-a-view-can-receive-focus)
  - [Managing focus state](#managing-focus-state)
  - [Exposing value types to focused views](#exposing-value-types-to-focused-views)
  - [Exposing reference types to focused views](#exposing-reference-types-to-focused-views)
  - [Setting focus scope](#setting-focus-scope)
  - [Controlling default focus](#controlling-default-focus)
  - [Resetting focus](#resetting-focus)
  - [Configuring effects](#configuring-effects)
  - [Sending and receiving user activities](#sending-and-receiving-user-activities)
  - [Sending and receiving URLs](#sending-and-receiving-urls)
  - [Handling external events](#handling-external-events)
  - [Handling background tasks](#handling-background-tasks)
  - [Importing and exporting transferable items](#importing-and-exporting-transferable-items)
  - [Importing and exporting using item providers](#importing-and-exporting-using-item-providers)

---
## Event handling

- [Gestures](/documentation/swiftui/gestures)

### Essentials

- [Adding interactivity with gestures](/documentation/swiftui/adding-interactivity-with-gestures)

### Recognizing tap gestures

- [func onTapGesture(count: Int, perform: () -> Void) -> some View](/documentation/swiftui/view/ontapgesture(count:perform:))
- [func onTapGesture(count:coordinateSpace:perform:)](/documentation/swiftui/view/ontapgesture(count:coordinatespace:perform:))
- [TapGesture](/documentation/swiftui/tapgesture)

#### Creating a tap gesture

- [init(count: Int)](/documentation/swiftui/tapgesture/init(count:))
- [var count: Int](/documentation/swiftui/tapgesture/count)
- [SpatialTapGesture](/documentation/swiftui/spatialtapgesture)

#### Creating a spatial tap gesture

- [init(count: Int, coordinateSpace: some CoordinateSpaceProtocol)](/documentation/swiftui/spatialtapgesture/init(count:coordinatespace:)-75s7q)
- [var coordinateSpace: CoordinateSpace](/documentation/swiftui/spatialtapgesture/coordinatespace)
- [var count: Int](/documentation/swiftui/spatialtapgesture/count)

#### Getting the gesture’s value

- [SpatialTapGesture.Value](/documentation/swiftui/spatialtapgesture/value)

##### Getting the tap location

- [var location: CGPoint](/documentation/swiftui/spatialtapgesture/value/location)
- [var location3D: Point3D](/documentation/swiftui/spatialtapgesture/value/location3d)

#### Deprecated initializers

- [init(count: Int, coordinateSpace: CoordinateSpace)](/documentation/swiftui/spatialtapgesture/init(count:coordinatespace:)-1b85g)

#### Initializers

- [init(count: Int, coordinateSpace3D: some CoordinateSpace3D)](/documentation/swiftui/spatialtapgesture/init(count:coordinatespace3d:))
- [init(count:coordinateSpace:)](/documentation/swiftui/spatialtapgesture/init(count:coordinatespace:))

### Recognizing long press gestures

- [func onLongPressGesture(minimumDuration: Double, maximumDistance: CGFloat, perform: () -> Void, onPressingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:maximumdistance:perform:onpressingchanged:))
- [func onLongPressGesture(minimumDuration: Double, perform: () -> Void, onPressingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongpressgesture(minimumduration:perform:onpressingchanged:))
- [func onLongTouchGesture(minimumDuration: Double, perform: () -> Void, onTouchingChanged: ((Bool) -> Void)?) -> some View](/documentation/swiftui/view/onlongtouchgesture(minimumduration:perform:ontouchingchanged:))
- [LongPressGesture](/documentation/swiftui/longpressgesture)

#### Creating a long press gesture

- [init(minimumDuration: Double)](/documentation/swiftui/longpressgesture/init(minimumduration:))
- [init(minimumDuration: Double, maximumDistance: CGFloat)](/documentation/swiftui/longpressgesture/init(minimumduration:maximumdistance:))
- [var minimumDuration: Double](/documentation/swiftui/longpressgesture/minimumduration)
- [var maximumDistance: CGFloat](/documentation/swiftui/longpressgesture/maximumdistance)

### Recognizing spatial events

- [SpatialEventGesture](/documentation/swiftui/spatialeventgesture)

#### Creating a spatial event gesture

- [init(coordinateSpace: any CoordinateSpaceProtocol)](/documentation/swiftui/spatialeventgesture/init(coordinatespace:))

#### Getting gesture properties

- [let coordinateSpace: CoordinateSpace](/documentation/swiftui/spatialeventgesture/coordinatespace)

#### Initializers

- [init(coordinateSpace3D: some CoordinateSpace3D)](/documentation/swiftui/spatialeventgesture/init(coordinatespace3d:))
- [SpatialEventCollection](/documentation/swiftui/spatialeventcollection)

#### Accessing the collection’s events

- [SpatialEventCollection.Event](/documentation/swiftui/spatialeventcollection/event)

##### Identifying the event

- [var timestamp: TimeInterval](/documentation/swiftui/spatialeventcollection/event/timestamp)
- [var id: SpatialEventCollection.Event.ID](/documentation/swiftui/spatialeventcollection/event/id-swift.property)
- [SpatialEventCollection.Event.ID](/documentation/swiftui/spatialeventcollection/event/id-swift.struct)
- [var kind: SpatialEventCollection.Event.Kind](/documentation/swiftui/spatialeventcollection/event/kind-swift.property)
- [SpatialEventCollection.Event.Kind](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum)

###### Getting the event type

- [case directPinch](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum/directpinch)
- [case indirectPinch](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum/indirectpinch)
- [case pointer](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum/pointer)
- [case touch](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum/touch)

###### Enumeration Cases

- [case pencil](/documentation/swiftui/spatialeventcollection/event/kind-swift.enum/pencil)
- [var modifierKeys: EventModifiers](/documentation/swiftui/spatialeventcollection/event/modifierkeys)

##### Locating the event

- [var location: CGPoint](/documentation/swiftui/spatialeventcollection/event/location)
- [var location3D: Point3D](/documentation/swiftui/spatialeventcollection/event/location3d)
- [var selectionRay: Ray3D?](/documentation/swiftui/spatialeventcollection/event/selectionray)
- [var inputDevicePose: SpatialEventCollection.Event.InputDevicePose?](/documentation/swiftui/spatialeventcollection/event/inputdevicepose-swift.property)
- [SpatialEventCollection.Event.InputDevicePose](/documentation/swiftui/spatialeventcollection/event/inputdevicepose-swift.struct)

###### Getting the event type

- [var altitude: Angle](/documentation/swiftui/spatialeventcollection/event/inputdevicepose-swift.struct/altitude)
- [var azimuth: Angle](/documentation/swiftui/spatialeventcollection/event/inputdevicepose-swift.struct/azimuth)
- [var pose3D: Pose3D](/documentation/swiftui/spatialeventcollection/event/inputdevicepose-swift.struct/pose3d)
- [var targetedEntity: Entity?](/documentation/swiftui/spatialeventcollection/event/targetedentity)

##### Getting the event’s current phase

- [var phase: SpatialEventCollection.Event.Phase](/documentation/swiftui/spatialeventcollection/event/phase-swift.property)
- [SpatialEventCollection.Event.Phase](/documentation/swiftui/spatialeventcollection/event/phase-swift.enum)

###### Getting the phase

- [case active](/documentation/swiftui/spatialeventcollection/event/phase-swift.enum/active)
- [case cancelled](/documentation/swiftui/spatialeventcollection/event/phase-swift.enum/cancelled)
- [case ended](/documentation/swiftui/spatialeventcollection/event/phase-swift.enum/ended)

##### Instance Properties

- [var chirality: Chirality?](/documentation/swiftui/spatialeventcollection/event/chirality)
- [var trackingAreaIdentifier: LayerRenderer.Drawable.TrackingArea.Identifier](/documentation/swiftui/spatialeventcollection/event/trackingareaidentifier)
- [subscript(SpatialEventCollection.Event.ID) -> SpatialEventCollection.Event?](/documentation/swiftui/spatialeventcollection/subscript(_:))

#### Iterating over events in the collection

- [func makeIterator() -> SpatialEventCollection.Iterator](/documentation/swiftui/spatialeventcollection/makeiterator())
- [SpatialEventCollection.Iterator](/documentation/swiftui/spatialeventcollection/iterator)

##### Getting the next event

- [func next() -> SpatialEventCollection.Event?](/documentation/swiftui/spatialeventcollection/iterator/next())
- [Chirality](/documentation/swiftui/chirality)

#### Enumeration Cases

- [case left](/documentation/swiftui/chirality/left)
- [case right](/documentation/swiftui/chirality/right)

### Recognizing gestures that change over time

- [func gesture(_:)](/documentation/swiftui/view/gesture(_:))
- [func gesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/gesture(_:isenabled:))
- [func gesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/gesture(_:name:isenabled:))
- [func gesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/gesture(_:including:))
- [DragGesture](/documentation/swiftui/draggesture)

#### Creating a drag gesture

- [init(minimumDistance: CGFloat, coordinateSpace: some CoordinateSpaceProtocol)](/documentation/swiftui/draggesture/init(minimumdistance:coordinatespace:)-8ffe5)
- [var minimumDistance: CGFloat](/documentation/swiftui/draggesture/minimumdistance)
- [var coordinateSpace: CoordinateSpace](/documentation/swiftui/draggesture/coordinatespace)

#### Deprecated initializers

- [init(minimumDistance: CGFloat, coordinateSpace: CoordinateSpace)](/documentation/swiftui/draggesture/init(minimumdistance:coordinatespace:)-3804h)

#### Structures

- [DragGesture.Value](/documentation/swiftui/draggesture/value)

##### Getting 2D position

- [var startLocation: CGPoint](/documentation/swiftui/draggesture/value/startlocation)
- [var location: CGPoint](/documentation/swiftui/draggesture/value/location)
- [var predictedEndLocation: CGPoint](/documentation/swiftui/draggesture/value/predictedendlocation)
- [var translation: CGSize](/documentation/swiftui/draggesture/value/translation)
- [var predictedEndTranslation: CGSize](/documentation/swiftui/draggesture/value/predictedendtranslation)

##### Getting 3D position

- [var startLocation3D: Point3D](/documentation/swiftui/draggesture/value/startlocation3d)
- [var location3D: Point3D](/documentation/swiftui/draggesture/value/location3d)
- [var predictedEndLocation3D: Point3D](/documentation/swiftui/draggesture/value/predictedendlocation3d)
- [var translation3D: Vector3D](/documentation/swiftui/draggesture/value/translation3d)
- [var predictedEndTranslation3D: Vector3D](/documentation/swiftui/draggesture/value/predictedendtranslation3d)
- [var startInputDevicePose3D: Pose3D?](/documentation/swiftui/draggesture/value/startinputdevicepose3d)
- [var inputDevicePose3D: Pose3D?](/documentation/swiftui/draggesture/value/inputdevicepose3d)

##### Handling changes over time

- [var time: Date](/documentation/swiftui/draggesture/value/time)
- [var velocity: CGSize](/documentation/swiftui/draggesture/value/velocity)

#### Initializers

- [init(minimumDistance: CGFloat, coordinateSpace3D: some CoordinateSpace3D)](/documentation/swiftui/draggesture/init(minimumdistance:coordinatespace3d:))
- [init(minimumDistance:coordinateSpace:)](/documentation/swiftui/draggesture/init(minimumdistance:coordinatespace:))
- [WindowDragGesture](/documentation/swiftui/windowdraggesture)

#### Structures

- [WindowDragGesture.Value](/documentation/swiftui/windowdraggesture/value)

#### Initializers

- [init()](/documentation/swiftui/windowdraggesture/init())
- [MagnifyGesture](/documentation/swiftui/magnifygesture)

#### Creating the gesture

- [init(minimumScaleDelta: CGFloat)](/documentation/swiftui/magnifygesture/init(minimumscaledelta:))
- [var minimumScaleDelta: CGFloat](/documentation/swiftui/magnifygesture/minimumscaledelta)
- [RotateGesture](/documentation/swiftui/rotategesture)

#### Creating the gesture

- [init(minimumAngleDelta: Angle)](/documentation/swiftui/rotategesture/init(minimumangledelta:))
- [var minimumAngleDelta: Angle](/documentation/swiftui/rotategesture/minimumangledelta)
- [RotateGesture3D](/documentation/swiftui/rotategesture3d)

#### Creating the gesture

- [init(constrainedToAxis: RotationAxis3D?, minimumAngleDelta: Angle)](/documentation/swiftui/rotategesture3d/init(constrainedtoaxis:minimumangledelta:))
- [var minimumAngleDelta: Angle](/documentation/swiftui/rotategesture3d/minimumangledelta)
- [var constrainedAxis: RotationAxis3D?](/documentation/swiftui/rotategesture3d/constrainedaxis)
- [GestureMask](/documentation/swiftui/gesturemask)

#### Getting gesture options

- [static let all: GestureMask](/documentation/swiftui/gesturemask/all)
- [static let gesture: GestureMask](/documentation/swiftui/gesturemask/gesture)
- [static let subviews: GestureMask](/documentation/swiftui/gesturemask/subviews)
- [static let none: GestureMask](/documentation/swiftui/gesturemask/none)

### Recognizing Apple Pencil gestures

- [func onPencilDoubleTap(perform: (PencilDoubleTapGestureValue) -> Void) -> some View](/documentation/swiftui/view/onpencildoubletap(perform:))
- [func onPencilSqueeze(perform: (PencilSqueezeGesturePhase) -> Void) -> some View](/documentation/swiftui/view/onpencilsqueeze(perform:))
- [var preferredPencilDoubleTapAction: PencilPreferredAction](/documentation/swiftui/environmentvalues/preferredpencildoubletapaction)
- [var preferredPencilSqueezeAction: PencilPreferredAction](/documentation/swiftui/environmentvalues/preferredpencilsqueezeaction)
- [PencilPreferredAction](/documentation/swiftui/pencilpreferredaction)

#### Getting the preffered actions

- [static let ignore: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/ignore)
- [static let showColorPalette: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/showcolorpalette)
- [static let showInkAttributes: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/showinkattributes)
- [static let switchEraser: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/switcheraser)
- [static let switchPrevious: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/switchprevious)

#### Type Properties

- [static let runSystemShortcut: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/runsystemshortcut)
- [static let showContextualPalette: PencilPreferredAction](/documentation/swiftui/pencilpreferredaction/showcontextualpalette)
- [PencilDoubleTapGestureValue](/documentation/swiftui/pencildoubletapgesturevalue)

#### Getting the gesture values

- [let hoverPose: PencilHoverPose?](/documentation/swiftui/pencildoubletapgesturevalue/hoverpose)
- [PencilSqueezeGestureValue](/documentation/swiftui/pencilsqueezegesturevalue)

#### Instance Properties

- [let hoverPose: PencilHoverPose?](/documentation/swiftui/pencilsqueezegesturevalue/hoverpose)
- [PencilSqueezeGesturePhase](/documentation/swiftui/pencilsqueezegesturephase)

#### Enumeration Cases

- [case active(PencilSqueezeGestureValue)](/documentation/swiftui/pencilsqueezegesturephase/active(_:))
- [case ended(PencilSqueezeGestureValue)](/documentation/swiftui/pencilsqueezegesturephase/ended(_:))
- [case failed](/documentation/swiftui/pencilsqueezegesturephase/failed)
- [PencilHoverPose](/documentation/swiftui/pencilhoverpose)

#### Getting the hover characteristics

- [let anchor: UnitPoint](/documentation/swiftui/pencilhoverpose/anchor)
- [let location: CGPoint](/documentation/swiftui/pencilhoverpose/location)
- [let zDistance: CGFloat](/documentation/swiftui/pencilhoverpose/zdistance)

#### Instance Properties

- [let altitude: Angle](/documentation/swiftui/pencilhoverpose/altitude)
- [let azimuth: Angle](/documentation/swiftui/pencilhoverpose/azimuth)
- [let roll: Angle](/documentation/swiftui/pencilhoverpose/roll)

### Combining gestures

- [Composing SwiftUI gestures](/documentation/swiftui/composing-swiftui-gestures)
- [func simultaneousGesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/simultaneousgesture(_:including:))
- [func simultaneousGesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/simultaneousgesture(_:isenabled:))
- [func simultaneousGesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/simultaneousgesture(_:name:isenabled:))
- [SequenceGesture](/documentation/swiftui/sequencegesture)

#### Creating the gesture

- [init(First, Second)](/documentation/swiftui/sequencegesture/init(_:_:))
- [var first: First](/documentation/swiftui/sequencegesture/first)
- [var second: Second](/documentation/swiftui/sequencegesture/second)

#### Getting the gesture’s values

- [SequenceGesture.Value](/documentation/swiftui/sequencegesture/value)

##### Getting gesture values

- [case first(First.Value)](/documentation/swiftui/sequencegesture/value/first(_:))
- [case second(First.Value, Second.Value?)](/documentation/swiftui/sequencegesture/value/second(_:_:))
- [SimultaneousGesture](/documentation/swiftui/simultaneousgesture)

#### Creating the gesture

- [init(First, Second)](/documentation/swiftui/simultaneousgesture/init(_:_:))
- [var first: First](/documentation/swiftui/simultaneousgesture/first)
- [var second: Second](/documentation/swiftui/simultaneousgesture/second)

#### Getting the gesture’s values

- [SimultaneousGesture.Value](/documentation/swiftui/simultaneousgesture/value)

##### Getting gesture values

- [var first: First.Value?](/documentation/swiftui/simultaneousgesture/value/first)
- [var second: Second.Value?](/documentation/swiftui/simultaneousgesture/value/second)
- [ExclusiveGesture](/documentation/swiftui/exclusivegesture)

#### Creating the gesture

- [init(First, Second)](/documentation/swiftui/exclusivegesture/init(_:_:))
- [var first: First](/documentation/swiftui/exclusivegesture/first)
- [var second: Second](/documentation/swiftui/exclusivegesture/second)

#### Supporting types

- [ExclusiveGesture.Value](/documentation/swiftui/exclusivegesture/value)

##### Getting gesture values

- [case first(First.Value)](/documentation/swiftui/exclusivegesture/value/first(_:))
- [case second(Second.Value)](/documentation/swiftui/exclusivegesture/value/second(_:))

### Defining custom gestures

- [func highPriorityGesture<T>(T, including: GestureMask) -> some View](/documentation/swiftui/view/highprioritygesture(_:including:))
- [func highPriorityGesture<T>(T, isEnabled: Bool) -> some View](/documentation/swiftui/view/highprioritygesture(_:isenabled:))
- [func highPriorityGesture<T>(T, name: String, isEnabled: Bool) -> some View](/documentation/swiftui/view/highprioritygesture(_:name:isenabled:))
- [func handGestureShortcut(HandGestureShortcut, isEnabled: Bool) -> some View](/documentation/swiftui/view/handgestureshortcut(_:isenabled:))
- [func defersSystemGestures(on: Edge.Set) -> some View](/documentation/swiftui/view/deferssystemgestures(on:))
- [Gesture](/documentation/swiftui/gesture)

#### Implementing a custom gesture

- [var body: Self.Body](/documentation/swiftui/gesture/body-swift.property)
- [Body](/documentation/swiftui/gesture/body-swift.associatedtype)

#### Performing the gesture

- [func updating<State>(GestureState<State>, body: (Self.Value, inout State, inout Transaction) -> Void) -> GestureStateGesture<Self, State>](/documentation/swiftui/gesture/updating(_:body:))
- [func onChanged((Self.Value) -> Void) -> _ChangedGesture<Self>](/documentation/swiftui/gesture/onchanged(_:))
- [func onEnded((Self.Value) -> Void) -> _EndedGesture<Self>](/documentation/swiftui/gesture/onended(_:))
- [Value](/documentation/swiftui/gesture/value)

#### Composing gestures

- [func simultaneously<Other>(with: Other) -> SimultaneousGesture<Self, Other>](/documentation/swiftui/gesture/simultaneously(with:))
- [func sequenced<Other>(before: Other) -> SequenceGesture<Self, Other>](/documentation/swiftui/gesture/sequenced(before:))
- [func exclusively<Other>(before: Other) -> ExclusiveGesture<Self, Other>](/documentation/swiftui/gesture/exclusively(before:))

#### Adding modifier keys to a gesture

- [func modifiers(EventModifiers) -> _ModifiersGesture<Self>](/documentation/swiftui/gesture/modifiers(_:))

#### Transforming a gesture

- [func map<T>((Self.Value) -> T) -> _MapGesture<Self, T>](/documentation/swiftui/gesture/map(_:))

#### Customizing gesture activation

- [func handActivationBehavior(HandActivationBehavior) -> some Gesture<Self.Value>
](/documentation/swiftui/gesture/handactivationbehavior(_:))

#### Using a gesture with a RealityKit entity

- [func targetedToAnyEntity() -> some Gesture<EntityTargetValue<Self.Value>>
](/documentation/swiftui/gesture/targetedtoanyentity())
- [func targetedToEntity(Entity) -> some Gesture<EntityTargetValue<Self.Value>>
](/documentation/swiftui/gesture/targetedtoentity(_:))
- [func targetedToEntity(where: QueryPredicate<Entity>) -> some Gesture<EntityTargetValue<Self.Value>>
](/documentation/swiftui/gesture/targetedtoentity(where:))
- [AnyGesture](/documentation/swiftui/anygesture)

#### Implementing a custom gesture

- [init<T>(T)](/documentation/swiftui/anygesture/init(_:))
- [HandActivationBehavior](/documentation/swiftui/handactivationbehavior)

#### Getting the behaviors

- [static let automatic: HandActivationBehavior](/documentation/swiftui/handactivationbehavior/automatic)
- [static let pinch: HandActivationBehavior](/documentation/swiftui/handactivationbehavior/pinch)
- [HandGestureShortcut](/documentation/swiftui/handgestureshortcut)

#### Type Properties

- [static let primaryAction: HandGestureShortcut](/documentation/swiftui/handgestureshortcut/primaryaction)

### Managing gesture state

- [GestureState](/documentation/swiftui/gesturestate)

#### Creating a gesture state

- [init(initialValue: Value)](/documentation/swiftui/gesturestate/init(initialvalue:))
- [init(initialValue: Value, reset: (Value, inout Transaction) -> Void)](/documentation/swiftui/gesturestate/init(initialvalue:reset:))
- [init(initialValue: Value, resetTransaction: Transaction)](/documentation/swiftui/gesturestate/init(initialvalue:resettransaction:))
- [init(reset: (Value, inout Transaction) -> Void)](/documentation/swiftui/gesturestate/init(reset:))
- [init(resetTransaction: Transaction)](/documentation/swiftui/gesturestate/init(resettransaction:))
- [init(wrappedValue: Value)](/documentation/swiftui/gesturestate/init(wrappedvalue:))
- [init(wrappedValue: Value, reset: (Value, inout Transaction) -> Void)](/documentation/swiftui/gesturestate/init(wrappedvalue:reset:))
- [init(wrappedValue: Value, resetTransaction: Transaction)](/documentation/swiftui/gesturestate/init(wrappedvalue:resettransaction:))

#### Getting the state

- [var wrappedValue: Value](/documentation/swiftui/gesturestate/wrappedvalue)
- [var projectedValue: GestureState<Value>](/documentation/swiftui/gesturestate/projectedvalue)
- [GestureStateGesture](/documentation/swiftui/gesturestategesture)

#### Creating an in-progress gesture

- [init(base: Base, state: GestureState<State>, body: (GestureStateGesture<Base, State>.Value, inout State, inout Transaction) -> Void)](/documentation/swiftui/gesturestategesture/init(base:state:body:))
- [var base: Base](/documentation/swiftui/gesturestategesture/base)
- [var state: GestureState<State>](/documentation/swiftui/gesturestategesture/state)

#### Supporting types

- [var body: (GestureStateGesture<Base, State>.Value, inout State, inout Transaction) -> Void](/documentation/swiftui/gesturestategesture/body)

### Handling activation events

- [func allowsWindowActivationEvents(Bool?) -> some View](/documentation/swiftui/view/allowswindowactivationevents(_:))

### Deprecated gestures

- [MagnificationGesture](/documentation/swiftui/magnificationgesture)

#### Creating the gesture

- [init(minimumScaleDelta: CGFloat)](/documentation/swiftui/magnificationgesture/init(minimumscaledelta:))
- [var minimumScaleDelta: CGFloat](/documentation/swiftui/magnificationgesture/minimumscaledelta)
- [RotationGesture](/documentation/swiftui/rotationgesture)

#### Creating the gesture

- [init(minimumAngleDelta: Angle)](/documentation/swiftui/rotationgesture/init(minimumangledelta:))
- [var minimumAngleDelta: Angle](/documentation/swiftui/rotationgesture/minimumangledelta)
- [Input events](/documentation/swiftui/input-events)

### Responding to keyboard input

- [func onKeyPress(KeyEquivalent, action: () -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(_:action:))
- [func onKeyPress(phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(phases:action:))
- [func onKeyPress(KeyEquivalent, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(_:phases:action:))
- [func onKeyPress(characters: CharacterSet, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(characters:phases:action:))
- [func onKeyPress(keys: Set<KeyEquivalent>, phases: KeyPress.Phases, action: (KeyPress) -> KeyPress.Result) -> some View](/documentation/swiftui/view/onkeypress(keys:phases:action:))
- [KeyPress](/documentation/swiftui/keypress)

#### Getting the keypress

- [let key: KeyEquivalent](/documentation/swiftui/keypress/key)
- [let characters: String](/documentation/swiftui/keypress/characters)
- [let modifiers: EventModifiers](/documentation/swiftui/keypress/modifiers)

#### Getting the phase of the keypress

- [let phase: KeyPress.Phases](/documentation/swiftui/keypress/phase)
- [KeyPress.Phases](/documentation/swiftui/keypress/phases)

##### Getting the phases

- [static let down: KeyPress.Phases](/documentation/swiftui/keypress/phases/down)
- [static let up: KeyPress.Phases](/documentation/swiftui/keypress/phases/up)
- [static let `repeat`: KeyPress.Phases](/documentation/swiftui/keypress/phases/repeat)
- [static let all: KeyPress.Phases](/documentation/swiftui/keypress/phases/all)

#### Getting the result

- [KeyPress.Result](/documentation/swiftui/keypress/result)

##### Getting the result

- [case handled](/documentation/swiftui/keypress/result/handled)
- [case ignored](/documentation/swiftui/keypress/result/ignored)

### Creating keyboard shortcuts

- [func keyboardShortcut(_:)](/documentation/swiftui/view/keyboardshortcut(_:))
- [func keyboardShortcut(KeyEquivalent, modifiers: EventModifiers) -> some View](/documentation/swiftui/view/keyboardshortcut(_:modifiers:))
- [func keyboardShortcut(KeyEquivalent, modifiers: EventModifiers, localization: KeyboardShortcut.Localization) -> some View](/documentation/swiftui/view/keyboardshortcut(_:modifiers:localization:))
- [var keyboardShortcut: KeyboardShortcut?](/documentation/swiftui/environmentvalues/keyboardshortcut)
- [KeyboardShortcut](/documentation/swiftui/keyboardshortcut)

#### Getting standard shortcuts

- [static let cancelAction: KeyboardShortcut](/documentation/swiftui/keyboardshortcut/cancelaction)
- [static let defaultAction: KeyboardShortcut](/documentation/swiftui/keyboardshortcut/defaultaction)

#### Creating a shortcut

- [init(KeyEquivalent, modifiers: EventModifiers)](/documentation/swiftui/keyboardshortcut/init(_:modifiers:))
- [var key: KeyEquivalent](/documentation/swiftui/keyboardshortcut/key)
- [var modifiers: EventModifiers](/documentation/swiftui/keyboardshortcut/modifiers)

#### Creating a localized shortcut

- [init(KeyEquivalent, modifiers: EventModifiers, localization: KeyboardShortcut.Localization)](/documentation/swiftui/keyboardshortcut/init(_:modifiers:localization:))
- [var localization: KeyboardShortcut.Localization](/documentation/swiftui/keyboardshortcut/localization-swift.property)
- [KeyboardShortcut.Localization](/documentation/swiftui/keyboardshortcut/localization-swift.struct)

##### Getting localization strategies

- [static let automatic: KeyboardShortcut.Localization](/documentation/swiftui/keyboardshortcut/localization-swift.struct/automatic)
- [static let custom: KeyboardShortcut.Localization](/documentation/swiftui/keyboardshortcut/localization-swift.struct/custom)
- [static let withoutMirroring: KeyboardShortcut.Localization](/documentation/swiftui/keyboardshortcut/localization-swift.struct/withoutmirroring)
- [KeyEquivalent](/documentation/swiftui/keyequivalent)

#### Getting arrow keys

- [static let upArrow: KeyEquivalent](/documentation/swiftui/keyequivalent/uparrow)
- [static let downArrow: KeyEquivalent](/documentation/swiftui/keyequivalent/downarrow)
- [static let leftArrow: KeyEquivalent](/documentation/swiftui/keyequivalent/leftarrow)
- [static let rightArrow: KeyEquivalent](/documentation/swiftui/keyequivalent/rightarrow)

#### Getting other special keys

- [static let clear: KeyEquivalent](/documentation/swiftui/keyequivalent/clear)
- [static let delete: KeyEquivalent](/documentation/swiftui/keyequivalent/delete)
- [static let deleteForward: KeyEquivalent](/documentation/swiftui/keyequivalent/deleteforward)
- [static let end: KeyEquivalent](/documentation/swiftui/keyequivalent/end)
- [static let escape: KeyEquivalent](/documentation/swiftui/keyequivalent/escape)
- [static let home: KeyEquivalent](/documentation/swiftui/keyequivalent/home)
- [static let pageDown: KeyEquivalent](/documentation/swiftui/keyequivalent/pagedown)
- [static let pageUp: KeyEquivalent](/documentation/swiftui/keyequivalent/pageup)
- [static let `return`: KeyEquivalent](/documentation/swiftui/keyequivalent/return)
- [static let space: KeyEquivalent](/documentation/swiftui/keyequivalent/space)
- [static let tab: KeyEquivalent](/documentation/swiftui/keyequivalent/tab)

#### Creating a key equivalent

- [init(Character)](/documentation/swiftui/keyequivalent/init(_:))
- [var character: Character](/documentation/swiftui/keyequivalent/character)
- [EventModifiers](/documentation/swiftui/eventmodifiers)

#### Getting modifier keys

- [static let all: EventModifiers](/documentation/swiftui/eventmodifiers/all)
- [static let capsLock: EventModifiers](/documentation/swiftui/eventmodifiers/capslock)
- [static let command: EventModifiers](/documentation/swiftui/eventmodifiers/command)
- [static let control: EventModifiers](/documentation/swiftui/eventmodifiers/control)
- [static let numericPad: EventModifiers](/documentation/swiftui/eventmodifiers/numericpad)
- [static let option: EventModifiers](/documentation/swiftui/eventmodifiers/option)
- [static let shift: EventModifiers](/documentation/swiftui/eventmodifiers/shift)

#### Creating a set of options

- [init(rawValue: Int)](/documentation/swiftui/eventmodifiers/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/eventmodifiers/rawvalue)

#### Deprecated modifiers

- [static let function: EventModifiers](/documentation/swiftui/eventmodifiers/function)

### Responding to modifier keys

- [func onModifierKeysChanged(mask: EventModifiers, initial: Bool, (EventModifiers, EventModifiers) -> Void) -> some View](/documentation/swiftui/view/onmodifierkeyschanged(mask:initial:_:))
- [func modifierKeyAlternate<V>(EventModifiers, () -> V) -> some View](/documentation/swiftui/view/modifierkeyalternate(_:_:))

### Responding to hover events

- [func onHover(perform: (Bool) -> Void) -> some View](/documentation/swiftui/view/onhover(perform:))
- [func onContinuousHover(coordinateSpace:perform:)](/documentation/swiftui/view/oncontinuoushover(coordinatespace:perform:))
- [func hoverEffect(_:isEnabled:)](/documentation/swiftui/view/hovereffect(_:isenabled:))
- [func hoverEffectDisabled(Bool) -> some View](/documentation/swiftui/view/hovereffectdisabled(_:))
- [func defaultHoverEffect(_:)](/documentation/swiftui/view/defaulthovereffect(_:))
- [var isHoverEffectEnabled: Bool](/documentation/swiftui/environmentvalues/ishovereffectenabled)
- [HoverPhase](/documentation/swiftui/hoverphase)

#### Getting hover phases

- [case active(CGPoint)](/documentation/swiftui/hoverphase/active(_:))
- [case ended](/documentation/swiftui/hoverphase/ended)
- [HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride)

#### Type Properties

- [static var active: HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/active)
- [static var inactive: HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/inactive)

#### Type Methods

- [static func activeTemporarily(trigger: some Equatable) -> HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/activetemporarily(trigger:))
- [static func inactiveTemporarily(trigger: some Equatable) -> HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/inactivetemporarily(trigger:))
- [static func toggled(trigger: some Equatable) -> HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/toggled(trigger:))
- [static func toggledTemporarily(trigger: some Equatable) -> HoverEffectPhaseOverride](/documentation/swiftui/hovereffectphaseoverride/toggledtemporarily(trigger:))
- [OrnamentHoverContentEffect](/documentation/swiftui/ornamenthovercontenteffect)
- [OrnamentHoverEffect](/documentation/swiftui/ornamenthovereffect)

### Modifying pointer appearance

- [func pointerStyle(PointerStyle?) -> some View](/documentation/swiftui/view/pointerstyle(_:))
- [PointerStyle](/documentation/swiftui/pointerstyle)

#### Getting built-in pointer styles

- [static let `default`: PointerStyle](/documentation/swiftui/pointerstyle/default)
- [static let horizontalText: PointerStyle](/documentation/swiftui/pointerstyle/horizontaltext)
- [static let verticalText: PointerStyle](/documentation/swiftui/pointerstyle/verticaltext)
- [static let rectSelection: PointerStyle](/documentation/swiftui/pointerstyle/rectselection)
- [static let grabIdle: PointerStyle](/documentation/swiftui/pointerstyle/grabidle)
- [static let grabActive: PointerStyle](/documentation/swiftui/pointerstyle/grabactive)
- [static let link: PointerStyle](/documentation/swiftui/pointerstyle/link)
- [static let zoomIn: PointerStyle](/documentation/swiftui/pointerstyle/zoomin)
- [static let zoomOut: PointerStyle](/documentation/swiftui/pointerstyle/zoomout)
- [static func frameResize(position: FrameResizePosition, directions: FrameResizeDirection.Set) -> PointerStyle](/documentation/swiftui/pointerstyle/frameresize(position:directions:))
- [static func columnResize(directions: HorizontalDirection.Set) -> PointerStyle](/documentation/swiftui/pointerstyle/columnresize(directions:))
- [static func rowResize(directions: VerticalDirection.Set) -> PointerStyle](/documentation/swiftui/pointerstyle/rowresize(directions:))

#### Creating custom pointer styles

- [static image(_:hotSpot:)](/documentation/swiftui/pointerstyle/image(_:hotspot:))
- [static func shape(some Shape, eoFill: Bool, size: CGSize) -> PointerStyle](/documentation/swiftui/pointerstyle/shape(_:eofill:size:))

#### Supporting types

- [HorizontalDirection](/documentation/swiftui/horizontaldirection)

##### Structures

- [HorizontalDirection.Set](/documentation/swiftui/horizontaldirection/set)

###### Initializers

- [init(HorizontalDirection)](/documentation/swiftui/horizontaldirection/set/init(_:))

###### Type Properties

- [static let all: HorizontalDirection.Set](/documentation/swiftui/horizontaldirection/set/all)
- [static let leading: HorizontalDirection.Set](/documentation/swiftui/horizontaldirection/set/leading)
- [static let trailing: HorizontalDirection.Set](/documentation/swiftui/horizontaldirection/set/trailing)

##### Enumeration Cases

- [case leading](/documentation/swiftui/horizontaldirection/leading)
- [case trailing](/documentation/swiftui/horizontaldirection/trailing)
- [VerticalDirection](/documentation/swiftui/verticaldirection)

##### Structures

- [VerticalDirection.Set](/documentation/swiftui/verticaldirection/set)

###### Initializers

- [init(VerticalDirection)](/documentation/swiftui/verticaldirection/set/init(_:))

###### Type Properties

- [static let all: VerticalDirection.Set](/documentation/swiftui/verticaldirection/set/all)
- [static let down: VerticalDirection.Set](/documentation/swiftui/verticaldirection/set/down)
- [static let up: VerticalDirection.Set](/documentation/swiftui/verticaldirection/set/up)

##### Enumeration Cases

- [case down](/documentation/swiftui/verticaldirection/down)
- [case up](/documentation/swiftui/verticaldirection/up)
- [FrameResizePosition](/documentation/swiftui/frameresizeposition)

##### Enumeration Cases

- [case bottom](/documentation/swiftui/frameresizeposition/bottom)
- [case bottomLeading](/documentation/swiftui/frameresizeposition/bottomleading)
- [case bottomTrailing](/documentation/swiftui/frameresizeposition/bottomtrailing)
- [case leading](/documentation/swiftui/frameresizeposition/leading)
- [case top](/documentation/swiftui/frameresizeposition/top)
- [case topLeading](/documentation/swiftui/frameresizeposition/topleading)
- [case topTrailing](/documentation/swiftui/frameresizeposition/toptrailing)
- [case trailing](/documentation/swiftui/frameresizeposition/trailing)
- [FrameResizeDirection](/documentation/swiftui/frameresizedirection)

##### Structures

- [FrameResizeDirection.Set](/documentation/swiftui/frameresizedirection/set)

###### Initializers

- [init(FrameResizeDirection)](/documentation/swiftui/frameresizedirection/set/init(_:))

###### Type Properties

- [static let all: FrameResizeDirection.Set](/documentation/swiftui/frameresizedirection/set/all)
- [static let inward: FrameResizeDirection.Set](/documentation/swiftui/frameresizedirection/set/inward)
- [static let outward: FrameResizeDirection.Set](/documentation/swiftui/frameresizedirection/set/outward)

##### Enumeration Cases

- [case inward](/documentation/swiftui/frameresizedirection/inward)
- [case outward](/documentation/swiftui/frameresizedirection/outward)

#### Type Properties

- [static let columnResize: PointerStyle](/documentation/swiftui/pointerstyle/columnresize)
- [static let rowResize: PointerStyle](/documentation/swiftui/pointerstyle/rowresize)
- [func pointerVisibility(Visibility) -> some View](/documentation/swiftui/view/pointervisibility(_:))

### Changing view appearance for hover events

- [func hoverEffect(HoverEffect) -> some View](/documentation/swiftui/view/hovereffect(_:))
- [HoverEffect](/documentation/swiftui/hovereffect)

#### Getting hover effects

- [static let automatic: HoverEffect](/documentation/swiftui/hovereffect/automatic)
- [static let highlight: HoverEffect](/documentation/swiftui/hovereffect/highlight)
- [static let lift: HoverEffect](/documentation/swiftui/hovereffect/lift)

#### Initializers

- [init<E>(E)](/documentation/swiftui/hovereffect/init(_:))
- [func hoverEffect(some CustomHoverEffect, in: HoverEffectGroup?, isEnabled: Bool) -> some View](/documentation/swiftui/view/hovereffect(_:in:isenabled:))
- [func hoverEffect(in: HoverEffectGroup?, isEnabled: Bool, body: (EmptyHoverEffectContent, Bool, GeometryProxy) -> some HoverEffectContent) -> some View](/documentation/swiftui/view/hovereffect(in:isenabled:body:))
- [CustomHoverEffect](/documentation/swiftui/customhovereffect)

#### Getting built-in hover effects

- [static var automatic: AutomaticHoverEffect](/documentation/swiftui/customhovereffect/automatic)
- [static var empty: EmptyHoverEffect](/documentation/swiftui/customhovereffect/empty)
- [static var highlight: HighlightHoverEffect](/documentation/swiftui/customhovereffect/highlight)
- [static var lift: LiftHoverEffect](/documentation/swiftui/customhovereffect/lift)

#### Creating custom hover effects

- [func hoverEffect(some CustomHoverEffect, in: HoverEffectGroup?, isEnabled: Bool) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffect(_:in:isenabled:))
- [func hoverEffect(in: HoverEffectGroup?, isEnabled: Bool, body: (EmptyHoverEffectContent, Bool, GeometryProxy) -> some HoverEffectContent) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffect(in:isenabled:body:)-swift.method)
- [func hoverEffectGroup(HoverEffectGroup?) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffectgroup(_:)-swift.method)
- [func hoverEffectGroup(id: String?, in: Namespace.ID, behavior: HoverEffectGroup.Behavior) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffectgroup(id:in:behavior:)-swift.method)
- [func hoverEffectDisabled(Bool) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffectdisabled(_:))

#### Supporting types

- [AutomaticHoverEffect](/documentation/swiftui/automatichovereffect)

##### Initializers

- [init()](/documentation/swiftui/automatichovereffect/init())
- [EmptyHoverEffect](/documentation/swiftui/emptyhovereffect)
- [HighlightHoverEffect](/documentation/swiftui/highlighthovereffect)

##### Initializers

- [init()](/documentation/swiftui/highlighthovereffect/init())
- [LiftHoverEffect](/documentation/swiftui/lifthovereffect)

##### Initializers

- [init()](/documentation/swiftui/lifthovereffect/init())

#### Associated Types

- [Body](/documentation/swiftui/customhovereffect/body)

#### Instance Methods

- [func body(content: Self.Content) -> Self.Body](/documentation/swiftui/customhovereffect/body(content:))
- [func hoverEffectPhaseOverride(HoverEffectPhaseOverride?) -> some CustomHoverEffect](/documentation/swiftui/customhovereffect/hovereffectphaseoverride(_:))

#### Type Aliases

- [CustomHoverEffect.Content](/documentation/swiftui/customhovereffect/content)

#### Type Methods

- [static func hoverEffect<C>(in: HoverEffectGroup?, isEnabled: Bool, body: (EmptyHoverEffectContent, Bool, GeometryProxy) -> C) -> ContentHoverEffect<C>](/documentation/swiftui/customhovereffect/hovereffect(in:isenabled:body:)-swift.type.method)
- [static func hoverEffectGroup(HoverEffectGroup?) -> GroupHoverEffect](/documentation/swiftui/customhovereffect/hovereffectgroup(_:)-swift.type.method)
- [static func hoverEffectGroup(id: String?, in: Namespace.ID, behavior: HoverEffectGroup.Behavior) -> GroupHoverEffect](/documentation/swiftui/customhovereffect/hovereffectgroup(id:in:behavior:)-swift.type.method)
- [static func ornament<Content>(attachmentAnchor: OrnamentAttachmentAnchor, contentAlignment: Alignment3D, ornament: () -> Content) -> OrnamentHoverEffect<Content>](/documentation/swiftui/customhovereffect/ornament(attachmentanchor:contentalignment:ornament:))
- [static func ornament<Content, EffectContent>(attachmentAnchor: OrnamentAttachmentAnchor, contentAlignment: Alignment3D, ornament: () -> Content, effect: (EmptyHoverEffectContent, Bool, GeometryProxy) -> EffectContent) -> OrnamentHoverContentEffect<Content, EffectContent>](/documentation/swiftui/customhovereffect/ornament(attachmentanchor:contentalignment:ornament:effect:))
- [ContentHoverEffect](/documentation/swiftui/contenthovereffect)
- [HoverEffectGroup](/documentation/swiftui/hovereffectgroup)

#### Structures

- [HoverEffectGroup.Behavior](/documentation/swiftui/hovereffectgroup/behavior)

##### Type Properties

- [static let activatesGroup: HoverEffectGroup.Behavior](/documentation/swiftui/hovereffectgroup/behavior/activatesgroup)
- [static let followsGroup: HoverEffectGroup.Behavior](/documentation/swiftui/hovereffectgroup/behavior/followsgroup)
- [static let ignoresGroup: HoverEffectGroup.Behavior](/documentation/swiftui/hovereffectgroup/behavior/ignoresgroup)
- [static let preservesGroup: HoverEffectGroup.Behavior](/documentation/swiftui/hovereffectgroup/behavior/preservesgroup)

#### Initializers

- [init(Namespace.ID, behavior: HoverEffectGroup.Behavior)](/documentation/swiftui/hovereffectgroup/init(_:behavior:))
- [init(id: String?, in: Namespace.ID, behavior: HoverEffectGroup.Behavior)](/documentation/swiftui/hovereffectgroup/init(id:in:behavior:))

#### Instance Methods

- [func behavior(HoverEffectGroup.Behavior) -> HoverEffectGroup](/documentation/swiftui/hovereffectgroup/behavior(_:))

#### Type Properties

- [static var systemOverlays: HoverEffectGroup](/documentation/swiftui/hovereffectgroup/systemoverlays)
- [func hoverEffectGroup() -> some View](/documentation/swiftui/view/hovereffectgroup())
- [func hoverEffectGroup(HoverEffectGroup?) -> some View](/documentation/swiftui/view/hovereffectgroup(_:))
- [func hoverEffectGroup(id: String?, in: Namespace.ID, behavior: HoverEffectGroup.Behavior) -> some View](/documentation/swiftui/view/hovereffectgroup(id:in:behavior:))
- [GroupHoverEffect](/documentation/swiftui/grouphovereffect)
- [HoverEffectContent](/documentation/swiftui/hovereffectcontent)

#### Instance Methods

- [func animation(Animation?, body: (EmptyHoverEffectContent) -> some HoverEffectContent) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/animation(_:body:))
- [func clipShape<S>(S, style: FillStyle) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/clipshape(_:style:))
- [func offset(CGSize) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/offset(_:))
- [func offset(x: CGFloat, y: CGFloat) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/offset(x:y:))
- [func opacity(Double) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/opacity(_:))
- [func rotationEffect(Angle, anchor: UnitPoint) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/rotationeffect(_:anchor:))
- [func scaleEffect(_:anchor:)](/documentation/swiftui/hovereffectcontent/scaleeffect(_:anchor:))
- [func scaleEffect(x: CGFloat, y: CGFloat, anchor: UnitPoint) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/scaleeffect(x:y:anchor:))
- [func transformEffect(CGAffineTransform) -> some HoverEffectContent](/documentation/swiftui/hovereffectcontent/transformeffect(_:))
- [EmptyHoverEffectContent](/documentation/swiftui/emptyhovereffectcontent)
- [func handPointerBehavior(HandPointerBehavior?) -> some View](/documentation/swiftui/view/handpointerbehavior(_:))
- [HandPointerBehavior](/documentation/swiftui/handpointerbehavior)

#### Type Properties

- [static let drawing: HandPointerBehavior](/documentation/swiftui/handpointerbehavior/drawing)
- [static let inactive: HandPointerBehavior](/documentation/swiftui/handpointerbehavior/inactive)

### Responding to submission events

- [func onSubmit(of: SubmitTriggers, () -> Void) -> some View](/documentation/swiftui/view/onsubmit(of:_:))
- [func submitScope(Bool) -> some View](/documentation/swiftui/view/submitscope(_:))
- [SubmitTriggers](/documentation/swiftui/submittriggers)

#### Getting submit triggers

- [static let search: SubmitTriggers](/documentation/swiftui/submittriggers/search)
- [static let text: SubmitTriggers](/documentation/swiftui/submittriggers/text)

#### Creating a set of options

- [init(rawValue: SubmitTriggers.RawValue)](/documentation/swiftui/submittriggers/init(rawvalue:))

### Labeling a submission event

- [func submitLabel(SubmitLabel) -> some View](/documentation/swiftui/view/submitlabel(_:))
- [SubmitLabel](/documentation/swiftui/submitlabel)

#### Getting submission labels

- [static var `continue`: SubmitLabel](/documentation/swiftui/submitlabel/continue)
- [static var done: SubmitLabel](/documentation/swiftui/submitlabel/done)
- [static var go: SubmitLabel](/documentation/swiftui/submitlabel/go)
- [static var join: SubmitLabel](/documentation/swiftui/submitlabel/join)
- [static var next: SubmitLabel](/documentation/swiftui/submitlabel/next)
- [static var `return`: SubmitLabel](/documentation/swiftui/submitlabel/return)
- [static var route: SubmitLabel](/documentation/swiftui/submitlabel/route)
- [static var search: SubmitLabel](/documentation/swiftui/submitlabel/search)
- [static var send: SubmitLabel](/documentation/swiftui/submitlabel/send)

### Responding to commands

- [func onMoveCommand(perform: ((MoveCommandDirection) -> Void)?) -> some View](/documentation/swiftui/view/onmovecommand(perform:))
- [func onDeleteCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/ondeletecommand(perform:))
- [func pageCommand<V>(value: Binding<V>, in: ClosedRange<V>, step: V) -> some View](/documentation/swiftui/view/pagecommand(value:in:step:))
- [func onExitCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onexitcommand(perform:))
- [func onPlayPauseCommand(perform: (() -> Void)?) -> some View](/documentation/swiftui/view/onplaypausecommand(perform:))
- [func onCommand(Selector, perform: (() -> Void)?) -> some View](/documentation/swiftui/view/oncommand(_:perform:))
- [MoveCommandDirection](/documentation/swiftui/movecommanddirection)

#### Getting move command directions

- [case up](/documentation/swiftui/movecommanddirection/up)
- [case down](/documentation/swiftui/movecommanddirection/down)
- [case left](/documentation/swiftui/movecommanddirection/left)
- [case right](/documentation/swiftui/movecommanddirection/right)

### Controlling hit testing

- [func allowsTightening(Bool) -> some View](/documentation/swiftui/view/allowstightening(_:))
- [func contentShape<S>(S, eoFill: Bool) -> some View](/documentation/swiftui/view/contentshape(_:eofill:))
- [func contentShape<S>(ContentShapeKinds, S, eoFill: Bool) -> some View](/documentation/swiftui/view/contentshape(_:_:eofill:))
- [ContentShapeKinds](/documentation/swiftui/contentshapekinds)

#### Getting shape kinds

- [static let interaction: ContentShapeKinds](/documentation/swiftui/contentshapekinds/interaction)
- [static let dragPreview: ContentShapeKinds](/documentation/swiftui/contentshapekinds/dragpreview)
- [static let contextMenuPreview: ContentShapeKinds](/documentation/swiftui/contentshapekinds/contextmenupreview)
- [static let focusEffect: ContentShapeKinds](/documentation/swiftui/contentshapekinds/focuseffect)
- [static let hoverEffect: ContentShapeKinds](/documentation/swiftui/contentshapekinds/hovereffect)
- [static let accessibility: ContentShapeKinds](/documentation/swiftui/contentshapekinds/accessibility)

#### Creating a set of options

- [init(rawValue: Int)](/documentation/swiftui/contentshapekinds/init(rawvalue:))

### Interacting with the Digital Crown

- [func digitalCrownAccessory(Visibility) -> some View](/documentation/swiftui/view/digitalcrownaccessory(_:))
- [func digitalCrownAccessory<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/digitalcrownaccessory(content:))
- [func digitalCrownRotation<V>(Binding<V>, from: V, through: V, sensitivity: DigitalCrownRotationalSensitivity, isContinuous: Bool, isHapticFeedbackEnabled: Bool, onChange: (DigitalCrownEvent) -> Void, onIdle: () -> Void) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:from:through:sensitivity:iscontinuous:ishapticfeedbackenabled:onchange:onidle:))
- [func digitalCrownRotation<V>(Binding<V>, onChange: (DigitalCrownEvent) -> Void, onIdle: () -> Void) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:onchange:onidle:))
- [func digitalCrownRotation(detent:from:through:by:sensitivity:isContinuous:isHapticFeedbackEnabled:onChange:onIdle:)](/documentation/swiftui/view/digitalcrownrotation(detent:from:through:by:sensitivity:iscontinuous:ishapticfeedbackenabled:onchange:onidle:))
- [func digitalCrownRotation<V>(Binding<V>) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:))
- [func digitalCrownRotation<V>(Binding<V>, from: V, through: V, by: V.Stride?, sensitivity: DigitalCrownRotationalSensitivity, isContinuous: Bool, isHapticFeedbackEnabled: Bool) -> some View](/documentation/swiftui/view/digitalcrownrotation(_:from:through:by:sensitivity:iscontinuous:ishapticfeedbackenabled:))
- [DigitalCrownEvent](/documentation/swiftui/digitalcrownevent)

#### Getting events

- [var offset: Double](/documentation/swiftui/digitalcrownevent/offset)
- [var velocity: Double](/documentation/swiftui/digitalcrownevent/velocity)
- [DigitalCrownRotationalSensitivity](/documentation/swiftui/digitalcrownrotationalsensitivity)

#### Getting sensitivity options

- [case low](/documentation/swiftui/digitalcrownrotationalsensitivity/low)
- [case medium](/documentation/swiftui/digitalcrownrotationalsensitivity/medium)
- [case high](/documentation/swiftui/digitalcrownrotationalsensitivity/high)

### Managing Touch Bar input

- [func touchBar<Content>(content: () -> Content) -> some View](/documentation/swiftui/view/touchbar(content:))
- [func touchBar<Content>(TouchBar<Content>) -> some View](/documentation/swiftui/view/touchbar(_:))
- [func touchBarItemPrincipal(Bool) -> some View](/documentation/swiftui/view/touchbaritemprincipal(_:))
- [func touchBarCustomizationLabel(Text) -> some View](/documentation/swiftui/view/touchbarcustomizationlabel(_:))
- [func touchBarItemPresence(TouchBarItemPresence) -> some View](/documentation/swiftui/view/touchbaritempresence(_:))
- [TouchBar](/documentation/swiftui/touchbar)

#### Creating a Touch Bar view

- [init(content: () -> Content)](/documentation/swiftui/touchbar/init(content:))
- [init(id: String, content: () -> Content)](/documentation/swiftui/touchbar/init(id:content:))
- [TouchBarItemPresence](/documentation/swiftui/touchbaritempresence)

#### Getting presence options

- [case `default`(String)](/documentation/swiftui/touchbaritempresence/default(_:))
- [case optional(String)](/documentation/swiftui/touchbaritempresence/optional(_:))
- [case required(String)](/documentation/swiftui/touchbaritempresence/required(_:))

### Responding to capture events

- [func onCameraCaptureEvent(isEnabled: Bool, action: (AVCaptureEvent) -> Void) -> some View](/documentation/swiftui/view/oncameracaptureevent(isenabled:action:))
- [func onCameraCaptureEvent(isEnabled: Bool, primaryAction: (AVCaptureEvent) -> Void, secondaryAction: (AVCaptureEvent) -> Void) -> some View](/documentation/swiftui/view/oncameracaptureevent(isenabled:primaryaction:secondaryaction:))
- [Clipboard](/documentation/swiftui/clipboard)

### Copying transferable items

- [func copyable<T>(@autoclosure () -> [T]) -> some View](/documentation/swiftui/view/copyable(_:))
- [func cuttable<T>(for: T.Type, action: () -> [T]) -> some View](/documentation/swiftui/view/cuttable(for:action:))
- [func pasteDestination<T>(for: T.Type, action: ([T]) -> Void, validator: ([T]) -> [T]) -> some View](/documentation/swiftui/view/pastedestination(for:action:validator:))

### Copying items using item providers

- [func onCopyCommand(perform: (() -> [NSItemProvider])?) -> some View](/documentation/swiftui/view/oncopycommand(perform:))
- [func onCutCommand(perform: (() -> [NSItemProvider])?) -> some View](/documentation/swiftui/view/oncutcommand(perform:))
- [func onPasteCommand(of:perform:)](/documentation/swiftui/view/onpastecommand(of:perform:))
- [func onPasteCommand(of:validator:perform:)](/documentation/swiftui/view/onpastecommand(of:validator:perform:))
- [Drag and drop](/documentation/swiftui/drag-and-drop)

### Essentials

- [Adopting drag and drop using SwiftUI](/documentation/swiftui/adopting-drag-and-drop-using-swiftui)
- [Making a view into a drag source](/documentation/swiftui/making-a-view-into-a-drag-source)

### Configuring drag and drop behavior

- [DragConfiguration](/documentation/swiftui/dragconfiguration)

#### Structures

- [DragConfiguration.OperationsOutsideApp](/documentation/swiftui/dragconfiguration/operationsoutsideapp-swift.struct)

##### Initializers

- [init(allowCopy: Bool)](/documentation/swiftui/dragconfiguration/operationsoutsideapp-swift.struct/init(allowcopy:))
- [init(allowCopy: Bool, allowMove: Bool, allowDelete: Bool)](/documentation/swiftui/dragconfiguration/operationsoutsideapp-swift.struct/init(allowcopy:allowmove:allowdelete:))

##### Instance Properties

- [var allowAlias: Bool](/documentation/swiftui/dragconfiguration/operationsoutsideapp-swift.struct/allowalias)
- [DragConfiguration.OperationsWithinApp](/documentation/swiftui/dragconfiguration/operationswithinapp-swift.struct)

##### Initializers

- [init(allowCopy: Bool, allowMove: Bool, allowDelete: Bool)](/documentation/swiftui/dragconfiguration/operationswithinapp-swift.struct/init(allowcopy:allowmove:allowdelete:))
- [init(allowMove: Bool)](/documentation/swiftui/dragconfiguration/operationswithinapp-swift.struct/init(allowmove:))

##### Instance Properties

- [var allowAlias: Bool](/documentation/swiftui/dragconfiguration/operationswithinapp-swift.struct/allowalias)

#### Initializers

- [init(allowMove: Bool)](/documentation/swiftui/dragconfiguration/init(allowmove:))
- [init(allowMove: Bool, allowDelete: Bool)](/documentation/swiftui/dragconfiguration/init(allowmove:allowdelete:))
- [init(operationsWithinApp: DragConfiguration.OperationsWithinApp, operationsOutsideApp: DragConfiguration.OperationsOutsideApp)](/documentation/swiftui/dragconfiguration/init(operationswithinapp:operationsoutsideapp:))

#### Instance Properties

- [var operationsOutsideApp: DragConfiguration.OperationsOutsideApp](/documentation/swiftui/dragconfiguration/operationsoutsideapp-swift.property)
- [var operationsWithinApp: DragConfiguration.OperationsWithinApp](/documentation/swiftui/dragconfiguration/operationswithinapp-swift.property)
- [DropConfiguration](/documentation/swiftui/dropconfiguration)

#### Initializers

- [init(operation: DropOperation)](/documentation/swiftui/dropconfiguration/init(operation:))

#### Instance Properties

- [var acceptedItemCount: Int?](/documentation/swiftui/dropconfiguration/accepteditemcount)
- [var operation: DropOperation](/documentation/swiftui/dropconfiguration/operation)

### Moving items

- [DragSession](/documentation/swiftui/dragsession)

#### Structures

- [DragSession.ID](/documentation/swiftui/dragsession/id-swift.struct)

##### Instance Methods

- [func matches(_:)](/documentation/swiftui/dragsession/id-swift.struct/matches(_:))

#### Instance Properties

- [var draggedItemIndex: Int](/documentation/swiftui/dragsession/draggeditemindex)
- [var id: DragSession.ID](/documentation/swiftui/dragsession/id-swift.property)
- [var location: CGPoint](/documentation/swiftui/dragsession/location)
- [var phase: DragSession.Phase](/documentation/swiftui/dragsession/phase-swift.property)

#### Instance Methods

- [func draggedItemIDs<ItemID>(for: ItemID.Type) -> [ItemID]](/documentation/swiftui/dragsession/draggeditemids(for:))

#### Enumerations

- [DragSession.Phase](/documentation/swiftui/dragsession/phase-swift.enum)

##### Enumeration Cases

- [case active](/documentation/swiftui/dragsession/phase-swift.enum/active)
- [case dataTransferCompleted](/documentation/swiftui/dragsession/phase-swift.enum/datatransfercompleted)
- [case ended(DropOperation)](/documentation/swiftui/dragsession/phase-swift.enum/ended(_:))
- [case ending(DropOperation)](/documentation/swiftui/dragsession/phase-swift.enum/ending(_:))
- [case initial](/documentation/swiftui/dragsession/phase-swift.enum/initial)
- [DropSession](/documentation/swiftui/dropsession)

#### Structures

- [DropSession.ID](/documentation/swiftui/dropsession/id-swift.struct)

##### Instance Methods

- [func matches(_:)](/documentation/swiftui/dropsession/id-swift.struct/matches(_:))
- [DropSession.LocalSession](/documentation/swiftui/dropsession/localsession-swift.struct)

##### Instance Methods

- [func draggedItemIDs<ItemID>(for: ItemID.Type) -> [ItemID]](/documentation/swiftui/dropsession/localsession-swift.struct/draggeditemids(for:))

#### Instance Properties

- [var id: DropSession.ID](/documentation/swiftui/dropsession/id-swift.property)
- [var itemsCount: Int](/documentation/swiftui/dropsession/itemscount)
- [var localSession: DropSession.LocalSession?](/documentation/swiftui/dropsession/localsession-swift.property)
- [var location: CGPoint](/documentation/swiftui/dropsession/location)
- [var phase: DropSession.Phase](/documentation/swiftui/dropsession/phase-swift.property)
- [var size: CGSize](/documentation/swiftui/dropsession/size)
- [var suggestedOperations: DropOperation.Set](/documentation/swiftui/dropsession/suggestedoperations)

#### Enumerations

- [DropSession.Phase](/documentation/swiftui/dropsession/phase-swift.enum)

##### Enumeration Cases

- [case active](/documentation/swiftui/dropsession/phase-swift.enum/active)
- [case dataTransferCompleted](/documentation/swiftui/dropsession/phase-swift.enum/datatransfercompleted)
- [case ended(DropOperation)](/documentation/swiftui/dropsession/phase-swift.enum/ended(_:))
- [case entering](/documentation/swiftui/dropsession/phase-swift.enum/entering)
- [case exiting](/documentation/swiftui/dropsession/phase-swift.enum/exiting)

### Moving transferable items

- [func draggable<T>(@autoclosure () -> T) -> some View](/documentation/swiftui/view/draggable(_:))
- [func draggable<V, T>(@autoclosure () -> T, preview: () -> V) -> some View](/documentation/swiftui/view/draggable(_:preview:))
- [func dropDestination<T>(for: T.Type, action: ([T], CGPoint) -> Bool, isTargeted: (Bool) -> Void) -> some View](/documentation/swiftui/view/dropdestination(for:action:istargeted:))

### Moving items using item providers

- [func itemProvider(Optional<() -> NSItemProvider?>) -> some View](/documentation/swiftui/view/itemprovider(_:))
- [func onDrag<V>(() -> NSItemProvider, preview: () -> V) -> some View](/documentation/swiftui/view/ondrag(_:preview:))
- [func onDrag(() -> NSItemProvider) -> some View](/documentation/swiftui/view/ondrag(_:))
- [func onDrop(of:isTargeted:perform:)](/documentation/swiftui/view/ondrop(of:istargeted:perform:))
- [func onDrop(of:delegate:)](/documentation/swiftui/view/ondrop(of:delegate:))
- [DropDelegate](/documentation/swiftui/dropdelegate)

#### Receiving drop information

- [func dropEntered(info: DropInfo)](/documentation/swiftui/dropdelegate/dropentered(info:))
- [func dropExited(info: DropInfo)](/documentation/swiftui/dropdelegate/dropexited(info:))
- [func dropUpdated(info: DropInfo) -> DropProposal?](/documentation/swiftui/dropdelegate/dropupdated(info:))
- [func validateDrop(info: DropInfo) -> Bool](/documentation/swiftui/dropdelegate/validatedrop(info:))
- [func performDrop(info: DropInfo) -> Bool](/documentation/swiftui/dropdelegate/performdrop(info:))
- [DropProposal](/documentation/swiftui/dropproposal)

#### Creating a drop proposal

- [init(operation: DropOperation)](/documentation/swiftui/dropproposal/init(operation:))
- [let operation: DropOperation](/documentation/swiftui/dropproposal/operation)

#### Initializers

- [init(withinApplication: DropOperation, outsideApplication: DropOperation)](/documentation/swiftui/dropproposal/init(withinapplication:outsideapplication:))

#### Instance Properties

- [let operationOutsideApplication: DropOperation?](/documentation/swiftui/dropproposal/operationoutsideapplication)
- [DropOperation](/documentation/swiftui/dropoperation)

#### Getting operation types

- [case cancel](/documentation/swiftui/dropoperation/cancel)
- [case copy](/documentation/swiftui/dropoperation/copy)
- [case forbidden](/documentation/swiftui/dropoperation/forbidden)
- [case move](/documentation/swiftui/dropoperation/move)

#### Structures

- [DropOperation.Set](/documentation/swiftui/dropoperation/set)

##### Initializers

- [init(rawValue: Int)](/documentation/swiftui/dropoperation/set/init(rawvalue:))

##### Type Properties

- [static let alias: DropOperation.Set](/documentation/swiftui/dropoperation/set/alias)
- [static let cancel: DropOperation.Set](/documentation/swiftui/dropoperation/set/cancel)
- [static let copy: DropOperation.Set](/documentation/swiftui/dropoperation/set/copy)
- [static let delete: DropOperation.Set](/documentation/swiftui/dropoperation/set/delete)
- [static let forbidden: DropOperation.Set](/documentation/swiftui/dropoperation/set/forbidden)
- [static let move: DropOperation.Set](/documentation/swiftui/dropoperation/set/move)

#### Enumeration Cases

- [case alias](/documentation/swiftui/dropoperation/alias)
- [case delete](/documentation/swiftui/dropoperation/delete)
- [DropInfo](/documentation/swiftui/dropinfo)

#### Getting the drop location

- [var location: CGPoint](/documentation/swiftui/dropinfo/location)

#### Checking for items

- [func hasItemsConforming(to: [UTType]) -> Bool](/documentation/swiftui/dropinfo/hasitemsconforming(to:)-47irh)
- [func itemProviders(for: [UTType]) -> [NSItemProvider]](/documentation/swiftui/dropinfo/itemproviders(for:)-93409)

#### Deprecated symbols

- [func hasItemsConforming(to: [String]) -> Bool](/documentation/swiftui/dropinfo/hasitemsconforming(to:)-4qeez)
- [func itemProviders(for: [String]) -> [NSItemProvider]](/documentation/swiftui/dropinfo/itemproviders(for:)-b6fo)

#### Instance Methods

- [func hasItemsConforming(to:)](/documentation/swiftui/dropinfo/hasitemsconforming(to:))
- [func itemProviders(for:)](/documentation/swiftui/dropinfo/itemproviders(for:))

### Describing preview formations

- [DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation)

#### Type Properties

- [static let `default`: DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation/default)
- [static let list: DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation/list)
- [static let none: DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation/none)
- [static let pile: DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation/pile)
- [static let stack: DragDropPreviewsFormation](/documentation/swiftui/dragdroppreviewsformation/stack)

### Configuring spring loading

- [func springLoadingBehavior(SpringLoadingBehavior) -> some View](/documentation/swiftui/view/springloadingbehavior(_:))
- [var springLoadingBehavior: SpringLoadingBehavior](/documentation/swiftui/environmentvalues/springloadingbehavior)
- [SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior)

#### Getting the behaviors

- [static let automatic: SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior/automatic)
- [static let enabled: SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior/enabled)
- [static let disabled: SpringLoadingBehavior](/documentation/swiftui/springloadingbehavior/disabled)
- [Focus](/documentation/swiftui/focus)

### Essentials

- [Focus Cookbook: Supporting and enhancing focus-driven interactions in your SwiftUI app](/documentation/swiftui/focus-cookbook-sample)

### Indicating that a view can receive focus

- [func focusable(Bool) -> some View](/documentation/swiftui/view/focusable(_:))
- [func focusable(Bool, interactions: FocusInteractions) -> some View](/documentation/swiftui/view/focusable(_:interactions:))
- [FocusInteractions](/documentation/swiftui/focusinteractions)

#### Creating the interaction types

- [static var automatic: FocusInteractions](/documentation/swiftui/focusinteractions/automatic)
- [static let activate: FocusInteractions](/documentation/swiftui/focusinteractions/activate)
- [static let edit: FocusInteractions](/documentation/swiftui/focusinteractions/edit)

### Managing focus state

- [func focused<Value>(FocusState<Value>.Binding, equals: Value) -> some View](/documentation/swiftui/view/focused(_:equals:))
- [func focused(FocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/focused(_:))
- [var isFocused: Bool](/documentation/swiftui/environmentvalues/isfocused)
- [FocusState](/documentation/swiftui/focusstate)

#### Creating a focus state

- [init()](/documentation/swiftui/focusstate/init())

#### Inspecting the focus state

- [var projectedValue: FocusState<Value>.Binding](/documentation/swiftui/focusstate/projectedvalue)
- [FocusState.Binding](/documentation/swiftui/focusstate/binding)

##### Inspecting the binding

- [var projectedValue: FocusState<Value>.Binding](/documentation/swiftui/focusstate/binding/projectedvalue)
- [var wrappedValue: Value](/documentation/swiftui/focusstate/binding/wrappedvalue)
- [var wrappedValue: Value](/documentation/swiftui/focusstate/wrappedvalue)
- [FocusedValue](/documentation/swiftui/focusedvalue)

#### Creating the value

- [init(_:)](/documentation/swiftui/focusedvalue/init(_:))

#### Getting the value

- [var wrappedValue: Value?](/documentation/swiftui/focusedvalue/wrappedvalue)
- [macro Entry()](/documentation/swiftui/entry())
- [FocusedValueKey](/documentation/swiftui/focusedvaluekey)

#### Specifying the value type

- [Value](/documentation/swiftui/focusedvaluekey/value)
- [FocusedBinding](/documentation/swiftui/focusedbinding)

#### Creating the binding

- [init(KeyPath<FocusedValues, Binding<Value>?>)](/documentation/swiftui/focusedbinding/init(_:))

#### Getting the value

- [var projectedValue: Binding<Value?>](/documentation/swiftui/focusedbinding/projectedvalue)
- [var wrappedValue: Value?](/documentation/swiftui/focusedbinding/wrappedvalue)
- [func searchFocused(FocusState<Bool>.Binding) -> some View](/documentation/swiftui/view/searchfocused(_:))
- [func searchFocused<V>(FocusState<V>.Binding, equals: V) -> some View](/documentation/swiftui/view/searchfocused(_:equals:))

### Exposing value types to focused views

- [func focusedValue<T>(T?) -> some View](/documentation/swiftui/view/focusedvalue(_:))
- [func focusedValue(_:_:)](/documentation/swiftui/view/focusedvalue(_:_:))
- [func focusedSceneValue<T>(T?) -> some View](/documentation/swiftui/view/focusedscenevalue(_:))
- [func focusedSceneValue(_:_:)](/documentation/swiftui/view/focusedscenevalue(_:_:))
- [FocusedValues](/documentation/swiftui/focusedvalues)

#### Getting the value for a key

- [subscript<Key>(Key.Type) -> Key.Value?](/documentation/swiftui/focusedvalues/subscript(_:))

### Exposing reference types to focused views

- [func focusedObject(_:)](/documentation/swiftui/view/focusedobject(_:))
- [func focusedSceneObject(_:)](/documentation/swiftui/view/focusedsceneobject(_:))
- [FocusedObject](/documentation/swiftui/focusedobject)

#### Creating the focused object

- [init()](/documentation/swiftui/focusedobject/init())

#### Getting the value

- [var projectedValue: FocusedObject<ObjectType>.Wrapper?](/documentation/swiftui/focusedobject/projectedvalue)
- [var wrappedValue: ObjectType?](/documentation/swiftui/focusedobject/wrappedvalue)
- [FocusedObject.Wrapper](/documentation/swiftui/focusedobject/wrapper)

##### Accessing members

- [subscript<T>(dynamicMember _: ReferenceWritableKeyPath<ObjectType, T>) -> Binding<T>](/documentation/swiftui/focusedobject/wrapper/subscript(dynamicmember:))

### Setting focus scope

- [func focusScope(Namespace.ID) -> some View](/documentation/swiftui/view/focusscope(_:))
- [func focusSection() -> some View](/documentation/swiftui/view/focussection())

### Controlling default focus

- [func prefersDefaultFocus(Bool, in: Namespace.ID) -> some View](/documentation/swiftui/view/prefersdefaultfocus(_:in:))
- [func defaultFocus<V>(FocusState<V>.Binding, V, priority: DefaultFocusEvaluationPriority) -> some View](/documentation/swiftui/view/defaultfocus(_:_:priority:))
- [DefaultFocusEvaluationPriority](/documentation/swiftui/defaultfocusevaluationpriority)

#### Getting the priorities

- [static let automatic: DefaultFocusEvaluationPriority](/documentation/swiftui/defaultfocusevaluationpriority/automatic)
- [static let userInitiated: DefaultFocusEvaluationPriority](/documentation/swiftui/defaultfocusevaluationpriority/userinitiated)

### Resetting focus

- [var resetFocus: ResetFocusAction](/documentation/swiftui/environmentvalues/resetfocus)
- [ResetFocusAction](/documentation/swiftui/resetfocusaction)

#### Calling the action

- [func callAsFunction(in: Namespace.ID)](/documentation/swiftui/resetfocusaction/callasfunction(in:))

### Configuring effects

- [func focusEffectDisabled(Bool) -> some View](/documentation/swiftui/view/focuseffectdisabled(_:))
- [var isFocusEffectEnabled: Bool](/documentation/swiftui/environmentvalues/isfocuseffectenabled)
- [System events](/documentation/swiftui/system-events)

### Sending and receiving user activities

- [Restoring your app’s state with SwiftUI](/documentation/swiftui/restoring-your-app-s-state-with-swiftui)
- [func userActivity<P>(String, element: P?, (P, NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/useractivity(_:element:_:))
- [func userActivity(String, isActive: Bool, (NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/useractivity(_:isactive:_:))
- [func onContinueUserActivity(String, perform: (NSUserActivity) -> ()) -> some View](/documentation/swiftui/view/oncontinueuseractivity(_:perform:))

### Sending and receiving URLs

- [var openURL: OpenURLAction](/documentation/swiftui/environmentvalues/openurl)
- [OpenURLAction](/documentation/swiftui/openurlaction)

#### Creating the action

- [init(handler: (URL) -> OpenURLAction.Result)](/documentation/swiftui/openurlaction/init(handler:))
- [OpenURLAction.Result](/documentation/swiftui/openurlaction/result)

##### Getting the results

- [static let discarded: OpenURLAction.Result](/documentation/swiftui/openurlaction/result/discarded)
- [static let handled: OpenURLAction.Result](/documentation/swiftui/openurlaction/result/handled)
- [static let systemAction: OpenURLAction.Result](/documentation/swiftui/openurlaction/result/systemaction)
- [static func systemAction(URL) -> OpenURLAction.Result](/documentation/swiftui/openurlaction/result/systemaction(_:))

##### Type Methods

- [static func systemAction(URL?, prefersInApp: Bool) -> OpenURLAction.Result](/documentation/swiftui/openurlaction/result/systemaction(_:prefersinapp:))

#### Calling the action

- [func callAsFunction(URL)](/documentation/swiftui/openurlaction/callasfunction(_:))
- [func callAsFunction(URL, completion: (Bool) -> Void)](/documentation/swiftui/openurlaction/callasfunction(_:completion:))

#### Instance Methods

- [func callAsFunction(URL, prefersInApp: Bool)](/documentation/swiftui/openurlaction/callasfunction(_:prefersinapp:))
- [func onOpenURL(perform: (URL) -> ()) -> some View](/documentation/swiftui/view/onopenurl(perform:))

### Handling external events

- [func handlesExternalEvents(matching: Set<String>) -> some Scene](/documentation/swiftui/scene/handlesexternalevents(matching:))
- [func handlesExternalEvents(preferring: Set<String>, allowing: Set<String>) -> some View](/documentation/swiftui/view/handlesexternalevents(preferring:allowing:))

### Handling background tasks

- [func backgroundTask<D, R>(BackgroundTask<D, R>, action: (D) async -> R) -> some Scene](/documentation/swiftui/scene/backgroundtask(_:action:))
- [BackgroundTask](/documentation/swiftui/backgroundtask)

#### Refreshing the app

- [static var appRefresh: BackgroundTask<String?, Void>](/documentation/swiftui/backgroundtask/apprefresh)
- [static func appRefresh(String) -> BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/apprefresh(_:))

#### Preparing for a snapshot

- [static var snapshot: BackgroundTask<SnapshotData, SnapshotResponse>](/documentation/swiftui/backgroundtask/snapshot)

#### Receiving connectivity updates

- [static var bluetoothAlert: BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/bluetoothalert)
- [static var watchConnectivity: BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/watchconnectivity)

#### Responding to URL sessions

- [static var urlSession: BackgroundTask<String, Void>](/documentation/swiftui/backgroundtask/urlsession)
- [static func urlSession(String) -> BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/urlsession(_:))
- [static func urlSession(matching: (String) -> Bool) -> BackgroundTask<String, Void>](/documentation/swiftui/backgroundtask/urlsession(matching:))

#### Updating intents and shortcuts

- [static var intentDidRun: BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/intentdidrun)
- [static var relevantShortcut: BackgroundTask<Void, Void>](/documentation/swiftui/backgroundtask/relevantshortcut)
- [SnapshotData](/documentation/swiftui/snapshotdata)

#### Getting the data

- [let identifier: String?](/documentation/swiftui/snapshotdata/identifier)
- [let reason: SnapshotData.SnapshotReason](/documentation/swiftui/snapshotdata/reason)
- [SnapshotData.SnapshotReason](/documentation/swiftui/snapshotdata/snapshotreason)

##### Getting the snapshot reasons

- [case appBackgrounded](/documentation/swiftui/snapshotdata/snapshotreason/appbackgrounded)
- [case appScheduled](/documentation/swiftui/snapshotdata/snapshotreason/appscheduled)
- [case complicationUpdate](/documentation/swiftui/snapshotdata/snapshotreason/complicationupdate)
- [case prelaunch](/documentation/swiftui/snapshotdata/snapshotreason/prelaunch)
- [case returnToDefaultState](/documentation/swiftui/snapshotdata/snapshotreason/returntodefaultstate)
- [SnapshotResponse](/documentation/swiftui/snapshotresponse)

#### Creating a response

- [init(restoredDefaultState: Bool, estimatedSnapshotExpiration: Date?, identifier: String?)](/documentation/swiftui/snapshotresponse/init(restoreddefaultstate:estimatedsnapshotexpiration:identifier:))

### Importing and exporting transferable items

- [func importableFromServices<T>(for: T.Type, action: ([T]) -> Bool) -> some View](/documentation/swiftui/view/importablefromservices(for:action:))
- [func exportableToServices<T>(@autoclosure () -> [T]) -> some View](/documentation/swiftui/view/exportabletoservices(_:))
- [func exportableToServices<T>(@autoclosure () -> [T], onEdit: ([T]) -> Bool) -> some View](/documentation/swiftui/view/exportabletoservices(_:onedit:))

### Importing and exporting using item providers

- [func importsItemProviders([UTType], onImport: ([NSItemProvider]) -> Bool) -> some View](/documentation/swiftui/view/importsitemproviders(_:onimport:))
- [func exportsItemProviders([UTType], onExport: () -> [NSItemProvider]) -> some View](/documentation/swiftui/view/exportsitemproviders(_:onexport:))
- [func exportsItemProviders([UTType], onExport: () -> [NSItemProvider], onEdit: ([NSItemProvider]) -> Bool) -> some View](/documentation/swiftui/view/exportsitemproviders(_:onexport:onedit:))

