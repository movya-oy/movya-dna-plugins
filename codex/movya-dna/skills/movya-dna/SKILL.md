---
name: movya-dna
description: Search and use Movya's shared company knowledge and reusable skills, or maintain that knowledge when the user requests it. Use for questions about Movya and work that needs Movya DNA. Requires an authorized Movya DNA account.
---

# Movya DNA

Use the connected Movya DNA tools for company knowledge. If the tools are unavailable or require authentication, ask the user to enable the plugin and complete sign-in in their client. Never ask for passwords or tokens. Installation alone does not establish a working connection.

## Working instructions

Movya DNA holds shared company knowledge and reusable skills. Before a task, use knowledge_list_skills to find relevant instructions, then knowledge_get_skill to read the selected skill. Before incorporating source documents or maintaining knowledge, read skill-knowledge-maintenance. Search and read existing pages before proposing or saving changes. Execute only work requested by the user and allowed by their permissions.

Canonical knowledge is English; translate queries and proposed edits while preserving meaning, names, uncertainty and provenance. Answer the user in their preferred language. Keep customer-specific content, credentials and unnecessary personal data outside DNA. Source documents stay local unless the user separately requests storage.

Use knowledge_search for discovery and knowledge_get_page for complete evidence; search scores do not establish relevance. Follow a skill's page references with knowledge_get_page and find its permitted attachments with knowledge_list_files(page=skill page ID). Read assets with knowledge_get_file; retain stable file IDs, not temporary download URLs.

Read the current page before updates, preserve unrelated content and use expected_version. Reuse the same operation_id and identical arguments after an unknown write outcome. On conflict, reread and reconcile; do not overwrite concurrent edits. Preserve uncertainty and plans as such, report unresolved contradictions, and never claim an unverified write succeeded. Respect preview-only requests. Discovering or reading a skill does not install it or authorize autonomous work.

## Verify the connection

For a read-only check, ask DNA to list the skills available to the signed-in account. An empty list can be a successful result. A missing tool, authorization error or failed request is not a successful connection.

Shared business skills and their references are retrieved from DNA under the user's permissions. This plugin contains general usage instructions only; do not export retrieved knowledge to files or publish it unless the user requests that work.
