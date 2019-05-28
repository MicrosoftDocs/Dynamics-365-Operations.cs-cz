---
title: Přeřazení dlouhodobého majetku
description: Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo.
author: saraschi2
manager: AnnBe
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df4a2fa3c1a38519da83391bcf1c4aa38b6504ff
ms.sourcegitcommit: 6890b5a372a18e11354003098a512685e339ddb0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/14/2019
ms.locfileid: "1541190"
---
# <a name="reclassify-fixed-assets"></a>Přeřazení dlouhodobého majetku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Chcete-li provést reklasifikaci dlouhodobého majetku, je nutné jej převést do nové skupiny dlouhodobého majetku nebo mu v rámci stejné skupiny přidělit nové číslo. 

Když je dlouhodobý majetek reklasifikován:

• Pro nový dlouhodobý majetek budou vytvořeny všechny knihy pro existující dlouhodobý majetek. Veškeré informace nastavené pro původní dlouhodobý majetek se zkopírují do nového dlouhodobého majetku. Stav knih původního dlouhodobého majetku je Zavřeno. 

• Nové knihy nového dlouhodobého majetku budou mít v poli **Datum pořízení** uvedeno datum reklasifikace. Datum v poli **Datum zahájení odpisu** bude zkopírováno z původních informací o majetku. Pokud již byl zahájen odpis, zobrazí se v poli **Datum posledního odpisu** datum reklasifikace. 

• Existující transakce dlouhodobého majetku pro původní dlouhodobý majetek jsou zrušeny a opětovně vytvořeny pro nový dlouhodobý majetek.

Chcete-li reklasifikovat dlouhodobý majetek, postupujte takto:

1. Přejděte na **Dlouhodobý majetek > Pravidelné úlohy > Reklasifikace.**
2. V poli **Skupina dlouhodobého majetku** zvolte skupinu, která má být reklasifikována.
3. V poli **Číslo dlouhodobého majetku** zvolte dlouhodobý majetek určený k reklasifikaci.
4. V poli **Nová skupina dlouhodobého majetku** vyberte skupinu, do které chcete dlouhodobý majetek převést.
    * Jestliže je nová skupina dlouhodobého majetku přiřazena k číselné řadě, pole **Nové číslo dlouhodobého majetku** se aktualizuje číslem z číselné řady nové skupiny dlouhodobého majetku. V opačném případě se pole **Nové číslo dlouhodobého majetku** aktualizuje číslem z číselné řady, která je nastavena na stránce **Parametry dlouhodobého majetku**. Pokud na stránce **Parametry dlouhodobého majetku** není nastavena číselná řada, zadejte číslo do pole **Nové číslo dlouhodobého majetku**.  
5. Do pole **Datum reklasifikace** zadejte datum.
6. V poli **Číselná řada dokladů** zadejte nebo vyberte hodnotu.
7. Klikněte na tlačítko **OK**.
