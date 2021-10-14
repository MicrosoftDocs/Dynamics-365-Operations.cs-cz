---
title: Nastavení nákladů u mezipodnikových objednávek
description: Toto téma vysvětluje, jak nastavit náklady u mezipodnikových objednávek
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 3786df5ce185fa8433d7c69bed5bef09b4983b8b
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548153"
---
# <a name="set-up-charges-on-intercompany-orders"></a>Nastavení nákladů u mezipodnikových objednávek

[!include [banner](../../includes/banner.md)]

Podle potřeby můžete nastavit přidání nákladů do mezipodnikových objednávek. Po přidání nákladu do mezipodnikové prodejní objednávky je tento automaticky synchronizován do mezipodnikové nákupní objednávky. Tato operace funguje oběma směry – z mezipodnikové prodejní objednávky do nákupní objednávky a naopak.

Náklady můžete použít pro přičtení zisku k mezipodnikové prodejní objednávce definováním nákladů jako mezipodnikového procenta.

Při nastavení nákladů k použití u mezipodnikových objednávek povolíte výpočet interního zisku pro mezipodnikovou prodejní objednávku z čisté částky původní prodejní objednávky. Tento postup je vhodný v případě, že váš mezipodnikový dodavatel prodává za nákladovou cenu. Následující postup popisuje nastavení u mezipodnikových odběratelů. Stejný postup lze použít u dodavatelů.

1. Přejděte na **Pohledávky \> Nastavení \> Poplatky \> Skupiny poplatků zákazníků**.
1. Vytvořte skupinu nákladů.
1. Přejděte na **Pohledávky \> Odběratelé \> Všichni odběratelé**. Vyberte odkaz na účet odběratele. V podokně akcí vyberte kartu **Odběratel** a potom vyberte záložku **Prodejní objednávka**.
1. V podokně akcí vyberte **Upravit** a povolte tak úpravy pole. V poli **Skupina nákladů** vyberte skupinu mezipodnikových nákladů, kterou jste vytvořili v kroku 2.
1. Přejděte na **Pohledávky \> Nastavení \> Náklady \> Automatické náklady**.
1. Vytvořte náklady vyplněním příslušných polí.
1. V poli **Vztah odběratele** vyberte skupinu mezipodnikových nákladů, kterou jste vytvořili v kroku 2.
1. Na záložce **Řádky** v poli **Kategorie** vyberte **Mezipodnikové procento**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
