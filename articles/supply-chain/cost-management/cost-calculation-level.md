---
title: Úroveň výpočtu nákladů
description: Tohle téma popisuje úroveň kusovníku, která se nazývá Úroveň výpočtu nákladů. Tato úroveň kusovníku vylučuje výrobní a dávkové objednávky ze svých výpočtů.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 41f2550ff22b838aa5d85022582fd9715917fe462aa34dbfc833941f5ada3325
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717383"
---
# <a name="cost-calculation-level"></a>Úroveň výpočtu nákladů

Úroveň kusovníku pojmenovaná jako **Úroveň výpočtu nákladů** vyloučí z výpočtů výrobní a dávkové objednávky. Systém používá tuto úroveň, když provádí výpočty nákladů ve verzích výpočtů nákladů. V procesech, jako je přepočet a uzavření zásob, systém místo toho používá úroveň kusovníku **Úroveň stanovení nákladů**.

Následující jednoduchý scénář ukazuje rozdíly mezi úrovněmi kusovníku **Úroveň výpočtu nákladů** a **Úroveň stanovení nákladů**.

Máte tři produkty: A, B a C. Produkt C je součástí produktu B a produkt B je součástí produktu A.

- **Úroveň stanovení nákladů** přiřazuje následující úrovně kusovníku:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

- **Úroveň výpočtu nákladů** přiřazuje následující úrovně kusovníku:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Poté se vytvoří výrobní objednávka pro produkt C a produkt A se přidá do kusovníku výrobní zakázky. Po odhadu objednávky jsou úrovně kusovníku aktualizovány následujícím způsobem:

- **Úroveň stanovení nákladů** přiřazuje následující úrovně kusovníku:

    - **Produkt B:** 1
    - **Produkt C:** 2
    - **Produkt A:** 3

- **Úroveň výpočtu nákladů** přiřazuje následující úrovně kusovníku:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Toto chování zajišťuje, že změny v kusovnících výrobní zakázky neovlivní následné výpočty nákladů.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]