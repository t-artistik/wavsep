<img src='http://sectoolmarket.com/images/website/wavsep_logo_big.png' alt='The Web Application Vulnerability Scanner Evaluation Project'>

<BR>

<br>
<br>
A vulnerable web application designed to help assessing the features, quality and accuracy of web application vulnerability scanners.<br>
<br>
This evaluation platform contains a collection of unique vulnerable web pages that can be used to test the various properties of web application scanners.<br>
<br>
<div>
<br>
<br>
<H3><br>
<br>
AS OF 2014/01/01, The Project File Hosting was migrated to Sourceforge.<br>
<br>
</H3><br>
<br>
<br>
New downloads (WAVSEP 1.5+) can be obtained from the project <a href='https://sourceforge.net/projects/wavsep/'>sourceforge repository</a>
<br /><div>

<b><u>Quickstart:</u></b> The easiest way to get started with wavsep evaluations is to use a pre-installed instance in one of the following training VMs (note that some of the path traversal test cases only work under windows):<br>
<a href='http://www.mavensecurity.com/web_security_dojo/'>Web Security Dojo v2.0+</a><br>
<a href='https://www.owasp.org/index.php/OWASP_Broken_Web_Applications_Project'>OWASP Broken Web Apps</a><br>
<a href='http://sourceforge.net/projects/null-gameover/files/'>null's GAMEOVER VM</a><br>

<b><u>Extras:</u><b><br>
<a href='https://github.com/andresriancho/pico-wavsep'>pico-wavsep (w3af)</a> - a minimalistic way to run wavsep<br>
<a href='https://github.com/rapid7-cookbooks/wavsep'>wavsep cookbook (rapid7)</a> - recipes to install and run wavsep on tomcat<br>

<b><u>Important Update:</u></b> as of v1.1.1, the auto-installer must be used - load war in tomcat, access URL "/wavsep/wavsep-install/install.jsp", and follow instructions (the installation scripts which are provided in the separate download are designed for legacy wavsep versions - 1.0.3/1.0).<br>

<br>
<br>
<H3><br>
<br>
Previous benchmarks performed using the platform:<br>
<br>
</H3><br>
<br>
<br>
<br>
<br>
<A href='http://www.sectoolmarket.com' ><br>
<br>
<br>
<br>
<B><br>
<br>
SecToolMarket - A Dynamic Security Benchmark Presentation Platform<br>
<br>
</B><br>
<br>
<br>
<br>
</A><br>
<br>
<br>
<br>
<BR><br>
<br>
<br>
<br>
<br>
<A href='http://sectooladdict.blogspot.com/2014/02/wavsep-web-application-scanner.html'><br>
<br>
<br>
<br>
<B><br>
<br>
The 2013/2014 comparison of 12 crucial aspects of 63 commercial, SAAS and open source scanners<br>
<br>
</B><br>
<br>
<br>
<br>
</A><br>
<br>
<br>
<br>
<BR><br>
<br>
<br>
<br>
<br>
<A href='http://sectooladdict.blogspot.com/2012/07/2012-web-application-scanner-benchmark.html'><br>
<br>
<br>
<br>
<B><br>
<br>
The 2012 comparison of 10 crucial aspects of 60 commercial & open source scanners<br>
<br>
</B><br>
<br>
<br>
<br>
</A><br>
<br>
<br>
<br>
<BR><br>
<br>
<br>
<br>
<br>
<A href='http://sectooladdict.blogspot.com/2011/08/commercial-web-application-scanner.html'><br>
<br>
<br>
<br>
<B><br>
<br>
The 2011 comparison of 60 commercial & open source scanners<br>
<br>
</B><br>
<br>
<br>
<br>
</A><br>
<br>
<br>
<br>
<BR><br>
<br>
<br>
<br>
<br>
<A href='http://sectooladdict.blogspot.com/2010/12/web-application-scanner-benchmark.html'><br>
<br>
<br>
<br>
<B><br>
<br>
The 2010 comparison of 42 open source scanners<br>
<br>
</B><br>
<br>
<br>
<br>
</A><br>
<br>
<br>
<br>
<b><u>Note:</u></b> as of v1.2 - in order to get a full coverage of the path traversal test cases, the tomcat web server <b><i>must</i></b> run with <b>admin/root/high privileged</b> OS user account.<br>
<br>
<BR><br>
<br>
<br>
<br>
<b><u>Potential Issue:</u></b> Even without the LFI/RFI test cases, due to the usage of the default derby-db location, wavsep might require the tomcat user to have <b>admin/root permissions</b> under linux/win7. Will be fixed ASAP. An alternative (and more elegant) solution was proposed by Steve Pinkham (@spinkham) of Maven Security: making sure $CATALINA_BASE/db exists and is writable by the tomcat process.<br>
For example, on Ubuntu, that's /var/lib/tomcat6:<br>
sudo mkdir /var/lib/tomcat6/db<br>
sudo chown tomcat6:tomcat6 /var/lib/tomcat6/db/<br>

Additional information can be found in the developer's blog:<br>
<a href='http://sectooladdict.blogspot.com/'>http://sectooladdict.blogspot.com/</a>

PDF files with detailed feature comparison are now hosted in the following web site: <a href='http://code.google.com/p/sectooladdict-benchmarks/'>http://code.google.com/p/sectooladdict-benchmarks/</a>

<br>
<br>
<H3><br>
<br>
Project WAVSEP currently includes the following test cases:<br>
<br>
</H3><br>
<br>
<br>
<u>Vulnerabilities:</u>
<ul>
<li><b>Path Traversal/LFI:</b> 816 test cases, implemented in 816 jsp pages (GET & POST)</li>
<li><b>Remote File Inclusion (XSS via RFI):</b> 108 test cases, implemented in 108 jsp pages (GET & POST)</li>
<li><b>Reflected XSS:</b> 66  test cases, implemented in 64 jsp pages (GET & POST)</li>
<li><b>Error Based SQL Injection:</b> 80  test cases, implemented in 76 jsp pages (GET & POST)</li>
<li><b>Blind SQL Injection:</b> 46  test cases, implemented in 44 jsp pages (GET & POST)</li>
<li><b>Time Based SQL Injection:</b> 10  test cases, implemented in 10 jsp pages (GET & POST)</li>
<li><b>Unvalidated Redirect:</b> 60  test cases, implemented in 60 jsp pages (GET & POST)</li>
<li><b>Old, Backup and Unreferenced Files:</b> 184 test cases, implemented in 184 files (GET Only)</li>
<li><b>Passive Information Disclosure/Session Vulnerabilities (inspired/imported from ZAP-WAVE):</b> 3 test cases of erroneous information leakage, and 2 cases of improper authentication / information disclosure - implemented in 5 jsp pages</li>
<li><b>Experimental Test Cases (inspired/imported from ZAP-WAVE):</b> 9 additional RXSS test cases (anticsrf tokens, secret input vectors, tag signatures, etc), and 2 additional SQLi test cases (INSERT) - implemented in 11 jsp pages (GET & POST)</li>
</ul>

<u>False Positives: </u>
<ul>
<li>7 different categories of false positive Reflected XSS vulnerabilities (GET & POST )</li>
<li>10 different categories of false positive SQL Injection vulnerabilities (GET & POST)</li>
<li>8 different categories of false positive path traversal/LFI vulnerabilities (GET & POST)</li>
<li>6 different categories of false positive (xss via) remote file inclusion vulnerabilities (GET & POST)</li>
<li>9 different categories of false positive unvalidated redirect vulnerabilities (GET & POST)</li>
<li>3 different behavior categories of false positive old, backup and unreferenced files (GET Only)</li>
</ul>

<u>Additional Features: </u>
<ul>
<li> A simple web interface for accessing the vulnerable pages </li>
<li> An auto-installer for the mysql database schema (/wavsep-install/install.jsp) </li>
<li> Sample detection & exploitation payloads for each and every test case </li>
<li> Database connection pool support, ensuring the consistency of scanning results </li>
</ul>

<br>
<br>
<H3><br>
<br>
Usage<br>
<br>
</H3><br>
<br>
<br>
Although some of the test cases are vulnerable to additional exposures, the purpose of each test case is to evaluate the detection accuracy of one type of exposure, and thus, “out of scope” exposures should be ignored when evaluating the accuracy of vulnerability scanners.<br>
<br>
<br>
<br>
<H3><br>
<br>
Installation<br>
<br>
</H3><br>
<br>
<br>
(@) Use a JRE/JDK that was installed using an offline installation (the online installation caused unknown bugs for some users).<br>
(1) Download & install Apache Tomcat 6.x<br>
(2) Download & install MySQL Community Server 5.5.x (Remember to enable remote root access if not in the same station as wavsep, and to choose a root password that you remember). <br>
(3) Copy the wavsep.war file into the tomcat webapps directory<br>
(Usually "C:\Program Files\Apache Software Foundation\Tomcat 6.0\webapps" - Windows 32/64 Installer)<br>
(4) Restart the application server<br>
(5) On <b>WinXP</b>, as long as you are using a high privileged user - you can skip this phase,  on <b>Win7</b>, make sure you run the tomcat server with administrative privileges (right click on and execute),and on <b>Ubuntu Linux</b>, run the following commands:<br>
<blockquote><i>sudo mkdir /var/lib/tomcat6/db</i><br>
<i>sudo chown tomcat6:tomcat6 /var/lib/tomcat6/db/</i><br>
(6) Initiate the install script at: <a href='http://localhost:8080/wavsep/wavsep-install/install.jsp'>http://localhost:8080/wavsep/wavsep-install/install.jsp</a><br>
(7) Provide the database host, port and root credentials to the installation script, in additional to customizable wavsep database user credentials.<br>
(8) Access the application at: <a href='http://localhost:8080/wavsep/'>http://localhost:8080/wavsep/</a></blockquote>

<br>
<br>
<H3><br>
<br>
Troubleshooting Installation Issues<br>
<br>
</H3><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 As of version v1.1.1, several installation related issues were fixed (encoding / other).<br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 Make sure the JRE/JDK was installed using an offline installer.<br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 Make sure the tomcat server was installed after the offline JRE/JDK installation.<br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 Make sure that the mysql server was installed with remote root connection enabled, and with a firewall rule exception (options in the mysql installer).<br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 If previous versions of wavsep v1.1.0+ were installed, it's best to delete the "db" folder which was created after the previous installation under the tomcat root directory - prior to installing the new version (the installation should work even without this deletion, as long as sql-related pages were not accessed in the current tomcat execution).<br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 If the previous derby database was not deleted prior to the installation for whatever reason, do not access any sql-related existing pages before accessing the schema installation page. <br>
<br>
</LI><br>
<br>
<br>
<br>
<br>
<LI><br>
<br>
 On windows 7, it might be necessary to run the tomcat server with administrative permissions for the SQLi test cases installation to work properly.<br>
<br>
</LI><br>
<br>
