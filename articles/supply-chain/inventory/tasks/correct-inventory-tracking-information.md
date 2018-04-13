---
title: "Oprava informací o sledování zásob"
description: "Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e28d10646f01604098de8cedc30c8c7a7c89866b
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="correct-inventory-tracking-information"></a>Oprava informací o sledování zásob

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Tento postup vás provede procesem vytvoření a zaúčtování deníku převodu zásob, za účelem opravit informace o sledování zásob. V tomto příkladu aktualizujeme informace o položky řízené dávkou pomocí změny nesprávně registrované dávky na jinou dávku. Tento proces můžete projít pomocí ukázkových dat společnosti USPI nebo pomocí vlastních dat. Při použití vlastních dat musí mít zboží, pro které je povolena dávka a nesmí být řízeno na základě umístění. Rovněž je třeba mít nastaven název deníku zásob pro převody zásob. Tyto úkoly obvykle provádějí zaměstnanci skladu.


## <a name="create-an-inventory-transfer-journal"></a>Vytvořit deník převodu zásob
1. Přejít do převodu.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko OK.

## <a name="create-journal-lines"></a>Vytvoření řádků deníku
1. Klikněte na položku Nová.
2. V poli Číslo zboží zadejte nebo vyberte hodnotu.
    * Pokud používáte USPI, vyberte položku M5003.  
3. Zadejte číslo do pole Množství.
4. Klepněte na kartu Dimenze zásob.
5. V poli Číslo dávky zadejte nebo vyberte hodnotu.
6. V poli Lokalita zadejte nebo vyberte hodnotu.
7. V poli Sklad zadejte nebo vyberte hodnotu.
8. V poli Číslo dávky zadejte nebo vyberte hodnotu.

## <a name="post-the-journal"></a>Zaúčtovat deník
1. Klikněte na položku Zaúčtovat.
2. Klikněte na tlačítko OK.

## <a name="check-tracing-information"></a>Kontrola informací o trase
1. Klepněte na položku Zásoby.
2. Klikněte na Trasa.
3. Klikněte na tlačítko OK.
    * Pomocí těchto informací trasování lze zpětně sledovat, ze které dávky jste opravili skladové položky.  Můžete také použít stránku Sledování položky pro tyto informace.  
4. Zavřete stránku.

## <a name="check-inventory-transactions"></a>Kontrola transakcí zásob
1. Klepněte na položku Zásoby.
2. Klikněte na Transakce.
    * V tomto poli se zobrazí transakce, které byly vytvořeny při zaúčtování deníku.   

