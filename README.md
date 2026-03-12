# Book_Tranlator
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
1. Place your dictionary at: `recursos/dicionario.txt`
2. Place input text at: `recursos/livro_entrada.txt`
3. Run the program and check output at: `saida/livro_traduzido.txt`

> If you use Maven/Gradle, add the commands here.  
> Otherwise, provide compilation commands for Windows and Linux/macOS.

## Notes
Unknown words are kept in brackets (e.g., `[palavra]`) so the output remains readable even with an incomplete dictionary.
