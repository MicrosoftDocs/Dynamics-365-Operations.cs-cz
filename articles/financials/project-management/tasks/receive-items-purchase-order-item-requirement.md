---
title: Přijetí položek na nákupní objednávce z požadavku na položku
description: Toto téma vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867288"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Přijetí položek na nákupní objednávce z požadavku na položku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak přijmout položky na nákupní objednávce z požadavku na položku.

Použitím požadavků zboží namísto transakcí zboží můžete naplánovat dodávku těsně před vlastním použitím zboží, vytvořit prodejní objednávku, zahrnout zboží do rámce obchodní smlouvy nebo zahrnout požadavek na zboží do provozního plánování. 

Tato úloha používá sadu dat USSI.

1. V navigačním podokně přejděte na **Moduly > Řízení projektů a účetnictví > Projekty > Všechny projekty**.
2. Vyberte odkaz na požadovaném řádku v seznamu.
3. V podokně akcí zvolte **Plán**.
4. Vyberte **Požadavky položek**
5. Zvolte **Nové**.
6. V novém řádku vložte nebo vyberte hodnotu v poli **Číslo položky**.
7. Zadejte číslo do pole **Množství**.
8. Zvolte **Uložit**.
9. V podokně akcí vyberte **Spravovat**.
10. Vyberte **Funkce**.
11. Vyberte **Vytvořit nákupní objednávku**.
12. Zaškrtněte políčko **Zahrnout vše**.
13. V poli **Účet dodavatele** zadejte nebo vyberte hodnotu.
14. Vyberte **OK**.
15. V navigačním podokně přejděte na **Moduly > Závazky > Nákupní objednávky > Všechny nákupní objednávky**.
16. Vyberte odkaz na požadovaném řádku v seznamu.
17. V podokně akcí klikněte na možnost **Zakoupit**.
18. Vyberte **Potvrdit**.
19. V podokně akcí klikněte na možnost **Přijmout**.
20. Vyberte **Příjemka produktu**.
21. Zadejte hodnotu do pole **Příjemka produktu**.
22. Vyberte **OK**.

