Network Analyzer Tool - User 
Manual 
Overview 
The Network Analyzer is a Python application that reads network log files (tcpdump 
format), automatically extracts statistics (top source/destination IPs, TCP flags, errors), 
detects security anomalies, and exports the results as interactive Excel spreadsheets or 
Markdown reports. 
System Requirements 
● Python 3.7+ 
● Operating System: Windows, macOS, or Linux 
● Required Python Libraries: 
o tkinter (usually included with Python) 
o matplotlib (optional, for graphs) 
o openpyxl (for Excel export) 
Installation 
Step 1: Install Python 
Download from python.org and ensure "Add Python to PATH" is checked during installation. 
Step 2: Install Dependencies 
Open a terminal/command prompt and run: 
pip install matplotlib openpyxl 
Step 3: Run the Application 
Navigate to the script folder and run: 
python Analyseur_réseau.py 
A window titled "
🛡
 SAE 1.05 - Analyseur Réseau avec Graphiques" should open. 
Using the Program 
Step-by-Step Guide 
1. Select a File 
● Click the "
📂
 Sélectionner un fichier" (Select File) button 
● Choose a network log file with one of these formats: 
o .txt (text files) 
o .log (log files) 
o .csv (CSV files) 
o .dump (tcpdump dumps) 
2. View Analysis Results 
Once a file is selected, the application automatically: 
● Parses the log file line-by-line 
● Extracts source IPs, destination IPs, TCP flags, and errors 
● Detects security alerts (DOS, SYN floods, unbalanced traffic) 
● Displays results in the main window with: 
o Text summary: Statistics and top IPs 
o Graphs (if matplotlib is installed): 
▪ Pie chart of top 5 source IPs 
▪ Pie chart of top 5 destination IPs 
▪ Bar chart of TCP flags 
▪ Pie chart of error types 
3. Export Results 
Option A: Export to Excel 
1. Click "
📊
 Export Excel (avec graphiques)" (Export Excel with graphs) 
2. Choose a save location and filename 
3. The generated .xlsx file contains: 
o Summary sheet: Key metrics (file name, analysis date, line count, IP 
counts, error count) 
o Sources sheet: Top 10 source IPs with pie chart 
o Destinations sheet: Top 10 destination IPs with pie chart 
o Flags TCP sheet: TCP flag distribution with bar chart 
o Error Types sheet (if errors detected): Error breakdown with pie chart 
o Error Details sheet: Line-by-line error listings 
o Alerts sheet (if alerts detected): Security anomalies detected 
Option B: Export to Markdown 
1. Click "
📝
 Export Markdown" (Export Markdown) 
2. Choose a save location and filename 
3. The generated .md file contains: 
o Analysis date and source file name 
o Global statistics 
o Top 10 source IPs with percentages 
o Top 10 destination IPs with percentages 
o Security alerts (if any) 
