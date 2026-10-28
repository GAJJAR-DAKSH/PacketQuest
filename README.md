# 📦 PacketQuest – Stop-and-Wait ARQ Simulation

### Interactive Networking Learning Lab | Computer Networks Project

PacketQuest is an interactive educational project that demonstrates the **Stop-and-Wait Automatic Repeat Request (ARQ)** protocol through a visual simulation based on an Amazon order delivery scenario.

It helps students understand reliable data transmission, acknowledgments (ACKs), timeouts, packet loss, retransmissions, and duplicate packet detection.

## 🚀 Features

- 📡 Interactive sender-to-receiver packet transmission
- 📬 ACK (acknowledgment) transmission visualization
- ⚠️ Packet loss and acknowledgment loss simulation
- ⏱️ Timeout and automatic retransmission
- 🔢 1-bit sequence number tracking (0 and 1)
- 🔁 Duplicate packet detection
- 📊 Live transmission logs and delivery statistics
- 🌙 Dark and light mode interface
- 📱 Responsive user interface
- 🐍 Python implementation of the ARQ protocol
- 🌐 Flask backend with REST API endpoints
- 🧪 Automated unit tests

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Web page structure |
| CSS3 | Styling and animations |
| JavaScript | Interactive simulation |
| Tailwind CSS | Responsive UI styling |
| Python | ARQ protocol implementation |
| Flask | Backend and API |
| unittest | Automated testing |

## 🧠 How Stop-and-Wait ARQ Works

1. **Send:** The sender transmits a data frame with a sequence number.
2. **Wait:** The sender waits for an acknowledgment from the receiver.
3. **Receive:** The receiver checks the incoming frame.
4. **Acknowledge:** The receiver sends an ACK if the frame is received.
5. **Timeout:** If the frame or ACK is lost, the sender retransmits the frame.
6. **Duplicate Detection:** The receiver identifies duplicate frames using sequence numbers.
7. **Success:** Once the ACK arrives, the sender proceeds to the next frame and toggles its sequence number.

### 🛒 Amazon Order Analogy

| Networking Concept | Amazon Order Example |
|---|---|
| Sender | Customer |
| Receiver | Amazon server |
| Data frame | Order request |
| ACK | Order confirmation |
| Noisy channel | Unreliable internet connection |
| Timeout | Waiting too long for confirmation |
| Retransmission | Placing the same order request again |
| Duplicate detection | Recognizing a repeated request |

## 📁 Project Structure

```text
PacketQuest/
├── app.py
├── arq_simulation.py
├── packet_quest_arq.html
├── AmazonOrder.html
├── StopAndWait.html
├── requirements.txt
├── test_app.py
├── test_arq_simulation.py
├── README.md
├── .gitignore
└── PacketQuest_Report.pdf
```

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.9 or newer
- pip package manager
- A modern web browser
- Git (optional, for cloning the repository)

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/PacketQuest.git
cd PacketQuest
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Run the Application

```bash
python app.py
```

Open the following URL in your browser:

**http://127.0.0.1:5000**

## 🔌 API Endpoints

### Health Check

```http
GET /api/health
```

Checks whether the Flask application is running.

Example response:

```json
{
  "status": "ok",
  "service": "packetquest"
}
```

### Run an ARQ Simulation

```http
POST /api/simulate
Content-Type: application/json
```

Example request:

```json
{
  "order_number": 1,
  "sequence_number": 0,
  "loss_probability": 0.3,
  "max_attempts": 100,
  "seed": 42
}
```

The endpoint returns the delivery result, number of attempts, duplicate count, and transmission event history.

## 🧪 Running Tests

Run all automated tests:

```bash
python -m unittest discover -v
```

Run the ARQ simulation tests:

```bash
python -m unittest -v test_arq_simulation.py
```

Run the Flask application tests:

```bash
python -m unittest -v test_app.py
```

## 🎯 Learning Objectives

- Understand the Stop-and-Wait ARQ protocol.
- Learn the importance of acknowledgments and timeouts.
- Understand retransmission in unreliable networks.
- Identify duplicate frames using sequence numbers.
- Explore the effect of packet loss on reliable communication.
- Understand the trade-off between reliability and throughput.

## 📄 Project Report

The repository includes `PacketQuest_Report.pdf`, which documents the project objectives, protocol workflow, transmission scenarios, system design, and implementation.

## 🔮 Future Improvements

- Add Selective Repeat and Go-Back-N ARQ simulations.
- Introduce adjustable network delay and timeout settings.
- Add additional network performance metrics.
- Improve visualization of packet transmission events.
- Deploy the Flask application online.

## 👨‍💻 Author

**Daksh Gajjar**

B.Tech Computer Science and Engineering

Nirma University

## 📜 License

This project is intended for educational and academic use.
