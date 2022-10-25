---
title: Řídicí panel řešení Invoice Capture
description: Tento článek popisuje řídicí panel řešení Invoice Capture.
author: sunfzam
ms.date: 10/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4c9000039488c1290f4ab992d7fe79b8ccac7b19
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690112"
---
# <a name="invoice-capture-solution-dashboard"></a>Řídicí panel řešení Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

V Invoice Capture řídicí panel obsahuje grafy, které poskytují přehled faktur, které byly importovány. Tyto grafy mohou pomoci správci závazků (AP) analyzovat výkon procesu generování faktur. Správce závazků může zobrazit stav procesu generování faktury a použitím různých filtrů může také zobrazit podrobnosti.

## <a name="available-charts"></a>Dostupné grafy

Na řídicím panelu jsou k dispozici následující grafy:

- **Všechny zachycené faktury podle stavu** – Tento graf ukazuje následující stavy zachycené faktury. Výběrem stavu mohou uživatelé filtrovat zachycené faktury v podrobném seznamu.

    - Zachyceno
    - Dokončeno
    - Probíhá kontrola
    - Zastaralé

- **Celkový objem zachycených faktur** – Tento graf zobrazuje počet zachycených faktur podle období. Uživatelé mohou změnit období pomocí rozevíracího seznamu.
- **Zachycené faktury od předních dodavatelů** – Tento graf zobrazuje celkový počet zachycených faktur podle dodavatele. Nahoře se zobrazí dodavatelé, kteří mají nejvíce faktur.
- **Dny dokončení na fakturu s výjimkami** – Tento graf ukazuje průměrný počet dní, které jsou potřeba k zachycení jedné faktury. Tyto informace mohou pomoci manažerovi závazků analyzovat čas na zpracování faktury, když je vyžadován manuální zásah. Pokud existuje vzestupný trend, uživatelé mohou zkontrolovat podrobnosti procesu a upravit nastavení, aby pomohli snížit počet požadovaných dní.
- **Neúplné faktury podle doby čekání** – Tento graf ukazuje počet dní, po které nebyla zachycená faktura vygenerována v systému plánování podnikových zdrojů (ERP). Čím větší je počet nevyřízených dní, tím delší je proces generování faktury. Správce závazků může proniknout do podrobně zachycených faktur a generovat faktury v systému ERP.
