---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e9deeeaf491b77700ba0833e429f05d376a4392
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914509"
---
# <a name="add-a-welcome-message"></a>Přidání uvítací zprávy

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí. Uvítací zpráva je nastavena pomocí modulu výstrahy.

Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví. Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání. Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.

Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.

Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.

1. V Dynamics 365 Commerce přejděte na web.
1. Vyberte **Fragmenty**.
1. Vyberte fragment záhlaví, do kterého chcete přidat zprávu.
1. Ve stromové struktuře rozbalte **Chybové/informační zprávy**.
1. Vyberte modul výstrahy.

    Pokud modul výstrahy ještě neexistuje, vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**. Vyberte modul výstrahy a poté klikněte na tlačítko **OK**.

1. V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**
1. Do pole **Vstupní text** zadejte text uvítací zprávy.
1. Uložte fragment záhlaví, vraťte jej se změnami a publikujte.

Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)

