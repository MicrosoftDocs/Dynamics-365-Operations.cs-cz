---
title: Parametry zásobování a získávání zdrojů pro Náklady za doručení
description: Tento článek popisuje, jak nastavit příslušné parametry zásobování a zdrojů, když používáte modul Náklady za doručení.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905972"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Parametry zásobování a získávání zdrojů pro Náklady za doručení

[!include [banner](../../includes/banner.md)]

Stránka **Parametry modulu Zásobování a zdroje** obsahuje několik nastavení, která jsou zvláště důležitá, když používáte modul **Náklady za doručení**. V dialogovém okně **Aktualizovat řádky objednávky**, které se otevírá ze stránky **Parametry modulu Zásobování a zdroje**, určete, zda mají být řádky nákupní objednávky automaticky aktualizovány, když jsou provedeny změny v záhlaví nákupní objednávky.

Abyste dokončili toto nastavení, postupujte takto.

1. Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.
1. Na kartě **Obecné** vyberte odkaz **Aktualizovat řádky objednávky**.
1. Dialogové okno **Aktualizovat řádky objednávky** obsahuje seznam polí v záhlaví objednávky, která mohou také použít automatické aktualizace na související pole v řádcích objednávky. Nastavte každé pole v seznamu na jednu z následujících hodnot:

    - **Vždy** – Řádky objednávky se aktualizují automaticky při aktualizaci záhlaví objednávky.
    - **Nikdy** – Řádky objednávky se nikdy neaktualizují při aktualizaci záhlaví objednávky.
    - **Výzva** - Uživatel bude vyzván k výběru, zda mají být řádky objednávky aktualizovány.
