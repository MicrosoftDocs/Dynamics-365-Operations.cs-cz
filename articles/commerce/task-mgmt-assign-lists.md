---
title: Přiřazení seznamů úkolů k obchodům nebo zaměstnancům
description: Tento článek popisuje, jak přiřadit seznamy úkolů k obchodům nebo zaměstnancům v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 956ea206888b2bbbbaf2edaa006c84f6f050f379
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909354"
---
# <a name="assign-task-lists-to-stores-or-employees"></a>Přiřazení seznamů úkolů k obchodům nebo zaměstnancům

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak přiřadit seznamy úkolů k obchodům nebo zaměstnancům v řešení Microsoft Dynamics 365 Commerce.

Správa úkolů v Dynamics 365 Commerce umožňuje přiřadit seznam úkolů několika obchodům nebo zaměstnancům nebo kombinaci obchodů a zaměstnanců. Například regionální manažer 20 obchodů bude chtít přiřadit seznam úkolů **Příprava na letní sezónu** ke všem 20 obchodům.

## <a name="start-the-task-list-assignment-process"></a>Spuštění procesu přiřazení seznamu úkolů

Chcete-li spustit proces přiřazování seznamu úkolů, postupujte podle následujících kroků.

1. Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.
1. Vyberte seznam úkolů, který chcete přiřadit.
1. Vyberte možnost **Spustit proces**.
1. V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název (například **Obchody ve východní oblasti**).
1. Do pole **Cílové datum** zadejte datum.
1. Chcete-li přiřadit seznam úkolů k obchodům, na kartě **Obchody** pomocí filtru **Organizační hierarchie** vyhledejte a vyberte obchody.

    Chcete-li přiřadit seznam úkolů zaměstnancům, na kartě **Pracovníci** vyhledejte a vyberte zaměstnance.

1. Tlačítkem **OK** spustíte proces. Seznam úkolů je přiřazen k vybraným obchodům nebo zaměstnancům.

Následující ilustrace znázorňuje příklad, jak najít a vybrat obchody v dialogovém okně **Spuštění procesu**.

![Vyhledání a výběr obchodů v dialogovém okně Spuštění procesu.](media/HQ-Assign-Tasks-Lists.png)

## <a name="assign-task-lists-on-a-recurring-basis"></a>Opakované přiřazování seznamů úkolů

Maloobchodní prodejce má někdy opakující se úkoly, například „Úkoly pro čtvrteční uzávěrku“ nebo „Úkoly pro první den v měsíci“. Pro ty by se mu hodila možnost pravidelného přiřazování seznamu úkolů.

1. Přejděte na **Retail a Commerce \> Správa úkolů \> Řízení správy úkolů**.
1. Vyberte seznam úkolů, který chcete přiřadit.
1. Vyberte možnost **Spustit proces**.
1. V dialogovém okně **Spuštění procesu** na kartě **Obecné** zadejete do pole **Název procesu** jeho název.
1. Nastavte možnost **Opakování** na **Ano**.
1. Do pole **Opakovaný posun cílového data ve dnech** zadejte počet dní. Zadáte -li například hodnotu **4**, cílové datum bude datem opakování plus čtyři dny.
1. Na kartě **Spustit na pozadí** a vyberte možnost **Opakování**.
1. V dialogovém okně **Definovat opakování** zadejte kritéria četnosti a poté klikněte na tlačítko **OK**.

Na následujícím obrázku je znázorněn příklad postupu při zadávání kritérií četnosti v dialogovém okně **Definovat opakování**.

![Zadání kritérií četnosti v dialogovém okně Definovat opakování.](media/HQ-Assign-Tasks-Lists-Recurrently.png)

## <a name="track-task-list-status"></a>Sledování stavu seznamu úkolů

Jste-li regilnální manažer nebo manažer obchodu, budete pravděpodobně chtít sledovat stav seznamů úkolů, které byly přiřazeny více obchodům nebo zaměstnancům. Poté můžete sledovat obchody nebo pracovníky, kteří nedokončili přiřazené úkoly včas. Administrativa Commerce umožňuje zobrazit stav seznamů úkolů, přeřadit úkoly nebo změnit stav úkolu.

Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.
1. Chcete- li zobrazit stav všech seznamů úkolů, které jsou přiřazeny k různým obchodům, vyberte kartu **Všechny seznamy úkolů**.

Chcete-li sledovat stav seznamu úkolů pro všechny úkoly, které vám jsou přiřazeny, postupujte následujícím způsobem.

1. Přejděte na **Retail a Commerce \> Správa úkolů \> Procesy správy úkolů**.
1. Chcete- li zobrazit nebo aktualizovat stav úkolů, které jsou vám přiřazeny, vyberte kartu **Moje úkoly** nebo **Všechny úkoly**.

## <a name="additional-resources"></a>Další zdroje

[Přehled správy úkolů](task-mgmt-overview.md)

[Konfigurace správy úkolů](task-mgmt-configure.md)

[Vytvoření seznamů úkolů a přidání úkolů](task-mgmt-create-lists.md)

[Správa úkolů v POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
