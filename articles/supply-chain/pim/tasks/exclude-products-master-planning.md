---
title: Vytvoření stavu životního cyklu produktu k vyloučení produktů z hlavního plánování
description: Tento postup popisuje, jak vytvořit nový stav životního cyklu produktu s vyloučením produktů z hlavního plánování a výpočtu úrovně Kusovníku.
author: cvocph
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cadf1d812e737309dbe8ca26d04ffb1ee88ef16a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818030"
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