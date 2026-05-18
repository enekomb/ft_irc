# ft_irc — IRC Server in C++

> 42 Urduliz — Common Core project

A fully functional **IRC server** built from scratch in C++, following the [RFC 1459](https://datatracker.ietf.org/doc/html/rfc1459) protocol standard. Compatible with real IRC clients (irssi, HexChat, WeeChat).

---

## Features

- TCP/IP server using **non-blocking sockets** and `poll()` for concurrent connections
- Full **IRC protocol** support: `NICK`, `USER`, `JOIN`, `PART`, `PRIVMSG`, `KICK`, `INVITE`, `TOPIC`, `MODE`
- **Channel management**: multiple channels, operator and regular user roles
- **Server password** authentication
- Graceful disconnection and robust error handling

## Build & Run

```bash
make
./ircserv <port> <password>
```

Connect with any IRC client:
```
/connect localhost <port> <password>
```

## Project Structure

```
ft_irc/
├── Server/          # Core server: socket setup, client accept loop
├── Client/          # Client state, message buffering
├── Channel/         # Channel logic, user roles
├── Commands/        # One file per IRC command handler
├── Poll/            # poll() event loop manager
├── main.cpp
├── colors.hpp       # Terminal color codes
└── Makefile
```

## Technical Highlights

| | |
|---|---|
| I/O model | Non-blocking sockets + `poll()` |
| Protocol | RFC 1459 compliant parsing |
| Architecture | Single-threaded event loop |
| Memory | Verified leak-free with Valgrind |
| Standard | C++98 |

## Skills

`C++` `TCP Sockets` `Network Programming` `Concurrency` `RFC Protocol` `Linux` `Makefile`
