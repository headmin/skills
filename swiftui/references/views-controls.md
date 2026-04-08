# Views: Controls — SwiftUI Reference

> Fetch full docs: `https://developer.apple.com/tutorials/data{path}.json`

## Contents
- [Styling buttons](#styling-buttons)
- [Styling pickers](#styling-pickers)
- [Styling menus](#styling-menus)
- [Styling toggles](#styling-toggles)
- [Styling indicators](#styling-indicators)
- [Styling views that display text](#styling-views-that-display-text)
- [Styling collection views](#styling-collection-views)
- [Styling navigation views](#styling-navigation-views)

---

### Styling buttons

- [func buttonStyle<S>(S) -> some View](/documentation/swiftui/view/buttonstyle(_:)) — apply button style
- [ButtonStyle](/documentation/swiftui/buttonstyle) — protocol for custom button appearance
- [PrimitiveButtonStyle](/documentation/swiftui/primitivebuttonstyle) — protocol for buttons with custom interaction
- [PrimitiveButtonStyleConfiguration](/documentation/swiftui/primitivebuttonstyleconfiguration) — config passed to primitive button styles
- [func signInWithAppleButtonStyle(SignInWithAppleButton.Style) -> some View](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))

Built-in button styles:
- [DefaultButtonStyle](/documentation/swiftui/defaultbuttonstyle) — platform default
- [AccessoryBarButtonStyle](/documentation/swiftui/accessorybarbuttonstyle) — accessory bar
- [AccessoryBarActionButtonStyle](/documentation/swiftui/accessorybaractionbuttonstyle) — accessory bar action
- [BorderedButtonStyle](/documentation/swiftui/borderedbuttonstyle) — bordered; `init(tint:)` [deprecated]
- [BorderedProminentButtonStyle](/documentation/swiftui/borderedprominentbuttonstyle) — bordered prominent
- [BorderlessButtonStyle](/documentation/swiftui/borderlessbuttonstyle) — borderless
- [CardButtonStyle](/documentation/swiftui/cardbuttonstyle) — card (tvOS)
- [LinkButtonStyle](/documentation/swiftui/linkbuttonstyle) — link appearance
- [PlainButtonStyle](/documentation/swiftui/plainbuttonstyle) — plain/unstyled

### Styling pickers

- [func pickerStyle<S>(S) -> some View](/documentation/swiftui/view/pickerstyle(_:)) — apply picker style
- [PickerStyle](/documentation/swiftui/pickerstyle) — protocol for custom picker appearance

Built-in picker styles:
- [DefaultPickerStyle](/documentation/swiftui/defaultpickerstyle) — `.automatic`
- [InlinePickerStyle](/documentation/swiftui/inlinepickerstyle) — `.inline`
- [MenuPickerStyle](/documentation/swiftui/menupickerstyle) — `.menu`
- [NavigationLinkPickerStyle](/documentation/swiftui/navigationlinkpickerstyle) — `.navigationLink`
- [PalettePickerStyle](/documentation/swiftui/palettepickerstyle) — `.palette`
- [RadioGroupPickerStyle](/documentation/swiftui/radiogrouppickerstyle) — `.radioGroup` (macOS)
- [SegmentedPickerStyle](/documentation/swiftui/segmentedpickerstyle) — `.segmented`
- [WheelPickerStyle](/documentation/swiftui/wheelpickerstyle) — `.wheel`
- [PopUpButtonPickerStyle](/documentation/swiftui/popupbuttonpickerstyle) [deprecated]

- [func datePickerStyle<S>(S) -> some View](/documentation/swiftui/view/datepickerstyle(_:)) — apply date picker style
- [DatePickerStyle](/documentation/swiftui/datepickerstyle) — protocol for custom date picker appearance
- [DatePickerStyleConfiguration](/documentation/swiftui/datepickerstyleconfiguration) — config for custom date picker styles

Built-in date picker styles:
- [DefaultDatePickerStyle](/documentation/swiftui/defaultdatepickerstyle) — `.automatic`
- [CompactDatePickerStyle](/documentation/swiftui/compactdatepickerstyle) — `.compact`
- [FieldDatePickerStyle](/documentation/swiftui/fielddatepickerstyle) — `.field` (macOS)
- [GraphicalDatePickerStyle](/documentation/swiftui/graphicaldatepickerstyle) — `.graphical`
- [StepperFieldDatePickerStyle](/documentation/swiftui/stepperfielddatepickerstyle) — `.stepperField` (macOS)
- [WheelDatePickerStyle](/documentation/swiftui/wheeldatepickerstyle) — `.wheel`

### Styling menus

- [func menuStyle<S>(S) -> some View](/documentation/swiftui/view/menustyle(_:)) — apply menu style
- [MenuStyle](/documentation/swiftui/menustyle) — protocol for custom menu appearance
- [MenuStyleConfiguration](/documentation/swiftui/menustyleconfiguration) — config for custom menu styles

Built-in menu styles:
- [DefaultMenuStyle](/documentation/swiftui/defaultmenustyle) — `.automatic`
- [ButtonMenuStyle](/documentation/swiftui/buttonmenustyle) — `.button`
- [BorderedButtonMenuStyle](/documentation/swiftui/borderedbuttonmenustyle) — `.borderedButton`
- [BorderlessButtonMenuStyle](/documentation/swiftui/borderlessbuttonmenustyle) — `.borderlessButton`

### Styling toggles

- [func toggleStyle<S>(S) -> some View](/documentation/swiftui/view/togglestyle(_:)) — apply toggle style
- [ToggleStyle](/documentation/swiftui/togglestyle) — protocol for custom toggle appearance
- [ToggleStyleConfiguration](/documentation/swiftui/togglestyleconfiguration) — config for custom toggle styles (label, isOn, isMixed)

Built-in toggle styles:
- [DefaultToggleStyle](/documentation/swiftui/defaulttogglestyle) — `.automatic`
- [ButtonToggleStyle](/documentation/swiftui/buttontogglestyle) — `.button`
- [CheckboxToggleStyle](/documentation/swiftui/checkboxtogglestyle) — `.checkbox` (macOS)
- [SwitchToggleStyle](/documentation/swiftui/switchtogglestyle) — `.switch`; `init(tint:)` [deprecated]

### Styling indicators

- [func gaugeStyle<S>(S) -> some View](/documentation/swiftui/view/gaugestyle(_:)) — apply gauge style
- [GaugeStyle](/documentation/swiftui/gaugestyle) — protocol for custom gauge appearance
- [GaugeStyleConfiguration](/documentation/swiftui/gaugestyleconfiguration) — config for custom gauge styles

Built-in gauge styles:
- [DefaultGaugeStyle](/documentation/swiftui/defaultgaugestyle) — `.automatic`
- [CircularGaugeStyle](/documentation/swiftui/circulargaugestyle) — `.circular`
- [AccessoryCircularGaugeStyle](/documentation/swiftui/accessorycirculargaugestyle) — `.accessoryCircular`
- [AccessoryCircularCapacityGaugeStyle](/documentation/swiftui/accessorycircularcapacitygaugestyle) — `.accessoryCircularCapacity`
- [LinearGaugeStyle](/documentation/swiftui/lineargaugestyle) — `.linear`; `init(tint:)` [deprecated]
- [LinearCapacityGaugeStyle](/documentation/swiftui/linearcapacitygaugestyle) — `.linearCapacity`
- [AccessoryLinearGaugeStyle](/documentation/swiftui/accessorylineargaugestyle) — `.accessoryLinear`
- [AccessoryLinearCapacityGaugeStyle](/documentation/swiftui/accessorylinearcapacitygaugestyle) — `.accessoryLinearCapacity`

- [func progressViewStyle<S>(S) -> some View](/documentation/swiftui/view/progressviewstyle(_:)) — apply progress view style
- [ProgressViewStyle](/documentation/swiftui/progressviewstyle) — protocol for custom progress view appearance
- [ProgressViewStyleConfiguration](/documentation/swiftui/progressviewstyleconfiguration) — config for custom progress view styles

Built-in progress view styles:
- [DefaultProgressViewStyle](/documentation/swiftui/defaultprogressviewstyle) — `.automatic`
- [CircularProgressViewStyle](/documentation/swiftui/circularprogressviewstyle) — `.circular`; `init(tint:)` [deprecated]
- [LinearProgressViewStyle](/documentation/swiftui/linearprogressviewstyle) — `.linear`; `init(tint:)` [deprecated]

### Styling views that display text

- [func labelStyle<S>(S) -> some View](/documentation/swiftui/view/labelstyle(_:)) — apply label style
- [LabelStyle](/documentation/swiftui/labelstyle) — protocol for custom label appearance
- [LabelStyleConfiguration](/documentation/swiftui/labelstyleconfiguration) — config for custom label styles (icon, title)

Built-in label styles:
- [DefaultLabelStyle](/documentation/swiftui/defaultlabelstyle) — `.automatic`
- [IconOnlyLabelStyle](/documentation/swiftui/icononlylabelstyle) — `.iconOnly`
- [TitleAndIconLabelStyle](/documentation/swiftui/titleandiconlabelstyle) — `.titleAndIcon`
- [TitleOnlyLabelStyle](/documentation/swiftui/titleonlylabelstyle) — `.titleOnly`

- [func textFieldStyle<S>(S) -> some View](/documentation/swiftui/view/textfieldstyle(_:)) — apply text field style
- [TextFieldStyle](/documentation/swiftui/textfieldstyle) — protocol for custom text field appearance

Built-in text field styles:
- [DefaultTextFieldStyle](/documentation/swiftui/defaulttextfieldstyle) — `.automatic`
- [PlainTextFieldStyle](/documentation/swiftui/plaintextfieldstyle) — `.plain`
- [RoundedBorderTextFieldStyle](/documentation/swiftui/roundedbordertextfieldstyle) — `.roundedBorder`
- [SquareBorderTextFieldStyle](/documentation/swiftui/squarebordertextfieldstyle) — `.squareBorder` (macOS)

- [func textEditorStyle(some TextEditorStyle) -> some View](/documentation/swiftui/view/texteditorstyle(_:)) — apply text editor style
- [TextEditorStyle](/documentation/swiftui/texteditorstyle) — protocol for custom text editor appearance
- [TextEditorStyleConfiguration](/documentation/swiftui/texteditorstyleconfiguration) — config for custom text editor styles

Built-in text editor styles:
- [AutomaticTextEditorStyle](/documentation/swiftui/automatictexteditorstyle) — `.automatic`
- [PlainTextEditorStyle](/documentation/swiftui/plaintexteditorstyle) — `.plain`
- [RoundedBorderTextEditorStyle](/documentation/swiftui/roundedbordertexteditorstyle) — `.roundedBorder`

### Styling collection views

- [func listStyle<S>(S) -> some View](/documentation/swiftui/view/liststyle(_:)) — apply list style
- [ListStyle](/documentation/swiftui/liststyle) — protocol for custom list appearance

Built-in list styles:
- [DefaultListStyle](/documentation/swiftui/defaultliststyle) — `.automatic`
- [BorderedListStyle](/documentation/swiftui/borderedliststyle) — `.bordered` (macOS)
- [CarouselListStyle](/documentation/swiftui/carouselliststyle) — `.carousel` (watchOS)
- [EllipticalListStyle](/documentation/swiftui/ellipticalliststyle) — `.elliptical` (watchOS)
- [GroupedListStyle](/documentation/swiftui/groupedliststyle) — `.grouped` (iOS)
- [InsetListStyle](/documentation/swiftui/insetliststyle) — `.inset`
- [InsetGroupedListStyle](/documentation/swiftui/insetgroupedliststyle) — `.insetGrouped` (iOS)
- [PlainListStyle](/documentation/swiftui/plainliststyle) — `.plain`
- [SidebarListStyle](/documentation/swiftui/sidebarliststyle) — `.sidebar`
- `.bordered(alternatesRowBackgrounds:)` [deprecated], `.inset(alternatesRowBackgrounds:)` [deprecated]

- [func tableStyle<S>(S) -> some View](/documentation/swiftui/view/tablestyle(_:)) — apply table style
- [TableStyle](/documentation/swiftui/tablestyle) — protocol for custom table appearance
- [TableStyleConfiguration](/documentation/swiftui/tablestyleconfiguration) — config for custom table styles

Built-in table styles:
- [AutomaticTableStyle](/documentation/swiftui/automatictablestyle) — `.automatic`
- [InsetTableStyle](/documentation/swiftui/insettablestyle) — `.inset`
- [BorderedTableStyle](/documentation/swiftui/borderedtablestyle) — `.bordered`
- `.inset(alternatesRowBackgrounds:)` [deprecated], `.bordered(alternatesRowBackgrounds:)` [deprecated]

- [func disclosureGroupStyle<S>(S) -> some View](/documentation/swiftui/view/disclosuregroupstyle(_:)) — apply disclosure group style
- [DisclosureGroupStyle](/documentation/swiftui/disclosuregroupstyle) — protocol for custom disclosure group appearance
- [DisclosureGroupStyleConfiguration](/documentation/swiftui/disclosuregroupstyleconfiguration) — config (label, content, isExpanded)
- [AutomaticDisclosureGroupStyle](/documentation/swiftui/automaticdisclosuregroupstyle) — `.automatic`

### Styling navigation views

- [func navigationSplitViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationsplitviewstyle(_:)) — apply navigation split view style
- [NavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle) — protocol for custom split view appearance

Built-in navigation split view styles:
- [AutomaticNavigationSplitViewStyle](/documentation/swiftui/automaticnavigationsplitviewstyle) — `.automatic`
- [BalancedNavigationSplitViewStyle](/documentation/swiftui/balancednavigationsplitviewstyle) — `.balanced`
- [ProminentDetailNavigationSplitViewStyle](/documentation/swiftui/prominentdetailnavigationsplitviewstyle) — `.prominentDetail`
