---
title: "Vyskladnění nejstarší dávky na mobilním zařízení"
description: "Toto téma popisuje, jak nastavit a použít možnosti, když chcete vyskladnit nejstarší dávku z mobilního zařízení."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: ee45fed40b10dbe913c73e1186b726a39831816d
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a>Vyskladnění nejstarší dávky na mobilním zařízení

[!include[banner](../includes/banner.md)]

Ke konfiguraci použít **Vyskladnit nejstarší dávku** lze přejít prostřednictvím nabídky mobilního zařízení a umožňuje vynutit nebo upozornit pracovníky skladu na vyskladnění nejstarší dávky na aktuálním místě.  

## <a name="where-it-applies"></a>Kdy se to používá
Možnost Vyskladnit nejstarší dávku je nakonfigurována pro položky nabídky mobilního zařízení a má vliv na vyskladnění dávky pod položkami.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Nastavení konfigurace pro vyskladnění nejstarší dávky 
Pro položky, které jsou nastaveny na použít stávající práce lze možnost **Vyskladnit nejstarší dávku** nastavit na hodnoty **žádná**, **upozornit** nebo **Vynutit** z nabídky mobilního zařízení.

**Žádná**: Pracovníci nebudou dostávat žádné zprávy a budou mít dovoleny vybrat všechny dávky v umístění.

**Upozornit** a **Vynutit**: seznam dávek s nejstarším datem vypršení platnosti se zobrazí nad ovládacím prvkem dávky, když pracovník vybere dávku. Pokud je skladové místo řízeno registrační značkou, seznam registračních značek vozidel, které mají nejstarší dávku, se zobrazí nad ovládacím prvkem registrační značky vozidla. 
-   **Upozornění**: Pokud zaměstnanec zvolí registrační značku nebo dávku, které nejsou uvedeny v seznamu, ovládací prvek bude ignorován a zobrazí se upozornění, že existuje starší dávka k výběru. Aby bylo možné pokračovat v práci, pracovník může vybrat stejnou registrační značku nebo dávku znovu.  
-   **Vynutit**: Zaměstnanci budou dále dostávat zprávy, že existuje starší dávka pro výdej.

