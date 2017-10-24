---
title: "Konfigurační pravidla"
description: "Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 72395b5068f0893d79be6f8095dae988c224d0aa
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="configuration-rules"></a>Konfigurační pravidla

[!include[banner](../includes/banner.md)]


Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.

Konfigurační pravidla jsou k dispozici při definování modelů konfigurace založené na dimenzích. Konfigurační pravidla se používají k vynucení nebo zakázání kombinace specifických položek v kusovníku. Poté, co byl vytvořen kusovník, a příslušné položky byly přiřazeny k jejich odpovídajícím konfiguračním skupinám, lze definovat jedno nebo více konfiguračních pravidel. Pokud dvě položky patří dohromady, operátor **Vybrat** slouží k jejich zařazení. Pokud se dvě položky vzájemně vylučují, operátor **Zrušit výběr** slouží k jejich vyloučení.  

**Poznámka:** Tyto informace se týkají pouze základních produktů, které používají konfiguraci založenou na dimenzích.  

Stávající konfigurace nejsou následnými změnami konfiguračních pravidel ovlivněny. Je však důležité tato pravidla stanovit před definováním nové konfigurace nebo je zkontrolovat, jestliže si myslíte, že došlo ke změně pravidel.  

**Poznámka:** Metoda **Vybrat** znamená, že odvozená konfigurační skupina, číslo položky a konfigurace se vyberou automaticky. Metoda **Zrušit výběr** znamená, že odvozenou konfigurační skupinu, číslo položky a konfiguraci nelze vybrat.

<a name="see-also"></a>Viz také
--------

[Konfigurace produktu založené na dimenzích](dimension-based-product-configuration.md)




