---
title: Zřízení Human Resources
description: Toto téma vysvětluje proces zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b5ea27c6650df0b94284902eb37e2169ea36261a
ms.sourcegitcommit: f5fd2122a889b04e14f18184aabd37f4bfb42974
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/10/2022
ms.locfileid: "7952695"
---
# <a name="provision-human-resources"></a>Zřízení Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma vysvětluje proces zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources. 

## <a name="prerequisites"></a>Předpoklady

Aby bylo možné zřídit nové produkční prostředí, musí být splněny následující požadavky:

- Zakoupili jste si aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Human Resources, a nedaří se vám provést kroky uvedené v tomto tématu, kontaktujte podporu.

- Globální správce se přihlásil do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořil nový projekt aplikace Human Resources. 

## <a name="provision-a-human-resources-trial-environment"></a>Zřídit zkušební prostředí Human Resources

Před zřízením prvního sandboxu nebo produkčního prostředí můžete zřídit [Zkušební prostředí Human Resources](https://go.microsoft.com/fwlink/p/?LinkId=2115962) k ověření funkčnosti Human Resources. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Human Resources. 

Zkušební prostředí poskytují možnost vyhodnotit funkce lidských zdrojů u jednotlivců, kteří ještě nemají přístup k prostředí lidských zdrojů. Pokud zřizujete zkušební prostředí a ověřený uživatel již má přístup k jednomu nebo více existujícím prostředím lidských zdrojů, bude uživatel přesměrován do stávajícího prostředí nebo seznamu prostředí.

Zkušební prostředí nejsou určena k použití jako produkční prostředí. Jsou omezeny na 30denní zkušební dobu. Po vypršení zkušebního prostředí bude prostředí a všechna data v něm smazána a nelze je obnovit. Prostředí nelze převést na sandbox nebo produkční prostředí. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

Při vytváření zkušebního prostředí pro lidské zdroje je v klientovi také vytvořeno zkušební prostředí Power Apps a je propojeno s prostředím lidských zdrojů. Prostředí Power Apps s názvem „TestDrive“ má stejné zkušební období jako prostředí lidských zdrojů.

> [!NOTE]
> Zřízení zkušebního prostředí lidských zdrojů se nezdaří, pokud ověřený uživatel nemá oprávnění k vytváření zkušebního prostředí Power Apps. Uživatel musí být zařazen do skupiny uživatelů, kteří mohou vytvářet zkušební prostředí v centru pro správu Power Platform. Další informace viz [Řízení, kdo může vytvářet a spravovat prostředí v centru pro správu Power Platform](/power-platform/admin/control-environment-creation).

## <a name="plan-human-resources-environments"></a>Plánování prostředí Human Resources

Než vytvoříte své první prostředí Human Resources, měli byste pečlivě naplánovat potřeby prostředí pro váš projekt. Základní předplatné Human Resources zahrnuje dvě prostředí: produkční prostředí a prostředí karantény. V závislosti na složitosti vašeho projektu možná budete muset zakoupit další prostředí izolovaného prostoru pro podporu projektových aktivit. 

Doporučení pro další prostředí:

- **Migrace dat**: Možná budete muset zvážit další prostředí pro aktivity migrace dat, aby bylo možné vaše prostředí karantény použít pro účely testování v celém projektu. Mít další prostředí umožňuje, aby aktivity migrace dat pokračovaly, zatímco aktivity testování a konfigurace probíhají současně v jiném prostředí.
- **Integrace**: Možná budete muset zvážit další prostředí pro konfiguraci a testování integrace. To by mohlo zahrnovat nativní integrace, jako jsou integrace Ceridian Dayforce LinkedIn Talent Hub, nebo vlastní integrace, jako jsou integrace pro mzdy, systémy sledování žadatelů nebo systémy a poskytovatele výhod.
- **Výcvik**: Abyste mohli své zaměstnance vyškolit v používání nového systému, možná budete potřebovat samostatné prostředí, které je nakonfigurováno se sadou tréninkových dat. 
- **Vícefázový projekt** : Možná budete potřebovat další prostředí pro podporu konfigurace, migrace dat, testování nebo jiných aktivit ve fázi projektu, která je plánována po počátečním uvedení projektu do provozu.

 > [!IMPORTANT]
 > Při návrhu vašeho prostředí doporučujeme:
 > - Používat produkční prostředí v celém projektu jako prostředí konfigurace GOLD. To je důležité, protože nelze zkopírovat prostředí karantény do produkčního prostředí. Když tedy uvedete do provozu, vaše GOLD prostředí je vaše produkční prostředí, a v tomto prostředí dokončíte své činnosti přechodu.</br></br>
 > - Před zahájením provozu proveďte předstíraný odřezek pomocí sandboxu nebo jiného prostředí. Můžete to udělat obnovením produkčního prostředí s vaší konfigurací GOLD do prostředí karantény.</br></br>
 > - Ponechte si podrobný kontrolní seznam pro vystřihování, který zahrnuje každý z datových balíčků potřebných k migraci konečných dat do produkčního prostředí během zastávky.</br></br>
 > - Používat prostředí sandbox v celém projektu jako prostředí konfigurace TEST. Pokud potřebujete další prostředí, může si je vaše organizace za příplatek zakoupit.</br></br>

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu

Pokud chcete použít ke správě svého prostředí aplikace Human Resources službu LCS, musíte nejprve vytvořit LCS projekt.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Human Resources.

   > [!NOTE]
   > Aby bylo zajištěno úspěšné zřízení, účet, který používáte k zřízení prostředí Human Resources, musí být přiřazen buď roli **Správce systému**, nebo **Přizpůsobení systému** v prostředí Power Apps spojeném s prostředím Human Resources. Další informace o přiřazení rolí zabezpečení uživatelům v Power Platform získáte v části [Konfigurace zabezpečení uživatele u zdrojů](/power-platform/admin/database-security).

2. Vyberte znaménko plus (**+**) a vytvořte projekt.

3. Vyberte **Microsoft Dynamics 365 Human Resources** jako název produktu a verzi produktu.

4. Výběr metodologie upgradování **Dynamics 365 Human Resources**.

5. Vyberte **Vytvořit**.

Více informací o zahájení práce s aplikací Human Resources naleznete v metodologii **Human Resources**, kterou jste vytvořili ve svém novém projektu. Po vytvoření projektu dokončete následující postup ke zřízení prostředí aplikace Human Resources.

## <a name="provision-a-human-resources-project"></a>Zřízení projektu aplikace Human Resources

Po vytvoření LCS projektu můžete zařadit aplikaci Human Resources do prostředí.

1. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Human Resources**.

2. Označte, zda se jedná o prostředí sandbox nebo produkční instanci aplikace Human Resources. Funkce předčasného náhledu mohou být k dispozici v instancích sandbox pro dřívější zpětnou vazbu a testování.
   
    > [!NOTE]
    > Typ instance Human Resources nelze po nastavení změnit. Před pokračováním ověřte, zda je vybrán správný typ instance.</br></br>
    > Typ instance aplikace Human Resources je oddělen od typu instance prostředí Microsoft Power Apps, který jste nastavili v centru správy Power Apps.
    
3. Pokud chcete, aby prostředí obsahovalo stejnou demonstrační datovou sadu, jaká se používá ve zkušebním prostředí Human Resources, zaškrtněte políčko **Zahrnout ukázková data**. Ukázková data jsou vhodná pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemají používat pro výrobní prostředí. Tuto možnost musíte zvolit při počátečním nasazení. Existující nasazení nelze aktualizovat později.

4. Aplikace Human Resources bude vždy zařazena v prostředí Microsoft Power Apps, aby byla možná integrace a rozšiřitelnost Power Apps. Než budete pokračovat, přečtěte si část Výběr prostředí Power Apps v tomto článku. Pokud již nemáte prostředí Power Apps, vyberte správu prostředí v LCS nebo přejděte do centra pro správu Power Apps. Poté postupujte podle kroků k [Vytvoření prostředí Power Apps](/powerapps/administrator/create-environment).

5. Vyberte prostředí, do kterého chcete zřídit aplikaci Human Resources.

6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

   Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Human Resources**.

    > [!NOTE]
    > Pokud ještě nesplňujete všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Human Resources. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

## <a name="select-a-power-apps-environment"></a>Výběr prostředí Power Apps

Pomocí nástrojů Power Apps lze integrovat a rozšířit použití dat Human Resources. Informace o prostředí Power Apps, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení prostředí Power Apps](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí Power Apps nasadit aplikaci Human Resources: 

1. V LCS vyberte možnost **Spravovat prostředí**. Můžete také přímo přejít do Centra pro správu Power Apps, kde můžete zobrazit existující prostředí a vytvořit nová.

2. Jedno prostředí aplikace Human Resources je mapováno na jedno prostředí Power Apps.

3. Prostředí Power Apps obsahuje aplikaci Human Resources spolu s odpovídajícími aplikacemi Power Apps, Power Automate a Dataverse. Je-li prostředí Power Apps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje. Při zřizování prostředí aplikace Human Resources můžete zřídit **zkušební** nebo **produkční** prostředí. Vyberte typ prostředí podle toho, jak bude prostředí používáno. 

4. Měly být zohledněny strategie integrace dat a testování, například Sandbox, UAT nebo výroba. Pečlivě zvažte implikace pro vaše nasazení, protože není snadné později změnit, které prostředí aplikace Human Resources je namapováno na prostředí Power Apps.

5. V aplikaci Human Resources nelze použít následující prostředí Power Apps. Jsou filtrovány ze seznamu výběru v rámci LCS:
 
    - **Výchozí prostředí Power Apps** – zatímco každý klient je automaticky zřízen ve výchozím prostředí Power Apps, nedoporučujeme je používat s Human Resources. Všichni uživatelé klienta mají přístup k prostředí Power Apps a mohou neúmyslně poškodit výrobní data při testování a procházení pomocí integrací Power Apps nebo Power Automate.
   
    - **Zkušební prostředí** – tato prostředí jsou vytvářena s datem vypršení platnosti. Po vypršení platnosti bude automaticky odebráno vaše prostředí a všechny instance Human Resources, které jsou v něm obsaženy.
   
    - **Nepodporované zeměpisné oblasti** – Prostředí musí být v podporované geografii. Další informace viz [Podporované zeměpisné oblasti](hr-admin-setup-provision.md#supported-geographies).

6. Možnosti duálního zápisu pro integraci dat lidských zdrojů s prostředím Power Apps lze použít pouze v případě, kdy je vybrána možnost **Povolit aplikace Dynamics 365** pro prostředí. V tématu [Domovská stránka pro duální zápis](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md) získáte více informací o duálním zápisu.

    > [!NOTE]
    > Možnost **Povolit aplikace Dynamics 365** musí být vybrána během vytváření prostředí Power Apps. Pokud tato možnost není v době zřízení vybrána, nebudete moci používat duální zápis k integraci dat mezi Dynamics 365 Human Resources a prostředím Power Apps ani instalovat do prostředí aplikace Dynamics 365, jako je Dynamics 365 Sales a Field Service. Tato možnost není reverzibilní. Další informace viz [Některé důležité úvahy při vytváření nového prostředí](//power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) na webu dokumentace Power Platform.

7. Po určení správného prostředí, které chcete použít, můžete pokračovat v procesu zřizování. 

### <a name="supported-geographies"></a>Podporované zeměpisné oblasti

Human Resources v současné době podporují následující zeměpisné oblasti:

- Spojené státy americké
- Evropa
- Spojené království
- Austrálie
- Kanada
- Asie 

Když vytváříte prostředí Human Resources, vyberete prostředí Power Apps ke spojení s prostředím Human Resources. Prostředí Human Resources je poté zřízeno ve stejné geografii Azure jako vybrané prostředí Power Apps. Můžete vybrat, kde se prostředí Human Resources a databáze fyzicky nacházejí, výběrem geografie při vytváření prostředí Power Apps, které bude spojeno s prostředím Human Resources.

Můžete vybrat *zeměpisnou oblast* Azure, ve které je zajištěno prostředí, ale nemůžete vybrat konkrétní *region* Azure. Automatizace určuje konkrétní oblast v geografii, ve které je prostředí vytvořeno, aby optimalizovalo vyvažování zátěže a výkon. Informace o geografických oblastech a oblastech Azure najdete v dokumentaci na [Zeměpisné oblasti Azure](https://azure.microsoft.com/global-infrastructure/geographies).

Data pro prostředí Human Resources budou vždy obsažena v geografii Azure, ve které je vytvořena. Nebude však vždy obsažen ve stejné oblasti Azure. Pro účely zotavení po havárii budou data replikována jak v primárním regionu Azure, tak v sekundární oblasti převzetí služeb při selhání v rámci geografie.

 > [!NOTE]
 > Migrace prostředí Human Resources z jednoho regionu Azure do jiného není podporována.

## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí

Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musíte explicitně udělit přístup. Musíte přidat uživatele a přiřadit jim příslušné role v prostředí Human Resources. Další informace naleznete v tématu [Vytvoření nových uživatelů](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
