# buffer

A buffer is **an area of Vim's memory used to hold text read from a file**. In addition, an empty buffer with no associated file can be created to allow the entry of text. The :e filename command can edit an existing file or a new file.
***
> A buffer is the in-memory text of a file.

Any time we open an existing file or create a new one using Vim, a buffer will be allocated as the in-memory representation of said file. Any changes we make will be tracked within the buffer. When we are ready to update the file, the buffer can be written to disk.

Vim allows us to work with a bunch of different buffers at once. When working on large projects, the list of buffers can quickly grow out of control. Being able to read, understand, navigate, and manage the list of buffers can be challenging. With the right tools at our fingertips, we should be able to get by
***
“Left unchecked, technical debt will ensure that the only work that gets done is unplanned work!” — Gene Kim
***
![[buff-win-tab.jpg]]
***
![[windows=tabs=buffers.jpg]]
#vim #buffer