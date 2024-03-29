---
title: Zadání dat faktury do systému závazků s použitím evidence faktur
description: Tento článek popisuje použití registru faktur k vytváření faktur.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc3f1107a9564120aae77a75e6232879bf3c51af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858372"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Zadání dat faktury do systému závazků s použitím evidence faktur

[!include [banner](../../includes/banner.md)]

Tento článek popisuje použití registru faktur k vytváření faktur. Potom použije evidenci faktur pro spárování faktury s nákupní objednávkou a dokončení výdajů na stránce faktury dodavatele.


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Nákupní objednávky**.
2. Klepnutím na možnost **Nová** vytvořte novou objednávku.
3. V poli **Účet dodavatele** v rozevíracím seznamu vyberte dodavatele. Vyberte například dodavatele **1001**.
4. Vyberte **OK**.
5. V poli **Číslo položky** vyberte z rozevíracího seznamu číslo položky služeb. Vyberte například **S0001**. Čistá částka je 75,00.  Jedná se o částku, která se očekává na faktuře.  
6. V podokně akcí klikněte na možnost **Zakoupit**.
7. Vyberte **Potvrdit**.

## <a name="create-and-post-and-invoice"></a>Vytvoření a zaúčtování faktury
1. V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Registr faktur**.
2. Zvolte **Nové**.
3. Otevřete vyhledávání a vyberte název registru faktury, který chcete použít.
4. Vyberte název registru faktury, který chcete použít.
5. Kliknutím na **Řádky** otevřete registr a zadejte řádky výdajů.
6. Ve vyhledávání vyberte dodavatele. Vyberte například dodavatele **1001**.
7. Do pole **Faktura** zadejte číslo faktury.
8. Zadejte hodnotu do pole **Popis**.
9. V poli **Dobropis** zadejte číslo.
10. V poli **Nákupní objednávka** otevřete rozevírací seznam a vyberte nákupní objednávku, kterou jste dříve vytvořili.
11. V poli **Schválil/a** zvýrazněte schvalujícího v rozevíracím seznamu a kliknutím na tlačítko **Vybrat** vyberte tohoto schvalujícího.
12. Zvolte **Zaúčtovat**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>otevřete fakturu z evidence a spárujte ji s nákupní objednávkou pro dokončení procesu fakturace
1. V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Evidence faktur**.
2. Kliknutím na možnost **Nákupní objednávka** vytvořte fakturu dodavatele z faktury v evidenci.
3. Vyberte fakturu, kterou chcete zkontrolovat.
4. Kliknutím na možnost **Aktualizovat stav párování** dokončete párování.
5. V podokně akcí vyberte **Možnosti**.
6. Vyberte **Změnit zobrazení**.
7. Vyberte **Zobrazení mřížky**.
8. Zvolte **Zaúčtovat**.
9. Zavřete stránku.
10. V navigačním podokně přejděte na **Moduly > Závazky > Dodavatelé > Dodavatelé**.
11. Vyberte dodavatele, který se nacházel na nákupní objednávce. Vyberte například dodavatele **1001**.
12. V podokně akcí vyberte možnost **Dodavatel**.
13. Vyberte **Transakce**.
14. Vyberte fakturu, kterou jste vytvořili. Časové rozlišení registru faktur bylo stornováno a zaúčtováno na příslušný účet výdajů.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
