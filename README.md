# Slidev Theme - NMT (Unofficial)

[![NPM version](https://img.shields.io/npm/v/slidev-theme-nmt?color=F141A8&label=)](https://www.npmjs.com/package/slidev-theme-the-unnamed)

A [Slidev](https://sli.dev/) theme based on the [The unnamed - VS Code theme](https://marketplace.visualstudio.com/items?itemName=eliostruyf.vscode-unnamed-theme) by [Elio Struyf](https://elio.dev).

This (unofficial) theme is for use IT lecturers at North Metropolitan TAFE.

We are restricting the customisation ability, but welcome feedback.

## Latest Update

- Add `Announcement` component ([Skip to Components section](#components))
- Tidy up errors in `ReadMe.md`
- 

## Usage

Add the following frontmatter to your `slides.md`.

Start Slidev then it will prompt you to install the theme automatically.

```yaml
---
theme: nmt
---
```

## Layouts

The theme currently has the following layouts:

- `about-me`
- `center`
- `cover`
- `default`
- `end`
- `grid`
- `section`
- `two-cols`
- `two-cols-2-1`
- and the ones from Slidev itself

### Cover

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/cover.png?raw=true)

#### Usage

```yaml
---
layout: cover
---
```

### About me

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/about-me.png?raw=true)

#### Usage

```yaml
---
layout: about-me

helloMsg: Your Presenter
name: Adrian Gould
position: left
company: "North Metropolitan TAFE"
jobRole: "ASL | HelpDesk Admin | ScreenCraft Admin"
subjects: "SaaS, API Dev, IoT"
msTeams: "Teams: adrian.gould@nmtafe.wa.edu.au"
website: "https://northmetrotafe.wa.edu.au"
github: "https://github.com/adygcode"
imageSrc: /ajg-designer.png
---
```

### Center

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/center.png?raw=true)

#### Usage

```yaml
---
layout: center
---
```

### Section

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/section.png?raw=true)

#### Usage

```yaml
---
layout: section
---
```

### Two columns

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/two-cols.png?raw=true)

#### Usage

```yaml
---
layout: two-cols
---

# Left

This shows on the left

::right::

# Right

This shows on the right
```

### Two columns 2-1

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/two-cols-2-1.png?raw=true)

#### Usage

```yaml
---
layout: two-cols-2-1
---

# Left

This shows on the left

::right::

# Right

This shows on the right
```

### Default

![](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/code.png?raw=true)

#### Usage

```yaml
---
layout: default
---
```

## Components

### Announcement component

A small component to add an announcement to a page.

> **TODO**: Move this component into a separate repository

Used in the form:

```vue
<Announcement type="default" title="Default Note" inline compact >
    Just something to think about
</Announcement>
```

- Types:
    - `type="type_identifier"`
    - where `type_identifier` is one of:
        - `brainstorm`
        - `duration`
        - `idea`
        - `default`
        - `info`
        - `important`
        - `priority`
        - `warning`
        - `error`

- Options:
    - `compact` or `compact="true|false"`
        - a smaller sized version (**optional**, default `false`)
    - `title="..."` 
        - title text (`...`) shown before the slot content (**optional**)
    - `inline` or `inline="true|false"` 
        - allow multiple announcements on a line (**optional**, default `false`)
    - `width="fit|full"` 
        - resizes to `full` width or `fit` to content (**optional**, default `fit`)

#### Icon Override

It is possible to override the icons:

```vue
<Announcement type="info" title="Heads up">
    Custom icon via slot
    <template #icon>
        <i class="i-fa7-solid-user-ninja h-5 w-5 mt-0.5"></i>
    </template>
</Announcement>
```

![Components](https://github.com/AdyGCode/slidev-theme-nmt/blob/main/assets/announcements.png?raw=true)




![Visits](https://visitorbadge.vercel.app//api/badge/0eb6e5bf-1c67-400f-a9b3-17f25997c209?style=for-the-badge&color=bd0000&labelColor=000000)
