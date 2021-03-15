---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980125"
---
# <a name="add-a-welcome-message"></a>Přidání uvítací zprávy


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí. Uvítací zpráva je nastavena pomocí modulu výstrahy.

Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví. Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání. Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.

Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.

Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.

1. V tvůrci webů Commerce přejděte na svůj web.
1. Vyberte **Fragmenty**.
1. Vyberte fragment záhlaví, do kterého chcete přidat zprávu.
1. Ve stromové struktuře rozbalte **Chybové/informační zprávy**.
1. Vyberte modul výstrahy a poté klikněte na tlačítko **OK**. Pokud modul výstrahy ještě neexistuje, nejprve vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**.
1. V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**
1. Do pole **Vstupní text** zadejte text uvítací zprávy.
1. Chcete-li vrátit fragment záhlaví se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte. 

Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]