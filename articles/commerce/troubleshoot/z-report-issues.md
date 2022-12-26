---
title: Problémy s odsouhlasením dat sestavy Z
description: Tento článek popisuje problémy, se kterými se mohou uživatelé setkat při odsouhlasení dat sestavy Z v centrále Commerce Headquarters. Popisuje také možné základní příčiny a řešení, která mohou pomoci předejít budoucím výskytům.
author: Shajain
ms.date: 12/06/2022
ms.topic: Troubleshooting
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.openlocfilehash: 9803134c4c77233e565525e96fd82af293d4c829
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9832124"
---
# <a name="issues-with-the-data-reconciliation-of-a-z-report"></a>Problémy s odsouhlasením dat sestavy Z

[!include [banner](../../includes/banner.md)]

Tento článek obsahuje pokyny pro odstraňování problémů, které vám mohou pomoci, pokud narazíte na problémy s odsouhlasením dat sestavy Z v centrále Microsoft Dynamics 365 Commerce Headquarters. Popisuje problémy, se kterými se uživatelé mohou setkat při odsouhlasení dat, možné základní příčiny a řešení, která mohou pomoci předejít budoucím výskytům.

## <a name="description"></a>popis

- Mezi částkami, které jsou uvedeny v sestavě Z, a součty, které jsou uvedeny ve vypočítaném výkazu, je nesoulad.
- Transakce v centrále má nesprávný počet řádkových položek nebo existuje nesoulad mezi součtem řádků a součtem transakce.
- Počet transakcí, které jsou zobrazeny ve směně v centrále, je menší než počet transakcí v sestavě Z.
- Odeslání výpisu se nezdařilo z jednoho z předchozích důvodů.

### <a name="root-cause"></a>Hlavní příčina

Nejčastější hlavní příčinou dříve popsaných příznaků je generování duplicitních ID transakcí v databázi kanálů. Duplicitní ID transakcí lze generovat z následujících důvodů:

- Místní databázové úložiště moderního pokladního místa (MPOS) je poškozeno.
- MPOS má některé transakce v režimu offline a je znovu aktivováno pomocí účtu, který nemá přístup k offline databázi.
- Vyskytl se problém s vlastními nastavením, které souvisí s generováním ID transakcí.

## <a name="resolution"></a>Řešení

Commerce obvykle používá číselnou řadu při generování sekvenčních ID transakcí. Pokud systém nemůže z nějakého důvodu určit, že byla použita číselná řada, vygeneruje se duplicitní ID transakce. 

Chcete-li vyřešit problém s duplicitním ID transakce, vytvořte lístek podpory a zkontrolujte, zda lze opravit data transakce. V některých případech, například když nedochází ke ztrátě dat v centrále, není žádná oprava dat možná ani nutná.

Chcete-li tomuto problému v budoucnu předejít, musíte v centrále povolit funkci **Povolit nové ID transakce pro zabránění duplicitním ID transakcí**. Tato funkce byla představena v Commerce verzi 10.0.19. Pomáhá předcházet vytváření sekvenčních ID transakcí tím, že zajišťuje, aby bylo pro každou transakci vytvořeno jedinečné ID. Další informace o této funkci viz [Prevence před vytvářením duplicitních ID transakcí](../channel-setup-retail.md#ensure-unique-transaction-ids).
