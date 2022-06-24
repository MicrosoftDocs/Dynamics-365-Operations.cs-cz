---
title: Vyskladnění nejstarší dávky na mobilním zařízení
description: Tento článek popisuje, jak nastavit a použít možnosti, když chcete vyskladnit nejstarší dávku z mobilního zařízení.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885631"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Vyskladnění nejstarší dávky na mobilním zařízení

[!include [banner](../includes/banner.md)]

Ke konfiguraci použít **Vyskladnit nejstarší dávku** lze přejít prostřednictvím nabídky mobilního zařízení a umožňuje vynutit nebo upozornit pracovníky skladu na vyskladnění nejstarší dávky na aktuálním místě.  

## <a name="where-it-applies"></a>Kdy se to používá
Možnost Vyskladnit nejstarší dávku je nakonfigurována pro položky nabídky mobilního zařízení a má vliv na vyskladnění dávky pod položkami.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Nastavení konfigurace pro vyskladnění nejstarší dávky 
Pro položky, které jsou nastaveny na použít stávající práce lze možnost **Vyskladnit nejstarší dávku** nastavit na hodnoty **žádná**, **upozornit** nebo **Vynutit** z nabídky mobilního zařízení.

**Žádná**: Pracovníci nebudou dostávat žádné zprávy a budou mít dovoleny vybrat všechny dávky v umístění.

**Upozornit** a **Vynutit**: seznam dávek s nejstarším datem vypršení platnosti se zobrazí nad ovládacím prvkem dávky, když pracovník vybere dávku. Pokud je skladové místo řízeno registrační značkou, seznam registračních značek vozidel, které mají nejstarší dávku, se zobrazí nad ovládacím prvkem registrační značky vozidla. 
-   **Upozornění**: Pokud zaměstnanec zvolí registrační značku nebo dávku, které nejsou uvedeny v seznamu, ovládací prvek bude ignorován a zobrazí se upozornění, že existuje starší dávka k výběru. Aby bylo možné pokračovat v práci, pracovník může vybrat stejnou registrační značku nebo dávku znovu.  
-   **Vynutit**: Zaměstnanci budou dále dostávat zprávy, že existuje starší dávka pro výdej.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]