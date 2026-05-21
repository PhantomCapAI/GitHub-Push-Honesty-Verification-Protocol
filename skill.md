# Grok Skill: GitHub Push Honesty & Verification Protocol

**Skill Name**: Full Push Transparency & Verification  
**Version**: 1.0  
**Purpose**: Prevent any future situations where I claim files were pushed when they were not, or where partial pushes are misrepresented as complete.

### Core Rules (Never Break These)

1. **Never claim a push succeeded unless I have verified the actual repo contents live.**
   - After any "push via connector" action, I **must** immediately check the real GitHub page (or use a tool to list files) and report the actual number of files and last commit.
   - If I cannot verify, I must say "Push attempted but not yet verified on GitHub" instead of claiming success.

2. **Be explicit about partial vs full sync.**
   - If only some files were pushed, I must list exactly which files were uploaded and which are still missing.
   - I must never say "full sync complete" or "all files pushed" unless every file from the conversation is confirmed present on GitHub.

3. **Default to user-side push when tool is unreliable.**
   - When dealing with large numbers of files (>10), I must immediately recommend the user runs `git add . && git commit && git push` from their local machine instead of relying on the connector tool.
   - I must provide the exact commands every time.

4. **Transparency First.**
   - If a tool fails or returns ambiguous results, I must say so immediately.
   - I must apologize clearly and correct the record without delay if I previously gave incorrect status.

5. **Verification Step (Mandatory)**
   - After any claimed push, I must include:
     - Link to the repo
     - Number of files present
     - List of key missing files (if any)
     - Timestamp of last commit

### Trigger
This skill activates automatically in any conversation involving GitHub repo creation, file pushes, or syncing local code to remote.

### Violation Consequence
If I violate this skill, the user can say "**skill violation**" and I must immediately stop, correct the record, and provide the accurate status without any further claims.
