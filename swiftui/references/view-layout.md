# View Layout — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [View layout](#view-layout)
- [Layout adjustments](#layout-adjustments)
- [Custom layout](#custom-layout)
- [Lists](#lists)
- [Tables](#tables)
- [View groupings](#view-groupings)
- [Scroll views](#scroll-views)

---
## View layout

- [Layout fundamentals](/documentation/swiftui/layout-fundamentals) (article)

### Choosing a layout

- [Picking container views for your content](/documentation/swiftui/picking-container-views-for-your-content) (article)

### Statically arranging views in one dimension

- [Building layouts with stack views](/documentation/swiftui/building-layouts-with-stack-views) (article)
- [HStack](/documentation/swiftui/hstack) — horizontal stack container
- [VStack](/documentation/swiftui/vstack) — vertical stack container

### Dynamically arranging views in one dimension

- [Grouping data with lazy stack views](/documentation/swiftui/grouping-data-with-lazy-stack-views) (article)
- [Creating performant scrollable stacks](/documentation/swiftui/creating-performant-scrollable-stacks) (article)
- [LazyHStack](/documentation/swiftui/lazyhstack) — lazy-loading horizontal stack
- [LazyVStack](/documentation/swiftui/lazyvstack) — lazy-loading vertical stack
- [PinnedScrollableViews](/documentation/swiftui/pinnedscrollableviews) — pin headers/footers in lazy stacks

### Statically arranging views in two dimensions

- [Grid](/documentation/swiftui/grid) — static two-dimensional grid container
- [GridRow](/documentation/swiftui/gridrow) — row within a Grid
- [func gridCellColumns(Int) -> some View](/documentation/swiftui/view/gridcellcolumns(_:))
- [func gridCellAnchor(UnitPoint) -> some View](/documentation/swiftui/view/gridcellanchor(_:))
- [func gridCellUnsizedAxes(Axis.Set) -> some View](/documentation/swiftui/view/gridcellunsizedaxes(_:))
- [func gridColumnAlignment(HorizontalAlignment) -> some View](/documentation/swiftui/view/gridcolumnalignment(_:))

### Dynamically arranging views in two dimensions

- [LazyHGrid](/documentation/swiftui/lazyhgrid) — lazy horizontal grid with row definitions
- [LazyVGrid](/documentation/swiftui/lazyvgrid) — lazy vertical grid with column definitions
- [GridItem](/documentation/swiftui/griditem) — sizing config for lazy grid rows/columns (adaptive, fixed, flexible)

### Layering views

- [Adding a background to your view](/documentation/swiftui/adding-a-background-to-your-view) (article)
- [ZStack](/documentation/swiftui/zstack) — overlapping stack container
- [ZStackContent3D](/documentation/swiftui/zstackcontent3d) — 3D ZStack support
- [func zIndex(Double) -> some View](/documentation/swiftui/view/zindex(_:))
- [func background(alignment:content:)](/documentation/swiftui/view/background(alignment:content:))
- [func background(_:ignoresSafeAreaEdges:)](/documentation/swiftui/view/background(_:ignoressafeareaedges:))
- [func background(ignoresSafeAreaEdges:)](/documentation/swiftui/view/background(ignoressafeareaedges:))
- [func background(_:in:fillStyle:)](/documentation/swiftui/view/background(_:in:fillstyle:))
- [func background(in:fillStyle:)](/documentation/swiftui/view/background(in:fillstyle:))
- [func overlay(alignment:content:)](/documentation/swiftui/view/overlay(alignment:content:))
- [func overlay(_:ignoresSafeAreaEdges:)](/documentation/swiftui/view/overlay(_:ignoressafeareaedges:))
- [func overlay(_:in:fillStyle:)](/documentation/swiftui/view/overlay(_:in:fillstyle:))
- [var backgroundMaterial: Material?](/documentation/swiftui/environmentvalues/backgroundmaterial)
- [func containerBackground(_:for:)](/documentation/swiftui/view/containerbackground(_:for:))
- [func containerBackground(for:alignment:content:)](/documentation/swiftui/view/containerbackground(for:alignment:content:))
- [ContainerBackgroundPlacement](/documentation/swiftui/containerbackgroundplacement) — placement targets: navigation, tabView, widget, subscriptionStore, window

### Automatically choosing the layout that fits

- [ViewThatFits](/documentation/swiftui/viewthatfits) — picks first child that fits available space

### Separators

- [Spacer](/documentation/swiftui/spacer) — flexible space in a stack
- [Divider](/documentation/swiftui/divider) — visual separator line

---
## Layout adjustments

- [Layout adjustments](/documentation/swiftui/layout-adjustments) (article)

### Fine-tuning a layout

- [Laying out a simple view](/documentation/swiftui/laying-out-a-simple-view) (article)
- [Inspecting view layout](/documentation/swiftui/inspecting-view-layout) (article)

### Adding padding around a view

- [func padding(_:)](/documentation/swiftui/view/padding(_:))
- [func padding(Edge.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding(_:_:))
- [func padding3D(_:)](/documentation/swiftui/view/padding3d(_:))
- [func padding3D(Edge3D.Set, CGFloat?) -> some View](/documentation/swiftui/view/padding3d(_:_:))
- [func scenePadding(Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:))
- [func scenePadding(ScenePadding, edges: Edge.Set) -> some View](/documentation/swiftui/view/scenepadding(_:edges:))
- [ScenePadding](/documentation/swiftui/scenepadding) — scene-level padding values (minimum, navigationBar)

### Influencing a view's size

- [func frame(width:height:alignment:)](/documentation/swiftui/view/frame(width:height:alignment:))
- [func frame(depth:alignment:)](/documentation/swiftui/view/frame(depth:alignment:))
- [func frame(minWidth:idealWidth:maxWidth:minHeight:idealHeight:maxHeight:alignment:)](/documentation/swiftui/view/frame(minwidth:idealwidth:maxwidth:minheight:idealheight:maxheight:alignment:))
- [func frame(minDepth:idealDepth:maxDepth:alignment:)](/documentation/swiftui/view/frame(mindepth:idealdepth:maxdepth:alignment:))
- [func containerRelativeFrame(_:alignment:)](/documentation/swiftui/view/containerrelativeframe(_:alignment:))
- [func containerRelativeFrame(_:alignment:_:)](/documentation/swiftui/view/containerrelativeframe(_:alignment:_:))
- [func containerRelativeFrame(_:count:span:spacing:alignment:)](/documentation/swiftui/view/containerrelativeframe(_:count:span:spacing:alignment:))
- [func fixedSize() -> some View](/documentation/swiftui/view/fixedsize())
- [func fixedSize(horizontal:vertical:)](/documentation/swiftui/view/fixedsize(horizontal:vertical:))
- [func layoutPriority(Double) -> some View](/documentation/swiftui/view/layoutpriority(_:))

### Adjusting a view's position

- [Making fine adjustments to a view's position](/documentation/swiftui/making-fine-adjustments-to-a-view-s-position) (article)
- [func position(_:)](/documentation/swiftui/view/position(_:))
- [func position(x:y:)](/documentation/swiftui/view/position(x:y:))
- [func offset(_:)](/documentation/swiftui/view/offset(_:))
- [func offset(x:y:)](/documentation/swiftui/view/offset(x:y:))
- [func offset(z:)](/documentation/swiftui/view/offset(z:))

### Aligning views

- [Aligning views within a stack](/documentation/swiftui/aligning-views-within-a-stack) (article)
- [Aligning views across stacks](/documentation/swiftui/aligning-views-across-stacks) (article)
- [func alignmentGuide(_:computeValue:)](/documentation/swiftui/view/alignmentguide(_:computevalue:))
- [Alignment](/documentation/swiftui/alignment) — 2D alignment (topLeading, center, bottomTrailing, etc.)
- [HorizontalAlignment](/documentation/swiftui/horizontalalignment) — horizontal guide (leading, center, trailing)
- [VerticalAlignment](/documentation/swiftui/verticalalignment) — vertical guide (top, center, bottom, firstTextBaseline, lastTextBaseline)
- [DepthAlignment](/documentation/swiftui/depthalignment) — depth guide (back, center, front)
- [AlignmentID](/documentation/swiftui/alignmentid) — protocol for custom alignment guides
- [ViewDimensions](/documentation/swiftui/viewdimensions) — width/height of a view for alignment calculations
- [ViewDimensions3D](/documentation/swiftui/viewdimensions3d) — 3D view dimensions
- [SpatialContainer](/documentation/swiftui/spatialcontainer) — 3D spatial container

### Setting margins

- [func contentMargins(_:for:)](/documentation/swiftui/view/contentmargins(_:for:))
- [func contentMargins(_:_:for:)](/documentation/swiftui/view/contentmargins(_:_:for:))
- [ContentMarginPlacement](/documentation/swiftui/contentmarginplacement) — automatic, scrollContent, scrollIndicators

### Staying in the safe areas

- [func ignoresSafeArea(_:edges:)](/documentation/swiftui/view/ignoressafearea(_:edges:))
- [func safeAreaInset(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareainset(edge:alignment:spacing:content:))
- [func safeAreaPadding(_:)](/documentation/swiftui/view/safeareapadding(_:))
- [func safeAreaPadding(_:_:)](/documentation/swiftui/view/safeareapadding(_:_:))
- [SafeAreaRegions](/documentation/swiftui/safearearegions) — all, container, keyboard

### Setting a layout direction

- [func layoutDirectionBehavior(_:)](/documentation/swiftui/view/layoutdirectionbehavior(_:))
- [LayoutDirectionBehavior](/documentation/swiftui/layoutdirectionbehavior) — fixed or mirrors layout direction
- [var layoutDirection: LayoutDirection](/documentation/swiftui/environmentvalues/layoutdirection)
- [LayoutDirection](/documentation/swiftui/layoutdirection) — leftToRight, rightToLeft
- [LayoutRotationUnaryLayout](/documentation/swiftui/layoutrotationunarylayout)

### Reacting to interface characteristics

- [var isLuminanceReduced: Bool](/documentation/swiftui/environmentvalues/isluminancereduced)
- [var displayScale: CGFloat](/documentation/swiftui/environmentvalues/displayscale)
- [var pixelLength: CGFloat](/documentation/swiftui/environmentvalues/pixellength)
- [var horizontalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/horizontalsizeclass)
- [var verticalSizeClass: UserInterfaceSizeClass?](/documentation/swiftui/environmentvalues/verticalsizeclass)
- [UserInterfaceSizeClass](/documentation/swiftui/userinterfacesizeclass) — compact, regular

### Accessing edges, regions, and layouts

- [Edge](/documentation/swiftui/edge) — top, bottom, leading, trailing
- [Edge.Set](/documentation/swiftui/edge/set) — edge set combinations (all, horizontal, vertical)
- [Edge.Corner](/documentation/swiftui/edge/corner) — corner positions
- [Edge.Corner.Set](/documentation/swiftui/edge/corner/set) — corner set combinations
- [Edge.Corner.Style](/documentation/swiftui/edge/corner/style) — corner styling (concentric, fixed)
- [Edge3D](/documentation/swiftui/edge3d) — 3D edges (top, bottom, leading, trailing, front, back)
- [Edge3D.Set](/documentation/swiftui/edge3d/set) — 3D edge set combinations
- [HorizontalEdge](/documentation/swiftui/horizontaledge) — leading, trailing
- [HorizontalEdge.Set](/documentation/swiftui/horizontaledge/set)
- [VerticalEdge](/documentation/swiftui/verticaledge) — top, bottom
- [VerticalEdge.Set](/documentation/swiftui/verticaledge/set)
- [EdgeInsets](/documentation/swiftui/edgeinsets) — insets for top, leading, bottom, trailing
- [EdgeInsets3D](/documentation/swiftui/edgeinsets3d) — 3D edge insets including front, back

---
## Custom layout

- [Custom layout](/documentation/swiftui/custom-layout) (article)

### Creating a custom layout container

- [Composing custom layouts with SwiftUI](/documentation/swiftui/composing-custom-layouts-with-swiftui) (article)
- [Layout](/documentation/swiftui/layout) — protocol for custom layout containers (sizeThatFits, placeSubviews)
- [LayoutSubview](/documentation/swiftui/layoutsubview) — proxy for a single subview in a custom layout
- [LayoutSubviews](/documentation/swiftui/layoutsubviews) — collection of layout subview proxies

### Configuring a custom layout

- [LayoutProperties](/documentation/swiftui/layoutproperties) — properties of a layout container (stackOrientation)
- [ProposedViewSize](/documentation/swiftui/proposedviewsize) — proposed size for layout (zero, infinity, unspecified)
- [ViewSpacing](/documentation/swiftui/viewspacing) — preferred spacing around a view

### Associating values with views in a custom layout

- [func layoutValue(key:value:)](/documentation/swiftui/view/layoutvalue(key:value:))
- [LayoutValueKey](/documentation/swiftui/layoutvaluekey) — protocol for custom layout values

### Transitioning between layout types

- [AnyLayout](/documentation/swiftui/anylayout) — type-erased layout for animated transitions
- [HStackLayout](/documentation/swiftui/hstacklayout) — Layout-conforming HStack
- [VStackLayout](/documentation/swiftui/vstacklayout) — Layout-conforming VStack
- [ZStackLayout](/documentation/swiftui/zstacklayout) — Layout-conforming ZStack
- [GridLayout](/documentation/swiftui/gridlayout) — Layout-conforming Grid

---
## Lists

- [Lists](/documentation/swiftui/lists) (article)

### Creating a list

- [Displaying data in lists](/documentation/swiftui/displaying-data-in-lists) (article)
- [List](/documentation/swiftui/list) — scrollable list container from views, data, or hierarchical data
- [func listStyle(_:)](/documentation/swiftui/view/liststyle(_:))

### Disclosing information progressively

- [OutlineGroup](/documentation/swiftui/outlinegroup) — recursive disclosure of hierarchical data
- [OutlineSubgroupChildren](/documentation/swiftui/outlinesubgroupchildren)
- [DisclosureGroup](/documentation/swiftui/disclosuregroup) — expandable/collapsible content group
- [func disclosureGroupStyle(_:)](/documentation/swiftui/view/disclosuregroupstyle(_:))

### Configuring a list's layout

- [func listRowInsets(_:)](/documentation/swiftui/view/listrowinsets(_:))
- [var defaultMinListRowHeight: CGFloat](/documentation/swiftui/environmentvalues/defaultminlistrowheight)
- [var defaultMinListHeaderHeight: CGFloat?](/documentation/swiftui/environmentvalues/defaultminlistheaderheight)
- [func listRowSpacing(_:)](/documentation/swiftui/view/listrowspacing(_:))
- [func listSectionSpacing(_:)](/documentation/swiftui/view/listsectionspacing(_:))
- [ListSectionSpacing](/documentation/swiftui/listsectionspacing) — default, compact, custom
- [func listSectionMargins(_:_:)](/documentation/swiftui/view/listsectionmargins(_:_:))

### Configuring rows

- [func listItemTint(_:)](/documentation/swiftui/view/listitemtint(_:))
- [ListItemTint](/documentation/swiftui/listitemtint) — monochrome, fixed, preferred

### Configuring headers

- [func headerProminence(_:)](/documentation/swiftui/view/headerprominence(_:))
- [var headerProminence: Prominence](/documentation/swiftui/environmentvalues/headerprominence)
- [Prominence](/documentation/swiftui/prominence) — standard, increased

### Configuring separators

- [func listRowSeparatorTint(_:edges:)](/documentation/swiftui/view/listrowseparatortint(_:edges:))
- [func listSectionSeparatorTint(_:edges:)](/documentation/swiftui/view/listsectionseparatortint(_:edges:))
- [func listRowSeparator(_:edges:)](/documentation/swiftui/view/listrowseparator(_:edges:))
- [func listSectionSeparator(_:edges:)](/documentation/swiftui/view/listsectionseparator(_:edges:))

### Configuring backgrounds

- [func listRowBackground(_:)](/documentation/swiftui/view/listrowbackground(_:))
- [func alternatingRowBackgrounds(_:)](/documentation/swiftui/view/alternatingrowbackgrounds(_:))
- [AlternatingRowBackgroundBehavior](/documentation/swiftui/alternatingrowbackgroundbehavior) — automatic, enabled, disabled
- [var backgroundProminence: BackgroundProminence](/documentation/swiftui/environmentvalues/backgroundprominence)
- [BackgroundProminence](/documentation/swiftui/backgroundprominence) — standard, increased

### Displaying a badge on a list item

- [func badge(_:)](/documentation/swiftui/view/badge(_:))
- [func badgeProminence(_:)](/documentation/swiftui/view/badgeprominence(_:))
- [var badgeProminence: BadgeProminence](/documentation/swiftui/environmentvalues/badgeprominence)
- [BadgeProminence](/documentation/swiftui/badgeprominence) — standard, increased, decreased

### Configuring interaction

- [func swipeActions(edge:allowsFullSwipe:content:)](/documentation/swiftui/view/swipeactions(edge:allowsfullswipe:content:))
- [func selectionDisabled(_:)](/documentation/swiftui/view/selectiondisabled(_:))
- [func listRowHoverEffect(_:)](/documentation/swiftui/view/listrowhovereffect(_:))
- [func listRowHoverEffectDisabled(_:)](/documentation/swiftui/view/listrowhovereffectdisabled(_:))

### Refreshing a list's content

- [func refreshable(action:)](/documentation/swiftui/view/refreshable(action:))
- [var refresh: RefreshAction?](/documentation/swiftui/environmentvalues/refresh)
- [RefreshAction](/documentation/swiftui/refreshaction) — async refresh callable

### Editing a list

- [func moveDisabled(_:)](/documentation/swiftui/view/movedisabled(_:))
- [func deleteDisabled(_:)](/documentation/swiftui/view/deletedisabled(_:))
- [var editMode: Binding<EditMode>?](/documentation/swiftui/environmentvalues/editmode)
- [EditMode](/documentation/swiftui/editmode) — active, inactive, transient
- [EditActions](/documentation/swiftui/editactions) — all, delete, move
- [EditableCollectionContent](/documentation/swiftui/editablecollectioncontent)
- [IndexedIdentifierCollection](/documentation/swiftui/indexedidentifiercollection)

### Configuring a section index

- [func listSectionIndexVisibility(_:)](/documentation/swiftui/view/listsectionindexvisibility(_:))
- [func sectionIndexLabel(_:)](/documentation/swiftui/view/sectionindexlabel(_:))

---
## Tables

- [Tables](/documentation/swiftui/tables) (article)

### Creating a table

- [Building a great Mac app with SwiftUI](/documentation/swiftui/building-a-great-mac-app-with-swiftui) (article)
- [Table](/documentation/swiftui/table) — multi-column data table (sortable, hierarchical, customizable columns)
- [func tableStyle(_:)](/documentation/swiftui/view/tablestyle(_:))

### Creating columns

- [TableColumn](/documentation/swiftui/tablecolumn) — single column definition (sortable, width-configurable)
- [TableColumnContent](/documentation/swiftui/tablecolumncontent) — protocol for column content
- [TableColumnAlignment](/documentation/swiftui/tablecolumnalignment) — automatic, leading, center, trailing, numeric
- [TableColumnBuilder](/documentation/swiftui/tablecolumnbuilder) — result builder for columns
- [TupleTableColumnContent](/documentation/swiftui/tupletablecolumncontent)
- [TableColumnForEach](/documentation/swiftui/tablecolumnforeach) — dynamic column generation

### Customizing columns

- [func tableColumnHeaders(_:)](/documentation/swiftui/view/tablecolumnheaders(_:))
- [TableColumnCustomization](/documentation/swiftui/tablecolumncustomization) — persisted column order/visibility
- [TableColumnCustomizationBehavior](/documentation/swiftui/tablecolumncustomizationbehavior) — reorder, resize, visibility

### Creating rows

- [TableRow](/documentation/swiftui/tablerow) — single table row
- [TableRowContent](/documentation/swiftui/tablerowcontent) — protocol for row content
- [TableHeaderRowContent](/documentation/swiftui/tableheaderrowcontent)
- [TupleTableRowContent](/documentation/swiftui/tupletablerowcontent)
- [TableForEachContent](/documentation/swiftui/tableforeachcontent)
- [EmptyTableRowContent](/documentation/swiftui/emptytablerowcontent)
- [DynamicTableRowContent](/documentation/swiftui/dynamictablerowcontent) — protocol for dynamic row content with drag/drop
- [ItemProviderTableRowModifier](/documentation/swiftui/itemprovidertablerowmodifier)
- [OnInsertTableRowModifier](/documentation/swiftui/oninserttablerowmodifier)
- [TableRowBuilder](/documentation/swiftui/tablerowbuilder) — result builder for rows

### Adding progressive disclosure

- [DisclosureTableRow](/documentation/swiftui/disclosuretablerow) — expandable row in a table
- [TableOutlineGroupContent](/documentation/swiftui/tableoutlinegroupcontent)

---
## View groupings

- [View groupings](/documentation/swiftui/view-groupings) (article)

### Grouping views into a container

- [Creating custom container views](/documentation/swiftui/creating-custom-container-views) (article)
- [Group](/documentation/swiftui/group) — transparent container that groups views without affecting layout
- [GroupElementsOfContent](/documentation/swiftui/groupelementsofcontent)
- [GroupSectionsOfContent](/documentation/swiftui/groupsectionsofcontent)

### Organizing views into sections

- [Section](/documentation/swiftui/section) — labeled section with optional header/footer, collapsible
- [SectionCollection](/documentation/swiftui/sectioncollection)
- [SectionConfiguration](/documentation/swiftui/sectionconfiguration) — section header/footer/content config
- [init(header:content:)](/documentation/swiftui/section/init(header:content:)) [deprecated]
- [init(footer:content:)](/documentation/swiftui/section/init(footer:content:)) [deprecated]
- [init(header:footer:content:)](/documentation/swiftui/section/init(header:footer:content:)) [deprecated]
- [func collapsible(_:)](/documentation/swiftui/section/collapsible(_:)) [deprecated]

### Iterating over dynamic data

- [ForEach](/documentation/swiftui/foreach) — creates views from identified data collections
- [ForEachSectionCollection](/documentation/swiftui/foreachsectioncollection)
- [ForEachSubviewCollection](/documentation/swiftui/foreachsubviewcollection)
- [DynamicViewContent](/documentation/swiftui/dynamicviewcontent) — protocol for dynamic collections (onDelete, onMove, onInsert)
- [func onInsert(of:perform:)](/documentation/swiftui/dynamicviewcontent/oninsert(of:perform:)-40hwa) [deprecated]

### Accessing a container's subviews

- [Subview](/documentation/swiftui/subview) — proxy for a single subview in a custom container
- [SubviewsCollection](/documentation/swiftui/subviewscollection) — collection of subview proxies
- [SubviewsCollectionSlice](/documentation/swiftui/subviewscollectionslice)
- [func containerValue(_:_:)](/documentation/swiftui/view/containervalue(_:_:))
- [ContainerValues](/documentation/swiftui/containervalues) — per-subview values in custom containers
- [ContainerValueKey](/documentation/swiftui/containervaluekey) — protocol for custom container value keys

### Grouping views into a box

- [GroupBox](/documentation/swiftui/groupbox) — bordered content box with optional label
- [func groupBoxStyle(_:)](/documentation/swiftui/view/groupboxstyle(_:))

### Grouping inputs

- [Form](/documentation/swiftui/form) — container for data entry controls
- [func formStyle(_:)](/documentation/swiftui/view/formstyle(_:))
- [LabeledContent](/documentation/swiftui/labeledcontent) — label-value pair for forms
- [func labeledContentStyle(_:)](/documentation/swiftui/view/labeledcontentstyle(_:))

### Presenting a group of controls

- [ControlGroup](/documentation/swiftui/controlgroup) — grouped set of controls
- [LabeledControlGroupContent](/documentation/swiftui/labeledcontrolgroupcontent)
- [func controlGroupStyle(_:)](/documentation/swiftui/view/controlgroupstyle(_:))

---
## Scroll views

- [Scroll views](/documentation/swiftui/scroll-views) (article)

### Creating a scroll view

- [ScrollView](/documentation/swiftui/scrollview) — scrollable content container
- [ScrollViewReader](/documentation/swiftui/scrollviewreader) — programmatic scroll access
- [ScrollViewProxy](/documentation/swiftui/scrollviewproxy) — proxy for scrollTo operations

### Managing scroll position

- [func scrollPosition(_:anchor:)](/documentation/swiftui/view/scrollposition(_:anchor:))
- [func scrollPosition(id:anchor:)](/documentation/swiftui/view/scrollposition(id:anchor:))
- [func defaultScrollAnchor(_:)](/documentation/swiftui/view/defaultscrollanchor(_:))
- [func defaultScrollAnchor(_:for:)](/documentation/swiftui/view/defaultscrollanchor(_:for:))
- [ScrollAnchorRole](/documentation/swiftui/scrollanchorrole) — alignment, initialOffset, sizeChanges
- [ScrollPosition](/documentation/swiftui/scrollposition) — programmatic scroll position state

### Defining scroll targets

- [func scrollTargetBehavior(_:)](/documentation/swiftui/view/scrolltargetbehavior(_:))
- [func scrollTargetLayout(isEnabled:)](/documentation/swiftui/view/scrolltargetlayout(isenabled:))
- [ScrollTarget](/documentation/swiftui/scrolltarget) — target rect + anchor
- [ScrollTargetBehavior](/documentation/swiftui/scrolltargetbehavior) — protocol for scroll snapping (paging, viewAligned)
- [ScrollTargetBehaviorContext](/documentation/swiftui/scrolltargetbehaviorcontext) — context for scroll target calculations
- [PagingScrollTargetBehavior](/documentation/swiftui/pagingscrolltargetbehavior) — page-based scroll snapping
- [ViewAlignedScrollTargetBehavior](/documentation/swiftui/viewalignedscrolltargetbehavior) — view-aligned scroll snapping
- [AnyScrollTargetBehavior](/documentation/swiftui/anyscrolltargetbehavior) — type-erased scroll target behavior
- [ScrollTargetBehaviorProperties](/documentation/swiftui/scrolltargetbehaviorproperties)
- [ScrollTargetBehaviorPropertiesContext](/documentation/swiftui/scrolltargetbehaviorpropertiescontext)

### Animating scroll transitions

- [func scrollTransition(_:axis:transition:)](/documentation/swiftui/view/scrolltransition(_:axis:transition:))
- [func scrollTransition(topLeading:bottomTrailing:axis:transition:)](/documentation/swiftui/view/scrolltransition(topleading:bottomtrailing:axis:transition:))
- [ScrollTransitionPhase](/documentation/swiftui/scrolltransitionphase) — identity, topLeading, bottomTrailing
- [ScrollTransitionConfiguration](/documentation/swiftui/scrolltransitionconfiguration) — identity, animated, interactive with threshold

### Responding to scroll view changes

- [func onScrollGeometryChange(for:of:action:)](/documentation/swiftui/view/onscrollgeometrychange(for:of:action:))
- [func onScrollTargetVisibilityChange(idType:threshold:_:)](/documentation/swiftui/view/onscrolltargetvisibilitychange(idtype:threshold:_:))
- [func onScrollVisibilityChange(threshold:_:)](/documentation/swiftui/view/onscrollvisibilitychange(threshold:_:))
- [func onScrollPhaseChange(_:)](/documentation/swiftui/view/onscrollphasechange(_:))
- [ScrollGeometry](/documentation/swiftui/scrollgeometry) — content offset, size, insets, visible rect
- [ScrollPhase](/documentation/swiftui/scrollphase) — idle, tracking, interacting, decelerating, animating
- [ScrollPhaseChangeContext](/documentation/swiftui/scrollphasechangecontext)

### Showing scroll indicators

- [func scrollIndicatorsFlash(onAppear:)](/documentation/swiftui/view/scrollindicatorsflash(onappear:))
- [func scrollIndicatorsFlash(trigger:)](/documentation/swiftui/view/scrollindicatorsflash(trigger:))
- [func scrollIndicators(_:axes:)](/documentation/swiftui/view/scrollindicators(_:axes:))
- [var horizontalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/horizontalscrollindicatorvisibility)
- [var verticalScrollIndicatorVisibility: ScrollIndicatorVisibility](/documentation/swiftui/environmentvalues/verticalscrollindicatorvisibility)
- [ScrollIndicatorVisibility](/documentation/swiftui/scrollindicatorvisibility) — automatic, hidden, never, visible

### Managing content visibility

- [func scrollContentBackground(_:)](/documentation/swiftui/view/scrollcontentbackground(_:))
- [func scrollClipDisabled(_:)](/documentation/swiftui/view/scrollclipdisabled(_:))
- [ScrollContentOffsetAdjustmentBehavior](/documentation/swiftui/scrollcontentoffsetadjustmentbehavior) — automatic, disabled

### Disabling scrolling

- [func scrollDisabled(_:)](/documentation/swiftui/view/scrolldisabled(_:))
- [var isScrollEnabled: Bool](/documentation/swiftui/environmentvalues/isscrollenabled)

### Configuring scroll bounce behavior

- [func scrollBounceBehavior(_:axes:)](/documentation/swiftui/view/scrollbouncebehavior(_:axes:))
- [var horizontalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/horizontalscrollbouncebehavior)
- [var verticalScrollBounceBehavior: ScrollBounceBehavior](/documentation/swiftui/environmentvalues/verticalscrollbouncebehavior)
- [ScrollBounceBehavior](/documentation/swiftui/scrollbouncebehavior) — automatic, always, basedOnSize

### Configuring scroll edge effects

- [func scrollEdgeEffectStyle(_:for:)](/documentation/swiftui/view/scrolledgeeffectstyle(_:for:))
- [func scrollEdgeEffectHidden(_:for:)](/documentation/swiftui/view/scrolledgeeffecthidden(_:for:))
- [ScrollEdgeEffectStyle](/documentation/swiftui/scrolledgeeffectstyle) — automatic, hard, soft
- [func safeAreaBar(edge:alignment:spacing:content:)](/documentation/swiftui/view/safeareabar(edge:alignment:spacing:content:))

### Interacting with a software keyboard

- [func scrollDismissesKeyboard(_:)](/documentation/swiftui/view/scrolldismisseskeyboard(_:))
- [var scrollDismissesKeyboardMode: ScrollDismissesKeyboardMode](/documentation/swiftui/environmentvalues/scrolldismisseskeyboardmode)
- [ScrollDismissesKeyboardMode](/documentation/swiftui/scrolldismisseskeyboardmode) — automatic, immediately, interactively, never

### Managing scrolling for different inputs

- [func scrollInputBehavior(_:for:)](/documentation/swiftui/view/scrollinputbehavior(_:for:))
- [ScrollInputKind](/documentation/swiftui/scrollinputkind) — handGestureShortcut, look
- [ScrollInputBehavior](/documentation/swiftui/scrollinputbehavior) — automatic, disabled, enabled
