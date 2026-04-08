# Accessibility — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Essentials](#essentials) | [Elements](#creating-accessible-elements) | [Identity & visibility](#identity--visibility) | [Types](#supporting-types)
- [Appearance](#accessible-appearance) | [Controls](#accessible-controls) | [Descriptions](#accessible-descriptions) | [Navigation](#accessible-navigation)

### Essentials
- [Accessibility fundamentals](/documentation/swiftui/accessibility-fundamentals) (article)
- [Creating accessible views](/documentation/swiftui/creating-accessible-views) (article)

### Creating accessible elements
- [func accessibilityElement(children:)](/documentation/swiftui/view/accessibilityelement(children:)) — wrap children with behavior
- [func accessibilityChildren(children:)](/documentation/swiftui/view/accessibilitychildren(children:)) — provide synthetic children
- [func accessibilityRepresentation(representation:)](/documentation/swiftui/view/accessibilityrepresentation(representation:)) — replace AX subtree
- [AccessibilityChildBehavior](/documentation/swiftui/accessibilitychildbehavior) — `combine`, `contain`, `ignore`

### Identity & visibility
- [func accessibilityIdentifier(_:)](/documentation/swiftui/view/accessibilityidentifier(_:)) | also [(_:isEnabled:)](/documentation/swiftui/view/accessibilityidentifier(_:isenabled:))
- [func accessibilityHidden(_:)](/documentation/swiftui/view/accessibilityhidden(_:)) | also [(_:isEnabled:)](/documentation/swiftui/view/accessibilityhidden(_:isenabled:))

### Supporting types
- [AccessibilityTechnologies](/documentation/swiftui/accessibilitytechnologies) — `switchControl`, `voiceOver`
- [AccessibilityAttachmentModifier](/documentation/swiftui/accessibilityattachmentmodifier) — modifier container for AX properties

### Accessible appearance
- [Accessible appearance](/documentation/swiftui/accessible-appearance) (article)
- [func accessibilityIgnoresInvertColors(_:)](/documentation/swiftui/view/accessibilityignoresinvertcolors(_:))
- Environment: [accessibilityInvertColors](/documentation/swiftui/environmentvalues/accessibilityinvertcolors), [accessibilityDifferentiateWithoutColor](/documentation/swiftui/environmentvalues/accessibilitydifferentiatewithoutcolor), [accessibilityLargeContentViewerEnabled](/documentation/swiftui/environmentvalues/accessibilitylargecontentviewerenabled), [accessibilityShowButtonShapes](/documentation/swiftui/environmentvalues/accessibilityshowbuttonshapes), [accessibilityReduceTransparency](/documentation/swiftui/environmentvalues/accessibilityreducetransparency), [legibilityWeight](/documentation/swiftui/environmentvalues/legibilityweight), [accessibilityDimFlashingLights](/documentation/swiftui/environmentvalues/accessibilitydimflashinglights), [accessibilityPlayAnimatedImages](/documentation/swiftui/environmentvalues/accessibilityplayanimatedimages), [accessibilityReduceMotion](/documentation/swiftui/environmentvalues/accessibilityreducemotion), [accessibilityAssistiveAccessEnabled](/documentation/swiftui/environmentvalues/accessibilityassistiveaccessenabled)
- [func accessibilityShowsLargeContentViewer()](/documentation/swiftui/view/accessibilityshowslargecontentviewer()) | also [(_:)](/documentation/swiftui/view/accessibilityshowslargecontentviewer(_:))
- [LegibilityWeight](/documentation/swiftui/legibilityweight) — `regular`, `bold`
- [AssistiveAccess](/documentation/swiftui/assistiveaccess) — container view for assistive access mode

### Accessible controls
- [Accessible controls](/documentation/swiftui/accessible-controls) (article)
- [func accessibilityAction(_:_:)](/documentation/swiftui/view/accessibilityaction(_:_:)) | [(named:_:)](/documentation/swiftui/view/accessibilityaction(named:_:)) | [(action:label:)](/documentation/swiftui/view/accessibilityaction(action:label:)) | [(intent:label:)](/documentation/swiftui/view/accessibilityaction(intent:label:)) | [(_:intent:)](/documentation/swiftui/view/accessibilityaction(_:intent:)) | [(named:intent:)](/documentation/swiftui/view/accessibilityaction(named:intent:))
- [func accessibilityActions(_:)](/documentation/swiftui/view/accessibilityactions(_:)) | [(category:_:)](/documentation/swiftui/view/accessibilityactions(category:_:))
- [func accessibilityAdjustableAction(_:)](/documentation/swiftui/view/accessibilityadjustableaction(_:)) | [accessibilityScrollAction(_:)](/documentation/swiftui/view/accessibilityscrollaction(_:))
- [AccessibilityActionKind](/documentation/swiftui/accessibilityactionkind) — `default`, `delete`, `escape`, `magicTap`, `showMenu`
- [AccessibilityAdjustmentDirection](/documentation/swiftui/accessibilityadjustmentdirection) — `decrement`, `increment`
- [AccessibilityActionCategory](/documentation/swiftui/accessibilityactioncategory) — `default`, `edit`
- [func accessibilityQuickAction(style:content:)](/documentation/swiftui/view/accessibilityquickaction(style:content:)) | [(style:isActive:content:)](/documentation/swiftui/view/accessibilityquickaction(style:isactive:content:))
- [AccessibilityQuickActionStyle](/documentation/swiftui/accessibilityquickactionstyle) — `outline` ([OutlineStyle](/documentation/swiftui/accessibilityquickactionoutlinestyle)), `prompt` ([PromptStyle](/documentation/swiftui/accessibilityquickactionpromptstyle))
- [func accessibilityActivationPoint(_:)](/documentation/swiftui/view/accessibilityactivationpoint(_:)) | also [(_:isEnabled:)](/documentation/swiftui/view/accessibilityactivationpoint(_:isenabled:))
- [func accessibilityDragPoint(_:description:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:)) | also [(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydragpoint(_:description:isenabled:))
- [func accessibilityDropPoint(_:description:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:)) | also [(_:description:isEnabled:)](/documentation/swiftui/view/accessibilitydroppoint(_:description:isenabled:))
- [func accessibilityDirectTouch(_:options:)](/documentation/swiftui/view/accessibilitydirecttouch(_:options:)) | [accessibilityZoomAction(_:)](/documentation/swiftui/view/accessibilityzoomaction(_:))
- [AccessibilityDirectTouchOptions](/documentation/swiftui/accessibilitydirecttouchoptions) — `requiresActivation`, `silentOnTouch`
- [AccessibilityZoomGestureAction](/documentation/swiftui/accessibilityzoomgestureaction) — props: `direction`, `location`, `point`; Direction: `zoomIn`, `zoomOut`
- [func accessibilityFocused(_:)](/documentation/swiftui/view/accessibilityfocused(_:)) | [(_:equals:)](/documentation/swiftui/view/accessibilityfocused(_:equals:))
- [AccessibilityFocusState](/documentation/swiftui/accessibilityfocusstate) — property wrapper for AX focus; nested [Binding](/documentation/swiftui/accessibilityfocusstate/binding)
- [func accessibilityRespondsToUserInteraction(_:)](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:)) | also [(_:isEnabled:)](/documentation/swiftui/view/accessibilityrespondstouserinteraction(_:isenabled:))

### Accessible descriptions
- [Accessible descriptions](/documentation/swiftui/accessible-descriptions) (article)
- [func accessibilityLabel(_:)](/documentation/swiftui/view/accessibilitylabel(_:)) | [(_:isEnabled:)](/documentation/swiftui/view/accessibilitylabel(_:isenabled:)) | [(content:)](/documentation/swiftui/view/accessibilitylabel(content:))
- [func accessibilityInputLabels(_:)](/documentation/swiftui/view/accessibilityinputlabels(_:)) | [(_:isEnabled:)](/documentation/swiftui/view/accessibilityinputlabels(_:isenabled:))
- [func accessibilityLabeledPair(role:id:in:)](/documentation/swiftui/view/accessibilitylabeledpair(role:id:in:)) — [AccessibilityLabeledPairRole](/documentation/swiftui/accessibilitylabeledpairrole): `content`, `label`
- [func accessibilityValue(_:)](/documentation/swiftui/view/accessibilityvalue(_:)) | [(_:isEnabled:)](/documentation/swiftui/view/accessibilityvalue(_:isenabled:))
- [func accessibilityTextContentType(_:)](/documentation/swiftui/view/accessibilitytextcontenttype(_:)) | [accessibilityHeading(_:)](/documentation/swiftui/view/accessibilityheading(_:))
- [AccessibilityHeadingLevel](/documentation/swiftui/accessibilityheadinglevel) — `h1`-`h6`, `unspecified`
- [AccessibilityTextContentType](/documentation/swiftui/accessibilitytextcontenttype) — `console`, `fileSystem`, `messaging`, `narrative`, `plain`, `sourceCode`, `spreadsheet`, `wordProcessing`
- [func accessibilityChartDescriptor(_:)](/documentation/swiftui/view/accessibilitychartdescriptor(_:)) — [AXChartDescriptorRepresentable](/documentation/swiftui/axchartdescriptorrepresentable) protocol
- [func accessibilityCustomContent(_:_:importance:)](/documentation/swiftui/view/accessibilitycustomcontent(_:_:importance:)) — [AccessibilityCustomContentKey](/documentation/swiftui/accessibilitycustomcontentkey)
- [func accessibilityAddTraits(_:)](/documentation/swiftui/view/accessibilityaddtraits(_:)) | [accessibilityRemoveTraits(_:)](/documentation/swiftui/view/accessibilityremovetraits(_:))
- [AccessibilityTraits](/documentation/swiftui/accessibilitytraits) — `allowsDirectInteraction`, `causesPageTurn`, `isButton`, `isHeader`, `isImage`, `isKeyboardKey`, `isLink`, `isModal`, `isSearchField`, `isSelected`, `isStaticText`, `isSummaryElement`, `isTabBar`, `isToggle`, `playsSound`, `startsMediaSession`, `updatesFrequently`
- [func accessibilityHint(_:)](/documentation/swiftui/view/accessibilityhint(_:)) | [(_:isEnabled:)](/documentation/swiftui/view/accessibilityhint(_:isenabled:))
- VoiceOver speech: [speechAdjustedPitch(_:)](/documentation/swiftui/view/speechadjustedpitch(_:)) | [speechAlwaysIncludesPunctuation(_:)](/documentation/swiftui/view/speechalwaysincludespunctuation(_:)) | [speechAnnouncementsQueued(_:)](/documentation/swiftui/view/speechannouncementsqueued(_:)) | [speechSpellsOutCharacters(_:)](/documentation/swiftui/view/speechspellsoutcharacters(_:))

### Accessible navigation
- [Accessible navigation](/documentation/swiftui/accessible-navigation) (article)
- [func accessibilityRotor(_:entries:)](/documentation/swiftui/view/accessibilityrotor(_:entries:)) | [(_:entries:entryID:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entryid:entrylabel:)) | [(_:entries:entryLabel:)](/documentation/swiftui/view/accessibilityrotor(_:entries:entrylabel:)) | [(_:textRanges:)](/documentation/swiftui/view/accessibilityrotor(_:textranges:))
- [AccessibilityRotorContent](/documentation/swiftui/accessibilityrotorcontent) — protocol | [AccessibilityRotorContentBuilder](/documentation/swiftui/accessibilityrotorcontentbuilder) — result builder
- [AccessibilityRotorEntry](/documentation/swiftui/accessibilityrotorentry) — single rotor entry
- [AccessibilitySystemRotor](/documentation/swiftui/accessibilitysystemrotor) — text: `textFields`, `boldText`, `italicText`, `underlineText`, `misspelledWords`; headings: `headings`, `headings(level:)`; links: `links`, `links(visited:)`; other: `images`, `landmarks`, `lists`, `tables`
- [func accessibilityRotorEntry(id:in:)](/documentation/swiftui/view/accessibilityrotorentry(id:in:)) | [accessibilityLinkedGroup(id:in:)](/documentation/swiftui/view/accessibilitylinkedgroup(id:in:)) | [accessibilitySortPriority(_:)](/documentation/swiftui/view/accessibilitysortpriority(_:))
