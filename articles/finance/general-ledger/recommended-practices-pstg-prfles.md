---
title: Doporučené postupy pro profily účtování
description: Toto téma popisuje doporučené postupy pro konfiguraci profilů účtování.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemSetup, CustPosting, VendPosting, InventPosting, AssetPosting, ProjPosting, AssetLeasePostingAccounts, ProjCategory, ITMCostTypeTable, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, MainAccount, SysDatabaseLogSetup, CustGroup, VendGroup, InventItemGroup
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 211dc42b80089eb1f59a435f09d6e9d9f956736b
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734268"
---
# <a name="recommended-practices-for-posting-profiles"></a>Doporučené postupy pro profily účtování

Existuje několik doporučených postupů, které byste měli dodržovat při konfiguraci účtování odesílání v celém systému. Toto téma popisuje různé scénáře a odpovídající doporučené postupy.

## <a name="setting-the-do-not-allow-manual-entry-flag"></a>Nastavení příznaku Nepovolit ruční zadání

Na stránce **Hlavní účty** je třeba vybrat zaškrtávací políčko **Nedovolte ruční zadávání** pro jakýkoli hlavní účet, který se používá pro profil účtování. Toto nastavení zabrání uživatelům v ručním zaúčtování položky deníku na hlavní účet. Pomáhá tedy zajistit, aby vedlejší kniha zůstala v rovnováze s hlavní knihou, a pomáhá usnadnit proces odsouhlasení.

Pokud jsou vyžadovány úpravy účtu, který je řízen systémem a automaticky zaúčtován, můžete použít jeden z těchto přístupů:

- Vytvořte sekundární hlavní účet, kam lze zaúčtovat úpravy. Poté použijte účet Celkem nebo zvláštní řádek ve finančních přehledech k seskupení a sečtení účtů dohromady.
- Vraťte původní transakce v příslušné dílčí knize, proveďte požadované opravy a poté transakci znovu zaúčtujte prostřednictvím stejné dílčí knihy.

## <a name="changing-posting-profiles-after-transactions-exist"></a>Změna profilů účtování poté, co transakce existují

Pokud změníte profil účtování poté, co transakce existují, odsouhlasení může selhat a vaše vedlejší kniha a hlavní kniha se mohou dostat do nerovnováhy. Obecně vám doporučujeme **neměnit** profil účtování poté, co transakce existují.

Pokud jsou nutné změny, použijte následující pokyny, které vám pomohou zajistit integritu systému:

- Proveďte změny během uzávěrky období.
- Proveďte změny, když v systému neprobíhají žádné jiné transakce.
- Před a po provedení změn ověřte účetní knihu a srovnejte ji s dílčí knihou.
- Pokud změníte profil účtování, zaúčtované transakce se neaktualizují. Pečlivě zvažte, zda jsou pro vaši změnu nutné nějaké úpravy.
- Pokud měníte profily účtování zásob, zvažte, jak tyto změny ovlivní vaše zásoby a zůstatky v hlavní knize. Některé změny mohou vyžadovat, abyste zásoby dostali na 0 (nulu), uzavřeli zásoby a poté je po provedení změn vrátili zpět.
- Vždy otestujte své změny v neprodukčním prostředí, než je provedete v produkci.

## <a name="using-database-logging-to-audit-changes-to-posting-profiles"></a>Použití protokolování databáze k auditu změn profilů odesílání

Zvažte nastavení protokolování databáze pro každý profil odesílání a tabulky parametrů, které řídí odesílání. Pokud se pak změní parametr nebo profil, budete mít úplný záznam auditu o tom, jaká hodnota byla změněna, kdo ji změnil, kdy byla změněna a jaká byla předchozí hodnota. Tyto informace mohou být kritické během vašeho procesu odsouhlasení a váš auditor může vyžadovat podpůrnou dokumentaci.

Další informace získáte v tématu [Konfigurace protokolování databáze](../../fin-ops-core/dev-itpro/sysadmin/configure-manage-database-log.md).

Následující tabulku použijte jako referenci pro běžné názvy tabulek, které souvisejí s profily účtování a souvisejícími parametry účtování.

| Název webové stránky | Navigační cesta | Název tabulky |
|-----------|-----------------|------------|
| Parametry závazků | Závazky &gt; Nastavení &gt; Parametry závazků | VendParm |
| Účetní profil dodavatele | Závazky &gt; Nastavení &gt; Účetní profil dodavatele | VendPosting |
| Kód nákladů | Závazky &gt; Nastavení poplatků &gt; Kód poplatků nebo Pohledávky &gt; Nastavení poplatků &gt; Kód poplatků | MarkupTable |
| Metody platby | Závazky &gt; Nastavení platby &gt; Metody platby | VendPaymMode |
| Platební slevy | Závazky &gt; Nastavení plateb &gt; Hotovostní slevy nebo Pohledávky &gt; Nastavení plateb &gt; Hotovostní slevy | CashDisc |
| Platební poplatek (dodavatel) | Závazky &gt; Nastavení platby &gt; Platební poplatek | VendPaymFee |
| Parametry pohledávek | Pohledávky &gt; Nastavení &gt; Parametry pohledávek | CustParm |
| Účetní profily odběratele | Pohledávky &gt; Nastavení &gt; Účetní profil odběratele | CustPosting |
| Metody platby | Pohledávky &gt; Nastavení platby &gt; Metody platby | CustPaymMode |
| Platební poplatek (odběratel) | Pohledávky &gt; Nastavení platby &gt; Metody plateb | CustPaymFee |
| Parametry leasingu majetku | Leasing majetku &gt; Nastavení &gt; Parametry leasingu majetku | AssetLeasePostingAccounts<br>AssetLeaseJournalParameters<br>AssetLeaseExecutoryCostPostingAccounts |
| Bankovní účty | Pokladna a banka &gt; Bankovní účty &gt; Bankovní účty | BankAccountsTable |
| Typy bankovních transakcí | Pokladna a banka &gt; Nastavení &gt; Typy bankovní transakce | BankTransType |
| Pravidla eliminace | Konsolidace &gt; Nastavení &gt; Pravidlo eliminace | LedgerEliminationRule<br>LedgerEliminationRuleLines |
| Kategorie výdajů | Správa výdajů &gt; Nastavení &gt; Obecné &gt; Kategorie výdajů | ProjCategories |
| Parametry dlouhodobého majetku | Dlouhodobý majetek &gt; Nastavení &gt; Parametry dlouhodobého majetku | AssetParameters |
| Účetní profily dlouhodobého majetku | Dlouhodobý majetek &gt; Nastavení &gt; Účetní profily dlouhodobého majetku | AssetLedgerAccounts<br>AssetDisposalParameters |
| Účty přecenění měny | Hlavní kniha &gt; Měny &gt; Účty přecenění měny | CurrencyLedgerGainLossAccount |
| Účty pro automatické transakce | Hlavní kniha &gt; Nastavení účtování &gt; Účty pro automatické transakce | LedgerSystemAccounts |
| Mezipodnikové účetnictví | Hlavní kniha &gt; Nastavení účtování &gt; Mezipodnikové účty | LedgerIntercompany |
| Definice účtování transakce | Hlavní kniha &gt; Nastavení účtování &gt; Definice účtování transakcí | JournalizingDefinitionTrans |
| Definice účtování | Hlavní kniha &gt; Nastavení účtování &gt; Definice účtování | JournalizingDefintion |
| Účtování (skladové zásoby) | Řízení zásob &gt; Nastavit &gt; Zaúčtování &gt; Zaúčtování | InventPosting |
| Kódy typu nákladů | Náklady za doručení &gt; Nastavení kalkulace &gt; Kódy typu nákladů | ITMCostTypeTable |
| Prostředky | Řízení výroby &gt; Nastavení &gt; Prostředky &gt; Prostředky | WrkCtrTable |
| Skupiny prostředků | Řízení výroby &gt; Nastavení &gt; Prostředky &gt; Skupiny prostředků | WrkCtrResourceGroup |
| Skupina účtování výroby | Řízení výroby &gt; Nastavení &gt; Výroba &gt; Skupina výroby | ProdGroup |
| Nákladové kategorie | Kontrola produkce &gt; Nastavení &gt; Trasy &gt; Nákladové kategorie | ProjCategory |
| Skupiny projektů | Projektové řízení a účetnictví &gt; Nastavení &gt; Účtování &gt; Projektové skupiny | ProjGroup |
| Nastavení účtování hlavní knihy (projekty) | Řízení a účetnictví projektu &gt; Nastavení &gt; Zaúčtování &gt; Nastavení účtování hlavní knihy | ProjPosting |
| Výchozí protiúčty pro výdaje | Projektové řízení a účetnictví &gt; Nastavení &gt; Účtování &gt; Výchozí protiúčty pro výdaje | ProjDefaultOffsetSetup |
| Profily zaúčtování správy rabatu | Správa rabatů &gt; Nastavení zaúčtování správy rabatu &gt; Profily pro správu rabatů | TAMRebatePosting |
| Skupina zaúčtování hlavní knihy (daň) | Daň &gt; Nastavení &gt; DPH &gt; Účetní skupina | TaxAccountGroup |

## <a name="changing-groups-after-transactions-exist"></a>Změna skupin poté, co transakce existují

Při změně skupin v hlavních datech buďte opatrní. Pokud k definování profilů odesílání používáte skupiny, jakákoli změna skupiny v hlavním záznamu může mít negativní dopad na schopnost uvést hlavní knihu do souladu s vedlejší knihou. Můžete například nakonfigurovat profil účtování zásob pro výnosy prodejní objednávky tak, aby byl pro každou skupinu položek použit jiný účet výnosů. Pokud změníte skupinu položek, která je přiřazena k položce poté, co transakce existují, budou výnosy z nových transakcí zaúčtovány na aktualizovaný účet. Veškeré výnosy, které byly zaúčtovány před změnou, však zůstanou na původním účtu.

## <a name="testing-posting-profiles"></a>Testování účetních profilů

Před spuštěním a poté, co provedete jakékoli změny nebo doplnění vašich profilů účtování nebo souvisejících parametrů, byste měli otestovat každý scénář. Minimálně byste měli otestovat každý typ účtování, abyste ověřili, že účtování funguje správně. Doporučený přístup je však otestovat každou transakci a kombinaci profilu zaúčtování.

Máte například dva profily účtování odběratelů, z nichž každý má tři záznamy, které jsou specifické pro skupiny zákazníků. V tomto případě byste měli otestovat každý typ transakce.

**Účetní profily:**

- **GEN** – Obecný profil účtování, který má jednu skupinu pro zaměstnance, jednu pro zákazníky a jednu pro mezipodnikové. Každá skupina ukazuje na jiný obchodní účet pohledávek.
- **PRE** – Profil zaúčtování zálohy, který má jeden záznam pro všechny zálohy, které odkazují na předplacené účty zákazníka.

### <a name="testing-scenarios"></a>Testovací scénáře

- Volný text faktury pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **GEN**
- Volný text faktury pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **PRE**
- Volný text prodejní objednávky pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **GEN**
- Volný text prodejní objednávky pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **PRE**
- Platební deník zákazníka pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **GEN**
- Platební deník zákazníka pro zákazníka ve skupině **Zaměstnanec**, která používá profil účtování **PRE**

V předchozím příkladu zopakujte jeden testovací scénář pro každou skupinu zákazníků a opakujte každou skupinu testovacích scénářů pro každý další typ transakce (například faktury projektu a správa služeb).

## <a name="reconciling-the-ledger-to-the-subledger"></a>Odsouhlasení hlavní knihy a dílčí knihy

Hlavní kniha by měla být v každém období odsouhlasena s vedlejší knihou. Mnoho modulů obsahuje předpřipravené zprávy, které lze použít k tomuto sladění. V závislosti na vašich místních požadavcích však možná budete muset vyvinout vlastní sestavy nebo rozšířit stávající sestavy, aby splňovaly vaše požadavky na sestavování.

Doporučujeme, abyste před uvedením do provozu provedli simulované období uzavření a odsouhlasili každou z vašich dílčích knih s hlavní knihou. Také doporučujeme, abyste před prvním uvedením do provozu provedli falešné vyřazení všech otevřených zůstatků a otevřených transakcí. V rámci tohoto procesu byste měli provést úplné odsouhlasení, abyste zajistili, že migrace zůstatků a otevřených transakcí bude v rovnováze se staršími systémy a že všechny dílčí knihy budou v rovnováze s hlavní knihou před vytvořením nových transakcí.
