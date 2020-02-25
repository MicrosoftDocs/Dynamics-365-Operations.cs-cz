---
title: Zřízení Human Resources
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3a7987a9b385fb6ba0294dc46b0d66be8228f06
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026260"
---
# <a name="provision-human-resources"></a>Zřízení Human Resources

Tento článek vás povede procesem zřízení nového produkčního prostředí pro aplikaci Microsoft Dynamics 365 Human Resources. Tento článek předpokládá, že jste si zakoupili aplikaci Human Resources prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Human Resources, a nedaří se vám provést kroky uvedené v tomto článku, kontaktujte podporu.

Pro začátek se musí globální správce přihlásit do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořit nový projekt aplikace Human Resources. Pokud vám v pořízení aplikace Human Resources nebrání problémy s licencí, není zapotřebí pomoc od zástupce služby Support or Dynamics Service Engineering (DSE).

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

2. Označte, zda se jedná o sandbox nebo produkční instanci aplikace Human Resources. Funkce předčasného náhledu mohou být k dispozici v instancích sandbox pro dřívější zpětnou vazbu a testování.
   
    > [!NOTE]
    > Typ instance Talent nelze po nastavení změnit. Před pokračováním ověřte, zda je vybrán správný typ instance.</br></br>
    > Typ instance aplikace Human Resources je oddělen od typu instance prostředí Microsoft Power Apps, který jste nastavili v centru správy Power Apps.
    
3. Pokud chcete, aby prostředí obsahovalo stejnou demonstrační datovou sadu, jaká se používá v prostředí zkušební ukázky aplikace Human Resources, zaškrtněte políčko **Zahrnout ukázková data**. To je vhodné pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemá používat pro výrobní prostředí.  Tuto možnost musíte zvolit při počátečním nasazení. Existující nasazení nelze aktualizovat později.

4. Aplikace Human Resources bude vždy zařazena v prostředí Microsoft Power Apps, aby byla možná integrace a rozšiřitelnost Power Apps. Než budete pokračovat, přečtěte si část Výběr prostředí Power Apps v tomto článku. Pokud již nemáte prostředí Power Apps, vyberte správu prostředí v LCS nebo přejděte do centra pro správu Power Apps. Poté postupujte podle kroků k [Vytvoření prostředí Power Apps](https://docs.microsoft.com/powerapps/administrator/create-environment).

    > [!NOTE]
    > K zobrazení existujících prostředí nebo vytváření nových prostředí musí být správce klienta zřizujícího aplikaci Human Resources přiřazen k licenci Power Apps P2. Pokud vaše organizace nemá Power Apps P2 licenci, můžete jednu získat ze svého CSP nebo ze stránky s cenami [Power Apps](https://powerapps.microsoft.com/pricing/).

5. Vyberte prostředí, do kterého chcete zřídit aplikaci Human Resources.

6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

   Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Human Resources**.

    > [!NOTE]
    > Pokud ještě nesplňujete všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Human Resources. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

    > Protože v rámci předplatného aplikace Human Resources jsou povolena pouze dvě prostředí LCS, můžete zvážit také využití 60denní zkušební verze [zkušební prostředí aplikace Human Resources](https://dynamics.microsoft.com/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Human Resources. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="select-a-power-apps-environment"></a>Výběr prostředí Power Apps

Integrace mezi prostředími aplikace Human Resources a Power Apps umožňuje integraci a rozšíření použití dat aplikace Human Resources pomocí nástrojů Power Apps. Pochopení účelu prostředí Power Apps vám umožní nejen vytvořit aplikace pro rozšíření aplikace Human Resources, ale také vybrat správné prostředí při zřizování aplikace Human Resources. Informace o prostředí Power Apps, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení prostředí Power Apps](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí Power Apps nasadit aplikaci Human Resources: 

1. V LCS vyberte **Prostředí pro správu** nebo přejděte přímo do centra pro správu Power Apps, ve kterém můžete zobrazit existující prostředí a vytvářet nová prostředí.

2. Jedno prostředí aplikace Human Resources je mapováno na jedno prostředí Power Apps.

3. Prostředí Power Apps obsahuje aplikaci Human Resources spolu s odpovídajícími aplikacemi Power Apps, Power Automate a Common Data Service. Je-li prostředí Power Apps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje. Při zřizování prostředí aplikace Human Resources můžete zřídit **zkušební** nebo **produkční** prostředí. Vyberte typ prostředí podle toho, jak bude prostředí používáno. 

4. Měly být zohledněny strategie integrace dat a testování, například Sandbox, UAT nebo výroba. Doporučujeme zvážit různé implikace na vaše nasazení, protože není snadné později změnit, které prostředí aplikace Human Resources je namapováno na prostředí Power Apps.

5. Následující prostředí Power Apps nelze použít pro aplikaci Human Resources a bude odfiltrováno ze seznamu voleb v rámci LCS:
 
    - **Výchozí prostředí Power Apps** - I když je každý klient automaticky vytvořen s výchozím prostředím Power Apps, nedoporučujeme je používat se systémem Human Resources, protože všichni uživatelé klientů mají přístup do prostředí Power Apps a mohou neúmyslně poškodit provozní data při testování a seznámení s integrací Power Apps nebo Power Automate.
   
    - **Zkušební prostředí** Tato prostředí jsou vytvářena s dobou platnosti a vyprší po uplynutí této doby, což způsobí, že prostředí a všechny obsažené instance aplikace Human Resources budou automaticky odebrány.
   
    - **Nepodporované oblasti** – Aplikace Human Resources je v současné době podporována pouze v následujících oblastech: Spojené státy, Evropa, Velká Británie, Austrálie, Kanada a Asie.
  
6. Po určení správného prostředí, které chcete použít, můžete pokračovat v procesu zřizování. 
 
## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí

Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, musíte přidat uživatele a přiřadit jim příslušné role v prostředí Human Resources. Globální správce, který nasadil aplikaci Human Resources, musí také spustit aplikaci Attract i Onboard k dokončení inicializace a povolit přístup pro ostatní uživatele klienta.  Dokud k tomu nedojde, ostatní uživatelé nebudou mít přístup do aplikací Attract a Onboard a získáte chyby narušení přístupu. Další informace naleznete v tématu [Vytvoření nových uživatelů](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
