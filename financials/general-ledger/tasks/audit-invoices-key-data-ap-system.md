--- 
title: "Auditování faktur a klíčových dat pro závazky"
description: "Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 38cc5587d970d05492638ed349484e6c002d5363
ms.contentlocale: cs-cz
ms.lasthandoff: 07/28/2017

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a>Auditování faktur a klíčových dat pro závazky

[!include[task guide banner](../../includes/task-guide-banner.md)]

Pokud od dodavatele obdržíte fakturu za zboží nebo služby na nákupní objednávce, mohou obchodní procesy vyžadovat, aby zboží nebo služby byly před schválením této faktury k platbě skutečně přijaty. Před prvním krokem ověřte, že je vybraný konfigurační klíč Párování faktur. 

Na stránce Parametry závazků zajistěte, že je vybrána možnost Povolit ověření párování faktur, pole Zaúčtovat fakturu s odchylkami je nastaveno na Vyžadovat schválení a pole Zásady párování řádků je nastaveno na Třícestné párování.

Tato procedura používá ukázkovou společnost USMF. Manažer závazků nebo osoba s rolí vedoucího účetnictví by prováděl tyto kroky.


## <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky
1. Přejděte na Všechny nákupní objednávky.
2. Klikněte na položku Nová.
3. V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Zadejte hodnotu do pole Účet dodavatele.
5. Klikněte na tlačítko OK.
6. Klikněte na položku Přidat řádek.
7. Zadejte hodnotu do pole Číslo zboží.
8. V podokně akcí klikněte na položku Nákup.
9. Klikněte na tlačítko Potvrdit.

## <a name="post-a-product-receipt"></a>Zaúčtování příjemky produktu
1. V podokně akcí klikněte na položku Přijmout.
2. Klikněte na položku Příjemka produktu.
3. Označte v seznamu vybraný řádek.
4. Zadejte hodnotu do pole Příjemka produktu.
5. Klikněte na tlačítko OK.

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a>Zaznamenání a párování faktury dodavatele s příjemkou produktu
1. V podokně akcí klikněte na položku Faktura.
2. Klikněte na položku Faktura.
3. Zadejte hodnotu do pole Číslo.
4. Kliknutím na Výchozí od: Objednané množství otevřete dialogové okno.
5. Vyberte volbu v poli Výchozí množství pro řádky.
6. Klikněte na tlačítko OK.
7. Klepněte na tlačítko Ano.
8. Klikněte na Spárovat příjemky produktu.
9. Klikněte na tlačítko OK.
10. V podokně akcí klikněte na položku Přehled.
11. Klikněte na položku Párování – podrobnosti.


