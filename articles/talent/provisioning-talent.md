---
title: "Zřízení Microsoft Dynamics 365 for Talent"
description: "Toto téma vás povede procesem zřízení nového prostředí pro aplikaci Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b4b54e97bdebc158adc3bc6d57a6661cd536f5fb
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Zřízení Microsoft Dynamics 365 for Talent

[!INCLUDE [banner](includes/banner.md)]

Toto téma vás povede procesem zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 for Talent. Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Talent, a nedaří se vám provést kroky uvedené v tomto tématu, kontaktujte podporu.

Pro začátek se musí globální správce má přihlásit do služby [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) a vytvořit nový projekt Talent. Pokud vám v pořízení aplikace Talent nebrání problémy s licencí, není zapotřebí pomoc od zástupce služby Support or Dynamics Service Engineering (DSE).

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu
Pokud chcete použít ke správě svého prostředí Talent službu LCS, musíte nejprve vytvořit LCS projekt.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.
2. Vyberte znaménko plus (**+**) a vytvořte projekt.
3. Vyberte **Microsoft Dynamics 365 pro Talent** jako název produktu a verzi produktu.
4. Vyberte metodologii **Dynamics 365 pro Talent**.
5. Vyberte **Vytvořit**.

Více informací o zahájení práce s aplikací Talent naleznete v metodologii **Talent**, kterou jste vytvořili ve svém nové projektu. Po vytvoření projektu dokončete následující postup ke zřízení prostředí Talent.

## <a name="provision-a-talent-project"></a>Zřízení projektu Talent
Po vytvoření LCS projektu můžete vytvořit zařadit aplikaci Talent do prostředí.

1. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.
2. Talent bude vždy zřízen do prostředí Microsoft PowerApps, aby byla možná integrace a rozšiřitelnost PowerApps. Než budete pokračovat, přečtěte si část Výběr prostředí PowerApps v tomto tématu. 
3. Pokud ještě nemáte PowerApps prostředí, postupujte podle kroků v části „Vytvoření nového prostředí PowerApps (je-li to zapotřebí)“ tohoto tématu, než budete pokračovat.

    > [!NOTE]
    > K zobrazení existujících prostředí nebo vytváření nových prostředí musí být správce klienta zřizujícího aplikaci Talent přiřazen k licenci PowerApps P2. Pokud vaše organizace nemá PowerApps P2 licenci, můžete jednu získat ze svého CSP nebo ze [stránky s cenami PowerApps](https://powerapps.microsoft.com/en-us/pricing/).

4. Vyberte **Přidat**a poté vyberte prostředí, do kterého chcete aplikaci Talent zřídit.
5. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

6. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

> [!NOTE]
> Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

> [!NOTE]
> Prostředí Talent, která jsou vytvořena prostřednictvím LCS, neobsahují ukázková data konfigurovaná pro úkoly lidských zdrojů nebo týkající se konkrétně aplikace Talent. Chcete-li prostředí, které obsahuje ukázková data, doporučujeme, abyste se přihlásili k bezplatnému 60-dennímu [zkušebnímu prostředí Talent](https://dynamics.microsoft.com/en-us/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Core HR. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="select-a-powerapps-environment"></a>Vyberte prostředí PowerApps.

Integrace mezi prostředími Talent a PowerApps umožňuje integraci a rozšíření použití dat aplikace Talent pomocí nástrojů PowerApps. Pochopení účelu prostředí PowerApps vám umožní nejen vytvořit aplikace pro rozšíření aplikace Talent, ale také provést vybrat správné prostředí při zřizování aplikace Talent. Informace o PowerApps prostředí, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení PowerApps prostředí](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí PowerApps nasadit aplikaci Talent: 
1. V LCS vyberte Prostředí pro správu nebo přejděte přímo do centra pro správu PowerApps, ve kterém můžete zobrazit existující prostředí a vytvářet nová prostředí.
2. Jedno prostředí Talent je mapováno na jedno prostředí PowerApps.
3. Prostředí PowerApps "obsahuje" aplikaci Talent, spolu s odpovídajícími aplikacemi PowerApps, Flow a CDS. Je-li prostředí PowerApps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje.
4. Měly být zohledněny strategie integrace dat a testování, například: Sandbox, UAT, výroba. Proto doporučujeme zvážit různé implikace na vaše nasazení, protože není snadné později změnit, které prostředí Talent je namapováno na prostředí PowerApps.
5. Následující prostředí PowerApps nelze použít pro aplikaci Talent a bude odfiltrováno ze seznamu voleb v rámci LCS:
 
    **Prostředí CDS 2.0** CDS 2.0 budou veřejně k dispozici od 21. března 2018; systém Talent však ještě nepodporuje CDS 2.0. I když můpžete vytvářet a zobrazit databáze CDS 2.0 v centru správy PowerApps, nebude je možné použít v aplikaci Talent. Možnost použít prostředí CDS 2.0 v nasazeních aplikace Talent bude k dispozici k pozdějšímu datu.
   
   > [!Note]
   > Chcete-li rozlišit mezi prostředími CDS 1.0 a CDS 2.0 na portálu správy, zvolte prostředí a podívejte se na **Podrobnosti**. Všechna prostředí CDS 2.0 odkazují na skutečnost, že "Můžete spravovat tato nastavení v centru pro správu Dynamics 365," odkazovat na verzi instance a nemít žádnou kartu Databáze. 
 
   **Výchozí prostředí Power Apps** I když je každý klient automaticky vytvořen s výchozím prostředím PowerApps, nedoporučujeme je používat se systémem Talent, protože všichni uživatelé klientů mají přístup do prostředí PowerApps a mohou neúmyslně poškodit data výroby při testování a seznámení s integrací PowerApps nebo Flow.
   
   <strong>Testovací jednotka prostředí</strong> Prostředí nazvaná například "TestDrive – alias@domain' jsou vytvářena s dobou platnosti 60 dní a vyprší po uplynutí této doby, což způsobí, že prostředí bude odebráno automaticky.
   
   **Nepodporované oblasti** Talent je v současné době podporován pouze v následujících oblastech: Spojené státy, Evropa a Austrálie.
  
6. Neexistuje žádná konkrétní akce k provedení po určení správného prostředí k použití. Pokračujte v procesu zajištění. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Vytvoření nového prostředí PowerApps prostředí (je-li požadováno)

Spusťte skript PowerShell pro vytvoření nového prostředí PowerApps pro aplikaci Talent v kontextu správce klienta, který má licenci PowerApps Plan 2. Skript automatizuje následující kroky:


 + Vytvoření prostředí PowerApps
 + Vytvoření databáze CDS 1.0
 + Vymazat všechny ukázková data v databázi CD 1.0


Při spuštění skriptu postupujte následujícím způsobem:

1. Stáhněte soubor ProvisionCDSEnvironment.zip z následujícího umístění: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Rozbalte celý obsah souboru ProvisionCDSEnviroinment.zip soubor do složky.

3. Spusťte program Windows PowerShell nebo Windows PowerShell ISE jako správce.

   Navštivte téma [Nastavení zásad spouštění](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) a dozvíte se více informací o zásadách spouštění, aby bylo možné spouštět skripty.
  
4. V prostředí PowerShell přejděte do složky, kde jste rozbalili soubor, a spusťte následující příkaz, s nahrazením hodnot podle pokynů níže:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** má být nahrazena názvem vašeho prostředí. Tento název se objeví v LCS a bude viditelný, když uživatel vybere prostředí Talent, které chce použít. 

   **YourLocation** má být nahrazena jednou z podporovaných oblasteí pro Talent: unitedsates, evropa, austrálie. 

   Volba **-Podrobné** je volitelná a poskytuje podrobné informace pro odeslání podpoře, když jsou zjištěny problémy.

5. Pokračujte v procesu zajištění.
 


## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí
Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, [přidáte uživatele](../dev-itpro/sysadmin/tasks/create-new-users.md) a [přiřadíte jim příslušné role](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) v prostředí Core HR. Je také nutné přidat tyto uživatele do prostředí PowerApps, aby měli přístup k aplikacím Attract a Onboard. Postup je popsán zde. Jestliže požadujete pomoc k dokončení kroků, přečtěte si příspěvek blogu [Představení centra správy PowerApps](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Dokončení tohoto postupu provede globální správce, který nasadil prostředí Talent.

1. Otevřete [Centrum správy PowerApps](https://preview.admin.powerapps.com/environments).
2. Zvolte příslušná prostředí.
3. Na kartě **Zabezpečení** přidejte požadované uživatele k roli **Tvůrce prostředí**.

    Všimněte si, že tento poslední krok manuálního přidání uživatelů do prostředí PowerApps je dočasný. Popřípadě bude dokončen automaticky po přidání uživatelů do Core HR.

