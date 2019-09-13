---
title: Vytváření skupin oprávnění POS
description: Toto téma vysvětluje, jak vytvořit skupinu oprávnění POS.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e6782c60aa659523775cc6c4eb1694430a4bf4f
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914777"
---
# <a name="create-pos-permission-groups"></a>Vytváření skupin oprávnění POS

[!include[task guide banner](../includes/task-guide-banner.md)]

Toto téma vysvětluje, jak vytvořit skupinu oprávnění POS. Tento úkol byl vytvořen pomocí ukázkových dat společnosti USRT. Tento úkol je určen pro roli Manažer maloobchodních operací.

1. V navigačním podokně přejděte na **Moduly > Maloobchod > Zaměstnanci > Skupiny oprávnění**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **ID skupiny oprávnění POS**.
4. Zadejte hodnotu do pole **Popis**.
5. Vyberte možnost **Ano** v poli **Zobrazit časové záznamy**. Nyní můžete povolit nebo zakázat různá oprávnění pro skupinu oprávnění POS. U některých oprávnění můžete nastavit hodnotu, která se použije k vyhodnocení, zda může uživatel POS provést akci. Tento průvodce úkolem povolí několik oprávnění, která můžete udělit pokladníkovi.  
6. Vyberte možnost **Ano** v poli **Povolit vytvoření objednávky**.
7. Vyberte možnost **Ano** v poli **Povolit úpravu objednávky**.
8. Vyberte možnost **Ano** v poli **Povolit načtení objednávky**.
9. Vyberte možnost **Ano** v poli **Povolit změnu hesla**.
10. Vyberte možnost **Ano** v poli **Povolit uzavření bez zadání částky**.
11. Zvolte **Uložit**. Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti. 
12. V navigačním podokně přejděte na **Moduly > Lidské zdroje > Práce > Práce**.
13. Dále přiřadíme skupinu oprávnění POS úloze. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
14. Vyberte možnost **Upravit**.
15. Rozbalte část **Klasifikace úlohy**.
16. V poli Skupina oprávnění POS zadejte nebo vyberte hodnotu. Pozice všech pracovníků pro tuto úlohu budou používat toto nastavení skupiny oprávnění POS, pokud oprávnění POS pracovníků nebylo přepsáno na úrovni jejich pozice.  
17. Zvolte **Uložit**. Po uložení změn bude nutné spustit plán Distribuce pracovníků a uplatnit tak změny v maloobchodní síti.  

