---
title: Přepočet čisté částky řádku při importu prodejních objednávek a nabídek
description: Tento článek popisuje, zda a jak systém přepočítá čisté částky řádku při importu prodejních objednávek a nabídek. Vysvětluje také, jak můžete ovládat chování v různých verzích Microsoft Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 08/05/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2022-06-08
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: edda0c016130e2a273adf8f3d3e00e2d3ae9d5c6
ms.sourcegitcommit: ce58bb883cd1b54026cbb9928f86cb2fee89f43d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9719327"
---
# <a name="recalculate-line-net-amounts-when-importing-sales-orders-and-quotations"></a>Přepočet čisté částky řádku při importu prodejních objednávek a nabídek

[!include [banner](../includes/banner.md)]

Tento článek popisuje, zda a jak systém přepočítá čisté částky řádku při importu prodejních objednávek a nabídek. Vysvětluje také, jak můžete ovládat chování v různých verzích Microsoft Dynamics 365 Supply Chain Management.

## <a name="how-updates-to-net-line-amounts-are-calculated-on-import"></a>Jak se při importu počítají aktualizace čistých částek řádku

Supply Chain Management verze 10.0.23 obsahuje [opravu chyby 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418). Tato oprava chyby změnila podmínky, za kterých lze pole **Čistá částka** na řádku aktualizovat nebo přepočítat při importu aktualizací stávajících prodejních objednávek a nabídek. Ve verzi 10.0.29 můžete tuto opravu chyby nahradit zapnutím funkce *Vypočítat čistou částku řádku při importu*. Tato funkce má podobný účinek, ale poskytuje globální nastavení, které vám v případě potřeby umožní vrátit se ke starému chování. Ačkoli díky novému chování systém pracuje intuitivnějším způsobem, může přinést neočekávané výsledky ve specifických scénářích, kde jsou splněny všechny následující podmínky:

- Data, která aktualizují existující záznamy, se importují prostřednictvím entity *Řádky prodejní objednávky V2*, *Řádky prodejní nabídky V2* nebo *Řádky objednávky vrácení* pomocí Open Data Protocol (OData), včetně situací, kdy používáte duální zápis, import/export přes Excel a některé integrace třetích stran.
- Zavedené [zásady hodnocení obchodních smluv](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper) zavádění zásady změn, které omezují změny na pole **Čistá částka** pro řádky prodejní objednávky, řádky prodejní nabídky a řádky návratové objednávky. Všimněte si, že pro řádky zpětné objednávky je pole **Čistá částka** vždy vypočítáno a nelze ho nastavit ručně.
- Importovaná data zahrnují změny pole **Čistá částka** na řádcích nebo změny (jako je jednotková cena, množství nebo sleva), které způsobí přepočet hodnoty **Čistá částka** na řádcích pro jeden nebo více existujících řádkových záznamů.

V těchto konkrétních scénářích je účinkem zásad hodnocení obchodních dohod omezení aktualizací pole **Čistá částka** na řádku. Toto omezení se označuje *zásady změn*. Kvůli této zásadě vás systém při použití uživatelského rozhraní k úpravě nebo přepočtu pole vyzve k potvrzení, zda chcete provést změnu. Když však importujete záznam, systém musí provést volbu za vás. Před verzí 10.0.23 systém vždy ponechal čistou částku řádku nezměněnou, pokud není čistá částka příchozího řádku 0 (nula). V novějších verzích však systém čistou částku vždy aktualizuje nebo přepočítává podle potřeby, pokud nemá výslovný příkaz to nedělat. Ačkoli je nové chování logičtější, může vám způsobit problémy, pokud již spouštíte procesy nebo integrace, které předpokládají starší chování. Tento článek popisuje, jak se v případě potřeby vrátit ke starému chování.

## <a name="control-calculations-of-line-net-amounts-in-versions-10029-and-later"></a>Kontrolní výpočty řádkových čistých částek ve verzích 10.0.29 a novějších

Supply Chain Management verze 10.0.29 obsahuje funkci, která je pojmenována *Vypočítat čistou částku řádku při importu*. Tato funkce přidává možnost s názvem **Vypočítat čistou částku řádku** ke stránce **Parametry pohledávek**. Tato možnost vám umožňuje vybrat mezi novým a starším chováním pro výpočet čisté částky řádku při importu.

### <a name="turn-the-calculate-line-net-amount-on-import-feature-on-or-off"></a>Zapnutí a vypnutí funkce Vypočítat čistou částku řádku při importu

Když aktualizujete na verzi 10.0.29, funkce *Vypočítat čistou částku řádku při importu* je ve výchozím nastavení zapnutá a nová možnost **Vypočítat čistou částku řádku** je zpočátku nastavena na *Ano*. Nastavení *Ano* odpovídá novému standardnímu chování. Odpovídá chování systému, když je funkce vypnutá, s výjimkou případu funkčnosti [parametru CalculateLineAmount](#CalculateLineAmount), jak je popsáno dále v tomto článku. Nastavení *Ne* odpovídá chování systému před verzí 10.0.23 a je poskytováno především pro podporu starších scénářů integrace.

Správci mohou zapnout a vypnout funkci *Vypočítat čistou částku řádku při importu* pomocí [pracovního prostoru pro správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="set-the-calculate-line-net-amount-option"></a>Nastavení možnosti Vypočítat čistou částku řádku

Když je funkce *Vypočítat čistou částku řádku při importu* zapnutá, můžete nastavit možnost **Vypočítat čistou částku řádku** podle následujících kroků.

1. Přejděte do **Pohledávky \> Nastavení \> Parametry pohledávek**.
1. Na kartě **Ceny** na pevné záložce **Výpočet čisté částky na řádku prostřednictvím integrace** nastavte možnost **Vypočítat čistou částku řádku** na jednu z následujících hodnot:

    - *Ano* – Systém vždy v případě potřeby přepočítá a aktualizuje částky řádku. (Bude proto ignorovat zásady hodnocení obchodních dohod.)
    - *Ne* – Pokud je stávající nebo příchozí čistá částka pro jakýkoli řádek 0 (nula), hodnota pro tento řádek se přepočítá na základě jiných hodnot (jako je jednotková cena, množství a sleva). Pokud se stávající nebo příchozí čistá částka liší od 0 (nuly) a je nastavena zásada změny v poli **Čistá částka** na řádku, pole není přepočítáno ani aktualizováno, i když by příchozí změny řádkové ceny, množství nebo slevy znamenaly, že by měl být přepočítán součet řádků. Toto chování odpovídá verzi 10.0.22.

### <a name="how-the-calculate-line-net-amount-on-import-feature-affects-the-calculatelineamount-parameter"></a><a name="CalculateLineAmount"></a>Jak funkce Vypočítat čistou částku řádku při importu ovlivňuje parametr CalculateLineAmount

Když je funkce *Vypočítat čistou částku řádku při importu* zapnutá, hodnota parametru `CalculateLineAmount` pro tabulky `SalesLine` a `SalesQuotationLine` nemá žádný vliv. Místo toho je chování řízeno globálně pomocí možnosti **Vypočítat čistou částku řádku**, která je popsána v předchozí části. Proto, když je tato funkce zapnutá, nesmíte být závislí na hodnotě `CalculateLineAmount`.

Když je funkce *Vypočítat čistou částku řádku při importu* vypnutá, parametr `CalculateLineAmount` pro tabulky `SalesLine` a `SalesQuotationLine` funguje stejně jako ve verzi Supply Chain Management verze 10.0.23 až 10.0.28, jak je popsáno v další části.

## <a name="control-line-net-amount-calculations-in-versions-10028-and-earlier"></a>Kontrolní výpočty čistých částek řádku ve verzích 10.0.28 a starších

Když byla [oprava chyby 604418](https://fix.lcs.dynamics.com/issue/results/?q=604418) zavedena ve verzi 10.0.23, bylo možné vybrat, jak se má každá relevantní datová entita chovat, když byla upravena čistá částka řádku nebo musela být přepočítána kvůli jiným změnám (jako je aktualizovaná cena položky). Toto chování můžete ovládat nastavením nového parametru `CalculateLineAmount` pro každý řádek na jednu z následujících hodnot v importovaném souboru:

- **`CalculateLineAmount` = *1*** – Pole **Čistá částka** na řádku se vždy přepočítá a aktualizuje bez ohledu na to, zda je pro pole nastavena zásada změny, a bez ohledu na hodnotu čisté částky příchozí nebo existující řádky.
- **`CalculateLineAmount` = *0*** – Pokud je stávající nebo příchozí čistá částka pro jakýkoli řádek 0 (nula), hodnota pro tento řádek se přepočítá na základě jiných hodnot (jako je jednotková cena, množství a sleva). Pokud se stávající nebo příchozí čistá částka liší od 0 (nuly) a je nastavena zásada změny v poli **Čistá částka** na řádku, pole není přepočítáno ani aktualizováno.  

Chování systému závisí na vaší verzi Supply Chain Management:

- Ve verzi 10.0.22 a starších se systém vždy chová, jako by bylo `CalculateLineAmount` nastaveno na *0*, a neexistuje způsob, jak ho přimět, aby choval, jako by bylo `CalculateLineAmount` nastaveno na *1*.
- Ve verzích 10.0.23 až 10.0.28 se systém chová, jako kdyby `CalculateLineAmount` bylo nastaveno na *1* pro všechny řádky, kde není explicitně nastaveno *0* v souboru importu.
