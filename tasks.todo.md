0.2.7 (Small patches) { Small tweaks and large rewrites to make Ox more comfy }
- [ ] Rewrite using crossterm for windows support and efficiency*
  - [ ] Build RGB ansi code function
  - [ ] Fix unwrap on terminal size
  - [ ] Properly implement terminal resizing
- [ ] Undoing
  - [ ] Undoing to origin makes file not dirty
    - [ ] Add last save index (0) to document
    - [ ] Set to patch number on save event
    - [ ] Detect when at last save index
      - [ ] Make not dirty
  - [ ] Undo / Redo patch limit to prevent high memory usage
    - [ ] When undo stack reaches a length over patch limit
    - [ ] Ensure that the file doesn't go back to not dirty!!!
- [ ] Bug Fixing
  - [ ] Add log file
    - [ ] Add command line option for log file location
    - [ ] Add support for appending to the log file
    - [ ] Add option to clear log file on start
    - [ ] Set up log file
  - [ ] Fix potential tab issues
    - [ ] Reproduce
    - [ ] Fix
  - [ ] Fix windows linebreak issue*
    - [ ] Reproduce
    - [ ] Fix
  - [ ] Fix file hanging*
    - [ ] Reproduce
    - [ ] Fix
- [ ] CLI
  - [ ] Allow jump to lines*
    - [ ] Add to help menu
    - [ ] Parse file name
- [ ] Themes
  - [ ] Allow changing of colours of warning, info and error messages in config file
    - [ ] Add to configuration file
    - [ ] Apply
  - [ ] Small line specific retokenization for performance
    - [ ] Added edited flag to each line
      - [ ] Update flag on edit
      - [ ] Update flag on retokenization
    - [ ] Add group list to each line
      - [ ] Update when group is edited
      - [ ] Update when group is retokenized
    - [ ] Only initially render if in view
  - [ ] Highlight search and replace messages
    - [ ] Add token priorities and background tokens
  - [ ] Transparent background
    - [ ] Add option to configuration file
    - [ ] Strip background colour
  - [ ] Improved language syntax highlighting support
  - [ ] 8/16 bit colour fallback*
    - [ ] Create 8 bit colours
    - [ ] Detect when fallback is required
      - [ ] Use colours
  - [ ] Live / Command for reloading of the config file
    - [ ] Create config reload command
    - [ ] Actually reload the config
  - [ ] Line number background
    - [ ] Add to configuration file
    - [ ] Add to line renderer
  - [ ] Add more languages
    - [ ] PHP*
    - [ ] JSON*
    - [ ] HTML*
    - [ ] CSS*
    - [ ] x86 Assembly
    - [ ] Go
    - [ ] C++
    - [ ] C#
    - [ ] Java
    - [ ] SQL
- [ ] General Editing
  - [ ] File overwrite prevention
    - [ ] Detect if file exists
      - [ ] Add overwrite confirmation
  - [ ] Fix hardcoded values
    - [ ] Fix confirm prompt values
  - [ ] Goto only if not on screen
    - [ ] Detect if cursor is on screen
      - [ ] Decide what to do
  - [ ] Better file save error messages
    - [ ] Fix weird behaviour when file has no path
  - [ ] Add support for cursor line wrapping*
    - [ ] Add option to config file
    - [ ] Apply
  - [ ] Save as sudo / read only files*
    - [ ] Add -r flag
    - [ ] Create read only mode
  - [ ] Don't load entire file into memory*
    - [ ] Research
    - [ ] Implement
  - [ ] Backup
    - [ ] Add configuration options
    - [ ] Backup to specific folder somewhere
  - [ ] Add help menu to view keybindings*
    - [ ] Add API to display boxes over existing text
    - [ ] Show overlay
    - [ ] Hide overlay
    - [ ] Handle resizes
  - [X] Ctrl + Z for undo
- [ ] Searching
  - [ ] Exit search when typing characters and catch up with events
- [ ] Formatting
  - [ ] Clippy
  - [ ] Rustfmt

0.2.8 (Mouse support) { To allow the mouse cursor to move the editor cursor & select text }
- [ ] Mouse selection support*
  - [ ] Read mouse events
  - [ ] Move the cursor when clicking with mouse
  - [ ] Add selection mode to document
  - [ ] Allow text selection with the mouse cursor

0.2.9 (Extensibility) { To allow even more extension to the editor }
- [ ] Delete word
- [ ] Move word
- [ ] Add option to hide parts of the editor (e.g. status line, tab line)

0.3.0 (IDE level features) { Allow for IDE level features to smooth out development experience }
- [ ] Auto indentation 
  - [ ] Detect when to auto indent
  - [ ] Find the amount of tabs needed
  - [ ] Insert tabs there
- [ ] Prettier
  - [ ] Find a way to access the prettier API
  - [ ] Add a confirmation
- [ ] Linting
  - [ ] Read output from cargo's JSON
  - [ ] Display issues in the command line
  - [ ] highlight different colors for errors and warnings
  - [ ] Add support for Pylint readings

0.3.1 (IDE level features #2) { More IDE level features }
- [ ] Auto brackets
  - [ ] Automatically insert brackets on opening pair
    - [ ] <
    - [ ] (
    - [ ] [
    - [ ] {
    - [ ] "
    - [ ] '
    - [ ] `
    - [ ] |
  - [ ] Move them around when pressing enter

0.3.2 (IDE level features #3) { Even more IDE features }
- [ ] Auto complete*
  - [ ] Get information from racer and display it in a menu
  - [ ] Add configuration entries for the autocomplete
  - [ ] Add support for file autocomplete too

0.3.3 (Navigation) { To help with navigating and managing your project from within the editor }
- [ ] File tree
  - [ ] Allow the document to be shifted up a bit
  - [ ] Render random text to the left of the document
  - [ ] List directory
  - [ ] Add cursor focus variable
  - [ ] Add mutable flags
  - [ ] Allow opening of files
  - [ ] Allow collapse and expand of files
  - [ ] Add sorting
  - [ ] Add file operations
    - [ ] New directory
    - [ ] New file
    - [ ] Delete directory
    - [ ] Delete file
    - [ ] Move file
    - [ ] Copy file

0.3.4 (Start up experience improvements) { Add a help menu and start menu and session saver }
- [ ] Start page
  - [ ] Store recently used documents
  - [ ] List them out
- [ ] Add ability to save sessions and load them from cli and start page
- [ ] Add detailed help menu / document / mode

Further ideas { Further fun ideas to look at }
- [ ] File encryption and decryption
- [ ] Automatically closing status line
- [ ] Discord rich presence
- [ ] Nice, personal greeting
- [ ] Theme changing depending on time of day
- [ ] Live HTML editor
- [ ] Split editors
- [ ] Terminal integration
- [ ] Todo list
- [ ] Cheatsheet downloader
- [ ] Stack overflow searcher
- [ ] HTML expansion like emmet
- [ ] Documentation viewer
- [ ] Pomodoro timer for work / rest balance
- [ ] Easter eggs
- [ ] Automated tests
- [ ] Theme builder
- [ ] Typing speed tests / statistics
- [ ] Package manager

0.1.1
- [X] Go to the next line at end of line
- [X] Go to the previous line at start of line
- [X] Solve unicode width issues
  - [X] Fix unicode cursor issues
  - [X] Add Home / End / PageUp / PageDown support
  - [X] Fix offset up/down issues
  - [X] Fix dodgy up/down unicode issues
- [X] Insertion of characters
- [X] Deletion of characters
  - [X] Deletion in middle of line
  - [X] Deletion at start of line
  - [X] Deletion at end of line
- [X] The enter key
  - [X] Enter at the start of a line
  - [X] Enter at the end of a line
  - [X] Enter in the middle of a line
- [X] Render tabs (4 spaces)
- [X] Save
- [X] Save as
- [X] Dirty files
- [X] Quit confirmation
- [X] Improve status bar
  - [X] File identification
  - [X] Cursor position
  - [X] File name
  - [X] File edited
  - [X] Current line
- [X] Revamp theme
- [X] Thorough commenting
- [X] Privatisation

0.2.0
- [X] Line numbers
- [X] Open document
- [X] New document
- [X] Search feature
  - [X] Searching on the same line as the cursor
    - [X] Backwards
    - [X] Forwards
  - [X] Searching forward by default
  - [X] Scroll offset with search
    - [X] Ensure the initial offset is saved
    - [X] Move the offset

0.2.1 (Undo & Redo)
- [X] Undo / Redo
  - [X] Undo
    - [X] Add event executor
  - [X] Set up EventStack
    - [X] Read Insertion
    - [X] Read Deletion
    - [X] Add reverse event lookup
    - [X] Read NewLine
      - [X] End of line
      - [X] Start of line
      - [X] Middle of line
    - [X] Support for offsets
    - [X] Read DeleteLine
      - [X] Middle of line
      - [X] Start of line
  - [X] Redo
    - [X] Set up seperate redo stack
    - [X] Clear redo stack on change
    - [X] Link up operations
  - [X] Set up smart undoing / redoing to undo by groups of common events
  - [X] Commit changes after inactivity period
  - [X] Refactor

0.2.2 (Input bug solving)
- [X] Fix clipboard bug

0.2.3 (Interface improvements)
- [X] CLAP cli
  - [X] Update documentation
- [X] Config file
  - [X] Add a default config path
  - [X] Allow a config argument
  - [X] Add hardcoded backup config file
  - [X] Read a config file and populate values
  - [X] Have a few example config files
  - [X] Left line number padding
- [X] Change default theme
- [X] Updated logo
- [X] Performance optimizations
- [X] No unwrap calls to reduce runtime errors
- [X] Proper status line and welcome message wrapping
- [X] Added left line number padding
- [X] Improved search command to show results in the middle of screen
- [X] Replace
  - [X] Fix X offset jumping
  - [X] Create replace all command
  - [X] Create replace some command
  - [X] Allow Regex expressions to be used?

0.2.4 (Syntax highlighting)
- [X] Add support for reading XDG config variable
- [X] Fix blank file runtime error
- [X] Use RON format instead
- [X] Syntax Highlighting
  - [X] Add basic Rust syntax
  - [X] Create a theme and regex definitions
  - [X] Implement basic colourization
  - [X] Fix overlapping tokens
  - [X] Fix fallout with unicode and trimming
    - [X] Trimming start
    - [X] Unicode
    - [X] Trimming end
  - [X] Finish Rust highlighting
  - [X] Add syntax to config file
  - [X] Allow for file type specific syntax highlighting
  - [X] Optimize
  - [X] Allow for multiline syntax highlighting
  - [X] Add Python
  - [X] Add Javascript
  - [X] Add C
  - [X] Add Ruby
  - [X] Add Crystal

0.2.5 (Multitasking) { Manage multiple buffers in one instance }
- [X] Tabs
  - [X] Allow holding several documents
  - [X] Set up current doc variable
  - [X] Rewrite editor to use documents from current doc
  - [X] Allow editor to move between different documents
  - [X] Add tab line
  - [X] Ctrl + Q closes document rather than editor
  - [X] Make current tab bold
  - [X] Remove open confirmation
- [X] Update hardcoded config file
- [X] Balance load between editor and document files
  - [X] Move variables
  - [X] Move methods around
- [X] Save all
  - [X] Add dirty indicator to tab
  - [X] Write function
  - [X] Set up keybinding
- [X] Dynamic tab offset

0.2.6 (Macros) { Allow for more keybindings and operations }
- [X] Fix file tab issue (27th)
- [X] Fix (0, 0) deletion issues
- [X] Macro system
  - [X] Allow special command mode
  - [X] Create Oxa parser (25th)
  - [X] Create unified event executor (2nd)
    - [X] Document functions
    - [X] Cursor functions
    - [X] Mass edit functions
    - [X] Tab functions
    - [X] Insertion function
    - [X] Allow repeated Ox commands
    - [X] Backspace functions
    - [X] Return functions
    - [X] Storage functions
    - [X] Allow multiple event execution
    - [X] Allow undo via reverse execution
      - [X] Split up events as much as possible
      - [X] Write the reverses for them
      - [X] Redo
      - [X] Fix committing issues
    - [X] Clippy
    - [X] Thorough Testing
  - [X] Write documentation for Ox (3rd)
  - [X] Have a few example macros (3rd)
    - [X] Goto line number
    - [X] Delete line
    - [X] Move cursor
    - [X] Move line
    - [X] Move forward a word
    - [X] Move backward a word
  - [X] Allow binding of macros to some keys (4th)
- [X] Distribution
  - [X] Rpm
  - [X] Deb
  - [X] Homebrew
- [X] Add more configuration options in the config file (6th)
  - [X] Multiple themes
    - [X] Read from config file
    - [X] Allow switching via command
  - [X] Status line format
    - [X] Form structure for information
    - [X] Allow config file reading
    - [X] Apply it
  - [X] Tab line format
    - [X] Add to configuration file
    - [X] Apply it
  - [X] Predefined macros
    - [X] Create it in config file
    - [X] Read and allow execution
  - [X] Update wiki

