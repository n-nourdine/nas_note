# nas_note

A Flutter package for secure note-taking with SQLite storage, supporting both mobile and desktop platforms.

## Features

- Create, read, update, and delete notes
- Cross-platform support (iOS, Android, Windows, Linux, macOS)
- Simple and intuitive API
- SQLite storage using sqflite and sqflite_common_ffi

## Getting started

Add this package to your Flutter project:

```yaml
dependencies:
  nas_note: ^0.0.1
```

## Usage

```dart
// Initialize the database
await DatabaseHelper.instance.initializeDatabaseFactory();

// Create a note
final note = Note(
  title: 'My Note',
  description: 'This is my first note',
  date: DateTime.now().toIso8601String(),
);

// Add the note to the database
await DatabaseHelper.instance.addNote(note);

// Get all notes
final notes = await DatabaseHelper.instance.getAllNotes();

// Update a note
final updatedNote = Note(
  id: 1,
  title: 'Updated Note',
  description: 'This note has been updated',
  date: DateTime.now().toIso8601String(),
);
await DatabaseHelper.instance.updateNote(updatedNote);

// Delete a note
await DatabaseHelper.instance.deleteNote(1);
```

## Additional information

For more information, please visit the [GitHub repository](https://github.com/yourusername/nas_note).

-------------------
