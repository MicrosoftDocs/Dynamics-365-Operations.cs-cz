---
title: Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva
description: Toto téma popisuje některá implementační rozhodnutí, která byste měli zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 192ed371eec24ed4e0532aaca341bb249a4933c7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680475"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva

[!include [banner](../includes/banner.md)]

Toto téma popisuje některá implementační rozhodnutí, která byste měli zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.

Finanční dimenze a hlavní účty jsou klíčové součásti fázi plánování pro implementaci. Po vytvoření se finanční dimenze a hlavní účty v systému používají na stránkách **Konfigurování účetní struktury**, **Rozšířené struktury pravidel** a **konfigurace finanční dimenze pro integraci aplikací**. Pořadí, které je definováno na těchto stránkách, slouží v systému k zadávání dat a spotřeby. V některých místech v systému se finanční dimenze a hlavní účty zobrazují v samostatných polích. Na dalších místech, jako jsou například deníky, finanční dimenze a hlavní účty, se zobrazí jako jeden řetězec.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Doporučené postupy při nastavování finančních dimenzí a hlavních účtů v systému zprava doleva

- Vyberete-li oddělovač účtové osnovy, vyberte jednu z možností dvojího oddělovače: dvojitá pomlčka (`--`), dvě čáry (`||`), dvě tečky (`..`), nebo dvojnásobné podtržení (`\\`).
- Když vytvoříte finanční dimenzi a hodnoty hlavního účtu, použijte pouze číslice a znaky zprava doleva.
- Nepoužívejte vybrané oddělovače účtové osnovy ve finanční dimenzi a hodnotách hlavního účtu.

Podle těchto doporučených postupů můžete zajistit konzistentní reprezentaci uživatelem definované objednávky v celém systému.
