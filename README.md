# Installation

To install the extension, the repository or the `chrome` folder must be downloaded. Since the extension is not loaded from the stores of the browser providers, it must be installed in the developer mode of the browsers. For this, the individual steps for the different tested browsers are listed below.

### Chrome

1. Go to the Extensions page by entering `chrome://extensions` in a new tab.
   - Alternatively, click on the Extensions menu puzzle button and select **Manage Extensions** at the bottom of the menu.
   - Or, click the Chrome menu, hover over **More Tools**, then select **Extensions**.
2. Enable Developer Mode by clicking the toggle switch next to **Developer mode**.
3. Click the **Load unpacked** button and select the `chrome` directory.
4. (Optional): Click the Extensions menu puzzle button in the address bar and then click the **Pin** button next to the *Pattern Highlighter* to keep its icon permanently displayed.

### Edge

1. Go to the Extensions page by entering `edge://extensions` in a new tab.
   - Alternatively, click the **Settings and more (...)** button, select **Extensions** and click **Manage extensions** on the opened popup.
2. Enable Developer Mode by clicking the toggle switch next to **Developer mode**.
3. Click the **Load unpacked** button and select the `chrome` directory.
4. (Optional): Click the Extensions menu puzzle button in the address bar and then click the **Show in Toolbar** button (eye icon) next to the *Pattern Highlighter* to keep its icon permanently displayed.

### Safari

In order to install the extension in Safari, it must first be converted into the compatible format. This requires an Xcode installation. To convert the Pattern Highlighter to a Safari extension, follow these steps.

1. Open a terminal window and navigate to the path of the repository (one directory level above the `chrome` folder).
2. Execute the following command: `xcrun safari-web-extension-converter --macos-only --project-location safari chrome`. ([More information about the command.](https://developer.apple.com/documentation/safariservices/safari_web_extensions/converting_a_web_extension_for_safari#3586260))
3. The command should have created a new folder named `safari` containing the Xcode project for extension. Also, a Xcode window should have opened. In Xcode, click the Run button, or choose **Product** > **Run** to build and run your app.
4. Now the developer menu in Safari has to be activated and unsigned extensions have to be allowed. After that, the extension can be activated in the browser. The necessary steps are explained [here](https://developer.apple.com/documentation/safariservices/safari_web_extensions/running_your_safari_web_extension#3744467).

### Firefox

#### Building the Firefox version

To build the firefox version, the complete repository must be downloaded.

##### Windows

1. Execute the `create_firefox_from_chrome.bat` batch script in the root directory of the repository, by double-clicking the file.
   - Alternatively, open `cmd.exe`, navigate to the root directory of the repository and execute the batch script from the command line.
2. The `firefox` folder should now contain not only the `manifest.json` file but also all other files and folders from the `chrome` folder.

##### Mac

1. Open a new terminal window, navigate to the root directory of the repository and execute the `create_firefox_from_chrome.sh` shell script.
   - To do so, execute the following command: `sh create_firefox_from_chrome.sh`.
2. The `firefox` folder should now contain not only the `manifest.json` file but also all other files and folders from the `chrome` folder.

#### Installation

1. Go to the Firefox Debugging page by entering `about:debugging` in a new tab.
2. Click the **This Firefox** button on the left side, then click the **Load Temporary Add-on...** button and select the `manifest.json` file in the `firefox` directory.
3. Go to the Extensions page by entering `about:addons` in a new tab.
4. Click the **Extensions** button on the left side and then click on the *Pattern Highlighter*.
5. Open the **Permissions** tab and click the toggle switch to the right of `Access your data for all websites` to give the Pattern Highlighter permissions to scan for patterns on all websites.
6. (Optional): Click the Extensions menu puzzle button in the address bar, right-click on the *Pattern Highlighter* and then click **Pin to Toolbar** to keep its icon permanently displayed.

Since the extension can currently only be installed via the method for developers, in Firefox it only remains installed until the browser is restarted.

### Opera

1. Go to the Extensions page by entering `opera://extensions` in a new tab (or use the `<kbd>`Cmd `</kbd>`/`<kbd>`Ctrl `</kbd>` + `<kbd>`Shift `</kbd>` + `<kbd>`E `</kbd>` shortcut).
2. Enable Developer Mode by clicking the toggle switch next to **Developer mode**.
3. Click the **Load unpacked** button and select the `chrome` directory.
4. (Optional): Click the Extensions menu cube button in the address bar and then click the **Pin** button next to the *Pattern Highlighter* to keep its icon permanently displayed.

## Libraries Used

- [Lit 2.7.2](https://lit.dev/) ([BSD-3-Clause](chrome/scripts/lit/LICENSE))
