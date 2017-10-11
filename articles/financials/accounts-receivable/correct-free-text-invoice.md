---
title: "Oprava faktury s volným textem"
description: "Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a143a373a63ab145ee4c25bb1abfab777cca6619
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017

---

# <a name="correct-a-free-text-invoice"></a>Oprava faktury s volným textem

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.

Pokud chcete upravit volnou fakturu, která již byla zaúčtována, otevřete ji. Na stránce **Faktura** vyberte možnost **Zrušit** a poté vyberte možnost **Správná faktura**. Vyberte kód důvodu, přidejte poznámky a vyberte datum pro novou, opravenou fakturu. Můžete upravit opravenou fakturu a zaúčtovat ji. 

Po zaúčtování opravené faktury se vytvoří zrušení faktury pro kreditní částku, která se rovná původní částce faktury. Kombinovaný zůstatek původní faktury a zrušení faktury je tedy 0 (nula). Zrušení faktury je vyrovnáno oproti původní faktuře. 

Po zaúčtování opravené fakturu budete mít tři faktury:

-   **Původní faktura** – Faktura obsahující informace, které opravujete.
-   **Zrušení faktury** – Systémem vygenerovaná faktura strany Dal, která byla vytvořena za účelem zrušení naposledy opravené faktury.
-   **Opravená faktura** – Faktura, která obsahuje informace o opravené faktuře.

Zrušení faktury a opravnou fakturu lze určit dvěma způsoby:

-   Na stránce **Všechny volné faktury** je sloupec **Oprava**, ve kterém můžete vidět, které faktury jsou zrušeny a které jsou opravné.
-   Záhlaví volné faktury zobrazuje stav **Zrušení faktury '\[číslo faktury\]'** nebo **Opravená faktura '\[číslo faktury\]'**.

> [!NOTE]
> Tato funkce je k dispozici pouze tehdy, je-li vybrán konfigurační klíč **Oprava volné faktury**.



