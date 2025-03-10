# P.A.S.-Fork: A Powerful Webshell for Stealth Penetration Testing

P.A.S.-Fork is a modified version of the popular P.A.S. webshell tool, designed to bypass web application firewalls (WAFs) and intrusion detection systems (IDS). Learn how to use P.A.S.-Fork for stealth penetration testing.

![P.A.S.-Fork Shell Backdoor](https://raw.githubusercontent.com/RootShelll/P.A.S.-Fork-WebShell/refs/heads/main/P.A.S.-Fork.png "P.A.S.-Fork Shell Backdoor")

## Password
Use the following password to access certain features:

```bash
R00t
```


A modified version of the well-known webshell - P.A.S. by Profexer ([0](https://krebsonsecurity.com/2017/08/blowing-the-whistle-on-bad-attribution/), [1](https://github.com/winstrool/pas-4.1.1b_source_code), [2](https://github.com/wordfence/grizzly/tree/master/pas-4.1.1b)). Tries to solve the problem of detecting some requests and responses by various **Web Application Firewalls** and **Intrusion Detection Systems**. In most cases, such detections entail retaliatory measures from the attacked side, which is not always permissible during penetration tests and in red teaming.

```diff
- This tool is for educational and testing purposes only and is not
- intended to be put into practise unless you have authorized access to the system
+ Before using, it's better to remove all HttpOnly cookies for the domain
```

<br/>

<details>
  <summary>Features of the original <b>P.A.S.</b></summary>
  
## **General**

* Works on PHP >= 4.1.0
* Doesn't use PHP sessions or store any data on a server
* Uses asynchronous requests like a AJAX
* Can use POST or GET request method
* Can obfuscate requests
* Can work in custom environment (aka SUID mode)
* Supports 22 different charsets
* Encrypts the source code with your key (password) at download
* Resulting file doesn't contain encryption key (password) in any form
* Has stealth mode
* Working with different tasks without reload page and losing data
* Can be switched from fixed to flexible view
* Keyboard-only compatibility
* Has message log
* Shows server time

## **File Manager**

* Can upload several files at once
* Can create file, directory, symbolic and hard link
* Can change files properties (path, modified date, permission, owner, group)
* Can download files
* Can delete files
* Has files buffer:
  * mark, unmark, show marked files;
  * copy, move files from buffer to the current dir;
  * download files from buffer;
  * clear buffer;
* Can search files:
  * in several paths;
  * with limited depth;
  * by name with wildcard and case-sensitive options;
  * by type (file, directory);
  * by mode (readable, writable, full access);
  * with SUID attribute;
  * by owner IDs with definition of intervals;
  * by group IDs with definition of intervals;
  * by created date with definition of intervals;
  * by modified date with definition of intervals;
  * by size with definition of intervals;
  * by specified text with regex and case-sensitive options;
* Can save file with specified end of line
* Fast change properties, download and delete specified file
* Has breadcrumbs
* Click on extension cell to copy file name
* Press **ESC** to close current dialog
* Press **Alt+T** to switch between opened dialogs

## **SQL Client**

* DB support:
  * MySQL (mysql, mysqli, PDO)
  * MSSQL (mssql, sqlsrv, PDO, PDO SQLSRV, PDO DBLIB, PDO ODBC)
  * PgSQL (pg, PDO)
* Tree view of database schema
* Shows column data types
* Can show only selected columns data
* Can show tables row count
* Can reload single base/scheme/table schema
* Can dump multiple tables/schemes/bases
* Can dump only selected schemes/tables/columns
* Can dump to SQL or CSV format
* Has pagination for some database types

## **PHP Console**

* Isolates the results HTML code from the main page
* Can be switched from vertical to horizontal composition
* Press **Ctrl+Enter** to evaluate code

## **Terminal**

* Can execute commands via specified command processor
* Can execute commands via specified function
* Type **?** to show help
* Has command history:
  * type **history [N]** to show command history, where optional parameter N is number of last commands;
  * press **Up** & **Down** keys to navigate from command history;
  * type **![N]** to execute command, where N is:
     * ! to execute the last command;
     * N>0 to execute command #N from the command histroy;
     * N<0 to execute command #N from the end of the previous command;
* Can create system report (type **report ?** to more info)
* Can run Socks5 server:
  * throught Perl (type **socks5.perl** to more info);
  * throught Python (type **socks5.python** to more info);
* Can bind port:
  * throught Perl (type **bindport.perl** to more info);
  * throught Python (type **bindport.python** to more info);

* Can back connect:
  * throught Perl (type **backconnect.perl** to more info);
  * throught Python (type **backconnect.python** to more info);

* Type **cls** or **clear** or press **CTRL+L** to clear output
</details>
<details>
  <summary><b>P.A.S. Fork</b> changes</summary>
  
  <br/>
  
* Work via GET requests (parameters in cookies)
* Automatic switching to POST (with cancellation)
* Obfuscation of query keys and values
* Obfuscation of uploaded files
* Obfuscation of response
* Authorization by password
* Authorization by HTTP header (user-agent by default)
* MySQL dump fix in PDO mode
* Renamed "PHP 4-style constructors"
* Removed **pcntl_exec**
* New initialization logic (ini_*)
* **opcache_invalidate** after saving the file
* Dark color mode
* Built-in [Ace](https://github.com/ajaxorg/ace) code editor (loaded on demand)
* Added file extensions in filenames
* Option to display **ctime** (to find malicious files)
* Option to invert terminal output
* Removed startup "execs"
* FileManager JS crash fix (on rare envs)
* Reload file bug fix
* XHR instead IFRAME communication by default
* The client referrer is not sent
* Removed **X-Content-Type-Options** header in responses
* **Clear output** in **PHP Console** checked by default
* Option to set default tab on startup
* Built-in [safemode](https://github.com/RootShelll/safemode/) script
* File sorting (Name, Ext, Size, etc)
* Sort by filename by default
* Reading **.gz** files (not saving)
* **Show as HTML** fix in **PHP Console**
* Maximize file editor window on double click
* Restoring minimized window position
* File reload interval (right click)
* Load default **favicon.ico** if exists
* Removed **expect** from exec's
* Syntax highlighting in PHP Console
* Reduce terminal prompt if it's too long 
* **Go!** button moved to the left
* PDO_PGSQL DSN Fix
* Change method on password page (to avoid caching)
* Custom environment fix
* **Global working dir** option (File Manager path)
* Single dir/file deletion bug fix
* Terminal **color** command
* **Show as HTML** iframe sandbox
* **history** command match fix
* Supported PHP versions: 5 >= 5.3, 7, 8
</details>
<br/>


## What is P.A.S.-Fork?

**P.A.S.-Fork** is a tool used for penetration testing, designed to remain undetected by WAFs and IDSs. It helps security professionals assess vulnerabilities without triggering defensive measures that could disrupt testing.

This version improves on the original P.A.S. webshell by adding enhanced stealth and obfuscation techniques, making it a useful tool for advanced security assessments.

> ⚠️ **Important**: This tool is for educational and testing purposes only. Use it responsibly and only on systems for which you have authorized access.

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

![P.A.S.-Fork Shell Backdoor](https://i.imgur.com/VHV2iGQ.jpeg "P.A.S.-Fork Shell Backdoor")

## Educational Use Only

> 📘 **Note**: This tool should only be used in authorized environments for educational or testing purposes. Unauthorized access to systems is illegal.
