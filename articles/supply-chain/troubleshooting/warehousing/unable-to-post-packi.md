---
title: Nelze zaúčtovat dodací list pro pozastavený řádek prodejní objednávky
description: Nemůžete zaúčtovat dodací list pro pozastavený řádek prodejní objednávky
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462846"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Nelze zaúčtovat dodací list pro pozastavený řádek prodejní objednávky

Kód chyby: SYS13203

## <a name="symptoms"></a>Příznaky

Když se pokusíte zaúčtovat dodací list pro vytížení, systém zobrazí následující chybovou zprávu:

> Nelze zaúčtovat dodací list při zastavení řádku prodejní objednávky poté, co je potvrzena nemožnost vybrat množství A odchozí zásilky.

## <a name="cause"></a>Příčina

Nejméně jeden související řádek prodejní objednávky může být pozastaven, což znamená, že systém zabrání dalšímu zpracování této prodejní objednávky. Mimo jiné to znamená, že systém k objednávce nezaúčtuje dodací list.

Uživatel se například mohl rozhodnout pozastavit jeden nebo více řádků objednávky, protože zákazník zavolal zpět a svou objednávku zrušil. Pokud by však odchozí zásilka již byla potvrzena, pak by zásilka obsahující prodejní objednávku již fyzicky opustila sklad, což znamená, že zastavení řádků prodejní objednávky nebude mít žádný účinek. Vzhledem k tomu, že již není možné zásilku fyzicky zastavit, můžete také zrušit pozastavení řádků, abyste mohli zaúčtovat dodací list. Zrušenou objednávku pak budete muset zpracovat jako vrácení.

## <a name="resolution"></a>Řešení

Abyste mohli zaúčtovat dodací list, ujistěte se pomocí následujícího postupu, že žádný z příslušných řádků prodejní objednávky není pozastaven.

1. Přejděte na **Všechny prodejní objednávky \> Prodej a marketing \> Všechny prodejní objednávky**.
1. Najděte a otevřete prodejní objednávku, se kterou máte potíže.
1. Na pevné záložce **Řádky prodejní objednávky** vyberte řádek prodejní objednávky.
1. Na pevné záložce **Detaily řádku** otevřete kartu **Všeobecné** a ujistěte se, že pole **Zastaveno** je nastaveno na *Ne*.
1. Pokračujte, dokud nebudou zastaveny všechny příslušné prodejní řádky.
1. Zkuste znovu zaúčtovat dodací list pro vytížení nebo prodejní objednávku.
