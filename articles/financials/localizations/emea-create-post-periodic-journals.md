---
title: "Rozdělení období do periodických deníků"
description: "Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30T00:00:00.000Z
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9b07d2c274d3e4818ffd917a730aeba3e5dff76c
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="split-periods-in-periodic-journals"></a>Rozdělení období do periodických deníků

[!include[banner](../includes/banner.md)]


Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován.

Pro opakované načtení a zaúčtování řádků transakcí můžete použít stránku **Periodické deníky**. Pro právnické osoby v České republice, Estonsku, Maďarsku, Litvě, Lotyšsku, Polsku a Rusku je stránka **Periodické deníky** rozšířena o funkci rozdělení na období. Další informace naleznete v tématu [Zaúčtování periodického deníku](/dynamics365/unified-operations/financials/general-ledger/tasks/post-periodic-journals)

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



