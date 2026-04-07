---
name: swiftui
description: SwiftUI API reference for macOS, iOS, visionOS. Use this skill whenever writing, reviewing, or debugging SwiftUI code — views, modifiers, layout, animation, data flow, event handling, accessibility, or UIKit/AppKit integration. Also use when the user asks about SwiftUI APIs, view modifiers, property wrappers, or needs to verify correct API usage for a specific Swift/platform version.
---

# SwiftUI API Reference

Complete SwiftUI framework reference from Apple Developer Documentation (2026).

## How to use this skill

1. Identify which topic area the task involves from the index below
2. Read only the relevant reference file(s) — do not load all files
3. Each reference file has its own table of contents at the top for fast scanning

## Topic Index

| Topic | File | What's in it |
|-------|------|-------------|
| App structure | `references/app-structure.md` | App protocol, scenes, windows, window groups, documents, navigation (NavigationSplitView, TabView), modal presentations, toolbars, search, ornaments |
| Data and storage | `references/data-storage.md` | @State, @Binding, @Observable, @Environment, preferences, @FetchRequest, @Query, @AppStorage, @SceneStorage, file management |
| Views: styling and animation | `references/views-styling-animation.md` | View protocol, view modifiers, view lifecycle, Liquid Glass, button/picker/toggle/menu styles, animations (phase, keyframe, transitions), TimelineView |
| Views: text and images | `references/views-text-images.md` | Text, AttributedString, TextField, TextEditor, SecureField, text selection, Font, Image, AsyncImage, canvas rendering |
| Views: controls | `references/views-controls.md` | Button, Link, Slider, Stepper, Picker, DatePicker, ColorPicker, Toggle, ProgressView, ContentUnavailableView, menus, commands |
| Views: shapes and drawing | `references/views-shapes-drawing.md` | Rectangle, Circle, Capsule, Path, Shape protocol, InsettableShape, fills/strokes, Canvas, GraphicsContext, Color, gradients, materials, ShapeStyle |
| Views: effects and geometry | `references/views-effects-geometry.md` | Transforms (scale, rotate, offset), blur, shadow, clipping, compositing, GeometryReader, GeometryProxy, Metal shaders, scroll views, safe area, alignment, padding |
| View layout | `references/view-layout.md` | HStack, VStack, ZStack, LazyHStack, LazyVStack, Grid, GridRow, Layout protocol, custom layouts, spacing, alignment guides, coordinate spaces |
| Event handling | `references/event-handling.md` | Gestures (Tap, LongPress, Drag, Magnify, Rotate), keyboard input, focus, hover, scroll events, clipboard/pasteboard, drag and drop, DigitalCrownEvent |
| Accessibility | `references/accessibility.md` | Accessibility modifiers, labels, traits, actions, rotor, VoiceOver, assistive technologies |
| Framework integration | `references/framework-integration.md` | UIViewRepresentable, NSViewRepresentable, UIViewControllerRepresentable, NSViewControllerRepresentable, WKInterfaceObjectRepresentable, UIHostingController, NSHostingController |

## Quick lookup patterns

**Property wrappers**: `references/data-storage.md` — @State, @Binding, @Observable, @Environment, @AppStorage, @FetchRequest, @Query

**Navigation**: `references/app-structure.md` — NavigationSplitView, NavigationStack, NavigationLink, TabView

**Lists and collections**: `references/views-effects-geometry.md` — List, Table, ScrollView, ForEach, LazyVGrid, LazyHGrid

**Modals**: `references/app-structure.md` — .sheet, .fullScreenCover, .popover, .alert, .confirmationDialog, .inspector

**Layout**: `references/view-layout.md` — stacks, grids, custom Layout protocol, alignment, spacing

**Gestures**: `references/event-handling.md` — TapGesture, DragGesture, gesture composition

**Bridging UIKit/AppKit**: `references/framework-integration.md` — representable protocols, hosting controllers
