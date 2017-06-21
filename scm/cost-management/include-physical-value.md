---
title: Zahrnovat fyzickou hodnotu
description: "Pole Zahrnout fyzickou hodnotu na pevné záložce Skladový model na stránce Skupiny modelů položky se používá k určení toho, zda se fyzicky aktualizované transakce promítnou do výpočtu průběžných průměrných nákladových ceny položky."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 2d45e7a56851f3f4ac7a7d2d8c4ca9f23b6535fc
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="include-physical-value"></a>Zahrnovat fyzickou hodnotu

[!include[banner](../includes/banner.md)]


Pole Zahrnout fyzickou hodnotu na pevné záložce Skladový model na stránce Skupiny modelů položky se používá k určení toho, zda se fyzicky aktualizované transakce promítnou do výpočtu průběžných průměrných nákladových ceny položky.

Zaškrtávací pole **Zahrnovat fyzickou hodnotu** má následující hodnoty.

| Hodnota    | Výsledek                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Vybrané | Při výpočtu průběžné průměrné nákladové ceny jsou použity fyzicky i finančně aktualizované transakce. |
| Proplaceno  | Pouze finančně aktualizované transakce jsou použity pro výpočet průběžné průměrné nákladové ceny.                                     |

Toto políčko má účinky, které se liší v závislosti na skladovém modelu, který používáte.

-   Označíte-li pole **Zahrnout fyzickou hodnotu** při použití metody FIFO, LIFO nebo skladového modelu s datem LIFO, uzávěrka skladu provede také úpravy u fyzicky aktualizovaných transakcí.
-   Pokud jste pro tyto skladové modely neoznačili políčko **Zahrnovat fyzickou hodnotu**, budou při uzávěrce skladu provedena vyrovnání pouze pro finančně aktualizované transakce.
-   Pokud použijete skladové modely s použitím váženého průměru nebo data váženého průměru, budou při uzávěrce skladu vyrovnány pouze finančně aktualizované transakce, bez ohledu na to, zda je zaškrtnuto políčko **Zahrnovat fyzickou hodnotu**, či nikoli.

**Příklad 1:** Označíte pole**Zahrnovat fyzickou hodnotu** a obdržíte následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla aktualizována podle dodacího listu
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla aktualizována podle faktury

V tomto případě bude průběžná průměrná nákladová cena 11,20 USD, protože při výpočtu nákladové ceny jsou použity fyzicky i finančně aktualizované transakce. **Příklad 2:** Neoznačíte pole **Zahrnovat fyzickou hodnotu** a nákladová cena v rámci konfigurace položky je 10,00 USD. Obdržíte nákupní objednávku na 20 kusů v ceně 12,00 USD, která byla aktualizována podle dodacího listu. Při zaúčtování prodejní objednávky se zaúčtuje částka nákladů 10,00 USD, protože průběžná průměrná nákladová cena nebude zahrnovat fyzicky zaúčtované transakce. **Poznámka:** Pokud pro porovnání označíte pole **Zahrnovat fyzickou hodnotu** pro toto zboží při zaúčtování prodejní objednávky, zaúčtované náklady budou 12,00 USD.




