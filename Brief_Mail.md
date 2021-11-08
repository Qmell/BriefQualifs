Brief_Mail.md

# Qualif_Le_Mail.md

un mail pas très net est passé sur notre serveur principal, une detection est remonté . Nous avons retrouvé ceci dans les logs. On vas quand même vérifier s'il n'ya pas de progation par le reseau. Merci de nous faire un retour bien developé que l'on renverra à la hierarchie. 
Essayer de retrouver un max d'info pour une analyse plus poussée.
un domaine est cité dans le mail, merci de faire la levé de doute également. Prenez vos précautions 

Artefacts 
AV 

AVAST    Win32:Apanas\ [Trj]    Malware infection
CLAMAV    Win.Trojan.Neshuta-1    Malware infection
Ms Defender    Virus:Win32/Neshta.A    Malware infection

hostname

jquery.services

mail

avsupport@autoitscript.com

Sysinternals - Strings 

P.reloc
SOFTWARE\Borland\Delphi\RTL
FPUMaskValue
IVXLCDMT
XH;XH~ P
\PROGRA~1\
QQQQQQSVW
QQQQQQS3
QQQQQQSV



C:\Windows\winsxs\amd64_microsoft-windows-p..snonwinpe.resources_31bf3856ad364e35_6.1.7601.17514_en-us_a1a558340567afb8*.*
C:\Windows\assembly\NativeImages_v2.0.50727_32\System.ComponentMod#\221fa10bd3cb407e43b7476af5039090*.*
C:\Windows\winsxs\amd64_microsoft-windows-i..ional-codepage-1026_31bf3856ad364e35_6.1.7600.16385_none_7fd5211b22da9c58*.*
C:\Windows\assembly\GAC_MSIL\Microsoft.Windows.Diagnosis.Commands.GetDiagInput.Resources*.*
C:\Python27\Lib\unittest*.*
C:\Windows\Boot\DVD\PCAT\en-US*.*
C:\Python27\tcl*.*
C:\Windows\winsxs\amd64_microsoft-windows-bcrypt-dll_31bf3856ad364e35_6.1.7600.16385_none_4a8185140916af36*.*
C:\Windows\winsxs\amd64_microsoft-windows-rasserver.resources_31bf3856ad364e35_6.1.7600.16385_en-us_d73605ecd5ec6277*.*
C:\Windows\winsxs\amd64_microsoft-windows-p..lprinting.resources_31bf3856ad364e35_6.1.7600.16385_en-us_cbe13c7988460358*.*

###################################################################################
###################################################################################

# Qualification du nom de domaine jquery.services : 


### Verdict : Malicious (OTX AlienVault)

IP Address
Domain Not Currently Resolving to an IP

WHOIS
Registrar:
NAMECHEAP INC,  

Creation Date:
Dec 29, 2020

Related Pulses
Alien Labs Pulses (1) , 
OTX User-Created Pulses (4)

Related Tags
9 Related Tags
cobalt strike, bluelight, inkysquid, cve20201380, cve202126411

VT Score : 10/89
Relations avec plusieur sous domaines 

