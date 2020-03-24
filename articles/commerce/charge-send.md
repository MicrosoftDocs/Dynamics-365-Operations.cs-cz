---
title: Expedice objednávek z jiného obchodu pomocí funkce odeslání nákladů
description: Toto téma popisuje funkci odeslání nákladů.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 0bbebcc7b2ab89bf2f5db7294acfca1d8a5ad96e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021833"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Expedice objednávek z jiného obchodu pomocí funkce odeslání nákladů

[!include [banner](includes/banner.md)]

Díky funkci odeslání nákladů v aplikaci Commerce mohou být objednávky odběratele provedeny v jednom obchodě a expedovány z jiného obchodu.

Objednávky odběratele v klientovi pokladního místa (POS) podporují více možností plnění. Některé příklady možností plnění zahrnují:

- Vyzvednutí ze stejného obchodu v jiné datum.
- Vyzvednutí z jiného obchodu ve stejné nebo jiné datum.
- Odeslání z výchozího expedičního skladu, který je přiřazen k obchodu, a doručení v určené datum.

Funkce odeslání nákladů používá následující operace POS: Expedovat všechny produkty a Expedovat vybrané produkty. To umožňuje pracovníkovi obchodu zvolit místo expedice, odkud lze plnit objednávku nebo řádek objednávky. Místo expedice ve výchozím nastavení je expediční sklad, který je přidružen k obchodu. Pracovník obchodu však může změnit toto místo a zvolit jakýkoliv obchod definovaný ve skupině lokátorů obchodů, která je přiřazená k obchodu.

Možnost vybrat adresy pro dodání zůstává nezměněna.

Způsoby dodání, které lze použít k plnění řádku objednávky, jsou založeny na konfiguraci platných způsobů dodání pro produkty a adresy. Protože pravidla pro platné způsoby dodání se udržují pouze v modulu Headquarters (HQ), klient POS zavolá v reálném čase pro načtení platných způsobů dodání pro řádek expedice.