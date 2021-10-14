---
title: Konfigurační pravidla
description: Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.
author: t-benebo
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ddc74777ae0cde5367667f93eb29ffb21531e02
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570770"
---
# <a name="configuration-rules"></a>Konfigurační pravidla

[!include [banner](../includes/banner.md)]

Tento článek obsahuje obecné informace o pravidlech konfigurace. Konfigurační pravidla definují vztah mezi položkami v kusovníku pro produkty, které používají technologii konfigurace založené na dimenzích.

Konfigurační pravidla jsou k dispozici při definování modelů konfigurace založené na dimenzích. Konfigurační pravidla se používají k vynucení nebo zakázání kombinace specifických položek v kusovníku. Poté, co byl vytvořen kusovník, a příslušné položky byly přiřazeny k jejich odpovídajícím konfiguračním skupinám, lze definovat jedno nebo více konfiguračních pravidel. Pokud dvě položky patří dohromady, operátor **Vybrat** slouží k jejich zařazení. Pokud se dvě položky vzájemně vylučují, operátor **Zrušit výběr** slouží k jejich vyloučení.  

**Poznámka:** Tyto informace se týkají pouze základních produktů, které používají konfiguraci založenou na dimenzích.  

Stávající konfigurace nejsou následnými změnami konfiguračních pravidel ovlivněny. Je však důležité tato pravidla stanovit před definováním nové konfigurace nebo je zkontrolovat, jestliže si myslíte, že došlo ke změně pravidel.  

**Poznámka:** Metoda **Vybrat** znamená, že odvozená konfigurační skupina, číslo položky a konfigurace se vyberou automaticky. Metoda **Zrušit výběr** znamená, že odvozenou konfigurační skupinu, číslo položky a konfiguraci nelze vybrat.

## <a name="additional-resources"></a>Další zdroje

[Přehled konfigurace produktu založeného na dimenzích](dimension-based-product-configuration.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]