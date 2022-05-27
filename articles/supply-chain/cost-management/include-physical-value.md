---
title: Zahrnovat fyzickou hodnotu
description: Pole Zahrnout fyzickou hodnotu na pevné záložce Skladový model na stránce Skupiny modelů položky se používá k určení toho, zda se fyzicky aktualizované transakce promítnou do výpočtu průběžných průměrných nákladových ceny položky.
author: JennySong-SH
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fb7a2a401bd7900555646c3ff0e1be9bf4a50d3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672395"
---
# <a name="include-physical-value"></a>Zahrnovat fyzickou hodnotu

[!include [banner](../includes/banner.md)]

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

**Příklad 1:** Označíte pole **Zahrnovat fyzickou hodnotu** a obdržíte následující nákupní objednávky:

-   Nákupní objednávka na 2 kusy v ceně 10,00 USD byla aktualizována podle dodacího listu.
-   Nákupní objednávka na 3 kusy v ceně 12,00 USD byla aktualizována podle faktury.

V tomto případě bude průběžná průměrná nákladová cena 11,20 USD(2x10+3x12)/(2+3), protože při výpočtu nákladové ceny jsou použity fyzicky i finančně aktualizované transakce. 

**Příklad 2:** Neoznačíte pole **Zahrnovat fyzickou hodnotu** a nákladová cena v rámci konfigurace položky je 10,00 USD. 

-   Obdržíte nákupní objednávku na 20 kusů v ceně 12,00 USD, která byla aktualizována podle dodacího listu.

Při zaúčtování prodejní objednávky se zaúčtuje částka nákladů 10,00 USD, protože průběžná průměrná nákladová cena nebude zahrnovat fyzicky zaúčtované transakce. 

> [!NOTE]
> Pokud pro porovnání označíte pole **Zahrnovat fyzickou hodnotu** pro toto zboží při zaúčtování prodejní objednávky, zaúčtované náklady budou 12,00 USD.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]