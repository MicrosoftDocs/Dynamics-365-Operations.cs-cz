---
title: Nejčastější dotazy k finančnímu výkaznictví
description: Toto téma poskytuje odpovědi na nejčastější dotazy týkající se finančního výkaznictví.
author: jiwo
ms.date: 07/07/2021
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
ms.openlocfilehash: dd493e855e45362c1681dc9cdfbbcb71f7627d64624cd093eadab32fd966c174
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733604"
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
- Kontaktujte podporu, abyste problém identifikovali a vyřešili ho. V systému mohou být nekonzistentní data. Technici podpory vám mohou pomoci identifikovat tento problém na serveru a najít konkrétní data, která mohou vyžadovat aktualizaci.

## <a name="how-does-the-selection-of-historical-rate-translation-affect-report-performance"></a>Jak výběr převodů historických kurzů ovlivňuje výkon sestav?

Historický kurz se obvykle používá u nerozděleného zisku, nemovitostí, pozemků a vybavení a účtů jmění. Historický kurz může být požadován na základě pokynů panelu FASB (Financial Accounting Standards Board) a pravidel GAAP. Další informace viz [Možnosti měny ve finančním výkaznictví](financial-reporting-currency-capability.md).

## <a name="how-many-types-of-currency-rate-are-there"></a>Kolik typů kurzů měny existuje?

Existují tři typy:

- **Aktuální kurz** – Tento typ se obvykle používá u rozvahových účtů. Obvykle je nazýván *spotovým směnným kurzem* a může jít o kurz k poslednímu dni v měsíci nebo k jinému předem určenému datu.
- **Průměrný kurz** – Tento typ se obvykle používá u účtů výsledovky (zisk/ztráta). Průměrný kurz můžete nastavit tak, aby šlo buď o jednoduchý průměr, nebo o vážený průměr.
- **Historický kurz** – Tento typ se obvykle používá u nerozděleného zisku, nemovitostí, pozemků a vybavení a účtů jmění. Tyto účty mohou být vyžadovány na základě pokynů panelu FASB (Financial Accounting Standards Board) nebo pravidel GAAP.

## <a name="how-does-historical-currency-translation-work"></a>Jak funguje převod historických měn?

Kurzy jsou specifické pro datum transakce. Proto je každá transakce převedena jednotlivě na základě nejbližšího směnného kurzu.

U převodů historických měn lze místo podrobností jednotlivých transakcí použít předem vypočítané zůstatky období. Toto chování se liší od chování pro převod aktuálního kurzu.

## <a name="how-does-historical-currency-translation-affect-performance"></a>Jak převod historických měn ovlivní výkon?

Při aktualizaci dat uvedených v sestavách může dojít ke zpoždění, protože částky je třeba přepočítat kontrolou podrobností transakce. Toto zpoždění se spustí pokaždé, když se aktualizují kurzy nebo když se zaúčtuje více transakcí. Pokud jsou například několikrát denně nastavovány tisíce účtů pro historický převod, aktualizace údajů v sestavě může trvat až hodinu. Na druhou stranu, pokud existuje menší počet konkrétních účtů, lze doby zpracování aktualizací dat sestavy zkrátit na minuty nebo méně.

Podobně platí, že když se generují sestavy pomocí převodu měny pro účty historického typu, budou provedeny další výpočty na transakci. V závislosti na počtu účtů se doba generování sestavy může více než zdvojnásobit.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
