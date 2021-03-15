---
title: Synchronizace na požádání s cenovým modulem Supply Chain Management
description: V tomto tématu je popsán způsob použití cenového modulu v aplikaci Microsoft Dynamics 365 Supply Chain Management z Dynamics 365 Sales.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 45a9de18a3ff9c50eba8b316171b492605d683d4
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130646"
---
# <a name="sync-on-demand-with-the-supply-chain-management-pricing-engine"></a>Synchronizace na požádání s cenovým modulem Supply Chain Management

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Management obsahuje cenový modul, který zpracovává obchodní smlouvy, ceníky, zákaznické věrnostní programy, promoakce a slevy. Cenový modul používá složitá pravidla k určení nejvhodnější ceny pro danou nabídku nebo objednávku. Při použití dvojitého zápisu, v aplikaci Dynamics 365 Sales použijete buď cenovou kalkulaci nebo cenový modul z Dynamics 365 Supply Chain Management na stránkách Nabídka nebo Objednávka.

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Použití cenového modulu ze Supply Chain Management v Sales

1. V Sales přejděte na **Prodej \> Objednávky**.
2. Volbo **Nová** vytvořte novou objednávku nebo vyberte existující objednávku v seznamu **Moje objednávky**.
3. Přidejte novou řádku objednávky.
4. Pokud vytváříte novou objednávku, vyberte v podokně Akce možnost **Ocenit objednávku**. Pokud aktualizujete existující objednávku, vyberte v podokně Akce možnost **Přepočítat**.

    Automaticky budou vyplněny následující sloupce:

    + Rozepsaná částka
    + Sleva %
    + Sleva
    + Částka bez přepravného
    + Částka s přepravným
    + Celková daň
    + Celková částka
    
5. Chcete-li zajistit, aby systém při výpočtu ceny přihlížel k obchodním a prodejním smlouvám, postupujte takto:
    1. Přejděte k prostředí Supply Chain Management .
    2. Přejděte na **Pohledávky \> Nastavení \> Parametry pohledávek**.
    3. Na vedlejším navigačním panelu vyberte kartu **Ceny**.
    4. Na pebné záložce **Hodnocení obchodní smlouvy** zrušte zaškrtnutí políčka **Ruční zadání**.

## <a name="how-it-works"></a>Jak to funguje

Když v Sales vyberete **Ocenit objednávku**, pro přidruženou prodejní objednávku je volána funkce **Součty** na kartě **Prodejní objednávka \> Zobrazení** v Supply Chain Management. Hodnoty celkové výše objednávky v Sales se používají k vyplnění odpovídajících sloupců v modulu Supply Chain Management.

Při výpočtu celkové částky prodejní objednávky v modulu Supply Chain Management vyhodnotí výpočet existující obchodní smlouvy a prodejní smlouvy pro zákazníka a produkty, které jsou uvedeny v prodejní objednávce. Tyto informace se použijí k výpočtu součtů. Když je vybrána možnost **Ocenit objednávku**, Sales automaticky převezme veškeré nastavení, které bylo provedeno v Supply Chain Management.

## <a name="limitations"></a>Omezení

Při vyplnění sloupců v Sales platí následující omezení:

+ Nastavení nákladů a přidělení nákladů v Supply Chain Management není replikováno v Sales.
+ Cenová kalkulace nebere v potaz zvláštní maloobchodní ceny, které jsou zadány ve sloupci **Maloobchodní síť** na stránce řádku prodejní objednávky v modulu Supply Chain Management.
+ Slevy, které jsou definovány v oddílu **Správa obchodních náhrad** v modulu Supply Chain Management, se neberou v úvahu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]