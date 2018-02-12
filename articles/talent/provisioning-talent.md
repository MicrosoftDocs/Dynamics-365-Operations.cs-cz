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
ms.sourcegitcommit: 6ffb97b53f522cfe8ccd8e89df854cbc557e4f1f
ms.openlocfilehash: fadc373b2c1c06987f22d4d9c20a9ab07b0c85d5
ms.contentlocale: cs-cz
ms.lasthandoff: 11/20/2017

---
# <a name="provision-microsoft-dynamics-365-for-talent"></a>Zřízení Microsoft Dynamics 365 for Talent
Toto téma vás povede procesem zřízení nového prostředí pro aplikaci Microsoft Dynamics 365 for Talent. Toto téma předpokládá, že jste si zakoupili aplikaci Talent prostřednictvím poskytovatele cloudového řešení (CSP) nebo smlouvy o podnikové architektuře (EA). Pokud máte existující licenci pro Microsoft Dynamics 365, která obsahuje servisní plán aplikace Talent, a nedaří se vám provést kroky uvedené v tomto tématu, kontaktujte podporu.

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

    Nové prostředí se zobrazí v seznamu prostředí v navigačním podokně na levé straně. Nelze však začít používat prostředí, dokud není stav nasazení aktualizován na **Nasazeno**. Tento proces trvá obvykle několik minut. Pokud se zřizování nezdaří, obraťte se na podporu.

6. Chcete-li začít používat své nové prostředí, zvolte **Přihlásit se do aplikace Talent**.

> [!NOTE]
> Pokud nesplňujete ještě všechny konečné předpoklady, můžete v projektu nasadit zkušební instanci aplikace Talent. Poté můžete tuto instanci použít k vyzkoušení vašeho řešení, dokud všechny předpoklady nesplníte. Pokud použijete nové prostředí pro testování, musíte stejným způsobem opakovat tento postup k vytvoření produkčního prostředí.

## <a name="create-a-new-powerapps-environment-if-required"></a>Vytvoření nového prostředí PowerApps prostředí (je-li požadováno)
1. Vyberte možnost **Spravovat prostředí** v LCS. Budete nasměrováni na [Centrum pro správu PowerApps](https://preview.admin.powerapps.com/environments), kde můžete zobrazit existující prostředí a vytvořit nová prostředí.
2. Vyberte tlačítko (**+**) **Nové prostředí**.
3. Zadání jedinečný název prostředí a vyberte umístění, do kterého ho chcete nasadit.

    > [!NOTE]
    > Talent není k dispozici ve všech oblastech. Nezapomeňte ověřit dostupnost před výběrem umístění vašeho prostředí.

4. Když se objeví dotaz, zda chcete vytvořit databázi, vyberte **Vytvořit databázi** pro vytvoření databáze služby Common Data Service, která musí být hostitelem části vašich dat aplikace Talent Vytvořením databáze také můžete integrovat aplikace PowerApps s aplikací Talent.
5. Zobrazí se dotaz, o který chcete použít pro databázi úroveň přístupu. Doporučujeme, abyste vybrali možnost **Omezit přístup**, protože tato možnost zabraňuje uživatelům aplikace Talent v přímém přístupu k citlivým datům pomocí aplikací PowerApps.
6. Vytvořená databáze CDS obsahuje ukázková data. Tato ukázková data jsou užitečná, protože můžete použít společnost ukázkových dat pro testování nebo vytvoření záznamů úkolů nebo průvodců záznamem úloh. Ukázková data však mimo jiné informace přidávají neaktivní zaměstnance a fiktivní adresy do vašeho produkčního prostředí. Chcete-li odstranit ukázková data, postupujte po vytvoření CDS databáze takto:

    > [!IMPORTANT]
    > Pokud jste dříve vytvořili CDS databázi a zadali do ní jakákoliv produkční data své společnosti, mějte na paměti, že tyto kroky odstraní **všechna** data ve vybrané databázi, včetně produkčních dat vaší společnosti.

    1. Přihlaste se do [PowerApps](https://preview.web.powerapps.com/home)a přejděte na prostředí, které jste vytvořili v kroku 2.
    2. Vyberte **Entity**. V pravé části stránky vyberte tlačítko s třemi tečkami (**...**) a vyberte **Vymazat všechna data**.
    3. Vyberte **Odstranit data** pro potvrzení, že si opravdu přejete odstranit data. Tato akce odstraní všechna ukázková data, která jsou ve výchozím nastavení součástí CDS. Odebere také jakákoliv další data, která byla zadána do vybrané databáze.

Nyní můžete používat své nové prostředí.

