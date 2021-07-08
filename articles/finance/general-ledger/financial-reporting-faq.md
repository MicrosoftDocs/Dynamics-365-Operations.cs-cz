---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266626"
---
# <a name="financial-reporting-faq"></a>Nejčastější dotazy k finančnímu výkaznictví

Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a>Jak omezím přístup k sestavě pomocí zabezpečení stromu?

Následující příklad ukazuje, jak omezit přístup k sestavě pomocí zabezpečení stromu.

Ukázková společnost USMF má sestavu **rozvahy**, ke které by neměli mít přístup všichni uživatelé finančního výkaznictví. Zabezpečení stromu můžete použít k omezení přístupu k jedné sestavě, aby k ní měl přístup pouze konkrétní uživatel.

1. Přihlaste se do Financial Reporter Report Designer.
2. Vyberte **Soubor \> Nový \> Definice stromu** pro vytvoření definice nového stromu.
3. Dvakrát klikněte (nebo dvakrát klepněte) na řádek **Souhrn** ve sloupci **Zabezpečení jednotky**.
4. Zvolte **Uživatelé a skupiny**.
5. Vyberte uživatele nebo skupiny vyžadující přístup k této sestavě.
6. Zvolte možnost **Uložit**.
7. V definici sestavy přidejte svou novou definici stromu.
8. V definici stromu vyberte **Nastavení**. Poté v možnosti **Výběr organizační jednotky** vyberte **Zahrnout všechny jednotky**.

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a>Jak zjistím, které účty neodpovídají mým zůstatkům?

Pokud máte sestavu, který nemá odpovídající zůstatky, použijte k identifikaci každého účtu a odchylky následující postupy.

### <a name="in-financial-reporter-report-designer"></a>V Financial Reporter Report Designer

1. Vytvořte novou definici řádku.
2. Zvolte **Upravit \> Vložit řádky z dimenzí**.
3. Vyberte **Hlavní účet**.
4. Vyberte **OK**.
5. Uložte definici řádku.
6. Vytvořte novou definici sloupce.
7. Vytvořte novou definici sestavy.
8. Vyberte **Nastavení** a zrušte označení této možnosti.
9. Vygenerujte sestavu. 
10. Exportujte sestavu do Microsoft Excel.

### <a name="in-dynamics-365-finance"></a>V Dynamics 365 Finance

1. Přejděte na **Hlavní kniha \> Dotazy a sestavy \> Předvaha**.
2. Nastavte následující pole:

    - **Od data** – Zadejte počáteční datum fiskálního roku.
    - **Do data** – Zadejte datum, pro které generujete sestavu.
    - **Finanční dimenze** – Nastavte toto pole na **Hlavní účet nastaven**.

3. Vyberte **Vypočítat**.
4. Exportujte sestavu do aplikace Excel.

Nyní byste měli být schopni zkopírovat data ze sestavy Excelu Financial Reporter do sestavy **Předvahy** a porovnat sloupce **Konečný zůstatek**.

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a>Když navrhuji sestavu v aplikaci Report Designer nebo když generuji finanční sestavu, obdržel jsem následující zprávu: „Operaci nelze dokončit kvůli problému v rámci poskytovatele dat.“ Jak mám reagovat?

Zpráva označuje, že došlo k problému, když se systém pokusil načíst finanční metadata z datového tržiště během vašeho používání finančního výkaznictví. Na tento problém lze odpovědět dvěma způsoby:

- Zkontrolujte stav integrace dat přechodem na **Nástroje \> Stav integrace** v aplikaci Report Designer. Pokud je integrace neúplná, počkejte na její dokončení. Až dostanete zprávu, vraťte se ke své předchozí činnosti.
- Kontaktujte podporu, abyste problém identifikovali a vyřešili ho. V systému mohou být nekonzistentní data. Technici podpory vám mohou pomoci identifikovat tento problém na serveru a najít konkrétní data, která mohou vyžadovat aktualizaci.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
