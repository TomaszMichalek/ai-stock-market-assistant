# Publishing checklist

1. Review all Markdown content and remove anything you do not want public.
2. Inspect both screenshots for private data and identifiable account information.
3. Confirm `workflow/workflow-structure.json` contains only node labels/types and connections.
4. **Do not upload the original n8n export.** It can contain credentials references, identifiers, code, prompts, and private values.
5. Create a **public** GitHub repository named `ai-stock-market-assistant` and select **no** auto-generated README or .gitignore.
6. On the empty repository page, choose **uploading an existing file**.
7. Upload the contents of this folder, retaining the `docs/`, `workflow/`, and `images/` paths (GitHub web drag-and-drop support varies; alternatively upload files by folder using Add file > Upload files).
8. Commit with message `Initial product portfolio documentation`.
9. Check the README diagram, links, and that no secrets or private account information are visible.
10. Copy the repository URL into the Miquido application.

If you prefer a single upload, use GitHub Desktop or the git command line to preserve folder structure reliably.
