---
title: Přidání závady do pracovního příkazu
description: Toto téma popisuje postup přidávání registrací závad do pracovních příkazů v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875551"
---
# <a name="add-fault-to-work-order"></a>Přidání závady do pracovního příkazu

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Můžete přidat závady nastavené v návrháři závad do pracovního příkazu. Majetek vybraný v pracovním příkazu musí obsahovat typy majetku, ke kterým je připojen jeden nebo více záznamů závad. Další informace o nastavení naleznete v části [Správa poruch](../setup-for-work-orders/fault-management.md).

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu vyberte pracovní příkaz, na kterém chcete provést registraci poruch, a klikněte na **Závada majetku**.

3. Na záložce s náhledem **Příznaky** klikněte **Přidat řádek**. Do pole **Závada** se automaticky zadá pořadové číslo závady.

4. V poli **Příznak poruchy** vyberte příslušný příznak.

5. Vyberte **Oblast poruchy** a **Typ poruchy**.

6. Do pole **Datum poruchy** se automaticky vloží aktuální datum. V případě potřeby můžete vybrat jiné datum.

7. Na záložce s náhledem **Příčiny vybraného příznaku** přidejte řádek popisující příčinu problému.

8. Na záložce s náhledem **Náprava vybraného příznaku** přidejte řádek popisující možné řešení problému.

9. Klikněte na možnost **Uložit**.

![Obrázek č. 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Zobrazení závad majetku

V seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku.

Klikněte na **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku** a otevřete seznam.


## <a name="print-asset-fault-report"></a>Tisk sestavy závad majetku

Na stránce se seznamem **Všechen majetek** můžete vytisknout sestavu závad majetku zobrazující všechny registrace závad, stejně jako grafický přehled statistik závad.

1. Klikněte na **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.

2. V seznamu **Majetek** vyberte majetek, pro který chcete vytisknout sestavu závad.

3. Na kartě **Obecné** > část **Sestavy** klikněte na **Závada majetku**.

4. Vložte určité období nebo vyberte typ závady.

5. Klepnutím na tlačítko **OK** sestavu vytisknete.

>[!NOTE]
>Můžete také vytisknout sestavu závad pro několik majetků nebo typů majetku kliknutím na **SPráva majetku** > **Sestavy** > **Majatek** > **Závada majetku**.

