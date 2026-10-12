<h1>🔐 dpapi-toolkit - Decrypt Windows Protected Data Easily</h1>

<p align="center">
  <a href="https://github.com/ali-montolalu/dpapi-toolkit"><img src="https://img.shields.io/badge/Download%20dpapi--toolkit-%234FC3F7?style=for-the-badge&logo=windows&logoColor=white" alt="Download Button" style="background-color:#4FC3F7; padding:12px 24px; border-radius:8px; font-size:18px; font-weight:bold;"></a>
</p>

<h2>📖 What is dpapi-toolkit?</h2>
dpapi-toolkit is a free, offline tool for Windows that helps you understand and unlock encrypted files created by Windows. When Windows protects passwords, browser data, or other sensitive information, it uses a system called DPAPI (Data Protection API). This toolkit looks at any DPAPI-protected file you give it, tells you exactly what format it is, identifies which special "master key" is needed to open it, and then decrypts it once you provide that key.

You do not need any programming skills. If you can drag and drop a file, you can use this tool. It works from a simple command line or through a friendly web interface that opens in your browser.

<h2>🎯 Why Use dpapi-toolkit?</h2>
- <strong>Identify instantly</strong> – Drop any DPAPI artifact and immediately see its format.
- <strong>Find the right key</strong> – The tool tells you exactly which master key is required.
- <strong>Decrypt offline</strong> – Everything runs on your own machine. No internet connection or cloud service needed.
- <strong>Two ways to work</strong> – Use the fast command-line interface or the easier web UI.
- <strong>Free and open source</strong> – The code is transparent and available for anyone to inspect.

<h2>💻 Who is this for?</h2>
This tool is perfect for:
- <strong>Forensic analysts</strong> who need to examine Windows systems.
- <strong>IT administrators</strong> recovering data for users.
- <strong>Security researchers</strong> studying Windows encryption.
- <strong>Curious users</strong> who want to understand what Windows protects on their own machine.

<h2>⬇️ Download and Install</h2>
Visit this link to download the application. The download page will show you the latest version and provide the file you need.

<a href="https://github.com/ali-montolalu/dpapi-toolkit" style="background-color:#81C784; color:#ffffff; padding:12px 24px; border-radius:8px; font-size:16px; font-weight:bold; text-decoration:none;">📥 Go to Download Page</a>

Once the download finishes, you will have a file on your computer. That file is the program itself. You can double-click it to run it, or keep it in a folder where you like to store your tools. There is no complicated installation wizard or setup process.

<h2>🚀 Getting Started – First Run</h2>
After you have the file downloaded, follow these simple steps:

1. <strong>Double-click the downloaded file</strong> to launch dpapi-toolkit.
2. A command window (black screen with text) will open. This is the command-line interface.
3. To use the web interface, open your browser and go to the address shown in the command window (usually <code>http://localhost:8080</code> or similar).
4. In the web interface, you will see a drag-and-drop area. Drag any DPAPI artifact file onto it.
5. The tool will immediately analyze the file and display:
   - The <strong>format</strong> of the file (for example, "Chrome Login Data" or "Credential File").
   - The <strong>master key GUID</strong> it needs (a long string of letters and numbers).
   - A status message telling you whether decryption is possible with the keys you have.

<h2>🖥️ Using the Command-Line Interface</h2>
If you prefer working with commands, dpapi-toolkit is just as easy.

Open a command prompt (press <code>Windows + R</code>, type <code>cmd</code>, and press Enter). Navigate to the folder where you saved the tool, then type:

<code>dpapi-toolkit.exe path\to\your\file.dat</code>

The tool will output the same information: format, master key GUID, and decryption status. To supply the master key, use the <code>--key</code> option:

<code>dpapi-toolkit.exe --key "your-master-key-GUID" path\to\your\file.dat</code>

If the key is correct, the decrypted data will be saved as a new file in the same folder.

<h2>🔑 Understanding Master Keys</h2>
Windows DPAPI uses "master keys" to encrypt and decrypt data. These keys are unique to each user and each machine. The toolkit identifies which specific master key is required for your file. You must obtain that key from the user profile (usually located in <code>C:\Users\[Username]\AppData\Roaming\Microsoft\Protect</code>). The toolkit can also help you locate and load these keys.

<h2>🛠️ Features in Detail</h2>
- <strong>Automatic format detection</strong> – Recognizes common DPAPI structures like Chrome, Edge, Firefox, Outlook, WiFi passwords, and more.
- <strong>Master key correlation</strong> – Matches the file to the correct master key from your system.
- <strong>Offline decryption</strong> – All processing is local. Nothing is uploaded.
- <strong>Web UI with drag-and-drop</strong> – A clean, modern interface for non-technical users.
- <strong>Command-line power</strong> – Scriptable and fast for advanced users.
- <strong>Cross-compatibility</strong> – Works with 32-bit and 64-bit Windows versions.

<h2>❓ Frequently Asked Questions</h2>

<strong>Q: Is this safe to use?</strong><br>
A: Yes. The tool runs entirely offline on your machine. It does not send any data anywhere. It is open source, meaning the code is publicly visible for anyone to review.

<strong>Q: Do I need to install anything else?</strong><br>
A: No. The downloaded file includes everything needed. There are no dependencies or additional downloads.

<strong>Q: What if the tool says "No matching key found"?</strong><br>
A: This means the master key required for your file is not present on the current machine. You need to obtain the correct master key from the original user profile.

<strong>Q: Can this decrypt any Windows password?</strong><br>
A: No. It only works with data protected by DPAPI. Not all Windows encryption uses DPAPI.

<strong>Q: Does it work on Windows 7, 8, 10, or 11?</strong><br>
A: Yes. The toolkit is compatible with all modern Windows versions.

<h2>📚 Example Workflow</h2>
Let us walk through a typical scenario:

1. You have a file called <code>Login Data</code> from a Chrome browser profile.
2. You drag it into the web UI.
3. The tool says: "Format: Chrome Login Data. Required Master Key: <code>{a1b2c3d4-...}</code>"
4. You locate that master key file in the user's <code>Protect</code> folder.
5. You load it into the toolkit (by dragging it in or using the command line).
6. The tool now decrypts the file and shows you the saved passwords in plain text.

This entire process takes less than a minute for someone familiar with the steps.

<h2>🧪 Testing and Verification</h2>
The toolkit has been tested against real-world DPAPI artifacts from multiple Windows versions. It successfully identifies and decrypts files such as:
- Chrome and Edge saved passwords
- Windows Credential Manager entries
- Outlook and mail client credentials
- Wi-Fi profile passwords
- App-specific encrypted settings

<h2>🤝 Getting Help and Support</h2>
If you run into any issues, the project has an active community. You can:
- Open an issue on the GitHub repository.
- Check the documentation folder in the repository.
- Look at existing issues to see if someone else had the same problem.

<h2>📜 License</h2>
This project is released under an open-source license. You are free to use, modify, and distribute it, as long as you follow the terms of the license. Refer to the LICENSE file in the repository for details.

<h2>✅ Final Checklist Before You Start</h2>
- [ ] Download the file from the provided link.
- [ ] Run the file (double-click it).
- [ ] Open the web UI in your browser (or use the command line).
- [ ] Drag your DPAPI file onto the interface.
- [ ] Read the format and master key information.
- [ ] Supply the master key and decrypt.

<h2>🔗 Quick Links</h2>
- <a href="https://github.com/ali-montolalu/dpapi-toolkit">Repository Home</a>
- <a href="https://github.com/ali-montolalu/dpapi-toolkit/releases">Releases and Downloads</a>
- <a href="https://github.com/ali-montolalu/dpapi-toolkit/issues">Issue Tracker</a>

<h2>💡 Final Thoughts</h2>
dpapi-toolkit removes the mystery from Windows encryption. Whether you are doing digital forensics, recovering lost data, or just exploring how your system works, this tool gives you a clear, simple path from encrypted file to readable data. It is fast, free, and designed for everyone – from complete beginners to seasoned professionals.

Try it today and see what your Windows system is really hiding.