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
ms.sourcegitcommit: 8b59ea6a2ac8c1c4e5df6e251fa3390639ff3f30
ms.openlocfilehash: e6266ef5890b5caaf33db76eeccfc8a7a6888a11
ms.contentlocale: cs-cz
ms.lasthandoff: 03/01/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Zřízení Microsoft Dynamics 365 for Talent

[!include[banner](includes/banner.md)]

[!include[banner](includes/banner.md)]

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
2. Talent bude vždy zřízen do prostředí Microsoft PowerApps, aby byla možná integrace a rozšiřitelnost PowerApps. Pokud ještě nemáte PowerApps prostředí, postupujte podle kroků v části „Vytvoření nového prostředí PowerApps (je-li to zapotřebí)“ tohoto tématu, než budete pokračovat.

    > [!NOTE]
    > K zobrazení existujících prostředí nebo vytváření nových prostředí musí být správce klienta zřizujícího aplikaci Talent přiřazen k licenci PowerApps P2. Pokud vaše organizace nemá PowerApps P2 licenci, můžete jednu získat ze svého CSP nebo ze [stránky s cenami PowerApps](https://powerapps.microsoft.com/en-us/pricing/).

3. Vyberte **Přidat**a poté vyberte prostředí, do kterého chcete aplikaci Talent zřídit.
4. K odsouhlasení smluvních podmínek vyberte **Ano** a začněte s nasazením.

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud není proces zřízení úspěšný, musíte kontaktovat podporu.

6. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

> [!NOTE]
> Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

> [!NOTE]
> Prostředí Talent, která jsou vytvořena prostřednictvím LCS, neobsahují ukázková data konfigurovaná pro úkoly lidských zdrojů nebo týkající se konkrétně aplikace Talent. Chcete-li prostředí, které obsahuje ukázková data, doporučujeme, abyste se přihlásili k bezplatnému 60-dennímu [zkušebnímu prostředí Talent](https://dynamics.microsoft.com/en-us/talent/overview/). Přestože zkušební prostředí je vlastněno uživatelem, který o něj požádal, mohou být jiní uživatelé pozváni prostřednictvím rozhraní správy pro Core HR. Zkušební prostředí obsahují fiktivní data, která slouží k bezpečnému prohlížení programu. Nejsou určena k použití jako produkční prostředí. Mějte na paměti, že po vypršení zkušebního prostředí po 60 dnech budou všechna data v prostředí smazána a nelze je obnovit. Můžete se zaregistrovat k novému zkušebnímu prostředí po vypršení platnosti existujícího prostředí.

## <a name="create-a-new-powerapps-environment-if-required"></a>Vytvoření nového prostředí PowerApps prostředí (je-li požadováno)
Integrace mezi prostředími Talent a PowerApps umožňuje integraci a rozšíření použití dat aplikace Talent pomocí nástrojů PowerApps. Pochopení účelů prostředí PowerApps vám pomůže sestavit aplikace, které splňují vaše potřeby rozšíření aplikace Talent. Informace o PowerApps prostředí, včetně rozsahu prostředí, přístupu k prostředí a k vytváření a volbě prostředí naleznete v tématu [Oznámení PowerApps prostředí](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). Zatímco každý klient je automaticky zřízen ve výchozím prostředí PowerApps, nemusí to být nejlepší prostředí pro nasazení aplikace Talent. Během tohoto kroku by se měly zvážit integrace dat a testovací strategie. Doporučujeme tedy zvážit implikace, které mohou mít dopad na vaše nasazení, protože není snadné později některá rozhodnutí změnit. 

Ačkoliv každý klient je automaticky zřízen ve výchozím prostředí PowerApps, nemusí to být nejlepší prostředí pro nasazení aplikace Talent. Integrace dat a testovací strategie by měly být během tohoto kroku zváženy. Proto doporučujeme zvážit různé implikace na vaše nasazení, protože není snadné prostředí PowerApps později změnit.

1. Vyberte možnost **Spravovat prostředí** v LCS. Budete nasměrováni na [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/environments), kde můžete zobrazit existující prostředí a vytvořit nová prostředí.
2. Vyberte **Nové prostředí**.
3. Zadání jedinečný název prostředí a vyberte umístění, do kterého ho chcete nasadit.

    > [!NOTE]
    > Talent není k dispozici ve všech oblastech. Nezapomeňte ověřit dostupnost před výběrem umístění vašeho prostředí.

4. Když se objeví dotaz, zda chcete vytvořit databázi, vyberte **Vytvořit databázi** pro vytvoření databáze služby Common Data Service, která musí být hostitelem části vašich dat aplikace Talent Vytvořením databáze také můžete integrovat aplikace PowerApps s aplikací Talent.
5. Zobrazí se dotaz na úroveň přístupu, kterou chcete použít pro databázi. Doporučujeme, abyste vybrali možnost **Omezit přístup**, protože tato možnost zabraňuje uživatelům aplikace Talent v přímém přístupu k citlivým datům pomocí aplikací PowerApps.
6. Vytvořená databáze CDS obsahuje ukázková data přidávající mimo jiné neaktivní zaměstnance a fiktivní adresy do vašeho produkčního prostředí. Chcete-li odstranit ukázková data, postupujte po vytvoření CDS databáze takto:

    > [!IMPORTANT]
    > Pokud jste dříve vytvořili CDS databázi a zadali do ní jakákoliv produkční data své společnosti, že tyto kroky odstraní **všechna** data ve vybrané databázi, včetně produkčních dat vaší společnosti.

    1. Přihlaste se k [PowerApps](https://preview.web.powerapps.com/home).
    2. V rozevíracím seznamu v pravé horní části vyberte prostředí, které jste vytvořili v kroku 2.
    3. Rozbalte **Common Data Service** v levém navigačním podokně a zvolte **Entity**.
    4. V pravé části stránky vyberte tlačítko s třemi tečkami (**...**) a vyberte **Vymazat všechna data**.
    5. Vyberte **Odstranit data** pro potvrzení, že si opravdu přejete odstranit data. Tato akce odstraní všechna ukázková data, která jsou ve výchozím nastavení součástí CDS. Odebere také jakákoliv další data, která byla zadána do vybrané databáze.

Nyní můžete používat své nové prostředí.

## <a name="grant-access-to-the-environment"></a>Zřízení přístupu k prostředí
Ve výchozím nastavení má k prostředí přístup globální správce, který ho vytvořil. Dalším uživatelům aplikace musí být explicitně udělen. Chcete-li udělit přístup, [přidáte uživatele](../dev-itpro/sysadmin/tasks/create-new-users.md) a [přiřadíte jim příslušné role](../dev-itpro/sysadmin/tasks/assign-users-security-roles.md) v prostředí Core HR. Je také nutné přidat tyto uživatele do prostředí PowerApps, aby měli přístup k aplikacím Attract a Onboard. Postup je popsán zde. Jestliže požadujete pomoc k dokončení kroků, přečtěte si příspěvek blogu [Představení centra správy PowerApps](https://powerapps.microsoft.com/en-us/blog/introducing-admin-center-for-powerapps/).

Dokončení tohoto postupu provede globální správce, který nasadil prostředí Talent.

1. Otevřete [Centrum správy PowerApps](https://preview.admin.powerapps.com/environments).
2. Zvolte příslušná prostředí.
3. Na kartě **Zabezpečení** přidejte požadované uživatele k roli **Tvůrce prostředí**.

Všimněte si, že tento poslední krok manuálního přidání uživatelů do prostředí PowerApps je dočasný. Popřípadě bude dokončen automaticky po přidání uživatelů do Core HR.

