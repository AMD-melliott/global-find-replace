# Global Find & Replace

## Exercise Goal

Learn to use VS Code's powerful search and replace features to make consistent changes across an entire project. This is an essential skill for maintaining large codebases and documentation!

**What you'll learn:**

- Using VS Code's global search across all files
- Previewing changes before applying them
- Performing project-wide find and replace operations
- Managing multi-file commits
- Working with batch changes safely and efficiently

---

## Scenario

**Breaking news!** Your company has rebranded. The product formerly known as "Project Alpha" is now called "**Omega App**".

Marketing sent you 5 documentation files that need updating ASAP. Manually editing each file would be tedious and error-prone. Instead, you'll use VS Code's global find & replace to update all mentions at once - professionally and confidently!

---

## Step-by-Step Instructions

### Step 1: Clone the Repository

Using your preferred method:

**Command Line:**

```bash
git clone https://github.com/AMD-melliott/global-find-replace.git
cd global-find-replace
```

**Or VS Code:**

1. `Ctrl+Shift+P` / `Cmd+Shift+P` → `Git: Clone`
2. Enter: `https://github.com/AMD-melliott/global-find-replace.git`
3. Open the cloned folder

---

### Step 2: Create a Branch

Let's create a branch for this refactoring work.

**Quick method:**

1. Click the branch name in the bottom-left (`main`)
2. Select **Create new branch**
3. Name it: `rebrand-to-omega-app`

---

### Step 3: Explore the Documentation Files

Before we make changes, let's see what we're working with.

**In the Explorer sidebar** (or press `Ctrl+Shift+E` / `Cmd+Shift+E`), you should see:

- `README.md`
- `overview.md`
- `getting-started.md`
- `features.md`
- `faq.md`
- `troubleshooting.md`

**Quick scan:** Open a few files and notice how many times "Project Alpha" appears. Imagine updating these manually across dozens of files - that's why search & replace is so powerful!

---

### Step 4: Open the Search Sidebar

Now let's access VS Code's global search feature.

**Method 1: Sidebar icon**

- Click the **magnifying glass icon** (🔍) in the left sidebar

**Method 2: Keyboard shortcut**

- Press `Ctrl+Shift+F` (Windows/Linux) or `Cmd+Shift+F` (Mac)

**Method 3: Command Palette**

- `Ctrl+Shift+P` / `Cmd+Shift+P` → `View: Show Search`

![vscode-search-sidebar](./screenshots/vscode-search-sidebar.png)

**What you're seeing:** The Search sidebar has two main text boxes:

- **Top box:** What to search for
- **Bottom box:** What to replace it with (click the arrow to expand)

**Learn more:** [VS Code Docs: Search across files](https://code.visualstudio.com/docs/editor/codebasics#_search-across-files)

---

### Step 5: Search for "Project Alpha"

Let's find all instances of the old product name.

1. In the **search box** (top field), type:
   ```
   Project Alpha
   ```

2. Press **Enter** or click the refresh icon

![vscode-search-results](./screenshots/vscode-search-results.png)

**What happened?** VS Code searched through ALL files in your project and found every match!

**You should see:**

- A list of files that contain "Project Alpha"
- The number of matches in each file
- Preview of each matching line
- Total count at the top (should be around 20+ matches)

**[SCREENSHOT PLACEHOLDER: Search results showing multiple files with match counts and previews]**

---

### Step 6: Review the Search Results

Before replacing anything, let's understand what we found.

**Click through the results:**

- Click on any match to open that file at that specific line
- The matching text is highlighted in yellow

**Notice:**

- `overview.md` - Multiple mentions in the overview
- `getting-started.md` - Installation and setup instructions
- `features.md` - Feature descriptions
- `faq.md` - Frequently asked questions
- `troubleshooting.md` - Help documentation

**This is important!** Always review search results before replacing to ensure you're changing the right things.

---

### Step 7: Expand the Replace Field

Now let's set up our replacement.

1. Click the **▶ arrow** to the left of the search box to reveal the replace field

**Or simply click in the second text box that appears**

![vscode-replace-field](./screenshots/vscode-replace-field.png)

**You should now see:**
- Search field (top): `Project Alpha`
- Replace field (bottom): empty and ready for input

---

### Step 8: Enter the Replacement Text

In the **replace field** (bottom box), type:
```
Omega App
```

**Important:** Match the capitalization! "Omega App" not "omega app" or "OMEGA APP"

![vscode-replace-entered](./screenshots/vscode-replace-entered.png)

**Don't click anything yet!** We want to preview changes first.

---

### Step 9: Preview Individual Replacements

VS Code gives you granular control over replacements. Let's preview before mass-replacing.

**For each search result, you'll see small icons:**

![vscode-replace-icons](./screenshots/vscode-replace-icons.png)

- **Replace icon** (➡️) - Replace this single instance
- **Dismiss icon** (✕) - Skip this instance

**Try it:**

1. Find a match in the results
2. Hover over it to see the replace preview
3. Notice how "Project Alpha" → "Omega App" is shown

**Don't replace yet - just observe!** This preview helps you catch any matches you might NOT want to replace.

**[SCREENSHOT PLACEHOLDER: Hover preview showing before/after text for a single replacement]**

---

### Step 10: Execute "Replace All"

Now that we've reviewed the results, let's replace all instances at once.

**Look for the "Replace All" button** at the right side of the replace field. It looks like: **⇄**

![vscode-replace-all](./screenshots/vscode-replace-all.png)

**Before clicking, take note:**

- How many files will be affected
- Total number of replacements
- Are you confident these are the right changes?

**When ready:**

1. Click the **"Replace All"** button (⇄)
2. VS Code may ask: **"Replace X occurrences across Y files?"**
3. Click **Replace** to confirm

**[SCREENSHOT PLACEHOLDER: Confirmation dialog asking to replace X occurrences across Y files]**

**What happened?** All instances of "Project Alpha" have been replaced with "Omega App" across all your documentation files!

**Learn more:** [VS Code Docs: Find and Replace](https://code.visualstudio.com/docs/editor/codebasics#_find-and-replace)

---

### Step 11: Verify the Changes

Let's make sure the replacements look correct.

**Method 1: Spot check files**

1. Open `overview.md`
2. Look for "Omega App" - it should appear where "Project Alpha" used to be
3. Open a few other files to verify

**Method 2: Search for the old name**

1. In the search box, search again for: `Project Alpha`
2. **You should get 0 results!**
3. Now search for: `Omega App`
4. **You should see all the places it now appears**

![vscode-verify-replacement](./screenshots/vscode-verify-replacement.png)

**Good practice:** Always verify that:

- All instances were replaced
- Nothing was missed
- Nothing incorrect was changed

---

### Step 12: Review Changes in Source Control

Now let's see what Git thinks about these changes.

1. Open **Source Control** (`Ctrl+Shift+G` / `Cmd+Shift+G`)

2. **You should see multiple modified files:**

   - overview.md
   - getting-started.md
   - features.md
   - faq.md
   - troubleshooting.md

![vscode-source-control-multi-file](./screenshots/vscode-source-control-multi-file.png)

**Notice:** The number next to "Changes" shows how many files were modified (should be 5 or 6)

**[SCREENSHOT PLACEHOLDER: Source Control panel showing 5-6 modified files listed under Changes]**

---

### Step 13: Review Individual File Changes

Before committing, let's review what changed in each file.

**Click on any file in the Source Control panel** (e.g., `overview.md`)

**The Diff View opens:**

- **Left side:** Original with "Project Alpha" (red)
- **Right side:** New with "Omega App" (green)

![vscode-diff-multi-change](./screenshots/vscode-diff-multi-change.png)

**Scroll through and verify:**

- All changes are replacements of "Project Alpha" → "Omega App"
- Nothing else was accidentally modified
- The context around each change looks correct

**Click through several files** to gain confidence in your changes.

**[SCREENSHOT PLACEHOLDER: Diff view showing multiple red/green changes across a file]**

---

### Step 14: Stage All Changes

Since all the changes are related (the rebrand), we'll stage them all together.

**In the Source Control panel:**

**Method 1: Stage all at once**

- Click the **+** icon next to "Changes"
- All modified files move to "Staged Changes"

**Method 2: Stage individually**

- Click the **+** icon next to each file
- Useful if you want to exclude some files

![vscode-stage-all](./screenshots/vscode-stage-all.png)

**What happened?** All your rebranding changes are now staged and ready to commit as a single, atomic change.

**[SCREENSHOT PLACEHOLDER: Source Control showing all files moved to Staged Changes section]**

---

### Step 15: Commit the Changes

Now let's create a commit with a clear message explaining this batch change.

**In the commit message box, type:**

```
Rebrand from Project Alpha to Omega App

- Updated all documentation files with new product name
- Replaced all instances across overview, guides, FAQ, and troubleshooting
- Consistent branding throughout documentation
```

![vscode-commit-message-multi-file](./screenshots/vscode-commit-message-multi-file.png)

**Click ✓ Commit**

**Why this commit message works:**

- Clear summary line
- Explains what changed
- Indicates scope (all documentation)
- Future developers will understand this was a deliberate rename

**[SCREENSHOT PLACEHOLDER: Commit message box with multi-line rebrand message]**

**Learn more:** [Conventional Commits](https://www.conventionalcommits.org/)

---

### Step 16: Verify the Commit

Let's confirm everything was committed correctly.

**Command Line:**
```bash
git log -1 --stat
```

**You should see:**

- Your commit message
- List of all files changed
- Number of insertions/deletions per file

![vscode-git-log-stat](./screenshots/vscode-git-log-stat.png)

**Or in VS Code:**

- Right-click any file in Explorer → **Open Timeline**
- See your commit in the file's history

**[SCREENSHOT PLACEHOLDER: Terminal showing git log with 5-6 files changed and statistics]**

---

### Step 17: Push and Create a Pull Request

Time to share your work!

1. **Push your branch:**

   - In Source Control, click **⋯** → **Push**
   - Or use the sync icon in the status bar

2. **Create a PR on GitHub:**

   - Navigate to `https://github.com/AMD-melliott/global-find-replace`
   - Click **Compare & pull request**
   - Title: `Rebrand from Project Alpha to Omega App`
   - Description:
     ```
     ## Changes
     This PR updates all documentation to reflect our new product name.

     - ✅ Replaced "Project Alpha" with "Omega App" across all docs
     - ✅ Updated 5 documentation files
     - ✅ Verified no instances of old name remain

     ## Files Changed
     - overview.md
     - getting-started.md
     - features.md
     - faq.md
     - troubleshooting.md
     ```
   - Click **Create pull request**

**Congratulations!** You've successfully performed a project-wide refactoring! 🎉

---

## Key Takeaways

✅ **Global search** finds patterns across entire projects instantly
✅ **Preview before replacing** prevents costly mistakes
✅ **Replace All** makes consistent changes efficiently
✅ **Batch commits** group related changes logically
✅ **Diff view** helps verify multi-file changes before committing

---

## Advanced Search Features

VS Code's search is even more powerful than what we used! Here are additional features:

### Case Sensitivity Toggle
![icon-case-sensitive](Aa) - Click to make search case-sensitive
- `Project Alpha` vs `project alpha` vs `PROJECT ALPHA`

### Match Whole Word
![icon-whole-word](ab|) - Only match complete words
- Finds "Project Alpha" but not "ProjectAlpha" or "Project_Alpha"

### Regular Expression Search
![icon-regex](.*) - Use regex patterns for complex searches
- Example: `Project\s+(Alpha|Beta)` finds "Project Alpha" or "Project Beta"

### Include/Exclude Files
- **files to include:** `*.md` (only Markdown files)
- **files to exclude:** `**/node_modules/**` (ignore dependencies)

![vscode-search-filters](./screenshots/vscode-search-filters.png)

**Learn more:** [VS Code Docs: Advanced search options](https://code.visualstudio.com/docs/editor/codebasics#_advanced-search-options)

---

## Bonus Challenges

### Challenge 1: Case-Sensitive Replacement

What if you needed to replace:
- "Project Alpha" → "Omega App"
- "PROJECT ALPHA" → "OMEGA APP"
- "project alpha" → "omega app"

**How would you do this?** (Hint: Multiple searches or regex)

### Challenge 2: Partial Replacement

Replace only "Alpha" → "Omega" but keep "Project":
- "Project Alpha" → "Project Omega"

**Try it!** Create a new branch and experiment.

### Challenge 3: Replace Across Specific Files

Use the "files to include" filter to replace only in Markdown files:
- Pattern: `*.md`
- Ignore other file types

### Challenge 4: Undo All Replacements

Practice safe experimentation:
1. Make a replacement
2. Use `Ctrl+Z` / `Cmd+Z` to undo
3. Or use Source Control → **Discard Changes**

---

## Common Use Cases for Global Find & Replace

**This technique is invaluable for:**

### Refactoring Code

- Rename variables: `oldName` → `newName`
- Update function names: `getData()` → `fetchData()`
- Change class names: `UserManager` → `UserService`

### Documentation Updates

- Product rebrands (like this exercise!)
- Fixing repeated typos
- Updating URLs: `http://` → `https://`

### Configuration Changes

- Update API endpoints across config files
- Change environment variables
- Update version numbers

### Consistency Fixes

- Standardize terminology
- Fix spacing inconsistencies
- Align naming conventions

---

## Troubleshooting

### "Replace All didn't work"

- Make sure the replace field is expanded
- Check that you entered replacement text
- Verify files aren't read-only

### "I replaced too much / wrong things"

- **Don't panic!**
- Press `Ctrl+Z` / `Cmd+Z` repeatedly to undo
- Or: Source Control → Right-click files → **Discard Changes**
- This is why we review before replacing!

### "Search isn't finding obvious matches"

- Check if case-sensitivity is enabled (Aa button)
- Check if "whole word" is enabled (ab| button)
- Look at include/exclude filters

### "Changes aren't showing in Source Control"

- Make sure you actually replaced (not just searched)
- Save the files (`Ctrl+S` / `Cmd+S` or enable auto-save)
- Refresh Source Control view

---

## Best Practices for Find & Replace

### ✅ DO:

- **Preview results** before replacing
- **Review changes** in diff view before committing
- **Use specific search terms** to avoid unintended matches
- **Test with "Replace" on one instance** first before "Replace All"
- **Create a branch** for large refactoring operations
- **Commit related changes together** with descriptive messages

### ❌ DON'T:

- Replace without reviewing results first
- Use overly broad search terms
- Skip checking the diff view
- Commit without verifying changes
- Ignore files you didn't expect to change
- Replace in auto-generated or dependency files without caution

---

## Real-World Application

**Professional developers use find & replace daily for:**

- **Codebase refactoring** - Renaming functions, variables, classes
- **API migrations** - Updating deprecated API calls
- **Brand consistency** - Ensuring consistent terminology
- **Bug fixes** - Correcting repeated errors
- **Localization** - Updating text strings
- **Configuration updates** - Changing environment-specific values

**Fun fact:** Large codebases like VS Code itself use find & replace thousands of times during development!

---

## Additional Resources

- [VS Code Find and Replace Documentation](https://code.visualstudio.com/docs/editor/codebasics#_find-and-replace)
- [Regular Expressions Tutorial](https://regexone.com/)
- [VS Code Search Tips and Tricks](https://code.visualstudio.com/docs/editor/codebasics#_advanced-search-options)
- [Search Editor](https://code.visualstudio.com/docs/editor/codebasics#_search-editor) - Save and reuse searches

---

## Quick Reference: Keyboard Shortcuts

| Action | Windows/Linux | Mac |
|--------|---------------|-----|
| Find in file | `Ctrl+F` | `Cmd+F` |
| Find in files | `Ctrl+Shift+F` | `Cmd+Shift+F` |
| Replace in file | `Ctrl+H` | `Cmd+Option+F` |
| Next match | `F3` | `Cmd+G` |
| Previous match | `Shift+F3` | `Cmd+Shift+G` |
| Toggle case sensitive | `Alt+C` | `Cmd+Alt+C` |
| Toggle regex | `Alt+R` | `Cmd+Alt+R` |
| Toggle whole word | `Alt+W` | `Cmd+Alt+W` |

---

**You've completed all the Git & GitHub training exercises!** 🎉

You now have practical experience with:
- ✅ Fork, clone, branch, commit, push workflow
- ✅ VS Code's Git integration and diff tools
- ✅ Merge conflict resolution
- ✅ Multi-window editing and Markdown documentation
- ✅ Project-wide search and replace

**These skills are the foundation of modern software development and documentation workflows!**
