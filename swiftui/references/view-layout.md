# View Layout — SwiftUI Reference

## Contents
- [View layout](#view-layout)
  - [Choosing a layout](#choosing-a-layout)
  - [Statically arranging views in one dimension](#statically-arranging-views-in-one-dimension)
  - [Dynamically arranging views in one dimension](#dynamically-arranging-views-in-one-dimension)
  - [Statically arranging views in two dimensions](#statically-arranging-views-in-two-dimensions)
  - [Dynamically arranging views in two dimensions](#dynamically-arranging-views-in-two-dimensions)
  - [Layering views](#layering-views)
  - [Automatically choosing the layout that fits](#automatically-choosing-the-layout-that-fits)
  - [Separators](#separators)
  - [Fine-tuning a layout](#fine-tuning-a-layout)
  - [Adding padding around a view](#adding-padding-around-a-view)
  - [Influencing a view’s size](#influencing-a-views-size)
  - [Adjusting a view’s position](#adjusting-a-views-position)
  - [Aligning views](#aligning-views)
  - [Setting margins](#setting-margins)
  - [Staying in the safe areas](#staying-in-the-safe-areas)
  - [Setting a layout direction](#setting-a-layout-direction)
  - [Reacting to interface characteristics](#reacting-to-interface-characteristics)
  - [Accessing edges, regions, and layouts](#accessing-edges-regions-and-layouts)
  - [Creating a custom layout container](#creating-a-custom-layout-container)
  - [Configuring a custom layout](#configuring-a-custom-layout)
  - [Associating values with views in a custom layout](#associating-values-with-views-in-a-custom-layout)
  - [Transitioning between layout types](#transitioning-between-layout-types)
  - [Creating a list](#creating-a-list)
  - [Disclosing information progressively](#disclosing-information-progressively)
  - [Configuring a list’s layout](#configuring-a-lists-layout)
  - [Configuring rows](#configuring-rows)
  - [Configuring headers](#configuring-headers)
  - [Configuring separators](#configuring-separators)
  - [Configuring backgrounds](#configuring-backgrounds)
  - [Displaying a badge on a list item](#displaying-a-badge-on-a-list-item)
  - [Configuring interaction](#configuring-interaction)
  - [Refreshing a list’s content](#refreshing-a-lists-content)
  - [Editing a list](#editing-a-list)
  - [Configuring a section index](#configuring-a-section-index)
  - [Creating a table](#creating-a-table)
  - [Creating columns](#creating-columns)
  - [Customizing columns](#customizing-columns)
  - [Creating rows](#creating-rows)
  - [Adding progressive disclosure](#adding-progressive-disclosure)
  - [Grouping views into a container](#grouping-views-into-a-container)
  - [Organizing views into sections](#organizing-views-into-sections)
  - [Iterating over dynamic data](#iterating-over-dynamic-data)
  - [Accessing a container’s subviews](#accessing-a-containers-subviews)
  - [Grouping views into a box](#grouping-views-into-a-box)
  - [Grouping inputs](#grouping-inputs)
  - [Presenting a group of controls](#presenting-a-group-of-controls)
  - [Creating a scroll view](#creating-a-scroll-view)
  - [Managing scroll position](#managing-scroll-position)
  - [Defining scroll targets](#defining-scroll-targets)
  - [Animating scroll transitions](#animating-scroll-transitions)
  - [Responding to scroll view changes](#responding-to-scroll-view-changes)
  - [Showing scroll indicators](#showing-scroll-indicators)
  - [Managing content visibility](#managing-content-visibility)
  - [Disabling scrolling](#disabling-scrolling)
  - [Configuring scroll bounce behavior](#configuring-scroll-bounce-behavior)
  - [Configuring scroll edge effects](#configuring-scroll-edge-effects)
  - [Interacting with a software keyboard](#interacting-with-a-software-keyboard)
  - [Managing scrolling for different inputs](#managing-scrolling-for-different-inputs)

---
## View layout

- [Layout fundamentals](/documentation/swiftui/layout-fundamentals)

### Choosing a layout

- [Picking container views for your content](/documentation/swiftui/picking-container-views-for-your-content)

### Statically arranging views in one dimension

- [Building layouts with stack views](/documentation/swiftui/building-layouts-with-stack-views)
- [HStack](/documentation/swiftui/hstack)

#### Creating a stack

- [init(alignment: VerticalAlignment, spacing: CGFloat?, content: () -> Content)](/documentation/swiftui/hstack/init(alignment:spacing:content:))
- [VStack](/documentation/swiftui/vstack)

#### Creating a stack

- [init(alignment: HorizontalAlignment, spacing: CGFloat?, content: () -> Content)](/documentation/swiftui/vstack/init(alignment:spacing:content:))

### Dynamically arranging views in one dimension

- [Grouping data with lazy stack views](/documentation/swiftui/grouping-data-with-lazy-stack-views)
- [Creating performant scrollable stacks](/documentation/swiftui/creating-performant-scrollable-stacks)
- [LazyHStack](/documentation/swiftui/lazyhstack)

#### Creating a lazy-loading horizontal stack

- [init(alignment: VerticalAlignment, spacing: CGFloat?, pinnedViews: PinnedScrollableViews, content: () -> Content)](/documentation/swiftui/lazyhstack/init(alignment:spacing:pinnedviews:content:))
- [LazyVStack](/documentation/swiftui/lazyvstack)

#### Creating a lazy-loading vertical stack

- [init(alignment: HorizontalAlignment, spacing: CGFloat?, pinnedViews: PinnedScrollableViews, content: () -> Content)](/documentation/swiftui/lazyvstack/init(alignment:spacing:pinnedviews:content:))
- [PinnedScrollableViews](/documentation/swiftui/pinnedscrollableviews)

#### Getting scrollable view types

- [static let sectionHeaders: PinnedScrollableViews](/documentation/swiftui/pinnedscrollableviews/sectionheaders)
- [static let sectionFooters: PinnedScrollableViews](/documentation/swiftui/pinnedscrollableviews/sectionfooters)

### Statically arranging views in two dimensions

- [Grid](/documentation/swiftui/grid)

#### Creating a grid

- [init(alignment: Alignment, horizontalSpacing: CGFloat?, verticalSpacing: CGFloat?, content: () -> Content)](/documentation/swiftui/grid/init(alignment:horizontalspacing:verticalspacing:content:))
- [GridRow](/documentation/swiftui/gridrow)

#### Creating a grid row

- [init(alignment: VerticalAlignment?, content: () -> Content)](/documentation/swiftui/gridrow/init(alignment:content:))
- [func gridCellColumns(Int) -> some View](/documentation/swiftui/view/gridcellcolumns(_:))
- [func gridCellAnchor(UnitPoint) -> some View](/documentation/swiftui/view/gridcellanchor(_:))
- [func gridCellUnsizedAxes(Axis.Set) -> some View](/documentation/swiftui/view/gridcellunsizedaxes(_:))
- [func gridColumnAlignment(HorizontalAlignment) -> some View](/documentation/swiftui/view/gridcolumnalignment(_:))

### Dynamically arranging views in two dimensions

- [LazyHGrid](/documentation/swiftui/lazyhgrid)

#### Creating a horizontal grid

- [init(rows: [GridItem], alignment: VerticalAlignment, spacing: CGFloat?, pinnedViews: PinnedScrollableViews, content: () -> Content)](/documentation/swiftui/lazyhgrid/init(rows:alignment:spacing:pinnedviews:content:))
- [LazyVGrid](/documentation/swiftui/lazyvgrid)

#### Creating a vertical grid

- [init(columns: [GridItem], alignment: HorizontalAlignment, spacing: CGFloat?, pinnedViews: PinnedScrollableViews, content: () -> Content)](/documentation/swiftui/lazyvgrid/init(columns:alignment:spacing:pinnedviews:content:))
- [GridItem](/documentation/swiftui/griditem)

#### Creating a grid item

- [init(GridItem.Size, spacing: CGFloat?, alignment: Alignment?)](/documentation/swiftui/griditem/init(_:spacing:alignment:))

#### Inspecting grid item properties

- [var alignment: Alignment?](/documentation/swiftui/griditem/alignment)
- [var spacing: CGFloat?](/documentation/swiftui/griditem/spacing)
- [var size: GridItem.Size](/documentation/swiftui/griditem/size-swift.property)
- [GridItem.Size](/documentation/swiftui/griditem/size-swift.enum)

##### Getting the sizes

- [case adaptive(minimum: CGFloat, maximum: CGFloat)](/documentation/swiftui/griditem/size-swift.enum/adaptive(minimum:maximum:))
- [case fixed(CGFloat)](/documentation/swiftui/griditem/size-swift.enum/fixed(_:))
- [case flexible(minimum: CGFloat, maximum: CGFloat)](/documentation/swiftui/griditem/size-swift.enum/flexible(minimum:maximum:))

### Layering views

- [Adding a background to your view](/documentation/swiftui/adding-a-background-to-your-view)
- [ZStack](/documentation/swiftui/zstack)

#### Creating a stack

- [init(alignment: Alignment, content: () -> Content)](/documentation/swiftui/zstack/init(alignment:content:))

#### Supporting symbols

- [ZStackContent3D](/documentation/swiftui/zstackcontent3d)

##### Initializers

- [init(spacing: CGFloat?, content: Content)](/documentation/swiftui/zstackcontent3d/init(spacing:content:))

##### Instance Properties

- [var content: Content](/documentation/swiftui/zstackcontent3d/content)
- [var spacing: CGFloat?](/documentation/swiftui/zstackcontent3d/spacing)

#### Initializers

- [init<V>(alignment: Alignment, spacing: CGFloat?, content: () -> V)](/documentation/swiftui/zstack/init(alignment:spacing:content:))
- [func zIndex(Double) -> some View](/documentation/swiftui/view/zindex(_:))
- [func background<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/background(alignment:content:))
- [func background<S>(S, ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/background(_:ignoressafeareaedges:))
- [func background(ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/background(ignoressafeareaedges:))
- [func background(_:in:fillStyle:)](/documentation/swiftui/view/background(_:in:fillstyle:))
- [func background(in:fillStyle:)](/documentation/swiftui/view/background(in:fillstyle:))
- [func overlay<V>(alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/overlay(alignment:content:))
- [func overlay<S>(S, ignoresSafeAreaEdges: Edge.Set) -> some View](/documentation/swiftui/view/overlay(_:ignoressafeareaedges:))
- [func overlay<S, T>(S, in: T, fillStyle: FillStyle) -> some View](/documentation/swiftui/view/overlay(_:in:fillstyle:))
- [var backgroundMaterial: Material?](/documentation/swiftui/environmentvalues/backgroundmaterial)
- [func containerBackground<S>(S, for: ContainerBackgroundPlacement) -> some View](/documentation/swiftui/view/containerbackground(_:for:))
- [func containerBackground<V>(for: ContainerBackgroundPlacement, alignment: Alignment, content: () -> V) -> some View](/documentation/swiftui/view/containerbackground(for:alignment:content:))
- [ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement)

#### Getting placements

- [static let navigation: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/navigation)
- [static let tabView: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/tabview)
- [static let widget: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/widget)

#### Getting StoreKit placements

- [static var subscriptionStore: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/subscriptionstore)
- [static var subscriptionStoreFullHeight: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/subscriptionstorefullheight)
- [static var subscriptionStoreHeader: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/subscriptionstoreheader)

#### Type Properties

- [static let navigationSplitView: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/navigationsplitview)
- [static let window: ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement/window)

### Automatically choosing the layout that fits

- [ViewThatFits](/documentation/swiftui/viewthatfits)

#### Creating a view that fits

- [init(in: Axis.Set, content: () -> Content)](/documentation/swiftui/viewthatfits/init(in:content:))

### Separators

- [Spacer](/documentation/swiftui/spacer)

#### Creating a spacer

- [init(minLength: CGFloat?)](/documentation/swiftui/spacer/init(minlength:))
- [var minLength: CGFloat?](/documentation/swiftui/spacer/minlength)
- [Divider](/documentation/swiftui/divider)

#### Creating a divider

- [init()](/documentation/swiftui/divider/init())
- [Layout adjustments](/documentation/swiftui/layout-adjustments)

### Fine-tuning a layout

- [Laying out a simple view](/documentation/swiftui/laying-out-a-simple-view)
- [Inspecting view layout](/documentation/swiftui/inspecting-view-layout)

### Adding padding around a view

- [func padding(_:)](/documentation/swiftui/view/padding(_:))
- [func padding(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding(_:_:))
- [func padding3D(_:)](/documentation/swiftui/view/padding3d(_:))
- [func padding3D(Edge3D.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding3d(_:_:))
- [func scenePadding(Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:))
- [func scenePadding(ScenePadding, edges: Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:edges:))
- [ScenePadding](/documentation/swiftui/scenepadding)

#### Getting padding values

- [static let minimum: ScenePadding](/documentation/swiftui/scenepadding/minimum)
- [static let navigationBar: ScenePadding](/documentation/swiftui/scenepadding/navigationbar)

### Influencing a view’s size

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

### Adjusting a view’s position

- [Making fine adjustments to a view’s position](/documentation/swiftui/making-fine-adjustments-to-a-view-s-position)
- [func position(CGPoint) -> some View](/documentation/swiftui/view/position(_:))
- [func position(x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/position(x:y:))
- [func offset(CGSize) -> some View](/documentation/swiftui/view/offset(_:))
- [func offset(x: CGFloat, y: CGFloat) -> some View](/documentation/swiftui/view/offset(x:y:))
- [func offset(z: CGFloat) -> some View](/documentation/swiftui/view/offset(z:))

### Aligning views

- [Aligning views within a stack](/documentation/swiftui/aligning-views-within-a-stack)
- [Aligning views across stacks](/documentation/swiftui/aligning-views-across-stacks)
- [func alignmentGuide(_:computeValue:)](/documentation/swiftui/view/alignmentguide(_:computevalue:))
- [Alignment](/documentation/swiftui/alignment)

#### Getting top guides

- [static let topLeading: Alignment](/documentation/swiftui/alignment/topleading)
- [static let top: Alignment](/documentation/swiftui/alignment/top)
- [static let topTrailing: Alignment](/documentation/swiftui/alignment/toptrailing)

#### Getting middle guides

- [static let leading: Alignment](/documentation/swiftui/alignment/leading)
- [static let center: Alignment](/documentation/swiftui/alignment/center)
- [static let trailing: Alignment](/documentation/swiftui/alignment/trailing)

#### Getting bottom guides

- [static let bottomLeading: Alignment](/documentation/swiftui/alignment/bottomleading)
- [static let bottom: Alignment](/documentation/swiftui/alignment/bottom)
- [static let bottomTrailing: Alignment](/documentation/swiftui/alignment/bottomtrailing)

#### Getting text baseline guides

- [static var leadingFirstTextBaseline: Alignment](/documentation/swiftui/alignment/leadingfirsttextbaseline)
- [static var centerFirstTextBaseline: Alignment](/documentation/swiftui/alignment/centerfirsttextbaseline)
- [static var trailingFirstTextBaseline: Alignment](/documentation/swiftui/alignment/trailingfirsttextbaseline)
- [static var leadingLastTextBaseline: Alignment](/documentation/swiftui/alignment/leadinglasttextbaseline)
- [static var centerLastTextBaseline: Alignment](/documentation/swiftui/alignment/centerlasttextbaseline)
- [static var trailingLastTextBaseline: Alignment](/documentation/swiftui/alignment/trailinglasttextbaseline)

#### Creating a custom alignment

- [init(horizontal: HorizontalAlignment, vertical: VerticalAlignment)](/documentation/swiftui/alignment/init(horizontal:vertical:))
- [var horizontal: HorizontalAlignment](/documentation/swiftui/alignment/horizontal)
- [var vertical: VerticalAlignment](/documentation/swiftui/alignment/vertical)
- [HorizontalAlignment](/documentation/swiftui/horizontalalignment)

#### Getting guides

- [static let leading: HorizontalAlignment](/documentation/swiftui/horizontalalignment/leading)
- [static let center: HorizontalAlignment](/documentation/swiftui/horizontalalignment/center)
- [static let trailing: HorizontalAlignment](/documentation/swiftui/horizontalalignment/trailing)
- [static let listRowSeparatorLeading: HorizontalAlignment](/documentation/swiftui/horizontalalignment/listrowseparatorleading)
- [static let listRowSeparatorTrailing: HorizontalAlignment](/documentation/swiftui/horizontalalignment/listrowseparatortrailing)

#### Creating a custom alignment

- [init(any AlignmentID.Type)](/documentation/swiftui/horizontalalignment/init(_:))
- [func combineExplicit<S>(S) -> CGFloat?](/documentation/swiftui/horizontalalignment/combineexplicit(_:))
- [VerticalAlignment](/documentation/swiftui/verticalalignment)

#### Getting guides

- [static let top: VerticalAlignment](/documentation/swiftui/verticalalignment/top)
- [static let center: VerticalAlignment](/documentation/swiftui/verticalalignment/center)
- [static let bottom: VerticalAlignment](/documentation/swiftui/verticalalignment/bottom)
- [static let firstTextBaseline: VerticalAlignment](/documentation/swiftui/verticalalignment/firsttextbaseline)
- [static let lastTextBaseline: VerticalAlignment](/documentation/swiftui/verticalalignment/lasttextbaseline)

#### Creating a custom alignment

- [init(any AlignmentID.Type)](/documentation/swiftui/verticalalignment/init(_:))
- [func combineExplicit<S>(S) -> CGFloat?](/documentation/swiftui/verticalalignment/combineexplicit(_:))
- [DepthAlignment](/documentation/swiftui/depthalignment)

#### Getting guides

- [static let back: DepthAlignment](/documentation/swiftui/depthalignment/back)
- [static let center: DepthAlignment](/documentation/swiftui/depthalignment/center)
- [static let front: DepthAlignment](/documentation/swiftui/depthalignment/front)

#### Initializers

- [init(any DepthAlignmentID.Type)](/documentation/swiftui/depthalignment/init(_:))

#### Instance Methods

- [func combineExplicit<S>(S) -> CGFloat?](/documentation/swiftui/depthalignment/combineexplicit(_:))
- [AlignmentID](/documentation/swiftui/alignmentid)

#### Getting the default value

- [static func defaultValue(in: ViewDimensions) -> CGFloat](/documentation/swiftui/alignmentid/defaultvalue(in:))
- [ViewDimensions](/documentation/swiftui/viewdimensions)

#### Getting dimensions

- [var height: CGFloat](/documentation/swiftui/viewdimensions/height)
- [var width: CGFloat](/documentation/swiftui/viewdimensions/width)

#### Accessing guide values

- [subscript(_:)](/documentation/swiftui/viewdimensions/subscript(_:))
- [subscript(explicit:)](/documentation/swiftui/viewdimensions/subscript(explicit:))
- [ViewDimensions3D](/documentation/swiftui/viewdimensions3d)

#### Instance Properties

- [var depth: CGFloat](/documentation/swiftui/viewdimensions3d/depth)
- [var height: CGFloat](/documentation/swiftui/viewdimensions3d/height)
- [var width: CGFloat](/documentation/swiftui/viewdimensions3d/width)

#### Subscripts

- [subscript(_:)](/documentation/swiftui/viewdimensions3d/subscript(_:))
- [subscript(explicit:)](/documentation/swiftui/viewdimensions3d/subscript(explicit:))
- [SpatialContainer](/documentation/swiftui/spatialcontainer)

#### Initializers

- [init(alignment: Alignment3D)](/documentation/swiftui/spatialcontainer/init(alignment:))

### Setting margins

- [func contentMargins(CGFloat, for: ContentMarginPlacement) -> some View](/documentation/swiftui/view/contentmargins(_:for:))
- [func contentMargins(_:_:for:)](/documentation/swiftui/view/contentmargins(_:_:for:))
- [ContentMarginPlacement](/documentation/swiftui/contentmarginplacement)

#### Getting the placement

- [static var automatic: ContentMarginPlacement](/documentation/swiftui/contentmarginplacement/automatic)
- [static var scrollContent: ContentMarginPlacement](/documentation/swiftui/contentmarginplacement/scrollcontent)
- [static var scrollIndicators: ContentMarginPlacement](/documentation/swiftui/contentmarginplacement/scrollindicators)

### Staying in the safe areas

- [func ignoresSafeArea(SafeAreaRegions, edges: Edge.Set) -> some View](/documentation/swiftui/view/ignoressafearea(_:edges:))
- [func safeAreaInset(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareainset(edge:alignment:spacing:content:))
- [func safeAreaPadding(_:)](/documentation/swiftui/view/safeareapadding(_:))
- [func safeAreaPadding(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/safeareapadding(_:_:))
- [SafeAreaRegions](/documentation/swiftui/safearearegions)

#### Getting safe area regions

- [static let all: SafeAreaRegions](/documentation/swiftui/safearearegions/all)
- [static let container: SafeAreaRegions](/documentation/swiftui/safearearegions/container)
- [static let keyboard: SafeAreaRegions](/documentation/swiftui/safearearegions/keyboard)

### Setting a layout direction

- [func layoutDirectionBehavior(LayoutDirectionBehavior) -> some View](/documentation/swiftui/view/layoutdirectionbehavior(_:))
- [LayoutDirectionBehavior](/documentation/swiftui/layoutdirectionbehavior)

#### Getting behaviors

- [case fixed](/documentation/swiftui/layoutdirectionbehavior/fixed)
- [static var mirrors: LayoutDirectionBehavior](/documentation/swiftui/layoutdirectionbehavior/mirrors)
- [case mirrors(in: LayoutDirection)](/documentation/swiftui/layoutdirectionbehavior/mirrors(in:))
- [var layoutDirection: LayoutDirection](/documentation/swiftui/environmentvalues/layoutdirection)
- [LayoutDirection](/documentation/swiftui/layoutdirection)

#### Getting layout directions

- [case leftToRight](/documentation/swiftui/layoutdirection/lefttoright)
- [case rightToLeft](/documentation/swiftui/layoutdirection/righttoleft)

#### Creating a layout direction

- [init?(UITraitEnvironmentLayoutDirection)](/documentation/swiftui/layoutdirection/init(_:))
- [LayoutRotationUnaryLayout](/documentation/swiftui/layoutrotationunarylayout)

### Reacting to interface characteristics

- [var isLuminanceReduced: Bool](/documentation/swiftui/environmentvalues/isluminancereduced)
- [var displayScale: CGFloat](/documentation/swiftui/environmentvalues/displayscale)
- [var pixelLength: CGFloat](/documentation/swiftui/environmentvalues/pixellength)
- [var horizontalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/horizontalsizeclass)
- [var verticalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/verticalsizeclass)
- [UserInterfaceSizeClass](/documentation/swiftui/userinterfacesizeclass)

#### Getting size classes

- [case compact](/documentation/swiftui/userinterfacesizeclass/compact)
- [case regular](/documentation/swiftui/userinterfacesizeclass/regular)

#### Creating a size class

- [init?(UIUserInterfaceSizeClass)](/documentation/swiftui/userinterfacesizeclass/init(_:))

### Accessing edges, regions, and layouts

- [Edge](/documentation/swiftui/edge)

#### Getting the edges

- [case top](/documentation/swiftui/edge/top)
- [case bottom](/documentation/swiftui/edge/bottom)
- [case leading](/documentation/swiftui/edge/leading)
- [case trailing](/documentation/swiftui/edge/trailing)

#### Creating an edge

- [init?(Edge3D)](/documentation/swiftui/edge/init(_:))

#### Accessing sets of edges

- [Edge.Set](/documentation/swiftui/edge/set)

##### Getting edge sets

- [static let all: Edge.Set](/documentation/swiftui/edge/set/all)
- [static let top: Edge.Set](/documentation/swiftui/edge/set/top)
- [static let bottom: Edge.Set](/documentation/swiftui/edge/set/bottom)
- [static let leading: Edge.Set](/documentation/swiftui/edge/set/leading)
- [static let trailing: Edge.Set](/documentation/swiftui/edge/set/trailing)
- [static let horizontal: Edge.Set](/documentation/swiftui/edge/set/horizontal)
- [static let vertical: Edge.Set](/documentation/swiftui/edge/set/vertical)

##### Creating an edge set

- [init(Edge)](/documentation/swiftui/edge/set/init(_:))

#### Enumerations

- [Edge.Corner](/documentation/swiftui/edge/corner)

##### Structures

- [Edge.Corner.Set](/documentation/swiftui/edge/corner/set)

###### Initializers

- [init(Edge.Corner)](/documentation/swiftui/edge/corner/set/init(_:))
- [init(rawValue: Int8)](/documentation/swiftui/edge/corner/set/init(rawvalue:))

###### Instance Methods

- [func contains(Edge.Corner) -> Bool](/documentation/swiftui/edge/corner/set/contains(_:))

###### Type Properties

- [static let all: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/all)
- [static let bottom: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/bottom)
- [static let bottomLeading: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/bottomleading)
- [static let bottomTrailing: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/bottomtrailing)
- [static let leading: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/leading)
- [static let none: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/none)
- [static let top: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/top)
- [static let topLeading: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/topleading)
- [static let topTrailing: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/toptrailing)
- [static let trailing: Edge.Corner.Set](/documentation/swiftui/edge/corner/set/trailing)
- [Edge.Corner.Style](/documentation/swiftui/edge/corner/style)

###### Type Properties

- [static var concentric: Edge.Corner.Style](/documentation/swiftui/edge/corner/style/concentric)

###### Type Methods

- [static func concentric(minimum: Edge.Corner.Style?) -> Edge.Corner.Style](/documentation/swiftui/edge/corner/style/concentric(minimum:))
- [static func fixed(CGFloat) -> Edge.Corner.Style](/documentation/swiftui/edge/corner/style/fixed(_:))

###### Default Implementations

- [ExpressibleByFloatLiteral Implementations](/documentation/swiftui/edge/corner/style/expressiblebyfloatliteral-implementations)

###### Initializers

- [init(floatLiteral: Edge.Corner.Style.FloatLiteralType)](/documentation/swiftui/edge/corner/style/init(floatliteral:))
- [ExpressibleByIntegerLiteral Implementations](/documentation/swiftui/edge/corner/style/expressiblebyintegerliteral-implementations)

###### Initializers

- [init(integerLiteral: Edge.Corner.Style.IntegerLiteralType)](/documentation/swiftui/edge/corner/style/init(integerliteral:))

##### Enumeration Cases

- [case bottomLeading](/documentation/swiftui/edge/corner/bottomleading)
- [case bottomTrailing](/documentation/swiftui/edge/corner/bottomtrailing)
- [case topLeading](/documentation/swiftui/edge/corner/topleading)
- [case topTrailing](/documentation/swiftui/edge/corner/toptrailing)
- [Edge3D](/documentation/swiftui/edge3d)

#### Getting the edges

- [case top](/documentation/swiftui/edge3d/top)
- [case bottom](/documentation/swiftui/edge3d/bottom)
- [case leading](/documentation/swiftui/edge3d/leading)
- [case trailing](/documentation/swiftui/edge3d/trailing)
- [case front](/documentation/swiftui/edge3d/front)
- [case back](/documentation/swiftui/edge3d/back)

#### Creating an edge

- [init(Edge)](/documentation/swiftui/edge3d/init(_:))

#### Accessing sets of edges

- [Edge3D.Set](/documentation/swiftui/edge3d/set)

##### Getting edge sets

- [static let all: Edge3D.Set](/documentation/swiftui/edge3d/set/all)
- [static let top: Edge3D.Set](/documentation/swiftui/edge3d/set/top)
- [static let bottom: Edge3D.Set](/documentation/swiftui/edge3d/set/bottom)
- [static let leading: Edge3D.Set](/documentation/swiftui/edge3d/set/leading)
- [static let front: Edge3D.Set](/documentation/swiftui/edge3d/set/front)
- [static let back: Edge3D.Set](/documentation/swiftui/edge3d/set/back)
- [static let trailing: Edge3D.Set](/documentation/swiftui/edge3d/set/trailing)
- [static let horizontal: Edge3D.Set](/documentation/swiftui/edge3d/set/horizontal)
- [static let vertical: Edge3D.Set](/documentation/swiftui/edge3d/set/vertical)
- [static let depth: Edge3D.Set](/documentation/swiftui/edge3d/set/depth)

##### Creating an edge set

- [init(_:)](/documentation/swiftui/edge3d/set/init(_:))
- [HorizontalEdge](/documentation/swiftui/horizontaledge)

#### Getting the edges

- [case leading](/documentation/swiftui/horizontaledge/leading)
- [case trailing](/documentation/swiftui/horizontaledge/trailing)

#### Accessing sets of edges

- [HorizontalEdge.Set](/documentation/swiftui/horizontaledge/set)

##### Getting edge sets

- [static let all: HorizontalEdge.Set](/documentation/swiftui/horizontaledge/set/all)
- [static let leading: HorizontalEdge.Set](/documentation/swiftui/horizontaledge/set/leading)
- [static let trailing: HorizontalEdge.Set](/documentation/swiftui/horizontaledge/set/trailing)

##### Creating an edge set

- [init(HorizontalEdge)](/documentation/swiftui/horizontaledge/set/init(_:))
- [VerticalEdge](/documentation/swiftui/verticaledge)

#### Getting the edges

- [case top](/documentation/swiftui/verticaledge/top)
- [case bottom](/documentation/swiftui/verticaledge/bottom)

#### Accessing sets of edges

- [VerticalEdge.Set](/documentation/swiftui/verticaledge/set)

##### Getting edge sets

- [static let all: VerticalEdge.Set](/documentation/swiftui/verticaledge/set/all)
- [static let top: VerticalEdge.Set](/documentation/swiftui/verticaledge/set/top)
- [static let bottom: VerticalEdge.Set](/documentation/swiftui/verticaledge/set/bottom)

##### Creating an edge set

- [init(VerticalEdge)](/documentation/swiftui/verticaledge/set/init(_:))
- [EdgeInsets](/documentation/swiftui/edgeinsets)

#### Getting edge insets

- [var top: CGFloat](/documentation/swiftui/edgeinsets/top)
- [var bottom: CGFloat](/documentation/swiftui/edgeinsets/bottom)
- [var leading: CGFloat](/documentation/swiftui/edgeinsets/leading)
- [var trailing: CGFloat](/documentation/swiftui/edgeinsets/trailing)

#### Creating an edge inset

- [init()](/documentation/swiftui/edgeinsets/init())
- [init(top: CGFloat, leading: CGFloat, bottom: CGFloat, trailing: CGFloat)](/documentation/swiftui/edgeinsets/init(top:leading:bottom:trailing:))
- [init(_:)](/documentation/swiftui/edgeinsets/init(_:))

#### Instance Methods

- [func inset(by: RectangleCornerInsets, edges: Edge.Set) -> EdgeInsets](/documentation/swiftui/edgeinsets/inset(by:edges:))
- [EdgeInsets3D](/documentation/swiftui/edgeinsets3d)

#### Getting edge insets

- [var top: CGFloat](/documentation/swiftui/edgeinsets3d/top)
- [var bottom: CGFloat](/documentation/swiftui/edgeinsets3d/bottom)
- [var leading: CGFloat](/documentation/swiftui/edgeinsets3d/leading)
- [var trailing: CGFloat](/documentation/swiftui/edgeinsets3d/trailing)
- [var front: CGFloat](/documentation/swiftui/edgeinsets3d/front)
- [var back: CGFloat](/documentation/swiftui/edgeinsets3d/back)

#### Creating an edge inset

- [init(horizontal: CGFloat, vertical: CGFloat, depth: CGFloat)](/documentation/swiftui/edgeinsets3d/init(horizontal:vertical:depth:))
- [init(top: CGFloat, leading: CGFloat, bottom: CGFloat, trailing: CGFloat, front: CGFloat, back: CGFloat)](/documentation/swiftui/edgeinsets3d/init(top:leading:bottom:trailing:front:back:))
- [Custom layout](/documentation/swiftui/custom-layout)

### Creating a custom layout container

- [Composing custom layouts with SwiftUI](/documentation/swiftui/composing-custom-layouts-with-swiftui)
- [Layout](/documentation/swiftui/layout)

#### Sizing the container and placing subviews

- [func sizeThatFits(proposal: ProposedViewSize, subviews: Self.Subviews, cache: inout Self.Cache) -> CGSize](/documentation/swiftui/layout/sizethatfits(proposal:subviews:cache:))
- [func placeSubviews(in: CGRect, proposal: ProposedViewSize, subviews: Self.Subviews, cache: inout Self.Cache)](/documentation/swiftui/layout/placesubviews(in:proposal:subviews:cache:))
- [Layout.Subviews](/documentation/swiftui/layout/subviews)

#### Reporting layout container characteristics

- [func explicitAlignment(of:in:proposal:subviews:cache:)](/documentation/swiftui/layout/explicitalignment(of:in:proposal:subviews:cache:))
- [func spacing(subviews: Self.Subviews, cache: inout Self.Cache) -> ViewSpacing](/documentation/swiftui/layout/spacing(subviews:cache:))
- [static var layoutProperties: LayoutProperties](/documentation/swiftui/layout/layoutproperties)

#### Managing a cache

- [func makeCache(subviews: Self.Subviews) -> Self.Cache](/documentation/swiftui/layout/makecache(subviews:))
- [func updateCache(inout Self.Cache, subviews: Self.Subviews)](/documentation/swiftui/layout/updatecache(_:subviews:))
- [Cache](/documentation/swiftui/layout/cache)

#### Supporting types

- [func callAsFunction<V>(() -> V) -> some View](/documentation/swiftui/layout/callasfunction(_:))

#### Instance Methods

- [func depthAlignment(DepthAlignment) -> some Layout](/documentation/swiftui/layout/depthalignment(_:))
- [func depthAlignment<Content>(DepthAlignment, content: () -> Content) -> some View](/documentation/swiftui/layout/depthalignment(_:content:))
- [LayoutSubview](/documentation/swiftui/layoutsubview)

#### Placing the subview

- [func place(at: CGPoint, anchor: UnitPoint, proposal: ProposedViewSize)](/documentation/swiftui/layoutsubview/place(at:anchor:proposal:))

#### Getting subview characteristics

- [func dimensions(in: ProposedViewSize) -> ViewDimensions](/documentation/swiftui/layoutsubview/dimensions(in:))
- [func sizeThatFits(ProposedViewSize) -> CGSize](/documentation/swiftui/layoutsubview/sizethatfits(_:))
- [var spacing: ViewSpacing](/documentation/swiftui/layoutsubview/spacing)
- [var priority: Double](/documentation/swiftui/layoutsubview/priority)

#### Getting custom values

- [subscript<K>(K.Type) -> K.Value](/documentation/swiftui/layoutsubview/subscript(_:))

#### Instance Properties

- [var containerValues: ContainerValues](/documentation/swiftui/layoutsubview/containervalues)
- [LayoutSubviews](/documentation/swiftui/layoutsubviews)

#### Getting the layout direction

- [var layoutDirection: LayoutDirection](/documentation/swiftui/layoutsubviews/layoutdirection)

#### Accessing subviews

- [subscript(_:)](/documentation/swiftui/layoutsubviews/subscript(_:))
- [var startIndex: Int](/documentation/swiftui/layoutsubviews/startindex)
- [var endIndex: Int](/documentation/swiftui/layoutsubviews/endindex)
- [LayoutSubviews.Element](/documentation/swiftui/layoutsubviews/element)
- [LayoutSubviews.Index](/documentation/swiftui/layoutsubviews/index)
- [LayoutSubviews.SubSequence](/documentation/swiftui/layoutsubviews/subsequence)

### Configuring a custom layout

- [LayoutProperties](/documentation/swiftui/layoutproperties)

#### Creating a layout properties instance

- [init()](/documentation/swiftui/layoutproperties/init())

#### Getting layout properties

- [var stackOrientation: Axis?](/documentation/swiftui/layoutproperties/stackorientation)
- [ProposedViewSize](/documentation/swiftui/proposedviewsize)

#### Getting standard proposals

- [static let zero: ProposedViewSize](/documentation/swiftui/proposedviewsize/zero)
- [static let infinity: ProposedViewSize](/documentation/swiftui/proposedviewsize/infinity)
- [static let unspecified: ProposedViewSize](/documentation/swiftui/proposedviewsize/unspecified)

#### Creating a custom size proposal

- [init(CGSize)](/documentation/swiftui/proposedviewsize/init(_:))
- [init(width: CGFloat?, height: CGFloat?)](/documentation/swiftui/proposedviewsize/init(width:height:))

#### Getting the proposal’s dimensions

- [var height: CGFloat?](/documentation/swiftui/proposedviewsize/height)
- [var width: CGFloat?](/documentation/swiftui/proposedviewsize/width)

#### Modifying a proposal

- [func replacingUnspecifiedDimensions(by: CGSize) -> CGSize](/documentation/swiftui/proposedviewsize/replacingunspecifieddimensions(by:))
- [ViewSpacing](/documentation/swiftui/viewspacing)

#### Creating spacing instances

- [init()](/documentation/swiftui/viewspacing/init())
- [static let zero: ViewSpacing](/documentation/swiftui/viewspacing/zero)

#### Measuring spacing distance

- [func distance(to: ViewSpacing, along: Axis) -> CGFloat](/documentation/swiftui/viewspacing/distance(to:along:))

#### Merging spacing instances

- [func formUnion(ViewSpacing, edges: Edge.Set)](/documentation/swiftui/viewspacing/formunion(_:edges:))
- [func union(ViewSpacing, edges: Edge.Set) -> ViewSpacing](/documentation/swiftui/viewspacing/union(_:edges:))

### Associating values with views in a custom layout

- [func layoutValue<K>(key: K.Type, value: K.Value) -> some View](/documentation/swiftui/view/layoutvalue(key:value:))
- [LayoutValueKey](/documentation/swiftui/layoutvaluekey)

#### Providing a default value

- [static var defaultValue: Self.Value](/documentation/swiftui/layoutvaluekey/defaultvalue)
- [Value](/documentation/swiftui/layoutvaluekey/value)

### Transitioning between layout types

- [AnyLayout](/documentation/swiftui/anylayout)

#### Creating the layout

- [init<L>(L)](/documentation/swiftui/anylayout/init(_:))
- [HStackLayout](/documentation/swiftui/hstacklayout)

#### Creating a horizontal stack

- [init(alignment: VerticalAlignment, spacing: CGFloat?)](/documentation/swiftui/hstacklayout/init(alignment:spacing:))

#### Getting the stack’s properties

- [var alignment: VerticalAlignment](/documentation/swiftui/hstacklayout/alignment)
- [var spacing: CGFloat?](/documentation/swiftui/hstacklayout/spacing)
- [VStackLayout](/documentation/swiftui/vstacklayout)

#### Creating a vertical stack

- [init(alignment: HorizontalAlignment, spacing: CGFloat?)](/documentation/swiftui/vstacklayout/init(alignment:spacing:))

#### Getting the stack’s properties

- [var alignment: HorizontalAlignment](/documentation/swiftui/vstacklayout/alignment)
- [var spacing: CGFloat?](/documentation/swiftui/vstacklayout/spacing)
- [ZStackLayout](/documentation/swiftui/zstacklayout)

#### Creating a stack

- [init(alignment: Alignment)](/documentation/swiftui/zstacklayout/init(alignment:))

#### Getting the stack’s properties

- [var alignment: Alignment](/documentation/swiftui/zstacklayout/alignment)
- [GridLayout](/documentation/swiftui/gridlayout)

#### Creating a grid

- [init(alignment: Alignment, horizontalSpacing: CGFloat?, verticalSpacing: CGFloat?)](/documentation/swiftui/gridlayout/init(alignment:horizontalspacing:verticalspacing:))

#### Getting the grid’s properties

- [var alignment: Alignment](/documentation/swiftui/gridlayout/alignment)
- [var horizontalSpacing: CGFloat?](/documentation/swiftui/gridlayout/horizontalspacing)
- [var verticalSpacing: CGFloat?](/documentation/swiftui/gridlayout/verticalspacing)

#### Type Aliases

- [GridLayout.Body](/documentation/swiftui/gridlayout/body)

#### Default Implementations

- [Layout Implementations](/documentation/swiftui/gridlayout/layout-implementations)

##### Structures

- [GridLayout.Cache](/documentation/swiftui/gridlayout/cache)
- [Lists](/documentation/swiftui/lists)

### Creating a list

- [Displaying data in lists](/documentation/swiftui/displaying-data-in-lists)
- [List](/documentation/swiftui/list)

#### Creating a list from a set of views

- [init(content: () -> Content)](/documentation/swiftui/list/init(content:))
- [init(selection:content:)](/documentation/swiftui/list/init(selection:content:))

#### Creating a list from enumerated data

- [init(_:rowContent:)](/documentation/swiftui/list/init(_:rowcontent:))
- [init(_:selection:rowContent:)](/documentation/swiftui/list/init(_:selection:rowcontent:))
- [init(_:id:rowContent:)](/documentation/swiftui/list/init(_:id:rowcontent:))
- [init(_:id:selection:rowContent:)](/documentation/swiftui/list/init(_:id:selection:rowcontent:))

#### Creating a list from hierarchical data

- [init(_:children:rowContent:)](/documentation/swiftui/list/init(_:children:rowcontent:))
- [init(_:children:selection:rowContent:)](/documentation/swiftui/list/init(_:children:selection:rowcontent:))
- [init(_:id:children:rowContent:)](/documentation/swiftui/list/init(_:id:children:rowcontent:))
- [init(_:id:children:selection:rowContent:)](/documentation/swiftui/list/init(_:id:children:selection:rowcontent:))

#### Creating a list from editable data

- [init<Data, RowContent>(Binding<Data>, editActions: EditActions<Data>, rowContent: (Binding<Data.Element>) -> RowContent)](/documentation/swiftui/list/init(_:editactions:rowcontent:))
- [init(_:editActions:selection:rowContent:)](/documentation/swiftui/list/init(_:editactions:selection:rowcontent:))
- [init<Data, ID, RowContent>(Binding<Data>, id: KeyPath<Data.Element, ID>, editActions: EditActions<Data>, rowContent: (Binding<Data.Element>) -> RowContent)](/documentation/swiftui/list/init(_:id:editactions:rowcontent:))
- [init(_:id:editActions:selection:rowContent:)](/documentation/swiftui/list/init(_:id:editactions:selection:rowcontent:))

#### Supporting types

- [var body: some View](/documentation/swiftui/list/body)
- [func listStyle<S>(S) -> some View](/documentation/swiftui/view/liststyle(_:))

### Disclosing information progressively

- [OutlineGroup](/documentation/swiftui/outlinegroup)

#### Creating an outline group

- [init(_:children:)](/documentation/swiftui/outlinegroup/init(_:children:))
- [init(_:children:content:)](/documentation/swiftui/outlinegroup/init(_:children:content:))
- [init(_:id:children:content:)](/documentation/swiftui/outlinegroup/init(_:id:children:content:))

#### Supporting types

- [OutlineSubgroupChildren](/documentation/swiftui/outlinesubgroupchildren)
- [DisclosureGroup](/documentation/swiftui/disclosuregroup)

#### Creating a disclosure group

- [init(_:content:)](/documentation/swiftui/disclosuregroup/init(_:content:))
- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/disclosuregroup/init(content:label:))
- [init(_:isExpanded:content:)](/documentation/swiftui/disclosuregroup/init(_:isexpanded:content:))
- [init(isExpanded: Binding<Bool>, content: () -> Content, label: () -> Label)](/documentation/swiftui/disclosuregroup/init(isexpanded:content:label:))
- [func disclosureGroupStyle<S>(S) -> some View](/documentation/swiftui/view/disclosuregroupstyle(_:))

### Configuring a list’s layout

- [func listRowInsets(EdgeInsets?) -> some View](/documentation/swiftui/view/listrowinsets(_:))
- [var defaultMinListRowHeight: CGFloat](/documentation/swiftui/environmentvalues/defaultminlistrowheight)
- [var defaultMinListHeaderHeight: CGFloat?](/documentation/swiftui/environmentvalues/defaultminlistheaderheight)
- [func listRowSpacing(CGFloat?) -> some View](/documentation/swiftui/view/listrowspacing(_:))
- [func listSectionSpacing(_:)](/documentation/swiftui/view/listsectionspacing(_:))
- [ListSectionSpacing](/documentation/swiftui/listsectionspacing)

#### Getting section spacing

- [static let `default`: ListSectionSpacing](/documentation/swiftui/listsectionspacing/default)
- [static let compact: ListSectionSpacing](/documentation/swiftui/listsectionspacing/compact)
- [static func custom(CGFloat) -> ListSectionSpacing](/documentation/swiftui/listsectionspacing/custom(_:))
- [func listSectionMargins(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/listsectionmargins(_:_:))

### Configuring rows

- [func listItemTint(_:)](/documentation/swiftui/view/listitemtint(_:))
- [ListItemTint](/documentation/swiftui/listitemtint)

#### Getting list item tint options

- [static let monochrome: ListItemTint](/documentation/swiftui/listitemtint/monochrome)
- [static func fixed(Color) -> ListItemTint](/documentation/swiftui/listitemtint/fixed(_:))
- [static func preferred(Color) -> ListItemTint](/documentation/swiftui/listitemtint/preferred(_:))

### Configuring headers

- [func headerProminence(Prominence) -> some View](/documentation/swiftui/view/headerprominence(_:))
- [var headerProminence: Prominence](/documentation/swiftui/environmentvalues/headerprominence)
- [Prominence](/documentation/swiftui/prominence)

#### Getting prominence options

- [case standard](/documentation/swiftui/prominence/standard)
- [case increased](/documentation/swiftui/prominence/increased)

### Configuring separators

- [func listRowSeparatorTint(Color?, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listrowseparatortint(_:edges:))
- [func listSectionSeparatorTint(Color?, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listsectionseparatortint(_:edges:))
- [func listRowSeparator(Visibility, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listrowseparator(_:edges:))
- [func listSectionSeparator(Visibility, edges: VerticalEdge.Set) -> some View](/documentation/swiftui/view/listsectionseparator(_:edges:))

### Configuring backgrounds

- [func listRowBackground<V>(V?) -> some View](/documentation/swiftui/view/listrowbackground(_:))
- [func alternatingRowBackgrounds(AlternatingRowBackgroundBehavior) -> some View](/documentation/swiftui/view/alternatingrowbackgrounds(_:))
- [AlternatingRowBackgroundBehavior](/documentation/swiftui/alternatingrowbackgroundbehavior)

#### Getting alternating row background behavior

- [static let automatic: AlternatingRowBackgroundBehavior](/documentation/swiftui/alternatingrowbackgroundbehavior/automatic)
- [static let enabled: AlternatingRowBackgroundBehavior](/documentation/swiftui/alternatingrowbackgroundbehavior/enabled)
- [static let disabled: AlternatingRowBackgroundBehavior](/documentation/swiftui/alternatingrowbackgroundbehavior/disabled)
- [var backgroundProminence: BackgroundProminence](/documentation/swiftui/environmentvalues/backgroundprominence)
- [BackgroundProminence](/documentation/swiftui/backgroundprominence)

#### Getting background prominence

- [static let standard: BackgroundProminence](/documentation/swiftui/backgroundprominence/standard)
- [static let increased: BackgroundProminence](/documentation/swiftui/backgroundprominence/increased)

### Displaying a badge on a list item

- [func badge(_:)](/documentation/swiftui/view/badge(_:))
- [func badgeProminence(BadgeProminence) -> some View](/documentation/swiftui/view/badgeprominence(_:))
- [var badgeProminence: BadgeProminence](/documentation/swiftui/environmentvalues/badgeprominence)
- [BadgeProminence](/documentation/swiftui/badgeprominence)

#### Getting background prominence

- [static let standard: BadgeProminence](/documentation/swiftui/badgeprominence/standard)
- [static let increased: BadgeProminence](/documentation/swiftui/badgeprominence/increased)
- [static let decreased: BadgeProminence](/documentation/swiftui/badgeprominence/decreased)

### Configuring interaction

- [func swipeActions<T>(edge: HorizontalEdge, allowsFullSwipe: Bool, content: () -> T) -> some View](/documentation/swiftui/view/swipeactions(edge:allowsfullswipe:content:))
- [func selectionDisabled(Bool) -> some View](/documentation/swiftui/view/selectiondisabled(_:))
- [func listRowHoverEffect(HoverEffect?) -> some View](/documentation/swiftui/view/listrowhovereffect(_:))
- [func listRowHoverEffectDisabled(Bool) -> some View](/documentation/swiftui/view/listrowhovereffectdisabled(_:))

### Refreshing a list’s content

- [func refreshable(action: () async -> Void) -> some View](/documentation/swiftui/view/refreshable(action:))
- [var refresh: RefreshAction?](/documentation/swiftui/environmentvalues/refresh)
- [RefreshAction](/documentation/swiftui/refreshaction)

#### Calling the action

- [func callAsFunction() async](/documentation/swiftui/refreshaction/callasfunction())

### Editing a list

- [func moveDisabled(Bool) -> some View](/documentation/swiftui/view/movedisabled(_:))
- [func deleteDisabled(Bool) -> some View](/documentation/swiftui/view/deletedisabled(_:))
- [var editMode: Binding<EditMode>?](/documentation/swiftui/environmentvalues/editmode)
- [EditMode](/documentation/swiftui/editmode)

#### Getting edit modes

- [case active](/documentation/swiftui/editmode/active)
- [case inactive](/documentation/swiftui/editmode/inactive)
- [case transient](/documentation/swiftui/editmode/transient)

#### Checking for editing mode

- [var isEditing: Bool](/documentation/swiftui/editmode/isediting)
- [EditActions](/documentation/swiftui/editactions)

#### Getting edit operations

- [static var all: EditActions<Data>](/documentation/swiftui/editactions/all-45m4m)
- [static var all: EditActions<Data>](/documentation/swiftui/editactions/all-4dctm)
- [static var all: EditActions<Data>](/documentation/swiftui/editactions/all-4uyun)
- [static var all: EditActions<Data>](/documentation/swiftui/editactions/all-6ryvk)
- [static var delete: EditActions<Data>](/documentation/swiftui/editactions/delete)
- [static var move: EditActions<Data>](/documentation/swiftui/editactions/move)

#### Creating an edit operation

- [init(rawValue: Int)](/documentation/swiftui/editactions/init(rawvalue:))
- [let rawValue: Int](/documentation/swiftui/editactions/rawvalue)
- [EditableCollectionContent](/documentation/swiftui/editablecollectioncontent)
- [IndexedIdentifierCollection](/documentation/swiftui/indexedidentifiercollection)

### Configuring a section index

- [func listSectionIndexVisibility(Visibility) -> some View](/documentation/swiftui/view/listsectionindexvisibility(_:))
- [func sectionIndexLabel(_:)](/documentation/swiftui/view/sectionindexlabel(_:))
- [Tables](/documentation/swiftui/tables)

### Creating a table

- [Building a great Mac app with SwiftUI](/documentation/swiftui/building-a-great-mac-app-with-swiftui)
- [Table](/documentation/swiftui/table)

#### Creating a table from columns

- [init<Data>(Data, columns: () -> Columns)](/documentation/swiftui/table/init(_:columns:))
- [init(_:selection:columns:)](/documentation/swiftui/table/init(_:selection:columns:))

#### Creating a sortable table from columns

- [init<Data, Sort>(Data, sortOrder: Binding<[Sort]>, columns: () -> Columns)](/documentation/swiftui/table/init(_:sortorder:columns:))
- [init(_:selection:sortOrder:columns:)](/documentation/swiftui/table/init(_:selection:sortorder:columns:))

#### Creating a table from columns and rows

- [init(of: Value.Type, columns: () -> Columns, rows: () -> Rows)](/documentation/swiftui/table/init(of:columns:rows:))
- [init(of:selection:columns:rows:)](/documentation/swiftui/table/init(of:selection:columns:rows:))

#### Creating a sortable table from columns and rows

- [init<Sort>(of: Value.Type, sortOrder: Binding<[Sort]>, columns: () -> Columns, rows: () -> Rows)](/documentation/swiftui/table/init(of:sortorder:columns:rows:))
- [init(of:selection:sortOrder:columns:rows:)](/documentation/swiftui/table/init(of:selection:sortorder:columns:rows:))
- [init<Sort>(sortOrder: Binding<[Sort]>, columns: () -> Columns, rows: () -> Rows)](/documentation/swiftui/table/init(sortorder:columns:rows:))
- [init(selection:sortOrder:columns:rows:)](/documentation/swiftui/table/init(selection:sortorder:columns:rows:))

#### Creating a table with customizable columns

- [init<Data>(Data, columnCustomization: Binding<TableColumnCustomization<Value>>, columns: () -> Columns)](/documentation/swiftui/table/init(_:columncustomization:columns:))
- [init(_:selection:columnCustomization:columns:)](/documentation/swiftui/table/init(_:selection:columncustomization:columns:))
- [init(_:selection:sortOrder:columnCustomization:columns:)](/documentation/swiftui/table/init(_:selection:sortorder:columncustomization:columns:))
- [init<Data, Sort>(Data, sortOrder: Binding<[Sort]>, columnCustomization: Binding<TableColumnCustomization<Value>>, columns: () -> Columns)](/documentation/swiftui/table/init(_:sortorder:columncustomization:columns:))

#### Creating a table with dynamically customizable columns

- [init(of: Value.Type, columnCustomization: Binding<TableColumnCustomization<Value>>, columns: () -> Columns, rows: () -> Rows)](/documentation/swiftui/table/init(of:columncustomization:columns:rows:))
- [init(of:selection:columnCustomization:columns:rows:)](/documentation/swiftui/table/init(of:selection:columncustomization:columns:rows:))
- [init(of:selection:sortOrder:columnCustomization:columns:rows:)](/documentation/swiftui/table/init(of:selection:sortorder:columncustomization:columns:rows:))
- [init<Sort>(of: Value.Type, sortOrder: Binding<[Sort]>, columnCustomization: Binding<TableColumnCustomization<Value>>, columns: () -> Columns, rows: () -> Rows)](/documentation/swiftui/table/init(of:sortorder:columncustomization:columns:rows:))

#### Creating a hierarchical table

- [init<Data>(Data, children: KeyPath<Value, Data?>, columnCustomization: Binding<TableColumnCustomization<Value>>?, columns: () -> Columns)](/documentation/swiftui/table/init(_:children:columncustomization:columns:))
- [init(_:children:selection:columnCustomization:columns:)](/documentation/swiftui/table/init(_:children:selection:columncustomization:columns:))
- [init(_:children:selection:sortOrder:columnCustomization:columns:)](/documentation/swiftui/table/init(_:children:selection:sortorder:columncustomization:columns:))
- [init<Data, Sort>(Data, children: KeyPath<Data.Element, Data?>, sortOrder: Binding<[Sort]>, columnCustomization: Binding<TableColumnCustomization<Value>>?, columns: () -> Columns)](/documentation/swiftui/table/init(_:children:sortorder:columncustomization:columns:))
- [func tableStyle<S>(S) -> some View](/documentation/swiftui/view/tablestyle(_:))

### Creating columns

- [TableColumn](/documentation/swiftui/tablecolumn)

#### Creating an unsortable column

- [init(_:value:)](/documentation/swiftui/tablecolumn/init(_:value:))
- [init(_:content:)](/documentation/swiftui/tablecolumn/init(_:content:))

#### Creating a sortable column

- [init(_:value:content:)](/documentation/swiftui/tablecolumn/init(_:value:content:))
- [init(_:value:comparator:)](/documentation/swiftui/tablecolumn/init(_:value:comparator:))
- [init(_:value:comparator:content:)](/documentation/swiftui/tablecolumn/init(_:value:comparator:content:))
- [init(_:sortUsing:content:)](/documentation/swiftui/tablecolumn/init(_:sortusing:content:))

#### Setting the column width

- [func width(CGFloat?) -> TableColumn<RowValue, Sort, Content, Label>](/documentation/swiftui/tablecolumn/width(_:))
- [func width(min: CGFloat?, ideal: CGFloat?, max: CGFloat?) -> TableColumn<RowValue, Sort, Content, Label>](/documentation/swiftui/tablecolumn/width(min:ideal:max:))
- [func width() -> TableColumn<RowValue, Sort, Content, Label>](/documentation/swiftui/tablecolumn/width())
- [TableColumnContent](/documentation/swiftui/tablecolumncontent)

#### Getting the column body

- [var tableColumnBody: Self.TableColumnBody](/documentation/swiftui/tablecolumncontent/tablecolumnbody-swift.property)
- [TableColumnBody](/documentation/swiftui/tablecolumncontent/tablecolumnbody-swift.associatedtype)

#### Defining the row value

- [TableRowValue](/documentation/swiftui/tablecolumncontent/tablerowvalue)

#### Defining the comparator

- [TableColumnSortComparator](/documentation/swiftui/tablecolumncontent/tablecolumnsortcomparator)

#### Configuring the content

- [func alignment(TableColumnAlignment) -> some TableColumnContent<Self.TableRowValue, Self.TableColumnSortComparator>
](/documentation/swiftui/tablecolumncontent/alignment(_:))
- [func customizationID(String) -> some TableColumnContent<Self.TableRowValue, Self.TableColumnSortComparator>
](/documentation/swiftui/tablecolumncontent/customizationid(_:))
- [func defaultVisibility(Visibility) -> some TableColumnContent<Self.TableRowValue, Self.TableColumnSortComparator>
](/documentation/swiftui/tablecolumncontent/defaultvisibility(_:))
- [func disabledCustomizationBehavior(TableColumnCustomizationBehavior) -> some TableColumnContent<Self.TableRowValue, Self.TableColumnSortComparator>
](/documentation/swiftui/tablecolumncontent/disabledcustomizationbehavior(_:))
- [TableColumnAlignment](/documentation/swiftui/tablecolumnalignment)

#### Getting the alignment

- [static var automatic: TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/automatic)
- [static var leading: TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/leading)
- [static var center: TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/center)
- [static var trailing: TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/trailing)
- [static var numeric: TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/numeric)
- [static func numeric(Locale.NumberingSystem) -> TableColumnAlignment](/documentation/swiftui/tablecolumnalignment/numeric(_:))
- [TableColumnBuilder](/documentation/swiftui/tablecolumnbuilder)

#### Building a column

- [static buildBlock(_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:))
- [static buildBlock(_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:))
- [static buildBlock(_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:))
- [static buildBlock(_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:))
- [static buildBlock(_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static buildBlock(_:_:_:_:_:_:_:_:_:_:)](/documentation/swiftui/tablecolumnbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))
- [static buildExpression(_:)](/documentation/swiftui/tablecolumnbuilder/buildexpression(_:))

#### Supporting types

- [TupleTableColumnContent](/documentation/swiftui/tupletablecolumncontent)

##### Accessing the value

- [var value: T](/documentation/swiftui/tupletablecolumncontent/value)

#### Type Methods

- [static buildEither(first:)](/documentation/swiftui/tablecolumnbuilder/buildeither(first:))
- [static buildEither(second:)](/documentation/swiftui/tablecolumnbuilder/buildeither(second:))
- [static buildIf(_:)](/documentation/swiftui/tablecolumnbuilder/buildif(_:))
- [static buildLimitedAvailability(_:)](/documentation/swiftui/tablecolumnbuilder/buildlimitedavailability(_:))
- [TableColumnForEach](/documentation/swiftui/tablecolumnforeach)

#### Creating the collection

- [init(_:content:)](/documentation/swiftui/tablecolumnforeach/init(_:content:))
- [init(Data, id: KeyPath<Data.Element, ID>, content: (Data.Element) -> Content)](/documentation/swiftui/tablecolumnforeach/init(_:id:content:))

#### Accessing collection content

- [var content: (Data.Element) -> Content](/documentation/swiftui/tablecolumnforeach/content)
- [var data: Data](/documentation/swiftui/tablecolumnforeach/data)

### Customizing columns

- [func tableColumnHeaders(Visibility) -> some View](/documentation/swiftui/view/tablecolumnheaders(_:))
- [TableColumnCustomization](/documentation/swiftui/tablecolumncustomization)

#### Creating a table column customization

- [init()](/documentation/swiftui/tablecolumncustomization/init())

#### Managing the customization

- [func resetOrder()](/documentation/swiftui/tablecolumncustomization/resetorder())
- [subscript(visibility _: String) -> Visibility](/documentation/swiftui/tablecolumncustomization/subscript(visibility:))
- [TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior)

#### Getting the customization behavior

- [static var all: TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior/all)
- [static let reorder: TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior/reorder)
- [static let resize: TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior/resize)
- [static let visibility: TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior/visibility)

#### Creating a behavior

- [init()](/documentation/swiftui/tablecolumncustomizationbehavior/init())

### Creating rows

- [TableRow](/documentation/swiftui/tablerow)

#### Creating a row

- [init(Value)](/documentation/swiftui/tablerow/init(_:))
- [TableRowContent](/documentation/swiftui/tablerowcontent)

#### Getting the row body

- [var tableRowBody: Self.TableRowBody](/documentation/swiftui/tablerowcontent/tablerowbody-swift.property)
- [TableRowBody](/documentation/swiftui/tablerowcontent/tablerowbody-swift.associatedtype)

#### Defining the row value

- [TableRowValue](/documentation/swiftui/tablerowcontent/tablerowvalue)

#### Managing interaction

- [func draggable<T>(@autoclosure () -> T) -> some TableRowContent<Self.TableRowValue>
](/documentation/swiftui/tablerowcontent/draggable(_:))
- [func dropDestination<T>(for: T.Type, action: ([T]) -> Void) -> some TableRowContent<Self.TableRowValue>
](/documentation/swiftui/tablerowcontent/dropdestination(for:action:))
- [func onHover(perform: (Bool) -> Void) -> some TableRowContent<Self.TableRowValue>
](/documentation/swiftui/tablerowcontent/onhover(perform:))
- [func itemProvider((() -> NSItemProvider?)?) -> ModifiedContent<Self, ItemProviderTableRowModifier>](/documentation/swiftui/tablerowcontent/itemprovider(_:))
- [ItemProviderTableRowModifier](/documentation/swiftui/itemprovidertablerowmodifier)

##### Instance Properties

- [var body: some _TableRowContentModifier](/documentation/swiftui/itemprovidertablerowmodifier/body-swift.property)

##### Type Aliases

- [ItemProviderTableRowModifier.Body](/documentation/swiftui/itemprovidertablerowmodifier/body-swift.typealias)

#### Adding a context menu to a row

- [func contextMenu<M>(menuItems: () -> M) -> ModifiedContent<Self, _ContextMenuTableRowModifier<M>>](/documentation/swiftui/tablerowcontent/contextmenu(menuitems:))
- [func contextMenu<M, P>(menuItems: () -> M, preview: () -> P) -> ModifiedContent<Self, _ContextMenuPreviewTableRowModifier<M, P>>](/documentation/swiftui/tablerowcontent/contextmenu(menuitems:preview:))

#### Instance Methods

- [func selectionDisabled(Bool) -> some TableRowContent<Self.TableRowValue>
](/documentation/swiftui/tablerowcontent/selectiondisabled(_:))
- [TableHeaderRowContent](/documentation/swiftui/tableheaderrowcontent)
- [TupleTableRowContent](/documentation/swiftui/tupletablerowcontent)

#### Accessing the value

- [var value: T](/documentation/swiftui/tupletablerowcontent/value)
- [TableForEachContent](/documentation/swiftui/tableforeachcontent)
- [EmptyTableRowContent](/documentation/swiftui/emptytablerowcontent)
- [DynamicTableRowContent](/documentation/swiftui/dynamictablerowcontent)

#### Getting row data

- [var data: Self.Data](/documentation/swiftui/dynamictablerowcontent/data-swift.property)
- [Data](/documentation/swiftui/dynamictablerowcontent/data-swift.associatedtype)

#### Inserting rows

- [func onInsert(of: [UTType], perform: (Int, [NSItemProvider]) -> Void) -> ModifiedContent<Self, OnInsertTableRowModifier>](/documentation/swiftui/dynamictablerowcontent/oninsert(of:perform:))
- [OnInsertTableRowModifier](/documentation/swiftui/oninserttablerowmodifier)

##### Instance Properties

- [var body: some _TableRowContentModifier](/documentation/swiftui/oninserttablerowmodifier/body-swift.property)

##### Type Aliases

- [OnInsertTableRowModifier.Body](/documentation/swiftui/oninserttablerowmodifier/body-swift.typealias)

#### Supporting drag and drop

- [func dropDestination<T>(for: T.Type, action: (Int, [T]) -> Void) -> ModifiedContent<Self, OnInsertTableRowModifier>](/documentation/swiftui/dynamictablerowcontent/dropdestination(for:action:))
- [TableRowBuilder](/documentation/swiftui/tablerowbuilder)

#### Building a row from sources

- [static func buildBlock<C>(C) -> C](/documentation/swiftui/tablerowbuilder/buildblock(_:))
- [static func buildBlock<C0, C1>(C0, C1) -> TupleTableRowContent<Value, (C0, C1)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:))
- [static func buildBlock<C0, C1, C2>(C0, C1, C2) -> TupleTableRowContent<Value, (C0, C1, C2)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:))
- [static func buildBlock<C0, C1, C2, C3>(C0, C1, C2, C3) -> TupleTableRowContent<Value, (C0, C1, C2, C3)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4>(C0, C1, C2, C3, C4) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5>(C0, C1, C2, C3, C4, C5) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4, C5)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6>(C0, C1, C2, C3, C4, C5, C6) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4, C5, C6)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7>(C0, C1, C2, C3, C4, C5, C6, C7) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4, C5, C6, C7)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8>(C0, C1, C2, C3, C4, C5, C6, C7, C8) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4, C5, C6, C7, C8)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:_:_:_:_:))
- [static func buildBlock<C0, C1, C2, C3, C4, C5, C6, C7, C8, C9>(C0, C1, C2, C3, C4, C5, C6, C7, C8, C9) -> TupleTableRowContent<Value, (C0, C1, C2, C3, C4, C5, C6, C7, C8, C9)>](/documentation/swiftui/tablerowbuilder/buildblock(_:_:_:_:_:_:_:_:_:_:))

#### Building a row from conditionals

- [static func buildIf<C>(C?) -> C?](/documentation/swiftui/tablerowbuilder/buildif(_:))
- [static func buildEither<T, F>(first: T) -> _ConditionalContent<T, F>](/documentation/swiftui/tablerowbuilder/buildeither(first:))
- [static func buildEither<T, F>(second: F) -> _ConditionalContent<T, F>](/documentation/swiftui/tablerowbuilder/buildeither(second:))
- [static func buildExpression<Content>(Content) -> Content](/documentation/swiftui/tablerowbuilder/buildexpression(_:))

### Adding progressive disclosure

- [DisclosureTableRow](/documentation/swiftui/disclosuretablerow)

#### Creating a disclosure table row

- [init<Value>(Value, isExpanded: Binding<Bool>?, content: () -> Content)](/documentation/swiftui/disclosuretablerow/init(_:isexpanded:content:))
- [TableOutlineGroupContent](/documentation/swiftui/tableoutlinegroupcontent)
- [View groupings](/documentation/swiftui/view-groupings)

### Grouping views into a container

- [Creating custom container views](/documentation/swiftui/creating-custom-container-views)
- [Group](/documentation/swiftui/group)

#### Creating a group

- [init(content:)](/documentation/swiftui/group/init(content:))

#### Initializers

- [init<Base, Result>(sections: Base, transform: (SectionCollection) -> Result)](/documentation/swiftui/group/init(sections:transform:))
- [init<Base, Result>(subviews: Base, transform: (SubviewsCollection) -> Result)](/documentation/swiftui/group/init(subviews:transform:))
- [GroupElementsOfContent](/documentation/swiftui/groupelementsofcontent)
- [GroupSectionsOfContent](/documentation/swiftui/groupsectionsofcontent)

### Organizing views into sections

- [Section](/documentation/swiftui/section)

#### Creating a section

- [init(content:)](/documentation/swiftui/section/init(content:))
- [init(_:content:)](/documentation/swiftui/section/init(_:content:))

#### Adding headers and footers

- [init(content:header:)](/documentation/swiftui/section/init(content:header:))
- [init(content: () -> Content, footer: () -> Footer)](/documentation/swiftui/section/init(content:footer:))
- [init(content: () -> Content, header: () -> Parent, footer: () -> Footer)](/documentation/swiftui/section/init(content:header:footer:))

#### Controlling collapsibility

- [init(_:isExpanded:content:)](/documentation/swiftui/section/init(_:isexpanded:content:))
- [init(isExpanded:content:header:)](/documentation/swiftui/section/init(isexpanded:content:header:))

#### Deprecated symbols

- [init(header: Parent, content: () -> Content)](/documentation/swiftui/section/init(header:content:))
- [init(footer: Footer, content: () -> Content)](/documentation/swiftui/section/init(footer:content:))
- [init(header: Parent, footer: Footer, content: () -> Content)](/documentation/swiftui/section/init(header:footer:content:))
- [func collapsible(Bool) -> some View](/documentation/swiftui/section/collapsible(_:))
- [SectionCollection](/documentation/swiftui/sectioncollection)
- [SectionConfiguration](/documentation/swiftui/sectionconfiguration)

#### Structures

- [SectionConfiguration.Actions](/documentation/swiftui/sectionconfiguration/actions-swift.struct)
- [SectionConfiguration.ID](/documentation/swiftui/sectionconfiguration/id-swift.struct)

#### Instance Properties

- [var actions: SectionConfiguration.Actions](/documentation/swiftui/sectionconfiguration/actions-swift.property)
- [var containerValues: ContainerValues](/documentation/swiftui/sectionconfiguration/containervalues)
- [var content: SubviewsCollection](/documentation/swiftui/sectionconfiguration/content)
- [var footer: SubviewsCollection](/documentation/swiftui/sectionconfiguration/footer)
- [var header: SubviewsCollection](/documentation/swiftui/sectionconfiguration/header)
- [var id: SectionConfiguration.ID](/documentation/swiftui/sectionconfiguration/id-swift.property)

### Iterating over dynamic data

- [ForEach](/documentation/swiftui/foreach)

#### Creating a collection

- [init(Data)](/documentation/swiftui/foreach/init(_:))
- [init(_:content:)](/documentation/swiftui/foreach/init(_:content:))
- [init(_:id:content:)](/documentation/swiftui/foreach/init(_:id:content:))

#### Creating an editable collection

- [init<C, R>(Binding<C>, editActions: EditActions<C>, content: (Binding<C.Element>) -> R)](/documentation/swiftui/foreach/init(_:editactions:content:))
- [init<C, R>(Binding<C>, id: KeyPath<C.Element, ID>, editActions: EditActions<C>, content: (Binding<C.Element>) -> R)](/documentation/swiftui/foreach/init(_:id:editactions:content:))

#### Accessing content

- [var content: (Data.Element) -> Content](/documentation/swiftui/foreach/content)
- [var data: Data](/documentation/swiftui/foreach/data)

#### Initializers

- [init<V>(sections: V, content: (SectionConfiguration) -> Content)](/documentation/swiftui/foreach/init(sections:content:))
- [init<V>(subviews: V, content: (Subview) -> Content)](/documentation/swiftui/foreach/init(subviews:content:))
- [ForEachSectionCollection](/documentation/swiftui/foreachsectioncollection)
- [ForEachSubviewCollection](/documentation/swiftui/foreachsubviewcollection)
- [DynamicViewContent](/documentation/swiftui/dynamicviewcontent)

#### Managing the data

- [var data: Self.Data](/documentation/swiftui/dynamicviewcontent/data-swift.property)
- [Data](/documentation/swiftui/dynamicviewcontent/data-swift.associatedtype)

#### Responding to updates

- [func onDelete(perform: Optional<(IndexSet) -> Void>) -> some DynamicViewContent](/documentation/swiftui/dynamicviewcontent/ondelete(perform:))
- [func onInsert(of: [UTType], perform: (Int, [NSItemProvider]) -> Void) -> some DynamicViewContent](/documentation/swiftui/dynamicviewcontent/oninsert(of:perform:)-418bq)
- [func onMove(perform: Optional<(IndexSet, Int) -> Void>) -> some DynamicViewContent](/documentation/swiftui/dynamicviewcontent/onmove(perform:))
- [func dropDestination<T>(for: T.Type, action: ([T], Int) -> Void) -> some DynamicViewContent](/documentation/swiftui/dynamicviewcontent/dropdestination(for:action:))

#### Deprecated symbols

- [func onInsert(of: [String], perform: (Int, [NSItemProvider]) -> Void) -> some DynamicViewContent](/documentation/swiftui/dynamicviewcontent/oninsert(of:perform:)-40hwa)

#### Instance Methods

- [func onInsert(of:perform:)](/documentation/swiftui/dynamicviewcontent/oninsert(of:perform:))

### Accessing a container’s subviews

- [Subview](/documentation/swiftui/subview)

#### Structures

- [Subview.ID](/documentation/swiftui/subview/id-swift.struct)

#### Instance Properties

- [var containerValues: ContainerValues](/documentation/swiftui/subview/containervalues)
- [var id: Subview.ID](/documentation/swiftui/subview/id-swift.property)

#### Enumerations

- [Subview.ContainerSizingOptions](/documentation/swiftui/subview/containersizingoptions)

##### Enumeration Cases

- [case uniform(axis: Axis.Set)](/documentation/swiftui/subview/containersizingoptions/uniform(axis:))
- [case variable](/documentation/swiftui/subview/containersizingoptions/variable)
- [SubviewsCollection](/documentation/swiftui/subviewscollection)
- [SubviewsCollectionSlice](/documentation/swiftui/subviewscollectionslice)
- [func containerValue<V>(WritableKeyPath<ContainerValues, V>, V) -> some View](/documentation/swiftui/view/containervalue(_:_:))
- [ContainerValues](/documentation/swiftui/containervalues)

#### Instance Methods

- [func hasTag<V>(V) -> Bool](/documentation/swiftui/containervalues/hastag(_:))
- [func tag<V>(for: V.Type) -> V?](/documentation/swiftui/containervalues/tag(for:))

#### Subscripts

- [subscript<Key>(Key.Type) -> Key.Value](/documentation/swiftui/containervalues/subscript(_:))
- [ContainerValueKey](/documentation/swiftui/containervaluekey)

#### Associated Types

- [Value](/documentation/swiftui/containervaluekey/value)

#### Type Properties

- [static var defaultValue: Self.Value](/documentation/swiftui/containervaluekey/defaultvalue)

### Grouping views into a box

- [GroupBox](/documentation/swiftui/groupbox)

#### Creating a group box

- [init(content: () -> Content)](/documentation/swiftui/groupbox/init(content:))
- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/groupbox/init(content:label:))
- [init(_:content:)](/documentation/swiftui/groupbox/init(_:content:))

#### Creating a group box from a configuration

- [init(GroupBoxStyleConfiguration)](/documentation/swiftui/groupbox/init(_:))

#### Deprecated initializers

- [init(label: Label, content: () -> Content)](/documentation/swiftui/groupbox/init(label:content:))
- [func groupBoxStyle<S>(S) -> some View](/documentation/swiftui/view/groupboxstyle(_:))

### Grouping inputs

- [Form](/documentation/swiftui/form)

#### Creating a form

- [init(content: () -> Content)](/documentation/swiftui/form/init(content:))

#### Creating a form from a configuration

- [init(FormStyleConfiguration)](/documentation/swiftui/form/init(_:))
- [func formStyle<S>(S) -> some View](/documentation/swiftui/view/formstyle(_:))
- [LabeledContent](/documentation/swiftui/labeledcontent)

#### Creating labeled content

- [init(_:content:)](/documentation/swiftui/labeledcontent/init(_:content:))
- [init(content: () -> Content, label: () -> Label)](/documentation/swiftui/labeledcontent/init(content:label:))
- [init(_:value:)](/documentation/swiftui/labeledcontent/init(_:value:))
- [init(_:value:format:)](/documentation/swiftui/labeledcontent/init(_:value:format:))
- [init(LabeledContentStyleConfiguration)](/documentation/swiftui/labeledcontent/init(_:))
- [func labeledContentStyle<S>(S) -> some View](/documentation/swiftui/view/labeledcontentstyle(_:))

### Presenting a group of controls

- [ControlGroup](/documentation/swiftui/controlgroup)

#### Creating a control group

- [init(content: () -> Content)](/documentation/swiftui/controlgroup/init(content:))
- [init<C, L>(content: () -> C, label: () -> L)](/documentation/swiftui/controlgroup/init(content:label:))
- [init(_:content:)](/documentation/swiftui/controlgroup/init(_:content:))

#### Creating a control group with an image

- [init(_:image:content:)](/documentation/swiftui/controlgroup/init(_:image:content:))
- [init(_:systemImage:content:)](/documentation/swiftui/controlgroup/init(_:systemimage:content:))

#### Creating a configured control group

- [init(ControlGroupStyleConfiguration)](/documentation/swiftui/controlgroup/init(_:))

#### Supporting types

- [LabeledControlGroupContent](/documentation/swiftui/labeledcontrolgroupcontent)
- [func controlGroupStyle<S>(S) -> some View](/documentation/swiftui/view/controlgroupstyle(_:))
- [Scroll views](/documentation/swiftui/scroll-views)

### Creating a scroll view

- [ScrollView](/documentation/swiftui/scrollview)

#### Creating a scroll view

- [init(Axis.Set, showsIndicators: Bool, content: () -> Content)](/documentation/swiftui/scrollview/init(_:showsindicators:content:))
- [init(Axis.Set, content: () -> Content)](/documentation/swiftui/scrollview/init(_:content:))

#### Configuring a scroll view

- [var content: Content](/documentation/swiftui/scrollview/content)
- [var axes: Axis.Set](/documentation/swiftui/scrollview/axes)
- [var showsIndicators: Bool](/documentation/swiftui/scrollview/showsindicators)

#### Supporting types

- [var body: some View](/documentation/swiftui/scrollview/body)
- [ScrollViewReader](/documentation/swiftui/scrollviewreader)

#### Creating a scroll view reader

- [init(content: (ScrollViewProxy) -> Content)](/documentation/swiftui/scrollviewreader/init(content:))

#### Configuring a scroll view reader

- [var content: (ScrollViewProxy) -> Content](/documentation/swiftui/scrollviewreader/content)
- [ScrollViewProxy](/documentation/swiftui/scrollviewproxy)

#### Performing scrolling

- [func scrollTo<ID>(ID, anchor: UnitPoint?)](/documentation/swiftui/scrollviewproxy/scrollto(_:anchor:))

### Managing scroll position

- [func scrollPosition(Binding<ScrollPosition>, anchor: UnitPoint?) -> some View](/documentation/swiftui/view/scrollposition(_:anchor:))
- [func scrollPosition(id: Binding<(some Hashable)?>, anchor: UnitPoint?) -> some View](/documentation/swiftui/view/scrollposition(id:anchor:))
- [func defaultScrollAnchor(UnitPoint?) -> some View](/documentation/swiftui/view/defaultscrollanchor(_:))
- [func defaultScrollAnchor(UnitPoint?, for: ScrollAnchorRole) -> some View](/documentation/swiftui/view/defaultscrollanchor(_:for:))
- [ScrollAnchorRole](/documentation/swiftui/scrollanchorrole)

#### Type Properties

- [static var alignment: ScrollAnchorRole](/documentation/swiftui/scrollanchorrole/alignment)
- [static var initialOffset: ScrollAnchorRole](/documentation/swiftui/scrollanchorrole/initialoffset)
- [static var sizeChanges: ScrollAnchorRole](/documentation/swiftui/scrollanchorrole/sizechanges)
- [ScrollPosition](/documentation/swiftui/scrollposition)

#### Initializers

- [init(id: some Hashable & Sendable, anchor: UnitPoint?)](/documentation/swiftui/scrollposition/init(id:anchor:))
- [init(idType: (some Hashable & Sendable).Type)](/documentation/swiftui/scrollposition/init(idtype:))
- [init(idType: (some Hashable & Sendable).Type, edge: Edge)](/documentation/swiftui/scrollposition/init(idtype:edge:))
- [init(idType: (some Hashable & Sendable).Type, point: CGPoint)](/documentation/swiftui/scrollposition/init(idtype:point:))
- [init(idType: (some Hashable & Sendable).Type, x: CGFloat)](/documentation/swiftui/scrollposition/init(idtype:x:))
- [init(idType: (some Hashable & Sendable).Type, x: CGFloat, y: CGFloat)](/documentation/swiftui/scrollposition/init(idtype:x:y:))
- [init(idType: (some Hashable & Sendable).Type, y: CGFloat)](/documentation/swiftui/scrollposition/init(idtype:y:))

#### Instance Properties

- [var edge: Edge?](/documentation/swiftui/scrollposition/edge)
- [var isPositionedByUser: Bool](/documentation/swiftui/scrollposition/ispositionedbyuser)
- [var point: CGPoint?](/documentation/swiftui/scrollposition/point)
- [var viewID: (any Hashable & Sendable)?](/documentation/swiftui/scrollposition/viewid)
- [var x: CGFloat?](/documentation/swiftui/scrollposition/x)
- [var y: CGFloat?](/documentation/swiftui/scrollposition/y)

#### Instance Methods

- [func scrollTo(edge: Edge)](/documentation/swiftui/scrollposition/scrollto(edge:))
- [func scrollTo(id: some Hashable & Sendable, anchor: UnitPoint?)](/documentation/swiftui/scrollposition/scrollto(id:anchor:))
- [func scrollTo(point: CGPoint)](/documentation/swiftui/scrollposition/scrollto(point:))
- [func scrollTo(x: CGFloat)](/documentation/swiftui/scrollposition/scrollto(x:))
- [func scrollTo(x: CGFloat, y: CGFloat)](/documentation/swiftui/scrollposition/scrollto(x:y:))
- [func scrollTo(y: CGFloat)](/documentation/swiftui/scrollposition/scrollto(y:))
- [func viewID<T>(type: T.Type) -> T?](/documentation/swiftui/scrollposition/viewid(type:))

### Defining scroll targets

- [func scrollTargetBehavior(some ScrollTargetBehavior) -> some View](/documentation/swiftui/view/scrolltargetbehavior(_:))
- [func scrollTargetLayout(isEnabled: Bool) -> some View](/documentation/swiftui/view/scrolltargetlayout(isenabled:))
- [ScrollTarget](/documentation/swiftui/scrolltarget)

#### Getting the scroll target

- [var anchor: UnitPoint?](/documentation/swiftui/scrolltarget/anchor)
- [var rect: CGRect](/documentation/swiftui/scrolltarget/rect)
- [ScrollTargetBehavior](/documentation/swiftui/scrolltargetbehavior)

#### Getting the scroll target behavior

- [static var paging: PagingScrollTargetBehavior](/documentation/swiftui/scrolltargetbehavior/paging)
- [static var viewAligned: ViewAlignedScrollTargetBehavior](/documentation/swiftui/scrolltargetbehavior/viewaligned)
- [static func viewAligned(limitBehavior: ViewAlignedScrollTargetBehavior.LimitBehavior) -> Self](/documentation/swiftui/scrolltargetbehavior/viewaligned(limitbehavior:))

#### Updating the proposed target

- [func updateTarget(inout ScrollTarget, context: Self.TargetContext)](/documentation/swiftui/scrolltargetbehavior/updatetarget(_:context:))
- [ScrollTargetBehavior.TargetContext](/documentation/swiftui/scrolltargetbehavior/targetcontext)

#### Instance Methods

- [func properties(context: Self.PropertiesContext) -> Self.Properties](/documentation/swiftui/scrolltargetbehavior/properties(context:))

#### Type Aliases

- [ScrollTargetBehavior.Properties](/documentation/swiftui/scrolltargetbehavior/properties)
- [ScrollTargetBehavior.PropertiesContext](/documentation/swiftui/scrolltargetbehavior/propertiescontext)

#### Type Methods

- [static func viewAligned(anchor: UnitPoint?) -> Self](/documentation/swiftui/scrolltargetbehavior/viewaligned(anchor:))
- [static func viewAligned(limitBehavior: ViewAlignedScrollTargetBehavior.LimitBehavior, anchor: UnitPoint?) -> Self](/documentation/swiftui/scrolltargetbehavior/viewaligned(limitbehavior:anchor:))
- [ScrollTargetBehaviorContext](/documentation/swiftui/scrolltargetbehaviorcontext)

#### Getting the scroll target behavior context

- [var axes: Axis.Set](/documentation/swiftui/scrolltargetbehaviorcontext/axes)
- [var containerSize: CGSize](/documentation/swiftui/scrolltargetbehaviorcontext/containersize)
- [var contentSize: CGSize](/documentation/swiftui/scrolltargetbehaviorcontext/contentsize)
- [var originalTarget: ScrollTarget](/documentation/swiftui/scrolltargetbehaviorcontext/originaltarget)
- [var velocity: CGVector](/documentation/swiftui/scrolltargetbehaviorcontext/velocity)

#### Accessing the context

- [subscript<T>(dynamicMember _: KeyPath<EnvironmentValues, T>) -> T](/documentation/swiftui/scrolltargetbehaviorcontext/subscript(dynamicmember:))
- [PagingScrollTargetBehavior](/documentation/swiftui/pagingscrolltargetbehavior)

#### Creating the target behavior

- [init()](/documentation/swiftui/pagingscrolltargetbehavior/init())
- [ViewAlignedScrollTargetBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior)

#### Creating the target behavior

- [init(limitBehavior: ViewAlignedScrollTargetBehavior.LimitBehavior)](/documentation/swiftui/viewalignedscrolltargetbehavior/init(limitbehavior:))
- [ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior)

##### Getting the limit behavior

- [static var automatic: ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior/automatic)
- [static var always: ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior/always)
- [static var never: ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior/never)

##### Type Properties

- [static var alwaysByFew: ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior/alwaysbyfew)
- [static var alwaysByOne: ViewAlignedScrollTargetBehavior.LimitBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior/limitbehavior/alwaysbyone)

#### Initializers

- [init(anchor: UnitPoint?)](/documentation/swiftui/viewalignedscrolltargetbehavior/init(anchor:))
- [init(limitBehavior: ViewAlignedScrollTargetBehavior.LimitBehavior, anchor: UnitPoint?)](/documentation/swiftui/viewalignedscrolltargetbehavior/init(limitbehavior:anchor:))
- [AnyScrollTargetBehavior](/documentation/swiftui/anyscrolltargetbehavior)

#### Initializers

- [init(some ScrollTargetBehavior)](/documentation/swiftui/anyscrolltargetbehavior/init(_:))

#### Instance Properties

- [var base: any ScrollTargetBehavior](/documentation/swiftui/anyscrolltargetbehavior/base)
- [ScrollTargetBehaviorProperties](/documentation/swiftui/scrolltargetbehaviorproperties)

#### Initializers

- [init()](/documentation/swiftui/scrolltargetbehaviorproperties/init())

#### Instance Properties

- [var limitsScrolls: Bool](/documentation/swiftui/scrolltargetbehaviorproperties/limitsscrolls)
- [ScrollTargetBehaviorPropertiesContext](/documentation/swiftui/scrolltargetbehaviorpropertiescontext)

#### Instance Properties

- [var axes: Axis.Set](/documentation/swiftui/scrolltargetbehaviorpropertiescontext/axes)
- [var environment: EnvironmentValues](/documentation/swiftui/scrolltargetbehaviorpropertiescontext/environment)

### Animating scroll transitions

- [func scrollTransition(ScrollTransitionConfiguration, axis: Axis?, transition: (EmptyVisualEffect, ScrollTransitionPhase) -> some VisualEffect) -> some View](/documentation/swiftui/view/scrolltransition(_:axis:transition:))
- [func scrollTransition(topLeading: ScrollTransitionConfiguration, bottomTrailing: ScrollTransitionConfiguration, axis: Axis?, transition: (EmptyVisualEffect, ScrollTransitionPhase) -> some VisualEffect) -> some View](/documentation/swiftui/view/scrolltransition(topleading:bottomtrailing:axis:transition:))
- [ScrollTransitionPhase](/documentation/swiftui/scrolltransitionphase)

#### Getting the phase

- [case identity](/documentation/swiftui/scrolltransitionphase/identity)
- [case topLeading](/documentation/swiftui/scrolltransitionphase/topleading)
- [case bottomTrailing](/documentation/swiftui/scrolltransitionphase/bottomtrailing)

#### Accessing the phase state

- [var isIdentity: Bool](/documentation/swiftui/scrolltransitionphase/isidentity)
- [var value: Double](/documentation/swiftui/scrolltransitionphase/value)
- [ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration)

#### Getting the configuration

- [static let identity: ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/identity)
- [static let animated: ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/animated)
- [static func animated(Animation) -> ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/animated(_:))
- [static let interactive: ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/interactive)
- [static func interactive(timingCurve: UnitCurve) -> ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/interactive(timingcurve:))

#### Accessing the configuration

- [func animation(Animation) -> ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/animation(_:))
- [func threshold(ScrollTransitionConfiguration.Threshold) -> ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration/threshold(_:))
- [ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold)

##### Getting the threshold

- [static var centered: ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/centered)
- [static let hidden: ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/hidden)
- [static let visible: ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/visible)
- [static func visible(Double) -> ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/visible(_:))

##### Modifying the threshold

- [func inset(by: Double) -> ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/inset(by:))
- [func interpolated(towards: ScrollTransitionConfiguration.Threshold, amount: Double) -> ScrollTransitionConfiguration.Threshold](/documentation/swiftui/scrolltransitionconfiguration/threshold/interpolated(towards:amount:))

### Responding to scroll view changes

- [func onScrollGeometryChange<T>(for: T.Type, of: (ScrollGeometry) -> T, action: (T, T) -> Void) -> some View](/documentation/swiftui/view/onscrollgeometrychange(for:of:action:))
- [func onScrollTargetVisibilityChange<ID>(idType: ID.Type, threshold: Double, ([ID]) -> Void) -> some View](/documentation/swiftui/view/onscrolltargetvisibilitychange(idtype:threshold:_:))
- [func onScrollVisibilityChange(threshold: Double, (Bool) -> Void) -> some View](/documentation/swiftui/view/onscrollvisibilitychange(threshold:_:))
- [func onScrollPhaseChange(_:)](/documentation/swiftui/view/onscrollphasechange(_:))
- [ScrollGeometry](/documentation/swiftui/scrollgeometry)

#### Initializers

- [init(contentOffset: CGPoint, contentSize: CGSize, contentInsets: EdgeInsets, containerSize: CGSize)](/documentation/swiftui/scrollgeometry/init(contentoffset:contentsize:contentinsets:containersize:))

#### Instance Properties

- [var bounds: CGRect](/documentation/swiftui/scrollgeometry/bounds)
- [var containerSize: CGSize](/documentation/swiftui/scrollgeometry/containersize)
- [var contentInsets: EdgeInsets](/documentation/swiftui/scrollgeometry/contentinsets)
- [var contentOffset: CGPoint](/documentation/swiftui/scrollgeometry/contentoffset)
- [var contentSize: CGSize](/documentation/swiftui/scrollgeometry/contentsize)
- [var visibleRect: CGRect](/documentation/swiftui/scrollgeometry/visiblerect)
- [ScrollPhase](/documentation/swiftui/scrollphase)

#### Getting scroll gesture states

- [case animating](/documentation/swiftui/scrollphase/animating)
- [case decelerating](/documentation/swiftui/scrollphase/decelerating)
- [case idle](/documentation/swiftui/scrollphase/idle)
- [case interacting](/documentation/swiftui/scrollphase/interacting)
- [case tracking](/documentation/swiftui/scrollphase/tracking)

#### Checking for active scrolling

- [var isScrolling: Bool](/documentation/swiftui/scrollphase/isscrolling)
- [ScrollPhaseChangeContext](/documentation/swiftui/scrollphasechangecontext)

#### Instance Properties

- [var geometry: ScrollGeometry](/documentation/swiftui/scrollphasechangecontext/geometry)
- [var velocity: CGVector?](/documentation/swiftui/scrollphasechangecontext/velocity)

### Showing scroll indicators

- [func scrollIndicatorsFlash(onAppear: Bool) -> some View](/documentation/swiftui/view/scrollindicatorsflash(onappear:))
- [func scrollIndicatorsFlash(trigger: some Equatable) -> some View](/documentation/swiftui/view/scrollindicatorsflash(trigger:))
- [func scrollIndicators(ScrollIndicatorVisibility, axes: Axis.Set) -> some View](/documentation/swiftui/view/scrollindicators(_:axes:))
- [var horizontalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/horizontalscrollindicatorvisibility)
- [var verticalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/verticalscrollindicatorvisibility)
- [ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility)

#### Getting visibilties

- [static var automatic: ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility/automatic)
- [static var hidden: ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility/hidden)
- [static var never: ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility/never)
- [static var visible: ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility/visible)

### Managing content visibility

- [func scrollContentBackground(Visibility) -> some View](/documentation/swiftui/view/scrollcontentbackground(_:))
- [func scrollClipDisabled(Bool) -> some View](/documentation/swiftui/view/scrollclipdisabled(_:))
- [ScrollContentOffsetAdjustmentBehavior](/documentation/swiftui/scrollcontentoffsetadjustmentbehavior)

#### Type Properties

- [static var automatic: ScrollContentOffsetAdjustmentBehavior](/documentation/swiftui/scrollcontentoffsetadjustmentbehavior/automatic)
- [static var disabled: ScrollContentOffsetAdjustmentBehavior](/documentation/swiftui/scrollcontentoffsetadjustmentbehavior/disabled)

### Disabling scrolling

- [func scrollDisabled(Bool) -> some View](/documentation/swiftui/view/scrolldisabled(_:))
- [var isScrollEnabled: Bool](/documentation/swiftui/environmentvalues/isscrollenabled)

### Configuring scroll bounce behavior

- [func scrollBounceBehavior(ScrollBounceBehavior, axes: Axis.Set) -> some View](/documentation/swiftui/view/scrollbouncebehavior(_:axes:))
- [var horizontalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/horizontalscrollbouncebehavior)
- [var verticalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/verticalscrollbouncebehavior)
- [ScrollBounceBehavior](/documentation/swiftui/scrollbouncebehavior)

#### Bounce behaviors

- [static var automatic: ScrollBounceBehavior](/documentation/swiftui/scrollbouncebehavior/automatic)
- [static var always: ScrollBounceBehavior](/documentation/swiftui/scrollbouncebehavior/always)
- [static var basedOnSize: ScrollBounceBehavior](/documentation/swiftui/scrollbouncebehavior/basedonsize)

### Configuring scroll edge effects

- [func scrollEdgeEffectStyle(ScrollEdgeEffectStyle?, for: Edge.Set) -> some View](/documentation/swiftui/view/scrolledgeeffectstyle(_:for:))
- [func scrollEdgeEffectHidden(Bool, for: Edge.Set) -> some View](/documentation/swiftui/view/scrolledgeeffecthidden(_:for:))
- [ScrollEdgeEffectStyle](/documentation/swiftui/scrolledgeeffectstyle)

#### Type Properties

- [static var automatic: ScrollEdgeEffectStyle](/documentation/swiftui/scrolledgeeffectstyle/automatic)
- [static var hard: ScrollEdgeEffectStyle](/documentation/swiftui/scrolledgeeffectstyle/hard)
- [static var soft: ScrollEdgeEffectStyle](/documentation/swiftui/scrolledgeeffectstyle/soft)
- [func safeAreaBar(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareabar(edge:alignment:spacing:content:))

### Interacting with a software keyboard

- [func scrollDismissesKeyboard(ScrollDismissesKeyboardMode) -> some View](/documentation/swiftui/view/scrolldismisseskeyboard(_:))
- [var scrollDismissesKeyboardMode: ScrollDismissesKeyboardMode](/documentation/swiftui/environmentvalues/scrolldismisseskeyboardmode)
- [ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode)

#### Getting modes

- [static var automatic: ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode/automatic)
- [static var immediately: ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode/immediately)
- [static var interactively: ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode/interactively)
- [static var never: ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode/never)

### Managing scrolling for different inputs

- [func scrollInputBehavior(ScrollInputBehavior, for: ScrollInputKind) -> some View](/documentation/swiftui/view/scrollinputbehavior(_:for:))
- [ScrollInputKind](/documentation/swiftui/scrollinputkind)

#### Type Properties

- [static let handGestureShortcut: ScrollInputKind](/documentation/swiftui/scrollinputkind/handgestureshortcut)
- [static let look: ScrollInputKind](/documentation/swiftui/scrollinputkind/look)

#### Type Methods

- [static func look(axes: Axis.Set) -> ScrollInputKind](/documentation/swiftui/scrollinputkind/look(axes:))
- [ScrollInputBehavior](/documentation/swiftui/scrollinputbehavior)

#### Type Properties

- [static let automatic: ScrollInputBehavior](/documentation/swiftui/scrollinputbehavior/automatic)
- [static let disabled: ScrollInputBehavior](/documentation/swiftui/scrollinputbehavior/disabled)
- [static let enabled: ScrollInputBehavior](/documentation/swiftui/scrollinputbehavior/enabled)

