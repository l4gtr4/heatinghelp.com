# Reflected XSS in heatinghelp.com

Hi Team,

## Summary
main website https://heatinghelp.com/ has an endpoint that is vulnerable to an injection vulnerability - namely a reflected injection of JavaScript, also known as Reflected Cross Site Scripting (XSS). As per OWASP's definition: "Cross-Site Scripting (XSS) attacks are a type of injection, in which malicious scripts are injected into otherwise benign and trusted websites. " This happens because one of the GET parameters "term" does not properly sanitize/escape user input, allowing an injection to occur.

## Steps To Reproduce:
- go to https://heatinghelp.com/search/?term=innerHTML%3Dlocation.hash%3E%23%3Cscript%3Ealert%281%29%3C%2Fscript%3E

## Response PoC
- screenshots

## Impact
With user interaction, an attacker could execute arbitrary Javascript code in a victim's browser. This would allow an attacker to unwillingly make a victim:

    Perform any action in the identified endpoint
    View any information that the user is able to view
    Modify any information that the user is able to modify (not sure if applicable in this case)
    Interact with other application users as if it were him - impersonation (not sure if applicable in this case)

> I hope this report will be useful

> Paypal: "monaimr46@gmail.com"

> coinbase: "monaimr46@gmail.com"

> BTC: "39X6wNeMG5YfgZo1poTRbbCYn5hhZ1kfaS"

> LTC: "MQ7JgpzhXZLb7YNQCehktJknLDuw8RfJys"

> DASH: "Xmg1mhfNZoFLk6J89ZYRXeRhLcFvDxsGRb"

> HAVE A NICE DAY SIR :-)
