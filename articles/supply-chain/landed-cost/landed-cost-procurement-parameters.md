---
title: Parametry zásobování a získávání zdrojů pro Náklady za doručení
description: Toto téma popisuje, jak nastavit příslušné parametry zásobování a zdrojů, když používáte modul Náklady za doručení.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500735"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Parametry zásobování a získávání zdrojů pro Náklady za doručení

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Stránka **Parametry modulu Zásobování a zdroje** obsahuje několik nastavení, která jsou zvláště důležitá, když používáte modul **Náklady za doručení**. V dialogovém okně **Aktualizovat řádky objednávky**, které se otevírá ze stránky **Parametry modulu Zásobování a zdroje**, určete, zda mají být řádky nákupní objednávky automaticky aktualizovány, když jsou provedeny změny v záhlaví nákupní objednávky.

Abyste dokončili toto nastavení, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Na kartě **Obecné** vyberte odkaz **Aktualizovat řádky objednávky**.
1. Dialogové okno **Aktualizovat řádky objednávky** obsahuje seznam polí v záhlaví objednávky, která mohou také použít automatické aktualizace na související pole v řádcích objednávky. Nastavte každé pole v seznamu na jednu z následujících hodnot:

    - **Vždy** – Řádky objednávky se aktualizují automaticky při aktualizaci záhlaví objednávky.
    - **Nikdy** – Řádky objednávky se nikdy neaktualizují při aktualizaci záhlaví objednávky.
    - **Výzva** - Uživatel bude vyzván k výběru, zda mají být řádky objednávky aktualizovány.
