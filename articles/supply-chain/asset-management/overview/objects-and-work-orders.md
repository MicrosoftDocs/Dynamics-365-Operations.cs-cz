---
title: Majetek a pracovní příkazy
description: Toto téma popisuje majetek a pracovní příkazy v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cddb0a25286c8ce9d72aef0b835809705ad577a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020932"
---
# <a name="assets-and-work-orders"></a>Majetek a pracovní příkazy

[!include [banner](../../includes/banner.md)]

 

Toto téma popisuje majetek a pracovní příkazy v modulu Správa majetku. Majetek a pracovní příkazy jsou ústředními částmi modulu Správa majetku. *Majetek* je stroj nebo část stroje, která vyžaduje nepřetržitou údržbu a servis. Majetek lze tvořit v hierarchické struktuře a může být spojen s funkčními místy. Úlohy údržby lze plánovat na všech úrovních struktury majetku.

Pro každý majetek jsou nastaveny různé údaje, například informace o produktu, specifikace majetku a požadované plány údržby. Následující ilustrace znázorňuje přehled dat o majetku a příslušnost majetku k typům práce. Červený text se používá pro příklady, které zobrazují dědičnost a závislosti.

![Diagram znázorňující data majetku související s typy úloh](media/05-overview-image.png)

Každý pracovní příkaz má typ pracovního příkazu, preventivní údržbu, opravnou údržbu nebo kontrolu. Pracovní příkaz obsahuje jednu nebo více úloh pracovního příkazu. Každá úloha pracovního příkazu definuje úlohu, která musí být provedena na majetku a souvisejícím typu úlohy. Příkladem souvisejících typů úloh jsou 10 000 km, 50 000 km, roční generální oprava a bezpečnostní prohlídka. Jeden pracovní příkaz může být spojen s více majetky.

Následující ilustrace znázorňuje přehled klíčových dat v pracovním příkazu.

![Diagram znázorňující klíčová data v pracovním příkazu](media/06-overview-image.png)

Pracovní příkaz může být spojen s jiným pracovním příkazem a typy úloh mohou obsahovat následující úlohy, které tvoří pracovní příkaz. Obecně neexistují žádné závislosti mezi pracovními příkazy. Proto mohou změnit stav svůj životního cyklu pracovního příkazu a mohou být naplánovány nezávisle na sobě.

Pracovní příkazy mohou být vytvářeny různými způsoby, které souvisejí s opravnou, preventivní nebo reaktivní údržbou. Pracovní příkazy lze rovněž vytvořit ručně. Následující ilustrace znázorňuje přehled procesu automatického nebo ručního vytváření pracovních příkazů.

![Diagram znázorňující automatické nebo ruční vytváření pracovních příkazů](media/07-overview-image.png)

Chcete-li naplánovat a spustit úlohu údržby v pracovním příkazu, je nutné provést několik kroků. Následující ilustrace znázorňuje přehled zpracování pracovního příkazu.

![Diagram znázorňující přehled zpracování pracovního příkazu](media/08-overview-image.png)

> [!NOTE]
> Obecně, když pracujete v aplikaci Dynamics 365 Supply Chain Management a modulu **Správa majetku**, vyberete **Nový** pro vytvoření nového záznamu, vyberete možnost **Upravit** pro aktualizaci existujícího záznamu a vyberete možnost **Uložit** pro uložení nových nebo upravených dat.
