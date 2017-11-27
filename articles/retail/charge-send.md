---
title: "Dodání objednávky z jiného obchodu"
description: "Toto téma popisuje funkci odeslání nákladů."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail Version
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: cs-cz
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Dodání objednávky z jiného obchodu

Díky funkci odeslání nákladů v aplikaci Dynamics 365 for Retail mohou být objednávky odběratele provedeny v jednom obchodě a expedovány z jiného obchodu. Objednávky odběratele v klientovi pokladního místa (POS) podporují více možností plnění. Některé příklady možností plnění zahrnují:
-   Vyzvednutí ze stejného obchodu v jiné datum.
-   Vyzvednutí z jiného obchodu ve stejné nebo jiné datum.
-   Odeslání z výchozího expedičního skladu, který je přiřazen k obchodu, a doručení v určené datum.

Funkce odeslání nákladů používá následující operace POS: Expedovat všechny produkty a Expedovat vybrané produkty. To umožňuje pracovníkovi obchodu zvolit místo expedice, odkud lze plnit objednávku nebo řádek objednávky. Místo expedice ve výchozím nastavení je expediční sklad, který je přidružen k obchodu. Pracovník obchodu však může změnit toto místo a zvolit jakýkoliv obchod definovaný ve skupině lokátorů obchodů, která je přiřazená k obchodu. 

Možnost vybrat adresy pro dodání zůstává nezměněna. 

Způsoby dodání, které lze použít k plnění řádku objednávky, jsou založeny na konfiguraci platných způsobů dodání pro produkty a adresy. Protože pravidla pro platné způsoby dodání se udržují pouze v modulu Retail headquarters (HQ), klient POS zavolá v reálném čase pro načtení platných způsobů dodání pro řádek expedice. 


