--- 
title: "Převedení fyzických zásob ve skladu"
description: "Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: fedb209ab111ed1fb6281fda2f4dea345e0905ef
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Převedení fyzických zásob ve skladu

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého. Předtím, než začnete, je třeba mít nastaven název deníku zásob pro převody zásob. Tento postup můžete projít v ukázkových datech společnosti USMF pomocí příkladových hodnot, které jsou zobrazeny, nebo můžete použít vlastní data, pokud máte produkty a nastavená umístění. Tyto úkoly obvykle provádějí zaměstnanci skladu.


## <a name="create-an-inventory-transfer-journal"></a>Vytvořit deník převodu zásob
1. Přejít do převodu.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko OK.
    * Pro každý řádek deníku je možné zadat hodnotu dimenzí „od“ a „do“. Ty jsou pro tento typ deníku nezbytné. Položky můžete převést do umístění pomocí různých pravidel. V tomto příkladu přeneseme položku v rámci stejného skladu, z umístění řízeného registrační značkou do umístění, která není řízeno registrační značkou.   

## <a name="create-journal-lines"></a>Vytvoření řádků deníku
1. Klikněte na položku Nová.
2. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat položku „A0001“.  
3. V poli Zdrojové pracoviště zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat položku „2“.  
4. V poli Cílové pracoviště zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat položku „2“.  
5. V poli Ze skladu zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat „24“.  
6. V poli Do skladu zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat „24“.  
7. V poli Ze skladového místa zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat „FL-001“.  
8. V poli Do skladového místa zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat „BULK-001“.  
9. Zadejte číslo do pole Množství.
10. Klepněte na kartu Dimenze zásob.
11. V poli Registrační značka zadejte nebo vyberte hodnotu.
    * Pokud používáte data USMF, můžete vybrat „24“.  
12. Klikněte na položku Uložit.

## <a name="post-the-inventory-transfer-journal"></a>Zaúčtovat deník převodu zásob
1. Klikněte na položku Zaúčtovat.
2. Klikněte na tlačítko OK.

## <a name="view-inventory-transactions"></a>Zobrazit skladové transakce
1. Klepněte na položku Zásoby.
2. Klikněte na Transakce.
    * V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.  


