*This project has been created as part of the 42 curriculum by aalrofat.*

# 📄 get_next_line

## 📝 Description
The **get_next_line** project is a C function designed to read and return a single line at a time from a given file descriptor (`fd`), whether reading from a regular file. It handles arbitrary `BUFFER_SIZE` values efficiently while preserving unread data across function calls.

### 💡 What did I learn from the project
Working on **get_next_line** deepened my understanding of `static` variables and how state persists between calls in C. I practiced careful dynamic memory allocation, string chunking/joining, handling `EOF` and newline (`\n`) edge cases, and preventing memory leaks when errors or end-of-file conditions occur.

## ⚙️ Instructions
1. Include `get_next_line.h` in your C source file.
2. Compile your code with the project source files and specify a `BUFFER_SIZE` macro, for example:
   - `cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 main.c get_next_line.c get_next_line_utils.c -o gnl_test`
3. Call `get_next_line(fd)` repeatedly inside a loop until it returns `NULL`.

## 🛠️ Key Components
- **`get_next_line`**: Reads from the file descriptor into a buffer until a newline is found or `EOF` is reached, returning one line per call.
- **Helper Utilities (`get_next_line_utils`)**: Handles string length calculation, joining buffers, searching for characters/newlines, and substring/remainder extraction.
- **Configurable `BUFFER_SIZE`**: Supports compiling with different buffer sizes (`-D BUFFER_SIZE=...`) without breaking behavior.

## 🔗 Resources
- [Linux man pages: read(2)](https://man7.org/linux/man-pages/man2/read.html)
- [Linux man pages: open(2)](https://man7.org/linux/man-pages/man2/open.html)
- [42 Norminette](https://github.com/42School/norminette)

### 🤖 AI Usage
- **Explaining Concepts**: Helped clarify static variable lifetime, file descriptor reading flow, and edge cases around newlines and `EOF`.
- **Code Organization**: Helped structure helper functions cleanly and maintain compliance with the Norminette.
- **Documentation**: Helped draft and refine the English in this README file.
