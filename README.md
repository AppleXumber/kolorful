# Kolorful

**Kolorful** is a Kotlin library designed to facilitate printing colored and styled text to the terminal using ANSI codes. This project allows for the customization of text color, background color, and text style (bold, underlined, etc.), with support for RGB values and predefined colors.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
    - [Code Example](#code-example)
    - [Supported Parameters](#supported-parameters)
- [Supported Styles](#supported-styles)
- [Supported Colors](#supported-colors)
- [Show 255 Colors](#show-255-colors)
- [License](#license)

## Installation

To use **Kolorful**, simply download the source code and include it in your Kotlin project. You can copy the files directly or integrate the class into your Maven or Gradle project.

## Usage

### Code Example

``` Kotlin
fun main() {
  val kolorful = Kolorful()
  val myString = "Hello World!"

  // Example using custom RGB values
  kolorful.println(myString, "255;00;250")

  // Example using predefined colors and styles
  kolorful.println(
    myString,
    Color.Red,
    Color.Black,
    Style.Bold,
    Style.Underlined
  )
}
```

### Supported Parameters

The `Kolorful` class offers two main methods: `print` and `println`. Both accept the following optional parameters:

- `message`: Any value to be printed (String, Int, etc.).
- `color`: Text color, which can be a predefined color (enum `Color`), an RGB value as a string in the format `R;G;B`, or an integer representing the color (0-255).
- `backgroundColor`: Background color, similar to the `color` parameter, using the enum `Color`, RGB values, or integers.
- `Style`: Text styles such as bold, underlined, italic, or strikethrough (enums `Style`).

## Supported Styles

The supported styles are defined in the `Style` enum:

- `Bold`: Bold text
- `Underlined`: Underlined text
- `Italic`: Italic text
- `Strikethrough`: Strikethrough text

You can combine how many styles as you want.

## Supported Colors

Colors are defined by the `Color` enum:

### `Color` Enum
- `Red`
- `Blue`
- `Black`
- `Green`
- `Yellow`
- `Magenta`
- `Cyan`
- `White`


Additionally, you can use RGB values in the format `"R;G;B"` or integers from 0 to 255.

## Show 255 Colors

The `show255Colors` function allows you to display all available colors from 0 to 255.

``
kolorful.show255Colors()
``

## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT). Feel free to use and modify it as needed.
