---
title: "Nastavení a nasazení místních prostředí"
description: "Toto téma poskytuje informace o tom, jak naplánovat, nastavit a nasadit místní prostředí."
author: sarvanisathish
manager: AnnBe
ms.date: 08/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations, Unified Operations
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: d100f6dbcbdf8f4c12ab04670fb598a88d48d84b
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: cs-cz
ms.lasthandoff: 08/10/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Nastavení a nasazení místních prostředí

Tento dokument popisuje jak naplánovat nasazení a nastavení infrastruktury a nasadit Microsoft Dynamics 365 Finance and Operations, edici Enterprise (místní).

## <a name="finance-and-operations-components"></a>Komponenty Finance and Operations

Aplikace Finance and Operations obsahuje tři hlavní komponenty:

- Server AOS (Application Object Server)
- Obchodní logika (BI)
- Finanční reporting / Management Reporter

Tyto komponenty závisí na následujícím systémovém softwaru:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1 s následujícími funkcemi:

    - Fultextové vyhledávání je povoleno.
    - Služby SQL Server Reporting Services (SSRS).
    - Služby SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Aplikace nebude fungovat, pokud nebude povoleno fultextové vyhledávání.

- SQL Server Management Studio
- Standalone Microsoft Azure Service Fabric
- Windows PowerShell 5.0 nebo vyšší
- Active Directory Federation Services (AD FS) na Windows Server 2016

  Řadič domény musí být Windows Server 2012 R2 nebo pozdější s funkční úrovní domény 2012 R2, nebo vyšší

  Více informací o funkčních úrovních domény najdete v: 
  - [Co jsou funkční úrovně Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Porozumění funkčním úrovním domén Active Directory](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Bity aplikace Finance and Operations jsou distribuovány pomocí Microsoft Dynamics Lifecycle Services (LCS). Před tím, než budete moci provést nasazení, musíte zakoupit licenční klíče prostřednictvím kanálu [Enterprise Agreements](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) a nastavit místní projekt v LCS. Nasazení lze zahájit pouze prostřednictvím LCS. Více informací o tom, jak nastavit místní projekty v LCS najdete v [Tvorba místního projektu v Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Ověřování

Místní aplikace pracuje s AD FS. Pro interakci s LCS musíte také nakonfigurovat Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations používá Standalone Service Fabric. Více informací najdete v [Dokumentace Service Fabric](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktura

Aplikace Finance and Operations je navržena tak, aby pracovala na hyper-konvergované architektuře. Hardwarová konfigurace obsahuje následující komponenty:

- Cluster Standalone Service Fabric, který je založen na virtuálních počítačích (VM) Windows Server 2016
- SQL Server (podporováno je Clustered SQL i Always-On)
- AD FS pro autentizaci
- Server Message Block (SMB) verze 3 sdílení souborů pro úložiště
- Nepovinné: Microsoft Office Server 2017

Více informací najdete v sekci [Systémové požadavky](../get-started/system-requirements.md) a příručkách týkajících se rozsahu.

### <a name="hardware-layout"></a>Uspořádání Hardwaru

Naplánujte svoji infrastrukturu a cluster Service Fabric na základě doporučeného rozsahu v sekci [Rozsah hardwaru pro místní prostředí](../get-started/hardware-sizing-on-premises-environments.md). Více informací o tom jak naplánovat cluster Service Fabric najdete v sekci [Naplánujte a připravte nasazení svého samostatného cluster Service Fabric](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

Následující tabulka obsahuje příklad uspořádání hardwaru. Tento příklad je použit v rámci tohoto tématu pro ilustraci nastavení.

> [!NOTE]
> Primární uzel clusteru Service Fabric musí mít alespoň tři uzly. V tomto příkladu je **Typ orchestrátoru** určen jako typ primárního uzlu.

| Účel počítače                                 | Název počítače    | Adresa IP    |
|-------------------------------------------------|-----------------|---------------|
| Řadič domény                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Souborový server                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On cluster                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klient                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric cluster/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric cluster/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric cluster/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric cluster/Orchestrátor 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric cluster/Orchestrátor 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric cluster/Orchestrátor 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Cluster Service Fabric / uzel Management Reporter | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric cluster/uzel SSRS                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Nastavení

### <a name="prerequisites"></a>Požadavky

Před začátkem nastavování musí být splněny následující požadavky. Nastavení těchto požadavků je mimo rámec tohoto dokumentu.

- Služba Active Directory Domain Services (AD DS) je instalována a nakonfigurována ve vaší síti.
- AD FS je nasazena.
- SQL Server, SSRS a Management Studio jsou nainstalovány.

### <a name="overview"></a>Přehled

Pro nastavení infrastruktury pro aplikaci Finance and Operations musí být provedeny následující kroky.

1. Naplánujte svůj název domény a zóny DNS
2. Naplánujte a získejte své certifikáty
3. Naplánujte uživatelské a servisní účty
4. Vytvořte zóny DNS a přidejte záznamy A
5. Připojte virtuální počítače k doméně
6. Přidejte požadovaný software do virtuálních počítačů
7. Stáhněte skripty nastavení z LCS
8. Popište svoji konfiguraci
9. Instalujte certifikáty
10. Nastavte samostatný cluster Service Fabric
11. Konfigurujte konektivitu LCS pro klienta
12. Nastavte uložení souborů
13. Nastavte SQL Server
14. Nakonfigurujte databáze
15. Zašifrujte přístupové údaje
16. Nastavit SSRS
17. Nakonfigurujte AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Naplánujte svůj název domény a zóny DNS

Doporučujeme vám použít název veřejně registrované domény pro vaši produkční instalaci AOS. Tím zajistíte možnost připojení mimo síť, pokud bude vyžadován vnější přístup.

Pokud je například doména vaší společnosti contoso.com, vaše zóna pro Finance and Operations (místní) by mohla být d365ffo.onprem.contoso.com a názvy hostitele by mohly být následující:

- ax.d365ffo.onprem.contoso.com pro počítače AOS
- sf.d365ffo.onprem.contoso.com pro cluster Service Fabric

### <a name="plan-and-acquire-your-certificates"></a>Naplánujte a získejte své certifikáty

Certifikáty Secure Sockets Layer (SSL) jsou vyžadovány pro zajištění clusteru Service Fabric a všech aplikací, které budou nasazeny. Pro vaši produkční a sandboxovou zátěž doporučujeme, aby jste získali certifikáty od certifikační autority, jako je [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) nebo [GlobalSign](https://www.globalsign.com/en/ssl/). Pokud je vaše doména nastavena se službami [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), můžete tyto certifikáty vytvořit prostřednictvím AD CS. Každý certifikát musí obsahovat privátní klíč, který byl vytvořen pro výměnu klíčů, a musí být exportovatelný do souboru Personal Information Exchange (.pfx).

Certifikáty podepsané svým držitelem mohou být použity pouze pro účely testování. Pro usnadnění, skripty nastavení obsahují skripty, které generují a exportují certifikáty podepsané uživatelem. Jak jsme se již zmínili, tyto certifikáty smějí být použity pouze pro účely testování.

| Účel                                      | Vysvětlení | Další požadavky |
|----------------------------------------------|-------------|-------------------------|
| Certifikát SQL Server SSL                   | Tento certifikát se používá pro šifrování dat, které se vysílají po síti mezi instancí SQL Server a klientskou aplikací. | <p>Doménový název certifikátu by se měl shodovat s plně kvalifikovaným názvem domény (fully qualified domain name - FQDN) instance SQL Serveru nebo příjemce.</p><p>Pokud je například příjemce SQL hostovaný na stroji DAX7SQLAOSQLA, DNS název certifikátu by měl být DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Certifikát Service Fabric            | Tento certifikát se také používá k zabezpečení komunikace uzel - uzel mezi uzly Service Fabric. Tento certifikát se také používá jako certifikát serveru, který je předán klientovi, který se připojí na cluster. | <p>Doménový název certifikátu se musí shodovat se zónou DNS ve které jsou hostovány AOS a Service Fabric.</p><p>Na příklad, doménový název certifikátu by mohl být \*.onprem.contoso.com nebo \*.contoso.com.</p><p>Pokud používáte referenční certifikát, referenční znak se týká pouze jedné úrovně. Subdoména, alternativní název subjektu (SAN) musí být aplikován na certifikát pokud obsahuje více než jednu úroveň, jako \*.contoso.com v předešlém příkladu.</p> |
| Klientský certifikát Service Fabric            | Tento certifikát je používán klienty pro zobrazení a správu clusteru Service Fabric. | |
| Šifrovací certifikát                     | Tento certifikát se používá pro šifrování citlivých informací jako je heslo pro SQL Server a uživatelské účty. | <p>Použití šifrovacího certifikátu musí obsahovat Data Encipherment (10) a neměl by obsahovat Server Authentication nebo Client Authentication.</p><p>Více informací najdete v [Správa tajných informací v aplikacích Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| Certifikát AOS SSL                          | <p>Tento certifikát se používá jako certifikát serveru, který je předán klientovi pro webové stránky AOS. Používá se rovněž pro povolení certifikátů Windows Communication Foundation (WCF) / Simple Object Access Protocol (SOAP).</p><p>Certifikát serveru Service Fabric zde lze použít, pokud se jedná o zástupný certifikát.</p> | <p>Název domény certifikátu musí odpovídat DNS zóně, kde je hostován AOS a Service Fabric.</p><p>Název domény certifikátu může být například \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com, or \*.contoso.com.</p><p>Pokud používáte zástupný certifikát, zástupný znak se týká pouze jedné úrovně. Subdoména, alternativní název předmětu (SAN), musí být aplikovaná k certifikátu v případě, že jde o více než jednu úroveň, např. \*. contoso.com v předchozím příkladu.</p> |
| Certifikát ověřování relace           | Tento certifikát AOS slouží k zabezpečení informací o relaci uživatele. | Jedná se také **sdílený** certifikát, který bude použit v době nasazení z LCS. |
| Certifikát šifrování dat a podepisování dat | Tyto certifikáty používá Server AOS k šifrování citlivých informací. | |
| Certifikát Finanční vykazování klienta       | Tento certifikát se používá pro zabezpečení komunikace mezi službami finančního vykazování a AOS. | |
| Certifikát vykazování                        | Tento certifikát se používá pro zabezpečení komunikace mezi SSRS a AOS. | |
| Certifikát Místní lokální agent           | <p>Tento certifikát se používá k zabezpečení komunikace mezi lokálním agentem, který je hostován místně, a LSC.</p><p>Tento certifikát umožňuje místnímu zástupci jednat v zastoupení vašeho Azure AD klienta a komunikovat s LCS pro orchestraci a sledování nasazení.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Naplánujte účty vašich uživatelů a služeb

Aby bylo Finance and Operations (místní) možné používat, je nutné vytvořit několik účtů uživatelů nebo služby. Je nutné vytvořit kombinací účtů spravované skupiny služeb (gMSAs), účtů domény a účtů SQL. Následující tabulka zobrazuje účty uživatele, jejich účel a příklad názvů, které budou použity v tomto tématu.

| Účet uživatele                                            | Typ           | Účel | Uživatelské jméno |
|---------------------------------------------------------|----------------|---------|-----------|
| Účet služby Finanční vykazování         | gMSA           |         | Contoso\\svc-FRAS$ |
| Účet služby procesu Finanční vykazování             | gMSA           |         | Contoso\\svc-FRPS$ |
| Účet služby Financial Reporting Click Once Designer | gMSA           |         | Contoso\\svc-FRCO$ |
| Účet služby AOS                                     | gMSA           | Tohoto uživatele je nutné vytvořit pro budoucí jištění. Plánujeme povolení AOS, aby pracoval s gMSA v budoucích verzích. Vytvořením tohoto uživatele v době instalace pomůžete zaručit bezproblémový přechod na gMSA. | Contoso\\svc-AXSF$ |
| Účet služby AOS                                     | Účet domény | AOS používá tohoto uživatele ve verzi GA. | Contoso\\AXServiceUser |
| Účet správce databáze SQL Serveru AOS                                   | Uživatel SQL       | Finance and Operations používá k ověření SQL tohoto uživatele\*. Tohoto uživatele také nahradí gMSA uživatel v nových verzí. | AXDBAdmin |
| Účet služby Agent místního nasazení                  | gMSA           | Tento účet používá místní agent k orchestraci nasazení v různých uzlech. | Contoso\\Svc-LocalAgent$ |

\*SQL uživatelské jméno a heslo pro ověřování serveru SQL jsou zabezpečené, protože jsou šifrovány a uloženy ve sdílené položce.

### <a name="create-dns-zones-and-add-a-records"></a>Vytvořte zóny DNS a přidejte záznamy A

DNS je integrován s AD DS a umožňuje vám organizovat, spravovat a najít prostředky v síti. Vytvořte zóny dopředného vyhledávání DNS a záznamy A pro název hostitele serveru AOS a cluster Service Fabric. V tomto případě je název serveru DNS zóny d365ffo.onprem.contoso.com a názvy záznamů A / hostitele jsou následující:

- **ax**.d365ffo.onprem.contoso.com pro počítače AOS
- **sf**.d365ffo.onprem.contoso.com pro cluster Service Fabric

#### <a name="add-a-dns-zone"></a>Přidejte zónu DNS

Zónu DNS můžete přidat následujícím postupem.

1. Přihlaste se k počítači řadiče domény, klepněte na tlačítko **Start** a spusťte Správce serveru DNS zadáním **dnsmgmt.msc**.
2. Klepněte pravým tlačítkem myši na název řadiče domény, klepněte na příkaz **Nová zóna** \> **Další**.
3. Vyberte **Primární zóna**.
4. Ponechte políčko **Uložit zónu ve službě Active Directory (k dispozici pouze v případě, že je DNS Server zapisovatelným řadičem domény)** zaškrtnuto a klepněte na tlačítko **Další**.
5. Vyberte **Všem serverům DNS spuštěným na řadičích domény v této doméně: Contoso.com** a klepněte na tlačítko **Další**.
6. Vyberte **Zónu dopředného vyhledávání** a klepněte na tlačítko **Další**.
7. Zadejte název zóny pro vaše nastavení a klepněte na tlačítko **Další**. Např. zadejte **d365ffo.onprem.contoso.com**.
8. Vyberte **Nepovolovat dynamické aktualizace** a klepněte na tlačítko **Další**.

#### <a name="set-up-an-a-record-for-aos"></a>Nastavte záznam A pro AOS

V nové zóně DNS vytvořte jeden záznam A s názvem **ax.d365ffo.onprem.contoso.com** pro **každý** uzel clusteru Service Fabric typu **AOSNodeType**. Nevytvářejte záznamy A pro jiné typy uzlů.

1. Klikněte pravým tlačítkem myši na novou zónu a klikněte na **Nový hostitel**.
2. Zadejte název a adresu IP uzlu Service Fabric (např. 10.179.108.12) a poté klepněte na tlačítko **Přidat hostitele**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Vytvořte záznam A pro orchestrator

V nové zóně DNS vytvořte jeden záznam A s názvem **sf.d365ffo.onprem.contoso.com** pro **každý** uzel clusteru Service Fabric typu **OrchestratorType**. Nevytvářejte záznamy A pro jiné typy uzlů.

1. Klikněte pravým tlačítkem myši na novou zónu a klikněte na **Nový hostitel**.
2. Zadejte název a IP adresu uzlu Service Fabric (např. 10.179.108.15) a klepněte na tlačítko **Přiřadit hostitele**.

#### <a name="join-vms-to-the-domain"></a>Spojte virtuální počítače s doménou

Připojte každý virtuální počítač k doméně podle sekce [Jak spojit Windows Server 2016 s doménou Active Directory](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Jako alternativu můžete použít skript Windows PowerShell.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Jakmile budou virtuální počítače spojeny s doménou, přidejte servisní účty AOS (Contoso\svc-AXSF$ , Contoso\svc-AXSF$ ) ke skupině lokálních administrátorů. V článku [Přidat člena k lokální skupině](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) se dozvíte jak to provést.

#### <a name="disable-user-access-control"></a>Zakažte řízení uživatelských účtů 

Spusťte následující skript a zakažte řízení uživatelských účtů na **každém** uzlu Service Fabric.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Po úspěšném skončení skriptu musíte uzel restartovat.

#### <a name="add-prerequisite-software-to-vms"></a>Přidejte požadovaný software do virtuálních počítačů

Následující tabulka obsahuje seznam požadovaného softwaru, který musí být v počítačích pro každý typ uzlu.

> [!NOTE]
> Po instalaci komponentů budete muset restartovat svůj počítač.

| Typ uzlu | Součást | Příkaz |
|-----------|-----------|---------|
| AOS       | SNAC - Ovladač ODBC | Zobrazit [Ovladač Microsoft ODBC 13.1 pro SQL Server – Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Rozhraní Microsoft .NET Framework verze 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Rozhraní Microsoft .NET Framework verze 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internetová informační služba (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Aplikace Microsoft Visual C++ Redistributable Packages pro aplikaci Microsoft Visual Studio 2013 | Viz [Aplikace Microsoft Visual C++ Redistributable Packages pro aplikaci Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Redistributable | Viz [Microsoft Access Database Engine 2010 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | Rozhraní .NET Framework verze 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | Rozhraní .NET Framework verze 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 v **nativním** režimu | |
| MR        | Rozhraní .NET Framework verze 2.0 – 3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | Rozhraní .NET Framework verze 4.0 – 4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Redistributable Packages pro aplikaci Visual Studio 2013. | Viz [Aplikace Microsoft Visual C++ Redistributable Packages pro aplikaci Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Stáhněte skripty nastavení z LCS

K dispozici několik skriptů k vylepšení zkušenosti nastavení. Tento postup slouží ke stažení skriptů nastavení z LCS.

1. Přihlaste se k LCS (<https://lcs.dynamics.com/v2>).
2. Na řídicím panelu klepněte na dlaždici **knihovna Shared asset**.
3. Klepněte na kartu **Model**.
4. V mřížce vyberte řádek **Dynamics 365 pro Operations – skripty pro místní nasazení**.
5. Klepněte na tlačítko **Verze** a stáhněte nejnovější verzi skriptů.

### <a name="describe-your-configuration"></a>Popište svoji konfiguraci

Tento oddíl obsahuje informace o skriptech, které je nutné spustit. Skripty jsou uvedeny v pořadí, ve kterém se musí spustit. Pro spuštění skriptů vyplňte šablonu na $(downloadPath)\\ConfigTemplate.xml. Soubor ConfigTemplate.xml popisuje clustery Service Fabric, certifikáty, které jsou použity k jejich konfiguraci a účty, kterým musí být udělen přístup k příslušným certifikátům. V uvedeném příkladu jsou vyplněné hodnoty pro příklad infrastruktury popsané v tomto tématu. Soubor šablony se použije v následujícím oddílu.

#### <a name="create-the-domain-account-for-a-service-user"></a>Vytvořte účet domény pro uživatele služby

Spusťte následující příkaz pro vytvoření účtu uživatele domény, contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Vytvořit gMSAs

1. Změňte adresář na **$(DownloadPath)** a spusťte následující příkaz prostředí Windows PowerShell.

    > [!NOTE]
    > Tento skript nevytváří uživatele. Namísto toho vytiskne příkazy, které je nutné ručně spustit v počítači řadiče domény.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Zkopírujte výstup příkazu do okna prostředí Windows PowerShell. Ujistěte se, že jsou odebrány zalomení řádků, a spusťte řádky v počítači řadiče domény služby Active Directory pomocí zvýšených oprávnění (pravým tlačítkem myši a poté klepněte na položku **Spustit jako správce**).
3. Spusťte následující skript v počítači řadiče domény služby Active Directory k ověření, že účty byly úspěšně vytvořeny. Ujistěte se, že spouštíte skript až potom, co jste nahradili vzor odpovídající konvenci názvů účtů služeb.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Spusťte skript Export-AddGMSAsONVMScript.ps1 v klientském počítači. Tento skript generuje skripty, které jsou spouštěny v každém virtuálním počítači Service Fabric, a přidává je do složky, která odpovídá názvu každého virtuálního počítače.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Zastavit IIS

Připojte jednotlivé virtuální počítače Service Fabric pomocí protokolu vzdálené plochy (RDP) a dokončete manuální kroky v [Spuštění nebo zastavení webového serveru (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Alternativně, použijte následující skript Windows PowerShell pomocí RDP pro připojení jednotlivých virtuálních počítačů Service Fabric.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_Funkce služby IIS by měla nainstalována, ale zakázána, protože existují některé závislosti knihovny DLL služby IIS v produktu._

### <a name="install-certificates"></a>Instalujte certifikáty

1. Pokud jste získali certifikáty, které byly uvedené v tomto tématu, od certifikačního úřadu, vyplňte název souboru .pfx a kryptografický otisk pro certifikáty v souboru ConfigTemplate.xml. Nastavte atribut **generateSelfSignedCert** na **False** a **exportovatelný** atribut na **False**. Zkopírujte soubory .pfx do složky $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Pokud používáte certifikáty podepsané uživatelem (pouze pro testovací účely), spusťte následující skript. Pro vytvoření certifikátů podepsaných uživatelem se v souboru ConfigTemplate.xml ujistěte, že **generateSelfSignedCert** je nastaven na hodnotu **True** a **exportovatelný** je nastaven na **True**. Skript aktualizuje soubor XML s kryptografickým otiskem pro certifikáty.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Exportujte nové certifikáty se soukromým klíčem (soubor .pfx). Použijte následující skript pro generování a spuštění exportních příkazů v prostředí Windows PowerShell. Soubory .pfx budou umístěny do složky certifikátů.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Certifikáty musí být nainstalovány a musí se nacházet v certifikátu:\\CurrentUser\\My. Certifikát musí být také exportovatelný.

    Pokud používáte certifikáty podepsané uživatelem, přejděte k další části. Tento proces nemusíte dokončovat.

4. Po exportu nebo zkopírovaní souborů .pfx do složky $(DownloadPath)\\InfrastructureScripts\\Certs spusťte následující příkazy pro generování skriptů, které budou umístěny do složek odpovídajících virtuálním počítačům.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Zkopírujte skripty v každé složce do virtuálních počítačů odpovídajících názvu složky.
6. Na každém virtuálním počítači spusťte skripty v pořadí, v jakém se objeví.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Nastavte standalone cluster Service Fabric

1. Spusťte následující příkaz pro generování souboru ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Další informace zobrazíte v sekci [Krok 1B: vytvořit cluster s více počítači](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Zabezpečení samostatného clusteru ve Windows pomocí certifikátů X.509](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) a [Vytvořit samostatný cluster spuštěný v systému Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Stáhněte [Samostatný instalační balíček Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) do jednoho z vašich uzlů Service Fabric. Po stažení souboru zip jej odblokujte klepnutím pravým tlačítkem myši na soubor zip a následným klepnutím na **Vlastnosti**. V dialogovém okně vyberte zaškrtávací políčko **Odblokovat** v pravém dolním rohu.
3. Zkopírujte soubor zip do jednoho uzlu v clusteru Service Fabric a rozbalte jej.
4. Spusťte následující příkazy pro vytvoření pravidla příchozí brány firewall na portech 443 a 445 ve všech uzlech.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Spusťte následující příkazy pro vytvoření pravidla příchozí brány firewall na port 80 pouze pro uzly SSRS.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopírujte váš soubor ClusterConfig.json do vašeho rozbaleného místa pro instalaci samostatné služby Service Fabric.
7. Přejděte k umístění rozbaleného místa instalace v prostředí Windows PowerShell pomocí zvýšených oprávnění a spusťte následující příkaz pro test ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Je-li test úspěšný, spusťte následující příkaz k nasazení clusteru.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Po vytvoření clusteru otevřete průzkumník Service Fabric v jakémkoliv klientském počítači pro ověření instalace:

    1. Instalujte klientský certifikát Service Fabric do CurrentUser\\My pokud již není nainstalován.
    2. Přejděte na **nastavení IE**\>**Režim kompatibility** a zrušte zaškrtnutí políčka **Zobrazení intranetových stránek v režimu kompatibility**.
    3. Přejděte na `https://sf.d365ffo.onprem.contoso.com:19080`, kde je sf.d365ffo.onprem.contoso.com hostitelským názvem clusteru Service Fabric, který je zadaný v zóně. Pokud není nakonfigurováno rozlišení názvu DNS, použijte adresu IP počítače.
    4. Vyberte klientský certifikát. Zobrazí se stránka **Průzkumník Service Fabric**.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Konfigurujte konektivitu LCS pro klienta

Nasazení a údržba Finance and Operations jsou orchestrovány prostřednictvím LCS pomocí místního lokálního agenta. Pro vytvoření připojení z LCS do klienta Finance and Operations, je nutné konfigurovat certifikát, který povoluje lokálnímu agentu jednat v zastoupení vašeho klienta Azure AD (například Contoso.Onmicrosoft.com).

Použijte certifikát lokálního agenta, který jste obdrželi od certifikačního úřadu nebo podepsaný certifikát, který jste vygenerovali pomocí skriptů.

Certifikáty k povolení LCS mohou přidat pouze uživatelské účty s oprávněním správce globálního adresáře. Standardně bude správcem globálního adresáře osoba, která se zaregistruje pro aplikaci Microsoft Office 365 pro vaší organizaci.

> [!NOTE]
> Certifikát je nutné konfigurovat přesně jednou za klienta. Všechna místní prostředí lze připojit k LCS pomocí stejného certifikátu.

1. Stáhněte a nainstalujte nejnovější verzi Azure PowerShell v klientském počítači. Další informace naleznete v tématu [Instalace a konfigurace prostředí PowerShell Azure](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Přihlaste se k [Azure portálu zákazníka](https://portal.azure.com) pro ověření, že máte roli správce globálního adresáře.
3. Spusťte následující skript z $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Nastavit úložiště souborů

Musíte vytvořit dvě vysoce dostupné sdílené položky SMB 3.0. Informace o způsobu povolení SMB 3.0 naleznete v tématu[Vylepšení zabezpečení SMB](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Zabezpečené dialektové vyjednávání nedokáže rozpoznat nebo zabránit degradaci SMB 2.0 nebo 3.0 na SMB 1.0. Z tohoto důvodu a také abyste mohli využívat všechny schopnosti SMB šifrování důrazně doporučujeme zakázat server SMB 1.0.

> [!NOTE]
> K zajištění, že jsou vaše data chráněna ve vašem prostředí i pokud nejsou právě využívána, je nutné povolit šifrování jednotky BitLocker ve všech počítačích. Informace o tom, jak povolit BitLocker najdete v [BitLocker: nasazení v systému Windows Server 2012 a pozdějším](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Sdílené úložiště, které obsahuje uživatelské dokumenty, které jsou odeslány na server AOS (například \\\\DAX7SQLAOFILE1\\aos-storage).
- Sdílené úložiště, které obsahuje poslední sestavení a konfigurační soubory pro orchestraci nasazení (například \\\\DAX7SQLAOFILE1\\agent)

    > [!NOTE]
    > Udržujte cestu ke sdílenému úložišti co nejkratší, aby nedošlo k překročení maximální délky cesty pro soubory, které budou umístěny do tohoto úložiště.

1. V počítači sdíleného úložiště spusťte následující příkaz.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Nastavte sdílené úložiště \\\\DAX7SQLAOFILE1\\aos-storage

2. Ve Správci serveru vyberte **Služby souborů a úložišť**\>**Sdílené**.
3. Klepněte na tlačítko **Úkoly**\>**Nové sdílení** pro vytvoření nového sdílení s názvem **aos-storage**.
4. Udělte oprávnění **Změnit** pro každý počítač v clusteru Service Fabric kromě **OrchestratorNodeType**.
5. Udělte oprávnění **Změnit** pro uživatele domény AOS (contoso\\AXServiceUser) a uživatele gMSA (contoso\\svc AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Nastavte sdílené úložiště agenta \\\\DAX7SQLAOFILE1\\

6. Přejděte zpět na Správce serveru, vyberte **Služby souborů a úložišť**\>**Sdílené**.
7. Klepněte na tlačítko **Úkoly**\>**Nové sdílení** pro vytvoření nového sdílení s názvem **agent**.
8. Udělte oprávnění **Úplné řízení** oprávnění uživateli gMSA pro agenta místního nasazení (contoso\\svc-LocalAgent$).

### <a name="set-up-sql-server"></a>Nastavte SQL Server

1. Nainstalujte SQL Server 2016 SP1 s vysokou dostupností, buď jako clustery SQL, které obsahují Storage Area Network (SAN) nebo v konfiguraci Always-On.  Ověřte, zda **Databázový modul, služby vykazování, fulltextové vyhledávání**, a **nástroje pro správu** jsou již nainstalovány.
> [!NOTE]
> Zkontrolujte prosím, zda SQL Always On je nastaven podle [Výběr počátečního data synchronizace stránky (Always On Availability Group Wizards)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) a postupujte podle [Příprava sekundárních databází ručně](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Spusťte službu SQL jako uživatel domény.
3. Získáte certifikát SSL od certifikační autority pro konfiguraci Finance and Operations. Pro účely testování můžete vytvořit a použít certifikát podepsaný svým držitelem.

**Certifikát podepsaný svým držitelem pro instanci Clustered SQL**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Certifikát podepsaný svým držitelem pro instanci Always-On SQL**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Pomocí certifikátu postupujte podle následujících kroků v [Povolení šifrování SSL pro instanci SQL Server pomocí Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) pro konfiguraci SSL na SQL Server.
5. Pro každý uzel clusteru postupujte následovně. Ujistěte se, že provádíte změny v neaktivním uzlu proveďte převzetí služeb při selhání po provedení změn.

    1. Importujte certifikát do LocalMachine\\My.
    2. Udělte oprávnění certifikátu pro účet služby, která se používá ke spuštění služby SQL. V aplikaci Microsoft Management Console (MMC) klepněte pravým tlačítkem myši na certifikát (certlm.msc) a klepněte na tlačítko **Úkoly**\>**Spravovat soukromé klíče**.
    3. Přidat kryptografický otisk certifikátu HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. V aplikaci Microsoft SQL Server Configuration Manager, nastavte **ForceEncryption** na **Ano**.

6. Exportujte veřejný klíč certifikátu (soubor .cer) a instalujte jej v důvěryhodném kořenu každého uzlu služby Service Fabric.

### <a name="configure-the-orchestratordata-database"></a>Konfigurovat databázi OrchestratorData

1.  Vytvořte prázdnou databázi s názvem **OrchestratorData**. Tuto databázi používá lokální agent pro orchestraci nasazení.
2.  Přidělte lokálnímu agentu gMSA (svc-LocalAgent$) **db\_owner** oprávnění pro databázi:

    1. Ve stromovém zobrazení rozbalte název serveru, rozbalte **Zabezpečení**\>**Přihlášení** a poté klepněte pravým tlačítkem myši a klepněte na položku **Nové přihlášení**.

        ![Nový příkaz přihlášení](./media/OPSetup_01_NewLogin.png)


    2. Vyhledejte účet služby **svc LocalAgent$**. Klepněte na tlačítko **Umístění** a vyberte **Celý adresář** a klepněte na tlačítko **Typy objektů** a vyberte **Účet služby**.

        ![Vyberte dialogové okno uživatele, účtu služby nebo skupiny](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Nastavte **Přiřadit ServerRole** na **Veřejné**.
    4. Přiřaďte oprávnění role databáze **db\_owner** k databázi OrchestratorData.

### <a name="configure-the-finance-and-operations-database"></a>Konfigurujte databázi aplikace Finance and Operations.

1. Přihlaste se k LCS (<https://lcs.dynamics.com/v2>).
2. Na řídicím panelu klepněte na dlaždici **knihovna Shared asset**.
3. Klepněte na kartu **Model**. 
4. V mřížce klepněte na řádek **Dynamics 365 pro operations místní, vydání Enterprise - ukázková data** pro stažení souboru zip.
5. Soubor zip obsahuje prázdné soubory a soubory s demo daty .bak. Podle potřeb vyberte odpovídající soubor .bak. Potřebujete-li např. demo data, obnovte soubor AxBootstrapDB_Demodata.bak. 
6. Obnovte databázi AxBootstrapDB_DemoData.bak.
7. Přejmenujte databázi **AXDBRAIN**.
8. Spusťte následující dotazy v obnovené databázi.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Aktualizujte databázové soubory:

    1. Klikněte pravým tlačítkem na databázi a poté klepněte na možnost **Vlastnosti**.
    2. Klepněte na tlačítko **Soubory** ke změně vlastnosti databáze.
    3. V poli **Počáteční velikost (MB)** zadejte hodnotu, která je větší než 5 120.

        ![Dialogové okno Vlastnosti databáze](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Pro **AXDBBuild\_Data**, nastavte pole **Autogrowth/maximalizační** na **200** megabajtů (MB).
    5. Pro **AXDBBuild\_Log**, nastavte pole **Autogrowth/maximalizační** na **500** MB.

        ![Změňte dialogové okno Autogrowth](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Vytvořte nového uživatele s povoleným ověřováním SQL (axdbadmin).
6. Pomocí informací v tabulce namapujte uživatele a databázové role.

    | Uživatel             | Typ    | Role databáze |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_owner     |
    | svc-LocalAgent$  | gMSA    | db\_owner     |
    | svc-FRPS$        | gMSA    | db\_owner     |
    | svc-FRAS$        | gMSA    | db\_owner     |
    | axdbadmin        | SqlUser | db\_owner     |

7. Poskytněte uživateli svc-AXSF$ a axdbadmin SQL přístup k následujícím rolím v databázi tempdb:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. V aplikaci Management Studio spusťte následující příkazy Transact SQL (T-SQL):

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Spusťte následující příkaz:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Konfigurujte databázi finančního výkaznictví

1.  Vytvořte prázdnou databázi s názvem **FinancialReporting**.
2.  Pomocí informací v tabulce namapujte uživatele a databázové role.

    | Uživatel             | Typ | Role databáze |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_owner     |
    | svc-FRPS$        | gMSA | db\_owner     |
    | svc-FRAS$        | gMSA | db\_owner     |

### <a name="encrypt-credentials"></a>Zašifrujte přístupové údaje

1. Na všechny klientské počítače instalujte šifrovací certifikát v úložišti certifikátů LocalMachine\\My.
2. Udělte aktuálnímu uživateli přístup pro čtení soukromého klíče tohoto certifikátu.
3. Vytvořte soubor Credentials.json, jak je uvedeno zde.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** je šifrované heslo uživatele domény pro uživatele domény AOS (contoso\\axserviceuser).
    - **SqlUser** je šifrovaný uživatel SQL (axdbadmin), který má přístup k databázi Finance and Operations (AXDBRAIN) a **SqlPassword** je šifrované heslo SQL.

4. Kopírujte soubor .json do sdílené SMB \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Aktualizujte soubor Credentials.json šifrovanými hodnotami.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. V Credentials.json, nahraďte **\<encryptedDomainUserPassword\>** šifrovaným heslem domény.
    2. Nahraďte **\<encryptedSqlUser\>** šifrovaným uživatelem SQL Finance and Operations.
    3. Nahraďte **\<encryptedSqlPassword\>** heslem pro SQL Finance and Operations.
    
### <a name="set-up-ssrs"></a>Nastavit SSRS

1.  Před zahájením práce se ujistěte, že jsou nainstalovány požadavky, které jsou uvedeny na začátku tohoto tématu.
2.  Postupujte dle [Konfigurace služby SQL Server Reporting Services pro místní nasazení](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>Konfigurace služby AD FS

Před provedením tohoto procesu musí být v systému Windows Server 2016 nasazeny AD FS. Informace o nasazení služby AD FS najdete v [Příručce nasazení systému Windows Server 2016 a Příručce nasazení 2012 R2 AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations vyžaduje další konfiguraci vedle výchozí tovární konfigurace AD FS. Pro následující kroky je spuštěno prostředí Windows PowerShell v počítači, ve kterém je nainstalována služba role AD FS. Uživatelský účet musí mít dostatečná oprávnění ke správě služby AD FS. Například uživatel musí mít účet správce domény.

1. Konfigurujte identifikátor služby AD FS tak, aby odpovídal vydavateli tokenu AD FS.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Není-li dokončena konfigurace služby AD FS pro smíšené prostředí, zakažte Windows Integrated Authentication (WIA) pro ověřovací připojení sítě intranet. Další informace o postupu při konfigurování WIA tak, aby mohl být použit s AD FS naleznete v tématu [Konfigurovat prohlížeče pro použití Windows Integrated Authentication (WIA) s AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Pro přihlášení e-mailová adresa uživatele musí být vstup přijatelného ověřování.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Aby AD FS důvěřovala aplikaci Finance and Operations pro výměnu ověřování, musí být zaregistrovány položky různých aplikací v AD FS v rámci skupiny aplikací AD FS. Pro urychlení procesu a redukci chyb můžete použít následující skript pro registraci. Kopírujte do počítače, ve kterém je nainstalována služba role AD FS, skript Publish-ADFSApplicationGroup.ps1 a adresář D365FO-OP. Potom spusťte skript pomocí účtu uživatele, jako je například účet správce, který má dostatečná oprávnění ke správě služby AD FS. Další informace o použití skriptu naleznete v dokumentaci, která je uvedena ve skriptu. Poznamenejte si ID klienta, které je uvedeno ve výstupu, protože tuto informaci budete potřebovat v LCS později.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

Konzole správy AD FS by měla vypadat jako na následujícím obrázku. Pro otevření správce serveru, klepněte na **Nástroje**\>**AD FS Management** a pak v dolní části stromového zobrazení na levé straně klepněte na **Skupiny aplikací**. Poklepáním na skupinu aplikací zobrazíte další informace.

![Vlastnosti skupiny aplikací](./media/OPSetup_05_ApplicatioGroupProperties.png)

Nakonec se, v rámci testu funkčnosti, ujistěte, že máte přístup konfigurační URL AD FS OpenID v uzlu Service Fabric typu **AOSNodeType** tak, že přejdete na stránky `https://<adfs-dns-name>/adfs/.well-known/openid-configuration`ve vašem webovém prohlížeči. Pokud se objeví zpráva oznamující, že stránky nejsou bezpečné, nepřidali jste certifikát AD FS SSL do úložiště Trusted Root Certification Authorities. Tento krok je popsán v příručce pro nasazení služby AD FS. Pokud na URL přistoupíte úspěšně, vrátí se soubor JavaScript Object Notation (JSON) obsahující konfigurace služby AD FS a uvidíte, že vaše URL AD FS je důvěryhodné.

Tímto je nastavení infrastruktury dokončeno. Následující části popisují jak přejít k [LCS](https://lcs.dynamics.com) pro nastavení vašeho konektoru nasadit váš Dynamics 365 do prostředí Finance and Operations.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konfigurace konektoru a instalace místního lokálního agenta

1. Přihlaste se k [LCS](https://lcs.dynamics.com/) a otevřete projekt místní implementace.
2. V hamburger menu klepněte na **Nastavení projektu**.

    ![Příkaz Nastavení projekt](./media/OPSetup_06_ProjectSettings.png)

3. Klepněte na **Místní konektory**.
4. Klepnutím na tlačítko **Přidat** vytvořte nový konektor.
5. Na kartě **Nastavení infrastruktury hostitele** stáhněte instalační program agenta.

    ![Stáhněte instalační program agenta na kartě Nastavení infrastruktury hostitele](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Ověřte, že soubor zip není blokován. Klepněte pravým tlačítkem myši na soubor, klepněte na tlačítko **Vlastnosti** a poté vyberte **Odblokovat**.
7. Rozbalte instalační program agenta na jednom z uzlů Service Fabric typu **OrchestratorType**.
8. Na kartě **Konfigurace agenta** zadejte konfigurační nastavení.
9. Uložte konfiguraci a klepněte na tlačítko **Stáhnout konfigurace** pro stažení konfiguračního souboru config.json.

    ![Stáhněte tlačítko konfigurace na kartě Konfigurace agenta.](./media/OPSetup_08_DownloadConfigurations.png)

10. Zkopírujte soubor localagent config.json do počítače, kde je umístěn instalační balíček agenta.
11. V okně příkazového řádku spusťte následující příkaz přechodem do složky, která obsahuje instalační program agenta.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Uživatel, který spustí tento příkaz, musí mít oprávnění **db\_owner** k databázi OrchestratorData.
    
12. Po úspěšné instalaci lokálního agenta přejděte zpět do vašeho místního konektoru v LCS.
13. Na kartě **Ověřit nastavení**, klepněte na tlačítko **Agent zpráv**. To otestuje LCS k vašemu lokálnímu agentu. Po úspěšném připojení bude stránka vypadat jako na obrázku níže.

     ![Ověřit agenta](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Nasaďte vaše prostředí Dynamics 365 pro prostředí Finance and Operations (místní)

1. Přejděte v LCS na místní projekt, jděte na **Prostředí**, **Sandbox** a klikněte na **Konfigurace**
2. Vyberte svoji **Topologii prostředí** a pomocí průvodce zahajte vaše nasazení.
3. Lokální agent převezme požadavek nasazení, zahájí nasazení a odešle zprávu zpět do LCS, až bude proces dokončen.

