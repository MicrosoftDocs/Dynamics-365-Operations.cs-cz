---
title: Odvozené knihy
description: Tento článek podává přehled o funkci Odvozená kniha.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a649fdbc355b3382bc6c80be03f8b37a06d5226
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176771"
---
# <a name="derived-books"></a>Odvozené knihy

[!include [banner](../includes/banner.md)]

Tento článek podává přehled o funkci Odvozená kniha.

Smyslem odvozených knih je zjednodušit zaúčtování transakcí knih dlouhodobého majetku naplánovaných v pravidelných intervalech.  Zvolíte jednu knihu jako primární. Jde obvykle o knihu používanou pro účetní odpisy. Pak ji připojíte k ostatním knihám, které jsou nastaveny pro zaúčtování transakcí ve stejných intervalech jako primární kniha. Knihy odpisů hodnoty DPH jsou často nastaveny jako odvozené knihy. 

Nejběžnější transakce pro nastavení zaúčtování odvozených knih jsou pořízení, úprava pořízení a likvidace. 

## <a name="example"></a>Příklad

Kniha B a kniha C jsou nastaveny jako odvozené knihy pro knihu A pro typ transakce pořízení. V knize A zadáte transakci pořízení majetku 123 s hodnotou 1 500,00. 

Při zaúčtování transakce je vygenerována transakce pořízení a je zaúčtována do majetku 123 pro knihu B a do majetku 123 pro knihu C s hodnotou 1 500,00. Při přípravě transakcí primární knihy k zaúčtování do deníku dlouhodobého majetku lze také zobrazit a upravit transakce odvozených knih odpisů. Při přípravě transakcí primární knihy v jiném deníku nelze zobrazit transakce odvozených hodnot. Avšak zaúčtováním do příslušných účtů a účtovacích vrstev po zaúčtování transakcí primární knihy.

> [!NOTE]                                                                                                                               
> Knihy, které jsou nastaveny pro zaúčtování transakcí v intervalech jiných než je interval pro primární knihu, musí být připojeny k dlouhodobému majetku jako samostatné knihy a nikoliv jako odvozené knihy.  

Další informace naleznete v tématu [Zaúčtování pomocí odvozených knih](post-derived-value-models.md).



