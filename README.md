

# Penetration Testing Automation Tool

This is a Python-based GUI tool designed to automate basic penetration testing tasks using popular security tools like Nmap and Nikto. It provides a user-friendly interface to perform reconnaissance and vulnerability scanning, and then generate a summary report of the findings.

To use in Windows use windows_pentest_tool.py

To use in Linux use Linux_pentest_tool.py

## Features

Nmap Integration:Perform Nmap scans for network discovery and service version detection.

Nikto Integration: Conduct Nikto scans for web server vulnerability assessment.In Windows Nikto is working for only SSL(HTTPS) not for http . For http use Kali Linux.

Metasploit Simulation: Includes a simulated Metasploit exploitation attempt, highlighting where a real integration would occur (with ethical considerations).

Report Generation: Compile scan results into a basic penetration test report.

User-Friendly GUI: Built with Tkinter for an intuitive graphical interface.



## Getting Started

### Prerequisites

Before running this tool, you need to have the following installed on your system:

Python 3.x: Download from [python.org](https://www.python.org/downloads/).

Nmap: Download from [nmap.org](https://nmap.org/download.html). Ensure it's added to your system's PATH.

Straberry Perl : Download from (https://strawberryperl.com/) . Ensure it's added to your system's PATH.

Nikto: Download from [cirt.net/nikto2](https://cirt.net/nikto2/). You will likely need to install Perl to run Nikto. Ensure the `nikto.pl` script's directory (or the script itself) is correctly referenced in the `pentest_tool.py` file, or that `nikto.pl` is directly executable and in your PATH.
    Perl: Nikto is a Perl script, so you need Perl installed. On Windows, you might use Strawberry Perl or ActiveState Perl.

### Installation

1.  Clone the repository:
    bash
    git clone https://github.com/dhanesh686-m/Automated-penetration-testing-tool.git
    cd Automated-penetration-testing-tool

2.  No special Python packages are required beyond `tkinter`, which is usually included with Python.

### Running the Tool

1.  Open a terminal or command prompt.
2.  Navigate to the directory where you saved `pentest_tool.py`.
3.  Run the script:
    bash
    python pentest_tool.py
    

## Usage

1.  Enter Target: Input the target IP address or domain name in the "Target IP/Domain" field.
2.  Run Nmap: Click "1. Run Nmap (Recon)" to perform a basic Nmap scan. The output will appear in the "Scan/Report Output" area.
3.  Run Nikto: Click "2. Run Nikto (Scan)" to execute a Nikto web vulnerability scan. The output will be displayed.
    Important Note for Nikto: The script currently expects `nikto.pl` at a specific path (`C:\nikto-nikto-2.5.0\program\nikto.pl`) for Windows. You must adjust this path in the               `run_nikto` method within `pentest_tool.py` to match your Nikto installation directory if it's different, or ensure `nikto.pl` is globally accessible via your system's PATH.
4.  Run Metasploit (Simulated): Click "3. Run Metasploit (Exploit - Simulated)" to see a simulation of a Metasploit operation. This is a simulation only and does not perform actual           exploitation.**
5.  Generate Report: Click "4. Generate Report" to compile the results from performed scans into a structured report.

## Important Considerations

Ethical Hacking: This tool is for educational purposes and legitimate security testing only. Always obtain explicit permission before scanning or testing any system you do not own or are not authorized to test.
Tool Paths: Ensure Nmap and Nikto executables/scripts are correctly configured in your system's PATH or that their full paths are specified in the `pentest_tool.py` script. The Nikto path is particularly important as highlighted in the `run_nikto` section.
Real-world vs. Simulation: The Metasploit functionality is *simulated*. Integrating real Metasploit requires more complex setup, often involving its RPC API.

## Contributing

Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an issue or submit a pull request.

