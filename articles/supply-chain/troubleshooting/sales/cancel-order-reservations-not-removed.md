---
title: Při zrušení objednávky nelze rezervace zrušit
description: Nemůžete zrušit prodejní objednávku, dokud nebude zrušena a stornována práce s ní spojená. Chcete-li to provést, proveďte tyto tři kroky.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475807"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Při zrušení objednávky nelze rezervace zrušit

## <a name="symptoms"></a>Příznaky

Pokud je s prodejní objednávkou spojena práce a pokusíte se ji zrušit, zobrazí se následující chybová zpráva:

> Rezervace nelze odebrat, protože je vytvořena práce, která je na rezervacích závislá.

Nemůžete zrušit prodejní objednávku, dokud nebude zrušena a stornována práce. Tento požadavek platí, i když je práce přidružená k prodejní objednávce uzavřena.

## <a name="resolution"></a>Řešení

Chcete-li opravit problém, postupujte následovně:

1. Zrušte práci a vložte zásoby zpět na požadované místo. Přejděte na příslušné vytížení prodejní objednávky a vyberte buď **Snížit vyskladněné množství** na řádku vytížení nebo **Stornovat práci** v podokně akcí.

    Práce má nyní stav *Zrušeno* a automaticky se vytvoří a zpracuje nová práce přesunu zásob, aby se zásoby vrátily zpět na místo, které bylo popsáno v době zrušení.

2. Odstraňte vytížení. Dodávka je také odstraněna.

3. Nyní byste měli být schopni přejít k prodejní objednávce a zrušit ji.
