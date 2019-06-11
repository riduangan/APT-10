# APT-10 - MAY 2019
Need more IOC and IOA 

APT 10 is attacking government and private company sector through previously unknown malware.

APT10 hacking group is targeting mostly commercial activities including aviation, satellite and maritime technology, industrial factory automation, automotive supplies, laboratory instruments, banking, and finance industries.

Threat actors using typosquatting domain names similar to real, legitimate tech companies to trick victims and inject the payload to the target machine.

Initially, Once the dropper variants entered into the system, they deliver different payloads with the help of following files.

jjs.exe – legitimate executable
jli.dll – malicious DLL
msvcrt100.dll – legitimate Microsoft C Runtime DLL
svchost.bin – binary file

Researchers also discovered PlugX and Quasar, two different Remote Access Trojans among these variants.

“PlugX is a modular structured malware that has many different operational plugins such as communication compression and encryption, network enumeration, files interaction, remote shell operations and more.”

During the first stage of the infection process, a loader starts abusing the legitimate executable process (  jjs.exe ) and inject the malicious DLL inside, a method is known as DLL Side-Loading.

According to Ensilo Research, “The malicious DLL maps the data file, svchost.bin, to memory and decrypt it. The decrypted content is a shellcode that is injected into svchost.exe and contains the actual malicious payload.”

The first variant delivers both PlugX and Quasar and the downloaded payload is a modified Quasar RAT to extract passwords from the victim machine using an addition called SharpSploit , a .NET post-exploitation library written in C#.

Another PlugX collects information about the infected machine such as the computer name, username, OS version, RAM usage, network interfaces, and resources. 

Researchers uncovered the APT10 attackers using C&C servers located in South Korea and some of the mentioned domain mappings were recently updated. Also, the certificate embedded in the Quasar sample.



credit to Balaji
https://gbhackers.com/chinese-apt10-hackers/
