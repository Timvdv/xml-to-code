# xml-to-code

Used to parse LLM XML output to code changes

## Features

- **XML Parsing:** Easily input XML instructions and parse them into structured code modifications.
- **Webview Interface:** Intuitive UI within VS Code for managing and applying code changes.
- **Diff Viewer:** Preview differences before applying changes to ensure accuracy.

---

## Installation

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/Timvdv/xml-to-code
   ```

2. **Navigate to the Extension Directory:**

   ```bash
   cd xml-to-code
   ```

3. **Install Dependencies:**

   ```bash
   npm install
   ```

4. **Open in VS Code:**

   ```bash
   code .
   ```

5. **Launch the Extension:**
   Press `F5` to open a new VS Code window with the extension loaded.

---

## Usage

1. **Open XML to Code View:**

   - Click on the **XML to Code** icon in the activity bar.
   - Alternatively, use the command palette (`Ctrl+Shift+P` or `Cmd+Shift+P` on Mac) and execute `Open XML to Code View`.

2. **Input XML Instructions:**

   - Paste your XML-formatted instructions into the provided textarea.
   - Ensure the XML follows the required schema for accurate parsing.

3. **Prepare Changes:**

   - Click the **Prepare Changes** button to parse the XML and generate a list of pending code changes.

4. **Review Changes:**

   - Review the list of changes in the **Changes** section.
   - Click on individual changes to view diffs and ensure they meet your requirements.

5. **Apply Changes:**

   - Once satisfied, click the **Apply Changes** button to execute the modifications in your workspace.

---

## Example

```xml
<file path="src/components/MyComponent.js" action="rewrite">
  <change>
    <description>Add new state management logic to MyComponent</description>
    <content>
===
import React, { useState } from 'react';

const MyComponent = () => {
  const [state, setState] = useState(null);

  // New state management logic
  const updateState = (newState) => {
    setState(newState);
  };

  return (
    <div>
      {/* Component JSX */}
    </div>
  );
};

export default MyComponent;
===
    </content>
  </change>
</file>
```

---

## Testing

Run the test suite to ensure the extension functions as expected:

```bash
npm test
```

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

---

Made to use together with:

- [RepoPrompt](https://repoprompt.com)\
  Use the **XML Whole** prompt for best results.

Extension is made with ❤️ by Tim van de Vathorst\
[GitHub](https://github.com/Timvdv/xml-to-code) | [Donate](https://www.paypal.me/timvandevathorst)

