# Install-Software-in-a-Linux-Distribution

<h2>Activity Overview</h2>

In this lab activity, I’ll use the Advanced Package Tool (APT) and sudo to install and uninstall applications in a Linux Bash shell. 

While installing Linux applications can be a complex task, the APT package manager manages most of this complexity for me and allows me to quickly and reliably manage the applications in a Linux environment.

I’ll use Suricata and tcpdump as an example. These are network security applications that can be used to capture and analyze network traffic.

The virtual machine I access in this lab has a Debian-based distribution of Linux running, and that works with the APT package manager. Using a virtual machine prevents damage to a system in the event its tools are used improperly. It also gives you the ability to revert to a previous state.

As a security analyst, I'll likely need to know how to install and manage applications on a Linux operating system. In this lab activity, I’ll learn how to do exactly that!

<h2>Scenario</h2>

My role as a security analyst requires that I have the Suricata and tcpdump network security applications installed on the system.

In this scenario, I have to install, uninstall, and reinstall these applications on your Linux Bash shell. I also need to confirm that I’ve installed them correctly.

Here’s how I do this: First, I’ll confirm that APT is installed on the Linux Bash shell. Next, I’ll use APT to install the Suricata application and confirm that it is installed. Then, I’ll uninstall the Suricata application and confirm this as well. Next, I’ll install the tcpdump application and list the applications currently installed. Finally, I’ll reinstall the Suricata application and confirm that both applications are installed.

<h2>Task 1. Ensure that APT is installed</h2>

First, I’ll check that the APT application is installed so that I can use it to manage applications. The simplest way to do this is to run the apt command in the Bash shell and check the response.

I’ll use the Bash shell by typing commands after the prompt. The prompt is represented by a dollar sign ($) followed by the input cursor.

- Confirm that the APT package manager is installed in the Linux environment. To do this, type ```apt``` after the command-line prompt and press ENTER.
  
When installed, apt displays basic usage information when you run it. This includes the version information and a description of the tool:

[image]

APT is already installed by default in the Linux Bash shell in this lab because this is a Debian-based system. APT is also the recommended package manager for Debian.

<h2>Task 2. Install and Uninstall the Suricata application</h2>

In this task, I must install Suricata, a network analysis tool used for intrusion detection, and verify that it installed correctly. Then, I’ll uninstall the application.

1. Use the APT package manager to install the Suricata application.

Type ```sudo apt install suricata``` after the command-line prompt and press ENTER.

Note: The apt install and apt remove commands must be prefixed with the sudo command as elevated privileges are required to install and uninstall software in Linux.

When I install an application with APT, the output displays details of all the software to be installed. This may include additional applications that depend on the new software. These additional applications are called the dependencies of the software to be installed.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

2. Verify that Suricata is installed by running the newly installed application.

Type ```suricata``` after the command-line prompt and press ENTER.

When Suricata is installed, version and usage information is listed:

3. Use the APT package manager to uninstall Suricata.

Type ```sudo apt remove suricata``` after the command-line prompt and press ENTER. Press ENTER (Yes) when prompted to continue.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

4. Verify that Suricata has been uninstalled by running the application command again.

Type ```suricata``` after the command-line prompt and press ENTER.

Since I uninstalled Suricata, it outputs an error message:

[image]

This message indicates that Suricata can't be found anymore.

<h2>Task 3. Install the tcpdump Application</h2>

In this task, I must install the tcpdump application. This is a command-line tool that can be used to capture network traffic in a Linux Bash shell.

- Use the APT package manager to install tcpdump.

Type ```sudo apt install tcpdump``` after the command-line prompt and press ENTER.

<h2>Task 4. List the installed applications</h2>

Next, I need to confirm that I’ve installed the required applications. It's important to be able to validate that the correct applications are installed. Often you may want to check that the correct versions are installed as well.

1. Use the APT package manager to list all installed applications.

Type ```apt list --installed``` after the command-line prompt and press ENTER.

This produces a long list of applications because Linux has a lot of software installed by default.

2. Search through the list to find the tcpdump application installed.

The Suricata application is not listed because I installed and then uninstalled that application:

[image]

<h2>Task 5. Reinstall the Suricata Application</h2>

In this task, I must reinstall the Suricata application and verify that it has been installed correctly.

1. Run the command to install the Suricata application.

Type ```sudo apt install suricata``` after the command-line prompt and press ENTER.

When prompted to continue, press the ENTER key to respond with the default response. (In this case, the default response is Yes.)

2. Use the APT package manager to list the installed applications.

Type ```apt list --installed``` after the command-line prompt and press ENTER.

3. Search through the list to confirm that the Suricata application has been installed.
   
The output should include the following lines:

[image]

<h2>Conclusion</h2>

Great work!

I now have practical experience with the APT package manager. I learned to

- install applications,
- uninstall applications, and
- list installed applications.
  
Being able to manage installed applications in Linux is a key skill for any security analyst.

