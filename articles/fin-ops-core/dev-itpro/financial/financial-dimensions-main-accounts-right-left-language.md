---
title: Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva
description: Tento článek popisuje rozhodnutí, která je třeba zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1e2c0ef5cd405232332847078c70af42f056e17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866753"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva

[!include [banner](../includes/banner.md)]

Tento článek popisuje některá implementační rozhodnutí, která byste měli zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.

Finanční dimenze a hlavní účty jsou klíčové součásti fázi plánování pro implementaci. Po vytvoření se finanční dimenze a hlavní účty v systému používají na stránkách **Konfigurování účetní struktury**, **Rozšířené struktury pravidel** a **konfigurace finanční dimenze pro integraci aplikací**. Pořadí, které je definováno na těchto stránkách, slouží v systému k zadávání dat a spotřeby. V některých místech v systému se finanční dimenze a hlavní účty zobrazují v samostatných polích. Na dalších místech, jako jsou například deníky, finanční dimenze a hlavní účty, se zobrazí jako jeden řetězec.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Doporučené postupy při nastavování finančních dimenzí a hlavních účtů v systému zprava doleva

- Vyberete-li oddělovač účtové osnovy, vyberte jednu z možností dvojího oddělovače: dvojitá pomlčka (`--`), dvě čáry (`||`), dvě tečky (`..`), nebo dvojnásobné podtržení (`\\`).
- Když vytvoříte finanční dimenzi a hodnoty hlavního účtu, použijte pouze číslice a znaky zprava doleva.
- Nepoužívejte vybrané oddělovače účtové osnovy ve finanční dimenzi a hodnotách hlavního účtu.

Podle těchto doporučených postupů můžete zajistit konzistentní reprezentaci uživatelem definované objednávky v celém systému.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
