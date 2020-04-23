---
title: Nastavení upřednostňovaného technika
description: Můžete vybrat libovolného pracovníka jako upřednostňovaného technika pro servisní zakázky nebo servisní smlouvy.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ea0265eb27fb5cf32f5f921caa7ac2e44a0116
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217280"
---
# <a name="set-up-a-preferred-technician"></a>Nastavení upřednostňovaného technika 

[!include [banner](../includes/banner.md)]


Můžete vybrat libovolného pracovníka jako upřednostňovaného technika pro servisní zakázky nebo servisní smlouvy. Je však vhodné přidat pracovníka do příslušnému týmu pro zasílání, aby pracovník byl k dispozici na **expediční vývěsce**.

## <a name="assign-employee-to-a-dispatch-team"></a>Přiřazení zaměstnance do expedičního týmu

1.  Klikněte na **Lidské zdroje** \> **Společné** \> **Pracovníci** \> **Pracovníci**. Otevřete stránku podrobností pracovníka dvojitým klepnutím na jeho jméno. V **podokně akcí** klepněte na tlačítko **nastavení** \>**expediční tým** k otevření formuláře **expedice pracovníků**.

2.  V poli **Expediční tým** vyberte tým, kterému chcete pracovníka přiřadit.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Přiřazení upřednostňovaného technika k servisní smlouvě

1.  Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**. Poklepáním na servisní smlouvu otevřete formulář Podrobnosti.

2.  Na kartě **Obecné** vyberte pole **Preferovaný technik** a přiřaďte odpovídajícího člena expedičního týmu jako upřednostňovaného technika pro servisní smlouvu.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Přiřazení upřednostňovaného technika k servisní zakázce

1.  Klikněte na **Řízení služeb** \> **Periodické** \> **Expediční vývěska**.
    

    > [!NOTE]
    > <P>Ve formuláři <STRONG>Expediční vývěska</STRONG> zadejte rozsah dat pro expediční aktivity, které chcete zobrazit. Uveďte také, zda chcete zobrazit zavřené aktivity a zda chcete omezit seznam expedičních aktivity na týmy, které patří ke sledování nebo jsou pro sledování autorizovány. Klepnutím na tlačítko <STRONG>OK</STRONG> otevřete formulář <STRONG>Expediční vývěska</STRONG>.</P>



2.  Vyberte řádek servisní aktivity, kterou chcete upravit.

3.  Na kartě **Související** použijte seznam **Pracovník** a přiřaďte člena odpovídajícího expedičního týmu jako upřednostňovaného technika pro volání servisu.

## <a name="see-also"></a>Viz také

[Přehled přípravy a zřízení servisních smluv](service-agreements.md)

[Ruční vytvoření servisních objednávek](create-service-orders-manually.md)

[Servisní smlouvy (formulář)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  


