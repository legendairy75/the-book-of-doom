- Directory Access Control(DAC) does not enablesystem administration to create security polocies like restricting spacific apps to only view log files, while allowing others to append nde data to the log files
- SEL implaments Manditory Access Control (MAC). Every process & system resorce has a spacific security lable called  a *SELinux context* or  *SELinux lable*
	- An identifyer which abstracts away system level details and focuses on the security properties
- #+BEGIN_NOTE
  It is importaint to remember that SEL policy rules are checked after DAC rules and are not used if DAC denies access first
  #+END_NOTE
-