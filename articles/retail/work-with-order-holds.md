---
title: "Blokování objednávky"
description: "Toto téma popisuje blokování objednávek v aplikaci Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: c0c0e9a0f863eb33d544f63e40e0531cdaaf6426
ms.contentlocale: cs-cz
ms.lasthandoff: 06/20/2017

---

# <a name="order-holds"></a>Blokování objednávky

[!include[banner](includes/banner.md)]


Toto téma popisuje blokování objednávek v aplikaci Dynamics 365 for Retail.

Objednávky mohou být blokovány z různých důvodů. Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele. Během prodejního procesu se stává, že prodejní objednávky musí být blokovány. Například prodejní objednávka může být blokována kvůli potížím s platbou odběratele kvůli podezření z podvodu nebo kvůli nutné kontrole správcem. Při blokování prodejní objednávky můžete určit důvody pro blokování prodejní objednávky přiřazením kódu prodejní objednávce. Kódy blokování prodejních objednávek se konfigurují v nabídce **Prodej a marketing** &gt; **Konfigurace** &gt; **Prodejní objednávky** &gt; **Kódy blokování objednávek**. Prodejní objednávku můžete blokovat ručně v době vytvoření objednávky nebo později. Navíc objednávku můžete blokovat automaticky na základě pravidel o podvodu. Zatímco je prodejní objednávka blokována, může ji aktualizovat dalšími informacemi. Případně můžete zkontrolovat prodejní objednávku, a pokračovat v práci na ní. Prodejní objednávku můžete zkontrolovat, zkontrolovat ji po přijetí, a dokonce i přebít kontrolu jiným uživatelem pomocí pracovní plochy pro blokování objednávky (**Maloobchodní prodej** &gt; **Odběratelé** &gt; **Blokování objednávek**). Když je objednávka hotová k dokončení, je nutné odebrat blokování před dokončením zpracování objednávek.



