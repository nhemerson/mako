# Changelog

## [Unreleased] - 2025-02-17

### Added
- Enhanced backend startup and configuration management
  - Improved startup.sh script with better path handling and configuration validation
  - Added comprehensive config file validation in validate_config.sh
  - Enhanced mako script with better Python version detection and environment setup
  - Added uv package manager integration for more reliable dependency management
  - Improved error handling and user feedback during startup
  - Added support for MAKO_CONFIG environment variable to override config location
  - Enhanced production safety checks and environment validation
  - Added IP address validation for HOST configuration

### Changed
- Updated Python and Node.js version requirements in template files
- Updated requirements.txt with latest dependency versions

## [Unreleased] - 2025-02-16

### Added
- Added datetime module (datetime, date, timedelta) to safe_globals
- Added random module to safe_globals for random number generation
- Integrated Bokeh plotting functionality
  - Shortcut to open bokeh plot in a new tab
  - Added support for interactive data visualization using Bokeh
  - Automatic plot rendering in output cells
  - Support for multiple plot types (line, scatter, bar charts)
  - Interactive features including zoom, pan, and hover tooltips
  - Plot state persistence across sessions
  - Responsive plot sizing within the notebook interface
  - Organized shortcuts by category (Code Execution, File Management, Navigation, Context Files)
  - Accessible keyboard shortcut reference
  - Clean, modern modal design with dark theme
- Enhanced keyboard shortcuts functionality
  - Command+Shift+P (Mac) or Ctrl+Shift+P (Windows) to create new Polars file
  - Command+Shift+L (Mac) or Ctrl+Shift+L (Windows) to create new SQL file
- Improved SQL functionality
  - Added ability to write and execute SQL queries
  - Support for saving SQL query results to Parquet files using `save_as:` directive
  - Automatic dataset registration in SQL context
  - Validation of referenced datasets

## [Unreleased] - 2025-02-11

### Added
- Added Settings Modal with comprehensive keyboard shortcuts display
  - Organized shortcuts by category (Code Execution, File Management, Navigation, Context Files)
  - Accessible keyboard shortcut reference
  - Clean, modern modal design with dark theme
- Enhanced keyboard shortcuts functionality
  - Command+Shift+P (Mac) or Ctrl+Shift+P (Windows) to create new Polars file
  - Command+Shift+L (Mac) or Ctrl+Shift+L (Windows) to create new SQL file
- Improved SQL functionality
  - Added ability to write and execute SQL queries
  - Support for saving SQL query results to Parquet files using `save_as:` directive
  - Automatic dataset registration in SQL context
  - Validation of referenced datasets

## [Unreleased] - 2025-02-10

### Added
- Added "Restore Closed Tab" functionality
  - Command+Shift+R (Mac) or Ctrl+Shift+R (Windows) to restore most recently closed tab
  - Maintains tab history for up to 10 recently closed tabs
  - Preserves tab content and type (code, dataset, or context)
  - Works globally across the entire application

## [Unreleased] - 2024-02-08

### Added
- Combined startup script (`mako`) for easier development setup
- Automatic browser opening on startup
- Integrated uv package manager for Python dependencies

### Changed
- Switched from pip to uv for Python package management
- Improved version checking for Python and Node.js
- Updated documentation with new startup instructions

### Fixed
- Python version detection in startup script
- Node.js version comparison logic

## [Unreleased] - 2025-02-05

### Added
- Fixed dataset context display functionality (2025-02-06)
  - Improved context loading and display in dataset view
  - Correctly shows context content when available
  - Better handling of loading states and error cases
  - Seamless integration with existing context editor
- Added automatic context file cleanup (2025-02-07)
  - Context files (.md) are now automatically deleted when their associated dataset is removed
  - Updated deletion confirmation message to inform users about context file removal
  - Prevents orphaned context files from remaining in storage
- Added keyboard shortcut to toggle sidebar (2025-02-06)
  - Command+D (Mac) or Ctrl+D (Windows) to toggle sidebar visibility
  - Works globally across the entire application
  - Functions within Monaco editors and outside
  - Maintains shortcut functionality regardless of focus state
- Added dataset context documentation feature (2025-02-06)
  - New "Add Context" option in dataset menu
  - Markdown editor for dataset documentation
  - Auto-saves context files alongside datasets
  - Syntax highlighting for markdown
  - Keyboard shortcut (Cmd/Ctrl + S) to save context
  - Context files (.md) stored with datasets for easy reference
- Improved DataFrame view with client-side pagination and formatting (2025-02-06)
  - Enhanced data formatting with proper handling of numeric, boolean, and null values
  - Client-side pagination for better performance with 100 rows per page
  - Improved error handling and loading states
  - Better visual styling with alternating row colors
  - Right-aligned numeric values in monospace font
  - Sticky headers and improved table borders
- Drag-and-drop functionality for editor tabs
  - Tabs can be reordered by dragging and dropping
  - Visual feedback during drag operations
  - Maintains tab state and content during reordering
- Secure environment variables handling for cloud storage access
  - Added support for GCS credentials via .env file
  - Implemented secure credential handling in code execution environment
  - Limited environment variable exposure for enhanced security
  - Fixed SSL compatibility issues with urllib3
- Dataset viewing capability with tabbed interface
- Improved Monaco Editor state preservation when switching between code and dataset tabs
  - Editor state is now maintained when switching between tabs
  - Better performance when switching between code files
  - Smoother transition between code and dataset views
- Enhanced DataFrame UI with DuckDB-inspired design
  - Added sticky headers and improved table styling
  - Added row count display and pagination
  - Improved typography with monospace for numeric values
  - Added alternating row colors for better readability
- Added collapsible Explore section in sidebar for better workspace management
- Added collapsible sidebar with ellipsis toggle
  - Smooth transition animation when collapsing/expanding
  - Maintains state between page reloads
  - Improves workspace real estate management
- Converted Settings page to modal interface
  - Added full-screen dark overlay for better focus
  - Maintained all existing settings functionality
  - Improved accessibility with keyboard navigation
- Added a save method to the LazyFrame returned by the scan_parquet function in ingestion.py
  - This method allows users to collect the LazyFrame 
  - Save it as a Parquet file in the local dataset folder 
  - The method ensures the dataset directory exists before saving 
  - Provides console output to confirm the save operation and file existence.
- Added Monaco editor state persistence across sessions (2025-02-06)
  - Editor tabs and their contents are now preserved when closing/reopening
  - Active tab selection is maintained
  - Editor split pane position is remembered
  - State is automatically saved on changes and tab switches

### Fixed
- Issue where Monaco Editor would lose state when switching to dataset tabs
- Improved tab switching performance by reusing editor instance
