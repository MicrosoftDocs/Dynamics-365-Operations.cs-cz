---
title: Možnosti transakce dlouhodobého majetku
description: Toto téma popisuje různé dostupné metody pro vytvoření transakcí dlouhodobého majetku.
author: moaamer
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c5530bb7b0472aad75ec04c00ba828b8efb877d
ms.sourcegitcommit: 5f5a8b1790076904f5fda567925089472868cc5a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891565"
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

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Volby pro zadání typů transakcí s dlouhodobým majetkem


| Typ transakce                    | Modul                   | Možnosti                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Pořízení, Oprava pořizovací ceny | Dlouhodobý majetek             | Dlouhodobý majetek, Skladový deník dlouhodobého majetku   |
|                                     | Hlavní kniha           | Hlavní deník                           |
|                                     | Závazky         | Deník faktur, Deník schválených faktur |
|                                     | Zásobování a zdroje | Nákupní objednávka                            |
| Odpisy                        | Dlouhodobý majetek             | Dlouhodobý majetek                              |
|                                     | Hlavní kniha           | Hlavní deník                           |
| Vyřazení                            | Dlouhodobý majetek             | Dlouhodobý majetek                              |
|                                     | Hlavní kniha           | Hlavní deník                           |
|                                     | Pohledávky      | Volné faktury                         |

Zbývající hodnota období odpisu dlouhodobého majetku se neaktualizuje, pokud je řádek deníku typu transakce odpisu vytvořený nebo importovaný prostřednictvím datové entity. Zbývající hodnota je aktualizována při použití procesu schválení odpisu pro vytvoření řádku deníku.

Další informace naleznete v tématu [Integrace dlouhodobého majetku](fixed-asset-integration.md).

Systém zabrání účtování odpisů dvakrát za stejné období. Pokud například dva uživatelé vytvoří návrhy odpisů samostatně za leden, odpisy od prvního uživatele budou zaúčtovány do prvního deníku. Když druhý uživatel zaúčtuje odpisy ve druhém deníku, systém zkontroluje datum, kdy došlo k poslednímu spuštění odpisu, a pro stejnou dobu nebude účtovat odpisy za stejné období.

### <a name="transactions-that-require-a-different-voucher-number"></a>Transakce, které vyžadují různá čísla dokladů

Následující transakce s dlouhodobým majetkem budou používat různá čísla dokladů:

- Je provedeno další pořízení dlouhodobého majetku a je vypočten 'opravný' odpis.
- Majetek je rozdělen.
- Je zapnutý parametr k vypočtení odpisu pro vyřazení, a pak je majetek vyřazen.
- Datum uvedení majetku do služby je před datem pořízení. Z tohoto důvodu je zaúčtována oprava odpisu.

> [!NOTE]
> Při zadávání transakcí zkontrolujte, zda se všechny transakce vztahují ke stejnému dlouhodobému majetku. Doklad nebude zaúčtován, pokud zahrnuje více než jeden dlouhodobý majetek, a to i v případě, že je pole **Nový doklad** nastaveno na **Pouze jedno číslo dokladu** na stránce **Názvy deníku** v hlavní knize. Pokud do dokladu zahrnete více než jeden dlouhodobý majetek, může se zobrazit zpráva Na doklad může existovat jen jedna transakce dlouhodobého majetku a tento doklad nebude možné zaúčtovat.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
