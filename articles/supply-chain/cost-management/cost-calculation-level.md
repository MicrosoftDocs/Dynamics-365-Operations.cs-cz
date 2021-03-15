---
title: Úroveň výpočtu nákladů
description: Tohle téma popisuje úroveň kusovníku, která se nazývá Úroveň výpočtu nákladů. Tato úroveň kusovníku vylučuje výrobní a dávkové objednávky ze svých výpočtů.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967715"
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