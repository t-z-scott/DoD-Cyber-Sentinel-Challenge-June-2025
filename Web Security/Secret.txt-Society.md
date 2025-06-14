**Difficulty: Very Easy**

_Description:_ Our team suspects that a Juche Jaguar developer accidentally left something interesting behind on a public site. You’ve been tasked with examining its structure. Can you uncover what the bots were told to ignore? Start with the usual entry points a crawler might explore. One disallowed path leads to a page where someone left behind more than just code.

# Completion Steps
1. If you don't already have one, create a wordlist with common website suffices. Some examples include `/index.txt`, `/robots.txt`, and `/secret[s].txt`.
2. Download a website fuzzer. I'm using Gobuster.
3. Go to your terminal and run this command: `gobuster dir -u https://juche.msoidentity.com -w common.txt` (or the equivalent command for your chosen website fuzzer).
   - TODO: explain the command
4. Gobuster should return `/robots.txt`.
5. Navigate to hxxps[://]juche[.]msoidentity[.]com/robots[.]txt. You'll see the blocked directory is /juchejaguar/.
6. Navigate to hxxps[://]juche[.]msoidentity[.]com/juchejaguar/, and you'll see the flag!

> Flag: C1{r0b0ts_arent_4lways_p0lit3}
