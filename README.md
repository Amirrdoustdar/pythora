# Pythora Chat Server & Client

A real-time chat platform built with Python sockets and MySQL. It supports secure authentication, private and group messaging, media transfers, and temporary messages with TTL.

---

## Features

- **Secure Authentication**: Passwords hashed with bcrypt.
- **Private & Group Chat**: Real-time messaging using Python `socket` and `threading`.
- **Media Support**: Transfer text, images, and audio via Base64 encoding.
- **Temporary Messages**: Send messages that expire after a specified TTL.
- **Robust Database Schema**: MySQL tables for `users`, `groups`, `group_members`, and `messages`.
- **Modular Design**: Separate modules for Server, Client, Database, and Auth logic.

---

## Getting Started

### Prerequisites

- Python 3.7+
- MySQL Server
- pip

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Amirrdoustdar/pythora-chat-server.git
   cd pythora-chat-server
   ```

2. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Setup the database**
   ```bash
   mysql -u root -p < chat_db_professional.sql
   ```

4. **Adjust configuration**
   - Open `database.py` and set your MySQL `user`, `password`, and `host` if needed.

---

## Usage

### Running the Server

```bash
python message_server.py
```
Server will start listening on `0.0.0.0:9090` by default.

### Running the Client

Open one or more terminals and run:

```bash
python client.py
```

1. **Sign Up** or **Login** when prompted.
2. Use the menu to send **Private** or **Group** messages.
3. Type `exit` to terminate.

---

## Directory Structure

```plaintext
pythora-chat-server/
├── client.py              # Client application
├── message_server.py      # Server application
├── database.py            # DB connection and CRUD operations
├── utils.py               # Utility functions (Base64, etc.)
├── signup.py              # Signup flow
├── login.py               # Login flow
├── requirements.txt       # Python dependencies
├── chat_db_professional.sql # SQL schema and tables
├── uploads/               # Directory for media files
└── README.md              # Project documentation
```

---

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
