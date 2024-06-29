![Screenshot 2024-03-09 at 0 28 29](https://github.com/samuelarbibe/dnd-timeline/assets/38098325/d7639942-0727-4f0f-91c3-eef43cb7f40b)

# [🎉 dnd-timeline](https://dnd-timeline.com)

## dnd-timeline: A headless timeline library, based on [`dnd-kit`](https://docs.dndkit.com/)



- **Headless:** `dnd-timeline` is a headless-ui library, and contains 0 styling, aside from functional styling (position, z-index, etc.).
- **Hook-based:** exposes simple hooks like `useItem` and `useRow`, that should integrate seamlessly into your existing architecture.
- **Flexible:** very slim and flexible by design. `dnd-timeline` exposes utility functions and positional styling, and you can use them in conjunction with you favorite libraries - styling libraries (MUI, tailwindcss, ant-design, etc.), and functional libraries (react-virtual, framer-motion, etc.)
- **Based on [`dnd-kit`](https://docs.dndkit.com/):** all features exposed by the [`dnd-kit`](https://docs.dndkit.com/) library are applicable to dnd-timeline.
- **Performant:** renders only when needed. All the intermediate states and animations are done using css transformations, and require 0 re-renders.
- **RTL:** `dnd-timeline` nativly supports RTL. simply declare one of the parent divs as rtl with `dir="rtl"`, and thats it.

![2024-03-09 00 35 27](https://github.com/samuelarbibe/dnd-timeline/assets/38098325/39e1e0c7-22ac-4286-8f35-58dc7380b7eb)

## Installation

The library requires a single peer-dependency: react

To install it, run:

```sh
npm install react
```

Then, you can install the library itself:

```sh
npm install dnd-timeline
```

## Features

- **Stacked rows:** Items whose relevance's intersect are stacked on top of each other inside the same row.
- **Snap to Grid:** Items snap into a pre-defined grid when dropped, that can be changed according to zoom level.
- **Time Axis:** An optional time axis can be displayed, with different markers according to zoom level.
- **Time Cursor:** An optional time cursor indicating the current time on top of the timeline.
- **Pan and zoom:** You can zoom by holding <kbd>Ctrl</kbd> and scrolling using the mouse wheel, and pan by holding <kbd>Ctrl + Shift</kbd> scrolling using the mouse wheel.
  ![2023-07-09 20 27 50](https://github.com/samuelarbibe/dnd-timeline/assets/38098325/b94f870b-5d32-4099-92f7-a1a236dbf7b1)
- **Dynamically disabled rows and items:** Items and Rows can be disabled according to a client-defined logic.
  ![2023-07-09 20 29 15](https://github.com/samuelarbibe/dnd-timeline/assets/38098325/a21f3afc-d075-448a-8fb7-fb445351b9f5)
- **Integration with external DnD:** The timeline can be used in conjunction with other DnD interactions in you app, to drag items into and outside of the timeline.
  ![2023-07-09 20 30 25](https://github.com/samuelarbibe/dnd-timeline/assets/38098325/bd354d06-415a-4561-9476-1b9b8463cdd1)

## Contribute

This project uses [turborepo](https://turbo.build/repo/docs) to manage the monorepo.
It also uses [pnpm](https://pnpm.io/) instead of npm as a package manager.

To install pnpm, you can run:
```sh
corepack enable pnpm
```

If you want to develop on your local machine, simply clone the project, and run

```sh
pnpm install
pnpm run dev
```

And all the examples will run on your local machine, likned to the local instance of the library.
Any changes made to the library will be reflected in the examples.

If you want to run only a specific example, checkout turborepo's [`--filter`](https://turbo.build/repo/docs/crafting-your-repository/running-tasks#using-filters) operator:
```sh
pnpm run dev --filter home...
```
For example this will run the `home` package and all the packages' it is depending on (`dnd-timeline`).
