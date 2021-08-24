---
title: Hybridní objednávky odběratele
description: Hybridní objednávka odběratele je jedna objednávka, která obsahuje produkty, které si může zákazník odnést z obchodu, jakož i výrobky, které budou dodány nebo vyzvednuty později.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 261164
ms.assetid: 9d99a5b9-4662-499a-bece-3ea1d6092934
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4cb448670af9a6ddce8008be008cf3b0ff76bbce65053bf4618ea6668c4568d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739522"
---
# <a name="hybrid-customer-orders"></a>Hybridní objednávky odběratele

[!include [banner](includes/banner.md)]

Hybridní objednávka odběratele je jedna objednávka, která obsahuje produkty, které si může zákazník odnést z obchodu, jakož i výrobky, které budou dodány nebo vyzvednuty později.

V aplikaci Commerce můžete u objednávky odběratele vybrat realizaci všech produktů nebo vybraných produktů. Řádky produktu označené jako řádky k provedení, jsou automaticky fakturovány po vytvoření objednávky. Podobně to platí pro objednávku, která má být vyzvednuta po vytvoření objednávky. Částka splatná u hybridních objednávek je určena přidáním procenta zálohy k řádkám produktu pro vyskladnění a dodávku s plnou částkou prováděcích linek. U hybridních objednávek systém přepíná mezi režimem objednávky zákazníka a režimem Cash and Carry takto:

- Pokud mají všechny produkty v košíku hodnotu **Provádět dodávku**, objednávka bude zpracovávána jako transakce Cash and Carry.
- Pokud některé nebo všechny řádky v košíku jsou nastaveny na hodnotu **Vybrat** nebo **Expedice dodávky**, objednávka bude zpracovávána jako transakce objednávky zákazníka.

Pokud je vybrán řádek nákupního košíku a je vybraná možnost **Zvolené vyskladnění**, **Vybraná expedice**, nebo **Vyvézt vybrané**, je s touto metodu doručení nastaven pouze konkrétní řádek košíku. V takovém případě bude tok operace pokračovat obvyklým způsobem. Pokud jsou ale možnost **Zvolené vyskladnění**, **Vybraná expedice**, nebo **Vyvézt vybrané** vybrány bez výběru řádku košíku, otevře se nová stránka se seznamem všech řádků košíku. Na této obrazovce můžete vybrat více řádků najednou k nastavení způsobu dodání. Při použití této metody pro výběr řádků bude přepsána jakákoli předchozí metoda doručení, která byla přiřazena k řádku.

## <a name="additional-resources"></a>Další zdroje

[Objednávky zákazníka v Modern POS (MPOS)](customer-orders-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]