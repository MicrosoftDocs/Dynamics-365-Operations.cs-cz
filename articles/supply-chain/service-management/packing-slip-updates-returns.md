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
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7f5bf5adb603d7edb40960b70cb71e25a2f0456
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423839"
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

  


