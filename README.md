
<img width="207" alt="Screenshot 2025-02-16 at 9 11 12 PM" src="https://github.com/user-attachments/assets/d84dc7f2-95d7-47d0-8c04-bb8701cf396a" />

Analytics Tools for Small Data

## What is Mako?

Mako is a modern web-based analytics platform that combines the power of an interactive code editor with robust data management capabilities. It provides data scientists, analysts, and developers with a seamless environment for writing, executing, and analyzing python code alongside powerful data visualization features. 

Mako is an analytics IDE with an opinion. Out of the box, it allows for a small set of python modules to be imported and used. 
- All built in python functions
- Polars for data processing
- Bokeh for plotting
- Pyarrow for data transfer

However, it is easy to add more modules as needed. The goals is to provide a concise workspace that is light in dependencies and easy to install.

## Key Features

- 🚀 Interactive code editor with syntax highlighting and multiple language support
- 📊 Real-time code execution environment
- 💾 Efficient data management system for importing and analyzing datasets
- 🎨 Beautiful split-pane interface with adjustable views
- 📁 Smart file management with multiple tabs
- 📈 Dataset visualization and analysis tools
- ⌨️ Comprehensive keyboard shortcuts for productivity
- 📝 SQL query support with dataset integration
- 📊 Interactive Bokeh plotting functionality

## Tech Stack

### Frontend
- SvelteKit
- Monaco Editor (VS Code's editor)
- TypeScript
- Bokeh for interactive visualizations

### Backend
- FastAPI
- Polars for data processing
- DuckDB for SQL queries
- Ruff for code linting
- Python standard library

## Local Development Setup

Prerequisites:
- Python 3.11+
- Node.js 18+
- uv package manager (for Python dependencies)

Launch development environment:
```bash
./mako run
```

This script will:
- Check for required Python and Node.js versions
- Install dependencies using uv
- Start both frontend and backend servers
- Automatically open your browser

## Configuration Setup

1. **Copy the example config**:
   ```bash
   cp config/mako.conf.example config/mako.conf
   ```

2. **Modify settings** in `config/mako.conf`:
   ```bash
   # Development settings
   ENVIRONMENT="development"
   LOG_LEVEL="debug"
   
   # Production adjustments
   # HOST="0.0.0.0"
   # ENVIRONMENT="production"
   # DEV_RELOAD="false"
   ```

3. **Secure sensitive values** using environment variables:
   ```bash
   export MAKO_API_KEY="your-secret-key"
   ```

4. **Run the application**:
   ```bash
   ./mako run
   ```

## Contributing

We welcome contributions! Please feel free to submit a Pull Request. I will make sure any accepted PRs are added to the next release and you are credited in the changelog.
