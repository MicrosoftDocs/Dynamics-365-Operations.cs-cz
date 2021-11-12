---
title: Plánování místní účtové osnovy
description: Toto téma poskytuje informace, které vám pomohou naplánovat účtovou osnovu, když máte zákonné/místní požadavky pro vaši organizaci.
author: veneva
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a99e4ef3355188f574930c1d885e53fcb3134ad1
ms.sourcegitcommit: c4500b626667185643b3a2e7fc3a004d42198d07
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/29/2021
ms.locfileid: "7725168"
---
# <a name="plan-your-local-chart-of-accounts"></a>Plánování místní účtové osnovy

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace, které vám pomohou naplánovat účtovou osnovu, když vaše organizace zahrnuje právnické osoby, které musí splňovat požadavky pro konkrétní lokality, kde podnikají. Toto téma používá k popisu účtových osnov následující výrazy:

- **Globální** – Účtová osnova, kterou organizace používá globálně. Ve většině případů budete konsolidovat podle této účtové osnovy.
- **Místní** – Účtová osnova, kterou používají právnické osoby v konkrétní zemi nebo regionu.
- **Sdílená** – Účtová osnova, kterou může používat více právnických osob. Sdílet lze jak globální účtovou osnovu, tak místní účtovou osnovu.

Můžete vytvořit a sdílet více účtových osnov. Sdílenou účtová osnovu může používat více právnických osob, avšak každé právnické osobě může být přidělena pouze jeden účtová osnova. Účtové osnovy, které používá právnická osoba, jsou definovány na stránce **Kniha**.

Při navrhování účtové osnovy se mnoho organizací zaměřuje na globální účtovou osnovu. Možnost sdílené účtové osnovy umožňuje vytvoření globální účtové osnovy. Vytvoření a používání jednotné účtové osnovy přináší výhody. Například správa a kontrola, údržba a podávání zpráv jsou jednodušší.

Většina organizací preferuje globální účtovou osnovu a je to nejjednodušší typ implementace. Některé právnické osoby nicméně vyžadují místní účtovou osnovu z následujících důvodů:

- Místní zákonné požadavky
- Požadavky místních účetních standardů
- Oborové požadavky
- Požadavky na výkaznictví a analýzy specifické pro společnost

Pokud vaše organizace vyžaduje, aby právnická osoba používala místní účtovou osnovu, máte dvě možnosti, jak ji implementovat:

- Přiřaďte globální účtovou osnovu a definujte další způsoby splnění místních požadavků.
- Přiřaďte místní účtovou osnovu právnické osobě a definujte vztahy ke globální účtové osnově.

Organizační struktura a struktura výkaznictví určují použitou možnost.

[![Diagram ukazující, jak organizační struktura určuje, zda použít globální nebo místní účtovou osnovu](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

Pokud je globální účtová osnova přiřazena právnické osobě, jsou k dispozici následující možnosti pro splnění místních požadavků na vykazování:

- Proveďte místní konsolidaci.
- Ke sledování místní účtové osnovy použijte finanční dimenzi.
- Vytvořte místní hlavní účty v globální účtové osnově.
- Proveďte externí mapování na místní účtovou osnovu.

Pokud je místní účtová osnova přiřazena právnické osobě, jedná možnost, která je momentálně k dispozici pro splnění globálních požadavků na vykazování, je globální konsolidace.

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>Globální účtová osnova přiřazená právnické osobě

Pokud musíte globální účtovou osnovu přiřadit právnické osobě, jsou k dispozici čtyři možnosti konfigurace systému, jak bylo popsáno výše. Pro všechny čtyři možnosti je nakonfigurována jedna účtová osnova a propojena s každou právnickou osobou na stránce **Hlavní kniha**. Každá možnost pak používá jiný přístup ke splnění požadavků na lokalizaci. Následující části popisují kroky na vysoké úrovni pro konfiguraci systému pro požadavky na lokalizaci. Popisují také výhody a nevýhody jednotlivých možností.

### <a name="do-local-consolidation"></a>Provedení místní konsolidace

Místní konsolidace je doporučený přístup ke splnění požadavků na místní účtovou osnovu a využití funkcí systému, který byl pro tento účel navržen.

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>Nastavení konsolidace pro místní účtovou osnovu

1. Vytvořte jedinou globální účtovou osnovu, která bude obsahovat všechny požadované hlavní účty.
2. V každé právnické osobě přiřaďte globální účtovou osnovu na stránce **Hlavní kniha**.
3. Vytvořte konsolidační právnickou osobu pro každou požadovanou lokalizaci.
4. Proveďte jeden z následujících kroků:

    - Pokud je vyžadována pouze jedna lokalizace, nakonfigurujte konsolidační účet na stránce **Hlavní účet** nebo použijte stránky **Konsolidační skupiny** a **Dodatečné konsolidační účty**.
    - Pokud je vyžadována více než jedna lokalizace nebo pokud číslo účtu i název účtu vyžadují překlad, použijte stránky **Konsolidační skupiny** a **Dodatečné konsolidační účty** reprezentující požadavky na lokalizaci.

5. Spusťte proces konsolidace a převeďte hodnotu ze zdrojové právnické osoby, která používá globální účtovou osnovu, na konsolidační společnost, která používá místní účtovou osnovu.

#### <a name="advantages"></a>Výhody

- Tento přístup poskytuje konzistentní způsob práce v celé organizaci.
- Provede se jeden překlad místní polohy.
- Tento přístup podporuje překlad jak hlavního ID účtu, tak názvu každého hlavního účtu.
- Podporuje více lokalizací.

#### <a name="disadvantages"></a>Nevýhody

- Je vytvořena další konsolidační společnost.
- Je dokončen další konsolidační proces.
- Tento přístup může vykazovat v lokalizovaném grafu pouze po dokončení procesu konsolidace.

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>Ke sledování místní účtové osnovy použijte finanční dimenzi

Tento přístup používá finanční dimenzi, kde hodnoty finanční dimenze představují místní hlavní účty, které jsou vyžadovány pro lokalizaci. Funguje dobře, pokud je vyžadována pouze jedna lokalizace. S přidáním dalších lokalizací a finančních dimenzí se však stává méně použitelným.

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>Nastavení finanční dimenze pro místní účtové osnovy

1. Vytvořte jedinou globální účtovou osnovu, která bude obsahovat všechny požadované hlavní účty.
2. V každé právnické osobě přiřaďte globální účtovou osnovu na stránce **Hlavní kniha**.
3. Vytvořte finanční dimenzi, která představuje místní účtovou osnovu.
4. Vytvořte hodnoty finanční dimenze, která představuje hlavní účty v místních účtových osnovách.
5. Aktualizujte strukturu účtu tak, aby zahrnovala finanční dimenzi „místní účtová osnova“.
6. Zajistěte, aby finanční dimenze „místní účtová osnova“ měla vždy hodnotu a aby nepovolovala prázdnou hodnotu. Zvažte použití odvozených dimenzí nebo pevných dimenzí.
7. Vytvořte sadu finančních dimenzí, kde finanční dimenze „místní účtová osnova“ je první vybranou finanční dimenzí. Sadu finančních dimenzí lze použít při generování předvahy.

#### <a name="advantages"></a>Výhody

- Hlavní účty globálních i lokálních účtových osnov existují na transakční úrovni. Hlavní účet je globální a hodnota finanční dimenze je místní.
- Tento přístup poskytuje výkaznictví v reálném čase a pohledy na globální finanční pozici i místní finanční pozici.

#### <a name="disadvantages"></a>Nevýhody

- Pokud je v parametrech hlavní knihy pole **Hodnoty používané pro souhrnný účet** nastaveno na **Rozúčtování**, finanční dimenze, které představují hlavní účet pro náklad/majetek/výnos, budou pro souhrnný účet pohledávky a závazky nesprávně použity. Doporučujeme, abyste místo toho nastavili pole na zdrojový dokument, abyste zajistili použití správných hodnot finanční dimenze.
- Pokud je vyžadováno mnoho místních účtových osnov a pro všechny se používá jedna finanční dimenze, může být seznam použitých hodnot finančních dimenzí dlouhý a obtížně se s ním pracuje.
- Je-li vyžadováno mnoho místních účetních osnov a k reprezentaci každého z nich je použita samostatná finanční dimenze, může být použitelnost a výkon systému ovlivněn přidáním sad finančních dimenzí a finančních dimenzí.
- Doporučujeme pečlivě zvážit počet požadovaných finančních dimenzí, počet hodnot v každé z nich a počet sad finančních dimenzí, protože všechny tyto faktory mohou ovlivnit výkon systému.

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>Vytvoření místních hlavních účtů v globální účtové osnově

*Na co se editor textu ptal:* V tomto přístupu místní hlavní účty v globální účtové osnově zahrnují hlavní účty v místní účtové osnově v globální účtové osnově.

*Originální verze:* Místní hlavní účty v rámci globálního přístupu k CoA jsou takové, že místní hlavní účty CoA jsou zahrnuty do globálního CoA.

*Má to říkat toto:* V tomto přístupu jsou lokální hlavní účty v místní účtové osnově zahrnuty do globální účtové osnovy.


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>Nastavení místních hlavních účtů v globální účtové osnově

1. Vytvořte jednu účtovou osnovu, která bude obsahovat hlavní účty pro globální účtovou osnovu i pro místní účtovou osnovu.
2. V každé právnické osobě přiřaďte účtovou osnovu na stránce **Hlavní kniha**.
3. Vytvořte celkové účty v účtové osnově, abyste sečetli hlavní účty, které představují stejný účel.
4. Vytvořte přepsání právnické osoby na každém místním účtu, abyste zabránili transakcím od jiných právnických osob, pro které místní účet nebyl navržen.
5. Vytvořte přepisy právnických osob na každém globálním účtu, abyste zabránili transakcím z lokalizačních právnických osob.

#### <a name="advantages"></a>Výhody

- Zobrazení globální finanční pozice i místní finanční pozice v reálném čase je k dispozici ve specifických sestavách a ve specifických pohledech v systému, jako je rozvahová finanční zpráva. Lze k němu také přistupovat pomocí tlačítka **Doba** na celkovém účtu.
- V účtu hlavní knihy nemáte další segment.

#### <a name="disadvantages"></a>Nevýhody

- Celkové využití účtu a viditelnost jsou omezené. Například celkový počet účtů není viditelný na stránce seznamu **Předvaha**.
- Údržba vyžaduje větší úsilí.
- Vytváření finančních zpráv vyžaduje další manuální úsilí.

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>Provedení externího mapování na místní účtovou osnovu

Přijetí globální účtové osnovy předpokládá, že mapování a lokalizace spravujete mimo systém. V tomto přístupu stačí vytvořit jedinou globální účtovou osnovu v Microsoft Dynamics 365 Finance a zvládnout požadavky mimo systém.

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>Nastavení externího mapování na místní účtovou osnovu

1. Vytvořte jedinou globální účtovou osnovu, která bude obsahovat všechny požadované hlavní účty.
2. V každé právnické osobě přiřaďte globální účtovou osnovu na stránce **Hlavní kniha**.
3. Provedení mapování na místní účtovou osnovu mimo Finance.

#### <a name="advantages"></a>Výhody

- Tento přístup poskytuje jednotný způsob práce v celé organizaci.

#### <a name="disadvantages"></a>Nevýhody

- Žádné místní hlášení ze systému není k dispozici.
- Tento přístup je náchylný k chybám při vytváření finančních výkazů.

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>Místní účtová osnova přiřazená právnické osobě

Pokud se vaše organizace rozhodne nepoužívat globální účtovou osnovu napříč právnickými osobami, vytvoří se pro každou jedinečnou místní účtovou osnovu samostatná účtová osnova. Každá právnická osoba je pak propojena s odpovídající účtovou osnovou na stránce **Hlavní kniha**.

### <a name="do-global-consolidation"></a>Provedení globální konsolidace

V tomto přístupu se konsolidační společnost používá ke shrnutí a spojení zůstatků z každé zdrojové místní společnosti do kombinované globální účtové osnovy v konsolidované společnosti. Tento přístup vyžaduje, abyste udržovali mapování každé místní účtové osnovy na globální účtovou osnovu v konsolidační společnosti.

#### <a name="set-up-global-consolidation"></a>Nastavení globální konsolidace

1. Vytvořte samostatnou účtovou osnovu pro každou právnickou osobu, která má jinou místní účtovou osnovu. Pokud mají některé právnické osoby stejnou účtovou osnovu, je vyžadována pouze jedna místní účtová osnova, kterou lze sdílet.
2. V každé právnické osobě přiřaďte příslušnou účtovou osnovu na stránce **Hlavní kniha**.
3. Volitelné: Vytvořte účtovou osnovu pro globální účtovou osnovu každé konsolidační společnosti, která má jinou globální účtovou osnovu.
4. Vytvořte konsolidační právní subjekt pro každou požadovanou úroveň konsolidace a přiřaďte příslušnou účtovou osnovu na stránce **Hlavní kniha**.
5. Proveďte jeden z následujících kroků:

    - Pokud je vyžadována pouze jedna konsolidace, nakonfigurujte konsolidační účet na stránce **Hlavní účet**.
    - Pokud je vyžadována více než jedna konsolidace nebo pokud číslo účtu i název účtu vyžadují překlad, použijte stránky **Konsolidační skupiny** a **Dodatečné konsolidační účty** reprezentující požadavky na globální účtovou osnovu.

6. Spusťte proces konsolidace a převeďte zůstatky z místních právnických osob do konsolidované právnické osoby. Tato konsolidovaná právnická osoba používá konsolidační účty, které jste definovali v kroku 5.

#### <a name="advantages"></a>Výhody

- Formát místních účetních standardů je aplikován nativně.
- Tento přístup poskytuje místnímu finančnímu týmu jednodušší způsob práce.

#### <a name="disadvantages"></a>Nevýhody

- Není k dispozici žádný pohled na globální pozici v reálném čase.
- Proces konsolidace může probíhat častěji.

## <a name="additional-resources"></a>Další prostředky

- [Plánování účetní osnovy](plan-chart-of-accounts.md)
- [Konfigurace účetních knih](configure-ledger.md)
- [Finanční dimenze a zaúčtování](Default-dimensions.md#balancing-dimension)
- [Sady finančních dimenzí](financial-dimension-sets.md)
- [Přehled konsolidace a vyloučení](../budgeting/consolidation-elimination-overview.md)
- [Skupiny konsolidačních účtů a další konsolidační účty](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
