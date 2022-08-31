---
title: Zaúčtování pohledávek
description: Tento článek vysvětluje, jak se konfigurují účtování v Pohledávek a uvádí příklady konfigurací účtování.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustPaymMode, CustCashDiscount, CommissionPosting, MarkupTable\_Cust, CustPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d679595a1f702c4e3ade138a87c817d245fcf79
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324322"
---
# <a name="accounts-receivable-posting"></a>Účtování pohledávek

[!include [banner](../includes/banner.md)]

Primární profil účtování pro modul **Pohledávky** je profil odesílání zákazníka. Tento profil účtování určuje souhrnný účet, který se použije při zaúčtování zůstatků zákazníka do hlavní knihy. Souhrnný účet je hlavní účet. Označuje se také jako obchodní účet pohledávek.

Sestavu **Zákazník pro odsouhlasení hlavní knihy** lze po zaúčtování použít k odsouhlasení zůstatků zákaznických účtů a účtů hlavní knihy. Sestava používá informace, které se nacházejí v souhrnném účtu pro profil účtování zákazníka. Nepoužije souhrnný účet z účetnictví, které je pro doklad vytvořeno. Pokud po zaúčtování transakcí provedete změny v profilu účtování zákazníka nebo skupině zákazníků přiřazené k zákazníkovi, může sestava zobrazovat rozdíly mezi zůstatkem účtu zákazníka a hlavní knihy. Chcete-li zobrazit pouze řádky, které mají rozdíly, a všechny řádky, pro které jsou účty zákazníků i účet hlavní knihy nulové, vyberte parametr **Pouze rozdíly** při tisku sestavy.

Další informace naleznete v tématu [Účetní profily zákazníka](../accounts-receivable/customer-posting-profiles.md).

V části Pohledávky je k dispozici několik konfigurací zaúčtování kromě profilu zaúčtování zákazníka. Další části poskytují více informací o těchto ostatních konfiguracích účtování.

## <a name="posting-accounts-for-methods-of-payment"></a>Účty účtování pro způsoby platby

Způsoby platby definují, jak bude platba zaúčtována do hlavní knihy. Řídí také chování výstupu platby. Obvykle je vytvořen jeden způsob platby pro každý typ platby, kterou vaše organizace přijímá (například hotovost, šek, kreditní karta, peněžní poukázka a bankovní převod).

Pole v části **Účtování** na pevné záložce **Všeobecné** řídí, jak bude platba zaúčtována do hlavní knihy. Nejprve musíte vybrat hodnotu v poli **Typ účtu**. Typ účtu, který vyberete, řídí chování účtu pole **Platební účet**. Doporučujeme vám vybrat **Banka** v poli **Typ účtu** a poté v poli vyberte bankovní účet v poli **Platební účet**. Výhodou tohoto přístupu je, že systém zaúčtuje platbu do vedlejší knihy banky, která podporuje odsouhlasení a další procesy související s hotovostí. Následující tabulka ukazuje příklad konfigurace profilu odesílání, pokud používáte modul **Správa hotovosti a banky**.

| Typ zaúčtování | Typ účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Bank of Contoso | Bankovní účet, který je spojen s aktivem | Kredit | Číslo | Pro každý způsob platby zadejte hlavní účet do pole **Platební účet**. |

Pokud neplánujete používat správu hotovosti a bank, měli byste si vybrat **Hlavní kniha** v poli **Typ účtu** a poté vybrat hlavní účet v poli **Platební účet**. Následující tabulka ukazuje příklad konfigurace profilu odesílání, pokud nepoužíváte modul Správa hotovosti a banky.

| Typ zaúčtování | Typ účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|--------------|---------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of Contoso | Materiál | Kredit | Číslo | Pro každý způsob platby zadejte hlavní účet do pole **Platební účet**. |

## <a name="bridging-accounts"></a>Překlenovací účty

Překlenovací zaúčtování je dvoufázový proces, který se používá při zaúčtování plateb. Je to volitelná funkce, kterou lze použít například u bankovních účtů s nulovým zůstatkem. Může pomoci zajistit hladší a včasnější proces odsouhlasení bank. V prvním kroku je platba zaúčtována na dočasný účet (překlenovací účet). Ve druhém kroku je zaúčtovaný záznam stornován a zaúčtován na bankovní účet, když je platba zúčtována bankou. Následující tabulka ukazuje příklad konfigurace profilu účtování pro překlenovací účtování.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Deník hlavní knihy | 130725 | Nevyúčtovaná hotovost | Pasiva | Debet | Ano | Pro každý způsob platby zadejte hlavní účet do pole **Překlenovací účet**. |

Více informací viz [Nastavení a zpracování překlenovacích plateb](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="posting-accounts-for-customer-cash-discounts"></a>Účty účtování pro platební slevy zákazníků

Pokud vaše organizace nabízí platební slevy zákazníkům výměnou za rychlou platbu, musíte nakonfigurovat kódy platebních slev a určit, jak mají být slevy zaúčtovány do hlavní knihy. Pro zadání hlavního účtu, který se používá k zaúčtování slevy v hotovosti zákazníka, je k dispozici několik možností.

Více informací získáte v části [Hotovostní slevy](../cash-bank-management/cash-discounts.md).

## <a name="posting-accounts-for-payment-fees"></a>Účty účtování pro platební poplatky

Platební poplatky vám umožňují automaticky přidat poplatek k platbě zákazníka, pokud platí sada podmínek. Poplatky za platbu lze naúčtovat zákazníkovi nebo je lze zaúčtovat na váš bankovní účet jako výdaj. Několik příkladů:

- Pokud zákazník platí kreditní kartou, naúčtujete mu 3 % z celkové platby.
- Vaše banka vám účtuje 1,00 USD za každý bankovní převod, který zpracujete, a poplatek za bankovní převod je účtován do nákladů.

Když nakonfigurujete poplatek za platbu zákazníka, pokud nastavíte pole **Poplatek** na **Zákazník**, pole **Hlavní účet** nebude dostupné a systém použije k zaúčtování poplatku profil zákazníka. Pokud nastavíte pole **Poplatek** na **Hlavní kniha**, musíte nastavit pole **Hlavní účet** na hlavní účet, kde bude zaúčtován poplatek za platbu. Obvykle bude tento hlavní účet nákladový účet. Následující tabulka ukazuje příklad konfigurace profilu účtování pro účtování platebního poplatku.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Deník hlavní knihy | 618190 | Výdaj bankovního poplatku | Výdaje | Debet | Ne |  Je-li v poli **Náklady** vybrána **Hlavní kniha**, vyberte tento účet v poli **Hlavní účet** u platebního poplatku. |

Další informace naleznete v tématu [Stanovení platebních poplatků odběratelů](../accounts-receivable/tasks/establish-customer-payment-fees.md).

## <a name="posting-accounts-for-charges-codes"></a>Účty účtování pro kódy poplatků

Pokud musíte kromě řádkových položek sledovat i částky prodeje, můžete použít kódy poplatků. Svým zákazníkům můžete například účtovat poplatky za přepravu a manipulaci nebo může interně vynaložit nějaké poplatky za přepravu a manipulaci. Můžete určit, zda se tyto částky zaúčtují na nákladové účty nebo zda se přidají k pořizovací ceně položek.

Můžete vytvořit kódy poplatků pro pohledávky a závazky. Když konfigurujete kód poplatků, musíte definovat účtování. Zaúčtování řídí debetní i kreditní účet. Pro každý kód poplatku, který vytváříte můžete vybrat typ účtování, který se použije. Následující tabulka ukazuje typické příklady kódů poplatků pro Pohledávky.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Platební poplatek | 411400 | Výnosy – poplatky | Výnosy | Kredit | Číslo | **Příklad pro nedostatek finančních prostředků:** Debetní účet zákazníka/dodavatele a kreditní knihy |
| Objednávka, dopravné | 403500 | Výnosy – doprava | Výnosy | Kredit | Číslo | **Příklad pro přepravu, která je účtována zákazníkovi:** Debetní účet zákazníka/dodavatele a kreditní knihy |
| Rabat\* | 403200 | Sleva | Výnosy | Debet | Číslo | **Příklad pro rabat zákazníka:** Debetní účet hlavní knihy zákazník/dodavatel kreditu |

\* V příkladu rabatu se zaúčtování použije pouze tehdy, když je do záhlaví nebo řádku nákupní objednávky přidán kód poplatku. Pokročilá funkce rabatu, která je dostupná v Microsoft Dynamics 365 Supply Chain Management, poskytuje větší kontrolu a automatizaci rabatů. Další informace naleznete v tématu [Rabaty zákazníkům](../../supply-chain/sales-marketing/tasks/process-customer-rebates.md).

Předchozí tabulka ukazuje tři typické příklady typů účtování, které lze použít pro kódy poplatků. Měla by se používat jako vodítko a vzorek. Neposkytuje úplný seznam všech možných kombinací nebo typů účtování, které lze použít.

Další informace naleznete v tématu [Vytvoření kódů poplatků](../accounts-receivable/create-charges-codes.md).

## <a name="posting-accounts-for-commissions"></a>Účty účtování provizí

Volitelně můžete nakonfigurovat systém pro výpočet provizí pro obchodního zástupce nebo skupinu obchodních zástupců na dané prodejní objednávce. Pokud tuto funkci povolíte, musíte nakonfigurovat účet účtování, který se používá k výpočtu provize. Tato konfigurace se provádí na stránce **Účtování provize** modulu **Prodej a marketing**.

Další informace naleznete v tématu [Nastavení pravidel provizí prodeje](../../supply-chain/sales-marketing/tasks/set-up-sales-commission-rules.md).
