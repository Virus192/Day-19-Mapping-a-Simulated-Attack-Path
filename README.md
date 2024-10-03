# Day-19-Mapping-a-Simulated-Attack-Path

When studying cybersecurity and penetration testing, it’s essential to understand how attacks can be structured in order to better defend against them. An attack diagram provides clarity, outlining each phase of a simulated attack, helping to ensure every step flows smoothly and ethically in a controlled environment.

Today, we’re going to walk through a simulated attack plan that targets a Windows Server, starting from gaining initial access and moving through to establishing a C2 connection and exfiltrating data. For this demonstration, we’ll use the attack diagram created with draw.io, which was a key tool at the start of our project.

## Attack Diagram

### Phase 1: Initial Access — The Brute Force Entry
Our simulation begins with the Initial Access phase. We’ll be leveraging Kali Linux to perform an RDP brute-force attack against the target Windows Server in this controlled scenario. The goal here is to understand how attackers might gain access by cracking login credentials. With any luck, we’ll simulate a successful authentication and access to the machine.

![Alt text](URL_to_image)

### Phase 2: Discovery — What Are We Working With?
Once inside, it’s time to survey the environment. In the Discovery phase, we’ll be executing basic commands like `whoami`, `ipconfig`, `net user`, and `net group`. These commands will reveal important system details that attackers might exploit, and learning how to use them can help defenders protect sensitive information. We’ll keep it simple by using these common commands in our simulation.

![Alt text](URL_to_image)

### Phase 3: Defense Evasion — Silencing the Alarms
With an established RDP session, we need to simulate how attackers avoid detection. Enter the Defense Evasion phase. The first priority? Disabling Windows Defender. This part of the exercise shows how attackers could neutralize security software. Understanding these methods is crucial for creating better defense mechanisms.

![Alt text](URL_to_image)

### Phase 4: Execution — Dropping the Agent
With defenses disabled, we move into the Execution phase. We’ll use PowerShell’s `Invoke-Expression` command to simulate downloading the Mythic Agent from the C2 server. Once it’s successfully downloaded, we’ll execute it on the Windows Server. This demonstrates how attackers might set up control over the compromised system.

![Alt text](URL_to_image)

### Phase 5: Command and Control — Establishing a Link
The next phase is Command and Control (C2), where the Mythic Agent helps simulate a C2 session. This phase helps us understand how attackers maintain control over a compromised system remotely. It’s important to see how these methods work in order to strengthen defenses against them.

![Alt text](URL_to_image)

### Phase 6: Exfiltration — Extracting the Goods
In the final phase, Exfiltration, we simulate extracting sensitive data. For this demonstration, we’ve placed a fake file, `password.txt`, on the Windows Server. We’ll use the C2 connection to download this file, simulating a data breach. This phase underscores how critical it is to protect sensitive files from unauthorized access.

![Alt text](URL_to_image)

## Wrapping It All Up
And that’s the attack path in a nutshell! By following this roadmap, we’ve successfully demonstrated a simulated attack to understand how a target machine could be compromised, how attackers maintain control, and how sensitive data might be exfiltrated. This knowledge is crucial for strengthening defenses and protecting against real-world threats.