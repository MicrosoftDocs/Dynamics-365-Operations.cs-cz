---
title: Produkt je blokován pro transakce
description: Po potvrzení plánování objednávek se zobrazí chybová zpráva s oznámením, že položka je pro transakce blokována.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752603"
---
# <a name="product-is-on-hold-for-transactions"></a>Produkt je blokován pro transakce

Kód chyby: SYS13295

## <a name="symptoms"></a>Příznaky

Poté, co potvrdíte plánované objednávky, zobrazí se následující chybová zpráva:

> Položka %1 je blokována pro transakce v %2.

## <a name="cause"></a>Příčina

Při popisu blokovaných položek systém používá termíny *blokováno*, *zastaveno* a *blokováno* zaměnitelně. Tato chyba znamená, že položka je nastavena jako **Zastaveno** ve výchozím nastavení objednávky.

Pokud je položka blokována a přidáte ji do nákupní objednávky nebo řádku prodejní objednávky, zobrazí se varovná zpráva. Při blokování položky není možné upravit skladové transakce související se řádkem prodejní či nákupní objednávky (například při účtování dodacího listu nebo faktury). Nakoupenou položku můžete blokovat a zároveň ji prodat. V takovém případě je vybráno zaškrtávací políčko **Zastaveno** na nákupní objednávce, ale položka není blokována u zásob nebo v prodejní objednávce.

Tady jsou některé z podmínek, které mohou způsobit zablokování prodeje čísla položky:

- Položka je stále ve vývoji nebo výrobě. Proto nechcete, aby byl prodán nebo rezervován.
- Obdrželi jste mnoho vadných položek a vady je třeba opravit, než bude možné předmět prodat.

V takových případech je možné blokovat položku, až dokud není problém vyřešen.

Při blokování položky a vytvoření řádku vratky se zobrazí zpráva. Nelze blokovat řadu ani šarži položky. Pokud mají být blokovány části položky, lze to provést přesunutím zásob nebo zablokováním celé zásoby položky na určené období.

## <a name="resolution"></a>Řešení

- Otevřete stránku **Výchozí nastavení objednávky** pro položku a zrušte zaškrtnutí tlačítka **Zastaveno**.
