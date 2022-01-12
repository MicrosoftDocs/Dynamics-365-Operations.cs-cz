---
title: Pozice hotovosti
description: Toto téma popisuje, jak funkce prognózování cashflow predikuje pozici hotovosti organizace pro konkrétní časy. Také popisuje možnosti, které jsou k dispozici pro zobrazování prognóz pro různá období.
author: ShivamPandey-msft
ms.date: 12/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 6bb99084a2ffef067dd0d7158ecb5e57d6d97d75
ms.sourcegitcommit: c8dc60bb760553f166409c2e06dd2377f601c006
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/23/2021
ms.locfileid: "7945782"
---
# <a name="cash-position"></a>Pozice hotovosti

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Pozice hotovosti je projekce cashflow, která se předpovídá na nejbližší období. Je založena na projekci hotovostních příjmů od zákazníků, kteří platí neuhrazené faktury a objednávky, a také na projekci hotovostních výdajů, které jsou vypláceny prodejcům za nákupní faktury a objednávky.

Když systém predikuje platby zákazníkovi, používá predikce plateb z funkce predikce plateb zákazníka. Bez predikcí plateb se k výpočtu data platby použije průměrná doba potřebná k převodu faktury zákazníka na platbu pro každého zákazníka. U otevřených objednávek zákazníků systém vypočítá datum faktury na základě průměrného počtu dnů pro fakturaci řádků objednávky na zákazníka. Poté použije datum faktury jako vstup pro funkci predikce platby. Funkce predikce plateb zákazníka vypočítá datum platby pro každý řádek objednávky. 

Datum platby neuhrazených faktur je přibližně z predikcí plateb výběrem data, které odpovídá padesátému percentilu kumulativní distribuční funkce, která je získána z pravděpodobností predikovaného intervalu.

Podobný přístup se používá k predikci plateb dodavatelům. Pro každého dodavatele systém vypočítá průměrnou dobu potřebnou k převodu faktury dodavatele na platbu. Tento počet dní se poté použije k výpočtu data platby. U otevřených objednávek dodavatelů systém vypočítá datum faktury s přihlédnutím k průměrnému počtu dní, který je vyžadován k převedení řádků objednávky na fakturu pro každého dodavatele. Pro každého dodavatele pak systém vypočítá datum platby pomocí průměrné doby potřebné k převodu faktury dodavatele na platbu.

Horní část karty **Pozice hotovosti** obsahuje graf pozice hotovosti. Tento graf ukazuje příliv a odliv hotovosti a jejich dopad na celkovou bilanci likvidity. Podrobnosti v grafu pozice hotovosti lze zobrazit v denních, týdenních, měsíčních nebo čtvrtletních obdobích. Když vyberete **Denně**, můžete zobrazit prognózy na příštích 21 dní. Když vyberete **Týdně**, můžete zobrazit prognózy na příštích 20 týdnů. Když vyberete **Měsíčně**, můžete zobrazit prognózy na příštích 12 měsíců. Když vyberete **Čtvrtletně**, můžete zobrazit prognózy na příštích 12 čtvrtletí. Graf můžete skrýt, pokud potřebujete více místa na obrazovce pro prohlížení obsahu na kartě **Pozice hotovosti**.

Spodní část karty **Pozice hotovosti** zobrazuje podrobnosti o pozici, cashflow, projektovaných platbách a bankovním účtu.

- Informace v mřížce **Podrobnosti o pozici** jsou uvedeny ve třech oddílech: seznam účtů likvidity, seznam dokumentů, které tvoří příliv hotovosti, a seznam dokumentů, které tvoří odtok hotovosti. Mřížka také zobrazuje zůstatky pozice hotovosti. U prvního sledovaného období je zůstatek na účtech likvidity počátečním zůstatkem. Pro následující období se zůstatky na účtech likvidity počítají na základě přičítání peněžních toků a odčítání peněžních odtoků z předchozích období. Chcete-li zobrazit podrobnosti transakcí, které tvoří zůstatek, vyberte odkaz **Zůstatek**.
- Mřížka **Cashflow** zobrazuje cashflow, peněžní odtoky agregované za období a jejich dopad na zůstatky na účtu likvidity. U prvního období je zůstatek na účtech likvidity počátečním zůstatkem. Pro následující období se zůstatky na účtech likvidity počítají na základě přičítání peněžních toků a odčítání peněžních odtoků z předchozích období.
- Mřížka **Předpokládaný bankovní zůstatek** zobrazuje očekávané odtoky hotovosti a jejich dopad na účty likvidity.
- Mřížka **Bankovní účet** ukazuje dopad očekávaných přílivů a odtoků hotovosti na bankovní zůstatek.

Chcete-li uložit a upravit pozici hotovosti, vytvořte snímek. Další informace o práci se snímky najdete v části [Přehled snímků](payment-snapshots.md).

## <a name="details-of-the-cash-position-capability"></a>Podrobnosti o funkci Pozice hotovosti 

Funkce Pozice hotovosti zahrnuje následující funkce. 

- Funkce Pozice hotovosti zobrazuje cashflow na základě existujících dokladů v systému a řádků přírůstku a úbytku hotovosti importovaných z externích systémů.
- Usnadňuje integraci dat cashflow z externích systémů do Dynamics 365 Finance. Pozice cashflow může využívat také rámec importu a exportu dat. Tento rámec usnadňuje integraci s Excel OData. Můžete také kombinovat data z více zdrojů a vytvořit komplexní řešení pozice cashflow.
- Představuje inteligentní pozici hotovosti. Pozice hotovosti se vytváří na základě chování platby zákazníka, aby bylo možné predikovat, kdy může společnost očekávat, že na její účty dorazí hotovost.
- U zákaznických objednávek a faktur se funkce AI predikce plateb zákazníků používá k určení historického platebního chování zákazníků, kdy bude objednávka nebo faktura zaplacena.
- U objednávek a faktur dodavatelů používáme průměrnou dobu mezi odesláním a zaplacením faktury podle dodavatele, abychom určili, kdy bude objednávka nebo faktura dodavatele zaplacena, čímž se zpřesní úbytek hotovosti.

To vytváří přesnější pohled na cashflow založený na historickém platebním chování pokladníka. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
