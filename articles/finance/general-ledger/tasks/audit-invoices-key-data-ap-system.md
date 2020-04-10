---
title: Auditování faktur a klíčových dat v systému závazků
description: Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e1af0dac107be6009eb3ca576c49ac5abbd9848
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139929"
---
# <a name="audit-invoices-and-key-data-in-ap-system"></a>Auditování faktur a klíčových dat v systému závazků

[!include [banner](../../includes/banner.md)]

Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty. Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur. 

Na stránce Parametry závazků zajistěte, že je vybrána možnost Povolit ověření párování faktur, pole Zaúčtovat fakturu s odchylkami je nastaveno na Vyžadovat schválení a pole Zásady párování řádků je nastaveno na Třícestné párování.

Tato procedura používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. Přejděte na **Všechny nákupní objednávky**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Účet dodavatele**.
4. Klikněte na tlačítko **OK**.
5. Klikněte na **Přidat řádek**.
6. Zadejte hodnotu do pole **Číslo zboží**.
7. V podokně akcí klikněte na možnost **Zakoupit**.
8. Klikněte na tlačítko **Potvrdit**.

## <a name="post-a-product-receipt"></a>Zaúčtování příjemky produktu
1. V podokně akcí klikněte na možnost **Přijmout**.
2. Klikněte na **Příjemka produktu**.
3. Zadejte hodnotu do pole **Příjemka produktu**.
4. Klikněte na tlačítko **OK**.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Zaznamenání a párování faktury dodavatele s příjemkou produktu
1. V podokně akcí klikněte na **Faktura > Faktura**.
2. Zadejte hodnotu do pole **Číslo**.
3. Kliknutím na **Výchozí od: Objednané množství** otevřete dialogové okno.
4. Vyberte možnost v poli **Výchozí množství pro řádky**.
5. Klikněte na tlačítko **OK**.
6. Klepněte na tlačítko **Ano**.
7. Klikněte na **Spárovat příjemky produktu**.
8. Klikněte na tlačítko **OK**.
9. V podokně akcí klikněte na položku **Přehled**.
10. Klikněte na položku **Podrobnosti párování**.

