---
title: Vytváření konfiguračních pravidel
description: Tento postup se zaměřuje na vytvoření konfiguračních pravidel, která lze použít pro konfiguraci založenou na dimenzích k vynucení nebo zamezení vzniku určitých kombinací řádků kusovníku.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMTable, BOMConfigRule, ConfigItemIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d75e9ecaa814085e8fce1836125553511cf4f48b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999724"
---
# <a name="create-configuration-rules"></a>Vytváření konfiguračních pravidel

[!include [banner](../../includes/banner.md)]

Tento postup se zaměřuje na vytvoření konfiguračních pravidel, která lze použít pro konfiguraci založenou na dimenzích k vynucení nebo zamezení vzniku určitých kombinací řádků kusovníku. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o sedmý postup z osmi, který vysvětluje vytvoření kombinací konfigurace založené na dimenzích.

1. Přejděte do nabídky Řízení informací o produktech > Kusovníky a receptury > Kusovníky.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Najděte a vyberte kusovník pro konfiguraci založenou na dimenzích.  
3. V podokně akcí klikněte na Možnosti.
4. Klikněte na tlačítko Změnit zobrazení.
5. Klikněte na možnost Zobrazení záhlaví.
    * Otevřením zobrazení záhlaví získejte přístup na pevnou záložku Konfigurační postup.  
6. Rozbalte nebo sbalte oddíl Konfigurační postup.
    * Pevná záložka Konfigurační postup musí být v rozbaleném stavu.  
7. Klikněte na možnost Konfigurační pravidla.
8. Klikněte na položku Nová.
9. Označte v seznamu vybraný řádek.
10. V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Zobrazí se položky v aktuální konfigurační skupině. Vyberte jednu, která představuje podmínku pravidla.  
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. Vyberte volbu v poli Metoda.
    * Je možné vynutit volbu nebo zrušení volby položky z jiné konfigurační skupiny.  
13. V poli Odvozená skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte požadovanou konfigurační skupinu.  
16. V poli Odvozené číslo položky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
17. Klikněte na odkaz na vybraném řádku v seznamu.
    * Vyberte číslo položky, které má být v závislosti na zvolené metodě vybráno nebo jehož volba má být zrušena.  
18. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]