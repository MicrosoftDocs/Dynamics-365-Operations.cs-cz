---
title: Účtování závazků
description: Tento článek vysvětluje, jak se konfigurují účtování v Závazcích a uvádí příklady konfigurací účtování.
author: rachel-profitt
ms.date: 01/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting, VendPaymMode, VendCashDiscount, MarkupTable\_Vend, VendPaymFee
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b3593e01ed4d0a88b5816803f1d67fa7ed5e0f6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908002"
---
# <a name="accounts-payable-posting"></a>Účtování závazků

[!include [banner](../includes/banner.md)]

Primární profil účtování pro modul **Závazky** je profil odesílání dodavatele. Tento profil účtování určuje souhrnný účet, který se použije při zaúčtování zůstatků dodavatele do hlavní knihy. Souhrnný účet je hlavní účet. Označuje se také jako obchodní účet závazků.

Další informace naleznete v tématu [Účetní profily dodavatele](../accounts-payable/vendor-posting-profiles.md).

V části Závazky je k dispozici několik konfigurací zaúčtování kromě profilu zaúčtování dodavatele. Další části poskytují více informací o těchto ostatních konfiguracích účtování.

## <a name="methods-of-payment-posting-accounts"></a>Účty účtování způsobů platby

Způsoby platby definují, jak bude platba zaúčtována do hlavní knihy. Řídí také chování výstupu platby. Obvykle je vytvořen jeden způsob platby pro každý typ platby, kterou vaše organizace provádí (například hotovost, šek, kreditní karta, peněžní poukázka a bankovní převod).

Pole v části **Účtování** na pevné záložce **Všeobecné** na stránce **Způsoby platby** (**Závazky > Nastavení plateb > Způsoby platby**) řídí, jak bude platba zaúčtována do hlavní knihy. Nejprve musíte vybrat hodnotu v poli **Typ účtu**. Typ účtu, který vyberete, řídí chování účtu pole **Platební účet**. Doporučujeme vám vybrat **Banka** v poli **Typ účtu** a poté v poli vyberte bankovní účet v poli **Platební účet**. Výhodou tohoto přístupu je, že systém zaúčtuje platbu do vedlejší knihy banky, která podporuje odsouhlasení a další procesy související s hotovostí. Následující tabulka ukazuje příklad konfigurace profilu odesílání, pokud používáte modul **Správa hotovosti a banky**.

| Typ zaúčtování | Typ účtu | Příklad názvu platebního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|--------------|------------------------------|--------------|---------------|------------------|-------------|
| Banka | Banka | Bank of America | Bankovní účet, který je spojen s aktivem | Debet | Ne | Pro každý způsob platby zadejte hlavní účet do pole **Platební účet**. |

Pokud neplánujete používat správu hotovosti a bank, měli byste si vybrat **Hlavní kniha** v poli **Typ účtu** a poté vybrat hlavní účet v poli **Platební účet**. Následující tabulka ukazuje příklad konfigurace profilu odesílání, pokud **nepoužíváte** modul Správa hotovosti a banky.

| Typ zaúčtování | Typ účtu |Příklad platebního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|--------------|------------------------|--------------|---------------|------------------|-------------|
| Ledger | Ledger | 100100: Bank of America | Materiál | Debet | Ne | Pro každý způsob platby zadejte hlavní účet do pole **Platební účet**. |

## <a name="bridging-accounts"></a>Překlenovací účty

Překlenovací zaúčtování je dvoufázový proces, který se používá při zaúčtování plateb. Je to volitelná funkce, kterou lze použít například u bankovních účtů s nulovým zůstatkem. Může pomoci zajistit hladší a včasnější proces odsouhlasení bank. V prvním kroku je platba zaúčtována na dočasný účet (překlenovací účet). Ve druhém kroku je zaúčtovaný záznam stornován a zaúčtován na bankovní účet, když je platba zúčtována bankou. Následující tabulka ukazuje příklad konfigurace profilu účtování pro překlenovací účtování.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Deník hlavní knihy | 130725 | Nevyúčtovaná hotovost | Pasiva | Debet | Ano | Pro každý způsob platby zadejte hlavní účet do pole **Překlenovací účet**. |

Více informací viz [Nastavení a zpracování překlenovacích plateb](../accounts-receivable/set-up-and-process-bridged-payments.md).

## <a name="customer-cash-discounts-posting-accounts"></a>Účty účtování zákaznických hotovostních slev

Pokud vaše organizace obdrží hotovostní slevy od dodavatelů výměnou za rychlou platbu, musíte nakonfigurovat kódy hotovostních slev a určit, jak mají být slevy zaúčtovány do hlavní knihy. Pro zadání hlavního účtu, který se používá k zaúčtování slevy v hotovosti zákazníka, je k dispozici několik možností.

Více informací získáte v části [Hotovostní slevy](../cash-bank-management/cash-discounts.md).

## <a name="payment-fee-posting-accounts"></a>Účty účtování platebního poplatku

Platební poplatky vám umožňují automaticky přidat poplatek k platbě dodavatele, pokud platí sada podmínek. Poplatky za platbu lze uhradit prodejci nebo je lze zaúčtovat na váš bankovní účet jako výdaj. Několik příkladů:

- Pokud platíte kreditní kartou, prodejce vám naúčtuje 3 % z celkové platby.
- Vaše banka vám účtuje 1,00 $ za každý bankovní převod, který zpracujete, a poplatek za bankovní převod je účtován do nákladů.

Když nakonfigurujete poplatek za platbu dodavatele, pokud nastavíte pole **Poplatek** do **Dodavatel**, pole **Hlavní účet** nebude dostupné a systém použije k zaúčtování poplatku profil dodavatele. Pokud nastavíte pole **Poplatek** na **Hlavní kniha**, musíte nastavit pole **Hlavní účet** na hlavní účet, kde bude zaúčtován poplatek za platbu. Obvykle bude tento hlavní účet nákladový účet. Následující tabulka ukazuje příklad konfigurace profilu účtování pro účtování platebního poplatku.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|----------------|------------------|-------------|
| Deník hlavní knihy | 618190 | Výdaj bankovního poplatku | Výdaje | Debet | Ne | Je-li v poli **Náklady** vybrána **Hlavní kniha**, vyberte tento účet v poli **Hlavní účet** na stránce **Platební poplatek**. |

Další informace naleznete v tématu [Definování platebních poplatků dodavatele](../accounts-payable/tasks/define-vendor-payment-fees.md).

## <a name="charges-code-posting-accounts"></a>Účty účtování kódů poplatků

Pokud musíte kromě řádkových položek sledovat i částky nákupu, můžete použít kódy poplatků. Váš dodavatel vám může například účtovat poplatky za přepravu a manipulaci nebo může interně vynaložit nějaké poplatky za přepravu a manipulaci. Můžete určit, zda se tyto částky zaúčtují na nákladové účty nebo zda se přidají k pořizovací ceně položek.

Můžete vytvořit kódy poplatků pro pohledávky a závazky. Když konfigurujete kód poplatků, musíte definovat účtování. Zaúčtování řídí debetní i kreditní účet. Když vytváříte kódy poplatků, můžete vybrat typ účtování, který se použije pro každý kód poplatku. Následující tabulka ukazuje příklady typických kódů poplatků pro Závazky na stránce **Kódy poplatků**.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Nákupní poplatek | Ponechte pole prázdné. | Nelze použít | Položka | Debet | Ne | **Příklad nákupního poplatku za položku:** </p><ul><li>Pole **Typ debetu** = **Zboží**</li><li>  Pole **Typ kreditu** = **Zákazník/dodavatel**.</li><li> Účtování zboží používá hlavní účet z profilu účtování zásob. |
| Objednávka, dopravné | 600120 | Dopravné | Výnosy | Debet | Ne | **Příklad pro přepravu, která se platí dodavateli:** </p><ul><li>Pole **Typ debetu** = **Účet hlavní knihy**</li><li> Pole **Typ kreditu** = **Zákazník/dodavatel** |
| Rabat\* | 503160 | Rabat dodavatele (proti COGS)| Výdaje | Kredit | Ne | **Příklad slevy dodavatele:**</p><ul><li>Pole **Typ debetu** = **Zákazník/dodavatel**</li><li>Pole **Typ kreditu** = **Účet hlavní knihy** |

\* V příkladu rabatu se zaúčtování použije pouze tehdy, když je do záhlaví nebo řádku nákupní objednávky přidán kód poplatku. Pokročilá funkce rabatu, která je dostupná v Microsoft Dynamics 365 Supply Chain Management, poskytuje větší kontrolu a automatizaci rabatů. Další informace naleznete v tématu [Rabaty dodavatele](../../supply-chain//procurement/vendor-rebates.md).

Předchozí tabulka ukazuje tři typické příklady typů účtování, které lze použít pro kódy poplatků. Měla by se používat jako vodítko a výběr vzorků. Neposkytuje úplný seznam všech možných kombinací nebo typů účtování, které lze použít.

Další informace naleznete v tématu [Vytvoření kódů poplatků](../accounts-receivable/create-charges-codes.md).
