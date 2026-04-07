# Views: Controls — SwiftUI Reference

## Contents
  - [Styling pickers](#styling-pickers)
  - [Styling menus](#styling-menus)
  - [Styling toggles](#styling-toggles)
  - [Styling indicators](#styling-indicators)
  - [Styling views that display text](#styling-views-that-display-text)
  - [Styling collection views](#styling-collection-views)
  - [Styling navigation views](#styling-navigation-views)

---
- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/primitivebuttonstyle/makebody(configuration:))
- [PrimitiveButtonStyle.Configuration](/documentation/swiftui/primitivebuttonstyle/configuration)
- [Body](/documentation/swiftui/primitivebuttonstyle/body)

#### Supporting types

- [DefaultButtonStyle](/documentation/swiftui/defaultbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/defaultbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: DefaultButtonStyle.Configuration) -> some View](/documentation/swiftui/defaultbuttonstyle/makebody(configuration:))
- [AccessoryBarButtonStyle](/documentation/swiftui/accessorybarbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/accessorybarbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: AccessoryBarButtonStyle.Configuration) -> some View](/documentation/swiftui/accessorybarbuttonstyle/makebody(configuration:))
- [AccessoryBarActionButtonStyle](/documentation/swiftui/accessorybaractionbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/accessorybaractionbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: AccessoryBarActionButtonStyle.Configuration) -> some View](/documentation/swiftui/accessorybaractionbuttonstyle/makebody(configuration:))
- [BorderedButtonStyle](/documentation/swiftui/borderedbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/borderedbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: BorderedButtonStyle.Configuration) -> some View](/documentation/swiftui/borderedbuttonstyle/makebody(configuration:))

##### Deprecated symbols

- [init(tint: Color)](/documentation/swiftui/borderedbuttonstyle/init(tint:))
- [BorderedProminentButtonStyle](/documentation/swiftui/borderedprominentbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/borderedprominentbuttonstyle/init())
- [BorderlessButtonStyle](/documentation/swiftui/borderlessbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/borderlessbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: BorderlessButtonStyle.Configuration) -> some View](/documentation/swiftui/borderlessbuttonstyle/makebody(configuration:))
- [CardButtonStyle](/documentation/swiftui/cardbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/cardbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: CardButtonStyle.Configuration) -> some View](/documentation/swiftui/cardbuttonstyle/makebody(configuration:))
- [LinkButtonStyle](/documentation/swiftui/linkbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/linkbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: LinkButtonStyle.Configuration) -> some View](/documentation/swiftui/linkbuttonstyle/makebody(configuration:))
- [PlainButtonStyle](/documentation/swiftui/plainbuttonstyle)

##### Creating the button style

- [init()](/documentation/swiftui/plainbuttonstyle/init())

##### Supporting types

- [func makeBody(configuration: PlainButtonStyle.Configuration) -> some View](/documentation/swiftui/plainbuttonstyle/makebody(configuration:))
- [PrimitiveButtonStyleConfiguration](/documentation/swiftui/primitivebuttonstyleconfiguration)

#### Configuring a button’s label

- [let label: PrimitiveButtonStyleConfiguration.Label](/documentation/swiftui/primitivebuttonstyleconfiguration/label-swift.property)
- [PrimitiveButtonStyleConfiguration.Label](/documentation/swiftui/primitivebuttonstyleconfiguration/label-swift.struct)

#### Initiating a button’s action

- [func trigger()](/documentation/swiftui/primitivebuttonstyleconfiguration/trigger())

#### Defining the button’s purpose

- [let role: ButtonRole?](/documentation/swiftui/primitivebuttonstyleconfiguration/role)
- [func signInWithAppleButtonStyle(SignInWithAppleButton.Style) -> some View](/documentation/swiftui/view/signinwithapplebuttonstyle(_:))

### Styling pickers

- [func pickerStyle<S>(S) -> some View](/documentation/swiftui/view/pickerstyle(_:))
- [PickerStyle](/documentation/swiftui/pickerstyle)

#### Getting built-in picker styles

- [static var automatic: DefaultPickerStyle](/documentation/swiftui/pickerstyle/automatic)
- [static var inline: InlinePickerStyle](/documentation/swiftui/pickerstyle/inline)
- [static var menu: MenuPickerStyle](/documentation/swiftui/pickerstyle/menu)
- [static var navigationLink: NavigationLinkPickerStyle](/documentation/swiftui/pickerstyle/navigationlink)
- [static var palette: PalettePickerStyle](/documentation/swiftui/pickerstyle/palette)
- [static var radioGroup: RadioGroupPickerStyle](/documentation/swiftui/pickerstyle/radiogroup)
- [static var segmented: SegmentedPickerStyle](/documentation/swiftui/pickerstyle/segmented)
- [static var wheel: WheelPickerStyle](/documentation/swiftui/pickerstyle/wheel)

#### Supporting types

- [DefaultPickerStyle](/documentation/swiftui/defaultpickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/defaultpickerstyle/init())
- [InlinePickerStyle](/documentation/swiftui/inlinepickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/inlinepickerstyle/init())
- [MenuPickerStyle](/documentation/swiftui/menupickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/menupickerstyle/init())
- [NavigationLinkPickerStyle](/documentation/swiftui/navigationlinkpickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/navigationlinkpickerstyle/init())
- [PalettePickerStyle](/documentation/swiftui/palettepickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/palettepickerstyle/init())
- [RadioGroupPickerStyle](/documentation/swiftui/radiogrouppickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/radiogrouppickerstyle/init())
- [SegmentedPickerStyle](/documentation/swiftui/segmentedpickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/segmentedpickerstyle/init())
- [WheelPickerStyle](/documentation/swiftui/wheelpickerstyle)

##### Creating the picker style

- [init()](/documentation/swiftui/wheelpickerstyle/init())

#### Deprecated styles

- [PopUpButtonPickerStyle](/documentation/swiftui/popupbuttonpickerstyle)

##### Initializers

- [init()](/documentation/swiftui/popupbuttonpickerstyle/init())
- [func datePickerStyle<S>(S) -> some View](/documentation/swiftui/view/datepickerstyle(_:))
- [DatePickerStyle](/documentation/swiftui/datepickerstyle)

#### Getting built-in date picker styles

- [static var automatic: DefaultDatePickerStyle](/documentation/swiftui/datepickerstyle/automatic)
- [static var compact: CompactDatePickerStyle](/documentation/swiftui/datepickerstyle/compact)
- [static var field: FieldDatePickerStyle](/documentation/swiftui/datepickerstyle/field)
- [static var graphical: GraphicalDatePickerStyle](/documentation/swiftui/datepickerstyle/graphical)
- [static var stepperField: StepperFieldDatePickerStyle](/documentation/swiftui/datepickerstyle/stepperfield)
- [static var wheel: WheelDatePickerStyle](/documentation/swiftui/datepickerstyle/wheel)

#### Creating custom date picker styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/datepickerstyle/makebody(configuration:))
- [DatePickerStyleConfiguration](/documentation/swiftui/datepickerstyleconfiguration)

##### Establishing the date range

- [var minimumDate: Date?](/documentation/swiftui/datepickerstyleconfiguration/minimumdate)
- [var maximumDate: Date?](/documentation/swiftui/datepickerstyleconfiguration/maximumdate)

##### Labeling the date picker

- [let label: DatePickerStyleConfiguration.Label](/documentation/swiftui/datepickerstyleconfiguration/label-swift.property)
- [DatePickerStyleConfiguration.Label](/documentation/swiftui/datepickerstyleconfiguration/label-swift.struct)
- [var displayedComponents: DatePickerComponents](/documentation/swiftui/datepickerstyleconfiguration/displayedcomponents)

##### Selecting the date

- [var selection: Date](/documentation/swiftui/datepickerstyleconfiguration/selection)
- [var $selection: Binding<Date>](/documentation/swiftui/datepickerstyleconfiguration/$selection)
- [DatePickerStyle.Configuration](/documentation/swiftui/datepickerstyle/configuration)
- [Body](/documentation/swiftui/datepickerstyle/body)

#### Supporting types

- [DefaultDatePickerStyle](/documentation/swiftui/defaultdatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/defaultdatepickerstyle/init())
- [CompactDatePickerStyle](/documentation/swiftui/compactdatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/compactdatepickerstyle/init())
- [FieldDatePickerStyle](/documentation/swiftui/fielddatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/fielddatepickerstyle/init())
- [GraphicalDatePickerStyle](/documentation/swiftui/graphicaldatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/graphicaldatepickerstyle/init())
- [StepperFieldDatePickerStyle](/documentation/swiftui/stepperfielddatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/stepperfielddatepickerstyle/init())
- [WheelDatePickerStyle](/documentation/swiftui/wheeldatepickerstyle)

##### Creating the date picker style

- [init()](/documentation/swiftui/wheeldatepickerstyle/init())

### Styling menus

- [func menuStyle<S>(S) -> some View](/documentation/swiftui/view/menustyle(_:))
- [MenuStyle](/documentation/swiftui/menustyle)

#### Getting built-in menu styles

- [static var automatic: DefaultMenuStyle](/documentation/swiftui/menustyle/automatic)
- [static var button: ButtonMenuStyle](/documentation/swiftui/menustyle/button)
- [static var borderedButton: BorderedButtonMenuStyle](/documentation/swiftui/menustyle/borderedbutton)
- [static var borderlessButton: BorderlessButtonMenuStyle](/documentation/swiftui/menustyle/borderlessbutton)

#### Creating custom menu styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/menustyle/makebody(configuration:))
- [MenuStyle.Configuration](/documentation/swiftui/menustyle/configuration)
- [Body](/documentation/swiftui/menustyle/body)

#### Supporting types

- [DefaultMenuStyle](/documentation/swiftui/defaultmenustyle)

##### Creating the menu style

- [init()](/documentation/swiftui/defaultmenustyle/init())
- [ButtonMenuStyle](/documentation/swiftui/buttonmenustyle)

##### Creating the menu style

- [init()](/documentation/swiftui/buttonmenustyle/init())
- [BorderlessButtonMenuStyle](/documentation/swiftui/borderlessbuttonmenustyle)

##### Creating a bordeless button menu style

- [init()](/documentation/swiftui/borderlessbuttonmenustyle/init())
- [init(showsMenuIndicator: Bool)](/documentation/swiftui/borderlessbuttonmenustyle/init(showsmenuindicator:))
- [BorderedButtonMenuStyle](/documentation/swiftui/borderedbuttonmenustyle)

##### Creating a bordered button menu style

- [init()](/documentation/swiftui/borderedbuttonmenustyle/init())
- [MenuStyleConfiguration](/documentation/swiftui/menustyleconfiguration)

#### Setting the label and content

- [MenuStyleConfiguration.Label](/documentation/swiftui/menustyleconfiguration/label)
- [MenuStyleConfiguration.Content](/documentation/swiftui/menustyleconfiguration/content)

### Styling toggles

- [func toggleStyle<S>(S) -> some View](/documentation/swiftui/view/togglestyle(_:))
- [ToggleStyle](/documentation/swiftui/togglestyle)

#### Getting built-in toggle styles

- [static var automatic: DefaultToggleStyle](/documentation/swiftui/togglestyle/automatic)
- [static var button: ButtonToggleStyle](/documentation/swiftui/togglestyle/button)
- [static var checkbox: CheckboxToggleStyle](/documentation/swiftui/togglestyle/checkbox)
- [static var `switch`: SwitchToggleStyle](/documentation/swiftui/togglestyle/switch)

#### Creating custom toggle styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/togglestyle/makebody(configuration:))
- [ToggleStyleConfiguration](/documentation/swiftui/togglestyleconfiguration)

##### Getting the label view

- [let label: ToggleStyleConfiguration.Label](/documentation/swiftui/togglestyleconfiguration/label-swift.property)
- [ToggleStyleConfiguration.Label](/documentation/swiftui/togglestyleconfiguration/label-swift.struct)

##### Managing the toggle state

- [var isMixed: Bool](/documentation/swiftui/togglestyleconfiguration/ismixed)
- [var isOn: Bool](/documentation/swiftui/togglestyleconfiguration/ison)
- [var $isOn: Binding<Bool>](/documentation/swiftui/togglestyleconfiguration/$ison)
- [ToggleStyle.Configuration](/documentation/swiftui/togglestyle/configuration)
- [Body](/documentation/swiftui/togglestyle/body)

#### Supporting types

- [DefaultToggleStyle](/documentation/swiftui/defaulttogglestyle)

##### Creating the toggle style

- [init()](/documentation/swiftui/defaulttogglestyle/init())

##### Supporting types

- [func makeBody(configuration: DefaultToggleStyle.Configuration) -> some View](/documentation/swiftui/defaulttogglestyle/makebody(configuration:))
- [ButtonToggleStyle](/documentation/swiftui/buttontogglestyle)

##### Creating the toggle style

- [init()](/documentation/swiftui/buttontogglestyle/init())

##### Supporting types

- [func makeBody(configuration: ButtonToggleStyle.Configuration) -> some View](/documentation/swiftui/buttontogglestyle/makebody(configuration:))
- [CheckboxToggleStyle](/documentation/swiftui/checkboxtogglestyle)

##### Creating the toggle style

- [init()](/documentation/swiftui/checkboxtogglestyle/init())

##### Supporting types

- [func makeBody(configuration: CheckboxToggleStyle.Configuration) -> some View](/documentation/swiftui/checkboxtogglestyle/makebody(configuration:))
- [SwitchToggleStyle](/documentation/swiftui/switchtogglestyle)

##### Creating the toggle style

- [init()](/documentation/swiftui/switchtogglestyle/init())

##### Supporting types

- [func makeBody(configuration: SwitchToggleStyle.Configuration) -> some View](/documentation/swiftui/switchtogglestyle/makebody(configuration:))

##### Deprecated initializers

- [init(tint: Color)](/documentation/swiftui/switchtogglestyle/init(tint:))
- [ToggleStyleConfiguration](/documentation/swiftui/togglestyleconfiguration)

#### Getting the label view

- [let label: ToggleStyleConfiguration.Label](/documentation/swiftui/togglestyleconfiguration/label-swift.property)
- [ToggleStyleConfiguration.Label](/documentation/swiftui/togglestyleconfiguration/label-swift.struct)

#### Managing the toggle state

- [var isMixed: Bool](/documentation/swiftui/togglestyleconfiguration/ismixed)
- [var isOn: Bool](/documentation/swiftui/togglestyleconfiguration/ison)
- [var $isOn: Binding<Bool>](/documentation/swiftui/togglestyleconfiguration/$ison)

### Styling indicators

- [func gaugeStyle<S>(S) -> some View](/documentation/swiftui/view/gaugestyle(_:))
- [GaugeStyle](/documentation/swiftui/gaugestyle)

#### Getting the automatic style

- [static var automatic: DefaultGaugeStyle](/documentation/swiftui/gaugestyle/automatic)

#### Getting circular gauge styles

- [static var circular: CircularGaugeStyle](/documentation/swiftui/gaugestyle/circular)
- [static var accessoryCircular: AccessoryCircularGaugeStyle](/documentation/swiftui/gaugestyle/accessorycircular)
- [static var accessoryCircularCapacity: AccessoryCircularCapacityGaugeStyle](/documentation/swiftui/gaugestyle/accessorycircularcapacity)

#### Getting linear gauge styles

- [static var linear: LinearGaugeStyle](/documentation/swiftui/gaugestyle/linear)
- [static var linearCapacity: LinearCapacityGaugeStyle](/documentation/swiftui/gaugestyle/linearcapacity)
- [static var accessoryLinear: AccessoryLinearGaugeStyle](/documentation/swiftui/gaugestyle/accessorylinear)
- [static var accessoryLinearCapacity: AccessoryLinearCapacityGaugeStyle](/documentation/swiftui/gaugestyle/accessorylinearcapacity)

#### Creating custom gauge styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/gaugestyle/makebody(configuration:))
- [GaugeStyle.Configuration](/documentation/swiftui/gaugestyle/configuration)
- [Body](/documentation/swiftui/gaugestyle/body)

#### Supporting types

- [DefaultGaugeStyle](/documentation/swiftui/defaultgaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/defaultgaugestyle/init())
- [CircularGaugeStyle](/documentation/swiftui/circulargaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/circulargaugestyle/init())
- [init(tint:)](/documentation/swiftui/circulargaugestyle/init(tint:))
- [AccessoryCircularGaugeStyle](/documentation/swiftui/accessorycirculargaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/accessorycirculargaugestyle/init())
- [AccessoryCircularCapacityGaugeStyle](/documentation/swiftui/accessorycircularcapacitygaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/accessorycircularcapacitygaugestyle/init())
- [LinearGaugeStyle](/documentation/swiftui/lineargaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/lineargaugestyle/init())

##### Deprecated initializers

- [init(tint:)](/documentation/swiftui/lineargaugestyle/init(tint:))
- [LinearCapacityGaugeStyle](/documentation/swiftui/linearcapacitygaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/linearcapacitygaugestyle/init())
- [AccessoryLinearGaugeStyle](/documentation/swiftui/accessorylineargaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/accessorylineargaugestyle/init())
- [AccessoryLinearCapacityGaugeStyle](/documentation/swiftui/accessorylinearcapacitygaugestyle)

##### Creating the gauge style

- [init()](/documentation/swiftui/accessorylinearcapacitygaugestyle/init())
- [GaugeStyleConfiguration](/documentation/swiftui/gaugestyleconfiguration)

#### Describing the purpose of the gauge

- [var label: GaugeStyleConfiguration.Label](/documentation/swiftui/gaugestyleconfiguration/label-swift.property)
- [GaugeStyleConfiguration.Label](/documentation/swiftui/gaugestyleconfiguration/label-swift.struct)

#### Reporting the range

- [var minimumValueLabel: GaugeStyleConfiguration.MinimumValueLabel?](/documentation/swiftui/gaugestyleconfiguration/minimumvaluelabel-swift.property)
- [GaugeStyleConfiguration.MinimumValueLabel](/documentation/swiftui/gaugestyleconfiguration/minimumvaluelabel-swift.struct)
- [var maximumValueLabel: GaugeStyleConfiguration.MaximumValueLabel?](/documentation/swiftui/gaugestyleconfiguration/maximumvaluelabel-swift.property)
- [GaugeStyleConfiguration.MaximumValueLabel](/documentation/swiftui/gaugestyleconfiguration/maximumvaluelabel-swift.struct)

#### Setting the value

- [var value: Double](/documentation/swiftui/gaugestyleconfiguration/value)
- [var currentValueLabel: GaugeStyleConfiguration.CurrentValueLabel?](/documentation/swiftui/gaugestyleconfiguration/currentvaluelabel-swift.property)
- [GaugeStyleConfiguration.CurrentValueLabel](/documentation/swiftui/gaugestyleconfiguration/currentvaluelabel-swift.struct)
- [GaugeStyleConfiguration.MarkedValueLabel](/documentation/swiftui/gaugestyleconfiguration/markedvaluelabel)
- [func progressViewStyle<S>(S) -> some View](/documentation/swiftui/view/progressviewstyle(_:))
- [ProgressViewStyle](/documentation/swiftui/progressviewstyle)

#### Getting built-in progress view styles

- [static var automatic: DefaultProgressViewStyle](/documentation/swiftui/progressviewstyle/automatic)
- [static var circular: CircularProgressViewStyle](/documentation/swiftui/progressviewstyle/circular)
- [static var linear: LinearProgressViewStyle](/documentation/swiftui/progressviewstyle/linear)

#### Creating custom progress view styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/progressviewstyle/makebody(configuration:))
- [ProgressViewStyle.Configuration](/documentation/swiftui/progressviewstyle/configuration)
- [Body](/documentation/swiftui/progressviewstyle/body)

#### Supporting types

- [DefaultProgressViewStyle](/documentation/swiftui/defaultprogressviewstyle)

##### Creating the progress view style

- [init()](/documentation/swiftui/defaultprogressviewstyle/init())
- [CircularProgressViewStyle](/documentation/swiftui/circularprogressviewstyle)

##### Creating the progress view style

- [init()](/documentation/swiftui/circularprogressviewstyle/init())

##### Deprecated initializers

- [init(tint: Color)](/documentation/swiftui/circularprogressviewstyle/init(tint:))
- [LinearProgressViewStyle](/documentation/swiftui/linearprogressviewstyle)

##### Creating the progress view style

- [init()](/documentation/swiftui/linearprogressviewstyle/init())

##### Deprecated initializers

- [init(tint: Color)](/documentation/swiftui/linearprogressviewstyle/init(tint:))
- [ProgressViewStyleConfiguration](/documentation/swiftui/progressviewstyleconfiguration)

#### Configuring the label

- [var label: ProgressViewStyleConfiguration.Label?](/documentation/swiftui/progressviewstyleconfiguration/label-swift.property)
- [ProgressViewStyleConfiguration.Label](/documentation/swiftui/progressviewstyleconfiguration/label-swift.struct)

#### Configuring the current value label

- [var currentValueLabel: ProgressViewStyleConfiguration.CurrentValueLabel?](/documentation/swiftui/progressviewstyleconfiguration/currentvaluelabel-swift.property)
- [ProgressViewStyleConfiguration.CurrentValueLabel](/documentation/swiftui/progressviewstyleconfiguration/currentvaluelabel-swift.struct)

#### Configuring progress completion

- [let fractionCompleted: Double?](/documentation/swiftui/progressviewstyleconfiguration/fractioncompleted)

### Styling views that display text

- [func labelStyle<S>(S) -> some View](/documentation/swiftui/view/labelstyle(_:))
- [LabelStyle](/documentation/swiftui/labelstyle)

#### Getting built-in label styles

- [static var automatic: DefaultLabelStyle](/documentation/swiftui/labelstyle/automatic)
- [static var iconOnly: IconOnlyLabelStyle](/documentation/swiftui/labelstyle/icononly)
- [static var titleAndIcon: TitleAndIconLabelStyle](/documentation/swiftui/labelstyle/titleandicon)
- [static var titleOnly: TitleOnlyLabelStyle](/documentation/swiftui/labelstyle/titleonly)

#### Creating custom label styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/labelstyle/makebody(configuration:))
- [LabelStyle.Configuration](/documentation/swiftui/labelstyle/configuration)
- [Body](/documentation/swiftui/labelstyle/body)

#### Supporting types

- [DefaultLabelStyle](/documentation/swiftui/defaultlabelstyle)

##### Creating the label style

- [init()](/documentation/swiftui/defaultlabelstyle/init())
- [IconOnlyLabelStyle](/documentation/swiftui/icononlylabelstyle)

##### Creating the label style

- [init()](/documentation/swiftui/icononlylabelstyle/init())
- [TitleAndIconLabelStyle](/documentation/swiftui/titleandiconlabelstyle)

##### Creating the label style

- [init()](/documentation/swiftui/titleandiconlabelstyle/init())
- [TitleOnlyLabelStyle](/documentation/swiftui/titleonlylabelstyle)

##### Creating the label style

- [init()](/documentation/swiftui/titleonlylabelstyle/init())
- [LabelStyleConfiguration](/documentation/swiftui/labelstyleconfiguration)

#### Setting the icon

- [var icon: LabelStyleConfiguration.Icon](/documentation/swiftui/labelstyleconfiguration/icon-swift.property)
- [LabelStyleConfiguration.Icon](/documentation/swiftui/labelstyleconfiguration/icon-swift.struct)

#### Setting the title

- [var title: LabelStyleConfiguration.Title](/documentation/swiftui/labelstyleconfiguration/title-swift.property)
- [LabelStyleConfiguration.Title](/documentation/swiftui/labelstyleconfiguration/title-swift.struct)
- [func textFieldStyle<S>(S) -> some View](/documentation/swiftui/view/textfieldstyle(_:))
- [TextFieldStyle](/documentation/swiftui/textfieldstyle)

#### Getting built-in text field styles

- [static var automatic: DefaultTextFieldStyle](/documentation/swiftui/textfieldstyle/automatic)
- [static var plain: PlainTextFieldStyle](/documentation/swiftui/textfieldstyle/plain)
- [static var roundedBorder: RoundedBorderTextFieldStyle](/documentation/swiftui/textfieldstyle/roundedborder)
- [static var squareBorder: SquareBorderTextFieldStyle](/documentation/swiftui/textfieldstyle/squareborder)

#### Supporting types

- [DefaultTextFieldStyle](/documentation/swiftui/defaulttextfieldstyle)

##### Creating the text field style

- [init()](/documentation/swiftui/defaulttextfieldstyle/init())
- [PlainTextFieldStyle](/documentation/swiftui/plaintextfieldstyle)

##### Creating the text field style

- [init()](/documentation/swiftui/plaintextfieldstyle/init())
- [RoundedBorderTextFieldStyle](/documentation/swiftui/roundedbordertextfieldstyle)

##### Creating the text field style

- [init()](/documentation/swiftui/roundedbordertextfieldstyle/init())
- [SquareBorderTextFieldStyle](/documentation/swiftui/squarebordertextfieldstyle)

##### Creating the text field style

- [init()](/documentation/swiftui/squarebordertextfieldstyle/init())
- [func textEditorStyle(some TextEditorStyle) -> some View](/documentation/swiftui/view/texteditorstyle(_:))
- [TextEditorStyle](/documentation/swiftui/texteditorstyle)

#### Getting built-in styles

- [static var automatic: AutomaticTextEditorStyle](/documentation/swiftui/texteditorstyle/automatic)
- [static var plain: PlainTextEditorStyle](/documentation/swiftui/texteditorstyle/plain)
- [static var roundedBorder: RoundedBorderTextEditorStyle](/documentation/swiftui/texteditorstyle/roundedborder)

#### Creating custom styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/texteditorstyle/makebody(configuration:))
- [TextEditorStyle.Configuration](/documentation/swiftui/texteditorstyle/configuration)
- [Body](/documentation/swiftui/texteditorstyle/body)

#### Supporting types

- [AutomaticTextEditorStyle](/documentation/swiftui/automatictexteditorstyle)

##### Creating the text editor style

- [init()](/documentation/swiftui/automatictexteditorstyle/init())
- [PlainTextEditorStyle](/documentation/swiftui/plaintexteditorstyle)

##### Creating the text editor style

- [init()](/documentation/swiftui/plaintexteditorstyle/init())
- [RoundedBorderTextEditorStyle](/documentation/swiftui/roundedbordertexteditorstyle)

##### Creating the text editor style

- [init()](/documentation/swiftui/roundedbordertexteditorstyle/init())
- [TextEditorStyleConfiguration](/documentation/swiftui/texteditorstyleconfiguration)

### Styling collection views

- [func listStyle<S>(S) -> some View](/documentation/swiftui/view/liststyle(_:))
- [ListStyle](/documentation/swiftui/liststyle)

#### Getting built-in list styles

- [static var automatic: DefaultListStyle](/documentation/swiftui/liststyle/automatic)
- [static var bordered: BorderedListStyle](/documentation/swiftui/liststyle/bordered)
- [static var carousel: CarouselListStyle](/documentation/swiftui/liststyle/carousel)
- [static var elliptical: EllipticalListStyle](/documentation/swiftui/liststyle/elliptical)
- [static var grouped: GroupedListStyle](/documentation/swiftui/liststyle/grouped)
- [static var inset: InsetListStyle](/documentation/swiftui/liststyle/inset)
- [static var insetGrouped: InsetGroupedListStyle](/documentation/swiftui/liststyle/insetgrouped)
- [static var plain: PlainListStyle](/documentation/swiftui/liststyle/plain)
- [static var sidebar: SidebarListStyle](/documentation/swiftui/liststyle/sidebar)

#### Deprecated styles

- [static func bordered(alternatesRowBackgrounds: Bool) -> BorderedListStyle](/documentation/swiftui/liststyle/bordered(alternatesrowbackgrounds:))
- [static func inset(alternatesRowBackgrounds: Bool) -> InsetListStyle](/documentation/swiftui/liststyle/inset(alternatesrowbackgrounds:))

#### Supporting types

- [DefaultListStyle](/documentation/swiftui/defaultliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/defaultliststyle/init())
- [BorderedListStyle](/documentation/swiftui/borderedliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/borderedliststyle/init())
- [init(alternatesRowBackgrounds: Bool)](/documentation/swiftui/borderedliststyle/init(alternatesrowbackgrounds:))
- [CarouselListStyle](/documentation/swiftui/carouselliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/carouselliststyle/init())
- [EllipticalListStyle](/documentation/swiftui/ellipticalliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/ellipticalliststyle/init())
- [GroupedListStyle](/documentation/swiftui/groupedliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/groupedliststyle/init())
- [InsetListStyle](/documentation/swiftui/insetliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/insetliststyle/init())
- [init(alternatesRowBackgrounds: Bool)](/documentation/swiftui/insetliststyle/init(alternatesrowbackgrounds:))
- [InsetGroupedListStyle](/documentation/swiftui/insetgroupedliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/insetgroupedliststyle/init())
- [PlainListStyle](/documentation/swiftui/plainliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/plainliststyle/init())
- [SidebarListStyle](/documentation/swiftui/sidebarliststyle)

##### Creating the list style

- [init()](/documentation/swiftui/sidebarliststyle/init())
- [func tableStyle<S>(S) -> some View](/documentation/swiftui/view/tablestyle(_:))
- [TableStyle](/documentation/swiftui/tablestyle)

#### Getting built-in table styles

- [static var automatic: AutomaticTableStyle](/documentation/swiftui/tablestyle/automatic)
- [static var inset: InsetTableStyle](/documentation/swiftui/tablestyle/inset)
- [static var bordered: BorderedTableStyle](/documentation/swiftui/tablestyle/bordered)

#### Creating custom table styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/tablestyle/makebody(configuration:))
- [TableStyle.Configuration](/documentation/swiftui/tablestyle/configuration)
- [Body](/documentation/swiftui/tablestyle/body)

#### Deprecated styles

- [static func inset(alternatesRowBackgrounds: Bool) -> InsetTableStyle](/documentation/swiftui/tablestyle/inset(alternatesrowbackgrounds:))
- [static func bordered(alternatesRowBackgrounds: Bool) -> BorderedTableStyle](/documentation/swiftui/tablestyle/bordered(alternatesrowbackgrounds:))

#### Supporting types

- [AutomaticTableStyle](/documentation/swiftui/automatictablestyle)
- [InsetTableStyle](/documentation/swiftui/insettablestyle)

##### Creating the table style

- [init()](/documentation/swiftui/insettablestyle/init())
- [init(alternatesRowBackgrounds: Bool)](/documentation/swiftui/insettablestyle/init(alternatesrowbackgrounds:))
- [BorderedTableStyle](/documentation/swiftui/borderedtablestyle)

##### Creating the table style

- [init()](/documentation/swiftui/borderedtablestyle/init())
- [init(alternatesRowBackgrounds: Bool)](/documentation/swiftui/borderedtablestyle/init(alternatesrowbackgrounds:))
- [TableStyleConfiguration](/documentation/swiftui/tablestyleconfiguration)
- [func disclosureGroupStyle<S>(S) -> some View](/documentation/swiftui/view/disclosuregroupstyle(_:))
- [DisclosureGroupStyle](/documentation/swiftui/disclosuregroupstyle)

#### Getting the styles

- [static var automatic: AutomaticDisclosureGroupStyle](/documentation/swiftui/disclosuregroupstyle/automatic)

#### Creating custom disclosure group styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/disclosuregroupstyle/makebody(configuration:))
- [DisclosureGroupStyleConfiguration](/documentation/swiftui/disclosuregroupstyleconfiguration)

##### Configuring the label

- [let label: DisclosureGroupStyleConfiguration.Label](/documentation/swiftui/disclosuregroupstyleconfiguration/label-swift.property)
- [DisclosureGroupStyleConfiguration.Label](/documentation/swiftui/disclosuregroupstyleconfiguration/label-swift.struct)

##### Configuring the content

- [let content: DisclosureGroupStyleConfiguration.Content](/documentation/swiftui/disclosuregroupstyleconfiguration/content-swift.property)
- [DisclosureGroupStyleConfiguration.Content](/documentation/swiftui/disclosuregroupstyleconfiguration/content-swift.struct)

##### Managing disclosure

- [var isExpanded: Bool](/documentation/swiftui/disclosuregroupstyleconfiguration/isexpanded)
- [var $isExpanded: Binding<Bool>](/documentation/swiftui/disclosuregroupstyleconfiguration/$isexpanded)
- [DisclosureGroupStyle.Configuration](/documentation/swiftui/disclosuregroupstyle/configuration)
- [Body](/documentation/swiftui/disclosuregroupstyle/body)

#### Supporting types

- [AutomaticDisclosureGroupStyle](/documentation/swiftui/automaticdisclosuregroupstyle)

##### Creating the disclosure group style

- [init()](/documentation/swiftui/automaticdisclosuregroupstyle/init())

### Styling navigation views

- [func navigationSplitViewStyle<S>(S) -> some View](/documentation/swiftui/view/navigationsplitviewstyle(_:))
- [NavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle)

#### Creating built-in styles

- [static var automatic: AutomaticNavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle/automatic)
- [static var balanced: BalancedNavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle/balanced)
- [static var prominentDetail: ProminentDetailNavigationSplitViewStyle](/documentation/swiftui/navigationsplitviewstyle/prominentdetail)

#### Creating custom styles

- [func makeBody(configuration: Self.Configuration) -> Self.Body](/documentation/swiftui/navigationsplitviewstyle/makebody(configuration:))
- [NavigationSplitViewStyle.Configuration](/documentation/swiftui/navigationsplitviewstyle/configuration)
- [Body](/documentation/swiftui/navigationsplitviewstyle/body)

#### Supporting types

- [AutomaticNavigationSplitViewStyle](/documentation/swiftui/automaticnavigationsplitviewstyle)

