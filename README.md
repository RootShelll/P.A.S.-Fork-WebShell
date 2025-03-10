# P.A.S.-Fork: A Powerful Webshell for Stealth Penetration Testing

P.A.S.-Fork is a modified version of the popular P.A.S. webshell tool, designed to bypass web application firewalls (WAFs) and intrusion detection systems (IDS). Learn how to use P.A.S.-Fork for stealth penetration testing.

## Password
Use the following password to access certain features:

<div style="display:flex;align-items:center;gap:10px;margin-top:10px">
    <input type="text" value="R00t" id="password" readonly onclick="this.select(); document.execCommand('copy');" style="padding:10px;border:2px solid #4CAF50;border-radius:5px;font-size:16px;width:200px;background-color:#f9f9f9;color:#333;transition:background-color 0.3s,border-color .3s">
    <button onclick="document.getElementById('password').select(); document.execCommand('copy');" style="padding:10px 15px;background-color:#4CAF50;color:#fff;border:none;border-radius:5px;cursor:pointer;transition:background-color .3s">Copy</button>
</div>

## What is P.A.S.-Fork?

**P.A.S.-Fork** is a tool used for penetration testing, designed to remain undetected by WAFs and IDSs. It helps security professionals assess vulnerabilities without triggering defensive measures that could disrupt testing.

This version improves on the original P.A.S. webshell by adding enhanced stealth and obfuscation techniques, making it a useful tool for advanced security assessments.

<div style="background-color: #222; padding: 10px; border-radius: 5px;">
    ⚠️ <strong>Important:</strong> This tool is for educational and testing purposes only. Use it responsibly and only on systems for which you have authorized access.
</div>

## Features of P.A.S.-Fork

- **Stealth Mode**: Operates without triggering WAF/IDS alarms.
- **File Manager**: Upload, delete, and manage files, with bulk operations and search functionalities.
- **SQL Client**: Supports multiple database systems including MySQL, MSSQL, and PostgreSQL.
- **Encryption**: Encrypts the source code for secure transfer and execution.
- **Asynchronous Requests**: Uses AJAX-like requests to avoid page reloads and retain data.

## How to Use P.A.S.-Fork

To get started with P.A.S.-Fork, follow these steps:

1. Download the webshell files from the GitHub repository.
2. Upload the files to your target system in a controlled environment.
3. Ensure that the target system's PHP version is >= 4.1.0 for compatibility.
4. Access the webshell interface via your browser and begin using its features like file management and SQL interaction.

> Always make sure to remove all HttpOnly cookies for the domain before starting the tool.

## Educational Use Only

<div style="background-color: #222; padding: 10px; border-radius: 5px;">
    📘 <strong>Note:</strong> This tool should only be used in authorized environments for educational or testing purposes. Unauthorized access to systems is illegal.
</div>
