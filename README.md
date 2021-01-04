# TailBlazor.HeroIcons

Tailwindcss HeroIcons for Blazor!

This package includes all 226 icons in the HeroIcon pack as of Version 0.4.1.

The full icon pack can be previewed here: [HeroIcons.com](https://heroicons.com)

This pack allows you to modify: size, stroke(colour), stroke width, width and height, and style (outlined or solid) for all the icons in an easy package with easy searching of available icons.


![Nuget](https://img.shields.io/nuget/v/TailBlazor.HeroIcons.svg)

![Demo](screenshot.png)

## Getting Setup

You can install the package via the NuGet package manager just search for TailBlazor.HeroIcons. You can also install via powershell using the following command.

`Install-Package TailBlazor.HeroIcons`

Or via the dotnet CLI.

`dotnet add package TailBlazor.HeroIcons`

### 1. Add Imports

Add line to your \_Imports.razor

```
@using TailBlazor.HeroIcons
```

### 2. Create HeroIcon Component

Add `TailBlazorHeroIcon` to your Blazor component and select the icon using `HeroIcon` enum.
Due to enum limitations they have been modified to removed '-'.

`clipboard-copy` has been changed to `ClipboardCopy`

```
<TailBlazorHeroIcon Icon="HeroIcon.X" />
```

### 3. Customization

By default you don't need to include anything but the `Icon` parameter. However if you want to customize aspects of the icon you can. by default they all have base values. The follow parameters are available

Parameter | Default Value
--- | ---
`Width` | `64`
`Height` | `64`
`StrokeWidth` | `2`
`Stroke` | `text-black`
`IconStyle` | `IconStyle.Outline`
`EnableComments` | `false`

Width, Height, and StrokeWidth all take an int.

Stroke takes any tailwind text colour you've added to your project: `text-blue-500`

IconStyle accepts `.Outline` and `.Solid`

when comments are enabled they can allow it easier for you to remember what you've used when inspecting an element for debugging.
Enabling it shows the following comment above the icon

`<!-- HeroIcon: annotation (style: outlined, size: 64x64, stroke (colour): text-grey-500, stroke-width: 2) -->`