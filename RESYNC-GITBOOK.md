# Re-sync this package with GitBook

Use this file only when replacing an earlier broken import.

## 1. Replace the repository content

Upload the contents of this ZIP to the root of the GitHub repository.

The repository root must contain:

```text
.gitbook.yaml
README.md
SUMMARY.md
getting-started/
concepts/
setup/
transactions/
smart-contracts/
rpc/
```

Commit the replacement to the branch connected to GitBook, normally `main`.

## 2. Confirm the source file

Open this file on GitHub:

```text
getting-started/quickstart.md
```

It must contain headings and paragraphs below `# Quickstart`.

## 3. Remove pending title-only changes

In GitBook, open **Change requests**. Discard or close any pending change request that contains the empty title-only pages.

## 4. Pull from GitHub

Open the Git Sync configuration and confirm:

```text
Branch: main
Project directory: ./
```

Then trigger a sync or reload the space after the GitHub commit is detected.

## 5. Do not edit README through GitBook

When Git Sync is active, manage `README.md`, `SUMMARY.md`, and page files in the repository to avoid conflicts.
