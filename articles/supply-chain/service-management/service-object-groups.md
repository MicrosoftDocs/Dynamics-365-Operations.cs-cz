---
title: Skupiny předmětů servisu
description: Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik.
author: sorenva
ms.date: 05/11/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b53d51e4165797b176cfe70a8e25311e41d2999e
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674750"
---
# <a name="service-object-groups"></a>Skupiny předmětů servisu

[!include [banner](../includes/banner.md)]

Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik. Můžete například seskupit předměty podle geografického umístění nebo typu.

## <a name="group-by-geographical-location"></a>Seskupení podle geografického umístění

Tato metoda seskupení slouží k zobrazení umístění různých objektů spravovaných vaší společností. Seskupení předmětů podle geografického umístění může být vhodné například v případě, že potřebujete určit předměty, pro které již v konkrétní zemi nebo oblasti poskytuje vaše společnost servis.

## <a name="example-of-grouping-by-geographical-location"></a>Příklad seskupení podle geografického umístění

Odběratel z Belgie volá vaše servisní středisko s požadavkem na vytvoření servisní smlouvy pro objekt ABC. Do všech předmětů, které jsou v Belgii servisovány, jste připojili skupinu předmětů pro zeměpisné umístění Belgie. Při použití této skupiny jako filtru můžete rychle vyhledat, zda již máte záznam pro ABC v programu, nebo zda je nutné nastavit nový předmět.

## <a name="group-by-type"></a>Seskupení podle typu

Pomocí této metody seskupení můžete zobrazit typy předmětů, pro které vaše společnost provádí servis. Seskupení předmětů může být vhodné také v případě, že chcete vytvořit nový objekt na základě podobných předmětů již existujících v daném programu.

## <a name="example-of-grouping-by-type"></a>Příklad seskupení podle typu

Odběratel volá s požadavkem na vytvoření servisní smlouvy pro klimatizační jednotku HIJ. Pro tento stroj již nemáte záznam. Nastavili jste však skupinu předmětů s názvem Klimatizační jednotky a přiřadili tuto skupinu ke všem předmětům klimatizačních jednotek. Proto můžete rychle vyhledávat a identifikovat všechny ostatní klimatizační jednotky a používat informace o šablonách z těchto předmětů, abyste vytvořili řádky servisní smlouvy pro HIJ. Použitím skupin předmětů tímto způsobem můžete rychle nastavit nové předměty a stanovit servisní úkoly služby, které je třeba na nich provést.

## <a name="create-service-object-groups"></a>Vytvoření skupin předmětů servisu

Vytvoření skupin, kterým lze přiřazovat předměty servisu. Servisní předměty jsou skladové položky a další produkty, u kterých se provádějí servis. Vložením předmětů servisu do skupin můžete vytvářet sestavy pro podobné a související předměty servisu. Skupina předmětů servisu může například obsahovat dva předměty servisu: jeden předmět servisu je sada a druhý předmět servisu je služba umožňující nainstalovat sadu.

Pro vytvoření skupin předmětů servisu postupujte takto:

1. Klikněte na **Správa servisu > Nastavení > Předměty servisu > Skupiny předmětů servisu**.

2. Kliknutím na možnost **Nový** vytvořte novou skupinu předmětů servisu.

3. Zadejte pro skupinu předmětů servisu jedinečný název a volitelně také popis.

Předměty servisu lze přiřadit ke skupině pomocí formuláře **Předměty servisu** . 

## <a name="see-also"></a>Viz také

[Tvorba předmětů servisu](create-service-objects.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]