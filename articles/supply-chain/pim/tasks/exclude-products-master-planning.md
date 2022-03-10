---
title: Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování
description: Tento postup popisuje, jak vytvořit nový stav životního cyklu produktu s vyloučením produktů z hlavního plánování a výpočtu úrovně Kusovníku.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7f72be341b81515b7c5540d66f61647df93af41
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567024"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a>Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování

[!include [banner](../../includes/banner.md)]

Tento postup popisuje, jak vytvořit nový stav životního cyklu produktu s vyloučením produktů z hlavního plánování a výpočtu úrovně Kusovníku.


## <a name="create-an-obsolete-state"></a>Vytvoření zastaralého stavu
1. Přejděte na Řízení informací o produktech > Nastavení > Stav životnosti produktu.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Stav.
4. Vyberte možnost Ne v poli Je aktivní pro plánování.
5. Zadejte nějakou hodnotu do pole Popis.

## <a name="associate-the-obsolete-state-to-a-released-product"></a>Přidružení zastaralého stavu k uvolněnému produktu
1. Zavřete stránku.
2. Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.
3. Použijte rychlý filtr pro hledání záznamů. Můžete například filtrovat v poli Hledat jméno pomocí hodnoty M00.
4. Klikněte na položku Upravit.
5. Označte v seznamu vybraný řádek.
6. V poli Stav cyklu životnosti produktu zadejte nebo vyberte hodnotu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]