---
title: "Držitelé zálohy"
description: "Informace o funkcích držitele zálohy v 365 Microsoft Dynamics pro operace."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262574
ms.assetid: 87924785-6032-4125-8279-5b1a758f4d80
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 8cfe98e3859778e4fdc61f22b437cb1b4d004549
ms.lasthandoff: 03/31/2017


---

# <a name="advance-holders"></a>Držitelé zálohy

[!include[banner](../includes/banner.md)]


Informace o funkcích držitele zálohy v 365 Microsoft Dynamics pro operace.

*Držitele zálohy* je zaměstnanec společnosti, která bude odpovídat za částku výdajů uvedenou v organizaci. Pouze pracovník společnosti může být držitelem zálohy. Při zadávání vládních zakázek se stane, podává držitel zálohy společnosti o výdaje, které byly provedeny. Společnost reimburses částky výdajů zaměstnance. Společnost řídí rovnováhu pro každého držitele zálohy. Uživatelé v právnických osobách, Estonska, Lotyšska, Litvy, Polska, České republiky, Maďarska a Ruska může vyjadřovat určité transakce průvodní operace společnosti zaměstnanci, kteří jsou odpovědní za částku výdajů poskytované organizací.

## <a name="set-up-an-advance-holder"></a>Nastavit držitele zálohy
Pokud chcete nastavit držitelem zálohy, je třeba doplnit následující úkoly v pořadí.
1.  Vytvoření skupiny držitelů záloh.
2.  Nastavte účetní profil zaměstnance.
3.  Nastavte parametry účtu závazků.
4.  Vytvořte specifické podmínky platby pro držitele zálohy.
5.  Vytvořte držitelem zálohy.

### <a name="advance-holder-groups"></a>Skupiny držitelů záloh

Použití **skupiny držitelů záloh** stránku vytvořit skupinu držitele zálohy. Můžete zadat název, popis a protiúčet pro skupinu držitele zálohy.
### <a name="employee-posting-profile"></a>Účetní profil zaměstnance

Použití **účetní profily zaměstnanců** stránku vytvořit profil pro transakce držitele zálohy. Můžete zadat následující informace pro účetní profil zaměstnance.
|Pole |popis|
|------|-----------|
|Účetní profil|Zadejte identifikační kód pro profil zaúčtování držitele zálohy.|
|popis|Zadejte stručný popis profilu zaúčtování.|
|Platné pro|Vyberte jednu z následujících možností pro úroveň seskupení pro účetní profil nastavení: 
**Tabulka** – tuto možnost lze nastavit účetní profil pro držitele jedné zálohy. Je třeba určit kód držitele zálohy v poli odkaz.
**Skupina** – tato možnost slouží k nastavení profilu zaúčtování pro skupiny držitelů záloh. Je třeba určit kód skupiny v poli odkaz.
**Všechny** – tato možnost slouží k nastavení účetního profilu pro všechny držitele záloh. | | Odkaz | Vyberte kód držitele zálohy, pokud je vybrána tabulka platí pro pole nebo vyberte skupinu držitele zálohy platí pro pole je vybrána skupina. | | Souhrnný účet | Vyberte součtový účet pro zaúčtování transakce. |



### <a name="account-payable-parameters"></a>Parametry závazků

Tak, aby odrážely transakce držitele zálohy musíte nastavit následující na **účet parametry závazků** stránce **držitelů záloh** oddílu.
|                                                |                   |
|------------------------------------------------|-------------------|
|  **Field**                                     | **Description**                                                                                                                                                                  |
| **Posting profile**                            | Vyberte výchozí profil pro dokončení transakce.                                                                                                         |
| **Advance holder sorting**                     | Je-li vybrána, držitelé zálohy se zobrazí na začátku seznamu **držitelů záloh** stránky.                                                                     |
| **Issue when balance is open**                 | Je-li vybrána, bude povoleno problém hotovostní zálohu držiteli zálohy, který má otevřený zůstatek kladný.                                                                      |
| **Uzavření pomocí skupiny pole platební bilance: název** | Vyberte kód platební doklad deníku. Tento kód deníku slouží ke generování hotovostní výdajové doklady a refundační doklady při uzavření zůstatků držitele zálohy prostřednictvím hotovosti. |
| **Cash**                                       | Zvolte pokladní účet, chcete-li zjistit doklady, které se používají pro uzavření zůstatků pro držitele zálohy.                                                                 |
| **Zůstatek zavírání přes bankovní skupina polí: název** | Vyberte kód deníku pro transakce, které uzavření salda přes banky.                                                                                                   |
| **Account type**                               | Vyberte banku pro uzavření zůstatků pro držitelem zálohy prostřednictvím banky.                                                                                                        |
| **Main account**                               | Vyberte kód bankovního účtu pro uzavření zůstatků pro držitelem zálohy prostřednictvím banky.                                                                                           |

### <a name="terms-of-payment-for-advance-holder"></a>Platební podmínky pro držitele zálohy

Správně zaregistrovat a zaúčtování nákupní objednávky prostřednictvím držitelem zálohy, je nutné použít podmínky platby, která byla nastavena pomocí **od držitele zálohy** možnost nastavena na **True**.
### <a name="create-an-advance-holder-creation"></a>Vytvořit vytvoření držitele zálohy

Před vytvořením držitelem zálohy, musí mít již nastavit pracovníků. Další informace naleznete v tématu [zadejte informace o pracovníkovi (úkol guide).](http://ax.help.dynamics.com/en/wiki/enter-worker-information/) Použití **držitelů záloh** stránku nastavení pracovníka jako držitelem zálohy. Vyberte pracovníka, který chcete použít jako držitel zálohy, klepněte na tlačítko **úprava**a potom nastavte **držitele zálohy** možnost na **True**. Musíte také vyplnit následující pole.
|                |                                                                                             |
|----------------|---------------------------------------------------------------------------------------------|
| **Field**      | **Description**                                                                             |
| **Group**      | Vyberte skupinu držitele zálohy.                                                             |
| **Series**     | Zadejte série dokladu, který slouží k ověření totožnosti držitele zálohy. |
| **Number**     | Zadejte číslo dokladu, který slouží k ověření totožnosti držitele zálohy. |
| **Issue date** | Vyberte nebo zadejte datum vydání dokumentu.                                                    |
| **Issued by**  | Zadejte údaje o orgánu nebo osoby, která dokument vydal.                       |

## <a name="advance-holder-inquiries-and-reports"></a>Držitel dotazy a sestavy záloh
### <a name="advance-holder-transactions-inquiry"></a>Dotaz na transakce držitele zálohy

Seznam transakcí držitelem zálohy, klepněte **transakce** tlačítko na **držitelů záloh** stránky. Transakce pro všechny držitele záloh nebo vytvořit konkrétní dotaz založený na transakce držitelů záloh, klepněte na tlačítko Zobrazit **závazků**&gt;**dotazy a sestavy**&gt;**předem držitelé dotazy a sestavy**&gt; transakce. Klepněte na tlačítko **dokladu** otevřete **doklad transakcí** stránky.
### <a name="advance-holder-balance-inquiry"></a>Dotaz Zůstatek držitele zálohy

Chcete-li zobrazit zůstatek držitelem zálohy použít **držitelů záloh** stránky. Zobrazení salda všech držitelů záloh nebo vytvořit konkrétní dotaz podle držitelé zálohy účtů, klepněte na **závazků**&gt;**dotazy a sestavy**&gt;**předem držitelé dotazy a sestavy**&gt;**rovnováhu.**
### <a name="advance-holder-balance-report"></a>Sestava zůstatku držitele zálohy

Chcete-li zobrazit náhled a vytisknout sestavu na základě informací o zůstatku držitelé zálohy, klepněte na tlačítko **závazků**&gt;**dotazy a sestavy**&gt;**předem držitelé dotazy a sestavy**&gt;**sestavu zůstatků držitele zálohy**.
### <a name="advance-holder-transactions-report"></a>Sestava transakcí držitelů záloh

Chcete-li zobrazit náhled a vytisknout sestavu založenou na transakce držitelů záloh, klepněte na **závazků**&gt;**dotazy a sestavy**&gt;**předem držitelé dotazy a sestavy**&gt;**sestava transakce držitele zálohy**.



<a name="see-also"></a>Viz také
--------

[Advance holder transactions](emea-advance-holders-transactions.md)




