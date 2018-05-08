---
title: "Přecenění cizí měny pro bankovní účty"
description: "Toto téma obsahuje informace o přecenění cizí měny pro bankovní účty."
author: ShylaThompson
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7e04c046aac0825a6a9d2b2b439bc2261ed61f16
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="currency-revaluation-for-bank-account-transactions"></a>Přecenění měny pro transakce bankovních účtů

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a>Přecenění částek v cizí měně pro transakce bankovního účtu

> [!IMPORTANT]
> Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v Polsku.

Přecenění částek v cizí měně můžete provést pro bankovní transakce. Poté můžete vytvořit sestavu pro zobrazení bankovních transakcí, které mají úpravy pro přecenění cizí měny.

1. Vyberte **Řízení hotovosti a banky** &gt; **pravidelné úlohy** &gt; **Banka - kurzové vyrovnání (FIFO/LIFO)**.
2. Do pole **K datu** zadejte koncové datum přecenění. Výpočet zahrnuje pouze transakce s datem, které je před zadaným datem.
3. Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** &gt; **přidat** k přidání bankovního účtu. Pokud nezadáte bankovní účet, jsou přeceněny částky pro všechny bankovní účty.
4. Vyberte **OK** a stránku dotazu zavřete.
5. Na stránce **Přecenění cizí měny** zaškrtněte políčko **Přepočet** k přecenění částek v cizí měně pro všechna otevřená období.

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a>Vytvořte sestavu pro zobrazení bankovních transakcí, které mají úpravy pro přecenění cizí měny.

> [!IMPORTANT]
> Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v Polsku.

1. Vyberte **řízení hotovosti a banky** &gt; **dotazy a sestavy** &gt; **banka – sestava kurzového vyrovnání**.
2. Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** k vyhledání jednoho nebo více bankovních účtů, pro které mají být zobrazeny údaje.
3. Volitelné: V poli **Bankovní účet** vyberte bankovní účet. Pokud toto pole ponecháte prázdné, bude sestava zahrnovat podrobnosti bankovních transakcí pro všechny bankovní účty.
4. Klepnutím na tlačítko **OK** sestavu vygenerujte. 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a>Výpočet vyrovnání kurzových rozdílů pro transakce bankovního účtu

> [!IMPORTANT]
> Tato část se vztahuje pouze na právnické osoby, které mají primární adresu v České republice, Estonsku, Litvě nebo Lotyšsku.

Musíte přecenit a upravit bankovní účty, pokud je mezi zúčtovací měnou a měnou vykazování rozdíl směnného kurzu. Pomocí této úlohy můžete vypočítat správný zůstatek ve zúčtovací měně a v měně pro vykazování pro bankovní účty.

1. Přejděte do nabídky **Pokladna a banka** &gt; **Nastavení** &gt; **Parametry pokladny a banky**.
2. Na kartě **Číselné řady** v poli **Reference** vyberte číselnou řadu pro referenci **Banka - úprava cizí měny**.
3. Zavřete stránku.
4. Vyberte **hlavní kniha** &gt; **nastavení** &gt; **měna** &gt; **směnné kurzy**. Na stránce **Směnné kurzy v měně** můžete definovat směnný kurz mezi dvěma měnami nebo párem měn.
5. Po skončení stránku zavřete.
6. Vyberte **hlavní kniha** &gt; **nastavení** &gt; **Hlavní kniha**. V polích **Nerealizované zisky** a **Nerealizované ztráty** vyberte hlavní účet, pro který jsou zaúčtovány směnné kurzy.
7. Zavřete stránku.
8. Vyberte **řízení hotovosti a banky** &gt; **pravidelné úlohy** &gt; **přecenění cizí měny**.
9. V poli **K datu** vyberte datum přecenění nebo datum úpravy.
10. V **od měny** vyberte aktuální kód měny. V poli **Do měny** vyberte měnu, ve které se mají provádět úpravy.
11. Vyberte **záznamy, které chcete zahrnout** &gt; **filtr** bankovního účtu, a poté vyberte **OK**.
12. Na stránce **přecenění cizí měny** vyberte **OK**. Vypočítá se úprava transakcí bankovního účtu ve vybraném datu.

> [!NOTE]
> V hlavní knize můžete zobrazit dvě samostatné transakce: jednu pro zúčtovací měnu a druhou pro měnu vykazování.

