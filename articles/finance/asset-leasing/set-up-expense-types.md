---
title: Nastavení typů výdajů
description: Toto téma vysvětluje, jak nastavit typy výdajů v leasingu majetku.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseExpenseTypeTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1e5af18921314061ba3256559d7fc7ceacef606a9b3d5cc3a8047c83494074fc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715135"
---
# <a name="set-up-expense-types"></a>Nastavení typů výdajů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak nastavit typy výdajů v leasingu majetku. Náklady, které nejsou představovány harmonogramem plateb, jsou známy jako *výdajové náklady*. Mezi příklady těchto nákladů patří majetkové daně, náklady na údržbu společného prostoru a náklady na pojištění.

## <a name="add-an-administrative-expense-type"></a>Přidání typu administrativních výdajů

1. Přejděte na **Leasing majetku \> Nastavení \> Typy výdajů**.
2. Zvolte **Nové**.
3. Do příslušných polí zadejte nový typ výdajů a popis.

## <a name="assign-accounts-to-administrative-costs"></a>Přiřazení účtů administrativním nákladům

Dále byste měli přidružit účty k typům výdajů. Z těchto účtů bude proveden odpis, když budou zaúčtovány položky plánu výdajů. Ofsetový účet je specifikován na řádcích **Harmonogram plateb zachraňovacích nákladů** každého leasingu.

1. Přejděte do nabídky **Leasing majetku \> Nastavení \> Parametry leasingu majetku**.
2. Na kartě **Účty** na pevné záložce **zachraňovací náklady** v poli **Typ výdaje** vyberte typ výdaje.
3. Vyberte **přidat**.
4. V poli **Typ knihy** vyberte typ knihy, který má být propojen s administrativními náklady.

    > [!NOTE]
    > K jednomu výdajovému účtu lze připojit více typů knih.

5. V poli **Kód účtu** zadejte, na které leasingy by se kniha měla vztahovat:

    - **Vše** - Aplikuje knihu pro všechny leasingy.
    - **Skupina** - Aplikuje knihu na konkrétní skupinu leasingů.
    - **Tabulka** - Aplikuje knihu pro konkrétní leasingy.

6. Pokud jste vybrali **Skupina** nebo **Tabulka** v poli **Kód účtu**, vyberte číslo účtu nebo číslo skupiny v poli **Číslo účtu/skupiny**.
7. V příslušných polích vyberte hlavní účet finančního leasingu a hlavní účet operativního leasingu.

Po dokončení těchto kroků můžete přidat výdaje prostřednictvím řádek **Harmonogram plateb exekutivních nákladů** na stránce **Podrobnosti o leasingu** vybraného leasingu. Alternativně můžete přidat náklady při vytváření nového pronájmu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
