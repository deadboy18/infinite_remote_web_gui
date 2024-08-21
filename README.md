# Custom HTML Templates for RustDesk Infinite Remote Web GUI

This repository contains custom HTML templates designed for the Infinite Remote Web GUI of RustDesk. These templates enhance the user interface by applying a consistent dark theme and adding animations for a more dynamic user experience.

![image](https://github.com/user-attachments/assets/093e0f6e-b03a-46b6-b752-b9d2db2666fb)
![image](https://github.com/user-attachments/assets/0c75c696-0444-4abe-8ea5-ec9765b5f230)
![image](https://github.com/user-attachments/assets/c0c52f97-4bc6-4e37-95b8-e9722058c978)
![image](https://github.com/user-attachments/assets/e13fd19e-76e7-433d-852f-91681c95423c)

## File Structure

The files in this repository should be placed in the following directory on your RustDesk API server:

```
/opt/rustdesk-api-server/api/templates/
```

### Included Files

- `base.html`: The base template that all other templates extend. It includes global styles and scripts.
- `login.html`: Template for the login page.
- `msg.html`: Template for displaying informational messages.
- `share.html`: Template for sharing machines with other users.
- `show_conn_log.html`: Template for displaying connection logs.
- `show_file_log.html`: Template for displaying file transfer logs.
- `show_work.html`: Template for displaying work statistics.
- `installers.html`: Template for providing download links to various installers.

## Installation

1. **Navigate to the Templates Directory**:
   Ensure you are in the correct directory on your RustDesk API server:

   ```sh
   cd /opt/rustdesk-api-server/api/templates/
   ```

2. **Replace Existing Templates**:
   Copy the custom HTML files from this repository to the `templates` directory:

   ```sh
   cp /path/to/your/custom/templates/* /opt/rustdesk-api-server/api/templates/
   ```

3. **Modify Installer Links**:
   The `installers.html` file contains links to various installers for Windows, Linux, and Mac. You need to replace the placeholder URLs with your actual domain or server paths.

   Open the `installers.html` file and replace instances of `https://your-domain-here.com` with your actual domain:

   ```html
   <a href="/static/configs/your-windows-exe-here.exe">Download</a>
   <!-- Change to -->
   <a href="https://your-domain.com/static/configs/your-windows-exe-here.exe">Download</a>
   ```

   Ensure that all the links point to the correct paths where your installer files are hosted.

## Customization

- **CSS and JS Customization**: All CSS and JavaScript files are linked in `base.html`. If you need to customize styles or scripts, make your changes in the `base.html` file.
- **Dynamic Content**: The templates use Django's templating language for dynamic content rendering. Ensure any modifications to the dynamic content blocks are done carefully to maintain functionality.

## Contribution

If you'd like to contribute to improving these templates or adding new features, please fork the repository and submit a pull request. I appreciate all contributions!
