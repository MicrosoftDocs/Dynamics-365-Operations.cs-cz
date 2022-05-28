---
title: Stanovení způsobu platby odběratele
description: Toto téma vysvětluje, jak vytvořit metodu platby pro platby odběratelů.
author: ShivamPandey-msft
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e8974ea20497124e24e95b3761317daf126839
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713889"
---
# <a name="establish-customer-method-of-payment"></a>Stanovení způsobu platby odběratele

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit metodu platby pro platby odběratelů. Tento úkol využívá ukázkovou společnost USMF.

1. V navigačním podokně přejděte na **Moduly > Pohledávky > Nastavení plateb > Metody platby**.
2. Zvolte **Nové**.
3. V poli **Metoda platby** zadejte Identifikátor pro metodu platby. ID metody platby je zobrazeno ve fakturách a platbách, proto vyberte dostatečně popisný název, aby bylo možné pochopit, jaký typ platby je zaznamenán, a pro jaký bankovní účet.  
4. Zadejte popis do pole **Popis**.
5. Vyberte, jaký stav platby je nutný pro zaúčtování platby. Při vytváření platby odběratele je možné je zaúčtovat pouze pokud stav platby odpovídá stavu platby, který je definován zde.  
6. Vyberte způsob jakým odběratelé musí vytvářet platby pro faktury. Tato možnost se používá pouze při spuštění návrhu platby. Návrh platby lze použít pro platby odběratelů při provádění přímých debetů a zavedení fondů z bankovních účtů zákazníků.  
7. Vyberte typ platby. Typ platby vám pomůže určit, zda u platby dojde k ověření, nebo nikoli.  
8. Vyberte, do jakého typu účtu budou platby zaúčtovány. Banka obvykle vybírá tuto možnost.  
9. Vyberte bankovní účet, do kterého bude zaznamenána tato platba.
10. Zadejte typ bankovní transakce pro identifikaci typu platby používané bankou. Typ bankovní transakce se používá v průběhu procesu odsouhlasení banky, umožňuje odsouhlasení usnadnit.  
11. Určete, zda platby budou dočasně zaúčtovávat na překlenovací účet. Pokud budete chtít vyzkoušet plovoucí čas pro platbu a banku tak odbavit, použijte funkci Překlenování. Platba se dočasně zaúčtuje do účtu hlavní knihy, dokud nedojde k odbavení banky, což způsobí přesunutí platby na bankovní účet, která jste definovali zde.  
12. Zadejte hlavní účet použitý pro překlenovací zaúčtování. Toto je hlavní účet, na který se platba dočasně zaúčtuje, používáte-li překlenování.  
13. Použijte kartu **Formátu souboru** pro definování nastavení pro elektronické platby.
14. Použijte kartu **Řízení platby** k definování polí, která jsou povinná. Pokud například potřebujete, aby všechny platby s touto metodou byly uloženy, můžete vybrat tuto možnost na této kartě.  
15. Na kartě **Atributy platby** definujte, které atributy platby chcete použít pro tuto metodu platby.
16. Zvolte **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
