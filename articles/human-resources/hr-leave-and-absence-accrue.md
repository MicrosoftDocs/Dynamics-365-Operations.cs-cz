---
title: Časově rozlišit plány pracovního volna a absence
description: Můžete časově rozlišit volno a absenci v Dynamics 365 Human Resources pro více zaměstnanců nebo pro jednotlivce.
author: andreabichsel
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ddd4c55f6ebfbe91fb949a92cb379f51d826c465
ms.sourcegitcommit: cee7887282d372c756c5c11f76684315f249bba5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/24/2021
ms.locfileid: "6303457"
---
# <a name="accrue-leave-and-absence-plans"></a>Časově rozlišit plány pracovního volna a absence

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Můžete časově rozlišit volno a absenci v Dynamics 365 Human Resources pro více zaměstnanců nebo pro jednotlivce.

## <a name="accrue-leave-and-absence-for-multiple-employees"></a>Časově rozlišit pracovní volno a absenci pro více zaměstnanců

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V nabídce **Správa pracovního volna** vyberte **časové rozlišení pracovního volna a plánů absencí**.

3. Zobrazí se dialogové okno **Časové rozlišení plánů pracovního volna a absence**. V **Časové rozlišení k** vyberte **Dnešní datum** nebo vyberte **Vlastní datum** a zadejte vlastní datum.

4. Pokud chcete spustit časové rozlišení pro všechny společnosti, vyberte **Všechny společnosti**. Pokud chcete zpracovat časové rozlišení pro jediný plán pracovního volna, vyberte **Ne** pro **Všechny plány** a potom vyberte a **Plán pracovního volna**. Pokud vyberete všechny společnosti, nemůžete vybrat individuální plán pracovního volna.

5. Chcete-li spustit proces časového rozlišení na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

    1. Zadejte informace pro proces časového rozlišení.
    2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a pak vyberte **OK**.
    3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.
    4. Vyberte **OK**. Proces časového rozlišení bude spuštěn s nastavenými parametry. 

## <a name="accrue-leave-and-absence-for-an-employee"></a>Časově rozlišit pracovní volno a absenci pro zaměstnance

1. V záznamu zaměstnance vyberte možnost **Pracovní volno**.

2. Vyberte **Časové rozlišení plánů pracovního volna a absence**.

3. Zobrazí se dialogové okno **Časové rozlišení plánů pracovního volna a absence**. V **Časové rozlišení k** vyberte **Dnešní datum** nebo vyberte **Vlastní datum** a zadejte vlastní datum.

4. Pokud chcete spustit časové rozlišení pro všechny společnosti, vyberte **Všechny společnosti**. Pokud chcete zpracovat časové rozlišení pro jediný plán pracovního volna, vyberte **Ne** pro **Všechny plány** a potom vyberte a **Plán pracovního volna**. Pokud vyberete všechny společnosti, nemůžete vybrat individuální plán pracovního volna.

5. Chcete-li spustit proces časového rozlišení na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

   1. Zadejte informace pro proces časového rozlišení.

   2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.

   3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.

   4. Vyberte **OK**. Proces časového rozlišení bude spuštěn s nastavenými parametry.

## <a name="delete-leave-and-absence-accruals-for-multiple-employees"></a>Odstranit časová rozlišení pracovního volna a absence pro více zaměstnanců

Odstranit záznamy o časovém rozlišení pro určitý plán a rozsah dat Data časového rozlišení musí být datována dnes nebo v budoucnosti.

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V nabídce **Správa pracovního volna** vyberte **Odstranit časová rozlišení pracovního volna a absence**.

3. V dialogovém okně **Odstranit časová rozlišení pracovního volna a absence** vyberte **Plán pracovního volna**.

4. Pokud je to možné, zvolte **Odstranit vyrovnání zůstatků**.

5. Zadejte nebo vyberte **Datum časového rozlišení volna**. Toto datum musí být buď dnešní, nebo v budoucnosti.

6. Vyberte **OK**. Proces časového rozlišení odstraní časová rozlišení s nastavenými parametry.

## <a name="delete-leave-and-absence-accruals-for-a-single-employee"></a>Odstranit časová rozlišení pracovního volna a absence pro jednoho zaměstnance

1. V záznamu zaměstnance vyberte možnost **Pracovní volno**.

2. Vyberte **Odstranit časové rozlišení plánů pracovního volna a absence**.

3. V dialogovém okně **Odstranit časová rozlišení pracovního volna a absence** vyberte **Plán pracovního volna**.

4. Pokud je to možné, zvolte **Odstranit vyrovnání zůstatků**.

5. Zadejte nebo vyberte **Datum časového rozlišení volna**. Toto datum musí být buď dnešní, nebo v budoucnosti.

6. Vyberte **OK**. Proces časového rozlišení odstraní časová rozlišení s nastavenými parametry.

## <a name="review-leave-accrual-and-deletion-processes"></a>Zkontrolovat procesy časového rozlišení a odstranění

**Vynechávat audit časového rozlišení** se zobrazí pokaždé, když spustíte nebo odstraníte časové rozlišení pro jednoho nebo všechny zaměstnance. Zobrazí se také datum a osoba, která akci provedla.

1. Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.

2. V nabídce **Správa pracovního volna** vyberte **Odstranit audit časového rozlišení pracovního volna**.

## <a name="leave-accrual-transaction-auditing"></a>Audit transakce časového rozlišení pracovního volna

Tato funkce pomáhá správcům pracovního volna a absence porozumět časově rozlišeným transakcím pracovního volna a absence souvisejícím se zůstatky volna zaměstnance pro konkrétní typ volna.

Chcete-li zobrazit podrobnosti transakce:

1. V záznamu zaměstnance vyberte možnost **Pracovní volno**.

2. Vyberte **Zobrazit volno** a potom vyberte kartu **Zůstatky**.

Chcete-li zobrazit akruální transakce související s konkrétním typem dovolené, vyberte číselnou hodnotu ve sloupci **Aktuální zůstatek**.

Chcete-li zobrazit podrobnosti transakce pro konkrétní částku časového rozlišení, vyberte řádek časového rozlišení a otevřete panel **Související informace** pravo a poté otevřete sekci **Podrobnosti transakce**. Sekce Podrobnosti transakce zobrazuje:

- Změny zůstatku typu dovolené zaměstnance
- Podrobnosti o zaměstnání pro dané akruální období
- Podrobnosti o akruálním období a sazbách
- Jakékoli změny provedené za účelem konfigurací plánu pracovního volna

![Audit transakce časového rozlišení zobrazení pracovního volna](media/hr-leave-and-absence-accrue-audit.png)

## <a name="see-also"></a>Viz také

[Přehled pracovního volna a absencí](hr-leave-and-absence-overview.md)</br>
[Vytvoření plánu pracovního volna a absence](hr-leave-and-absence-plans.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
