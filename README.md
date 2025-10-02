# Applying a Custom VS Code Theme (from JSON)

This guide walks you through importing a theme you’ve exported/downloaded as a JSON file directly into your **VS Code user settings**.

---

## Instructions

1. **Grab the `tokenColors` Section**
   - Open the downloaded JSON in a code editor.
   - Find the property called **`tokenColors`** and copy the full array.  
   - 💡 *Tip: In VS Code you can collapse the array before copying to make things easier.*

2. **Open VS Code Settings (JSON view)**
   - Open the command palette:
     - **Windows/Linux:** `Ctrl + Shift + P`
     - **macOS:** `Cmd + Shift + P`
   - Search for **“settings json”** and choose  
     **Preferences: Open User Settings (JSON)**.

3. **Insert Token Color Rules**
   - Add this block if it doesn’t already exist:
     ```json
     "editor.tokenColorCustomizations": {
       "textMateRules": []
     }
     ```
   - Replace the empty `textMateRules` with the array you copied from the theme file.

4. **Grab the `colors` Section**
   - Go back to your downloaded JSON.
   - Copy the entire **`colors`** object.

5. **Insert Workbench Colors**
   - In your `settings.json`, add:
     ```json
     "workbench.colorCustomizations": { ... }
     ```
   - Replace the `{ ... }` with the `colors` object you just copied.

6. **Save and Apply**
   - Save the settings file:
     - **Windows/Linux:** `Ctrl + S`
     - **macOS:** `Cmd + S`  
   - Your editor should immediately pick up the new look.

---

🎨 Done! Your custom theme is now active in VS Code.
