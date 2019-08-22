---
title: Zobrazení majetku
description: Toto téma popisuje zobrazení majetku v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63e5ec5b2a47706763df8105932d722986535a9b
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783123"
---
# <a name="asset-view"></a>Zobrazení majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Toto téma popisuje zobrazení majetku v modulu Správa majetku. Stránka **Zobrazení majetku** zobrazuje aktivní majetek a funkční místa ve stromovém zobrazení. Proto můžete snadno získat přehled o vztazích majetku a funkčních místech. Dále můžete zobrazit podrobné informace o funkčních místech, majetku a souvisejících kusovnících. Můžete také získat rychlý přehled o aktivních požadavcích na údržbu a pracovních příkazech, které souvisejí s majetkem.

1. Vyberte **Správa majetku** \> **Společné** \> **Majetek** \> **Zobrazení majetku**.
2. Chcete-li změnit zobrazení na stránce, vyberte novou hodnotu v poli **Zobrazení**.

    > [!NOTE]
    > Výchozí zobrazení, které se zobrazí při otevření stránky **Zobrazení majetku**, závisí na hodnotě, která je vybrána v poli **Zobrazení** na kartě **Majetek** na stránce **Parametry správy majetku** (**Správa majetku** \> **Nastavení** \> **Parametry správy majetku**).

Na pravé straně stránky se na pevných záložkách zobrazí podrobnosti o vybraném zobrazení.

Stopa s popisem cesty, která se zobrazuje nad stromovým zobrazení, zobrazuje aktuální výběr ve stromovém zobrazení. Tato stopa s popisem cesty používá následující formát:

ID funkčního místa / ID funkčního místa (pokud existuje více než jedno funkční místo) \>ID majetku / ID majetku (pokud existuje více než jeden majetek) – číslo položky.

Pokud jste ve stromovém zobrazení vybrali nějaký majetek, můžete vybrat **Aktivní požadavky** nebo **Aktivní pracovní příkazy** a zobrazit tak požadavky na údržbu nebo pracovní příkazy, které souvisejí s majetkem. Chcete-li otevřít související zobrazení, vyberte **Otevřít** \> **Funkční místo**, **Majetek** nebo **Kusovník majetku**.

Možnost **Funkční místo majetku**, kterou můžete vybrat v poli **Zobrazení**, je také k dispozici v libovolném vyhledávání majetku, kde můžete vybrat majetek. Stromové zobrazení se zobrazí na kartě **Zobrazení majetku**, například kde [vytvoříte majetek](../objects/create-an-object.md), vytvoříte požadavek údržby nebo vytvoříte pracovní příkaz.
