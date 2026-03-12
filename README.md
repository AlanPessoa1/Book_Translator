# Book_Translator
# Concurrent Book Translator (Java)

A CLI application that translates a text file using multiple threads.  
The translation is performed using a shared dictionary protected by a **Semaphore**, while a live terminal monitor displays progress and performance statistics.

## Key Concepts Demonstrated
- Concurrency with `Runnable` tasks and multiple threads
- Shared resource synchronization with a **fair Semaphore**
- Thread-safe metrics using `AtomicInteger` / `AtomicLong`
- Real-time progress monitoring in the terminal
- File I/O (UTF-8) for input/output text processing

## Project Structure
- `modelo/` domain models (dictionary, text blocks, statistics)
- `tarefa/` translation task (per thread)
- `controle/` orchestration + progress monitor
- `util/` config + file utilities

## How to Run

### Requirements
- Java 17+ (or Java 11+ if your code supports it)

### Project layout (original academic structure)
This repository keeps the original course structure (no Maven/Gradle) to match the submitted version.

### Input files
- Dictionary: `recursos/dicionario.txt`
- Input text: `recursos/livro_entrada.txt`

### Compile
**Windows (PowerShell):**
```powershell
mkdir bin -ea 0
Get-ChildItem -Recurse -Filter *.java src | ForEach-Object { $_.FullName } | Set-Content sources.txt
javac -encoding UTF-8 -d bin @sources.txt

## Notes
Unknown words are kept in brackets (e.g., `[palavra]`) so the output remains readable even with an incomplete dictionary.
