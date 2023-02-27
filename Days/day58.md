# Fuzzing

# What is Fuzzing

Fuzz testing or fuzzing is an automated software testing method that injects invalid, malformed, or unexpected inputs into a system to reveal software defects and vulnerabilities. A fuzzing tool injects these inputs into the system and then monitors for exceptions such as crashes or information leakage. Put more simply, fuzzing introduces unexpected inputs into a system and watches to see if the system has any negative reactions to the inputs that indicate security, performance, or quality gaps or issues.

Most professional bug bounty hunters believe that Fuzzing is essential for any effective vulnerability assessment because it allows them to identify subtly broken pieces of code that may be resistant to more traditional testing methodologies. Additionally, most consider it one of the most effective means of locating zero-day attacks, whereby attackers can infiltrate systems without being detected until after the damage has been done.

# **What is the history of fuzz testing?**

According to `fuzzing.info`, the term “fuzz” was created by Professor Barton Miller in the 1980s. Logged into a UNIX system via a dial-up network during a storm, Miller noticed considerable interference on the signal. The interference ultimately resulted in a crash. Miller later had his students perform a simulation of his experience using a fuzz generator to bombard UNIX systems with noise to see if they would crash.