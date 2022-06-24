---
title: Přidání chyby do pracovního příkazu
description: Tento článek popisuje postup přidávání registrací závad do pracovních příkazů v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7905dcd4c29872ec2601359baefa78545140397c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857888"
---
# <a name="add-fault-to-work-order"></a>Přidání chyby do pracovního příkazu

[!include [banner](../../includes/banner.md)]



Můžete přidat závady nastavené v návrháři závad do pracovního příkazu. Majetek vybraný v pracovním příkazu musí obsahovat typy majetku, ke kterým je připojen jeden nebo více záznamů závad. Další informace o funkcích správy případů naleznete v tématu [Správa chyb](../setup-for-work-orders/fault-management.md).

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz, u kterého chcete provést registraci chyby, a v podokně akcí na kartě **Pracovní příkaz** ve skupině **Majetek** vyberte **Chyba majetku**.

3. Na pevné záložce **Příznaky** vyberte **Přidat řádek**. Do pole **Závada** se automaticky zadá pořadové číslo závady.

4. V poli **Příznak závady** vyberte příslušný příznak.

5. V polích **Oblast chyby** a **Typ chyby** vyberte příslušné hodnoty.

6. Do pole **Datum poruchy** se automaticky vloží aktuální datum. Můžete vybrat jiné datum podle potřeby.

7. Na pevné záložce **Příčiny vybraného příznaku** přidejte řádek popisující příčinu problému.

8. Na pevné záložce **Náprava vybraného příznaku** přidejte řádek popisující možné řešení problému.

9. Zvolte **Uložit**.

Následující obrázek znázorňuje příklad stránky registrace závady.

![Obrázek č. 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Zobrazení závad majetku

V seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku.

Na stránce seznamu **Závady majetku** můžete získat přehled o všech závadách zaregistrovaných u majetku. Chcete-li stránku otevřít , vyberte **Správa majetku** > **Dotazy** > **Závada majetku** > **Závady majetku** a otevřete seznam.


## <a name="print-asset-fault-report"></a>Tisk sestavy závad majetku

Na stránce se seznamem **Všechen majetek** můžete vytisknout sestavu závad majetku zobrazující všechny registrace závad a grafický přehled statistik závad.

1. Vyberte **Správa majetku** > **Společné** > **Majetek** > **Všechen majetek**.

2. Vyberte majetek, pro který chcete vytisknout sestavu chyb.

3. Na panelu akcí na kartě **Obecné** ve skupině **Sestavy** vyberte **Závada majetku**.

4. Zadejte konkrétní období nebo vyberte typ závady.

5. Klepnutím na tlačítko **OK** sestavu vytisknete.

>[!NOTE]
>Můžete také vytisknout sestavu závad pro několik majetků nebo typů majetku výběrem **Správa majetku** > **Sestavy** > **Majatek** > **Závada majetku**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]