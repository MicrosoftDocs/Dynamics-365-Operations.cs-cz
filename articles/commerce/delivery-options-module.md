---
title: Modul možností doručení
description: Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661192"
---
# <a name="delivery-options-module"></a>Modul možností doručení

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Toto téma popisuje moduly možností dodání a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Moduly možností doručení umožňují zákazníkům vybrat způsob doručení, jako je například dopravce nebo vyzvednutí pro jejich online objednávku. Pro určení způsobu doručení je vyžadována dodací adresa. Pokud se změní dodací adresa, je nutné znovu načíst možnosti dodání. Pokud objednávka obsahuje pouze položky, které budou vydány v obchodě, bude tento modul automaticky skrytý.

Informace o tom, jak konfigurovat režimy doručení, naleznete v části [Nastavení online kanálu](channel-setup-online.md) a [Nastavení způsobů dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Každý režim dodání může mít související poplatek. Informace o tom, jak nakonfigurovat náklady pro online obchod, naleznete v tématu [Omnikanál – pokročilé automatické náklady](omni-auto-charges.md).

V Commerce verze 10.0.13 byl aktualizován modul voleb doručení, aby podporoval **Náklady záhlaví bez proměrného** a **Doprava jako náklad řádku** funkce. Pokud je prorace vypnutá, očekává se, že pracovní postup elektronického obchodování neumožňuje smíšený způsob doručení pro položky v košíku (to znamená, že některé položky jsou vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí). **Náklady záhlaví bez proměrného** funkce vyžaduje, aby **Povolit konzistentní zpracování způsobu doručení v kanálu** vlajka zapnuta v centrále Commerce. Pokud je funkce zapnuta, bude přepravní poplatky budou účtovány buď na úrovni záhlaví, nebo úrovni řádku, podle konfigurace centrály Commerce.

Téma Fabrikam podporuje smíšený způsob doručení, kdy jsou některé položky vybrány pro odeslání, jiné jsou vybrány pro vyzvednutí. V tomto režimu budou poplatky za přepravu poměrné pro všechny položky, které jsou vybrány pro způsob doručení. Aby smíšený režim doručení fungoval, musíte nejprve nakonfigurovat **Náklady záhlaví s proměrným** funkci v centrále Commerce. Další informace o této konfiguraci naleznete v části [Poměrné poplatky za záhlaví odpovídají řádkům prodeje](pro-rate-charges-matching-lines.md).

Pokud se na řádkové položky vztahují poplatky za dopravu, mohou být pro každou položku zobrazeny v řádku košíku. Tato funkce vyžaduje, aby **Zobrazit poplatky pro položky řádku** vlastnost byla zapnuta jak pro zboží pro modul košíku i modul pokladny. Další informace viz [Modul košíku](add-cart-module.md) a [Modul pokladny](add-checkout-module.md).

Následující obrázek ukazuje příklad modulu možností dodání na stránce pokladny.

![Příklad modulu možností dodání na stránce pokladny](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a>Vlastnosti modulu možností dodání

| Vlastnost | Hodnoty | popis |
|----------|--------|-------------|
| Záhlaví | Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**) | Volitelný nadpis pro modul možností dodání. |
| Vlastní název třídy CSS | Text | Vlastní název třídy kaskádových stylů (CSS), ktera bude použita k vykreslení tohoto modulu, je-li to relevantní. |
| Možnost režimu filtrování doručení | **Nefiltrovat** nebo **Režimy bez dopravy** | Hodnota, která určuje, zda by modul voleb doručení měl odfiltrovat všechny režimy doručení bez dodání. |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a>Na stránku pokladny přidejte modul dodání a nastavte požadované vlastnosti.

Modul možností dodání lze přidat pouze do modulu pokladny. Další informace o konfiguraci modulu voleb dodání a jeho přidání na stránku pokladny naleznete na stránce [Modul pokladny](add-checkout-module.md).

## <a name="additional-resources"></a>Další prostředky

[Modul košíku](add-cart-module.md)

[Modul pokladny](add-checkout-module.md)

[Modul platby](payment-module.md)

[Modul dodací adresy](ship-address-module.md)

[Modul podrobností objednávky](order-confirmation-module.md)

[Modul dárkového poukazu](add-giftcard.md)

[Nastavení online kanálu](channel-setup-online.md)

[Omnikanálové rozšířené automatické náklady](omni-auto-charges.md)

[Poměrné rozdělení nákladů záhlaví na odpovídající řádky prodeje](pro-rate-charges-matching-lines.md)

[Nastavit způsoby dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
