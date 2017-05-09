---
title: "Oprava faktury s volným textem"
description: "Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


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




