---
title: "Rozdělení období do periodických deníků"
description: "Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261354
ms.assetid: 76c0d7bf-f795-4d42-9a86-a9f36989962c
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 8343c3c28e9b3cf79bdee568b81fc8cad659f4ab
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="split-periods-in-periodic-journals"></a>Rozdělení období do periodických deníků

[!include[banner](../includes/banner.md)]


Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován.

Pro opakované načtení a zaúčtování řádků transakcí můžete použít stránku **Periodické deníky**. Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku je stránka **Periodické deníky** rozšířena o funkci rozdělení na období. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Příklad: Rozdělení na období do periodických deníků

Pojišťovna nabízí organizaci slevu při předplacení pojistného za celý rok. Platba je zaúčtována do majetkového účtu, například jako předplatné pojistného. Potom umoříte vaše měsíční náklady na pojistné během celého roku vytvořením periodického deníku, který obsahuje kredit na předplaceném účtu pojištění a debet na výdajovém účtu pojištění. V takovém případě můžete použít funkci rozdělení na období. Klikněte na tlačítko **Rozdělit mezi období** v podokně akcí na stránce **Řádky periodického****deníku** a potom zadejte následující pole.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pole**             | **Popis**                                                                                                                                                                                             |
| **Počáteční datum**        | Vyberte datum pro první řádek periodického deníku.                                                                                                                                                        |
| **Počet období** | Zadejte počet období, napříč kterými má být řádek deníku rozdělen. Tato hodnota určuje, kolik nových transakcí je generováno. Částka transakce je rovnoměrně rozložena mezi nové transakce. |
| **Jednotka**              | Vyberte měrnou jednotku pro dané období.                                                                                                                                                                  |
| **Interval období**   | Určete interval mezi účetními obdobími.                                                                                                                                                              |

Chcete-li například generovat čtvrtletní zaúčtování, zadejte hodnotu **4** do pole **Počet období**, vyberte možnost **Měsíce** v poli **Jednotka** a zadejte hodnotu **3** do pole **Interval období**. Systém generuje čtyři řádky deníku, každý pro jednu čtvrtinu částky řádku deníku, který jste zadali ve 3měsíčních intervalech. Podobná funkce je také k dispozici pro hlavní deník. Při zobrazení řádků hlavního deníku vyberte **Periodický deník**&gt;**Uložit deník**.




