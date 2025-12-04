⚙️ Configuration File Updater
This script provides a single Python function, update_server_config, designed to update specific key-value pairs in simple configuration files (e.g., .conf, .ini).

Core Logic Explained
The function works by using a two-step file handling process:

Read: The file is opened once in read mode ("r") to load all existing lines into memory as a list (lines = file.readlines()).

Write/Rewrite: The file is immediately opened again in write mode ("w"). This action truncates (clears) the file.

Iteration & Update: The script iterates through the stored lines. If a line contains the specified key, it is rewritten with the new key=value string. All other lines are written back exactly as they were, preserving comments and other settings.

Usage
To update a setting, call the function with the file path, the key to find, and the new value.
