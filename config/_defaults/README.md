# Configuration Directory

This directory contains configuration files for managing file operations and string replacements in your project. Below is a description of each file and its purpose:

## File Descriptions

### `files.txt`
Defines a list of files to be copied, separated by line breaks. Each line specifies a source file and a destination file, separated by a colon (`:`).

- **Source File:** Path calculated from the config directory root.
- **Destination File:** Path calculated from the project directory root.

### `replace.txt`
Includes files where string replacements need to be performed. Each line contains a replacement file name (calculated from the config root), followed by a colon (`:`) and a list of file names or regular expressions where replacements should be made.

### `strings.properties`
Contains pairs of token names and values to perform replacements with. Each line defines a token and its corresponding value, separated by an equals sign (`=`).

### `signing.gradle`
An example of an app signing configuration file. This file typically includes the configuration for signing your Android app, such as the keystore location, alias, and passwords.

## Usage

### File Operations
- Use `files.txt` to determine which files need to be copied or moved from the config directory to the project directory.

- If you want to include specific files in your project: 
1. create empty config/[YourProjectName]/files.txt
2. list required files to copy, following the provided example 

### String Replacements
- Use `replace.txt` and `strings.properties` to perform token replacements in the specified files.

- If you want to replace strings in project-specific file from above step:
1. create empty config/[YourProjectName]/replace.txt
2. create file with required tokens at config/[YourProjectName]/[YourCustomValues].properties
3. register your token file in config/[YourProjectName]/replace.txt together with destination files to perform replacements in.

### App Signing
- Refer to `signing.gradle` for an example of how to configure app signing in your project.

**Note:** Ensure that the paths and tokens are correctly defined in the respective files to avoid any issues during the build process.
