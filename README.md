# Edith File Manager

**Version**: 2.5.3  
**Application Title**: Edith File Manager

This is a simple PHP-based file management system that allows users to view and manage files in a web environment.

## Features

- Authentication with username and password
- Role-based access (readonly for specific users)
- Error reporting and theming customization
- Light and simple configuration for file management

## Configuration

### Authentication

Authentication is enabled by default. You can manage users and their access in the configuration.

- **$use_auth**: Set to `true` to enable authentication.  
- **$auth_users**: Define users and their password hashes here. The file uses PHP's `password_hash` function for security.
  ```php
  $auth_users = array(
      'admin' => 'hashed_password_for_admin',
      'user' => 'hashed_password_for_user'
  );
  ```
  By default, the application has two users:
  - `admin`: admin@123
  - `user`: 12345

- **Readonly users**: You can restrict certain users to read-only access by adding them to the `$readonly_users` array.
  ```php
  $readonly_users = array('user');
  ```

### Theme and Error Reporting

- **$CONFIG**: The default settings include:
  - `lang`: Language of the interface (default is English).
  - `error_reporting`: Toggle error reporting.
  - `show_hidden`: Option to display hidden files.
  - `hide_Cols`: Option to hide columns in the file manager.
  - `theme`: Choose between "light" and "dark" themes.

### Readonly Mode

- **$global_readonly**: When set to `true`, the application will operate in read-only mode globally, meaning no file modifications can be made.

## Security Notes

- Passwords are hashed using `password_hash`, ensuring a secure login system.
- Ensure to update default user passwords before using the application in production.

## How to Use

1. Modify the configuration in `index.php` as needed.
2. Upload the files to your server.
3. Open the application in a browser, and log in using the credentials.


## Requirements

- PHP 5.5.0 or higher.
- Fileinfo, iconv, zip, tar and mbstring extensions are strongly recommended.

### :loudspeaker: Features

- :cd: Open Source, light and extremely simple
- :iphone: Mobile friendly view for touch devices
- :information_source: Basic features likes Create, Delete, Modify, View, Download, Copy and Move files
- :arrow_double_up: Ajax Upload, Ability to drag & drop, upload from URL, multiple files upload with file extensions filter
- :file_folder: Ability to create folders and files
- :gift: Ability to compress, extract files (`zip`, `tar`)
- :sunglasses: Support user permissions - based on session and each user root folder mapping
- :floppy_disk: Copy direct file URL
- :pencil2: Cloud9 IDE - Syntax highlighting for over `150+` languages, Over `35+` themes with your favorite programming style
- :page_facing_up: Google/Microsoft doc viewer helps you preview `PDF/DOC/XLS/PPT/etc`. 25 MB can be previewed with the Google Drive viewer
- :zap: Backup files and IP blacklist and whitelist
- :mag_right: Search - Search and filter files using `datatable js`
- :file_folder: Exclude folders and files from listing
- :globe_with_meridians: Multi-language(32+) support and for translations `translation.json` is file required
- :bangbang: lots more...