---
title: Stanovení způsobu platby odběratele
description: Vytvořte metodu platby pro úhrady odběratelů.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab035c6268b701c78da32d589e99ece38c31781d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "348956"
---
# <a name="establish-customer-method-of-payment"></a>Stanovení způsobu platby odběratele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vytvořte metodu platby pro úhrady odběratelů. Tento úkol používá ukázkovou společnost USMF.

1. Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.
2. Klikněte na položku Nová.
3. V poli Metoda platby zadejte Identifikátor pro metodu platby.
    * ID metody platby je zobrazeno ve fakturách a platbách, proto vyberte dostatečně popisný název, aby bylo možné pochopit, jaký typ platby je zaznamenán, a pro jaký bankovní účet.  
4. Zadejte popis do pole Popis.
5. Vyberte, jaký stav platby je nutný pro zaúčtování platby.
    * Při vytváření platby odběratele je možné je zaúčtovat pouze pokud stav platby odpovídá stavu platby, který je definován zde.  
6. Vyberte způsob jakým odběratelé musí vytvářet platby pro faktury.
    * Tato možnost se používá pouze při spuštění návrhu platby. Návrh platby lze použít pro platby odběratelů při provádění přímých debetů a zavedení fondů z bankovních účtů zákazníků.  
7. Vyberte typ platby.
    * Typ platby vám pomůže určit, zda u platby dojde k ověření, nebo nikoli.  
8. Vyberte, do jakého typu účtu budou platby zaúčtovány.
    * Banka obvykle vybírá tuto možnost.  
9. Vyberte bankovní účet, do kterého bude zaznamenána tato platba.
10. Zadejte typ bankovní transakce pro identifikaci typu platby používané bankou.
    * Typ bankovní transakce se používá v průběhu procesu odsouhlasení banky, umožňuje odsouhlasení usnadnit.  
11. Určete, zda platby budou dočasně zaúčtovávat na překlenovací účet.
    * Pokud budete chtít vyzkoušet plovoucí čas pro platbu a banku tak odbavit, použijte funkci Překlenování. Platba se dočasně zaúčtuje do účtu hlavní knihy, dokud nedojde k odbavení banky, což způsobí přesunutí platby na bankovní účet, která jste definovali zde.  
12. Zadejte hlavní účet použitý pro překlenovací zaúčtování.
    * Toto je hlavní účet, na který se platba dočasně zaúčtuje, používáte-li překlenování.  
13. Použijte kartu Formátu souboru pro definování nastavení pro elektronické platby.
14. Použijte kartu Řízení platby k definování polí, která jsou povinná.
    * Pokud například potřebujete, aby všechny platby s touto metodou byly uloženy, můžete vybrat tuto možnost na této kartě.  
15. Na kartě Atributy platby definujte, které atributy platby chcete použít pro tuto metodu platby.
16. Klikněte na položku Uložit.

