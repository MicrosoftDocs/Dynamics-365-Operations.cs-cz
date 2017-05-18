---
title: "Správa aktualizací standardních nákladů"
description: "Aktualizace dat standardních nákladů lze spravovat pomocí dvou různých metod – metody s jednou verzí a se dvěma verzemi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 12ef9b3de7b489eb53de0a7ea82e4605cd2f4b0b
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


---

# <a name="manage-standard-cost-updates"></a>Správa aktualizací standardních nákladů

[!include[banner](../includes/banner.md)]


Aktualizace dat standardních nákladů lze spravovat pomocí dvou různých metod – metody s jednou verzí a se dvěma verzemi. 

Metoda s jednou verzí používá jednu nákladovou verzi obsahující všechny záznamy o nákladech. Tyto záznamy zahrnují původní náklady a všechny aktualizace nákladů.
Metoda se dvěma verzemi využívá jednu verzi, která obsahuje záznamy o původních nákladech, a druhou verzi, která obsahuje záznamy o všech aktualizacích nákladů. Hlavní výhodou metody se dvěma verzemi je jasné zobrazení a možnost sledování aktualizací nákladů v samostatné verzi nákladů, bez ovlivnění původní verze nákladů. Metodu se dvěma verzemi lze použít k identifikaci více přírůstkových aktualizací, kdy každé přírůstkové aktualizaci bude odpovídat samostatná verze nákladů obsahující přírůstkové záznamy nákladů. **Příklad:** následující příklad znázorňuje použití přístupu s jednou verzí a dvěma verzemi pro aktualizace standardních nákladů ve výrobním prostředí. Například aktualizace odpovídající novým položkám nebo opravám chyb. Předpokládejme, že jedna nákladová verze reprezentuje standardní náklady pro aktuální rok. Identifikátor pro tuto verzi je 2016-STD. Verze 2016-STD obsahuje aktuální aktivní náklady pro všechny položky. Dále obsahuje aktuální aktivní náklady pro všechny položky a všechny nákladové kategorie související s postupy a vzorce výpočtu režie, které byly známy na počátku roku 2016. 2016-STD je původní verze ocenění.
-   **Metoda aktualizace údajů nákladů s použitím jedné verze** − Metoda s jednou verzí znamená, že původní nákladová verze 2016-STD bude obsahovat všechny záznamy nákladů. Aktualizace nákladů jsou zaznamenány do 2016-STD a jsou nastavena na stav "Nevyřízené". Nevyřízené náklady lze zadat ručně pro nově zakoupené položky nebo mohou být vypočteny pro vyráběnou položku cílem zohlednit opravy. Při použití metody s jednou verzí nevyžadují výpočty kusovníku záložní datový zdroj vzhledem k tomu, že v nákladové verzi jsou obsaženy všechny aktivní náklady. Po aktivaci nevyřízených nákladů bude původní nákladová verze 2016-STD znovu obsahovat všechny aktuální aktivní náklady.
-   **Metoda aktualizace údajů nákladů s použitím dvou verzí** − Metoda se dvěma verzemi vyžaduje další nákladovou verzi, která bude obsahovat pouze aktualizace nákladů. Identifikátor pro tuto verzi je 2016-STD-CHANGES. Aktualizace nákladů jsou zaznamenány do 2016-STD-CHANGES a jsou nastaveny na stav "Nevyřízené". S přístupem se dvěma verzemi kalkulace kusovníku pro nevyřízené náklady vyžadují pro vyráběné položky záložní datový zdroj. Důvodem je skutečnost, že dodatečná nákladová verze 2016-STD-CHANGES obsahuje pouze podmnožinu dat nákladů. Zálohu lze vyjádřit jako aktivní náklady nebo jako nákladovou verzi 2016-STD, protože obě tyto položky identifikují zdroj dat nákladů v případech, kdy tento zdroj neexistuje ve verzi 2016-STD-CHANGES. Po aktivaci čekajících nákladů bude nákladová verze 2016-STD-CHANGES obsahovat aktuální aktivní náklady odrážející aktualizace, zatímco původní nákladová verze 2016-STD zůstane nedotčena. Při použití přístupu využívajícího dvě verze je vhodné nastavit zásady blokování pro původní nákladovou verzi a zabránit tak aktualizacím. Identické zásady blokování by měly být nastaveny pro dodatečnou nákladovou verzi, s výjimkou zadaného počátečního data a selektivního použití zásad blokování pro umožnění aktualizací. Určené počáteční datum musí být s každou dávkou změn aktualizováno, aby odpovídalo naplánovanému datu aktivace.

V tomto příkladu byla použita dodatečná nákladová verze pro správu aktualizací v průběhu roku 2016. Lze použít více dodatečných nákladových verzí (například samostatnou verzi pro každou dávku aktualizací). Při použití více dalších nákladů musí být záloha vyjádřena jako aktivní náklady, protože aktivní náklady jsou rozděleny na více nákladových verzích.






