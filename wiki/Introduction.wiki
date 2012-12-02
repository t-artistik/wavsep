<b><u>Introduction</u></b><br>
The wavsep project is aimed to assist security researchers, analysts, consultants, QA engineers and software developers in evaluating the various features of web application vulnerability scanners.<br><br>
<b><u>Details</u></b><br>
The project currently focuses on accuracy evaluation, by presenting a series of vulnerability challenges for web application scanners, in order to verify which unique instances can be detected by the evaluated products.<br><br>
The project structure is designed around directories containing isolated vulnerabilities – <br><br>
Each one of the vulnerability-based directories focuses on a single vulnerability, with multiple test cases that attempt to simulate specific instances of the vulnerability (although each test case might be vulnerable to additional security exposures).<br><br>
The project is implemented as a web application which is implemented in JSP, and contains a JSP page that serves as a database installer.<br><br>
Although it runs on both Linux and Windows, in order for all the test cases to function properly, it's best to install the application on Windows (10+ LFI test cases).