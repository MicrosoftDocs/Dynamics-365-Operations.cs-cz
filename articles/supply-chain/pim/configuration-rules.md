---
title: Konfigurační pravidla
description: Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e70713fb25584e26f97bcb7c769da6954aa36b81
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423476"
---
# <a name="configuration-rules"></a>Konfigurační pravidla

[!include [banner](../includes/banner.md)]

Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.

Konfigurační pravidla jsou k dispozici při definování modelů konfigurace založené na dimenzích. Konfigurační pravidla se používají k vynucení nebo zakázání kombinace specifických položek v kusovníku. Poté, co byl vytvořen kusovník, a příslušné položky byly přiřazeny k jejich odpovídajícím konfiguračním skupinám, lze definovat jedno nebo více konfiguračních pravidel. Pokud dvě položky patří dohromady, operátor **Vybrat** slouží k jejich zařazení. Pokud se dvě položky vzájemně vylučují, operátor **Zrušit výběr** slouží k jejich vyloučení.  

**Poznámka:** Tyto informace se týkají pouze základních produktů, které používají konfiguraci založenou na dimenzích.  

Stávající konfigurace nejsou následnými změnami konfiguračních pravidel ovlivněny. Je však důležité tato pravidla stanovit před definováním nové konfigurace nebo je zkontrolovat, jestliže si myslíte, že došlo ke změně pravidel.  

**Poznámka:** Metoda **Vybrat** znamená, že odvozená konfigurační skupina, číslo položky a konfigurace se vyberou automaticky. Metoda **Zrušit výběr** znamená, že odvozenou konfigurační skupinu, číslo položky a konfiguraci nelze vybrat.

<a name="additional-resources"></a>Další zdroje
--------

[Přehled konfigurace produktu založeného na dimenzích](dimension-based-product-configuration.md)



