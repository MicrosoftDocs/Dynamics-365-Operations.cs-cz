---
title: Zřízení aplikace Talent
description: Toto téma vás povede procesem zřízení nového prostředí pro aplikaci Dynamics 365 for Talent.
author: andreabichsel
manager: AnnBe
ms.date: 00/05/2019
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
ms.openlocfilehash: 98f60e466b8b97215fdba0f48ca53ca57157283b
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/12/2019
ms.locfileid: "969367"
---
# <a name="provision-talent"></a>Zřízení aplikace Talent

[!include [banner](includes/banner.md)]

Toto téma vás povede procesem zřízení nového produkčního prostředí pro aplikaci Dynamics 365 for Talent. Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Talent, a nedaří se vám provést kroky uvedené v tomto tématu, kontaktujte podporu.

Pro začátek se musí globální správce má přihlásit do služby [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) a vytvořit nový projekt Talent. Pokud vám v pořízení aplikace Talent nebrání problémy s licencí, není zapotřebí pomoc od zástupce služby Support or Dynamics Service Engineering (DSE).

## <a name="create-an-lcs-project"></a>Vytvoření LCS projektu
Pokud chcete použít ke správě svého prostředí Talent službu LCS, musíte nejprve vytvořit LCS projekt.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index) pomocí účtu, který jste použili pro přihlášení se k odběru aplikace Talent.
2. Vyberte znaménko plus (**+**) a vytvořte projekt.
3. Vyberte **Microsoft Dynamics 365 for Talent** jako název produktu a verzi produktu.
4. Výběr metodologie upgradování **Dynamics 365 for Talent**.
5. Vyberte **Vytvořit**.

Více informací o zahájení práce s aplikací Talent naleznete v metodologii **Talent**, kterou jste vytvořili ve svém nové projektu. Po vytvoření projektu dokončete následující postup ke zřízení prostředí Talent.

## <a name="provision-a-talent-project"></a>Zřízení projektu Talent
Po vytvoření LCS projektu můžete vytvořit zařadit aplikaci Talent do prostředí.

1. Ve svém LCS projektu vyberte dlaždici **Správa aplikace Talent**.
2. Talent bude vždy zřízen v prostředí Microsoft PowerApps, aby byla možná integrace a rozšiřitelnost PowerApps. Než budete pokračovat, přečtěte si část Výběr prostředí PowerApps v tomto tématu. Pokud již nemáte prostředí PowerApps, vyberte správu prostředí v LCS nebo přejděte do centra pro správu PowerApps. Poté postupujte podle kroků k [Vytvoření prostředí PowerApps](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > K zobrazení existujících prostředí nebo vytváření nových prostředí musí být správce klienta zřizujícího aplikaci Talent přiřazen k licenci PowerApps P2. Pokud vaše organizace nemá PowerApps P2 licenci, můžete jednu získat ze svého CSP nebo ze [stránky s cenami PowerApps](https://powerapps.microsoft.com/en-us/pricing/).

4. Vyberte **Přidat**a poté vyberte prostředí, do kterého chcete aplikaci Talent zřídit.
5. Pokud chcete, aby prostředí obsahovalo stejnou datovou sadu, jaká se používá ve zkušenosti talentové zkušební jednotky, zaškrtněte políčko **Zahrnout ukázková data**. To je vhodné pro dlouhodobá demonstrační nebo školicí prostředí a nikdy se nemá používat pro výrobní prostředí.  Tuto možnost musíte zvolit při počátečním nasazení. Existující nasazení nelze aktualizovat později.
6. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

7. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

    > [!NOTE]
    > Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

    > Protože v rámci předplatného aplikace Talent jsou povolena pouze dvě prostředí LCS, můžete zvážit také využití 60denní zkušenbí verze [zkušební prostředí Talent](https://dynamics.microsoft.com/en-us/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Core HR. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="select-a-powerapps-environment"></a>Vyberte prostředí PowerApps.

Integrace mezi prostředími Talent a PowerApps umožňuje integraci a rozšíření použití dat aplikace Talent pomocí nástrojů PowerApps. Pochopení účelu prostředí PowerApps vám umožní nejen vytvořit aplikace pro rozšíření aplikace Talent, ale také provést vybrat správné prostředí při zřizování aplikace Talent. Informace o PowerApps prostředí, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení PowerApps prostředí](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Použijte následující pokyny při určování, do kterého prostředí PowerApps nasadit aplikaci Talent: 

1. V LCS vyberte **Prostředí pro správu** nebo přejděte přímo do centra pro správu PowerApps, ve kterém můžete zobrazit existující prostředí a vytvářet nová prostředí.
2. Jedno prostředí Talent je mapováno na jedno prostředí PowerApps.
3. Prostředí PowerApps "obsahuje" aplikaci Talent, spolu s odpovídajícími aplikacemi PowerApps, Flow a Common Data Service. Je-li prostředí PowerApps odstraněno, jsou s ním odstraněny i aplikace, které obsahuje. Při zřizování prostředí Talent lze zřídit buď zkušební nebo produkční prostředí. Vyberte typ prostředí podle toho, jak bude prostředí používáno. 
4. Měly být zohledněny strategie integrace dat a testování, například Sandbox, UAT nebo výroba. Doporučujeme zvážit různé implikace na vaše nasazení, protože není snadné později změnit, které prostředí Talent je namapováno na prostředí PowerApps.
5. Následující prostředí PowerApps nelze použít pro aplikaci Talent a bude odfiltrováno ze seznamu voleb v rámci LCS:
 
    - **Výchozí prostředí Power Apps** I když je každý klient automaticky vytvořen s výchozím prostředím PowerApps, nedoporučujeme je používat se systémem Talent, protože všichni uživatelé klientů mají přístup do prostředí PowerApps a mohou neúmyslně poškodit data výroby při testování a seznámení s integrací PowerApps nebo Flow.
   
    - **Zkušební prostředí** Tato prostředí jsou vytvářena s dobou platnosti a vyprší po uplynutí této doby, což způsobí, že prostředí a všechny obsažené instance aplikace Talent budou odebrány automaticky.
   
    - **Nepodporované oblasti** - Talent je v současné době podporován pouze v následujících oblastech: Spojené státy, Evropa, Velká Británie nebo Austrálie.
  
6. Po určení správného prostředí, které chcete použít, můžete pokračovat v procesu zřizování. 
 
## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí
Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, musíte přidat uživatele a přiřadit jim příslušné role v prostředí Core HR. Globální správce, který nasadil aplikaci Talent, musí také spustit aplikaci Attract i Onboard k dokončení inicializace a povolit přístup pro ostatní uživatele klienta.  Dokud k tomu nedojde, ostatní uživatelé nebudou mít přístup do aplikací Attract a Onboard a získáte chyby narušení přístupu. Další informace naleznete v tématu [Vytvoření nových uživatelů](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) a [Přiřazení uživatelů k rolím zabezpečení](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
