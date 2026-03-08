# Cyber Intelligence Toolkit (www.nightvzn.xyz)

A **FastAPI-based web application** for performing **domain, IP, email, and DNS intelligence analysis**.  
This toolkit provides a simple web interface to quickly gather technical details, visualize IP/email locations, and perform DNS lookups.



<img width="2518" height="1424" alt="image" src="https://github.com/user-attachments/assets/8c96d9bc-8320-4291-b5a9-c54487c8d925" />

---

# 🚀 Features

## Domain Analysis
- Retrieve domain information
- Perform subdomain scanning
- View domain registration, hosting, and technical details

## IP Geolocation
- Lookup IP address locations
- Display interactive **world map** using Plotly
- Shows city, country, and coordinates

## Email Header Analysis
- Analyze email headers for routing information
- Build **geographical email route timelines**
- Interactive map visualizing email hops

## DNS Lookup
- Retrieve DNS records for domains
- Supports A, MX, CNAME, NS, TXT, and other record types

---

# 🏗 Project Structure

```
project/
│
├── main.py                  # FastAPI app and routes
├── tools/
│   ├── domain_info.py       # Domain scanning functions
│   ├── ip_locator.py        # IP geolocation functions
│   ├── email_analyzer.py    # Email header analysis
│   └── dns_lookup.py        # DNS record lookups
│
├── templates/
│   └── index.html
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
└── README.md
```

---

# ⚙️ Installation

## 1. Clone the Repository

```bash
git clone https://github.com/yourusername/cyber-intel-toolkit.git
cd cyber-intel-toolkit
```

---

## 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

### Mac / Linux
```bash
source venv/bin/activate
```

### Windows
```bash
venv\Scripts\activate
```

---

## 3. Install Dependencies

```bash
pip install fastapi uvicorn jinja2 plotly python-multipart requests
```

---

# ▶️ Running the Application

Start the development server with Uvicorn:

```bash
uvicorn main:app --reload
```

Open your browser:

```
http://127.0.0.1:8000
```

---

# 🌐 Application Routes

| Route | Method | Description |
|-------|--------|-------------|
| `/` | GET | Main page, displays input form |
| `/` | POST | Runs selected tool and displays results |

---

# 🛠 Available Tools

### 1️⃣ Domain Info (`tool=domain`)
- Input: domain name (e.g., `example.com`)
- Output: domain registration, hosting info, subdomains

### 2️⃣ IP Locator (`tool=ip`)
- Input: IP address (e.g., `8.8.8.8`)
- Output: City, country, coordinates
- Interactive **map visualization** with Plotly

### 3️⃣ Email Header Analyzer (`tool=email`)
- Input: raw email header
- Output: route of email through servers
- Interactive **geographical timeline map**

### 4️⃣ DNS Lookup (`tool=dns`)
- Input: domain name
- Output: DNS records (A, MX, NS, TXT, etc.)

---

# 📊 Map Visualization

- **Plotly** used for rendering maps
- Maps update dynamically based on IP or email header analysis
- Custom styling: dark theme with lime markers for clarity

---

# 🧠 Error Handling

- Invalid input returns a clean page with no results
- Maps render only if geolocation data exists
- Tools fail gracefully for unreachable domains/IPs or malformed email headers

---

# 🔒 Security Notes

- The app does **not store sensitive information** permanently
- Ensure email headers do not contain private data before analyzing
- Consider deploying behind HTTPS for secure usage

---

# 📈 Future Improvements

- Multi-IP or multi-domain scanning
- Integration with threat intelligence APIs
- User authentication for saved sessions
- Real-time update notifications
- Docker containerization and cloud deployment

---

# 🛠 Tech Stack

- **Python**
- **FastAPI**
- **Jinja2**
- **Plotly**
- **Uvicorn**
- **HTML/CSS/JS** for front-end

---

# 🧪 Example Workflow

1. User navigates to homepage `/`.
2. Select a tool from the dropdown (Domain, IP, Email, DNS).
3. Enter the target (domain name, IP, or email header).
4. Click **Submit**.
5. Tool output appears below the form.
6. If applicable, interactive map displays results (IP location or email route).

---

# 📜 License

MIT License

---

# 👨‍💻 Author

This application is a **cyber intelligence toolkit** for quick domain, IP, email, and DNS analysis.  
Contributions, improvements, and feature suggestions are welcome.
