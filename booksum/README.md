# Usage:
This subdirectory contains two directories.
- `links` contains, for each summary website, a TSV with the book title, and the associated URL to the archive.org webpage.
- `alignments` contains JSONL files, where each line is a JSON with book, chapter, and source information. For example:
```json
{"gutenberg_id": "27681",
"is_aggregate": true,
"source": "cliffnotes",
"chapter_id": "The Last of the Mohicans.chapters 7-8",
"chapter_path": "all_chapterized_books/27681-chapters/chapters_7_to_8.txt",
"summary_url": "https://web.archive.org/web/20201101053205/https://www.cliffsnotes.com/literature/l/the-last-of-the-mohicans/summary-and-analysis/chapters-78"}
```

## Chapterized Project Gutenberg Data
The chapterized book text from Gutenberg, for the books used in this shared task, can be downloaded here:  
https://storage.cloud.google.com/creative-summ-booksum/all_chapterized_books.zip  
NOTE: this ZIP combines a subset of the BookSum dataset, and a subset of the NovelChapter dataset. We recommend shared task participants use this version.
