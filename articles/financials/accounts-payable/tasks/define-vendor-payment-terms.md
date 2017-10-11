--- 
title: "Definování platebních podmínek dodavatelů"
description: "Nastavte platební podmínky pro faktury dodavatele."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Definování platebních podmínek dodavatelů

[!include[task guide banner](../../includes/task-guide-banner.md)]

Nastavte platební podmínky pro faktury dodavatele. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte do nabídky Závazky > Nastavení platby > Podmínky platby.
2. Klikněte na položku Nová.
    * Stránku Podmínky platby lze použít pro definování způsobu výpočtu data splatnosti. Nepoužívá se při definování způsobu výpočtu data platební slevy.  
3. V poli Platební podmínky zadejte hodnotu.
4. Zadejte nějakou hodnotu do pole Popis.
5. Zadejte číslo do pole Dny.
    * Číslo zadané v tomto poli se použije pro přidání k datu splatnosti nebo na konec období identifikované podle způsobu platby. Například když si zvolíte Netto, číslo bude přidáno do data splatnosti. Pokud vyberete možnost Aktuální měsíc, číslo se přidá k poslednímu dni aktuálního měsíce pro výpočet data splatnosti.  
6. Klikněte na položku Uložit.
7. Zavřete stránku.
8. Přejděte do nabídky Závazky > Nastavení platby > Platební slevy.
9. Klikněte na položku Nová.
10. V poli Platební slevy zadejte ID.
11. Zadejte nějakou hodnotu do pole Popis.
12. Pokud dodavatel nabízí vrstvenou slevu, vyberte následující platební slevu po vypršení platnosti aktuální.
13. Zavřete stránku.
14. Zadejte číslo do pole Dny.
    * Množství zadané v poli Dny se použije k výpočtu data platební slevy, a to na základě možností vybraných v poli Netto/Běžný. Pokud byla vybrána možnost Netto, množství bude přidáno k datu faktury pro určení data platební slevy. Pokud byla vybrána možnost Aktuální měsíc, množství bude přidáno ke konci aktuálního měsíce pro určení data platební slevy.  
15. Zadejte procentuální hodnotu platební slevy do pole Sleva. 
16. Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury odběratele.
17. Zadejte hlavního účtu, ke kterému bude platební sleva zaúčtována pro faktury dodavatele.
    * Je-li hodnota Slevové protiúčty nastavena na Použít hlavní účet pro slevu dodavatele, použije se Hlavní účet.  Pokud je možnost nastavena na Účty na řádcích faktury, platební sleva se zaúčtuje do účtů majetku / nákladů na řádky faktury.  
18. Klikněte na položku Uložit.

