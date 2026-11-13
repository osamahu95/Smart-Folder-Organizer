# Smart Folder Organizer

A Windows desktop utility built with **C# and .NET 10 Windows Forms** that helps users automatically organize files into categorized folders based on their file extensions and custom organization rules.

## Overview

Smart Folder Organizer is a lightweight Windows utility designed to simplify file management.

Users can select any directory, scan its contents, preview the proposed organization, and automatically move files into their respective categorized folders.

The primary goal is to make file organization simple, safe, and customizable.

## Features

### 1. Folder Selection
- Select any directory from the local system.
- Browse folders using Windows Folder Browser Dialog.
- Display the selected directory path.
- Validate directory access and permissions.

### 2. File Scanning
- Scan files inside the selected directory.
- Retrieve file names, extensions, sizes, and paths.
- Display scanned files in a DataGridView.
- Handle inaccessible files and directories.

### 3. Automatic File Categorization

Categorize files based on their extensions.

| Category | Extensions |
|---|---|
| Documents | PDF, DOCX, DOC, TXT |
| Images | JPG, JPEG, PNG, GIF, SVG |
| Videos | MP4, AVI, MKV, MOV |
| Audio | MP3, WAV, AAC, FLAC |
| Archives | ZIP, RAR, 7Z |
| Spreadsheets | XLSX, XLS, CSV |
| Applications | EXE, MSI |
| Others | Uncategorized extensions |

### 4. Organization Preview
- Preview the proposed folder structure.
- Show which files will be moved.
- Display source and destination paths.
- Allow users to review changes before execution.

### 5. File Organization
- Automatically create category folders.
- Move files into their respective folders.
- Handle duplicate filenames safely.
- Handle file access and permission errors.
- Display operation progress and results.

### 6. Operation History
- Maintain a record of file movements.
- Store original and destination paths.
- Display operation timestamps.
- Provide the foundation for undo functionality.

### 7. Configuration & Settings
- Configure custom file categories.
- Define custom extension mappings.
- Configure organization rules.
- Persist application settings using JSON.

## Technology Stack

| Technology | Purpose |
|---|---|
| C# | Application development |
| .NET 10 | Runtime |
| Windows Forms | Desktop user interface |
| System.IO | File and directory operations |
| LINQ | Filtering and categorization |
| System.Text.Json | JSON serialization |
| Async/Await | Background operations |

## Project Architecture

The application follows a layered structure to separate UI responsibilities from business logic.

```text
SmartFolderOrganizer/
│
├── Forms/
│   └── MainForm.cs
│
├── Models/
│   ├── FileItem.cs
│   └── OrganizationRule.cs
│
├── Services/
│   ├── FileScannerService.cs
│   ├── FileCategorizerService.cs
│   ├── FileOrganizerService.cs
│   └── HistoryService.cs
│
├── Interfaces/
│   └── IFileOrganizerService.cs
│
├── Configuration/
│   └── appsettings.json
│
├── Resources/
│
├── Program.cs
│
└── README.md
```

## Development Roadmap

### Phase 1: Basic User Interface
- [ ] Create Windows Forms project.
- [ ] Design the main application window.
- [ ] Add folder selection functionality.
- [ ] Add Scan and Organize buttons.
- [ ] Create a DataGridView for displaying files.

### Phase 2: File Scanning
- [ ] Implement FileScannerService.
- [ ] Scan selected directories.
- [ ] Retrieve file metadata.
- [ ] Display scanned files.
- [ ] Handle scanning exceptions.

### Phase 3: File Categorization
- [ ] Implement FileCategorizerService.
- [ ] Define default file categories.
- [ ] Map file extensions to categories.
- [ ] Support uncategorized files.
- [ ] Display category information.

### Phase 4: Organization Preview
- [ ] Generate proposed folder structure.
- [ ] Calculate destination paths.
- [ ] Display source and destination locations.
- [ ] Validate proposed operations.
- [ ] Allow users to review changes.

### Phase 5: File Organization
- [ ] Implement FileOrganizerService.
- [ ] Create category directories.
- [ ] Move files to destination folders.
- [ ] Handle duplicate filenames.
- [ ] Implement progress reporting.
- [ ] Add cancellation support.
- [ ] Handle file operation failures.

### Phase 6: History & Settings
- [ ] Implement HistoryService.
- [ ] Save operation history in JSON.
- [ ] Load previous operation records.
- [ ] Add application settings.
- [ ] Support custom categorization rules.
- [ ] Implement undo functionality.

## Engineering Considerations

The following engineering practices should be considered during development:

- Separation of concerns.
- SOLID principles.
- Interface-based service design.
- Asynchronous file processing.
- Proper exception handling.
- Safe file movement.
- CancellationToken support.
- Logging and diagnostics.
- Input validation.
- Maintainable and testable code.

## Future Enhancements

Potential improvements for future versions:

- Automatic folder monitoring.
- Scheduled file organization.
- Custom user-defined rules.
- Duplicate file detection using SHA-256.
- Advanced filtering and searching.
- Drag-and-drop folder selection.
- Dark and light themes.
- File organization statistics dashboard.
- Undo and restore operations.
- Export organization reports.

## Safety Considerations

File operations should be performed carefully to avoid accidental data loss.

- Always preview file movements before execution.
- Never silently overwrite existing files.
- Handle duplicate filenames safely.
- Preserve original files when an operation fails.
- Provide meaningful error messages.
- Restrict operations to the selected directory and its intended destinations.

## Project Goals

The main objectives of this project are:

1. Build a practical Windows desktop utility.
2. Develop strong C# and WinForms development skills.
3. Understand file system operations in .NET.
4. Practice OOP, SOLID, and clean architecture.
5. Implement asynchronous background processing.
6. Develop a maintainable application that can evolve into a production-quality utility.

---

**Project Name:** Smart Folder Organizer  
**Platform:** Windows Desktop  
**Framework:** .NET 10  
**Language:** C#  
**UI Framework:** Windows Forms  
**Storage:** Local File System + JSON Configuration

**Status:** In Development
