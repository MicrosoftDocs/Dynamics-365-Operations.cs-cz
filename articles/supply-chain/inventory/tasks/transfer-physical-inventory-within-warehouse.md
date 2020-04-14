---
title: Převedení fyzických zásob ve skladu
description: Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 899701413814ce38a4367618ed72d1039eca0bf8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148163"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a>Převedení fyzických zásob ve skladu

[!include [banner](../../includes/banner.md)]

Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob za účelem registrace pohybu zboží z jednoho umístění ve skladu do druhého. Předtím, než začnete, je třeba mít nastaven název deníku zásob pro převody zásob. Tento postup můžete projít v ukázkových datech společnosti USMF pomocí příkladových hodnot, které jsou zobrazeny, nebo můžete použít vlastní data, pokud máte produkty a nastavená umístění. Tyto úkoly obvykle provádějí zaměstnanci skladu.


## <a name="create-an-inventory-transfer-journal"></a>Vytvořit deník převodu zásob
1. V **Navigačním podokně** přejděte na **Řízení zásob > Položky deníku > Položky > Převod**.
2. Klepněte na možnost **Nový**.
3. V poli **Název** zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko **OK**. Pro každý řádek deníku je možné zadat hodnotu dimenzí „od“ a „do“. Ty jsou pro tento typ deníku nezbytné. Položky můžete převést do umístění pomocí různých pravidel. V tomto příkladu přeneseme položku v rámci stejného skladu, z umístění řízeného registrační značkou do umístění, která není řízeno registrační značkou.   

## <a name="create-journal-lines"></a>Vytvořit řádky deníku
1. Na pevné záložce **Řádky deníku** klikněte klepněte na položku **Nový**.
2. V poli **Číslo položky** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat položku „A0001“.  
3. V poli **Zdrojové pracoviště** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat položku „2“.  
4. V poli **Cílové pracoviště** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat položku „2“.  
5. V poli **Ze skladu zadejte** nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat „24“.  
6. V poli **Do skladu** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat „24“.  
7. V poli **Ze skladového místa** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat „FL-001“.  
8. V poli **Do skladového místa** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat „BULK-001“.  
9. Zadejte číslo do pole **Množství**.
10. Na pevné záložce **Podrobnosti řádku** klikněte na kartu **Dimenze zásob**.
11. V možnosti **Z dimenzí zásob** v poli **Registrační značka** zadejte nebo vyberte hodnotu. Pokud používáte data USMF, můžete vybrat „24“.  
12. Klikněte na možnost **Uložit**.

## <a name="post-the-inventory-transfer-journal"></a>Zaúčtovat deník převodu zásob
1. V **podokně akcí** klikněte na **Zaúčtovat**.
2. Klikněte na tlačítko **OK**.

## <a name="view-inventory-transactions"></a>Zobrazit skladové transakce
1. Klikněte na položku **Zásoby**.
2. Klikněte **Transakce**. V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.  

