---
title: Vytvoření oddělení a jejich přidružení k hierarchii oddělení
description: Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace. Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje. Oddělení můžete použít k sestavování funkčních oblastí. Oddělení mohou mít odpovědnost ze zisků a ztrát.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 14e0acb2ea16641eecb81bcf23c8b7d778b2b208
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303562"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Vytvoření oddělení a jejich přidružení k hierarchii oddělení

[!include [banner](includes/banner.md)]

Oddělení je provozní jednotka, která představuje kategorie nebo funkční oblasti organizace. Oddělení je zodpovědný za určitou oblast organizace, jako například prodej, účtování nebo lidské zdroje. Oddělení můžete použít k sestavování funkčních oblastí. Oddělení mohou mít odpovědnost ze zisků a ztrát.

Oddělení mohou obsahovat i skupinu nákladových středisek. Pozice lze přiřadit k oddělení. Chcete-li vytvořit oddělení, klikněte na možnost **Lidské zdroje** &gt; **Oddělení** &gt; **Oddělení**. V následující tabulce jsou popsána pole, která jsou k dispozici.

| Pole               | Popis                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Název                | Zadejte název oddělení.                                                                                                                                                                                  |
| Číslo oddělení   | výchozí hodnota může být generována automaticky, pokud je přiřazen kód číselné řady k odkazu **Číslo organizace** na stránce **Číselné řady**.                                                 |
| Vyhledávací název         | Zadejte název nebo zkratku, které lze použít pro rychlé hledání oddělení.                                                                                                                                            |
| Poznámka                | Sem zadejte případné doplňkové informace.                                                                                                                                                                            |
| V hierarchii        | Zaškrtnuté políčko označuje, že oddělení je součástí hierarchie oddělení. Informace o přidávání oddělení do hierarchie oddělení naleznete níže v tomto článku. |
| Číslo DUNS         | Zkratka DUNS znamená systém čísel univerzálních dat. Toto je devíticiferné číslo vydané organizací Dun & Bradstreet.                                                                                                     |
| Manažer             | Zadejte osobu, které řídí oddělení.                                                                                                                                                                    |
| Adresy           | Přidejte informace o adrese pro oddělení Například můžete přidat poštovní adresu budovy, ve které se oddělení nachází.                                                                          |
| Kontaktní informace | Přidejte kontaktní informace pro oddělení. Například můžete přidat telefonní číslo na oddělení služeb v oddělení.                                                                                           |

Pro přidání oddělení do hierarchie oddělení postupujte takto:

1.  Klikněte na nabídku **Lidské zdroje** &gt; **Oddělení** &gt; **Hierarchie oddělení**.
2.  Klepněte na tlačítko **Upravit**a poté vyberte organizaci, pod kterou má oddělení spadat.
3.  Klepněte na tlačítko **Vložit**a v seznamu vyberte **Oddělení**.
4.  V zobrazeném seznamu oddělení vyberte oddělení, které chcete přidat do hierarchie.
5.  Uložte změny. Obdržíte zprávu, že byla vytvořena pracovní verzi hierarchie.
6.  Po dokončení práce klikněte v návrháři hierarchie na tlačítko **Publikovat**. Můžete zadat datum začátku platnosti, které určuje, kdy má být hierarchie publikována. Například chcete-li přidat nové oddělení na začátku dalšího kalendářního roku, nastavte platné datum od 1. ledna nového kalendářního roku. Změny hierarchie se projeví k tomuto datu.

## <a name="steps-for-creating-a-department"></a>Postup při vytváření oddělení
Ohledně podrobného postupu pro vytvoření nového oddělení nahlédněte do tématu [Definování nových oddělení](../fin-and-ops/hr/tasks/define-new-departments.md). 
