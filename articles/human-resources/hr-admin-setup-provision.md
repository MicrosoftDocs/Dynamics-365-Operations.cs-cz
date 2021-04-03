---
title: Zřízení Human Resources
description: Tento článek vás povede procesem zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 43aacf454d6a2c9eb8cda5bb54a2bf8e8965070d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466873"
---
# <a name="provision-human-resources"></a>Zřízení Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tento článek vás povede procesem zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources. Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Human Resources, a nedaří se vám provést kroky uvedené v tomto článku, kontaktujte podporu.

Pro začátek se musí globální správce přihlásit do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořit nový projekt aplikace Human Resources. Pokud vám v pořízení aplikace Human Resources nebrání problémy s licencí, není zapotřebí pomoc od zástupce služby Support or Dynamics Service Engineering (DSE).

## <a name="plan-human-resources-environments"></a>Plánování prostředí Human Resources

Než vytvoříte své první prostředí Human Resources, měli byste pečlivě naplánovat potřeby prostředí pro váš projekt. Základní předplatné Human Resources zahrnuje dvě prostředí: produkční prostředí a prostředí karantény. V závislosti na složitosti vašeho projektu možná budete muset zakoupit další prostředí izolovaného prostoru pro podporu projektových aktivit. 

Mezi aspekty pro další prostředí patří mimo jiné následující:

- **Migrace dat**: Možná budete muset zvážit další prostředí pro aktivity migrace dat, aby bylo možné vaše prostředí karantény použít pro účely testování v celém projektu. Mít další prostředí umožňuje, aby aktivity migrace dat pokračovaly, zatímco aktivity testování a konfigurace probíhají současně v jiném prostředí.
- **Integrace**: Možná budete muset zvážit další prostředí pro konfiguraci a testování integrace. To by mohlo zahrnovat nativní integrace, jako jsou integrace Ceridian Dayforce LinkedIn Talent Hub, nebo vlastní integrace, jako jsou integrace pro mzdy, systémy sledování žadatelů nebo systémy a poskytovatele výhod.
- **Výcvik**: Abyste mohli své zaměstnance vyškolit v používání nového systému, možná budete potřebovat samostatné prostředí, které je nakonfigurováno se sadou tréninkových dat. 
- **Vícefázový projekt** : Možná budete potřebovat další prostředí pro podporu konfigurace, migrace dat, testování nebo jiných aktivit ve fázi projektu, která je plánována po počátečním uvedení projektu do provozu.

 > [!IMPORTANT]
 > Doporučujeme používat produkční prostředí v celém projektu jako prostředí konfigurace GOLD. To je důležité, protože nelze zkopírovat prostředí karantény do produkčního prostředí. Když tedy uvedete do provozu, vaše GOLD prostředí je vaše produkční prostředí, a v tomto prostředí dokončíte své činnosti přechodu.</br></br>
 > Doporučujeme, abyste před zahájením provozu provedli předstíraný odřezek pomocí sandboxu nebo jiného prostředí. Můžete to udělat obnovením produkčního prostředí s vaší konfigurací GOLD do prostředí karantény.</br></br>
 > Doporučujeme, abyste si nechali podrobný kontrolní seznam pro vystřihování, který zahrnuje každý z datových balíčků potřebných k migraci konečných dat do produkčního prostředí během zastávky.</br></br>
 > Také doporučujeme používat sandbox prostředí v celém projektu jako prostředí konfigurace TEST. Pokud potřebujete další prostředí, může si je vaše organizace za příplatek zakoupit.</br></br>

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu

Pokud chcete použít ke správě svého prostředí aplikace Human Resources službu LCS, musíte nejprve vytvořit LCS projekt.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Human Resources.

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
    
3. Pokud chcete, aby prostředí obsahovalo stejnou demonstrační datovou sadu, jaká se používá v prostředí zkušební ukázky aplikace Human Resources, zaškrtněte políčko **Zahrnout ukázková data**. Ukázková data jsou vhodná pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemají používat pro výrobní prostředí. Tuto možnost musíte zvolit při počátečním nasazení. Existující nasazení nelze aktualizovat později.

4. Aplikace Human Resources bude vždy zařazena v prostředí Microsoft Power Apps, aby byla možná integrace a rozšiřitelnost Power Apps. Než budete pokračovat, přečtěte si část Výběr prostředí Power Apps v tomto článku. Pokud již nemáte prostředí Power Apps, vyberte správu prostředí v LCS nebo přejděte do centra pro správu Power Apps. Poté postupujte podle kroků k [Vytvoření prostředí Power Apps](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Vyberte prostředí, do kterého chcete zřídit aplikaci Human Resources.

6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

   Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Human Resources**.

    > [!NOTE]
    > Pokud ještě nesplňujete všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Human Resources. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

    > Můžete zvážit využití [zkušebního prostředí Human Resources](https://go.microsoft.com/fwlink/p/?LinkId=2115962) zdarma na 60 dní. Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Human Resources. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="select-a-power-apps-environment"></a>Výběr prostředí Power Apps

Pomocí nástrojů Power Apps lze integrovat a rozšířit použití dat Human Resources. Informace o prostředí Power Apps, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení prostředí Power Apps](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí Power Apps nasadit aplikaci Human Resources: 

1. V LCS vyberte možnost **Spravovat prostředí**. Můžete také přímo přejít do Centra pro správu Power Apps, kde můžete zobrazit existující prostředí a vytvořit nová.

2. Jedno prostředí aplikace Human Resources je mapováno na jedno prostředí Power Apps.

3. Prostředí Power Apps obsahuje aplikaci Human Resources spolu s odpovídajícími aplikacemi Power Apps, Power Automate a Dataverse. Je-li prostředí Power Apps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje. Při zřizování prostředí aplikace Human Resources můžete zřídit **zkušební** nebo **produkční** prostředí. Vyberte typ prostředí podle toho, jak bude prostředí používáno. 

4. Měly být zohledněny strategie integrace dat a testování, například Sandbox, UAT nebo výroba. Pečlivě zvažte implikace pro vaše nasazení, protože není snadné později změnit, které prostředí aplikace Human Resources je namapováno na prostředí Power Apps.

5. Pro Human Resources nelze použít následující prostředí Power Apps. Jsou filtrovány ze seznamu výběru v rámci LCS:
 
    - **Výchozí prostředí Power Apps** – zatímco každý klient je automaticky zřízen ve výchozím prostředí Power Apps, nedoporučujeme je používat s Human Resources. Všichni uživatelé klienta mají přístup k prostředí Power Apps a mohou neúmyslně poškodit výrobní data při testování a procházení pomocí integrací Power Apps nebo Power Automate.
   
    - **Zkušební prostředí** – tato prostředí jsou vytvářena s datem vypršení platnosti. Po vypršení platnosti bude automaticky odebráno vaše prostředí a všechny instance Human Resources, které jsou v něm obsaženy.
   
    - **Nepodporované oblasti** – Aplikace Human Resources je v současné době podporována pouze v následujících oblastech: Spojené státy, Evropa, Spojené království, Austrálie, Kanada a Asie.

    > [!NOTE]
    > Prostředí Human Resources je zajišťováno ve stejné oblasti, v níž je prostředí Power Apps zajišťováno. Migrace prostředí Human Resources do jiné oblasti není podporována.

6. Po určení správného prostředí, které chcete použít, můžete pokračovat v procesu zřizování. 
 
## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí

Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musíte explicitně udělit přístup. Musíte přidat uživatele a přiřadit jim příslušné role v prostředí Human Resources. Globální správce, který nasadil aplikaci Human Resources, musí také spustit aplikaci Attract i Onboard k dokončení inicializace a povolit přístup pro ostatní uživatele klienta. Dokud k tomu nedojde, ostatní uživatelé nebudou mít přístup do aplikací Attract a Onboard a získáte chyby narušení přístupu. Další informace naleznete v tématu [Vytvoření nových uživatelů](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]