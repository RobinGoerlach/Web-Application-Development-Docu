# Tailwind CSS Classes

This document summarizes the Tailwind CSS classes used in a sample HTML file.

## Layout and Positioning:
- `max-w-md`, `max-w-lg`, `max-w-2xl`, `md:max-w-2xl`, `sm:max-w-xl`: Set maximum width for responsive layouts.
- `mx-auto`: Centre's the element horizontally.
- `p-5`, `p-8`, `px-4`, `px-5`, `py-2`, `py-3`, `py-10`, `pl-5`, `pr-5`: Padding on various sides.
- `m-4`, `m-10`, `mt-2`, `mt-3`, `mt-4`, `mt-10`: Margin on various sides.
- `space-y-2`, `space-y-3`: Vertical spacing between child elements.
- `min-h-screen`: Sets minimum height to the screen height.
- `flex`, `flex-col`, `flex-row`, `flex-1`, `sm:flex`, `sm:flex-shrink-0`: Flexbox for layout.
- `grid`, `grid-cols-4`, `grid-cols-6`, `sm:grid-cols-6`: Grid layout with multiple columns.
- `gap-3`: Gap between grid items.
- `absolute`, `relative`: Absolute and relative positioning.
- `float-right`: Floats an element to the right.

## Background Colours and Gradients:
- `bg-gray-200`, `bg-white`, `bg-black`, `bg-pink-400`, `bg-yellow-200`, `bg-red-200`, `bg-blue-200`, `bg-purple-200`, `bg-green-50`, `bg-blue-400`, `bg-gray-100`, `bg-blue-50`, `bg-blue-500`: Various background colours.
- `bg-gradient-to-r`: Horizontal gradient.
  - `from-yellow-600`, `to-blue-400`, `via-black`: Gradient from yellow to blue with black in between.

## Borders and Rounding:
- `border`, `border-solid`, `border-4`: Borders and edges.
- `border-blue-500`, `border-blue-300`: Blue border colours.
- `rounded-md`: Rounded corners.

## Shadows:
- `shadow-md`, `shadow-lg`: Shadows around the element.

## Text and Typography:
- `font-bold`, `font-semibold`, `font-mono`, `italic`, `tracking-wide`: Text styles and font weights.
- `text-white`, `text-blue-900`, `text-gray-700`, `text-gray-800`: Text colours.
- `leading-6`: Line height.

## Responsive Breakpoints:
- `sm:bg-red-200`, `sm:flex`, `sm:hidden`, `sm:block`, `sm:py-12`, `sm:rounded-3xl`, `sm:skew-y-0`, `sm:-rotate-6`, `sm:max-w-xl`: Small screen responsive classes (640px).
- `md:bg-blue-200`: Medium screen responsive class (768px).
- `lg:bg-purple-200`: Large screen responsive class (1024px).
- `xl:bg-yellow-200`: Extra-large screen responsive class (1280px).

## Buttons and Interactivity:
- `hover:bg-blue-900`: Change background colour on hover.
- `focus:outline-none`, `focus:ring`, `focus:ring-offset-2`, `focus:ring-offset-red-500`: Focus styles for interactive elements.

## Custom Classes (defined in internal CSS):
- `.btn-indigo`: Button with blue border, blue background, white text, and hover effect.

This file documents the Tailwind CSS classes used for layout, colours, text formatting, and responsive design.
