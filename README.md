# Word Encoder CLI

`word-encoder-cli` is a simple command-line tool built with Go that encodes text using the ROT13 cipher. It features an interactive TUI (Text-based User Interface) powered by `bubbletea`, allowing users to choose between encoding text from a file or from direct keyboard input.

## Features

-   Interactive menu for selecting the input method.
-   **File Mode:** Encodes the contents of a local file (`data.txt`).
-   **Interactive Mode:** Encodes text typed directly into the terminal line by line.
-   Implements the standard ROT13 substitution cipher.

## Prerequisites

-   [Go](https://go.dev/doc/install) version 1.24 or later.

## Installation

1.  Clone the repository to your local machine:
    ```sh
    git clone https://github.com/favourthemaster/word-encoder-cli.git
    ```
2.  Navigate to the project directory:
    ```sh
    cd word-encoder-cli
    ```

## Usage

To start the application, run the following command from the project's root directory:
```sh
go run main.go
```

You will be greeted with an interactive menu to choose your input source:

```
Select if you would like to work with file input or type in input:

(•) File input
( ) Type in input

(press q to quit)
```

### Controls

-   **Up/Down Arrow Keys** (or `k`/`j`): Navigate the menu.
-   **Enter**: Select an option.
-   **q / esc / Ctrl+C**: Quit the application.

### Input Modes

#### File Input

When you select "File input", the program will attempt to read a file named `data.txt` from the same directory. It will encode the entire content of this file using ROT13 and print the output to your terminal.

**To use this mode:**

1.  Create a file named `data.txt` in the project directory.
2.  Add any text you wish to encode into this file.
3.  Run the application and choose the "File input" option.

#### Type in Input

When you select "Type in input", the program will enter an interactive mode where you can type directly into the console. After you type a line of text and press `Enter`, the encoded version of that line will be printed.

To exit this input mode, press `Ctrl+D` (to signal EOF) on a new line.

## Dependencies

This project uses the following Go package to create the terminal interface:

-   [github.com/charmbracelet/bubbletea](https://github.com/charmbracelet/bubbletea)

Go modules will automatically handle the installation of this dependency when you run the program.
