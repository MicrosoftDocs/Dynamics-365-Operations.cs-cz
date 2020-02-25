---
title: Zřízení aplikace Talent
description: Toto téma vás povede procesem zřízení nového prostředí pro aplikaci Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 05/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d06c0d14fb99e5544a5da05078f5b3a559f9e806
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025502"
---
# <a name="provision-talent"></a>Zřízení aplikace Talent

Toto téma vás povede procesem zřízení nového produkčního prostředí pro aplikaci Dynamics 365 Talent. Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Talent, a nedaří se vám provést kroky uvedené v tomto tématu, kontaktujte podporu.

Pro začátek se musí globální správce má přihlásit do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořit nový projekt Talent. Pokud vám v pořízení aplikace Talent nebrání problémy s licencí, není zapotřebí pomoc od zástupce služby Support or Dynamics Service Engineering (DSE).

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu
Pokud chcete použít ke správě svého prostředí Talent službu LCS, musíte nejprve vytvořit LCS projekt.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.
2. Vyberte znaménko plus (**+**) a vytvořte projekt.
3. Vyberte **Microsoft Dynamics 365 Talent** jako název produktu a verzi produktu.
4. Výběr metodologie upgradování **Dynamics 365 Talent**.
5. Vyberte **Vytvořit**.

Více informací o zahájení práce s aplikací Talent naleznete v metodologii **Talent**, kterou jste vytvořili ve svém nové projektu. Po vytvoření projektu dokončete následující postup ke zřízení prostředí Talent.

## <a name="provision-a-talent-project"></a>Zřízení projektu Talent
Po vytvoření LCS projektu můžete vytvořit zařadit aplikaci Talent do prostředí.

1. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.
2. Označte, zda se jedná o sandbox nebo produkční instanci aplikace Talent. Funkce předčasného náhledu mohou být k dispozici v instancích sandbox pro dřívější zpětnou vazbu a testování. 

    > [!NOTE]
    > Typ instance Talent nelze po nastavení změnit. Před pokračováním ověřte, zda je vybrán správný typ instance.

    > [!NOTE]
    > Typ instance aplikace Talent je oddělen od typu instance prostředí Microsoft Power Apps, který jste nastavili v centru správy Power Apps.
3. Pokud chcete, aby prostředí obsahovalo stejnou datovou sadu, jaká se používá ve zkušenosti talentové zkušební jednotky, zaškrtněte políčko **Zahrnout ukázková data**. To je vhodné pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemá používat pro výrobní prostředí.  Tuto možnost musíte zvolit při počátečním nasazení. Existující nasazení nelze aktualizovat později.
4. Talent bude vždy zřízen v prostředí Microsoft Power Apps, aby byla možná integrace a rozšiřitelnost Power Apps. Než budete pokračovat, přečtěte si část Výběr prostředí Power Apps v tomto tématu. Pokud již nemáte prostředí Power Apps, vyberte správu prostředí v LCS nebo přejděte do centra pro správu Power Apps. Poté postupujte podle kroků k [Vytvoření prostředí Power Apps](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > K zobrazení existujících prostředí nebo vytváření nových prostředí musí být správce klienta zřizujícího aplikaci Talent přiřazen k licenci Power Apps P2. Pokud vaše organizace nemá Power Apps P2 licenci, můžete jednu získat ze svého CSP nebo ze stránky s cenami [Power Apps](https://powerapps.microsoft.com/pricing/).

5. Vyberte prostředí, do kterého chcete zřídit Talent.
6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

    > [!NOTE]
    > Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

    > Protože v rámci předplatného aplikace Talent jsou povolena pouze dvě prostředí LCS, můžete zvážit také využití 60denní zkušenbí verze [zkušební prostředí Talent](https://dynamics.microsoft.com/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Human Resources. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="select-a-power-apps-environment"></a>Výběr prostředí Power Apps

Integrace mezi prostředími Talent a Power Apps umožňuje integraci a rozšíření použití dat aplikace Talent pomocí nástrojů Power Apps. Pochopení účelu prostředí Power Apps vám umožní nejen vytvořit aplikace pro rozšíření aplikace Talent, ale také provést vybrat správné prostředí při zřizování aplikace Talent. Informace o prostředí Power Apps, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení prostředí Power Apps](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí Power Apps nasadit aplikaci Talent: 

1. V LCS vyberte **Prostředí pro správu** nebo přejděte přímo do centra pro správu Power Apps, ve kterém můžete zobrazit existující prostředí a vytvářet nová prostředí.
2. Jedno prostředí Talent je mapováno na jedno prostředí Power Apps.
3. Prostředí Power Apps obsahuje aplikaci Talent, spolu s odpovídajícími aplikacemi Power Apps, Power Automate a Common Data Service. Je-li prostředí Power Apps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje. Při zřizování prostředí Talent můžete zřídit **zkušební** nebo **produkční** prostředí. Vyberte typ prostředí podle toho, jak bude prostředí používáno. 
4. Měly být zohledněny strategie integrace dat a testování, například Sandbox, UAT nebo výroba. Doporučujeme zvážit různé implikace na vaše nasazení, protože není snadné později změnit, které prostředí Talent je namapováno na prostředí Power Apps.
5. Následující prostředí Power Apps nelze použít pro aplikaci Talent a bude odfiltrováno ze seznamu voleb v rámci LCS:
 
    - **Výchozí prostředí Power Apps** - I když je každý klient automaticky vytvořen s výchozím prostředím Power Apps, nedoporučujeme je používat se systémem Talent, protože všichni uživatelé klientů mají přístup do prostředí Power Apps a mohou neúmyslně poškodit provozní data při testování a seznámení s integrací Power Apps nebo Power Automate.
   
    - **Zkušební prostředí** Tato prostředí jsou vytvářena s dobou platnosti a vyprší po uplynutí této doby, což způsobí, že prostředí a všechny obsažené instance aplikace Talent budou odebrány automaticky.
   
    - **Nepodporované oblasti** - Talent je v současné době podporován pouze v následujících oblastech: Spojené státy, Evropa, Velká Británie, Austrálie, Kanada a Asie.
  
6. Po určení správného prostředí, které chcete použít, můžete pokračovat v procesu zřizování. 
 
## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí
Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, musíte přidat uživatele a přiřadit jim příslušné role v prostředí Human Resources. Globální správce, který nasadil aplikaci Talent, musí také spustit aplikaci Attract i Onboard k dokončení inicializace a povolit přístup pro ostatní uživatele klienta.  Dokud k tomu nedojde, ostatní uživatelé nebudou mít přístup do aplikací Attract a Onboard a získáte chyby narušení přístupu. Další informace naleznete v tématu [Vytvoření nových uživatelů](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
