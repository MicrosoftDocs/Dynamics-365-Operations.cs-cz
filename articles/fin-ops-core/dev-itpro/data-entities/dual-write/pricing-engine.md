---
title: Synchronizace na požádání s cenovým modulem Supply Chain Management
description: V tomto článku je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Supply Chain Management z aplikace Microsoft Dynamics 365 Sales.
author: RamaKrishnamoorthy
ms.date: 03/10/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 727e60ceee3f5c8c33d2da93128eedc1dc7bcb9f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288946"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synchronizace na požádání s cenovým modulem Supply Chain Management

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management obsahuje cenový modul, který zpracovává obchodní smlouvy, ceníky, zákaznické věrnostní programy, promoakce a slevy. Cenový modul používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nebo objednávku. Při použití dvojitého zápisu použijete buď statickou cenovou kalkulaci, nebo cenový modul Supply Chain Management na stránkách **Nabídka** a **Objednávka** v aplikaci Microsoft Dynamics 365 Sales.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Použití cenového modulu ze Supply Chain Management v Sales

1. V Sales přejděte na **Prodej \> Objednávky**.
1. Volbo **Nová** vytvořte novou objednávku nebo vyberte existující objednávku v seznamu **Moje objednávky**.
1. Přidejte novou řádku objednávky.
1. Pokud vytváříte novou objednávku, vyberte v podokně Akce možnost **Ocenit objednávku**. Pokud aktualizujete existující objednávku, vyberte v podokně Akce možnost **Přepočítat**.
1. Automaticky budou vyplněny následující sloupce:

    - Rozepsaná částka
    - Sleva %
    - Sleva
    - Částka bez přepravného
    - Částka s přepravným
    - Celková daň
    - Celková částka

> [!NOTE]
> Podobný postup platí při vytváření nabídek.

## <a name="how-it-works"></a>Jak to funguje

Když vytvoříte objednávku v Sales, bude tato objednávka okamžitě synchronizována do Supply Chain Management pomocí hodnot, které jste zadali v Sales. Když v Sales vyberete položku **Ocenit objednávku** nebo **Cenová nabídka**, Supply Chain Management vypočítá cenu pro každý řádek objednávky a celkovou objednávku na základě pravidel obchodní smlouvy, která jsou definována v Supply Chain Management. Nové vypočítané hodnoty se poté synchronizují zpět do Sales.

## <a name="set-trade-agreement-evaluation-options-in-supply-chain-management"></a>Nastavení možnosti hodnocení obchodních smluv v Supply Chain Management

Supply Chain Management můžete konfigurovat tak, aby při výpočtu ceny objednávky, která byla vytvořena v Sales, respektoval nebo ignoroval obchodní smlouvy. Chcete-li nastavit tuto možnost, postupujte následujícím způsobem.

1. Přihlaste se do prostředí Supply Chain Management.
1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Ceny** na záložce **Hodnocení obchodní smlouvy** přidejte nebo odstraňte řádek pro zásadu **Ruční zadání**, jak potřebujete. Přítomnost nebo nepřítomnost této zásady řídí, zda cenový modul Supply Chain Management automaticky přepíše prodejní cenu zadanou v Sales.

    - Pokud zásada **Ruční zadání** *není* přítomná v nastavení **Hodnocení obchodní smlouvy**, Supply Chain Management je hlavním prvkem určujícím cenu. Když uživatel vybere **Ocenit objednávku** nebo **Cenová nabídka** v podokně akcí v Sales, zavolá se cenový modul Supply Chain Management a prodejní cena zadaná v Sales se přepíše, pokud se nerovná prodejní ceně vypočítané v Supply Chain Management.
    - Pokud zásada **Ruční zadání** *je* přítomná v nastavení **Hodnocení obchodní smlouvy**, je hlavním prvkem určujícím cenu aplikace Sales. Prodejní cena, která byla zadána v Sales, nebude automaticky přepsána, když uživatel vybere v podokně akcí v Sales položku **Ocenit objednávku** nebo **Cenová nabídka**.
    - Řádky objednávek a řádky nabídek, které mají v poli **Cena za jednotku** a/nebo **Sleva** hodnotu *0* (nula), jsou v Sales považovány za zvláštní případ. Je-li k dispozici cena příslušné obchodní dohody, Supply Chain Management ji *vždy* použije na tato pole, bez ohledu na nastavení **Hodnocení obchodní smlouvy**.

    Příklad každého z těchto případů naleznete v následujících scénářích.

## <a name="example-scenario-1-trade-agreement-evaluation-without-the-manual-entry-option"></a>Ukázkový scénář 1: Hodnocení obchodní smlouvy bez možnosti Ruční zadání

V tomto scénáři nastavení **Hodnocení obchodní smlouvy** v Supply Chain Management *nezahrnuje* zásadu **Ruční zadání**. Uživatel aplikace Sales zadá řádek objednávky, který má v Sales nenulovou prodejní cenu, a pro položku Supply Chain Management není definována žádná prodejní cena.

1. V Sales uživatel vytvoří řádek objednávky, který má v poli **Cena za jednotku** hodnotu 1 amerického dolaru (USD).
1. Řádek objednávky je synchronizován se Supply Chain Management s prodejní cenou 1 USD.
1. V Sales uživatel vybere v podokně akcí možnost **Ocenit objednávku**.
1. Supply Chain Management vyhledá relevantní ceny a slevy a poté vypočítá celkové částky. Protože položka nemá v Supply Chain Management žádnou prodejní cenu, výpočet aktualizuje řádek tak, aby měla prodejní cenu 0 USD.
1. Nová prodejní cena řádku se synchronizuje zpět do Sales.
1. Výsledkem je řádek objednávky v Sales, který má prodejní cenu 0 USD.

## <a name="example-scenario-2-trade-agreement-evaluation-with-the-manual-entry-option"></a>Ukázkový scénář 2: Hodnocení obchodní smlouvy s možností Ruční zadání

V tomto scénáři nastavení **Hodnocení obchodní smlouvy** v Supply Chain Management *zahrnuje* zásadu **Ruční zadání**. Uživatel Sales zadá řádek objednávky, který má v Sales nenulovou prodejní cenu. Supply Chain Management obsahuje obchodní smlouvu, která stanoví prodejní cenu 2 USD za objednanou položku.

1. V Sales uživatel vytvoří řádek objednávky pro položku, která má v poli **Cena za jednotku** hodnotu 1 USD.
1. Řádek objednávky je synchronizován se Supply Chain Management s prodejní cenou 1 USD.
1. V Sales uživatel vybere v podokně akcí možnost **Ocenit objednávku**.
1. Protože nastaven **Hodnocení obchodní smlouvy** v Supply Chain Management zahrnuje zásadu **Ruční zadání**, prodejní cena se nezmění, i když příslušná obchodní smlouva stanoví jinou prodejní cenu.
1. Prodejní cena zůstává nezměněna v Sales a Supply Chain Management.

## <a name="example-scenario-3-trade-agreement-evaluation-for-an-item-that-has-a-sales-price-of-zero-in-sales"></a>Ukázkový scénář 3: Hodnocení obchodní smlouvy pro položku, která má nulovou prodejní cenu v Sales

V tomto scénáři nastavení **Hodnocení obchodní smlouvy** v Supply Chain Management *zahrnuje* zásadu **Ruční zadání**. Uživatel Sales zadá řádek objednávky, který má v Sales nulovou (0) prodejní cenu. Supply Chain Management obsahuje obchodní smlouvu, která stanoví prodejní cenu 2 USD za objednanou položku.

1. V Sales uživatel vytvoří řádek objednávky, který má v poli **Cena za jednotku** hodnotu 0 USD a v poli **Řádková sleva** hodnotu 0 USD.
1. Řádek objednávky je synchronizován se Supply Chain Management s prodejní cenou 0 USD.
1. Protože aplikace Supply Chain Management obdržela řádek objednávky, který má prodejní cenu 0 (nula), zavolá cenový modul, i když je zapnuta možnost **Ruční zadání**. Cenový modul vrátí prodejní cenu 2 USD, která je stanovena obchodní smlouvou, a aktualizuje řádek objednávky v Supply Chain Management.
1. Aktualizovaná prodejní cena ještě není synchronizována s řádkem objednávky v Sales.
1. V Sales uživatel vybere v podokně akcí možnost **Ocenit objednávku**.
1. Řádek objednávky v Supply Chain Management si zachová prodejní cenu 2 USD, která je nyní synchronizována zpět do Sales. Proto se hodnota **Cena za jednotku** řádku objednávky v Sales aktualizuje z 0 USD na 2 USD.
1. V Sales uživatel zadá novou hodnotu **Řádková sleva** ve výši 0,50 USD. Sales nyní vypočítá, že hodnota **Rozšířená částka** pro řádek je 1,50 USD.
1. Řádek objednávky je synchronizován se Supply Chain Management a jeho **Řádková sleva** má hodnotu 0,50 USD.
1. V Sales uživatel vybere v podokně akcí možnost **Ocenit objednávku**.
1. V řádku objednávky v Sales se nemění žádné ceny ani slevy.

## <a name="limitations"></a>Omezení

Při vyplnění sloupců v Sales platí následující omezení:

- Nastavení nákladů a přidělení nákladů v Supply Chain Management není replikováno v Sales.
- Cenová kalkulace nebere v potaz zvláštní maloobchodní ceny, které jsou zadány ve sloupci **Maloobchodní síť** na stránce řádku prodejní objednávky v modulu Supply Chain Management.
- Slevy, které jsou definovány v oddílu **Správa obchodních náhrad** v modulu Supply Chain Management, se neberou v úvahu.
- Ceny nezohledňují prodejní smlouvy.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
