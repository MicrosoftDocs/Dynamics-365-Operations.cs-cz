---
title: "Blokování objednávky"
description: "Toto téma popisuje blokování objednávek v aplikaci Dynamics AX pomocí kategorie Maloobchodní a velkoobchodní prodej."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 1cb18e3275b8dcdf0a61531ee056995f6e8fbc8d
ms.lasthandoff: 03/31/2017


---

# <a name="order-holds"></a>Blokování objednávky

[!include[banner](includes/banner.md)]


Toto téma popisuje blokování objednávek v aplikaci Dynamics AX pomocí kategorie Maloobchodní a velkoobchodní prodej.

Objednávky mohou být blokovány z různých důvodů. Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele. Během prodejního procesu se stává, že prodejní objednávky musí být blokovány. Například prodejní objednávka může být blokována kvůli potížím s platbou odběratele kvůli podezření z podvodu nebo kvůli nutné kontrole správcem. Při blokování prodejní objednávky můžete určit důvody pro blokování prodejní objednávky přiřazením kódu prodejní objednávce. Kódy blokování prodejní objednávky, které jsou nakonfigurovány na **prodeje a marketingu**&gt;**nastavení**&gt;**prodejní objednávky**&gt;**objednávka obsahuje kódy**. Prodejní objednávku můžete blokovat ručně v době vytvoření objednávky nebo později. Navíc objednávku můžete blokovat automaticky na základě pravidel o podvodu. Zatímco je prodejní objednávka blokována, může ji aktualizovat dalšími informacemi. Případně můžete zkontrolovat prodejní objednávku, a pokračovat v práci na ní. Můžete rezervovat prodejní objednávky, zkontrolujte jej a dokonce Přepsat rezervaci jiného uživatele v pořadí podle držení workbench (**maloobchodní a commerce**&gt;**zákazníci**&gt;**nařídit blokování**). Když je objednávka hotová k dokončení, je nutné odebrat blokování před dokončením zpracování objednávek.




