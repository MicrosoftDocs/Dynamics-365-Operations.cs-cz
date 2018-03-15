---
title: "Skupiny předmětů servisu"
description: "Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectGroups
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: fa503ac82286099a0eafc7034d169e165b538e2c
ms.contentlocale: cs-cz
ms.lasthandoff: 02/21/2018

---

# <a name="service-object-groups"></a>Skupiny předmětů servisu 

[!include[banner](../includes/banner.md)]

Použití skupin objektů je vhodné při řazení a filtrování dat o objektech pro účely sestav a statistik. Můžete například seskupit předměty podle geografického umístění nebo typu.

## <a name="group-by-geographical-location"></a>Seskupení podle geografického umístění

Tato metoda seskupení slouží k zobrazení umístění různých objektů spravovaných vaší společností. Seskupení předmětů podle geografického umístění může být vhodné například v případě, že potřebujete určit předměty, pro které již v konkrétní zemi nebo oblasti poskytuje vaše společnost servis.

## <a name="example"></a>Příklad

Odběratel z Belgie volá vaše servisní středisko s požadavkem na vytvoření servisní smlouvy pro objekt ABC. Do všech předmětů, které jsou v Belgii servisovány, jste připojili skupinu předmětů pro zeměpisné umístění Belgie. Při použití této skupiny jako filtru můžete rychle vyhledat, zda již máte záznam pro ABC v programu, nebo zda je nutné nastavit nový předmět. 

## <a name="group-by-type"></a>Seskupení podle typu

Pomocí této metody seskupení můžete zobrazit typy předmětů, pro které vaše společnost provádí servis. Seskupení předmětů může být vhodné také v případě, že chcete vytvořit nový objekt na základě podobných předmětů již existujících v daném programu.

## <a name="example"></a>Příklad

Odběratel volá s požadavkem na vytvoření servisní smlouvy pro klimatizační jednotku HIJ. Pro tento stroj již nemáte záznam. Nastavili jste však skupinu předmětů s názvem Klimatizační jednotky a přiřadili tuto skupinu ke všem předmětům klimatizačních jednotek. Proto můžete rychle vyhledávat a identifikovat všechny ostatní klimatizační jednotky a používat informace o šablonách z těchto předmětů, abyste vytvořili řádky servisní smlouvy pro HIJ. Použitím skupin předmětů tímto způsobem můžete rychle nastavit nové předměty a stanovit servisní úkoly služby, které je třeba na nich provést. 




