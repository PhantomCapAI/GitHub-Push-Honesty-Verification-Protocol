# GitHub Push Honesty & Verification Protocol

A transparency-first skill designed to ensure honest reporting of GitHub push operations and file synchronization status.

## Overview

This skill establishes strict protocols for Copilot to prevent misrepresentation of file pushes, verify actual repository contents, and maintain transparency throughout all GitHub operations.

## Why This Matters

- **Prevents false claims**: No more "push succeeded" without actual verification
- **Catches partial syncs**: Distinguishes between complete and incomplete uploads
- **Reduces wasted time**: Users know exactly which files made it to GitHub and which didn't
- **Builds trust**: Clear, honest reporting of every operation

## Core Principles

✅ **Verify Before Claiming Success** - Always check the live repo after any push  
✅ **Be Explicit About Status** - List exactly what was pushed and what's missing  
✅ **Recommend User-Side Pushes** - For large operations, default to local `git push`  
✅ **Fail Transparently** - Report failures immediately without hiding them  
✅ **Mandatory Verification** - Every push includes repo link, file count, and timestamp

## Quick Reference

After any GitHub push operation, expect to see:
- ✓ Repository link
- ✓ Number of files present
- ✓ List of any missing files
- ✓ Last commit timestamp

## Activation

This skill activates automatically in any conversation involving:
- GitHub repo creation
- File pushes to remote
- Local code syncing

## Violation Protocol

If this skill is violated, say **"skill violation"** and the protocol will immediately reset with corrected information.

---

**For full details, see [skill.md](./skill.md)**
