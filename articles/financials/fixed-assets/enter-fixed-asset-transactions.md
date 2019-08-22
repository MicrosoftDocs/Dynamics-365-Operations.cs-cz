---
title: Možnosti transakce dlouhodobého majetku
description: Toto téma popisuje různé dostupné metody pro vytvoření transakcí dlouhodobého majetku.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f08750c369475f9d8be3c723aaf4eb6cf36eb7c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840546"
---
# <a name="fixed-asset-transaction-options"></a>Možnosti transakce dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Toto téma popisuje různé dostupné metody pro vytvoření transakcí dlouhodobého majetku.

Dlouhodobý majetek lze nastavit pro účely integrace se závazky, pohledávkami, zprostředkováním a zajištěním zdrojů a hlavní knihou. Položky lze rovněž převádět ve správě zásob na dlouhodobý majetek pro vnitřní použití.

## <a name="accounts-payable"></a>Závazky
Transakce s dlouhodobým majetkem lze zadat na stránce Doklad deníku. Tuto stránku lze otevřít ze stránky Deník faktur. Stránku Doklad deníku můžete otevřít také ze stránky Deník schválených faktur. V poli Typ protiúčtu vyberte možnost Dlouhodobý majetek. Pak v poli Protiúčet vyberte číslo dlouhodobého majetku. Na kartě Dlouhodobý majetek zadejte hodnoty do polí Typ transakce a Kniha.

## <a name="accounts-receivable"></a>Pohledávky
Transakce s dlouhodobým majetkem lze zadat na stránce Volná faktura.  Na stránce Volná faktura v mřížce Řádky faktury vyberte položku řádku. Klikněte na pevnou záložku Podrobnosti řádku. Zadejte číslo dlouhodobého majetku a knihu transakce vyřazení. U faktur s volným textem je druh transakce s dlouhodobým majetkem vždy definován jako možnost Vyřazení – odprodej.

## <a name="procurement-and-sourcing"></a>Zásobování a zdroje
Transakce s dlouhodobým majetkem lze zadat na stránce Nákupní objednávka. Zadejte požadované informace pro vytvoření nákupní objednávky a klikněte na OK. Na stránce Nákupní objednávka klikněte na pevnou záložku Podrobnosti řádku. Potom na kartě Dlouhodobý majetek zadejte informace o dlouhodobém majetku. 

Chcete-li zaúčtovat transakci pořízení pro existující položku dlouhodobého majetku, určete číslo položky dlouhodobého majetku, knihu a typ transakce. Dlouhodobý majetek nelze zaúčtovat, pokud chybí některá z těchto informací. Chcete-li zaúčtovat transakci pořízení pro novou položku dlouhodobého majetku, vyberte možnost Nový dlouhodobý majetek? a potom vyberte skupinu pevného majetku, do níž má být nová položka majetku přiřazena. Pokud se však položka nachází ve skupině skladových modelů, která používá skladový model standardních nákladů, nebudou žádná z polí dlouhodobého majetku pro daný řádek dostupná. Dále volby definované na stránce Parametry dlouhodobého majetku určují, zda můžete zaúčtovat transakce pořízení z nákupních modulů. 

Pokud se pro pořízení dlouhodobého majetku použije nákupní objednávka nebo skladový deník dlouhodobého majetku, bude ovlivněna hodnota zásob.

## <a name="general-ledger"></a>Hlavní kniha
Kterýkoliv typ transakce s dlouhodobým majetkem lze zaúčtovat na stránce Hlavní deník. K zaúčtování transakcí můžete také použít deníky ve formuláři Dlouhodobý majetek.

## <a name="options-for-entering-fixed-asset-transaction-types"></a>Volby pro zadání typů transakcí s dlouhodobým majetkem


| Typ transakce                    | Modul                   | Možnosti                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Pořízení, Oprava pořizovací ceny | Dlouhodobý majetek             | Dlouhodobý majetek, Skladový deník dlouhodobého majetku   |
|                                     | Hlavní kniha           | Hlavní deník                           |
|                                     | Závazky         | Deník faktur, Deník schválených faktur |
|                                     | Zásobování a zdroje | Nákupní objednávka                            |
| Odpisy                        | Dlouhodobý majetek             | Dlouhodobý majetek                              |
|                                     | Hlavní kniha           | Hlavní deník                           |
| Vyřazení                            | Dlouhodobý majetek             | Dlouhodobý majetek                              |
| ** **                               | Hlavní kniha           | Hlavní deník                           |
| ** **                               | Pohledávky      | Volné faktury                         |


Zbývající hodnota období odpisu dlouhodobého majetku se neaktualizuje, pokud je řádek deníku typu transakce odpisu vytvořený nebo importovaný prostřednictvím datové entity. Tato hodnota je aktualizována při použití procesu schválení odpisu pro vytvoření řádku deníku.

Další informace naleznete v tématu [Integrace dlouhodobého majetku](fixed-asset-integration.md).
