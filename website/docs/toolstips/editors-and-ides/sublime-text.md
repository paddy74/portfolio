# Sublime Text

- **Website**: `https://www.sublimetext.com/`
- **Best for**: entry level developers, editing markdown.
- **Strengths**:
  - simple interface
  - cross-platform
  - many extensions, including one for integration with GitLab (`GitlabIntegrate`).
  - powerful visual git-client integrated (`sublime-merge`)

A powerful text editor, sublime text is an excellent choice for editing plain text documents, but scales up to full code-editing. Installing extensions is simple.

## Configuration

Put the following in the User `Preferences.sublime-settings`.

```json
{
  "font_size": 12,
  "rulers": [79, 88, 120],
  "spell_check": true,
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true,
  "ensure_newline_at_eof_on_save": true,
  "folder_exclude_patterns": ["public"]
}
```
