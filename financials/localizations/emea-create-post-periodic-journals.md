---
title: "Rozdělit období v periodických denících."
description: "Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261354
ms.assetid: 76c0d7bf-f795-4d42-9a86-a9f36989962c
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: 58ab77aea9e66834c516806e5f0cfe3069c94ff3
ms.lasthandoff: 03/31/2017


---

# <a name="split-periods-in-periodic-journals"></a>Rozdělit období v periodických denících.

[!include[banner](../includes/banner.md)]


Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém zaúčtování deníku. Při vytváření deníku zadáte interval pro opakování, například dny nebo měsíce. Můžete také určit počet období, pro které bude deník účtován.

Chcete-li opakovaně načíst a zaúčtování řádků transakcí, můžete použít **periodické deníky** stránky. Pro právnické osoby v České republice, Estonsko, Maďarsko, Lotyšsko, Litvu, Polsko a Rusko **periodické deníky** stránky je prodloužena o rozdělení období funkce. <!---For more information, see [Create and process a periodic journal](http://ax.help.dynamics.com/en/wiki/create-and-process-a-periodic-journal/).-->

### <a name="example-split-for-periods-in-periodic-journals"></a>Příklad: Rozdělit mezi období v periodických denících.

Pojišťovna nabízí slevy pro prepaying pojistné za celý rok organizaci. Platba je zaúčtována do majetkového účtu, například jako předplatné pojistného. Potom umoříte vaše měsíční náklady na pojistné během celého roku vytvořením periodického deníku, který obsahuje kredit na předplaceném účtu pojištění a debet na výdajovém účtu pojištění. V takovém případě můžete rozdělit období funkce. Klepněte **rozdělit mezi období** tlačítka v podokně akcí **periodického deníku****řádky** stránku a potom zadejte následující pole.

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**             | **Description**                                                                                                                                                                                             |
| **Start date**        | Vyberte datum pro první řádek periodického deníku.                                                                                                                                                        |
| **Number of periods** | Zadejte počet období, na které chcete rozdělit řádek deníku. Tato hodnota určuje, kolik nových transakcí je generováno. Částka transakce je rovnoměrně rozložena mezi nové transakce. |
| **Unit**              | Vyberte měrnou jednotku pro období.                                                                                                                                                                  |
| **Interval období**   | Určete interval mezi účetní období.                                                                                                                                                              |

Generovat čtvrtletní zaúčtování, zadejte **4** v **počet období** pole: vyberte **měsíců** v **jednotky** pole a zadejte **3** v **interval období** pole. Systém generuje čtyři řádky deníku, každý pro jednu čtvrtinu částky řádku deníku, který jste zadali v intervalech 3 měsíce. Podobná funkce je také k dispozici pro finanční deník. Při zobrazení řádky finančního deníku, vyberte **periodický deník**&gt;**deníku Uložit**.




