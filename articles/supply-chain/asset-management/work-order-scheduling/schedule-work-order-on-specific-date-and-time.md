---
title: Naplánování pracovního příkazu na konkrétní datum a čas
description: Toto téma vysvětluje, jak naplánovat pracovní příkaz k určitému datu a času v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 921e78f2fc7e6254aa27ce70cdbbf0516aad7e11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214979"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a>Naplánování pracovního příkazu na konkrétní datum a čas

[!include [banner](../../includes/banner.md)]

 

Je-li nutné naplánovat pracovní příkaz k určitému datu *a* času, můžete přepsat standardní proces plánování v modulu Správa majetku a vytvořit specifický plán pro pracovní příkaz.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu pracovních příkazů klikněte na ID pracovního příkazu ve sloupci **Pracovní příkaz**.

3. Klikněte na možnost **Upravit**.

4. Na pevné záložce **Záhlaví pracovního příkazu** vložte počáteční a koncové datum a čas do polí **Očekávaný začátek** a **Očekávaný konec**.

    ![Obrázek č. 1](media/05-work-order-scheduling.png)

5. Na kartě **Obecné** klikněte na možnost **Naplánovat** pro použití standardního procesu plánování, nebo klikněte na **Vypravit**, chcete-li přiřadit pracovní příkaz pro určitého pracovníka.

6. Chcete-li přepsat všechny stávající rezervace kapacit, aby se zajistilo, že je v očekávaném období naplánována pracovní objednávka, proveďte výběr podle následujícího obrázku v dialogovém okně **Naplánovat pracovní příkaz** > sekce **Omezená kapacita**. To znamená, že proces plánování bude ignorovat existující rezervace kapacity, protože pracovní příkaz musí začínat očekávaným počátečním časem.

    ![Obrázek č. 2](media/06-work-order-scheduling.png)

7. Plánování zahájíte kliknutím na tlačítko **OK**.

8. Je-li výsledkem procesu plánování dvojitá rezervace, zobrazí se na obrazovce zpráva a můžete upravit související pracovní příkazy.

>[!NOTE]
>Chcete-li naplánovat pracovníka údržby pro daný pracovní příkaz, musí být pracovník údržby k dispozici v očekávaném počátečním datu a čase. Dostupnost pracovníka je nastavena v [kalendáři pracovníka](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md). 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]