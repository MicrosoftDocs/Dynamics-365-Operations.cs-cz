---
title: Oprava faktury s volným textem
description: Tento článek vysvětluje, jak opravit volnou fakturu, která byla zaúčtována, a znovu ji vystavit jako opravenou fakturu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76cf1f24a31f246a41601908ebba308551925d90
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176840"
---
# <a name="correct-a-free-text-invoice"></a>Oprava faktury s volným textem

[!include [banner](../includes/banner.md)]

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
> Tato funkce je k dispozici pouze tehdy, je-li vybrán konfigurační klíč **Oprava volné faktury**. Další informace o povolení konfiguračních klíčů naleznete v části Povolení (nebo zakázání) konfiguračních klíčů v tématu [Režimy údržby](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/maintenance-mode). 


