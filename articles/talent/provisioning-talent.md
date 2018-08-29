---
title: "Zřízení aplikace Talent"
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
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 2fc4119f3b33aa583274f4d823e296752cdde41d
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="provision-talent"></a>Zřízení aplikace Talent

[!include [banner](includes/banner.md)]

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
5. Pokud chcete, aby prostředí obsahovalo stejnou datovou sadu, jaká se používá ve zkušenosti talentové zkušební jednotky, zaškrtněte políčko Zahrnout ukázková data.  To je vhodné pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemá používat pro výrobní prostředí.  Všimněte si, že musíte vybrat tuto možnost při původním nasazení a nemůžete aktualizovat později stávajícího nasazení.
6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

> [!NOTE]
> Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

> [!NOTE]
> Protože v rámci předplatného aplikace Talent jsou povolena pouze dvě prostředí LCS, můžete zvážit také využití 60denní zkušenbí verze [zkušební prostředí Talent](https://dynamics.microsoft.com/en-us/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Core HR. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

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

2. Ze složky stahování klepněte pravým tlačítkem myši na právě stažený soubor ProvisionCDSEnvironment.zip a vyberte **vlastnosti**.  Pokud se v dolní části dialogového okna Soubor pochází z jiného počítače a může být blokován pro ochranu tohoto počítače, zaškrtněte políčko **Odblokovat** a klepněte na tlačítko **použít** a pak **OK**.

3. Rozbalte celý obsah souboru ProvisionCDSEnviroinment.zip soubor do složky jiné než kořenové.

4. Spusťte program Windows PowerShell nebo Windows PowerShell ISE jako správce.

   Navštivte téma [Nastavení zásad spouštění](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) a dozvíte se více informací o zásadách spouštění, aby bylo možné spouštět skripty. Doporučujeme použití příkazu Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope Process, ale postupujte podle zásad zabezpečení vaší společnosti a po dokončení zavřete okno PowerShell. 
  
5. V prostředí PowerShell přejděte do složky, kde jste rozbalili soubor, a spusťte následující příkaz, s nahrazením hodnot podle pokynů níže:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** má být nahrazena názvem vašeho prostředí. Tento název se objeví v LCS a bude viditelný, když uživatel vybere prostředí Talent, které chce použít. 

   **YourLocation** má být nahrazena jednou z podporovaných oblasteí pro Talent: unitedstates, evropa, austrálie. 

   Volba **-Podrobné** je volitelná a poskytuje podrobné informace pro odeslání podpoře, když jsou zjištěny problémy.

6. Pokračujte v procesu zajištění.
 

## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí
Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, [přidáte uživatele](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [přiřadíte jim příslušné role](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) v prostředí Core HR. Globální správce, který nasadil aplikaci Talent, musí také spustit aplikaci Attract i Onboard k dokončení inicializace a povolit přístup pro ostatní uživatele klienta.  Dokud k tomu nedojde, ostatní uživatelé nebudou mít přístup do aplikací Attract a Onboard a získáte chyby narušení přístupu.


