# The Quant's Bible
This is the second of two repositories dedicated to the _Quant's Bible_, a public and open-access knowledgebase containing rigorous mathematical foundations for independent quant researchers. This specific repository provides the web container that the viewer can see and interact with. 

### Technical Specifications
##### Primary Editor
The primary editor used to alter the notes is _Obsidian_, which is a free software used for note-taking. Obsidian uses Markdown documents that enable simple note formatting and organization. 

##### Vercel
The notes are hosted with the use of _Vercel_. 

##### Digital Garden
In addition to Obsidian being the primary editor to organize the notes, the synchronization between the editor's local repository and Vercel's online servers is done with the _Digital Garden_ plugin. This is a free plugin that allows notes hosting without having to manually code all visual elements. Below are the specific extensions that were added to Digital Garden to extend its functionality: 

**1. Extensions by Ole Eskild Steenses**
- _Copy Code Button_ adds a copy button to every code block, enabling readers to easily copy the code they are reading rather than having to manually scroll through the code block.
- _Giscus Comments_ allows readers with Github accounts to comment on the page they are reading. This is useful for suggestions or spotting errors.
- _Image Lightbox_ allows readers to click on any image and view it full-sized.
- _Sidebar Controls_ allows readers to collapse the left sidebar, which provides a file tree that allows them to switch between various notes in the repository, and the right sidebar, which allows them to conveniently fast-forward or backward between various parts of the specific note they are reading.

**2. Extensions by Kolten Bendickson**
- _Clean Print_ adds a small print icon on the bottom-left that gives readers a:
	- 	 Live layout preview to see how the page will look like before printing.
	- 	 Study-sheet presets that allow for the alteration of size notes to account for reader's choice of paper used.
	- 	 Option theme styling for readers who want it to be printed with the original look and colors (default print presets are white).
	- 	 Styling and page numbering if the printed page is long.
-  _Reading Progress & Reusume_ provides a minimalist reading progress bar on the top of the UI, along with optional personote resume prompts.
- _Resizable Panes & Reading Width_ gives accessible side-pane resizing, reversible collapse, and a live centered reading-width control.
