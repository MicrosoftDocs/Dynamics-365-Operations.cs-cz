---
title: Aktualizace dodacího listu pro vrácení
description: Před přijetím vrácených položek na sklad je nutné aktualizovat dodací list objednávky, do které náleží.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 446306237492df22e98dc1efee2bc1542cdab1ea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202185"
---
# <a name="packing-slip-updates-for-returns"></a>Aktualizace dodacího listu pro vrácení  

[!include [banner](../includes/banner.md)]


Před přijetím vrácených položek na sklad je nutné aktualizovat dodací list objednávky, do které náleží. Stejně jako je proces aktualizace faktury aktualizací finanční transakce, proces aktualizace dodacího listu je fyzickou aktualizací skladového záznamu a potvrzuje tedy změny zásob. V případě vrácení jsou kroky přiřazené k dispoziční akci implementovány v průběhu aktualizace dodacího listu.

Aktualizaci dodacího listu lze zpracovat buď v deníku doručení položek, nebo ve vratce.

Jako součást procesu účtování dodacích listů lze volitelně přiřadit referenční číslo dodacího listu z přepravních dokumentů odběratele k řádkům objednávky. Toto přiřazení je nepovinné a má pouze informativní charakter. Nevytváří žádné aktualizace transakcí.

Pokud nebyly dodány všechny očekávané vrácené položky, měli byste zadat pouze množství obdržené v aktualizaci dodacího listu. Ponechte zbývající položky na objednávce, dokud nebudou dodána zbylá část vrácené dodávky.

Při odeslání položky zpět z karantény do oddělení expedice a příjmu, například pokud karanténní inspektor neobdrží informace k uložení položek na skladu, je dále nutné aktualizovat odpovídající dodací list, aby došlo ke správné registraci a reakci na dispoziční kód, který byl zadán jako výsledek karantény.

Při aktualizaci dodacího listu pro vrácenou položku, která pochází z prodejní smlouvy, je závazek prodejní smlouvy pro danou položku automaticky aktualizován tak, aby odrážel změnu množství nebo částky. 

## <a name="see-also"></a>Viz také

[Provádění aktualizací faktur pro vrácení](perform-invoice-updates-for-returns.md)

  


