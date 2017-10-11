---
title: "Blokování zásob"
description: "Tento článek obsahuje přehled informací o blokování zásob, které je součástí vlastního procesu kontroly kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Blokování zásob můžete použít pro zabránění zpracování nebo spotřeby položek."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventBlocking, InventQualityOrderTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2094
ms.assetid: 1968e32f-eff9-4c17-8f7f-a870f0c38fbc
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7d00aaa272de32d4ef2082bf1822125800ca8a1e
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="inventory-blocking"></a>Blokování zásob

[!include[banner](../includes/banner.md)]


Tento článek obsahuje přehled informací o blokování zásob, které je součástí vlastního procesu kontroly kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Blokování zásob můžete použít pro zabránění zpracování nebo spotřeby položek.

Skladové položky lze blokovat následujícími způsoby:
-   Ručně
-   Vytvořením objednávky kvality.
-   Pomocí procesu, který generuje objednávku kvality.
-   Použitím blokování stavu zásob

## <a name="blocking-items-manually"></a>Ruční blokování položek
Množství položky je možné blokovat tak, že vytvoříte transakci na stránce **Blokování zásob**. Blokovat lze ručně pouze zboží, které je dostupné na skladě. Při ručním blokování množství je nutné zvážit, zda budou do plánování aktivit zahrnuty očekávané příjmy jako očekávané množství na skladě. Očekávané příjmy jsou blokované položky, u nichž je očekávána dostupnost ve skladu po dokončení kontroly. Očekávané datum můžete spravovat. Standardně je vybrána možnost **Očekávané příjmy** pro položky, které jsou zablokovány pomocí objednávky kvality. Ruční blokování množství lze zrušit odstraněním transakce na stránce **Blokování zásob**.

## <a name="blocking-items-by-creating-a-quality-order"></a>Blokování položek vytvořením objednávky kvality
Je možné zadání položek, které musí být kontrolovány pro vytváření objednávky kvality na stránce **Objednávky kvality**. Při vytváření objednávky kvality je blokováno množství položek, které zadáte. Plán vzorkování, který je spojený s objednávkou kvality, řídí pouze množství položek, které musí být zkontrolovány, nikoli množství, které je blokováno. Bez ohledu na množství, které bude odesláno ke kontrole podle plánu vzorkování, bude blokováno množství položek, které je zadáno v objednávce kvality.

## <a name="blocking-items-by-using-a-process-that-generates-a-quality-order"></a>Blokování položek pomocí procesu, který generuje objednávku kvality
Pokud množství položek uvádí, že je nutné položku zkontrolovat, je množství položek blokováno automaticky. Proto při automatickém generování objednávky kvality řídí vzorkovací položka, která je spojena s objednávkou kvality, počet blokovaných položek a nejen množství položek, které budou zkontrolovány. Je-li vybrána možnost **Úplné blokování** na stránce **Vzorkování položek**, celé množství, například řádek nákupní objednávky, bude blokováno při inventuře bez ohledu na množství vzorkování položky.
### <a name="example"></a>Příklad

V následujícím příkladu je generována objednávka kvality po zaúčtování dodacího listu k nákupní objednávce. Na stránce **Přiřazení kvality** jste uvedli, že zaúčtování dodacího listu nákupní objednávky je proces, který aktivuje objednávku kvality.

|Nastavení                                                                     |Uživatelská akce                 |Výsledek             |
|--------------------------------------------------------------------------|----------------------------|-------------------|
| Přiřazení kvality určuje, že při zaúčtování dodacího listu nákupní objednávky musí být vygenerovaná objednávky kvality. Nastavení vzorkování položky objednávky kvality určuje, že musí být zkontrolováno 10 % z počtu řádků nákupní objednávky. Kromě toho vybraná možnost **Úplné blokování** v nastavení položky vzorkování značí, že musí být blokován celý počet řádků nákupní objednávky při inventuře bez ohledu na množství, které je odesláno ke kontrole. | Dodací list bude zaúčtován. | Objednávka kvality bude vygenerována. 10 % z množství položky na nákupní objednávce bude odesláno ke kontrole. Plný počet řádků nákupní objednávky bude blokován. |

## <a name="blocking-items-by-using-inventory-status-blocking"></a>Blokování položek použitím blokování stavu zásob
Můžete určit, jaké stavy zásob jsou stavy blokování, pomocí parametru **Blokování zásob** na stránce **Stavy zásob**.  Stavy zásob nelze použít jako stavy blokování pro výrobní zakázky, prodejní objednávky, převodní příkazy, výstupní transakce nebo integrace projektu. Pro výstupní práci používejte položky, které mají stav zásob „dostupné“. Pokud máte položky se stavem **Zničeno** a použijete u těchto položek hlavní plánování, položky budou považovány za chybějící a sklad se automaticky doplní.



<a name="see-also"></a>Viz také
--------

[Vytvoření a správa blokování zásob (Průvodce záznamem úloh)](/dynamics365/unified-operations/supply-chain/inventory/tasks/create-maintain-inventory-blocking)

[Procesy správy kvality](quality-management-processes.md)

[Kontrola kvality zboží (průvodce záznamem úloh)](/dynamics365/unified-operations/supply-chain/inventory/tasks/inspect-quality-goods)
